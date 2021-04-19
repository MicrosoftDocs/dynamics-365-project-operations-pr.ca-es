---
title: Rendiment de propostes de factura de projecte
description: Aquest tema proporciona informació sobre millores de rendiment a les propostes de factures de projectes.
author: Yowelle
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 78c924cba8107471a5f8e6d6a38265890d32d72b
ms.sourcegitcommit: 2350c6f3728067a8298adde640e6fdd5984eb077
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "5573547"
---
# <a name="project-invoice-proposal-performance"></a>Rendiment de propostes de factura de projecte

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Quan creeu una proposta de factura nova, és possible que trobeu problemes de rendiment a mesura que augmenti el nombre de projectes i subprojectes. Per millorar el rendiment, hi ha disponible una característica que redueix el temps necessari per crear una nova proposta de factura per a les transaccions de projectes comptabilitzades.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Habilitar la millora del rendiment de la proposta de factura del projecte
Per habilitar la característica de millora del rendiment de la proposta de factura del projecte, seguiu els passos següents.

1.  Aneu a **Administració de característiques** > **Totes**. A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.
2.  Seleccioneu **Habilita ara**.
3.  Actualitzeu el navegador i, a continuació, creeu una proposta de factura nova.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Desactiveu la millora del rendiment de la proposta de factura del projecte
Completeu els passos a continuació per desactivar la millora del rendiment de la proposta de factura del projecte.

1.  Aneu a **Administració de característiques** > **Totes**. A la llista de característiques, localitzeu **Millora del rendiment de la proposta de factura del projecte**.
2.  Seleccioneu **Inhabilita**.
3.  Actualitzeu el navegador.

> [!NOTE]
> El rendiment de la proposta de factura no es pot aplicar quan les regles de facturació estan habilitades o els processos per lots s'estan executant.
