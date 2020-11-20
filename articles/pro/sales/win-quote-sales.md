---
title: Tancament d'una oferta (bàsic)
description: En aquest tema es proporciona informació sobre el tancament d'una oferta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175699"
---
# <a name="close-a-quote---lite"></a>Tancament d'una oferta (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una oportunitat de projecte es pot tancar com a guanyada o perduda. les operacions d'activació i revisió en les ofertes no s'admeten al Microsoft Dynamics 365 Project Operations; per tant, es pot tancar un esborrany d'oferta.

## <a name="close-a-quote-as-won"></a>Tancament d'una oferta com a guanyada

El tancament d'una oferta de projecte com a guanyada tancarà l'oferta amb l'estat definit com a Tancada i la raó per a l'estat definida com a Guanyada. Quan tanqueu l'oferta, l'oferta del projecte és de només de lectura i crea un esborrany de contracte del projecte que conté la informació de l'oferta. Com que no es pot tornar a obrir una oferta tancada, hi ha un quadre de diàleg de confirmació abans que es facin els canvis, ja que una oferta tancada no es pot tornar a obrir i els canvis són irreversibles.

Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacte financer del tancament d'una oferta com a guanyada

Si no s'ha registrat cap valor real per al temps enregistrat en un projecte mentre encara està vinculat a un esborrany d'oferta, només es registra el cost del temps o de la despesa. Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous. L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat. Si els valors reals de costos fan referència a una línia de contracte de temps i material, el sistema crearà automàticament valors reals de vendes sense facturar per a quan es tanqui l'oferta i es creï el contracte del projecte. Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de tornar a processar els valors reals de cost en funció de les regles de divisió de la facturació per als clients del contracte del projecte.

## <a name="closing-a-quote-as-lost"></a>Tancament d'una oferta com a perduda:

Si tanqueu una oferta de projecte com a Perduda, es definirà l'estat com a Tancada i la raó per a l'estat a Perduda. En tancar l'oferta, l'oferta del projecte passa a ser només de lectura. Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.

Si l'oferta del projecte que es tanca com a perduda té un projecte al qual es fa referència en qualsevol de les seves línies, aquest projecte també es marca com a tancat i totes les reserves de recursos a partir d'aquell dia es cancel·len.

> [!NOTE]
> Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.
