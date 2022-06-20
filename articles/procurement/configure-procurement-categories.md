---
title: Utilitza categories d'adquisició amb ordres de compra de projectes i factures pendents del proveïdor
description: En aquest article es descriu com configurar les categories d'adquisició que es poden utilitzar amb ordres de compra de projectes i factures pendents del proveïdor.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927408"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilitza categories d'adquisició amb ordres de compra de projectes i factures pendents del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els professionals de compres poden crear i mantenir catàlegs dels articles i serveis que es poden utilitzar en comandes de compra de projectes i factures pendents del proveïdor. [Els catàlegs](/dynamics365/supply-chain/procurement/procurement-catalogs) de contractació us ofereixen una manera fàcil de categoritzar les compres sense haver de configurar i utilitzar un catàleg de productes alliberats. Cada categoria d'adquisició es pot assignar a una categoria de projecte per a transaccions de temps, despesa o article. Després de publicar una factura pendent del proveïdor que utilitza una categoria d'adquisició, el sistema crearà temps, despesa o material de projectes reals, transaccions de projecte i entrades subledger.

## <a name="minimum-version-requirements"></a>Requisits mínims de versió

Les versions següents són necessàries per utilitzar categories d'adquisició amb ordres de compra de projectes per a escenaris no emmagatzemats/basats en recursos de Microsoft Dynamics 365 Project Operations:

- Versió de la solució d'operacions Dataverse del projecte 4.41.0.45 o posterior
- Entorn de finances i operacions versió 10.0.26 o posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executa mapes de doble escriptura per al suport de la categoria de contractació

Assegureu-vos que l'assignació per al **proveïdor del projecte d'exportació de la línia de factura del proveïdor d'operacions del projecte msdyn\_ projectvendorinvoicelines** utilitzi la versió 1.0.0.4 o posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Habilita la clau de característica per a les categories de contractació

Seguiu aquests passos per habilitar la funcionalitat per utilitzar categories d'adquisició amb ordres de compra de projectes.

1. Al Dynamics 365 Finance, obriu l'àrea de treball d'administració **de** funcions.
1. A la llista de funcions, cerqueu les categories d'adquisició **d'ús a Les operacions del projecte per a la funció d'escenaris basats en recursos o no emmagatzemats** i, a continuació, seleccioneu **Habilita**.

> [!IMPORTANT]
> Com a requisit previ, també heu d'habilitar la funció Habilita les factures pendents del **proveïdor a Les operacions del projecte per a la funció d'escenaris basats en recursos o no emmagatzemats**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapa de categories de projectes a la jerarquia de categories de contractació

Seguiu aquests passos per assignar categories de projectes a categories de contractació a la jerarquia de **categories** de contractació:

1. Aneu a les **categories \> de contractació de contractació i aprovisionament**.
1. Seleccioneu **Edita la jerarquia de categories**.
1. Seleccioneu el node de jerarquia de categories de categories desitjat i, a continuació, a la **pestanya Assigna les categories** del projecte, associeu el node amb la categoria del projecte des de la **categoria Temps**, **Despesa** o Projecte **d'element** (és a dir, la **categoria Per** defecte o **despesa** per defecte).
1. Seleccioneu **Desa**.
1. Tanqueu la pàgina.

> [!NOTE]
> Assignar una categoria de contractació a una categoria de projecte és opcional. Si una categoria d'adquisició no està assignada, el sistema utilitzarà el valor definit al camp Element de la **secció Valors** per defecte de la **categoria del projecte a la** pestanya Operacions del projecte al Dynamics 365 Customer engagement **de la** pàgina Gestió de projectes i paràmetres comptables **.**
