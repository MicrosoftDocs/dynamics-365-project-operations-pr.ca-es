---
title: Importació i manteniment de transaccions de targeta de crèdit
description: En aquest tema es descriu la manera d'importar i mantenir transaccions amb targetes de crèdit relacionades amb les despeses. Aquestes transaccions es poden establir de manera que s'importin automàticament segons una planificació recurrent, o es poden importar manualment quan es necessitin.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: edeab157aa2fa6cf518ad086b4c1f22c5b45fa04
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005149"
---
# <a name="import-and-maintain-credit-card-transactions"></a>Importació i manteniment de transaccions de targeta de crèdit

Les transaccions de targetes de crèdit relacionades amb despeses es poden configurar de manera que s'importin automàticament segons una planificació periòdica. Alternativament, les transaccions es poden importar manualment a mesura que es necessitin. Les transaccions de targeta de crèdit s'importen a través de l'entitat Dades de transaccions de targeta de crèdit.

Per a més informació sobre les entitats de dades, vegeu [Entitats de dades](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).

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