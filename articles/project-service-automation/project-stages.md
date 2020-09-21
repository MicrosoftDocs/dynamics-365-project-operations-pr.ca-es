---
title: Fases del projecte
description: Aquest tema proporciona informació sobre les fases del projecte.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749469"
---
# <a name="project-stages"></a>Fases del projecte 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les fases del projecte s'actualitzen per reflectir l'estat del projecte a mesura que avança. El flux del procés de negoci per defecte actualitza automàticament algunes fases del projecte i altres s'actualitzen manualment per part de l'administrador de projecte. 

Les fases següents es defineixen al BPF per defecte:

- New
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
