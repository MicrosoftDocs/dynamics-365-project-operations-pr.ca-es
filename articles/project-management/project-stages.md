---
title: Fases del projecte
description: En aquest tema s'ofereix informació sobre les fases del projecte disponibles al Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127461"
---
# <a name="project-stages"></a>Fases del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les fases d'un projecte estan dissenyades per reflectir l'estat del projecte a mesura que avança. Les personalitzacions es poden utilitzar per actualitzar els trams automàticament amb flux del procés de negoci, el Power Automate o extensions de complements.

Les fases següents es defineixen al flux del procés de negoci per defecte:

- Nova
- Oferta
- Pla
- Lliura
- Complet
- Tanca  

## <a name="new"></a>Nova

Quan creeu un projecte, la fase del projecte es defineix a **Nou**. Si el projecte es va crear a partir d'una plantilla, pot ser que hi hagi dades de planificació, estimació i equips. Altrament, és només un esbós del projecte i els components restants s'han d'introduir.

## <a name="quote"></a>Oferta

Quan associeu un projecte a una oferta o creeu un projecte a partir d'una oferta, la fase de projecte es defineix com a **Oferta** i les dates d'inici i finalització previstes s'actualitzen. Quan el projecte està en la fase **Oferta**, els detalls de l'oferta es mostren a la pestanya **Vendes** de la pàgina **Entitat del projecte**.

## <a name="plan"></a>Pla

Quan guanyeu una oferta associada amb un projecte, i quan el projecte avança a la fase **Contracte**, la fase de projecte s'actualitza a **Pla**. Quan el projecte està en la fase **Pla**, els detalls del contracte es mostren a la pàgina **Entitat del projecte**.

## <a name="deliver"></a>Lliurament

Quan s'hagi completat el pla del projecte i ja esteu a punt per iniciar el projecte, l'administrador del projecte hauria d'actualitzar la fase del projecte a **Lliurament** per mostrar que el projecte ha començat.

## <a name="complete"></a>Completat 

Quan s'hagi completat el treball per al projecte, l'administrador del projecte pot actualitzar la fase a **Completat**. En actualitzar la fase de projecte a **Completat**, l'administrador del projecte indica que el treball s'ha completat al 100 per cent, però que s'ha de mantenir obert el projecte de manera que es puguin registrar les entrades de temps o de despesa pendents.

## <a name="close"></a>Tanca

Quan s'hagin registrat totes les transaccions per al projecte, l'administrador del projecte pot actualitzar la fase a **Tancat**. En aquest moment, no es pot registrar cap transacció i el projecte es defineix com a només de lectura.

