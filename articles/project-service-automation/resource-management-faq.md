---
title: PMF de l'administració de recursos
description: Aquest tema proporciona respostes a les preguntes més freqüents sobre l'administració de recursos.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: fdf7f1e2-e4a2-4c68-aa03-4a41c7b10531
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 87da759b3b30ed6d38866c045194cde79837c209
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749546"
---
# <a name="resource-management-faq"></a>PMF de l'administració de recursos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Quina diferència hi ha entre un membre de l'equip i un requisit de recursos?

Un membre de l'equip del projecte es pot assignar a tasques, reservar o tenir un excés de reserva, i definir-lo com a aprovador. Un requisit de recurs pot existir sense membres de l'equip d'un projecte, com un esborrany de la demanda. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Quina diferència hi ha entre les hores proposades i les reservades de manera flexible?

Les hores proposades i les hores reservades de manera flexible tenen una visibilitat diferent. Les hores proposades només són visibles pels administradors de recursos i per l'administrador de projectes que han iniciat la demanda mitjançant una sol·licitud de recurs. Les hores reservades de manera flexible són visibles per qualsevol persona que tingui accés al Tauler de planificació.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Com puc veure les hores reservades de manera flexible per als recursos d'un equip?

Les reserves flexibles es poden fer quan reserveu un requisit de recurs. Els recursos que s'han reservat de manera flexible en un equip del projecte apareixen com a membres de l'equip que tenen hores reservades de manera flexible. També apareixen al Tauler de planificació.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Com puc canviar les hores requerides i les dates d'inici i d'acabament per a un recurs (genèric o amb nom) que he reservat?

Després de reservar els recursos, seleccioneu **Mantén les reserves** per fer els canvis necessaris.

## <a name="what-resources-types-does-project-service-automation-support"></a>Quins tipus de recursos admet el Project Service Automation?

**Usuari** i **Contacte** són els únics tipus de recurs admesos al Dynamics 365 Project Service Automation. Tot i que podeu crear altres tipus de recursos (per exemple, **Equipament** i **Grup**), no s'admet cap cas d'ús d'extrem a extrem.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Quina diferència hi ha entre una assignació i una reserva?

Les assignacions són l'assignació de recursos a tasques de projecte a la planificació del projecte. Els recursos poden ser recursos reals o genèrics. Les reserves són l'assignació fixa o flexible de recursos a un projecte. Les reserves fixes consumeixen la capacitat d'un recurs. Idealment, per als recursos reals, les reserves i les assignacions haurien de concordar, perquè no es diferencien. No obstant, el PSA no obliga a aplicar aquesta concordança. La visualització Conciliació mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.
