---
title: Configuració de la integració amb targeta de crèdit
description: En aquest tema s'explica com treballar amb transaccions amb targetes de crèdit relacionades amb despeses.
author: suvaidya
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51c364dff41d856e493581e1b87fd29571f641c70e7233bdebb910efbc64b983
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996199"
---
# <a name="set-up-credit-card-integration"></a>Configuració de la integració amb targeta de crèdit

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les transaccions de targetes de crèdit relacionades amb despeses es poden configurar de manera que s'importin automàticament segons una planificació periòdica. Alternativament, les transaccions es poden importar manualment a mesura que es necessitin. Les transaccions de targeta de crèdit s'importen a través de l'entitat de dades de transaccions de targeta de crèdit.

## <a name="import-credit-card-transactions"></a>Importació de transaccions de targeta de crèdit

Per importar transaccions de targeta de crèdit, seguiu aquests passos:

1. A la pàgina **Transaccions de targeta de crèdit**, seleccioneu **Importa transaccions**. Si obriu l'administració de dades per primer cop, el sistema ha d'actualitzar la llista d'entitats de dades per poder continuar.
2. Al camp **Nom**, introduïu una descripció única de la feina d'importació.
3. Al camp **Format de les dades d'origen**, seleccioneu el format del fitxer que conté les transaccions de targeta de crèdit que s'importarà.
4. Seleccioneu **Carrega** i, a continuació, cerqueu i seleccioneu el fitxer que voleu importar.
5. Després d'haver carregat el fitxer, valideu l'assignació del fitxer de transaccions de targeta de crèdit i les columnes de l'entitat Dades de transaccions de targeta de crèdit seleccionant l'enllaç **Visualitza l'assignació** a la peça. Si hi ha errors d'assignació o si heu de canviar l'assignació, feu els canvis de l'assignació des de la pestanya **Visualització de l'assignació** o de la pestanya **Detalls de l'assignació**.
6. Per automatitzar les transaccions amb targeta de crèdit, seleccioneu **Crea una feina de dades periòdica**. A continuació, podeu definir la periodicitat que defineix amb quina freqüència s'han d'importar les transaccions de targeta de crèdit. Quan hàgiu acabat, trieu **D'acord**.
7. Per importar el fitxer seleccionat ara, seleccioneu **Importa**.
8. Si s'han produït errors durant la importació, podeu visualitzar el registre d'execució o les dades intermèdies per veure els errors que heu de corregir per assegurar-vos que s'importa correctament.

> [!NOTE]
> Si heu d'importar més d'un format de fitxer, heu de crear feines d'importació independents per a cada tipus de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reassignar les transaccions de targeta de crèdit per a empleats acomiadats

Després d'acomiadar un registre d'empleat, el compte dels Serveis de domini de l'Active Directory (AD DS) de l'empleat està inhabilitat. No obstant això, poden haver-hi transaccions de targetes de crèdit actives que s'hagin de comptabilitzar com a despeses i reemborsar. A la pàgina **Transaccions de targeta de crèdit**, podeu reassignar l'empleat per a qualsevol transacció de targeta de crèdit en què l'empleat associat hagi estat acomiadat.

Seleccioneu una o més transaccions de targeta de crèdit i, a continuació, seleccioneu **Reassigna les transaccions**. A continuació, podeu seleccionar un altre empleat al qual assignar les transaccions de targeta de crèdit. Un cop s'hagin reassignat les transaccions de targeta de crèdit, es poden seleccionar per a un informe de despeses i pagar-se mitjançant procés habitual per al reemborsament de l'informe de despeses.

## <a name="delete-credit-card-transactions"></a>Suprimir transaccions de targeta de crèdit 

De vegades, després d'importar transaccions de targeta de crèdit, és possible que calgui suprimir determinades transaccions. Això podria ser perquè les transaccions són duplicades o perquè les dades no són precises. Els administradors poden utilitzar la característica **Suprimeix transaccions de targeta de crèdit** per seleccionar i suprimir transaccions de targeta de crèdit que no estan **adjuntades** a un informe de despeses. 

1. Aneu a **Tasques periòdiques** > **Suprimeix transaccions de targeta de crèdit**.
2. Seleccioneu **Filtra** i proporcioneu informació per identificar els registres que voleu incloure.
3. Seleccioneu **D'acord** per suprimir els registres. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
