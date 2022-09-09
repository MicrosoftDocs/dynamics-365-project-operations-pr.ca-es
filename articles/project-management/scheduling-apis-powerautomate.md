---
title: Ús d'API de planificació de projectes amb el Power Automate
description: Aquest article proporciona un flux d'exemple que utilitza les interfícies de programació d'aplicacions de planificació de projectes (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404451"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Ús d'API de planificació de projectes amb el Power Automate

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest article es descriu un flux d'exemple que mostra com crear un pla de projecte complet mitjançant l'ús Microsoft Power Automate, com crear un conjunt d'operacions i com actualitzar una entitat. L'exemple demostra com crear un projecte, un membre de l'equip del projecte, conjunts d'operacions, tasques del projecte i assignacions de recursos. En aquest article també s'explica com actualitzar una entitat i executar un conjunt d'operacions.

A continuació es mostra una llista completa dels passos que es documenten al flux d'exemple d'aquest article:

1. [Crear un PowerApps activador](#1)
2. [Crear un projecte](#2)
3. [Inicialitzar una variable per al membre de l'equip](#3)
4. [Crear un membre genèric de l'equip](#4)
5. [Crear un conjunt d'operacions](#5)
6. [Crear un cub de projecte](#6)
7. [Inicialitzar una variable per a l'estat de l'enllaç](#7)
8. [Inicialitzar una variable per al nombre de tasques](#8)
9. [Inicialitzar una variable per a l'identificador de tasca del projecte](#9)
10. [Fes fins que](#10)
11. [Definir una tasca del projecte](#11)
12. [Crear una tasca de projecte](#12)
13. [Crear una assignació de recursos](#13)
14. [Decrementar una variable](#14)
15. [Canviar el nom d'una tasca del projecte](#15)
16. [Executeu un conjunt d'operacions](#16)

## <a name="assumptions"></a>Supòsits

Aquest article suposa que teniu un coneixement bàsic de la plataforma, els fluxos al Dataverse núvol i la interfície de programació d'aplicacions de planificació de projectes (API). Per obtenir més informació, vegeu la [secció Referències](#references) més endavant d'aquest article.

## <a name="create-a-flow"></a>Creació d'un flux

### <a name="select-an-environment"></a>Permet seleccionar un entorn.

Podeu crear el flux al Power Automate vostre entorn.

1. Aneu a <https://flow.microsoft.com>, i utilitzeu les credencials d'administrador per iniciar la sessió.
2. A l'extrem superior dret, seleccioneu **Entorns**.
3. A la llista, seleccioneu l'entorn on Dynamics 365 Project Operations s'instal·la.

### <a name="create-a-solution"></a>Crear una solució

Seguiu aquests passos per crear un [flux](/power-automate/overview-solution-flows) conscient de la solució. En crear un flux conscient de la solució, podeu exportar més fàcilment el flux per utilitzar-lo més endavant.

1. A la subfinestra de navegació, seleccioneu **Solucions**.
2. A la **pàgina Solucions**, seleccioneu **Solució nova**.
3. Al quadre de **diàleg Solució** nova, definiu els camps necessaris i, a continuació, seleccioneu **Crea**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Pas 1: creeu un PowerApps activador

1. A la **pàgina Solucions**, seleccioneu la solució que heu creat i, a continuació, seleccioneu **Crea**.
2. A la subfinestra esquerra, seleccioneu **Flux de núvol** \> **Automatització** \> **flux del núvol** \> **instantani.**
3. Al camp Nom **del flux, introduïu** Planifica el **flux de demostració de l'API**.
4. A l'opció **Trieu com activar aquesta llista de flux**, seleccioneu **Power Apps**. Quan creeu un Power Apps activador, la lògica depèn de vosaltres com a autor. En aquest article, deixeu els paràmetres d'entrada en blanc amb finalitats de prova.
5. Seleccioneu **Crea**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pas 2: Crear un projecte

Seguiu aquests passos per crear un projecte d'exemple.

1. Al flux que heu creat, seleccioneu **Pas nou**.

    ![Afegint un nou pas.](media/newstep.png)

2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.

    ![Selecció d'una operació.](media/chooseactiontab.png)

3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.

![Canvi de nom d'un pas.](media/renamestep.png)

4. Canvieu el nom del pas **Crea un projecte**.
5. Al camp Nom **de l'acció**, seleccioneu **msdyn\_ CreateProjectV1**.
6. **Al camp del tema\_ msdyn**, seleccioneu **Afegeix contingut** dinàmic.
7. A la **pestanya Expressió**, al camp de funcions, introduïu **Nom del projecte - utcNow()**.
8. Seleccioneu **D'acord**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Pas 3: inicialitzar una variable per al membre de l'equip

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **inicialitzar la variable**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **membre** de l'equip Init.
5. **Al camp Nom**, introduïu **TeamMemberAction**.
6. **Al camp Tipus**, seleccioneu **Cadena**.
7. **Al camp Valor**, introduïu **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Pas 4: Creeu un membre genèric de l'equip

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Crea un membre de l'equip**.
5. Per al camp Nom **de l'acció**, seleccioneu **TeamMemberAction** al **quadre de diàleg Contingut** dinàmic.
6. **Al camp Paràmetres** d'acció, introduïu la informació del paràmetre següent.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Aquí teniu una explicació dels paràmetres:

    - **\@\@ odata.type** - El nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_ projectteam".**
    - **msdyn\_ projectteamid** – La clau principal de l'identificador de l'equip del projecte. El valor és una expressió globalment identificador únic (GUID).   L'identificador es genera a partir de la pestanya d'expressió.

    - **msdyn\_ project\@ odata.bind** – L'identificador del projecte del projecte propietari. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Les cometes són obligatòries. Per exemple, introduïu **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**".
    - **Nom\_ msdyn**- El nom del membre de l'equip. Per exemple, introduïu **"ScheduleAPIDemoTM1".**

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Pas 5: creeu un conjunt d'operacions

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Crea un conjunt d'operacions**.
5. Al camp Nom de l'acció **, seleccioneu l'acció** personalitzada msdyn **CreateOperationSetV1\_**.Dataverse
6. **Al camp Descripció**, introduïu **ScheduleAPIDemoOperationSet**.
7. **Al camp Projecte**, introduïu **/msdyn\_ projects(**.
8. Al quadre de **diàleg Contingut** dinàmic, seleccioneu **msdyn\_ CreateProjectV1Response ProjectId**.
9. **Al camp Projecte**, introduïu **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Pas 6: creeu un cub de projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **afegeix una fila** nova. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Crea un cub**.
5. Al camp Nom **de la** taula, seleccioneu **Cubells** de projecte.
6. **Al camp Nom**, introduïu **ScheduleAPIDemoBucket1**.
7. Per al **camp Projecte**, seleccioneu **msdyn\_ CreateProjectV1Response ProjectId** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Pas 7: inicialitzeu una variable per a l'estat de l'enllaç

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **inicialitzar la variable**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Init linkstatus**.
5. **Al camp Nom**, introduïu **linkstatus**.
6. **Al camp Tipus**, seleccioneu **Nombre enter**.
7. **Al camp Valor**, introduïu **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Pas 8: inicialitzeu una variable per al nombre de tasques

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **inicialitzar la variable**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Init Nombre de tasques**.
5. **Al camp Nom**, introduïu **el nombre de tasques**.
6. **Al camp Tipus**, seleccioneu **Nombre enter**.
7. **Al camp Valor**, introduïu **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Pas 9: inicialitzeu una variable per a l'identificador de tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **inicialitzar la variable**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Init ProjectTaskID**.
5. **Al camp Nom**, introduïu **el nombre de tasques**.
6. **Al camp Tipus**, seleccioneu **Cadena**.
7. Per al **camp Valor**, introduïu **guid()** al creador d'expressions.

## <a name="step-10-do-until"></a><a id="10"></a> Pas 10: feu fins que

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **do fins** que. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Definiu el primer valor de l'expressió condicional a la **variable nombre de tasques** del **quadre de diàleg Contingut** dinàmic.
4. Establiu la condició en **menys d'igual a**.
5. Definiu el segon valor de l'enunciat condicional a **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Pas 11: definiu una tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** establerta. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Defineix la tasca** del projecte.
5. **Al camp Nom**, seleccioneu **msdyn\_ projecttaskid**.
6. Per al **camp Valor**, introduïu **guid()** al creador d'expressions.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Pas 12: crear una tasca de projecte

Seguiu aquests passos per crear una tasca de projecte que tingui un identificador únic que pertanyi al projecte actual i al dipòsit de projecte que heu creat.

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Crea una tasca** del projecte.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **PssCreateV1\_.**
6. **Al camp Entitat**, introduïu la informació del paràmetre següent.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Aquí teniu una explicació dels paràmetres:

    - **\@\@ odata.type** - El nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_ projecttask".**
    - **msdyn\_ projecttaskid** – L'identificador únic de la tasca. El valor s'ha d'establir en una variable dinàmica a partir de **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – L'identificador del projecte del projecte propietari. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Les cometes són obligatòries. Per exemple, introduïu **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**".
    - **msdyn\_ subject** - Qualsevol nom de tasca.
    - **msdyn\_ projectbucket\@ odata.bind** – El cub del projecte que conté les tasques. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea cub". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Les cometes són obligatòries. Per exemple, introduïu **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**".
    - **Inici msdyn\_** - Contingut dinàmic per a la data d'inici. Per exemple, demà es representarà com a **"addDays(utcNow(), 1)"**.
    - **inici programat\_ msdyn**- La data d'inici programada. Per exemple, demà es representarà com a **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – La data prevista de finalització. Seleccioneu una data en el futur. Per exemple, especifiqueu **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** - L'estat de l'enllaç. Per exemple, introduïu **"192350000".**

7. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Pas 13: crear una assignació de recursos

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Crea una assignació**.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **PssCreateV1\_.**
6. **Al camp Entitat**, introduïu la informació del paràmetre següent.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Pas 14: desxifrar una variable

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** de decrement. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. **Al camp Nom**, seleccioneu **nombre de tasques**.
4. **Al camp Valor**, introduïu **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Pas 15: canvieu el nom d'una tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Canvia el nom de la tasca** del projecte.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **PssUpdateV1\_.**
6. **Al camp Entitat**, introduïu la informació del paràmetre següent.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Pas 16: executeu un conjunt d'operacions

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **realitza l'acció de desembossament**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas **Executa el conjunt d'operacions**.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **ExecuteOperationSetV1\_.**
6. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response OperationSetId** al **quadre de diàleg Contingut de Dynamid**.

## <a name="references"></a>Referències

- [Visió general de com integrar fluxos amb Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](schedule-api-preview.md)
- [Visió general dels fluxos del núvol - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visió general dels fluxos conscients de solucions - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
