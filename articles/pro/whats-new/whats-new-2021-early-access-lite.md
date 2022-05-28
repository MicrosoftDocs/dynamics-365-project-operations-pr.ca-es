---
title: "Novetats de l'accés anticipat 2 de 2021: implementació bàsica del Project Operations"
description: En aquest tema es proporciona informació sobre les característiques disponibles a la versió d'accés anticipat 2 de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7b5f3528e4b4e615b8e7f24bfd3702746fd584c9
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723664"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Novetats de l'accés anticipat 2 de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.23.0.4

La versió només s'aplica quan s'ha [optat per un entorn d'accés anticipat](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

[Administració de subcontracte](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview): aquesta característica proporciona una millor visibilitat i control sobre tots els aspectes del treball d'un projecte. La visualització prèvia de l'administració de subcontracte inclou les capacitats següents:

  - Un administrador de projectes pot crear un subcontracte amb un proveïdor. Per defecte, les llistes de preus adjuntes al registre del proveïdor s'utilitzen per a la subcontractació. El compte del proveïdor té un tipus de relació de **Proveïdor** o **Distribuïdor**.
  - Un administrador de projectes pot desglossar totes les compres com a elements de línia del subcontracte. Les línies del subcontracte poden ser per temps, despeses o productes. La classe de transacció de la línia del subcontracte determina per a què serveix la línia.
  - L'administrador del compte del proveïdor i l'administrador del projecte poden iterar el subcontracte. Els preus es poden ajustar a les llistes de preus de compra que hi ha adjuntes al subcontracte.
  - Durant el procés, si la línia de subcontracte és per a temps, l'administrador del compte del proveïdor pot associar contactes del proveïdor amb cada línia de subcontracte. Aquesta associació proporciona informació a l'administrador del projecte sobre qui està treballant en el subcontracte. Quan un contacte del proveïdor s'associa amb una línia del subcontracte, el sistema crea automàticament un recurs que es pot reservar a partir del contacte, si encara no existeix cap recurs que es pot reservar.
  - El mètode de facturació de cada línia de subcontracte pot ser de preu fix o de temps i material. Per a les línies del subcontracte de preu fix, es configura una planificació de la factura basada en fites.
