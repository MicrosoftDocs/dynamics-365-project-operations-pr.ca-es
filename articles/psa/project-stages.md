---
title: Tipus de fases del projecte
description: Aquest tema proporciona informació sobre les fases del projecte.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008974"
---
# <a name="project-stage-types"></a>Tipus de fases del projecte 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les fases d'un projecte estan dissenyades per reflectir l'estat del projecte a mesura que avança. Les personalitzacions es poden utilitzar per actualitzar els trams automàticament amb flux del procés de negoci, el Power Automate o extensions de complements.

Les fases següents es defineixen al BPF per defecte:

- Nova
- Oferta
- Pla
- Lliurament
- Completat
- Tanca 

## <a name="new"></a>New

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]