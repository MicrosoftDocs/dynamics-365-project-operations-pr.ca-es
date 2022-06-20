---
title: Utilitzar el complement Project Service per planificar el vostre treball al Microsoft Project | MicrosoftDocs
description: En aquest article s'ofereix informació sobre com afegir, configurar i utilitzar el complement del Microsoft Project per al Servei del Microsoft Project.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: d286adfdffa6a0b5f0c96eb14be588c6cedb80c2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925522"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Utilitzar el complement Project Service Automation per planificar el vostre treball al Microsoft Project

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

El [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] us facilita la planificació del projecte, incloent-hi les estimacions. Podeu definir el treball perquè els costos, l'esforç i el valor de les vendes siguin clars quan es presenti la proposta final.  

 Ara podeu instal·lar el [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i realitzar la planificació del treball en l'entorn familiar del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilitzeu les capacitats de planificació i gestió robustes del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i actualitzeu el pla del vostre projecte al Project Service Automation.  

> [!IMPORTANT]
> - Per utilitzar la característica d'administració de documents del SharePoint per emmagatzemar els vostres fitxers del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per als projectes del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], l'administrador del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] haurà d'activar l'administració de documents. 
> - El [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] només és compatible amb el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descarregar i instal·lar el complement  
 Heu de tenir la informació d'inici de sessió del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] preparada. Necessitareu aquesta informació per connectar-vos del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Al centre de baixades, baixeu el complement per a la versió compatible del servei del Project Service, ja sigui la [V2.X](/dynamics365/project-operations/psa/overview#guidance-for-earlier-versions-app-version-2x-or-1x) o la [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Feu clic a l'enllaç de descàrrega.  

3.  Quan s'hagi completat la descàrrega, feu clic a **Sí** per instal·lar el complement.  

## <a name="configure-the-add-in"></a>Configurar el complement  

1. Obriu el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i feu clic a la pestanya **Project Service**.  

2. Feu clic a **Connecta**.  

3. Introduïu la vostra informació d'inici de sessió i feu clic a **Inicia sessió**.  

   Ara podeu començar a utilitzar el complement.  

## <a name="read-from-a-template"></a>Llegir d'una plantilla  
 Llegiu des d'una plantilla que hàgiu creat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i copiat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per començar la planificació del projecte. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md)  

1.  A la pestanya **Project Service**, feu clic a **Lectura** > **Plantilla de projecte del Project Service Automation**.  

2.  Trieu una plantilla de projecte de la llista i feu clic a **Obre**.  

    > [!NOTE]
    >  Per defecte, les tasques que es copien de la plantilla al projecte es defineixes com planificades manualment.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Assignar funcions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] als recursos del projecte  

1.  Obriu un projecte i feu clic a la franja **Tasca**.  

2.  Feu clic al menú **Gràfic de Gantt** i seleccioneu **Full de recurs**.  

3.  Al full de recurs, feu clic al menú desplegable **Funció de recurs del Project Service** i seleccioneu una funció del Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Seleccionar el personal del projecte amb recursos  

1.  A la pestanya Project Service, seleccioneu una fila i feu clic a **Cerca recursos**.  

2.  A la pantalla **Reserva el recurs**, seleccioneu el recurs que voleu utilitzar per al projecte.  

3.  Feu clic a **Reserva** i, a continuació, a **D'acord**.  

## <a name="publish-your-project"></a>Publicar el projecte  
Quan s'hagi completat la planificació del projecte, el següent pas és importar i publicar el projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

El projecte s'importarà al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. S'aplica el procés de generació de preus i d'equip. Obriu el projecte a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per veure que s'han generat l'equip, les estimacions del projecte i l'estructura del desglossament del treball. La taula següent mostra on trobar els resultats:

| Project | Detalles |
| ---- | --- |
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gràfic de Gantt**   | Importa a la pantalla de l-**estructura del desglossament del treball** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Full de recursos** |   Importa a la pantalla dels **membres de l'equip del projecte** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilitzar l'ús**    |    Importa a la pantalla d'**Estimacions del projecte** de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Per importar i publicar el vostre projecte**  
1. A la pestanya **Project Service**, feu clic a **Publica** > **Nou projecte del Project Service Automation**.  

2. Al quadre de diàleg **Publicació en un projecte nou del Project Service**, introduïu el **Nom del projecte** i seleccioneu el **Client**.  

3. De forma opcional, marqueu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer de projecte de pla al Project Service Automation.  

4. Feu clic a **Publica**.  

   Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com només de lectura.  Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar un projecte que s'ha importat  
 Per fer canvis en un pla de projecte que s'ha importat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], teniu dues opcions:  

- Obriu el fitxer mestre i editeu-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desenllaçar el fitxer i editar-lo directament al Project Service. Per defecte, un projecte que s'ha carregat del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] està bloquejat i només es pot editar al Project. Per editar el fitxer al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el fitxer ha d'estar desenllaçat.  

### <a name="edit-in-pn_microsoft_project"></a>Editeu-ho al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Des del menú principal, feu clic a **Project Service** > **Projectes**.  

2. A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Feu clic a **Obre al MS Project** de la franja. Això obrirà el fitxer mestre enllaçat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desenllaçar un fitxer i editar-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Des del menú principal, feu clic a **Project Service** > **Projectes**.  

2. A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Feu clic a **Desenllaça del MS Project** de la franja.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Carregar un fitxer del Project al SharePoint o als grups de l'Office  
 Podeu carregar el fitxer del Project al SharePoint i trobar-lo als documents associats del projecte del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Heu de demanar a l'administrador que configuri l'administració de documents del SharePoint i l'activi per a l'entitat del Project. 

 També podeu carregar el fitxer del Project al [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si heu configurat els Grups de l'Office.

### <a name="upload-a-file-for-sharepoint"></a>Pujar un fitxer per al SharePoint  

1. Des del menú principal, feu clic a **Project Service** > **Carrega**.  

2. Seleccioneu **Als documents del projecte de Project Service Automation**.  

3. Al diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.  

   - Si feu clic a **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation, executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.  

   - Si feu clic a **No**, l'enllaç del botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.  

4. Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Carregar un fitxer per als Grups de l'Office  

1. Des del menú principal, feu clic a **Project Service** > **Carrega**.  

2. Seleccioneu **Als documents del projecte de Project Service Automation**.  

3. Al diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.  

   - Si feu clic a **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation, executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.  

   - Si feu clic a **No**, l'enllaç del botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.  

4. Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicar el vostre projecte com a plantilla  
 Podeu desar el vostre projecte i reutilitzar-lo desant-lo com a plantilla de projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Les plantilles de projecte són plans de projecte reutilitzables al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md)  

1. A la pestanya **Project Service**, feu clic a **Publica** > **Nova plantilla de projecte del Project Service Automation**.  

2. Al quadre de diàleg **Publicació en una plantilla nova del Project Service**, introduïu el **Nom de la plantilla del projecte**.  

3. De forma opcional, marqueu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Feu clic a **Publica**.  

Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com plantilla només de lectura.  Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Lectura d'una planificació carregada per recursos

Quan es llegeix un projecte de Project Service Automation, el calendari del recurs no se sincronitza amb el client d'escriptori. Si hi ha diferències en la durada de la tasca, l'esforç o el final, probablement és degut a que els recursos i el client d'escriptori no han aplicat al projecte el mateix calendari de plantilla d'hores de feina.


## <a name="data-synchronization"></a>Sincronització de dades

A la taula següent es descriu la manera com se sincronitzen les dades entre Project Service Automation i el complement d'escriptori de Microsoft Project.

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Tasca del projecte | Venciment | ● | - |
| Tasca del projecte | Esforç estimat | ● | - |
| Tasca del projecte | ID de client d’MS Project | ● | - |
| Tasca del projecte | Tasca principal | ● | - |
| Tasca del projecte | Project | ● | - |
| Tasca del projecte | Tasca del projecte | ● | - |
| Tasca del projecte | Nom de la tasca del projecte | ● | - |
| Tasca del projecte | Unitat de recursos (obsolet a la versió 3.0) | ● | - |
| Tasca del projecte | Durada planificada | ● | - |
| Tasca del projecte | Data d’inici | ● | - |
| Tasca del projecte | ID de WBS | ● | - |

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Membre de l'equip | ID de client d’MS Project | ● | - |
| Membre de l'equip | Nom de la posició | ● | - |
| Membre de l'equip | projecte | ● | ● |
| Membre de l'equip | Equip del projecte | ● | ● |
| Membre de l'equip | Unitat de recursos | - | ● |
| Membre de l'equip | Funció | - | ● |
| Membre de l'equip | Hores de feina | No sincronitzat | No sincronitzat |

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Assignació de recursos | Data d'inici | ● | - |
| Assignació de recursos | Hores | ● | - |
| Assignació de recursos | ID de client d’MS Project | ● | - |
| Assignació de recursos | Feina planejada | ● | - |
| Assignació de recursos | Project | ● | - |
| Assignació de recursos | Equip del projecte | ● | - |
| Assignació de recursos | Assignació de recursos | ● | - |
| Assignació de recursos | Tasca | ● | - |
| Assignació de recursos | Data final | ● | - |

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dependències de les tasques del projecte | Dependència de les tasques del projecte | ● | - |
| Dependències de les tasques del projecte | Tipus d’enllaç | ● | - |
| Dependències de les tasques del projecte | Tasca predecessora | ● | - |
| Dependències de les tasques del projecte | Project | ● | - |
| Dependències de les tasques del projecte | Tasca successora | ● | - |

### <a name="see-also"></a>Vegeu també  
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
