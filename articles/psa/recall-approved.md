---
title: Recuperar entrades de temps o de despeses aprovades
description: En aquest tema es proporciona informació sobre com recuperar una transacció de despesa i temps de projecte aprovada anteriorment.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 71f75c1c516ca6e652baf311aa14e0c3fd4ba81e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998174"
---
# <a name="recall-approved-time-or-expense-entries"></a>Recuperar entrades de temps o de despeses aprovades

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un membre d'un equip del projecte o una altra persona que presenti una entrada de temps o de despesa, pot recuperar l'entrada de temps o despesa després d'haver estat aprovada. El procés de recuperació d'una entrada de temps o de despesa té dos passos:

1. Un remitent sol·licita una recuperació.
2. Un aprovador aprova la recuperació.

## <a name="request-a-recall"></a>Sol·licitar una recuperació

Seguiu aquests passos per sol·licitar la recuperació d'una entrada de temps o de despesa aprovada.

1. Per a les entrades de temps, aneu a **Projectes** \> **El meu treball** \> **Entrada de temps**.

    -o bé-

    Per a les entrades de despeses, aneu a **Projectes** \> **El meu treball** \> **Despeses**.

2. Per a entrades de temps, seleccioneu totes les entrades de temps per a una combinació específica d'un projecte i una tasca. De manera alternativa, a la quadrícula, seleccioneu les cel·les individuals per al temps d'una data concreta per a un projecte concret.

    -o bé-

    Per a les entrades de despeses, seleccioneu la fila de l'entrada de la despesa que voleu recuperar.

3. Seleccioneu **Recupera**. Apareix un quadre de diàleg de confirmació. Si les entrades de temps i de despeses seleccionades ja estaven aprovades, se us demanarà que introduïu un motiu per a la recuperació.
4. Introduïu un motiu per a la recuperació i, a continuació, seleccioneu **D'acord** per confirmar l'operació. El sistema envia a la persona que ha aprovat les entrades una sol·licitud per aprovar la recuperació.

> [!NOTE]
> Tot i que les entrades de temps i de despeses aprovades es poden recuperar, si un temps o una despesa aprovada ja s'ha facturat al client, no es pot crear una sol·licitud de recuperació. Un usuari que provi de crear una sol·licitud de recuperació rebrà un missatge que indica que el temps o la despesa no es poden recuperar perquè ja s'han facturat.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar o rebutjar una sol·licitud de recuperació

Seguiu aquests passos per aprovar o rebutjar una sol·licitud de recuperació.

1. Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.
2. A la pàgina de llista **Aprovacions**, canvieu la visualització a **Sol·licituds de recuperació pendents d'aprovació**. Es mostra una llista de sol·licituds de recuperació enviades.
3. Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Aprova** o **Rebutja**.
4. Si heu seleccionat **Aprova**, rebreu un missatge d'advertiment que explica l'impacte de l'aprovació. Seleccioneu **D'acord** per confirmar l'operació. La sol·licitud de recuperació s'ha aprovat.

    -o bé-

    Si heu seleccionat **Rebutja**, la sol·licitud de recuperació es rebutja.

> [!NOTE]
> Com quan es demana una recuperació, quan s'aprova una recuperació, el sistema comprova si hi ha activitats de facturació a les entrades de temps o de despeses. Si una entrada ja s'ha facturat o si està en un esborrany de factura, l'aprovador rebrà un missatge d'error que indica que el temps o la despesa no es poden aprovar per a la recuperació, perquè ja s'han facturat.

## <a name="impact-of-a-recall-request"></a>Impacte d'una sol·licitud de recuperació

Quan una aprovació es recupera, hi ha un impacte operacional i un impacte financer.

### <a name="operational-impact"></a>Impacte operacional

Si una sol·licitud de recuperació d'aprova, el registre d'aprovació es marca com a **Rebutjat**. L'estat de l'entrada es canvia a **Retornada** o **Rebutjada** en funció de si es tracta d'una entrada de temps o d'una entrada de despesa.

El membre del grup de projectes pot visualitzar les entrades, editar i tornar a enviar les entrades o suprimir les entrades del tot.

Si es rebutja una sol·licitud de recuperació, l'estat de l'entrada continua sent **Aprovada** i l'entrada no es pot editar pel membre de l'equip del projecte o l'aprovador del projecte.

### <a name="financial-impact"></a>Impacte financer

Si s'aprova una sol·licitud de recuperació, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:

- El camp **Estat d'ajustament** s'actualitza com a **Ajustat**.
- El camp **Estat de facturació** s'actualitza com a **Cancel·lat**.

A continuació, les entrades d'inversió es creen a la taula Valors reals. Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals. Els únics valors que no es copien són els valors de quantitat. Aquests valors s'inverteixen en el seu lloc. Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**. El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i el camp **Estat de facturació** es defineix com a **Cancel·lat**. A causa d'aquests canvis, la despesa i el registre d'entrada d'ingressos registrats al projecte ja no comptabilitzaran a les quantitats que representin aquests valors reals.

Si es rebutja una sol·licitud de recuperació, no hi ha cap impacte financer en el projecte.

## <a name="changes-to-time-entry-records"></a>Canvis en els registres d'entrada de temps

A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de temps aprovades quan es recuperen.

![Transicions d'estat de l'entrada de temps](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Canvis en els registres d'entrada de despeses

A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de despeses aprovades quan es recuperen.

![Transicions d'estat de l'entrada de despeses](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]