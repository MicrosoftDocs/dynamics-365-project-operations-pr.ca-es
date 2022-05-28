---
title: Utilitza les API de planificació del projecte amb Power Automate
description: Aquest tema proporciona un flux d'exemple que utilitza les interfícies de programació d'aplicacions de planificació del projecte (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 9708226b0955cfa6c405b9616c14765f9ebc21f7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597694"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Utilitza les API de planificació del projecte amb Power Automate

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Aquest tema descriu un flux d'exemple que mostra com crear un pla de projecte complet mitjançant Microsoft Power Automate, com crear un conjunt d'operacions i com actualitzar una entitat. L'exemple mostra com crear un projecte, un membre de l'equip del projecte, un conjunt d'operacions, tasques de projecte i assignacions de recursos. Aquest tema també explica com actualitzar una entitat i executar un conjunt d'operacions.

A continuació es mostra una llista completa dels passos que es documenten en el flux d'exemple en aquest tema:

1. [Crear un PowerApps disparador](#1)
2. [Crear un projecte](#2)
3. [Inicialitza una variable per al membre de l'equip](#3)
4. [Crear un membre genèric de l'equip](#4)
5. [Crear un conjunt d'operacions](#5)
6. [Crear una galleda de projecte](#6)
7. [Inicialitza una variable per a l'estat de l'enllaç](#7)
8. [Inicialitza una variable per al nombre de tasques](#8)
9. [Inicialitza una variable per a l'identificador de la tasca del projecte](#9)
10. [Fes-ho fins que](#10)
11. [Definir una tasca de projecte](#11)
12. [Crear una tasca de projecte](#12)
13. [Crear una assignació de recursos](#13)
14. [Decrementar una variable](#14)
15. [Canvia el nom d'una tasca de projecte](#15)
16. [Executar un conjunt d'operacions](#16)

## <a name="assumptions"></a>Supòsits

Aquest tema assumeix que teniu un coneixement bàsic de la plataforma, els fluxos en el Dataverse núvol i la interfície de programació d'aplicacions de planificació de projectes (API). Per obtenir més informació, vegeu la [secció Referències](#references) més endavant en aquest tema.

## <a name="create-a-flow"></a>Creació d'un flux

### <a name="select-an-environment"></a>Permet seleccionar un entorn.

Podeu crear el Power Automate flux en el vostre entorn.

1. Aneu a <https://flow.microsoft.com> i utilitzeu les credencials d'administrador per iniciar la sessió.
2. A l'extrem superior dret, seleccioneu **Entorns**.
3. A la llista, seleccioneu l'entorn on Dynamics 365 Project Operations està instal·lat.

### <a name="create-a-solution"></a>Crear una solució

Seguiu aquests passos per crear un [flux](/power-automate/overview-solution-flows) conscient de la solució. En crear un flux conscient de la solució, podeu exportar més fàcilment el flux per utilitzar-lo més endavant.

1. A la subfinestra de navegació, seleccioneu **Solucions**.
2. A la **pàgina Solucions**, seleccioneu **Solució nova**.
3. Al quadre de diàleg Crea una **solució**, definiu els camps obligatoris i, a continuació, seleccioneu **Crea**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Pas 1: crea un PowerApps disparador

1. A la **pàgina Solucions**, seleccioneu la solució que heu creat i seleccioneu **Crea**.
2. A la subfinestra esquerra, seleccioneu **Flux de núvols** \> **Automation** \> **Cloud flux** \> **instantani.**
3. Al camp Nom **del** flux, introduïu **Planifica el flux** de demostració de l'API.
4. A la **selecció De com activar aquesta llista de flux**, seleccioneu **Power Apps**. Quan creeu un Power Apps disparador, la lògica depèn de vosaltres com a autor. En aquest tema, deixeu els paràmetres d'entrada en blanc per a propòsits de prova.
5. Seleccioneu **Crea**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Pas 2: Crear un projecte

Seguiu aquests passos per crear un projecte d'exemple.

1. Al flux que heu creat, seleccioneu **Pas nou**.

    ![Afegir un nou pas.](media/newstep.png)

2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.

    ![Selecció d'una operació.](media/chooseactiontab.png)

3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.

![Canviar el nom d'un pas.](media/renamestep.png)

4. Canvia el nom del pas **Crea un projecte**.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **CreateProjectV1\_.**
6. A sota del **camp tema\_ msdyn**, seleccioneu **Afegeix contingut** dinàmic.
7. A la **pestanya Expressió**, al camp funció, introduïu **Nom del projecte - utcNow()**.
8. Seleccioneu **D'acord**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Pas 3: inicialitza una variable per al membre de l'equip

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** Inicialitza. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del membre **de l'equip init pas**.
5. **Al camp Nom**, introduïu **TeamMemberAction**.
6. **Al camp Tipus**, seleccioneu **Cadena**.
7. **Al camp Valor**, introduïu **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Pas 4: creeu un membre genèric de l'equip

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Crea un membre de l'equip**.
5. Per al camp Nom **de l'acció**, seleccioneu **TeamMemberAction** al quadre de **diàleg Contingut** dinàmic.
6. **Al camp Paràmetres** d'acció, introduïu la informació de paràmetres següent.

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

    - **\@\@ odata.type** : el nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_ projectteam".**
    - **msdyn\_ projectteamid** – La clau principal de l'identificador de l'equip del projecte. El valor és una expressió d'identificador únic (GUID) global.   L'identificador es genera des de la pestanya expressió.

    - **msdyn\_ project\@ odata.bind** – L'identificador del projecte del projecte propietari. El valor serà contingut dinàmic que prové de la resposta del pas "Crea un projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Es requereixen cometes. Per exemple, introduïu **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **Nom\_ msdyn**: el nom del membre de l'equip. Per exemple, introduïu **"ScheduleAPIDemoTM1".**

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Pas 5: crea un conjunt d'operacions

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Crea un conjunt** d'operacions.
5. **Al camp Nom** de l'acció, seleccioneu l'acció **personalitzada msdyn\_ CreateOperationSetV1** Dataverse.
6. **Al camp Descripció**, introduïu **ScheduleAPIDemoOperationSet**.
7. **Al camp Projecte**, introduïu **/msdyn\_ projects(**.
8. Al quadre de **diàleg Contingut** dinàmic, seleccioneu **msdyn\_ CreateProjectV1Response ProjectId**.
9. **Al camp Projecte**, introduïu **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Pas 6: creeu una galleda de projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **afegeix una fila** nova. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Crea una galleda**.
5. Al camp Nom **de la** taula, seleccioneu **Cubells del projecte**.
6. **Al camp Nom**, introduïu **ScheduleAPIDemoBucket1**.
7. Per al **camp Projecte**, seleccioneu **msdyn\_ CreateProjectV1Response ProjectId** al quadre de **diàleg Contingut** dinàmic.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Pas 7: inicialitza una variable per a l'estat de l'enllaç

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** Inicialitza. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Init linkstatus**.
5. **Al camp Nom**, introduïu **linkstatus**.
6. **Al camp Tipus**, seleccioneu **Enter**.
7. **Al camp Valor**, introduïu **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Pas 8: inicialitza una variable per al nombre de tasques

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** Inicialitza. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Nombre d'init de tasques**.
5. **Al camp Nom**, introduïu **el nombre de tasques**.
6. **Al camp Tipus**, seleccioneu **Enter**.
7. **Al camp Valor**, introduïu **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Pas 9: inicialitza una variable per a l'identificador de la tasca del projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** Inicialitza. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Init ProjectTaskID**.
5. **Al camp Nom**, introduïu **el nombre de tasques**.
6. **Al camp Tipus**, seleccioneu **Cadena**.
7. Per al **camp Valor**, introduïu **GUID()** al creador d'expressions.

## <a name="step-10-do-until"></a><a id="10"></a> Pas 10: Feu-ho fins que

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **fes fins**. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Estableix el primer valor de la declaració condicional al **nombre de tasques variables des** del **quadre de diàleg Contingut** dinàmic.
4. Estableix la condició en **menys del mateix a**.
5. Estableix el segon valor de la declaració condicional a **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Pas 11: definiu una tasca de projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** establerta. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas nou, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom de la **tasca del conjunt de passos del** projecte.
5. **Al camp Nom**, seleccioneu **msdyn\_ projecttaskid**.
6. Per al **camp Valor**, introduïu **GUID()** al creador d'expressions.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Pas 12: crea una tasca de projecte

Seguiu aquests passos per crear una tasca de projecte que tingui un identificador únic que pertany al projecte actual i a la galleda del projecte que heu creat.

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Crea una tasca de projecte**.
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

    - **\@\@ odata.type** : el nom de l'entitat. Per exemple, introduïu **"Microsoft.Dynamics.CRM.msdyn\_ projecttask".**
    - **msdyn\_ projecttaskid** : L'identificador únic de la tasca. El valor s'ha d'establir en una variable dinàmica a partir de **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – L'identificador del projecte del projecte propietari. El valor serà contingut dinàmic que prové de la resposta del pas "Crea un projecte". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Es requereixen cometes. Per exemple, introduïu **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **tema msdyn\_**: qualsevol nom de tasca.
    - **msdyn\_ projectbucket\@ odata.bind** – La galleda del projecte que conté les tasques. El valor serà contingut dinàmic que prové de la resposta del pas "Crea cub". Assegureu-vos d'introduir el camí complet i afegir contingut dinàmic entre parèntesis. Es requereixen cometes. Per exemple, introduïu **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **inici\_ msdyn**: contingut dinàmic per a la data d'inici. Per exemple, demà es representarà com a **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** : la data d'inici programada. Per exemple, demà es representarà com a **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** : la data de finalització programada. Seleccioneu una data en el futur. Per exemple, especifiqueu **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** : L'estat de l'enllaç. Per exemple, introduïu **"192350000".**

7. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Pas 13: crea una assignació de recursos

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Crea una tasca**.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **PssCreateV1\_.**
6. **Al camp Entitat**, introduïu la informació del paràmetre següent.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Per al **camp OperationSetId**, seleccioneu **msdyn\_ CreateOperationSetV1Response** al **quadre de diàleg Contingut** dinàmic.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Pas 14: Decrementa una variable

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **la variable** decrement. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. **Al camp Nom**, seleccioneu **el nombre de tasques**.
4. **Al camp Valor**, introduïu **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Pas 15: canvia el nom d'una tasca de projecte

1. Al flux, seleccioneu **Pas nou**.
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del pas **Canvia el nom de la tasca** del projecte.
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
2. Al quadre de **diàleg Trieu una operació**, al camp de cerca, introduïu **Realitza una acció** sense límits. A continuació, a la **pestanya Accions**, seleccioneu l'operació a la llista de resultats.
3. Al pas, seleccioneu l'el·lipsi (**...**) i, a continuació, seleccioneu **Canvia el nom**.
4. Canvia el nom del conjunt d'operacions Executa el **pas**.
5. Al camp Nom de l'acció **, seleccioneu** msdyn **ExecuteOperationSetV1\_.**
6. Per al camp OperationSetId, seleccioneu **msdyn** CreateOperationSetV1Response OperationSetId **al quadre de \_ diàleg Denamid content**.**·**

## <a name="references"></a>Referències

- [Visió general de com integrar els fluxos amb Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Utilitzar les API de planificació de projectes per fer operacions amb entitats de planificació](schedule-api-preview.md)
- [Visió general dels fluxos del núvol - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Visió general dels fluxos conscients de la solució - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
