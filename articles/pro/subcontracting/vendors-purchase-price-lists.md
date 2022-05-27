---
title: Administració del proveïdor i de la llista de preus de compra al Project Operations
description: Aquest tema proporciona informació que us ajudarà a crear i mantenir dades del proveïdor i llistes de preu de compra per a la subcontractació.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9c76d5ca45e03167f0ccfd2c1c7013f91fef0f86
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576718"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Administració del proveïdor i de la llista de preus de compra al Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

## <a name="vendors-in-project-operations"></a>Proveïdors al Project Operations

Al Microsoft Dynamics 365 Project Operations, els comptes del proveïdor tenen un tipus de relació de **Proveïdor** o **Distribuïdor**. Només podeu seleccionar un registre de compte que tingui un d'aquests tipus de relació com a proveïdor en un subcontracte.

Podeu associar una o més llistes de preus de compra amb un registre de proveïdor. Tanmateix, cada llista de preus de compra associada amb un registre de proveïdor ha de tenir una efecteivitat de data diferent. El Project Operations no admet l'efectivitat de dates superposades per a les llistes de preus de compra.

Per defecte, els camps i conceptes següents d'un registre de proveïdor s'utilitzen per a qualsevol subcontracte que es creï per al proveïdor:

- Condicions de pagament
- Facturació al contacte
- Contacte principal

    > [!NOTE]
    > Per defecte, el contacte principal del proveïdor s'utilitza com a administrador de compte del proveïdor del subcontracte.

- Moneda
- Llistes de preus de compra actuals

## <a name="purchase-price-lists-in-project-operations"></a>Llistes de preus de compra al Project Operations

Una llista de preus on el camp **Context** està definit com a **Compra** es considera una llista de preus de compra. Podeu definir les llistes de preus de compra perquè representin un catàleg de tarifes de compra per al temps, les despeses i els materials. Les llistes de preus de compra semblen llistes de preus de cost i vendes del Project Operations. Els conceptes següents s'apliquen a les llistes de preus de compra de la mateixa manera que s'apliquen a les llistes de preus de cost i de venda:

- **Effectivitat de les dates**: les llistes de preus de compra tenen efectivitat de les dates. L'efectevitat de les dates està representada pels camps de data d'inici i d'acabament de cada llista de preus. El temps entre la data d'inici i la data d'acabament és el període efectiu de la data.
- **Moneda**: la moneda de la capçalera de la llista de preus s'utilitza com a moneda en què s'expressen els preus de compra per a la mà d'obra, les categories de despeses i els productes del catàleg.
- **Unitat de temps per defecte**: la unitat de temps per defecte expressa els preus laborals per a les compres. El camp d'unitat de temps d'una llista de preus només s'utilitza per proporcionar un valor per defecte. Aquest valor es pot canviar a les files de preus de funcions individuals.

Podeu adjuntar llistes de preus de compra als registres del proveïdor com a associacions anomenades llistes de preus del projecte. Aquestes llistes de preus s'utilitzen per introduir els preus per defecte a les línies de subcontractació. Per defecte, quan s'adjunten diverses llistes de preus de compra a un registre del proveïdor, la llista de preus més recent s'utilitza per als subcontractes creats per al proveïdor. Només es poden adjuntar les llistes de preus en què el camp **Context** està definit com a **Compra** als registres del proveïdor.

### <a name="subcontract-specific-purchase-price-lists"></a>Llistes de preus de compra específiques del subcontracte

També podeu adjuntar llistes de preus de compra als subcontractes com a associacions anomenades llistes de preus del projecte. Aquestes llistes de preus s'utilitzen per introduir els preus per defecte a les línies de subcontractació. Per defecte, quan s'adjunten diverses llistes de preus de compra a un subcontracte, cadascuna ha de tenir una efectivitat de dates diferent. El Project Operations no admet les llistes de preus de compra que tenen l'efectivitat de dates superposades. Només es poden adjuntar les llistes de preus en què el camp **Context** està definit com a **Compra** als subcontractes.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
