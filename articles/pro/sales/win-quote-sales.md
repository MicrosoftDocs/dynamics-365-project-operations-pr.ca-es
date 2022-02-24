---
title: Tancament d'una oferta (bàsic)
description: En aquest tema es proporciona informació sobre el tancament d'una oferta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272256"
---
# <a name="close-a-quote---lite"></a>Tancament d'una oferta (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una oportunitat de projecte es pot tancar com a guanyada o perduda. Una oferta en esborrany es pot tancar perquè les operacions Activa i Revisa a les ofertes no estàn admeses al Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Tancament d'una oferta com a guanyada

Quan tanqueu una oferta de projecte com a Guanyada, l'estat es defineix com a Tancat i la raó per a l'estat és Guanyat. Quan tanqueu l'oferta, l'oferta del projecte és de només de lectura i crea un esborrany de contracte del projecte que conté la informació de l'oferta. Com que una oferta tancada no es pot tornar a obrir, un diàleg de confirmació confirmarà els canvis.

Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacte financer del tancament d'una oferta com a guanyada

Si hi ha valors reals per al temps en un projecte mentre encara està adjunt a un esborrany d'oferta, només es registra el cost del temps o la despesa. Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous. L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat. Si el valors reals del cost fan referència a una línia de contracte de temps i materials, es creen els valors reals de vendes no facturats corresponents per al moment en què l'oferta es tanqui i es creï el contracte del projecte. Si els valors reals del cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de reprocessar els valors reals del cost que es basen en les regles de facturació fraccionades per als clients de contracte del projecte.

## <a name="closing-a-quote-as-lost"></a>Tancament d'una oferta com a perduda:

Quan tanqueu una oferta de projecte com a Perduda, l'estat es defineix com a Tancat i la raó per a l'estat és Perdut. En tancar l'oferta, l'oferta del projecte passa a ser només de lectura. Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.

Si l'oferta del projecte que es tanca com a Perduda fa referència a un projecte en qualsevol de les seves línies, aquest projecte també es marca com a Tancat. Qualsevol reserva de recursos a partir d'aquell dia es cancel·la.

> [!NOTE]
> Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]