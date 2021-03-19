---
title: Desenvolupament de plantilles de projecte amb la característica Copia el projecte
description: En aquest tema es proporciona informació sobre com crear plantilles de projecte mitjançant l'acció personalitzada Copia el projecte.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 27847575e2d6ec9af77d24f756b13d3aeb0efea7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286911"
---
# <a name="develop-project-templates-with-copy-project"></a>Desenvolupament de plantilles de projecte amb la característica Copia el projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations és compatible amb la capacitat de copiar un projecte i revertir les assignacions als recursos genèrics que representen la funció. Els clients poden utilitzar aquesta funcionalitat per crear plantilles de projecte bàsiques.

Quan seleccioneu **Copia el projecte**, l'estat del projecte de destinació s'actualitza. Utilitzeu **Raó per a l'estat** per determinar quan ha finalitzat l'acció de còpia. En seleccionar **Copia el projecte** també s'actualitza la data d'inici del projecte a la data d'inici actual si no es detecta cap data de la destinació a l'entitat del projecte de destinació.

## <a name="copy-project-custom-action"></a>Acció personalitzada Copia el projecte 

### <a name="name"></a>Nom 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Paràmetres d’entrada
Hi ha tres paràmetres d'entrada:

| Paràmetre          | Type   | Valors                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** o **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Referència d’entitat | Projecte d'origen |
| Objectiu             | Referència d’entitat | Projecte de destinació |


- **{"clearTeamsAndAssignments":true}** : comportament per defecte d'un projecte per al web, i suprimirà totes les assignacions i membres de l'equip.
- **{"removeNamedResources":true}** comportament per defecte del Project Operations, i revertirà les assignacions a recursos genèrics.

Per veure més valors per defecte en accions, vegeu [Utilitzar les accions de l'API web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Especificar els camps que es copiaran 
Quan es crida l'acció, **Copia el projecte** consultarà la visualització del projecte **Copia les columnes del projecte** per determinar quins camps s'han de copiar quan es copia el projecte.


### <a name="example"></a>Exemple
A l'exemple següent es mostra com es truca a l'acció personalitzada **CopyProject** amb el conjunt de paràmetres **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]