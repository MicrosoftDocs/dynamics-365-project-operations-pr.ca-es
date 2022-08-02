---
title: Utilitzeu categories de contractació amb comandes de compra de projectes i factures pendents del proveïdor
description: En aquest article es descriu com configurar les categories de contractació que es poden utilitzar amb les comandes de compra del projecte i les factures pendents dels proveïdors.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Utilitzeu categories de contractació amb comandes de compra de projectes i factures pendents del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els professionals de compres poden crear i mantenir catàlegs dels articles i serveis que es poden utilitzar en les comandes de compra de projectes i factures pendents dels proveïdors. [Els catàlegs](/dynamics365/supply-chain/procurement/procurement-catalogs) d'aprovisionament us ofereixen una manera senzilla de categoritzar les compres sense haver de configurar i utilitzar un catàleg de productes alliberats. Cada categoria de contractació es pot assignar a una categoria de projecte per a transaccions de temps, despeses o articles. Després de publicar una factura pendent del proveïdor que utilitza una categoria de contractació, el sistema crearà entrades reals de projectes de temps, despeses o materials, transaccions de projecte i subscripcions.

## <a name="minimum-version-requirements"></a>Requisits mínims de versió

Les versions següents han d'utilitzar categories de contractació amb ordres de compra de projectes per a escenaris Microsoft Dynamics 365 Project Operations no estocats o basats en recursos:

- Versió 4.41.0.45 o posterior de la solució project operations Dataverse
- Entorn financer i operacions versió 10.0.26 o posterior

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Executeu mapes de doble escriptura per al suport de categories de contractació

Assegureu-vos que l'assignació per a **l'entitat d'exportació de la línia de factures del proveïdor del projecte d'integració del Project Operations msdyn\_ projectvendorinvoicelines** utilitzi la versió 1.0.0.4 o posterior.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Habiliteu la clau de característica per a les categories de contractació

Seguiu aquests passos per habilitar la funcionalitat per utilitzar categories de contractació amb ordres de compra de projectes.

1. En Dynamics 365 Finance, obriu l'espai **de treball Gestió** de funcions.
1. A la llista de característiques, cerqueu utilitza categories de contractació a la **característica Operacions de projecte per a escenaris basats en recursos/no emmagatzemats** i, a continuació, seleccioneu **Habilita**.

> [!IMPORTANT]
> Com a requisit previ, també heu d'habilitar la funció Habilita les factures pendents del **proveïdor al Project Operations per a escenaris basats en recursos/no emmagatzemats**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Mapa de categories de projectes en la jerarquia de categories de contractació

Seguiu aquests passos per assignar les categories de projectes a les categories de contractació de la **jerarquia de categories de** contractació:

1. Aneu a Aprovisionament **i aprovisionament \> Categories** de contractació.
1. Seleccioneu **Edita la jerarquia de categories**.
1. Seleccioneu el node de jerarquia de categories desitjat i, a continuació, a la **pestanya Assigna categories** de projecte, associeu el node amb la categoria de projecte des de la **categoria Temps** **, despesa** o projecte **element** (és a dir, la **categoria Temps** per defecte o **Despesa** per defecte).
1. Seleccioneu **Desa**.
1. Tanqueu la pàgina.

> [!NOTE]
> Assignar una categoria de contractació a una categoria de projecte és opcional. Si una categoria de contractació no està mapejada, el sistema utilitzarà el valor que s'estableix al camp Element **de la** secció Per defecte de la **categoria Projecte a la** pestanya Operacions **del projecte al Dynamics 365 Customer engagement** de la **pàgina Paràmetres comptables** i d'administració de projecte.
