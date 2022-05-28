---
title: Recorda les entrades aprovades prèviament
description: Aquest tema explica com un membre de l'equip del projecte pot sol·licitar la recuperació dels registres de temps, despesa i ús de material prèviament enviats i aprovats, i com un gestor de projectes pot aprovar o rebutjar sol·licituds de recuperació.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 18796e803ff73806aaa60b453048ee3160406b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586562"
---
# <a name="recall-previously-approved-entries"></a>Recorda les entrades aprovades prèviament

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Un membre de l'equip del projecte que presenti una entrada de temps, despesa o ús de material pot recordar aquesta entrada després d'haver estat aprovada. El procés de recuperació té dos passos principals:

1. Un remitent sol·licita una recuperació.
2. Un aprovador aprova la sol·licitud de retirada.

## <a name="request-a-recall"></a>Sol·licitar una recuperació

Seguiu aquests passos per sol·licitar la recuperació de les entrades de temps, despesa o ús de material aprovades.

1. Segueix un d'aquests passos, en funció del tipus d'entrada que vulguis recordar:

    - Per a les entrades de temps, aneu a **Project** \> **My Work** \> **Time Entry** i seleccioneu totes les entrades de temps per a una combinació específica d'un projecte i una tasca. De manera alternativa, a la quadrícula, seleccioneu les cel·les individuals per al temps d'una data concreta per a un projecte concret.
    - Per a les entrades de despeses, aneu a **Projectes** \> **Les meves despeses de** treball \>**i** seleccioneu la fila per a l'entrada de despeses que voleu recuperar.
    - Per a les entrades d'ús de material, aneu al **Registre d'ús de material de projectes** \> **i** \> **seleccioneu la fila per a l'entrada d'ús de material que voleu recuperar.**

2. Seleccioneu **Recupera**. Apareix un quadre de diàleg de confirmació. Si les entrades d'ús de temps, despesa o ús de material seleccionades ja s'han aprovat, se us demanarà que introduïu un motiu per a la retirada.
3. Introduïu un motiu per a la recuperació i, a continuació, seleccioneu **D'acord** per confirmar l'operació. El sistema envia a la persona que ha aprovat les entrades una sol·licitud per aprovar la recuperació.

> [!IMPORTANT]
> No podeu crear una sol·licitud de recuperació per a una entrada de temps, despesa o ús de material aprovada que ja s'ha facturat al client. Si ho intenteu, rebreu un missatge que indica que l'entrada de temps, despesa o ús de material no es pot recuperar perquè ja s'ha facturat. En aquest cas, només es pot sol·licitar la retirada de l'entrada si s'utilitza una factura correctiva per emetre un crèdit complet o reembossament al client a la factura original.

## <a name="approve-or-reject-a-recall-request"></a>Aprovar o rebutjar una sol·licitud de recuperació

Seguiu aquests passos per aprovar o rebutjar una sol·licitud de recuperació.

1. Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.
2. A la pàgina de llista **Aprovacions**, canvieu la visualització a **Sol·licituds de recuperació pendents d'aprovació**. Es mostra una llista de sol·licituds de recuperació enviades.
3. Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Aprova** o **Rebutja**.
4. Si heu seleccionat **Aprova**, rebreu un missatge d'advertiment que explica l'impacte de l'aprovació. Seleccioneu **D'acord** per confirmar l'operació. La sol·licitud de recuperació s'ha aprovat.

    -o bé-

    Si heu seleccionat **Rebutja**, la sol·licitud de recuperació es rebutja.

> [!IMPORTANT]
> Quan s'aprova una retirada, de la mateixa manera que quan se sol·licita, el sistema comprova si hi ha cap activitat de facturació en les entrades de temps, despesa o ús de material. Si una entrada ja s'ha facturat o si es troba en un esborrany de factura, l'aprovador rep un missatge d'error que indica que el temps o la despesa no es poden aprovar per a la seva retirada perquè ja s'ha facturat. En aquest cas, l'aprovant només pot aprovar la retirada si s'utilitza una factura correctiva per emetre un crèdit complet o reembossament al client a la factura original.

## <a name="impact-of-a-recall-request"></a>Impacte d'una sol·licitud de recuperació

Quan una aprovació es recupera, hi ha un impacte operacional i un impacte financer.

### <a name="operational-impact"></a>Impacte operacional

Si una sol·licitud de recuperació d'aprova, el registre d'aprovació es marca com a **Rebutjat**. L'estat de l'entrada es canvia a **Retornat o** Rebutjat **, depenent de si es tracta d'una entrada de temps o d'una entrada de despesa o ús de** material.

El membre de l'equip del projecte pot visualitzar entrades, editar i tornar a enviar entrades o suprimir completament les entrades.

Si es rebutja una sol·licitud de recuperació, l'estat de l'entrada continua sent **Aprovada** i l'entrada no es pot editar pel membre de l'equip del projecte o l'aprovador del projecte.

### <a name="financial-impact"></a>Impacte financer

Si s'aprova una sol·licitud de recuperació, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:

- El camp **Estat d'ajustament** s'actualitza com a **Ajustat**.
- El camp **Estat de facturació** s'actualitza com a **Cancel·lat**.

A continuació, les entrades d'inversió es creen a la taula Valors reals. Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals. Els únics valors que no es copien són els valors de quantitat. Aquests valors s'inverteixen en el seu lloc. Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**. El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i el camp **Estat de facturació** es defineix com a **Cancel·lat**. A causa d'aquests canvis, la despesa i el registre d'entrada d'ingressos registrats al projecte ja no comptabilitzaran a les quantitats que representin aquests valors reals.

Si es rebutja una sol·licitud de recuperació, no hi ha cap impacte financer en el projecte.

## <a name="changes-to-time-entry-records"></a>Canvis en els registres d'entrada de temps

La il·lustració següent mostra els canvis que es produeixen per a les entrades de temps aprovades i els registres d'aprovació corresponents quan es retiren.

![Transicions d'estat d'entrada de temps.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Canvis en els registres d'entrada de despeses i ús de material

La il·lustració següent mostra els canvis que es produeixen per a les entrades de despeses i ús de material aprovades i els registres d'aprovació corresponents quan es retiren.

![Transició de l'estat d'entrada de despeses.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
