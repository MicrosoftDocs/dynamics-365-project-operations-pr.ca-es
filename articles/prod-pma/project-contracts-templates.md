---
title: Sincronitzar els contractes del projecte i els projectes directament des del Project Service Automation al Finance and Operations
description: Aquest tema descriu la plantilla i tasques subjacents que s'utilitzen per sincronitzar els contractes del projecte i els projectes directament des del Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0b3bc159fff25c4f6e5b1ed1b2eabbba675fb0f5
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642621"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Sincronitzar els contractes del projecte i els projectes directament des del Project Service Automation al Finance and Operations

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Aquest tema descriu la plantilla i tasques subjacents que s'utilitzen per sincronitzar els contractes del projecte i els projectes directament des del Dynamics 365 Project Service Automation al Dynamics 365 Finance.

> [!NOTE] 
> Si utilitzeu l'Enterprise Edition 7.3.0, heu d'instal·lar el KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de dades del Project Service Automation al Finance

> [!NOTE]
> Per poder utilitzar la solució d'integració del Project Service Automation al Finance, heu d'estar familiaritzat amb la característica d'integració de dades del Dynamics 365.

La solució d'integració del Project Service Automation al Finance utilitza la característica d'integració de dades per sincronitzar dades entre les instàncies del Project Service Automation i el Finance. La plantilla d'integració que està disponible amb la característica d'integració de dades permet el flux de dades sobre les els contractes del projecte, els projectes, les línies de contracte i les fites de les línies de contracte del projecte del Project Service Automation al Finance.

A la il·lustració següent es mostren les dades que se sincronitzen entre el Project Service Automation i el Finance.

[![Flux de dades per a la integració de Project Service Automation amb el Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Plantilles i tasques

Per accedir a les plantilles disponibles, al centre d'administració del Microsoft Power Apps, seleccioneu **Projectes** i, a continuació, a la cantonada superior dreta, seleccioneu **Nou projecte** per seleccionar les plantilles públiques.

Les plantilles i les tasques subjacents següents s'utilitzen per sincronitzar els contractes del projecte i els projectes del Project Service Automation al Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integració amb el Dynamics 365 Project Service Automation v2.x
- **Nom de la plantilla en la integració de dades**: projectes i contractes (PSA a Fin and Ops)
- **Nom de les tasques del projecte:**

    - Contractes del projecte del PSA a Fin and Ops
    - Projectes del PSA a Fin and Ops
    - Línies de contracte del projecte del PSA a Fin and Ops
    - Fites de les línies de contracte del projecte del PSA a Fin and Ops
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integració amb el Dynamics 365 Project Service Automation v3.x
Hi ha un canvi d'esquema a Project Service Automation que afecta la plantilla de fita de la línia de contracte del projecte i l'ús de la versió v2 de la plantilla és necessari per integrar el Project Service Automation v3.x amb el Dynamics 365.

- **Nom de la plantilla en la integració de dades**: projectes i contractes (PSA 3.x a Fin and Ops), v2
- **Nom de les tasques del projecte:**

    - Contractes del projecte del PSA a Fin and Ops
    - Projectes del PSA a Fin and Ops
    - Línies de contracte del projecte del PSA a Fin and Ops
    - Fites de les línies de contracte del projecte del PSA a Fin and Ops

Abans que es produeixi la sincronització de contractes del projecte i projectes, cal sincronitzar els comptes.

## <a name="entity-set"></a>Conjunt d'entitats

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Comandes                           | Entitat d'integració per a contracte del projecte                |
| Projectes                         | Entitat d'integració per al projecte                         |
| Línies de comanda                      | Entitat d'integració per a la línia de contracte del projecte           |
| Fites de línia de contracte del projecte | Entitat d'integració per a la fita de la línia de contracte del projecte |

## <a name="entity-flow"></a>Flux d'entitat

Els contractes del projecte estan administrats al Project Service Automation i se sincronitzen amb el Finance com a contractes del projecte. Com a part de la plantilla d'integració, podeu definir l'origen d'integració al Finance per al contracte del projecte.

Els projectes de temps i materials i els projectes de preu fix estan administrats al Project Service Automation i se sincronitzen amb el Finance com a projectes. Com a part de la plantilla d'integració, podeu definir l'origen d'integració al Finance per al projecte.

Les línies de contracte del projecte estan administrats al Project Service Automation i se sincronitzen amb el Finance com a normes de facturació dels contractes del projecte. Si el mètode de facturació difereix del tipus de projecte per defecte, la sincronització actualitza el tipus de projecte per al projecte de la línia de contracte i el grup de projectes.

Les fites de les línies de contracte del projecte estan administrats al Project Service Automation i se sincronitzen amb el Finance com a fites de normes de facturació dels contractes del projecte.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solució d'integració del Project Service Automation al Finance

El camp **Identificador del contracte del projecte** està disponible a la pàgina **Contractes del projecte**. Aquest camp té una clau natural i única per donar suport a la integració.

Quan es crea un nou contracte de projecte, si encara no existeix un valor d'**Identificador del contracte del projecte**, es genera automàticament mitjançant una seqüència de números. El valor es compon d'**ORD** seguit d'una seqüència de números que incrementa i, a continuació, un sufix de sis caràcters. Aquest és un exemple: **ORD-01022-Z4M9Q0**.

El camp **Número del projecte** està disponible a la pàgina **Projectes**. Aquest camp té una clau natural i única per donar suport a la integració.

Quan es crea un nou projecte, si encara no existeix un valor de **Número del projecte**, es genera automàticament mitjançant una seqüència de números. El valor es compon de **PRJ** seguit d'una seqüència de números que incrementa i, a continuació, un sufix de sis caràcters. Aquest és un exemple: **PRJ-01049-CCNID0**.

Quan s'aplica la solució d'integració del Project Service Automation al Finance, un script d'actualització configura el camp **Identificador del contracte del projecte** per als contractes de projecte existents i el camp **Número de projecte** per a projectes existents al Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Requisits previs i configuració de l'assignació

- Abans que es produeixi la sincronització de contractes del projecte i projectes, cal sincronitzar els comptes.
- Al conjunt de connexions, afegiu una assignació de camp de clau d'integració per a **msdyn\_organizationalunits** a **msdyn\_name \[Nom\]**. Pot ser que hàgiu d'afegir un projecte al conjunt de connexions. Per obtenir més informació, vegeu [Integrar dades al Common Data Service per a les aplicacions](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Al conjunt de connexions, afegiu una assignació de camp de clau d'integració per a **msdyn\_projects** a **msdynce\_projectnumber \[Número de projecte\]**. Pot ser que hàgiu d'afegir un projecte al conjunt de connexions. Per obtenir més informació, vegeu [Integrar dades al Common Data Service per a les aplicacions](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- El valor **SourceDataID** per a contractes de projecte i projectes es pot actualitzar a un valor diferent o suprimir-se de l'assignació. El valor per defecte de la plantilla és **Project Service Automation**.
- L'assignació **PaymentTerms** ha d'estar actualitzada de manera que reflecteixi els terminis de pagament vàlids al Finance. També podeu suprimir l'assignació de la tasca del projecte. L'assignació de valor per defecte té els valors per defecte per a les dades de demostració. A la taula següent es mostren els valors del Project Service Automation.

    | Valor | Descripció   |
    |-------|---------------|
    | 1     | Pagament a 30 dies        |
    | 2     | 2 % 10, pagament a 30 dies |
    | 3     | Pagament a 45 dies        |
    | 4     | Pagament a 60 dies        |

## <a name="power-query"></a>Power Query

Heu d'utilitzar el Microsoft Power Query per a l'Excel per filtrar les dades si es compleixen les condicions següents:

- Teniu comandes de vendes al Dynamics 365 Sales.
- Teniu diverses unitats organitzatives al Project Service Automation, i aquestes unitats organitzatives s'assignaran a diverses entitats jurídiques al Finance.

Si heu d'utilitzar el Power Query, seguiu aquestes instruccions:

- La plantilla Projectes i contractes (PSA a Fin and Ops) té un filtre per defecte que inclou només les comandes de venda del tipus **Element de treball (msdyn\_ordertype = 192350001)**. Aquest filtre ajuda a garantir que els contractes del projecte no es creen per a les comandes de vendes al Finance. Si creeu una plantilla pròpia, heu d'afegir aquest filtre.
- Heu de crear un filtre del Power Query que inclogui només les organitzacions de contractes que s'han de sincronitzar amb l'entitat jurídica del conjunt de connexions d'integració. Per exemple, els contractes de projecte que teniu amb la unitat organitzativa de contracte de Contoso US s'han de sincronitzar a l'entitat jurídica USSI, però els contractes de projecte que teniu amb la unitat organitzativa de contracte de Contoso Global se sincronitzaran amb l'entitat jurídica USMF. Si no afegiu aquest filtre a l'assignació de tasques, tots els contractes del projecte se sincronitzaran amb l'entitat jurídica que es defineixi per al conjunt de connexions, independentment de la unitat organitzativa del contracte.

## <a name="template-mapping-in-data-integration"></a>Assignació de plantilles a la integració de dades

> [!NOTE] 
> Els camps **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** i **AddressZipCode** no s'inclouen a l'assignació per defecte per a contractes de projecte. Podeu afegir les assignacions si necessiteu que se sincronitzin aquestes dades per als contractes del projecte.
>
> Els camps **Descripció**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** i **ProjectType** no s'inclouen a l'assignació per defecte per als projectes. Podeu afegir les assignacions si necessiteu que se sincronitzin aquestes dades per als projectes.

A les il·lustracions següents es mostren exemples de l'assignació de tasques de plantilla a la integració de dades. L'assignació mostra la informació de camp que se sincronitzarà del Project Service Automation al Finance.

[![Assignació de plantilla de contracte de projecte](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Assignació de plantilla de projecte](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Assignació de plantilla de línies de contracte de projecte](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Assignació de plantilla de fites de línia de contracte de projecte](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Assignació de fites de línia de contracte del projecte a la plantilla Projectes i contractes (PSA 3.x a Dynamics), v2:

[![Assignació de fites de línia de contracte de projecte amb una plantilla de segona versió](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
