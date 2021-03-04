---
title: Flux de treball d'administració de despeses
description: Aquest tema explica com podeu utilitzar el sistema de flux de treball al Microsoft Dynamics 365 Finance per configurar un procés de revisió per als informes de despeses a l'administració de despeses.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960550"
---
# <a name="expense-management-workflow"></a>Flux de treball d'administració de despeses

Podeu utilitzar el sistema de flux de treball per configurar un procés de revisió per als informes de despeses a l'administració de despeses. Podeu configurar un flux de treball que utilitzi els següents criteris per determinar qui aprova els informes de despeses:

- Jerarquia d'informes d'empleats i límits d'aprovació predefinits
- Aprovació de diversos nivells que admet aprovadors intermedis i un aprovador final
- Dimensions financeres i responsabilitat del projecte
- Assignació a usuaris específics o grups d'usuaris

Es poden crear aprovacions de flux de treball per a informes de despeses, peticions de viatges, avançaments d'efectiu i recuperació de l'impost sobre el valor afegit (IVA).

**Exemple**

El següent procés és un exemple del flux de treball d'administració de despeses per a un informe de despeses.

1. Un empleat crea i desa un informe de despeses.
2. L'empleat envia l'informe de despeses per a la seva aprovació. L'aprovador s'identifica en funció de les regles que es van definir quan es va configurar el flux de treball.
3. L'aprovador rep una notificació que un informe de despeses està a punt per a la seva aprovació. L'aprovador revisa l'informe de despeses i verifica que es compleixin les següents condicions:

    - Les despeses no infringeixen cap norma de despeses. Si una despesa infringeix una norma, l'aprovador verifica que l'informe de despeses inclou una justificació empresarial vàlida.
    - A l'informe de despeses s'adjunten rebuts electrònics.

4. L'aprovador aprova l'informe de despeses.
5. L'informe de despeses s'assigna al coordinador de comptes a pagar per a la comptabilització.
6. Es produeix un dels passos següents, depenent de si la comptabilització automàtica està configurada:

    - Si la comptabilització automàtica està configurada, l'informe de despeses es processa per al pagament i l'estat de l'informe de despeses s'actualitza.
    - Si no està configurada la comptabilització automàtica, el coordinador de comptes a pagar verifica que tots els rebuts originals s'han enviat i que els rebuts s'alineen amb les despeses de l'informe de despeses. Tots els codis d'impostos que s'introdueixen en l'informe de despeses també s'han de verificar com a correctes.

Després de verificar aquests requisits, es comptabilitza l'informe de despeses.

Després que es comptabilitzi l'informe de despeses, s'autoritza el pagament de l'informe de despeses i es reemborsa a l'empleat.
