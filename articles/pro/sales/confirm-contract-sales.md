---
title: Confirmació d'un contracte de projecte
description: Aquest tema proporciona informació sobre com confirmar un contracte al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128271"
---
# <a name="confirm-a-project-contract"></a>Confirmació d'un contracte de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Un contracte de projecte al Dynamics 365 Project Operations pot ser actiu amb una raó **Confirmat**, o tancat amb una raó **Perdut**. Quan es confirma un contracte de projecte, l'estat s'actualitza d'**Esborrany** a **Actiu** i la raó per a l'estat és **Confirmat**. Un contracte actiu o tancat no es pot editar o reobrir. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impacte financer de confirmar un contracte de projecte

Després que es confirmi un contracte de projecte, l'aplicació recalcula els costos invertint els valors reals de cost més antics i creant nous valors reals de cost. Els nous valors reals de cost llavors es processen segons el mètode de facturació de la línia de contracte del projecte associat. Si els valors reals de cost fan referència a una línia de contracte de temps i material, l'aplicació torna a crear automàticament els valors reals de vendes no facturades corresponents. Si els valors reals de cost fan referència a una línia de contracte de preu fix, l'aplicació deixa de processar els valors reals de cost.

Els límits que no s'han de superar, la configuració d'imputabilitat i els preus i el cost dels valors reals s'avaluen i s'actualitzen com a part del procés de confirmació.

## <a name="close-a-project-contract-as-lost"></a>Tancar un contracte de projecte com a perdut

Quan es tanca un contracte de projecte com a perdut, l'estat del contracte s'actualitza a **Tancat** i la raó per a l'estat és **Perdut**. El contracte del projecte es converteix en només de lectura. Es proporciona un diàleg de confirmació abans que els canvis es completin perquè no podeu reobrir un contracte de projecte tancat.

Si el contracte de projecte que es tanca com a perdut fa referència a un projecte en les seves línies, aquest projecte també es marca com a tancat. Qualsevol reserva de recursos a partir d'aquell dia es cancel·la. Es revertirà qualsevol valor real de venda sense facturar al contracte del projecte que no estigui en una factura.

> [!NOTE]
> Al Dynamics 365 Project Operations, el tancament d'un contracte de projecte com a perdut no afectarà l'estat de l'oportunitat associada. L'oportunitat romandrà oberta i ha de tancar-se manualment.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]