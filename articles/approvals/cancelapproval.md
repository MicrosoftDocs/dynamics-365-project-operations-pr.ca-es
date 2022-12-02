---
title: Cancel·lar l'aprovació de les entrades aprovades anteriorment
description: En aquest article s'explica com un administrador de projecte pot cancel·lar l'aprovació de les entrades de temps, despesa o ús de materials prèviament aprovades.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930444"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Cancel·lar l'aprovació de les entrades aprovades anteriorment

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Un administrador de projecte o aprovador que ha aprovat prèviament entrades de temps, despesa o ús de materials, en pot cancel·lar l'aprovació. 

Seguiu aquests passos per cancel·lar l'aprovació d'una entrada de temps, de despesa o ús de materials que hàgiu aprovat prèviament.

1. Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.
2. A la pàgina de llista **Aprovacions** es mostren totes les entrades de temps pendents d'aprovació. Canvieu la visualització a **Les meves aprovacions anteriors**.
3. Seleccioneu les aprovacions de temps, despesa o materials que voleu cancel·lar. A continuació, a la subfinestra Acció, seleccioneu **Cancel·la l'aprovació**.
4. Al quadre del missatge de confirmació que apareix, seleccioneu **D'acord** per confirmar l'operació.

> [!IMPORTANT]
> No podeu cancel·lar l'aprovació d'una entrada de temps, despesa i ús material prèviament aprovada que ja s'hagi facturat al client. Si ho intenteu, rebeu un missatge que indica que la aprovació no es pot cancel·lar perquè ja s'ha facturat. En aquest cas, podeu cancel·lar l'aprovació només si s'utilitza una factura correctiva per emetre un abonament complet o un reemborsament al client per a la factura original.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impacte de la cancel·lació de l'aprovació d'una entrada prèviament aprovada

Quan una aprovació es cancel·la, hi ha un impacte operacional i un impacte financer.

### <a name="operational-impact"></a>Impacte operacional

Si es cancel·la l'aprovació d'una entrada, el registre d'aprovació es marca com a **Enviat**. L'estat de l'entrada es canvia a **Enviat**. En aquesta fase, un membre de l'equip del projecte pot recuperar l'entrada sense enviar una sol·licitud de retirada.

L'aprovador pot canviar els valors de **Quantitat facturable** i **Tipus de facturació** i, a continuació, aprovar l'entrada una altra vegada.

### <a name="financial-impact"></a>Impacte financer

Si es cancel·la l'aprovació d'una entrada, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:

- El camp **Estat d'ajustament** s'actualitza com a **Ajustat**.
- El camp **Estat de facturació** s'actualitza com a **Cancel·lat**.

A continuació, les entrades d'inversió es creen a la taula Valors reals. Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals. Els únics valors que no es copien són els valors de quantitat. Aquests valors s'inverteixen en el seu lloc. Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**. El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i el camp **Estat de facturació** es defineix com a **Cancel·lat**. A causa d'aquests canvis, la despesa i el registre d'entrada d'ingressos registrats al projecte ja no comptabilitzaran a les quantitats que representin aquests valors reals.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
