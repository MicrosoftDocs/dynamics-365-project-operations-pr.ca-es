---
title: Utilitzar les categories de proveïment amb comandes de compra de projectes i factures de proveïdors pendents
description: En aquest article es descriu com es configuren les categories de proveïment que es poden utilitzar amb les categories de proveïment amb les comandes de compra de projectes i les factures de proveïdor pendents.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028598"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilitzar les categories de proveïment amb comandes de compra de projectes i factures de proveïdors pendents

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els professionals de compra poden crear i mantenir catàlegs dels articles i serveis que es poden utilitzar en les comandes de compra del projecte i en les factures de proveïdor pendents. Els [catàlegs de compres](/dynamics365/supply-chain/procurement/procurement-catalogs) us ofereixen una manera fàcil de classificar per categories les compres sense haver de configurar i utilitzar un catàleg de productes publicat. Cada categoria de compra es pot assignar a una categoria de projecte per a les transaccions de temps, despesa o article. Després de comptabilitzar una factura del proveïdor pendent que utilitza una categoria de compra, el sistema crearà els valors reals de temps, despesa o materials del projecte, les transaccions del projecte i les entrades de subllibre.

## <a name="minimum-version-requirements"></a>Requisits mínims de la versió

Les versions següents són necessàries per utilitzar les categories de proveïment amb les comandes de compra del projecte en escenaris no mantinguts en existències/basats en recursos del Microsoft Dynamics 365 Project Operations:

- Versió de la solució Project Operations Dataverse 4.41.0.45 o posterior
- Entorn de finances i operacions, versió 10.0.26 o posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executar assignacions de doble escriptura per a la compatibilitat amb les categories de proveïment

Assegureu-vos que l'assignació d'**Entitat d'exportació de línia de factura del proveïdor del projecte d'integració del Project Operations msdyn\_projectvendorinvoicelines** utilitza la versió 1.0.0.4 o posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Habilitar la clau de característica per a les categories de proveïment

Seguiu aquests passos per habilitar la funcionalitat per utilitzar categories de proveïment amb comandes de compra de projectes.

1. Al Dynamics 365 Finance, obriu a l'àrea de treball **Administració de característiques**.
1. A la llista de característiques, cerqueu la característica **Utilitzar les categories de proveïment al Project Operations per a escenaris basats en recursos o sense existències** i, a continuació, seleccioneu **Habilita**.

> [!IMPORTANT]
> Com a requisit previ, heu d'habilitar també la característica **Habilita les factures del proveïdor pendents al Project Operations per a escenaris basats en recursos o sense existències**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Assignar categories de projecte a la jerarquia de categories de proveïment

Seguiu aquests passos per assignar categories de projecte a les categories de proveïment en la jerarquia de **Categoria de proveïment**:

1. Aneu a **Contractació i proveïment \> Categories de contractació**.
1. Seleccioneu **Edita la jerarquia de categories**.
1. Seleccioneu el node de jerarquia de categories desitjat i, a continuació, a la pestanya **Assigna categories de projecte**, associeu el node amb la categoria de projecte de la categoria **Temps**, **Despesa** o **Projecte d'element** (és a dir, la categoria **Per defecte-Temps** o **Per defecte-Despesa**).
1. Seleccioneu **Desa**.
1. Tanqueu la pàgina.

> [!NOTE]
> L'assignació d'una categoria de proveïment a una categoria de projecte és opcional. Si no s'assigna cap categoria de proveïment, el sistema **utilitzarà el valor definit al camp Article** de la secció **Valors per defecte de la categoria de projecte** a la pestanya **Project Operations al Dynamics 365 Customer Engagement** de la pàgina **Paràmetres d'administració de projectes i comptabilitat**.
