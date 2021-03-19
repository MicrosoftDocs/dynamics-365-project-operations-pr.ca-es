---
title: Configuració de la integració amb targeta de crèdit
description: En aquest tema es descriu la manera d'importar i mantenir transaccions amb targetes de crèdit relacionades amb les despeses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cd60d338e2b2a2d74d4d7f55bb5a1723f10c29ab
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276156"
---
# <a name="set-up-credit-card-integration"></a>Configuració de la integració amb targeta de crèdit

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les transaccions de targetes de crèdit relacionades amb despeses es poden configurar de manera que s'importin automàticament segons una planificació periòdica. Alternativament, les transaccions es poden importar manualment a mesura que es necessitin. Les transaccions de targeta de crèdit s'importen a través de l'entitat Dades de transaccions de targeta de crèdit.

## <a name="import-credit-card-transactions"></a>Importació de transaccions de targeta de crèdit

1. A la pàgina **Transaccions de targeta de crèdit**, seleccioneu **Importa transaccions**. Si obriu l'administració de dades per primer cop, el sistema ha d'actualitzar la llista d'entitats de dades per poder continuar.
2. Al camp **Nom**, introduïu una descripció única de la feina d'importació.
3. Al camp **Format de les dades d'origen**, seleccioneu el format del fitxer que conté les transaccions de targeta de crèdit que s'importarà.
4. Seleccioneu **Carrega** i, a continuació, cerqueu i seleccioneu el fitxer que voleu importar.
5. Després d'haver carregat el fitxer, valideu l'assignació del fitxer de transaccions de targeta de crèdit i les columnes de l'entitat Dades de transaccions de targeta de crèdit seleccionant l'enllaç **Visualitza l'assignació** a la peça. Si hi ha errors d'assignació o si heu de canviar l'assignació, feu els canvis de l'assignació des de la pestanya **Visualització de l'assignació** o de la pestanya **Detalls de l'assignació**.
6. Per automatitzar les transaccions amb targeta de crèdit, seleccioneu **Crea una feina de dades periòdica**. A continuació, podeu definir la periodicitat que defineix amb quina freqüència s'han d'importar les transaccions de targeta de crèdit. Quan hàgiu acabat, trieu **D'acord**.
7. Per importar el fitxer seleccionat ara, seleccioneu **Importa**.
8. Si es produeixen errors durant la importació, podeu visualitzar el registre d'execució o les dades intermèdies per veure els errors que heu d'esmenar per garantir una importació correcta.

> [!NOTE]
> Si heu d'importar més d'un format de fitxer, heu de crear feines d'importació independents per a cada tipus de format.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>Reassignar les transaccions de targeta de crèdit per a empleats acomiadats

Després d'acomiadar un registre d'empleat, el compte dels Serveis de domini de l'Active Directory (AD DS) de l'empleat està inhabilitat. No obstant això, poden haver-hi transaccions de targetes de crèdit actives que s'hagin de comptabilitzar com a despeses i reemborsar. Des de la pàgina **Transaccions de targeta de crèdit**, podeu reassignar el treballador per a qualsevol transacció de targeta de crèdit en la qual s'hagi acomiadat l'empleat associat.

Seleccioneu una o més transaccions de targeta de crèdit i, a continuació, seleccioneu **Reassigna les transaccions**. A continuació, podeu seleccionar un altre empleat al qual assignar les transaccions de targeta de crèdit. Un cop s'hagin reassignat les transaccions de targeta de crèdit, es poden seleccionar per a un informe de despeses i pagar-se mitjançant procés habitual per al reemborsament de l'informe de despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]