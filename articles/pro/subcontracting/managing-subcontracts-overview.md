---
title: Administració de subcontractacions al Project Operations
description: En aquest tema es proporciona informació general del procés d'administració de subcontractació d'extrem a extrem al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994219"
---
# <a name="subcontract-management-in-project-operations"></a>Administració de subcontractacions al Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La subcontractació al Microsoft Dynamics 365 Project Operations admet el següent flux del procés de negoci.

![Flux del procés de subcontractació](../media/SubcontractingProcessFlow.png)

Aquesta és una descripció pas a pas del procés de subcontractació.

1. L'administrador del projecte crea un subcontracte amb un proveïdor. Per defecte, les llistes de preus adjuntes al registre del proveïdor s'utilitzen per a la subcontractació. El compte del proveïdor té un tipus de relació de **Proveïdor** o **Distribuïdor**.
2. L'administrador del projecte pot desglossar totes les compres com a elements de línia del subcontracte. Les línies del subcontracte poden ser per temps, despeses o productes. La classe de transacció seleccionada a cada línia del subcontracte determina per a què serveix la línia.
3. L'administrador del compte del proveïdor i l'administrador del projecte poden iterar el subcontracte. Els preus es poden ajustar a les llistes de preus de compra que hi ha adjuntes al subcontracte.
4. En aquest punt o més endavant en el procés, si la línia del subcontracte és per al temps, l'administrador del compte del proveïdor associa els contactes amb cada línia de subcontractació. Aquesta associació proporciona informació a l'administrador del projecte sobre qui està treballant en el subcontracte. Quan un contacte s'associa amb una línia del subcontracte, el sistema crea automàticament un recurs que es pot reservar a partir del contacte, si encara no existeix cap recurs que es pot reservar.
5. El mètode de facturació de cada línia del subcontracte pot ser **Preu fix** o **Temps i material**. Per a les línies del subcontracte de preu fix, podeu configurar una planificació de la factura basada en fites.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
