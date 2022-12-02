---
title: Desenvolupament de plantilles de projecte amb la característica Copia el projecte
description: En aquest article es proporciona informació sobre com crear plantilles de projecte mitjançant l'acció personalitzada Copia el projecte.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923820"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolupament de plantilles de projecte amb la característica Copia el projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Dynamics 365 Project Operations és compatible amb la capacitat de copiar un projecte i revertir les assignacions als recursos genèrics que representen la funció. Els clients poden utilitzar aquesta funcionalitat per crear plantilles de projecte bàsiques.

Quan seleccioneu **Copia el projecte**, l'estat del projecte de destinació s'actualitza. Utilitzeu **Raó per a l'estat** per determinar quan ha finalitzat l'acció de còpia. En seleccionar **Copia el projecte** també s'actualitza la data d'inici del projecte a la data d'inici actual si no es detecta cap data de la destinació a l'entitat del projecte de destinació.

## <a name="copy-project-custom-action"></a>Acció personalitzada Copia el projecte

### <a name="name"></a>Nom 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Paràmetres d’entrada

Hi ha tres paràmetres d'entrada:

- **ReplaceNamedResources** o **ClearTeamsAndAssignments**: definiu només una de les opcions. No els definiu tots dos.

    - **\{"ReplaceNamedResources":true\}**: comportament per defecte del Project Operations. Els recursos amb nom se substitueixen per recursos genèrics.
    - **\{"ClearTeamsAndAssignments":true\}**: el comportament per defecte del Project for the Web. Totes les assignacions i els membres de l'equip se suprimeixen.

- **SourceProject**: referència de l'entitat del projecte d'origen del qual es copiarà. Aquest paràmetre no pot ser nul.
- **Target**: referència de l'entitat del projecte de destinació al qual es copiarà. Aquest paràmetre no pot ser nul.

La taula següent ofereix un resum dels tres paràmetres.

| Paràmetre                | Type             | Valor                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Boolean          | **True** o **False** |
| ClearTeamsAndAssignments | Boolean          | **True** o **False** |
| SourceProject            | Referència d’entitat | El projecte d'origen    |
| Meta                   | Referència d’entitat | El projecte de destinació    |

Per veure més valors per defecte a les accions, vegeu [Utilitzar les accions de l'API web](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Validacions

Es fan les validacions següents.

1. Comprova els valors nuls i recupera els projectes d'origen i de destinació per confirmar l'existència d'ambdós projectes a l'organització.
2. El sistema valida que el projecte de destinació és vàlid per copiar verificant les condicions següents:

    - Al projecte no hi ha cap activitat anterior (incloent-hi la selecció de la pestanya **Tasques**) i es crea el projecte.
    - No hi ha cap còpia prèvia, no s'ha sol·licitat cap importació en aquest projecte i el projecte no té un estat **Amb error**.

3. No es crida l'operació mitjançant HTTP.

## <a name="specify-fields-to-copy"></a>Especificar els camps que es copiaran

Quan es crida l'acció, **Copia el projecte** consultarà la visualització del projecte **Copia les columnes del projecte** per determinar quins camps s'han de copiar quan es copia el projecte.

### <a name="example"></a>Exemple

A l'exemple següent es mostra com es crida l'acció personalitzada **CopyProjectV3** amb el conjunt de paràmetres **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
