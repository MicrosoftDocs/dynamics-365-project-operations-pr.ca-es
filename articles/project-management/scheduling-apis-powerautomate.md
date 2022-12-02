---
title: Ús d'API de planificació de projectes amb el Power Automate
description: Aquest article proporciona un flux d'exemple que utilitza les interfícies de programació d'aplicacions (API) de la planificació de projectes.
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

En aquest article es descriu un flux d'exemple que mostra com crear un pla de projecte complet mitjançant el Microsoft Power Automate, com crear un conjunt d'operacions i com actualitzar una entitat. A l'exemple s'explica com es crea un projecte, un membre de l'equip del projecte, conjunts d'operacions, tasques del projecte i assignacions de recursos. En aquest article també s'explica com actualitzar una entitat i executar un conjunt d'operacions.

A continuació es mostra una llista completa dels passos documentats al flux d'exemple d'aquest article:

1. [Crear un disparador del PowerApps](#1)
2. [Crear un projecte](#2)
3. [Inicialitzar una variable per al membre de l'equip](#3)
4. [Crear un membres de l'equip genèric](#4)
5. [Crear un conjunt d'operacions](#5)
6. [Crear un dipòsit de projecte](#6)
7. [Inicialitzar una variable per a l'estat de l'enllaç](#7)
8. [Inicialitzar una variable per al nombre de tasques](#8)
9. [Inicialitzar una variable per a l'ID de tasca del projecte](#9)
10. [Fer fins a](#10)
11. [Definir una tasca del projecte](#11)
12. [Crear una tasca del projecte](#12)
13. [Crear una assignació de recursos](#13)
14. [Disminuir una variable](#14)
15. [Canviar una tasca del projecte](#15)
16. [Executar un conjunt d'operacions](#16)

## <a name="assumptions"></a>Supòsits

En aquest article es dona per suposat que teniu coneixements bàsics de la plataforma Dataverse, els fluxos de núvol i la Interfície de programació d'aplicacions (API) de Planificació de projectes. Per obtenir més informació, vegeu la secció [Referències](#references) més endavant en aquest article.

## <a name="create-a-flow"></a>Creació d'un flux

### <a name="select-an-environment"></a>Permet seleccionar un entorn.

Podeu crear el flux del Power Automate a l'entorn.

1. Aneu a <https://flow.microsoft.com> i inicieu la sessió amb les credencials de l'administrador.
2. A la cantonada superior dreta, seleccioneu **Entorns**.
3. A la llista, seleccioneu l'entorn on està instal·lat el Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Crear una solució

Per crear un [flux per a la solució](/power-automate/overview-solution-flows), seguiu aquests passos. En crear un flux per a la solució, podeu exportar més fàcilment el flux per utilitzar-lo més endavant.

1. A la subfinestra de navegació, seleccioneu **Solucions**.
2. A la pàgina **Solucions**, seleccioneu **Solució nova**.
3. Al quadre de diàleg **Solució nova**, definiu els camps necessaris i seleccioneu **Crea**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Pas 1: Crear un disparador del PowerApps

1. A la pàgina **Solucions** seleccioneu la solució que heu creat i, a continuació, seleccioneu **Crea**.
2. A la subfinestra esquerra, seleccioneu **Fluxos de núvol** \> **Automatització** \> **Flux de núvol** \> **Instantani**.
3. Al camp **Nom del flux**, introduïu **Flux de demostració de l'API de planificació**.
4. A la llista **Trieu com disparar aquest flux**, seleccioneu **Power Apps**. Quan creeu un disparador del Power Apps, com a autor en decidiu la lògica. En aquest article, deixeu els paràmetres d'entrada en blanc per a les proves.
5. Seleccioneu **Crea**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pas 2: Crear un projecte

Seguiu aquests passos per crear projecte de mostra.

1. Al flux que heu creat, seleccioneu **Pas nou**.

    ![Afegir un pas nou.](media/newstep.png)

2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.

    ![Seleccionar una operació.](media/chooseactiontab.png)

3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.

![Canviar el nom d'un pas.](media/renamestep.png)

4. Canvieu el nom del pas per **Crea un projecte**.
5. Al camp **Nom de l'acció**, seleccioneu **msdyn\_CreateProjectV1**.
6. Al camp **msdyn\_subject**, seleccioneu **Afegeix contingut dinàmic**.
7. A la pestanya **Expressió**, al camp de funció, introduïu **Nom del projecte - utcNow()**.
8. Seleccioneu **D'acord**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Pas 3: Inicialitzar una variable per al membre de l'equip

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **inicialitzar una variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **membre de l'equip Init**.
5. Al camp **Nom**, introduïu **TeamMemberAction**.
6. Al camp **Tipus** seleccioneu **Cadena**.
7. Al camp **Valor**, introduïu **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Pas 4: Crear un membre de l'equip genèric

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Crear un membre de l'equip**.
5. Per al camp **Nom de l'acció**, seleccioneu **TeamMemberAction** al quadre de diàleg **Contingut dinàmic**.
6. Al camp **Paràmetres d'acció**, introduïu la informació de paràmetre següent.

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

    Aquesta es mostra una explicació dels paràmetres:

    - **\@\@odata.type**: el nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid**: la clau principal de l'ID de l'equip del projecte. El valor és una expressió d'identificador únic global (GUID).   L'ID es genera a partir de la pestanya d'expressió.

    - **msdyn\_project\@odata.bind**: l'ID del projecte del projecte propietari. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea un projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre els parèntesis. Calen cometes. Per exemple, introduïu **"/msdyn\_projects(AFEGIR CONTINGUT DINÀMIC)"**.
    - **msdyn\_name**: nom del membre de l'equip. Per exemple, introduïu **ScheduleAPIDemoTM1**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Pas 5: Crear un conjunt d'operacions

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Crea un conjunt d'operacions**.
5. Al camp **Nom de l'acció**, seleccioneu l'acció personalitzada del Dataverse **msdyn\_CreateOperationSetV1**.
6. Al camp **Descripció**, introduïu **ScheduleAPIDemoOperationSet**.
7. Al camp **Projecte**, introduïu **msdyn\_projects(**.
8. Al quadre de diàleg **Contingut dinàmic**, seleccioneu **msdyn\_CreateProjectV1Response ProjectId**.
9. Al camp **Projecte**, introduïu **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Pas 6: Crear un dipòsit de projectes

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **afegir una fila nova**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Crea un dipòsit**.
5. Al camp **Nom de la taula**, seleccioneu **Dipòsits de projectes**.
6. Al camp **Nom**, introduïu **ScheduleAPIDemoBucket1**.
7. Per al camp **Projecte**, seleccioneu **msdyn\_CreateProjectV1Response ProjectId** al quadre de diàleg **Contingut dinàmic**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Pas 7: Inicialitzar una variable per a l'estat de l'enllaç

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **inicialitzar una variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Init linkstatus**.
5. Al camp **Nom**, introduïu **linkstatus**.
6. Al camp **Tipus** seleccioneu **Enter**.
7. Al camp **Valor**, introduïu **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Pas 8: Inicialitzar una variable per al nombre de tasques

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **inicialitzar una variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Init Nombre de tasques**.
5. Al camp **Nom**, introduïu **nombre de tasques**.
6. Al camp **Tipus** seleccioneu **Enter**.
7. Al camp **Valor**, introduïu **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Pas 9: Inicialitzar una variable per a l'ID de tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **inicialitzar una variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Init ProjectTaskID**.
5. Al camp **Nom**, introduïu **nombre de tasques**.
6. Al camp **Tipus** seleccioneu **Cadena**.
7. Per al camp **Valor**, introduïu **guid()** al creador d'expressions.

## <a name="step-10-do-until"></a><a id="10"></a>Pas 10: Fer fins a

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **fer fins a**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Definiu el primer valor de la sentència condicional amb la variable **nombre de tasques** del quadre de diàleg **Contingut dinàmic**.
4. Definiu la condició com a **inferior a igual que**.
5. Definiu el segon valor de la sentència condicional en **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Pas 11: Definir una tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **definir la variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Definir tasca del projecte**.
5. Al camp **Nom**, seleccioneu **msdyn\_projecttaskid**.
6. Per al camp **Valor**, introduïu **guid()** al creador d'expressions.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Pas 12: Crear una tasca del projecte

Seguiu aquests passos per crear una tasca del projecte que tingui un identificador únic que pertany al projecte actual i el dipòsit de projectes que heu creat.

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Crear una tasca del projecte**.
5. Al camp **Nom de l'acció**, seleccioneu **msdyn\_PssCreateV1**.
6. Al camp **Entitat**, introduïu la informació de paràmetre següent.

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

    Aquesta es mostra una explicació dels paràmetres:

    - **\@\@odata.type**: el nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid**: ID únic de la tasca. El valor s'ha d'establir en una variable dinàmica de **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind**: l'ID del projecte del projecte propietari. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea un projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre els parèntesis. Calen cometes. Per exemple, introduïu **"/msdyn\_projects(AFEGIR CONTINGUT DINÀMIC)"**.
    - **msdyn\_subject**: qualsevol nom de tasca.
    - **msdyn\_projectbucket\@odata.bind**: dipòsit de projectes que conté les tasques. El valor serà el contingut dinàmic que prové de la resposta del pas "Crea un dipòsit". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre els parèntesis. Calen cometes. Per exemple, introduïu **"/msdyn\_projectbuckets(AFEGIR CONTINGUT DINÀMIC)"**.
    - **msdyn\_start**: contingut dinàmic per a la data d'inici. Per exemple, demà es representarà com **text "addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart**: la data d'inici planificada. Per exemple, demà es representarà com **text "addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend**: la data d'acabament planificada. Seleccioneu una data en el futur. Per exemple, especifiqueu **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus**: estat de l'enllaç. Per exemple, escriviu **"192350000"**.

7. Per al camp **OperationSetId**, seleccioneu **msdyn\_CreateOperationSetV1Response** al quadre de diàleg **Contingut dinàmic**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Pas 13: Crear una assignació de recursos

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Crea una assignació**.
5. Al camp **Nom de l'acció**, seleccioneu **msdyn\_PssCreateV1**.
6. Al camp **Entitat**, introduïu la informació de paràmetre següent.

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

7. Per al camp **OperationSetId**, seleccioneu **msdyn\_CreateOperationSetV1Response** al quadre de diàleg **Contingut dinàmic**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Pas 14: Disminuir una variable

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **disminuir una variable**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al camp **Nom**, seleccioneu **nombre de tasques**.
4. Al camp **Valor**, introduïu **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Pas 15: Canviar el nom d'una tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Canviar el nom d'una tasca del projecte**.
5. Al camp **Nom de l'acció**, seleccioneu **msdyn\_PssUpdateV1**.
6. Al camp **Entitat**, introduïu la informació de paràmetre següent.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Per al camp **OperationSetId**, seleccioneu **msdyn\_CreateOperationSetV1Response** al quadre de diàleg **Contingut dinàmic**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Pas 16: Executar un conjunt d'operacions

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de diàleg **Trieu una operació**, al camp de cerca, introduïu **dur a terme una acció no enllaçada**. Després, a la pestanya **Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvieu el nom del pas per **Executa un conjunt d'operacions**.
5. Al camp **Nom de l'acció**, seleccioneu **msdyn\_ExecuteOperationSetV1**.
6. Per al camp **OperationSetId**, seleccioneu **msdyn\_CreateOperationSetV1Response OperationSetId** al quadre de diàleg **Contingut dinàmic**.

## <a name="references"></a>Referències

- [Informació general sobre com integrar els fluxos amb el Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](schedule-api-preview.md)
- [Informació general dels fluxos de núvol - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Informació general dels fluxos sensibles a la solució - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
