---
title: Gestió de projectes i reserves al calendari de l'Office 365
description: Com gestionar de projectes i reserves al calendari de l'Office 365
author: ruhercul
manager: kfend
ms.service: project-operations
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
- D365PS
- ProjectOperations
ms.openlocfilehash: 1df4864ca8dbf6948ca88a7c82a6c0a676e3bd53
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275031"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a>Gestió de projectes i reserves al calendari (Project Service)

> [!Note]
> OBSOLET: aquesta característica ha quedat obsoleta i ja no està disponible.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

Visualitzeu cites personals, reserves de projectes i assignacions d'ordres de treball del servei de camp mitjançant el calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Si tot està només en un lloc, és més fàcil gestionar el vostre dia. Les cites, les reserves i les tasques estan disponibles al calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
 Si utilitzeu el [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], també podeu introduir les vostres cites personals a la visualització d'entrades de temps del Project Service. Això permet als administradors de recursos i projectes saber la vostra disponibilitat quant als projectes. També ajuda a estalviar-vos temps, ja que no heu d'introduir la informació sobre les vostres cites personals dos cops. Simplement podeu importar les vostres cites personals del calendari a la visualització d'entrades de temps del Project Service.  
  
 El vostre calendari sincronitzarà les reserves d'ordres de treball i projectes des del dia actual fins a les quatre properes setmanes. Es pot canviar la configuració.  
  
 La sincronització només es pot realitzar unidireccionalment, del PSA al calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)]. Podeu sincronitzar en l'ordre invers. 
  
 Per obtenir informació sobre com utilitzar el calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)], vegeu [Calendari de l'Outlook a la web per a l'empresa](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).  
  
## <a name="setup"></a>Programa d'instal·lació  
 Abans de poder veure i gestionar les reserves al calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)], heu de configurar algunes coses.  
  
- Haureu de tenir les credencials d'administrador global o administrador del sistema de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)].  
  
- El vostre administrador haurà de configurar el perfil de servidor de correu electrònic i cada usuari haurà de configurar la seva bústia de correu. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Configurar el processament de correu electrònic a través de la sincronització del servidor](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a>Activar la sincronització de la vostra organització (tasca d'administració)  
  
1.  Des del menú principal, feu clic a **Configuració** > **Administració**.  
  
2.  Feu clic a **Configuració del sistema**.  
  
3.  Feu clic a la pestanya **Sincronització**.  
  
4.  A **Seleccioneu si voleu sincronitzar les reserves de recursos amb l'Outlook**, marqueu **Sincronitza les reserves de recursos amb l'Outlook**.  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a>Activar la sincronització del vostre perfil d'usuari (tasca d'usuari)  
  
1.  Feu clic al botó **Configuració** a la cantonada superior dreta de la pantalla.  
  
2.  Feu clic a **Opcions**.  
  
3.  Feu clic a la pestanya **Sincronització**.  
  
4.  A **Sincronització de reserves de recursos**, marqueu **Sincronitza les reserves de recursos amb l'Outlook**.  
  
## <a name="import-your-personal-appointments-user-task"></a>Importació de les cites personals (tasca d'usuari)  
 Simplement podeu importar les vostres cites personals del calendari a la visualització d'entrades de temps del Project Service Automation.  
  
1. Obriu el calendari de l'[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] i feu clic a **Importa dades**.  
  
2. A la pantalla Filtres, seleccioneu **Cites de l'Exchange** i feu clic a **Aplica**.  
  
3. El sistema generarà cites a la visualització d'entrades de temps com a entrades suggerides de la setmana actual. Per afegir entrades d'una altra setmana, feu clic a **Anterior** o **Següent**.  
  
4. Seleccioneu la cita que voleu afegir a la visualització d'entrades de temps del Project Service Automation.  
  
5. Al quadre emergent **Entrada de temps**, seleccioneu les opcions adequades per convertir la cita en una visualització d'entrades de temps del Project Service Automation.  
  
6. Feu clic a **Desa**.  
  
### <a name="see-also"></a>Vegeu també  
 [Guia de temps, despeses i col·laboració](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]