---
title: Procés de conversió de planificació del projecte del Project Service Automation al Project Operations
description: En aquest article es proporciona informació general sobre els canvis en les característiques per al Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642556"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Procés de conversió de planificació del projecte del Project Service Automation al Project Operations

Quan un projecte s'ha actualitzat correctament des del Microsoft Dynamics 365 Project Service Automation 3.X al Dynamics 365 Project Operations Lite, no és possible editar les tasques de projecte ala quadrícula de tasques d'estructura del desglossament del treball (WBS). Els clients podran revisar la WBS a la quadrícula de seguiment on s'han afegit camps nous per proporcionar tots els detalls relacionats amb la tasca. Per als projectes en què cal fer edicions a la WBS, podeu convertir selectivament els projectes elegibles a la nova experiència de planificació del Project for the Web.

## <a name="project-conversion-process"></a>Procés de conversió del projecte

Seguiu aquests passos per convertir un projecte.

1. Obriu la pàgina principal del projecte i seleccioneu **Converteix** a la subfinestra d'accions.
1. Al quadre del missatge de confirmació, seleccioneu **D'acord** per iniciar la conversió del projecte. Es produeixen les accions següents:

    1. Apareix una barra de missatges a la pàgina principal del projecte que diu: "La planificació del projecte s'està convertint. No podeu fer canvis fins al projecte fins que no es completi la conversió."
    1. Se us redirigeix a la llista de projectes.

    Un cop completada la conversió del projecte, es produeixen les accions següents:

    1. L'administrador de projecte assignat rep una notificació a la dreta de l'aplicació.
    1. La barra de missatges estableix que la conversió en curs s'està eliminant.
    1. La pestanya **Planificació** mostra l'experiència de planificació nova amb Project for the Web. Qualsevol usuari que té les llicències i funcions de seguretat adequades pot editar la WBS.
    1. El camp **Motor de planificació** s'actualitza a **Project for the Web**.
    1. El botó **Converteix** s'elimina de la subfinestra d'accions.

> [!IMPORTANT]
> No es permet la conversió massiva de projectes. Qualsevol intent d'actualitzar un gran volum de projectes al mateix temps es limitarà. Aquesta limitació ajuda a garantir un rendiment alt per a tots els clients.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tasques manuals i tasques automàtiques

Quan s'actualitza un entorn des del Project Service Automation al Project Operations, totes les tasques de la WBS es consideren planificades automàticament. El concepte de tasques planificades manualment no està disponible a Project for the Web. No obstant això , podeu definir el comportament de planificació preferit per als vostres projectes utilitzant l'opció de configuració del [mode de planificació](/project-management/scheduling-modes.md) en crear nous projectes.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operacions restringides per a projectes previs a la conversió

Aquesta secció detalla les diferències funcionals que podeu esperar quan els projectes no s'han convertit.

### <a name="copy-project"></a>Copia el projecte

L'operació **Copia** només s'admet en projectes convertits. Els projectes actualitzats no es poden copiar abans de la conversió.

### <a name="move-project"></a>Mou el producte

Un canvi en la data d'inici d'un projecte no desplaçarà proporcionalment l'inici de les tasques tret que el projecte s'hagi convertit.

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quines diferències hi ha entre els projectes convertits i els nous projectes que es creen un cop completada l'actualització?

Per als projectes convertits després que l'entorn s'hagi actualitzat, es definirà un indicador que indica a la planificació que respecti només el calendari del projecte. Aquest comportament coincideix amb el comportament del Project Service Automation. Tanmateix, l'indicador no es definirà per als projectes nous que es creen després de l'actualització. Per tant, la planificació respectarà les hores de feina dels recursos quan s'assignin a una tasca.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Què he de fer si el meu projecte no es pot convertir?

Si el vostre projecte no es pot convertir, el primer pas es revisar els registres d'error per identificar els problemes habituals relacionats amb la WBS. Si els registres no indiquen un error concret en què podeu actuar, poseu-vos en contacte amb el Servei d'atenció al client perquè puguin revisar el cas amb més profunditat.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Com es gestionen els tancaments d'empresa al Project for the Web?

El Project for the Web no respecta els tancaments d'empresa que l'empresa defineix en el nivell de l'organització. Tanmateix, es respectaran altres tipus de dies lliures que es defineixin en una plantilla d'hores de feina determinada.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quines són les limitacions del Project for the Web?

Conulteu [Crear una estructura del desglossament del treball: limitacions del projecte](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Puc esperar canvis en les meves estimacions de cost i de vendes?

En pocs casos en què es recalculen els contorns de l'assignació de recursos o en què es troben en un límit de dates diferent que el projecte d'origen, podríeu veure diferències en les estimacions de vendes i de cost. Com a part del procés d'actualització, està previst que els clients provin un conjunt de projectes d'exemple representatiu per tal que coneguin els possibles canvis en la planificació.
