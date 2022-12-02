---
title: Pàgina d'inici de les actualitzacions
description: Aquest article mostra on es troba informació important sobre les característiques noves i canviades al Dynamics 365 Project Service Automation, i el procés per actualitzar a la versió més recent.
ms.prod: ''
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
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
ms.openlocfilehash: 5dcf41af31a60b952ce82c08e3c082490d59d4f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926626"
---
# <a name="upgrade-home-page"></a>Pàgina d'inici de les actualitzacions

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Actualització de la versió de PSA 2.x o 1.x a la versió 3.x

### <a name="new-instances"></a>Noves instàncies

A partir del 17 de maig de 2019, en seleccionar el Project Service Automation durant el proveïment d'una instància nova, la versió 3.x s'instal·la per defecte.

### <a name="existing-instances"></a>Instàncies existents

Anteriorment, els clients que tinguessin una instància de la versió 2.x del PSA i que necessitessin actualitzar a la versió 3.x, que és la versió basada en la interfície de client unificada (UCI) del PSA, havien de contactar amb el suport tècnic de Microsoft i proporcionar els detalls de la seves instàncies, de manera que el servei tècnic pogués habilitar l'actualització a la versió 3.x. A partir de l'1 de març de 2020, els clients que tenen una instància de la versió 2.x de PSA i necessiten actualitzar a la versió 3.x, podran actualitzar les seves instàncies directament des del portal d'administració sense haver de contactar amb el suport tècnic de Microsoft.  

> [!NOTE]
> La versió 3.x del PSA inclou canvis significatius. S'ha construït sobre el marc de la interfície unificada per ajudar a proporcionar una experiència d'usuari millorada. L'aplicació redissenyada ofereix una interfície d'usuari (IU) coherent i homogènia, i segueix els principis de disseny responsiu per a una òptima visualització en qualsevol mida de pantalla o dispositiu. Hi ha hagut altres canvis a l'aplicació. Algunes de les àrees que s'ha canviat inclouen els preus, la reserva i l'assignació de recursos, el temps, les despeses i les aprovacions.

Abans de començar el procés d'actualització, us recomanem que completeu les tasques següents:

- Verifiqueu si tant el Dynamics 365 Field Service com el Project Service Automation estan instal·lats a la instància identificada. Si totes dues solucions estan instal·lades, heu de planificar l'actualització de tots dos abans de reprendre l'ús periòdic de la instància.
- Reviseu amb atenció els articles següents. La conscienciació i la comprensió dels canvis entre versions us ajudaran en el procés d'actualització. Aquests articles proporcionen informació sobre els canvis més importants del PSA, així com les consideracions i recomanacions per planificar l'actualització a la versió 3.x.

    - [Novetats o canvis al Project Service Automation versió 3](whats-new-changed-v3.md)
    - [Consideracions d'actualització - Project Service Automation 2.x o 1.x a la versió 3.x](upgrade-v3.md)

- Actualitzeu la instància d'espai aïllat per avaluar els canvis en la implementació abans d'actualitzar la instància de producció.

Després d'haver revisat els articles que s'han esmentat abans i que estigueu preparat per actualitzar a la versió 3.x o la versió basada en UCI, envieu una sol·licitud al suport tècnic de Microsoft per fer que l'actualització estigui disponible des del Centre d'administració. A la vostra sol·licitud, proporcioneu els detalls de la instància.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versions anteriors del PSA (versió PSA 2.x) en una instància creada recentment

A partir del 17 de maig de 2019, totes les instàncies noves tindran l'UCI com a client per defecte. En coherència amb aquest canvi, la versió 3.x de PSA i la versió 8.x del Field Service seran subministrades per defecte, perquè aquestes versions estan dissenyades per treballar amb el client UCI.

A partir de l'1 de març de 2020, els clients del Dynamics PSA ja no podran crear un nou entorn amb versions anteriors de PSA, per exemple versió 2.x de PSA o inferior. Qualsevol entorn nou només serà per obtenir la versió 3.x del PSA.

> [!NOTE]
> Per obtenir la millor experiència en utilitzar versions anteriors de les aplicacions del Field Service i el PSA, aneu a la pàgina **Configuració del sistema** i per al camp **Utilitza només la nova interfície unificada (recomanat)** seleccioneu **No**, perquè aquestes versions no estan dissenyades perquè es carreguin correctament a l'UCI. Després d'haver desactivat l'UCI, podeu obrir i executar aquestes versions de Field Service i el PSA mitjançant el client web antic. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
