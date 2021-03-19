---
title: Notes del desenvolupador per a aprovacions
description: Aquest tema proporciona informació addicional al desenvolupador sobre com treballar amb aprovacions.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290257"
---
# <a name="developer-notes-for-approvals"></a>Notes del desenvolupador per a aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació. Les transicions de registre correctes asseguren que: 

  - Totes les files de suport es creen en taules relacionades, com diaris i valors reals.
  - L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]