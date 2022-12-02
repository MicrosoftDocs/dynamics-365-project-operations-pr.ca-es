---
title: Cancel·lar entrades de temps i de despeses aprovades prèviament
description: En aquest article es proporciona informació sobre com cancel·lar una transacció de despesa i temps de projecte aprovada.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
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
ms.openlocfilehash: 840f163ee9bf1fc98f140efdcc0d37a5424ddb8f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933296"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Cancel·lar entrades de temps o de despeses aprovades prèviament

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A la versió més recent del Dynamics 365 Project Service Automation, els aprovadors poden cancel·lar les entrades de temps o de despeses que prèviament s'havien aprovat.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Cancel·lar una entrada de temps o de despeses aprovada prèviament

Seguiu aquests passos per cancel·lar una entrada de temps o de despesa que hàgiu aprovat prèviament.

1. Aneu a **Projectes** \> **El meu treball** \> **Aprovacions**.
2. A la pàgina de llista **Aprovacions**, canvieu la visualització a **Les meves aprovacions anteriors**. Es mostra una llista de les entrades de temps i de despesa que heu aprovat prèviament.
3. Seleccioneu una o diverses entrades i, a continuació , seleccioneu **Cancel·la l'aprovació**. Rebeu un missatge d'advertiment.
4. Seleccioneu **D'acord** per cancel·lar l'aprovació.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Entendre l'impacte de cancel·lar una aprovació d'entrada de temps o de despesa

Quan una aprovació es cancel·la, hi ha un impacte operacional i un impacte financer.

### <a name="operational-impact"></a>Impacte operacional

A la part de les operacions, quan es cancel·la una aprovació, l'estat del registre es restableix a **Esborrany** i l'aprovació ja no apareix a la visualització **Les meves aprovacions anteriors**. En lloc d'això, l'aprovació cancel·lada es mostra a la visualització **Entrades de temps per a l'aprovació** o **Entrades de despesa per a l'aprovació**, en funció de si era una entrada de temps o de despeses. A més, l'estat de l'entrada relacionada de temps o despeses es canvia a **Enviada**, de manera que l'entrada relacionada sigui coherent amb les aprovacions que tenen un estat **Esborrany**.

Com a aprovador, podeu editar alguns dels camps d'una aprovació que té l'estat **Esborrany**. Aquests camps inclouen **Tipus de facturació** i **Hores facturables per ales entrades de temps**. Després de fer canvis, podeu aprovar el registre de nou. O bé, podeu rebutjar l'entrada. Si rebutgeu l'aprovació d'una entrada de temps, l'estat de l'entrada es canvia a **Retornada**. Si rebutgeu l'aprovació d'una entrada de despeses, l'estat de l'entrada es canvia a **Rebutjada**. Funcionalment, tant les entrades retornades com rebutjades es comporten igualment com una entrada que té un estat **Esborrany**. Un membre de l'equip del projecte pot fer els canvis necessaris a l'entrada i després tornar-la a enviar per a la seva aprovació o suprimir l'entrada per complet.

### <a name="financial-impact"></a>Impacte financer

Un projecte també es veu afectat financerament quan es cancel·la una aprovació. En primer lloc, els valors reals corresponents al cost i les vendes s'actualitzen de la següent manera:

- L'estat d'ajustament es defineix com a **Ajustat**.
- L'estat de facturació es defineix com a **Cancel·lat**.

A continuació, les entrades d'inversió es creen a la taula Valors reals. Per crear entrades d'inversió, el sistema copia els valors de camp dels valors reals originals. Els únics valors que no es copien són els valors de quantitat. Aquests valors s'inverteixen en el seu lloc. Els valors reals invertits es creen per als valors reals **Cost** i **Vendes no facturades**. El camp **Estat d'ajustament** dels valors reals invertits es defineix com a **No ajustable** i l'estat de facturació es defineix com a **Cancel·lat**.

Després de fer aquests canvis, l'import que s'ha registrat com a invertit en el projecte i el registre d'entrada d'ingressos del projecte ja no comptabilitzarà per a les quantitats que representin aquests valors reals.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
