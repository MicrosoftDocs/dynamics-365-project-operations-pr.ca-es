---
title: Planifiqueu el vostre treball al Microsoft Project amb el complement Project Service
description: En aquest tema es proporciona informació sobre com utilitzar el complement del Microsoft Project per al Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145931"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Planifiqueu el vostre treball al Microsoft Project amb el complement Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

El [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] us facilita la planificació del projecte, incloent-hi les estimacions. Podeu definir el treball perquè els costos, l'esforç i el valor de les vendes siguin clars quan es presenti la proposta final.  

Podeu instal·lar el [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] i realitzar la planificació del treball en l'entorn familiar del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Utilitzeu les capacitats de planificació i gestió robustes del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i actualitzeu el pla del vostre projecte al Project Service Automation.  

> [!IMPORTANT]
> - Per utilitzar la característica d'administració de documents del SharePoint per emmagatzemar els vostres fitxers del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per als projectes del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], l'administrador del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] haurà d'activar l'administració de documents. 
> - El [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] només és compatible amb el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Descarregar i instal·lar el complement  
 Heu de tenir la informació d'inici de sessió del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] preparada. Necessitareu aquesta informació per connectar-vos del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Al centre de baixades, baixeu el complement per a la versió compatible del servei del Project Service, ja sigui la [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) o la [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Seleccioneu l'enllaç de descàrrega.  

3.  Quan s'hagi completat la descàrrega, seleccioneu **Sí** per instal·lar el complement.  

## <a name="configure-the-add-in"></a>Configurar el complement  

1. Obriu el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i seleccioneu la pestanya **Project Service**.  

2. Seleccioneu **Connecta**.  

3. Introduïu la vostra informació d'inici de sessió i seleccioneu **Inicia sessió**.  

   Ara podeu començar a utilitzar el complement.  

## <a name="read-from-a-template"></a>Llegir d'una plantilla  
 Llegiu des d'una plantilla que hàgiu creat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] i copiat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] per començar la planificació del projecte. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md)  

1.  A la pestanya **Project Service**, seleccioneu **Lectura** > **Plantilla de projecte del Project Service Automation**.  

2.  Trieu una plantilla de projecte de la llista i seleccioneu **Obre**.  

    > [!NOTE]
    >  Per defecte, les tasques que es copien de la plantilla al projecte es defineixes com planificades manualment.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Assignar funcions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] als recursos del projecte  

1.  Obriu un projecte i seleccioneu la franja **Tasca**.  

2. Seleccioneu el menú **Gràfic de Gantt** i seleccioneu **Full de recurs**.  

3. Al full de recurs, seleccioneu el menú desplegable **Funció de recurs del Project Service** i seleccioneu una funció del Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Seleccionar el personal del projecte amb recursos  

1.  A la pestanya Project Service, seleccioneu una fila i seleccioneu **Cerca recursos**.  

2.  A la pantalla **Reserva el recurs**, seleccioneu el recurs que voleu utilitzar per al projecte.  

3.  Seleccioneu **Llibre** i, a continuació, **D'acord**.  

## <a name="publish-your-project"></a>Publicar el projecte  
Quan s'hagi completat la planificació del projecte, el següent pas és importar i publicar el projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

El projecte s'importarà al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. S'aplica el procés de generació de preus i d'equip. Obriu el projecte a [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] per veure que s'han generat l'equip, les estimacions del projecte i l'estructura del desglossament del treball. La taula següent mostra on trobar els resultats.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gràfic de Gantt**   | Importa a la pantalla de l-**estructura del desglossament del treball** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Full de recursos** |   Importa a la pantalla dels **membres de l'equip del projecte** del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Utilitzar l'ús**    |    Importa a la pantalla d'**Estimacions del projecte** de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].     |

**Per importar i publicar el vostre projecte**  
1. A la pestanya **Project Service**, aneu a **Publica** > **Nou projecte del Project Service Automation**.  

2. Al quadre de diàleg **Publicació en un projecte nou del Project Service**, introduïu el **Nom del projecte** i seleccioneu el **Client**.  

3. De forma opcional, seleccioneu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer de projecte de pla al Project Service Automation.  

4. Seleccioneu **Publica**.  

   Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com només de lectura.  Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Editar un projecte que s'ha importat  
 Per fer canvis en un pla de projecte que s'ha importat al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], teniu dues opcions:  

- Obriu el fitxer mestre i editeu-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Desenllaçar el fitxer i editar-lo directament al Project Service. Per defecte, un projecte que s'ha carregat del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] està bloquejat i només es pot editar al Project. Per editar el fitxer al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], el fitxer ha d'estar desenllaçat.  

### <a name="edit-in-pn_microsoft_project"></a>Edita-ho a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Al menú principal, aneu a **Project Service** > **Projectes**.  

2. A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccioneu **Obre al MS Project** de la franja. Això obrirà el fitxer mestre enllaçat al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Desenllaçar un fitxer i editar-lo al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Al menú principal, aneu a **Project Service** > **Projectes**.  

2. A la llista de projectes, obriu el que vàreu crear al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Seleccioneu **Desenllaça del MS Project** de la franja.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Carregar un fitxer del Project al SharePoint o als grups de l'Office  
 Podeu carregar el fitxer del Project al SharePoint i trobar-lo als documents associats del projecte del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Heu de demanar a l'administrador que configuri l'administració de documents del SharePoint i l'activi per a l'entitat del Project. 

 També podeu carregar el fitxer del Project al [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] si heu configurat els Grups de l'Office.

### <a name="upload-a-file-for-sharepoint"></a>Pujar un fitxer per al SharePoint  

1. Al menú principal, aneu a **Project Service** > **Carrega**.  

2. Seleccioneu **Als documents del projecte de Project Service Automation**.  

3. Al quadre de diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.  

   - Si seleccioneu **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation i executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.  

   - Si seleccioneu **No**, l'enllaç d'**Obre a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.  

4. Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Carregar un fitxer per als Grups de l'Office  

1. Al menú principal, aneu a **Project Service** > **Carrega**.  

2. Seleccioneu **Als documents del projecte de Project Service Automation**.  

3. Al quadre de diàleg **Permet l'obertura al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]**, seleccioneu **Sí** o **No**.  

   - Si seleccioneu **Sí**, podreu seleccionar el botó **Obre al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** al Project Service Automation i executar el [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i carregar el fitxer del Project de la biblioteca de documents del SharePoint.  

   - Si seleccioneu **No**, l'enllaç d'**Obre a [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** no funcionarà.  

4. Es pot trobar el fitxer del [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a **Documents** per al projecte específic del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publicar el vostre projecte com a plantilla  
 Podeu desar el vostre projecte i reutilitzar-lo desant-lo com a plantilla de projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Les plantilles de projecte són plans de projecte reutilitzables al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Per obtenir més informació, vegeu [Crear una plantilla de projecte (Project Service Automation)](../psa/create-project-template.md). 

1. A la pestanya **Project Service**, aneu a **Publica** > **Nova plantilla de projecte del Project Service Automation**.  

2. Al quadre de diàleg **Publicació en una plantilla nova del Project Service**, introduïu el **Nom de la plantilla del projecte**.  

3. De forma opcional, seleccioneu la casella **Enllaça el pla de projecte al Project Service Automation** per enllaçar el fitxer de projecte al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Seleccioneu **Publica**.  

Enllaçar el fitxer del Project al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] farà que el fitxer del Project sigui el fitxer mestre i defineix l'estructura del desglossament del treball al [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] com plantilla només de lectura.  Per fer canvis al pla del projecte, cal fer-los al [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] i publicar-los com a actualitzacions del [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Lectura d'una planificació carregada per recursos

Quan es llegeix un projecte de Project Service Automation, el calendari del recurs no se sincronitza amb el client d'escriptori. Si hi ha diferències en la durada de la tasca, l'esforç o el final, probablement és degut a que els recursos i el client d'escriptori no han aplicat al projecte el mateix calendari de plantilla d'hores de feina.


## <a name="data-synchronization"></a>Sincronització de les dades
Les taules d'aquesta secció proporcionen informació sobre la sincronització de dades d'entitat entre el Project Service Automation i el complement d'escriptori del Microsoft Project.

### <a name="project-task-entity-table"></a>Taula d'entitats de la tasca del projecte
A la taula següent es descriu la manera que se sincronitzen les dades d'entitats de les tasques de projecte entre el Project Service Automation i el complement d'escriptori de Microsoft Project.

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Tasca del projecte | Venciment | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Esforç estimat | Sincronitzat | No està sincronitzat |
| Tasca del projecte | ID de client d’MS Project | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Tasca principal | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Project | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Tasca del projecte | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Nom de la tasca del projecte | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Unitat de recursos (obsolet a la versió 3.0) | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Durada planificada | Sincronitzat | No està sincronitzat |
| Tasca del projecte | Data d’inici | Sincronitzat | No està sincronitzat |
| Tasca del projecte | ID de WBS | Sincronitzat | No està sincronitzat |

### <a name="team-member-entity-table"></a>Taula d'entitats dels membres de l'equip
A la taula següent es descriu la manera que se sincronitzen les dades d'entitats dels membres de l'equip entre Project Service Automation i el complement d'escriptori de Microsoft Project.

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Membre de l'equip | ID de client d’MS Project | Sincronitzat | No està sincronitzat |
| Membre de l'equip | Nom de la posició | Sincronitzat | No està sincronitzat |
| Membre de l'equip | projecte | Sincronitzat | Sincronitzat |
| Membre de l'equip | Equip del projecte | Sincronitzat | Sincronitzat |
| Membre de l'equip | Unitat de recursos | No està sincronitzat | Sincronitzat |
| Membre de l'equip | Funció | No està sincronitzat | Sincronitzat |
| Membre de l'equip | Hores de feina | No està sincronitzat | No està sincronitzat |

### <a name="resource-assignment-entity-table"></a>Taula d'entitats d'assignació de recursos
A la taula següent es descriu la manera que se sincronitzen les dades d'entitats d'assignació de recursos entre Project Service Automation i el complement d'escriptori de Microsoft Project.

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Assignació de recursos | Data d'inici | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Hores | Sincronitzat | No està sincronitzat |
| Assignació de recursos | ID de client d’MS Project | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Feina planejada | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Project | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Equip del projecte | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Assignació de recursos | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Tasca | Sincronitzat | No està sincronitzat |
| Assignació de recursos | Data final | Sincronitzat | No està sincronitzat |

### <a name="project-task-dependencies-entity-table"></a>Taula d'entitats de les dependències de la tasca del projecte
A la taula següent es descriu la manera que se sincronitzen les dades d'entitats de les dependències de la tasca de projecte entre el Project Service Automation i el complement d'escriptori de Microsoft Project.

| **Entitat** | **Camp** | **De Microsoft Project a Project Service Automation** | **De Project Service Automation a Microsoft Project** |
| --- | --- | --- | --- |
| Dependències de les tasques del projecte | Dependència de les tasques del projecte | Sincronitzat | No està sincronitzat |
| Dependències de les tasques del projecte | Tipus d’enllaç | Sincronitzat | No està sincronitzat |
| Dependències de les tasques del projecte | Tasca predecessora | Sincronitzat | No està sincronitzat |
| Dependències de les tasques del projecte | Project | Sincronitzat | No està sincronitzat |
| Dependències de les tasques del projecte | Tasca successora | Sincronitzat | No està sincronitzat |

### <a name="additional-resources"></a>Recursos addicionals
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)
