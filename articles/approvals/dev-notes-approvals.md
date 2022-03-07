---
title: Notes del desenvolupador per a aprovacions
description: Aquest tema proporciona informació addicional al desenvolupador sobre com treballar amb aprovacions.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cfa4928eda286bee298a2c33f4e9c25b576f495795fc2deda33b393e372465b1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991654"
---
# <a name="developer-notes-for-approvals"></a>Notes del desenvolupador per a aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació. Les transicions de registre correctes asseguren que: 

  - Totes les files de suport es creen en taules relacionades, com diaris i valors reals.
  - L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]