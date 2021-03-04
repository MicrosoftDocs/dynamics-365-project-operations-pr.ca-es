---
title: Tancar una oferta
description: En aquest tema es proporciona informació sobre el tancament d'ofertes al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124671"
---
# <a name="close-a-quote"></a>Tancar una oferta

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una oportunitat de projecte es pot tancar com a guanyada o perduda. Com que les funcions d'activació i revisió en les ofertes no s'admeten al Microsoft Dynamics 365 Project Operations, podeu tancar un esborrany d'oferta.

## <a name="close-a-quote-as-won"></a>Tancament d'una oferta com a guanyada

El tancament d'una oferta de projecte com a guanyada definirà l'estat de l'oferta a **Tancada** i la raó per a l'estat a **Guanyada**. Quan tanqueu una oferta, passa a ser de només de lectura i es crea un esborrany de contracte del projecte amb tota la informació de l'oferta. Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.

El contracte de projecte creat a partir d'una oferta de projecte també es posa a la vostra disposició al mòdul d'administració de projectes i comptabilitat del Project Operations. Si un contracte de projecte no s'assigna a un projecte a cap de les línies, aquest contracte de projecte es posa a la vostra disposició com a contracte de projecte inactiu i s'activa tan bon punt s'assigna un projecte com a mínim a una de les seves línies de contracte.

Si l'oferta està unida a una oportunitat, la resta d'ofertes de projectes a l'oportunitat es tancaran automàticament com a perdudes.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impacte financer del tancament d'una oferta com a guanyada

Si no s'ha registrat cap valor real per al temps enregistrat en un projecte mentre encara està vinculat a un esborrany d'oferta, només es registra el cost del temps o de la despesa. Després de tancar una oferta com a guanyada, l'aplicació refactoritzarà els costos revertint els valors reals del cost més antics i tornant a crear valors reals de cost nous. L'aplicació processarà els valors reals d'aquests costos en funció del mètode de facturació de la línia de contracte del projecte associat. Si els valors reals de costos fan referència a una línia de contracte de temps i material, el sistema crearà automàticament valors reals de vendes sense facturar per a quan es tanqui l'oferta i es creï el contracte del projecte. Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixarà de tornar a processar els valors reals de cost en funció de les regles de divisió de la facturació per als clients del contracte del projecte.

Tots els valors reals tornats a processar estan disponibles al mòdul d'administració de projectes i comptabilitat perquè el comptable del projecte els revisi, actualitzi i comptabilitzi al registre general. 

## <a name="close-a-quote-as-lost"></a>Tancament d'una oferta com a perduda

Si tanqueu una oferta de projecte com a Perduda, es definirà l'estat com a **Tancada** i la raó per a l'estat a **Perduda**. El tancament de l'oferta fa que sigui només de lectura. Com que no es pot tornar a obrir una oferta tancada, abans de tancar una oferta, un quadre de diàleg de confirmació confirmarà els canvis.

Si l'oferta del projecte que es tanca com a perduda té un projecte al qual es fa referència en qualsevol de les seves línies, aquest projecte també es marca com a tancat i totes les reserves de recursos a partir d'aquell dia es cancel·len.

> [!NOTE]
> Al Project Operations, si tanqueu una oferta com a guanyada o perduda, l'estat de l'oportunitat no es veurà afectat i romandrà oberta fins que es tanqui manualment.


[!INCLUDE[footer-include](../includes/footer-banner.md)]