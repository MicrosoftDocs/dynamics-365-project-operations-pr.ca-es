---
title: Habilitar les característiques de l'aplicació Project Finder Mobile
description: Com habilitar les característiques de l'aplicació Project Finder Mobile per al Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 038c5c66-f136-4c7e-88c2-30ada80bbf38
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 9265ee78b20899026277e5af8e589112cd9fac74
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749429"
---
# <a name="enable-project-finder-mobile-app-features-project-service"></a>Habilitar les característiques de l'aplicació Project Finder Mobile (Project Service)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Els vostres recursos poden utilitzar l'aplicació Project Finder Mobile amb l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per cercar nous projectes amb els quals treballar i actualitzar el conjunt d'aptituds.  
  
 L'aplicació està disponible per a telèfons [!INCLUDE[tn_Apple_iphone](../includes/tn-apple-iphone.md)], [!INCLUDE[tn_android](../includes/tn-android.md)] i [!INCLUDE[pn_windows_phone](../includes/pn-windows-phone.md)].  
  
 Heu de definir un parell d'opcions a la configuració de paràmetres per a la vostra unitat organitzativa perquè els usuaris puguin veure els requisits dels recursos dels projectes i actualitzar les seves aptituds.  
  
> [!NOTE]
>  L'aplicació mòbil Project Finder Mobile només funciona amb el [!INCLUDE[pn_crm_online_shortest](../includes/pn-crm-online-shortest.md)], no amb instal·lacions locals.  
  
1. Aneu a **Project Service > Paràmetres**.  
  
2. Feu clic als paràmetres que vulgueu utilitzar per habilitar les característiques de l'aplicació mòbil Project Finder Mobile.  
  
3. A l'àrea **General**, definiu **Requisits de recursos visibles per als recursos** com a **Sí**.  
  
4. Definiu **Permet l'actualització d'aptitud per recurs** com a **Sí**.  
  
   ![ProjectService_ProjectFinderEnable](../project-service/media/project-service-project-finder-enable.png "ProjectService_ProjectFinderEnable")  
  
   És una configuració global. Els administradors de projectes poden definir si un projecte individual estarà visible a la pàgina **Equip del projecte** del projecte.  
  
   ![ProjectService_ProjectTeamVisible](../project-service/media/project-service-project-team-visible.png "ProjectService_ProjectTeamVisible")  
  
## <a name="email-notifications"></a>Notificacions de correu electrònic  
 l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] envia correus electrònics en relació amb sol·licituds de recursos als destinataris i a les hores següents:  
  
|Destinatari|Incidència|  
|---------------|-----------|  
|Administrador de projectes|-   Quan un recurs es subscriu a un projecte amb l'aplicació mòbil Project Finder Mobile.|  
|Recurs|-   Quan el treball del projecte al qual s'ha subscrit el recursos ja s'ha omplert per un altre recurs.<br />-   Quan la sol·licitud d'aprovació s'hagi aprovat o rebutjat.<br />-   Quan la sol·licitud d'aprovació de subscripció s'hagi aprovat o rebutjat.|  
  
## <a name="privacy-notice"></a>Avís de privadesa  
 [!INCLUDE[cc_privacy_crm_project_finder_mobile_app](../includes/cc-privacy-crm-project-finder-mobile-app.md)]  
  
### <a name="see-also"></a>Vegeu també  
 [Definir recursos](../project-service/set-up-resources.md)
