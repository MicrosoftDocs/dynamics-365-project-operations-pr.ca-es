---
title: Conceptes clau en la subcontractació
description: En aquest tema s'expliquen alguns conceptes clau que s'apliquen a la subcontractació del Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578099"
---
# <a name="key-concepts-in-subcontracting"></a>Conceptes clau en la subcontractació

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest tema s'expliquen alguns conceptes clau que hauríeu de tenir en compte abans de començar a utilitzar la funcionalitat de subcontractació del Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unitat de contracte de la subcontractació

La unitat de contracte representa la divisió o la pràctica propietària del lliurament del projecte final. La unitat de contracte també és la divisió que entra a la relació de contracte amb el proveïdor.

## <a name="purchase-currency"></a>Moneda de compra

Al Project Operations, la moneda de compra és la moneda en què es crea el subcontracte. També és la moneda en què es registren els costos del subcontractista en un projecte. La moneda de compra pot diferir de la moneda del projecte i la moneda del projecte pot, al seu torn, diferir de la moneda de vendes.

## <a name="billing-methods-on-subcontract-lines"></a>Mètodes de facturació a les línies de subcontractació

Per als projectes, normalment hi ha una quota fixa i models de contracte basats en el consum. El Project Operations és compatible amb aquests mètodes de facturació en els contextos de vendes i compra. Per a una compra, els mètodes de facturació funcionen de la manera següent:

- **Temps i material**: quan una línia de subcontractació utilitza el mètode de facturació de **Temps i material**, el cost del temps es registra al projecte a mesura que els subcontractistes treballen en aquest projecte i enregistren el temps. Aquestes transaccions de cost dels subcontractistes es fan coincidir amb els elements de línia de les factures del proveïdor. En aquest model, els administradors de projecte que utilitzen el Project Operations poden aparellar i verificar les línies de factura del proveïdor amb el temps del subcontractista que s'ha registrat i aprovat. Un cop completada la verificació, els valors reals de cost anteriors que es van registrar després de l'aprovació s'inverteixen i es creen nous valors reals de cost basats en la factura del proveïdor al projecte.
- **Preu fix**: en aquest model de contracte de quota fixa, les factures del proveïdor es basen en fites fixes. Tanmateix, els recursos del subcontractista també poden informar sobre el temps. A continuació, l'administrador del projecte revisa i aprova les hores. Quan s'aprova, el Project Operations crea valors reals de cost temporals en el projecte. Quan el proveïdor envia una factura per a una fita, l'administrador del projecte pot fer coincidir els valors reals de cost enregistrats anteriorment amb la fita. Quan la verificació s'hagi completat, els valors reals de cost s'inverteixen i el cost basat en la fita es registra.

## <a name="project-price-lists-on-subcontracts"></a>Llistes de preus de projectes en subcontractes

Les llistes de preus del projecte són llistes de preus que s'utilitzen per configurar els preus d'compra per al temps, les despeses i altres components relacionats amb el projecte. Hi pot haver diverses llistes de preus, cadascuna de les quals pot tenir la seva pròpia data efectiva de subcontractació al Project Operations. El Project Operations no admet dates efectives superposades a les llistes de preus del projecte per a un subcontracte.

## <a name="transaction-classes-on-subcontracts"></a>Classes de transaccions als subcontractes

El Project Operations admet quatre tipus de classes de transaccions:

- Temps
- Despesa
- Material
- Tarifa

Els costos de compra només es poden calcular i generar a les classes de transaccions **Temps**, **Despesa** i **Material**. La **tarifa** és una classe de transaccions només d'ingressos i no està disponible al contingut de la compra.

## <a name="purchase-pricing-dimensions"></a>Dimensions de preus de la compra

Les dimensions de preus us permeten decidir quins atributs s'utilitzen per a la configuració del preu de compra i per a les transaccions de temps. En relació amb la compra, el Project Operations només admet els conjunts fixos de dimensions per a la configuració del preu de compra i per a definir el valor per defecte. Per configurar el preu de compra i definir el valor per defecte de les línies del subcontracte i les transaccions de temps del subcontracte, els atributs són **Funció** i **Recurs que es pot reservar**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
