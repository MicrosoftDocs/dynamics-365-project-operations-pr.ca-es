---
title: Registrar temps, despeses i ús de materials dels components subcontractats
description: Microsoft explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrat en projectes a partir de components subcontractats Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522501"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registre de temps, despeses i ús de material en projectes de components subcontractats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Microsoft explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrat en projectes a partir de components subcontractats Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Cost del temps del subcontractista en els projectes
En operacions de projecte, els treballadors contractats poden registrar el temps en els projectes de manera similar als empleats. A l'hora d'introduir temps en projectes i/o tasques del projecte, un treballador amb contracte pot seleccionar una línia específica de subcontractació i subcontractació.

Quan s'aprova el temps presentat pels treballadors contractats, el cost del projecte es registra mitjançant la taxa de cost unitari que s'estableix per a aquest recurs de treballador del contracte a l'apartat **Preus** de treball de la llista de preus de compra de la subcontractació.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Cost de les despeses subcontractades dels projectes
A l'hora d'introduir les despeses incorregudes en projectes, podeu seleccionar una línia de subcontractació i subcontractació a l'assentament de despeses. 

Quan es presenta i s'aprova aquest assentament de despeses, el cost de la despesa es registra en el projecte en funció del cost unitari que s'estableix per a aquesta categoria de transacció a l'apartat **Preus** de categoria de la llista de preus de compra del subcontractat.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Costos per a materials subcontractats en projectes
Quan introduïu l'ús de material en projectes, podeu seleccionar una línia de subcontractació i subcontractació al registre d'ús de materials. Quan s'envia i s'aprova el registre d'ús del material, el cost del material es registra al projecte en funció del cost unitari que s'estableix per a aquest producte a la secció Articles de la llista de preus **de la** llista de preus del subcontractat.

L'ús de material també es pot registrar per escriure en productes en projectes. Aquest tipus d'ús de material també es pot vincular a una línia de subcontractació i subcontractació. Quan enregistreu l'ús de material per a productes d'escriptura, heu d'introduir el cost per unitat del producte d'escriptura. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
