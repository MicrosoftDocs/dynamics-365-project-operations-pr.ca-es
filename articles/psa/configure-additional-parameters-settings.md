---
title: Configurar paràmetres addicionals
description: Com configurar paràmetres addicionals al Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 24a4fe83471da916fb91cfe20e739279c08d8e5e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072212"
---
# <a name="configure-additional-parameter-settings-project-service"></a>Configurar paràmetres addicionals (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Un cop hàgiu configurat els elements als temes anteriors, heu de definir paràmetres addicionals per utilitzar-los per als vostres projectes. Quan hàgiu instal·lat l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per primer cop, podeu crear paràmetres per crear per primer cop tots els registres necessaris per que funcionin a l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Ara és el moment de tornar enrere i configurar camps addicionals per a aquests paràmetres.  
  
 Haureu d'haver configurat els paràmetres següents:  
  
-   Unitat organitzativa  
  
-   Freqüència de facturació  
  
-   Plantilles d'hores de feina  
  
-   Llista de preus  
 
En aquest pas, també indicareu quin tipus d'assignació de recursos voleu:  
  
- **Central**. Només els administradors de recursos poden assignar recursos a projectes.  
  
- **Híbrida**. Els administradors de recursos, projectes i comptes poden assignar recursos a projectes.  
  
 
Per definir els paràmetres del projecte:  
  
1. Aneu a **Project Service > Paràmetres**.  
  
2. Feu clic als paràmetres que voleu configurar (els que vàreu crear en instal·lar per primer cop l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]) o feu clic a **Crea** per crear-ne de nous.  
  
3. A l'àrea **General** , definiu totes les opcions per als paràmetres del vostre projecte.  
  
4. A l'àrea **Llista de preus** , feu clic a **+** per afegir una llista de preus, seleccioneu una llista de preus a la llista desplegable **Llista de preus de paràmetres de projecte** i feu clic a **Desa**.  
  
5. Feu clic al botó **Desa** a la cantonada inferior dreta de la pantalla.  

> [!NOTE]
> El registre del paràmetre del projecte s'ha de mantenir perquè el Project Service funcioni de manera correcta. Aquest registre no s'ha de suprimir.

### <a name="see-also"></a>Vegeu també  
 [Definir recursos](../psa/set-up-resources.md)