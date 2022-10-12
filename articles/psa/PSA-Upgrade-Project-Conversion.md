---
title: Canvis de característiques per al Project Service Automation a Project Operations
description: Aquest article proporciona una visió general dels canvis de la característica per Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621305"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>Canvis de característiques per al Project Service Automation a Project Operations

Després que un projecte s'hagi actualitzat correctament de 3.X a Microsoft Dynamics 365 Project Service Automation Lite, no és possible editar les tasques del projecte a l'estructura de desglossament del treball de la quadrícula de Dynamics 365 Project Operations tasques (WBS). Els clients podran revisar els WBS a la quadrícula de seguiment on s'han afegit nous camps per proporcionar tots els detalls relacionats amb la tasca. Per als projectes en què es requereixen modificacions al WBS, podeu convertir selectivament els projectes elegibles al nou projecte per a l'experiència de programació web.

## <a name="project-conversion-process"></a>Procés de conversió de projectes

Per convertir un projecte, seguiu aquests passos.

1. Obriu la pàgina principal del projecte i seleccioneu **Converteix** a la subfinestra d'accions.
1. Al quadre del missatge de confirmació, seleccioneu **D'acord** per iniciar la conversió del projecte. Es produeixen les accions següents:

    1. Una barra de missatges que apareix a la pàgina principal del projecte indica: "La planificació del projecte s'està convertint. No es poden fer canvis en el projecte fins que no s'hagi completat la conversió."
    1. Se us redirigeix a la llista de projectes.

    Un cop finalitzada la conversió del projecte, es produeixen les accions següents:

    1. El gestor de projecte assignat rep una notificació a la part dreta de l'aplicació.
    1. Se suprimeix la barra de missatges que indica que la conversió està en curs.
    1. La **pestanya Planificació** mostra la nova experiència de planificació amb Project per al web. Qualsevol usuari que tingui les llicències i funcions de seguretat adequades pot editar el WBS.
    1. El **camp Motor** de planificació s'actualitza a **Project for the web**.
    1. El **botó Converteix** s'elimina de la subfinestra d'accions.

> [!IMPORTANT]
> No es permet la conversió massiva de projectes. Qualsevol intent d'actualitzar un gran volum de projectes al mateix temps serà accelerat. Aquesta limitació ajuda a garantir un alt rendiment per a tots els clients.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tasques manuals vs. tasques automàtiques

Quan s'actualitza un entorn de Project Service Automation a Project Operations, totes les tasques del WBS es consideren programades automàticament. El concepte de tasques planificades manualment no està disponible al Projecte per al web. Tanmateix, podeu definir el comportament de planificació preferit per als vostres projectes mitjançant la configuració del [mode](/project-management/scheduling-modes.md) de planificació quan creeu projectes nous.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Operacions restringides per a projectes de pre-conversió

En aquesta secció es descriuen les diferències funcionals que podeu esperar quan els projectes no s'han convertit.

### <a name="copy-project"></a>Còpia projecte

L'operació **Copy** només s'admet en projectes convertits. Els projectes actualitzats no es poden copiar abans de la conversió.

### <a name="move-project"></a>Mou el projecte

Un canvi a la data d'inici d'un projecte no mourà proporcionalment l'inici de les tasques tret que el projecte s'hagi convertit.

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quines diferències hi ha entre els projectes convertits i els nous que es creen un cop finalitzada l'actualització?

Per als projectes que es converteixen després d'actualitzar l'entorn, s'establirà una bandera que indiqui que la planificació només respecti el calendari del projecte. Aquest comportament coincideix amb el comportament del Project Service Automation. Tanmateix, la bandera no es definirà per als projectes nous que es creïn després de l'actualització. Per tant, l'horari respectarà l'horari de treball dels recursos quan s'assignin a una tasca.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Què he de fer si el meu projecte no es converteix?

Si el vostre projecte no es converteix, el primer pas és revisar els registres d'error per identificar qualsevol problema comú relacionat amb el vostre WBS. Si els registres no indiquen cap error específic sobre el qual pugueu prendre mesures, poseu-vos en contacte amb el servei d'atenció al client perquè el vostre cas es pugui revisar més endavant.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Com es gestionen els tancaments d'empreses a Project for the web?

El projecte per al web no respecta els tancaments empresarials que l'empresa defineix a nivell d'organització. No obstant això, respectarà altres tipus de dies de descans que es defineixin en una determinada plantilla d'hores de treball.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quines són les limitacions de Project for the web?

Vegeu [Crear una estructura del desglossament del treball: Limitacions](/project-management/create-wbs#project-limitations.md) del projecte.

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Puc esperar canvis en les meves estimacions de costos i vendes?

En casos excepcionals en què es tornen a calcular els contorns d'assignació de recursos o en què es troben en un límit de dates diferent del projecte d'origen, és possible que vegeu diferències en les estimacions de vendes i costos. Com a part del procés d'actualització, s'espera que els clients provin un conjunt d'exemple representatiu de projectes, de manera que puguin entendre qualsevol possible canvi de planificació.
