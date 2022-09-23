---
title: Publicació d'informes de despeses
description: En aquest article s'explica com publicar informes de despeses.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524857"
---
# <a name="post-expense-reports"></a>Publicació d'informes de despeses

Després que s'hagi aprovat i transferit un informe de despesa al registre general, es pot comptabilitzar. Quan comptabilitzeu un informe de despeses, s'identifiquen les despeses aptes per a la recuperació de l'impost sobre el valor afegit (IVA). La tasca de verificació i recuperació dels pagaments de l'IVA s'assigna a l'empleat que s'encarrega de la verificació de l'informe de despeses.

Si les despeses derivades d'un informe de despeses es cobren a una empresa diferent de l'empresa que contracta el treballador, hauràs de verificar tant l'empresa a la qual es deuen aquestes despeses com l'empresa que les deu. Per exemple, l'empleat que va enviar un informe de despeses treballa per a l'empresa DAT però va cobrar una despesa a l'empresa DIR. En aquest cas, DAT és l'empresa a la qual es deu la despesa i DIR és l'empresa que deu la despesa. Després de verificar aquestes línies del llibre diari, podeu publicar les línies de despesa al llibre de comptabilitat general.

Per comptabilitzar un informe de despeses, a la pàgina **Informes de despeses aprovats**, seleccioneu l'informe de despeses i, a continuació, a la subfinestra d'acció, seleccioneu **Comptabilitza**.

També podeu comptabilitzar tots els informes de despeses a la llista alhora. Seleccioneu tots els informes de despeses i, a continuació, seleccioneu **Comptabilitza**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Habiliteu la possibilitat de publicar responsabilitats de despeses en moneda del proveïdor per a la funció de mètode de pagament en efectiu

La **possibilitat de publicar responsabilitats de despeses en moneda del proveïdor per a la funció de mètode** de pagament en efectiu permet publicar informes de despeses en una moneda del proveïdor per a la forma de pagament en efectiu.

Actualment, quan envieu despeses en efectiu, els informes de despeses es publiquen a la moneda comptable. A causa de la conversió d'import entre la moneda de la transacció, la moneda comptable i la moneda del proveïdor, es paga un import incorrecte als proveïdors si la data de transacció de la despesa i la data de pagament real tenen tipus de canvi diferents.

Aquesta funció garantirà que el saldo del proveïdor es registri a la moneda del proveïdor quan es publiqui l'informe de despeses.

1. Aneu a **Àrees de treball** \> **Administració de característiques**.
2. A la llista, cerqueu i seleccioneu **Capacitat per publicar la responsabilitat de despeses en la moneda del proveïdor per a la forma** de pagament en efectiu i, a continuació, seleccioneu **Habilita ara**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
