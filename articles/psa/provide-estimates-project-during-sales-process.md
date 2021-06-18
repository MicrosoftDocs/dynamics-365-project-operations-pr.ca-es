---
title: Proporcionar estimacions de treball per a un projecte durant el procés de vendes
description: Com proporcionar estimacions de treball per a un projecte durant el procés de vendes al Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998219"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Proporcionar estimacions de treball per a un projecte durant el procés de vendes (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Durant el procés de vendes, podeu elaborar estimacions de vendes des de zero amb línies d'oferta. Les capacitats de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] al [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] proporcionen una manera més científica i determinista d'arribar amb una estimació de vendes desglossant els elements de treball i associant els atributs rellevants que contribueixen a les estimacions del projecte en l'estructura del desglossament del treball.  
  
 Una vegada guanyada la venda, podeu utilitzar l'estructura del desglossament del treball associada al vostre pla de projecte i millorar-la per tal de completar amb èxit el projecte.  
  
## <a name="link-a-project-to-a-quote-line"></a>Enllaçar un projecte amb una línia d'oferta  
 Quan creeu una línia d'oferta basada en un projecte, podeu crear un nou projecte a partir de la línia d'oferta. Podeu utilitzar plantilles de projecte, que poden ser plans de projecte estàndard preconfigurats i estimacions financeres habituals a la vostra organització, o una còpia d'un pla de projecte i les estimacions d'un projecte passat. Quan creeu un projecte, la tria d'una plantilla de projecte proporciona una base per refinar el pla de projecte, les estimacions i els requisits de les funcions. Si el vostre projecte es crea a partir de l'oferta, el projecte s'associa automàticament a la línia d'oferta.  
  
## <a name="project-estimate-components"></a>Components d'estimació del projecte  
 L'estructura del desglossament del treball en un projecte proporciona una manera de desglossar la feina en tasques, mantenir una jerarquia de tasques i assignar una estimació de l'esforç necessari per completar cada tasca. També podeu associar funcions a una tasca per indicar una estimació del tipus de recurs necessari per completar una tasca i una planificació.  
  
 L'estructura del desglossament del treball ajuda a calcular l'esforç de treball i de planificació. Per defecte, el projecte utilitza llistes de preus per defecte que heu definit prèviament. El cost i els preus de vendes definits a les llistes de preus ajuden a determinar les estimacions financeres per al desglossament de feina del projecte.  
  
 Si el vostre projecte està associat amb un pressupost, i l'oferta té una llista de preus diferent del valor per defecte, la llista de preus de l'oferta s'utilitza per a les estimacions financeres.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Importar estimacions d'un projecte a una oferta  
 Quan ja teniu les estimacions de projecte dins del projecte, podeu importar aquestes estimacions a la línia d'oferta:  
  
-   A **Detalls de la línia d'oferta**, feu clic a **Importa des d'estimacions**. 

-   Seleccioneu si importareu estimacions de projecte resumides per tipus d'operació, funció o nivell de node d'estructura del desglossament del treball.  
  
### <a name="see-also"></a>Vegeu també  
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]