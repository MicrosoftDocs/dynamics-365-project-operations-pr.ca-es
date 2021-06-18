---
title: Notes del desenvolupador per a aprovacions
description: Aquest tema proporciona informació addicional al desenvolupador sobre com treballar amb aprovacions.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996779"
---
# <a name="developer-notes-for-approvals"></a>Notes del desenvolupador per a aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació. Les transicions de registre correctes asseguren que: 

  - Totes les files de suport es creen en taules relacionades, com diaris i valors reals.
  - L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]