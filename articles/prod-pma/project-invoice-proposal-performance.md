---
title: Rendiment de propostes de factura de projecte
description: Aquest tema proporciona informació sobre millores de rendiment a les propostes de factures de projectes.
author: Yowelle
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0e7a9eedc80a88e80b7788be4fe4b2f969be8ba1
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999479"
---
# <a name="project-invoice-proposal-performance"></a>Rendiment de propostes de factura de projecte

[!include [banner](../includes/banner.md)]

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
