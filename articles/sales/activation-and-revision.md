---
title: Activar i revisar una oferta de projecte
description: Aquest article proporciona informació sobre l'activació i la revocació d'ofertes al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410368"
---
# <a name="activate-and-revise-a-project-quote"></a>Activar i revisar una oferta de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les capacitats d'activació i revisió us ajuden a fer un seguiment de les versions de les ofertes basades en projectes durant les fases d'estimació i revisió. Quan s'activa un esborrany d'una oferta, passa a ser només de lectura.

Les capacitats d'activació i revisió us permeten dur a terme les tasques següents:

- Guanyar o perdre ofertes només després de l'activació.
- Revisar una oferta per fer canvis a l'oferta existent o crear una versió nova.

> [!NOTE]
> Després d'habilitar la característica per a l'activació i la revisió de les ofertes, no es pot inhabilitar.

Per activar i revisar les ofertes basades en projectes, seguiu aquests passos:

1. Aneu a **Configuració** \> **Paràmetres**.
1. Obriu el registre **Paràmetres**.
1. A la subfinestra Acció, a la pestanya **Control de característica**, seleccioneu **Habilita l'activació i la revisió d'ofertes**.
1. Al quadre de diàleg de confirmació, seleccioneu **D'acord**.
1. Al cap d'uns moments, actualitzeu el navegador. Ara, les capacitats d'activació i revisió haurien d'estar disponibles. Sabreu que aquestes capacitats s'han habilitat si el botó **Habilita l'activació i la revisió per a les ofertes** ja no apareix a la subfinestra Acció.

## <a name="activating-a-quote"></a>Activar una oferta

Un cop habilitada la característica per a l'activació i la revisió de les ofertes, els botons **Tanca l'oferta com a guanyada** i **Tanca l'oferta com a perduda** a la subfinestra Acció no estan disponibles per a les ofertes de projecte en fase d'esborrany. Només estan disponibles quan s'activa una oferta.

L'activació representa la fase del procés d'ofertes en què es vol impedir fer més canvis a l'oferta. En aquesta fase, l'oferta s'envia per a la revisió interna o al client.

Els botons **Tanca l'oferta com a guanyada** i **Tanca l'oferta com a perduda** a la subfinestra Acció estan disponibles per a les ofertes activades. Segons el resultat de la revisió interna o del client, podeu utilitzar un d'aquests botons per tancar una oferta activada. Per fer negociacions i canvis en les ofertes activades, seleccioneu **Revisa l'oferta**.

## <a name="revising-a-quote"></a>Revisar una oferta

Si heu de fer canvis en una oferta activada, seleccioneu **Revisa l'oferta**. L'oferta es tanca i s'utilitza el codi de raó **revisada**. A continuació es crea una oferta nova que té el mateix identificador i un número de revisió incrementat. Tots els detalls de l'oferta original es copien a l'oferta nova. L'oferta nova està en estat d'esborrany i es pot editar segons calgui.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
