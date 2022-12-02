---
title: Recuperació d'entrades aprovades prèviament
description: En aquest article s'explica com un membre de l'equip del projecte pot sol·licitar la revisió de registres de temps, despesa i ús materials prèviament enviats i aprovats, i com un administrador de projecte pot aprovar o rebutjar sol·licituds de revisió.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930352"
---
# <a name="recall-previously-approved-entries"></a>Recuperació d'entrades aprovades prèviament

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Un membre d'un equip del projecte que presenti una entrada de temps, despesa o ús de material, pot recuperar l'entrada després d'haver estat aprovada. El procés de revisió està format per dos passos principals:

1. Un remitent sol·licita una recuperació.
2. Un aprovador aprova la sol·licitud de revisió.

## <a name="request-a-recall"></a>Sol·licitar una recuperació

Seguiu aquests passos per sol·licitar la revisió d'entrades de temps, despesa o ús de material aprovades.

1. Seguiu un d'aquests passos, en funció del tipus d'entrada que vulgueu revisar:

    - Per a les entrades de temps, aneu a **Projectes** \> **La meva feina** \> **Entrada de temps** i seleccioneu totes les entrades de temps per a una combinació específica d'un projecte i una tasca. De manera alternativa, a la quadrícula, seleccioneu les cel·les individuals per al temps d'una data concreta per a un projecte concret.
    - Per a les entrades de despeses, aneu a **Projectes** \> **El meu treball** \> **Despeses** i seleccioneu la fila de l'entrada de la despesa que voleu recuperar.
    - Per a les entrades d'ús de materials, aneu a **Projectes** \> **El meu treball** \> **Registre d'ús de materials** i seleccioneu la fila de l'entrada d'ús de materials que voleu recuperar.

2. Seleccioneu **Recupera**. Apareix un quadre de diàleg de confirmació. Si les entrades de temps, despesa o ús de material seleccionades ja estaven aprovades, se us demanarà que introduïu un motiu per a la recuperació.
3. Introduïu un motiu per a la recuperació i, a continuació, seleccioneu **D'acord** per confirmar l'operació. El sistema envia a la persona que ha aprovat les entrades una sol·licitud per aprovar la recuperació.

> [!IMPORTANT]
> No podeu crear una sol·licitud de recuperació per a una entrada de temps, despesa i ús material aprovada que ja s'hagi facturat al client. Si ho intenteu, rebreu un missatge que indica que el registre de temps, despesa o ús de materials no es poden recuperar perquè ja s'han facturat. En aquest cas, podeu sol·licitar la recuperació de l'entrada només si s'utilitza una factura correctiva per emetre un abonament complet o un reemborsament al client per a la factura original.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar o rebutjar una sol·licitud de recuperació

Seguiu aquests passos per aprovar o rebutjar una sol·licitud de recuperació.

1. Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.
2. A la pàgina de llista **Aprovacions**, canvieu la visualització a **Sol·licituds de recuperació pendents d'aprovació**. Es mostra una llista de sol·licituds de recuperació enviades.
3. Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Aprova** o **Rebutja**.
4. Si heu seleccionat **Aprova**, rebreu un missatge d'advertiment que explica l'impacte de l'aprovació. Seleccioneu **D'acord** per confirmar l'operació. La sol·licitud de recuperació s'ha aprovat.

    -o bé-

    Si heu seleccionat **Rebutja**, la sol·licitud de recuperació es rebutja.

> [!IMPORTANT]
> Quan s'aprova una recuperació, igual que quan se sol·licita, el sistema comprova si hi ha activitats de facturació a les entrades de temps, despesa o ús de materials. Si una entrada ja s'ha facturat o si està en un esborrany de factura, l'aprovador rep un missatge d'error que indica que el temps o la despesa no es poden aprovar per a la recuperació, perquè ja s'han facturat. En aquest cas, l'aprovador pot sol·licitar la recuperació de l'entrada només si s'utilitza una factura correctiva per emetre un abonament complet o un reemborsament al client per a la factura original.

## <a name="impact-of-a-recall-request"></a>Impacte d'una sol·licitud de recuperació

Quan una aprovació es recupera, hi ha un impacte operacional i un impacte financer.

### <a name="operational-impact"></a>Impacte operacional

Si una sol·licitud de recuperació d'aprova, el registre d'aprovació es marca com a **Rebutjat**. L'estat de l'entrada es canvia a **Retornada** o **Rebutjada** en funció de si es tracta d'una entrada de temps o d'una entrada de despesa o d'ús de materials.

El membre del grup de projectes pot visualitzar les entrades, editar i tornar a enviar les entrades o suprimir les entrades del tot.

Si es rebutja una sol·licitud de recuperació, l'estat de l'entrada continua sent **Aprovada** i l'entrada no es pot editar pel membre de l'equip del projecte o l'aprovador del projecte.

### <a name="financial-impact"></a>Impacte financer

Si s'aprova una sol·licitud de recuperació, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:

- El camp **Estat d'ajustament** s'actualitza com a **Ajustat**.
- El camp **Estat de facturació** s'actualitza com a **Cancel·lat**.

A continuació, les entrades d'inversió es creen a la taula Valors reals. Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals. Els únics valors que no es copien són els valors de quantitat. Aquests valors s'inverteixen en el seu lloc. Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**. El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i el camp **Estat de facturació** es defineix com a **Cancel·lat**. A causa d'aquests canvis, la despesa i el registre d'entrada d'ingressos registrats al projecte ja no comptabilitzaran a les quantitats que representin aquests valors reals.

Si es rebutja una sol·licitud de recuperació, no hi ha cap impacte financer en el projecte.

## <a name="changes-to-time-entry-records"></a>Canvis en els registres d'entrada de temps

A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de temps aprovades i els registres d'aprovació corresponents quan es recuperen.

![Transicions d'estat de l'entrada de temps.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Canvis en els registres d'entrada de despeses i ús de materials

A la il·lustració següent es mostren els canvis que es produeixen per a les entrades de temps i ús de materials aprovades i els registres d'aprovació corresponents quan es recuperen.

![Transicions d'estat de l'entrada de despeses.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
