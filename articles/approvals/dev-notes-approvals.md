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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483936"
---
# <a name="developer-notes-for-approvals"></a>Notes del desenvolupador per a aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació. Les transicions de registre correctes asseguren que: 

  - Totes les files de suport es creen en taules relacionades, com diaris i valors reals.
  - L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.
