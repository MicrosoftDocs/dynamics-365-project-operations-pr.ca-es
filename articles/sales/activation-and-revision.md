---
title: Activar i revisar un pressupost de projecte
description: Aquest article proporciona informació sobre com activar i revisar les cotitzacions a Microsoft Dynamics 365 Project Operations.
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
# <a name="activate-and-revise-a-project-quote"></a>Activar i revisar un pressupost de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les capacitats d'activació i revisió us ajuden a fer un seguiment del versionat de les cotitzacions basades en projectes durant les fases d'estimació i negociació. Quan s'activa un esborrany d'un pressupost, passa a ser només de lectura.

Les capacitats d'activació i revisió us permeten realitzar les tasques següents:

- Guanyar o perdre cometes només després de l'activació.
- Reviseu una oferta per fer canvis a l'oferta existent o crear-ne una de nova.

> [!NOTE]
> Un cop habilitada la funció d'activació i revisió de pressupostos, no es pot desactivar.

Per activar la possibilitat d'activar i revisar les cotitzacions basades en projectes, seguiu aquests passos.

1. Aneu a **Paràmetres de configuració** \> **·**.
1. Obriu el **registre Paràmetres**.
1. A la subfinestra d'accions, a la **pestanya Control de** característiques, seleccioneu **Habilita l'activació i la revisió de les cometes**.
1. Al quadre de diàleg de confirmació, seleccioneu **D'acord**.
1. Al cap d'uns instants, actualitzeu el navegador. Les capacitats d'activació i revisió ja haurien d'estar disponibles. Sabreu que aquestes capacitats s'han habilitat si el botó Activa l'activació i la **revisió de les cometes** ja no apareix a la subfinestra d'accions.

## <a name="activating-a-quote"></a>Activació d'un pressupost

Un cop habilitada la funció d'activació i revisió de les ofertes, els botons Tanca l'oferta com a guanyada **i** Tanca l'oferta **com a perduts** de la subfinestra d'accions no estan disponibles per a les ofertes d'esborrany del projecte. Només estan disponibles després d'activar un pressupost.

L'activació representa l'etapa del procés de cotització quan voleu evitar més canvis a l'oferta. En aquesta fase, el pressupost s'envia per a la revisió interna o al client.

Els **botons Tanca l'oferta com a guanyada** i **Tanca l'oferta com a perduts** de la subfinestra d'accions estan disponibles per a les cometes activades. En funció del resultat de la revisió interna o del client, podeu utilitzar un d'aquests botons per tancar una oferta activada. Podeu fer negociacions i canvis a les cotitzacions activades seleccionant **Revisar pressupost**.

## <a name="revising-a-quote"></a>Revisió d'un pressupost

Si heu de fer canvis en una oferta activada, seleccioneu **Revisa l'oferta**. La cita es tanca i s'utilitza el **codi de motiu revisat**. A continuació, es crea una oferta nova que té el mateix identificador i un número de revisió augmentat. Tots els detalls de la cita original es copien a la nova cita. La nova cita es troba en estat d'esborrany i es pot editar segons sigui necessari.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
