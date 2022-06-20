---
title: Notes del desenvolupador per a aprovacions
description: En aquest article s'ofereix informació addicional per als desenvolupadors sobre com treballar amb aprovacions.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: df3e27f95bffb9c169644fa3e42ff1e9b2b6ff54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924740"
---
# <a name="developer-notes-for-approvals"></a>Notes del desenvolupador per a aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació. Les transicions de registre correctes asseguren que: 

  - Totes les files de suport es creen en taules relacionades, com diaris i valors reals.
  - L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]