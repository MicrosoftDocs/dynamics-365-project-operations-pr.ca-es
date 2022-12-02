---
title: Registrar temps, despeses i ús de materials dels components subcontractats
description: En aquest article s'explica com es fa el seguiment del temps, la despesa i l'ús del material registrat en projectes dels components subcontractats al Microsoft Dynamics 365 Project Operations.
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
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registrar temps, despeses i ús de materials en projectes dels components subcontractats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest article s'explica com es fa el seguiment del temps, la despesa i l'ús del material registrat en projectes dels components subcontractats al Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Càlcul de costos de temps de subcontractista en projectes
Al Project Operations, els treballadors contractats poden registrar el temps dedicat als projectes de manera semblant als empleats. Quan introdueix el temps als projectes o les tasques de projecte, un treballador contractat pot seleccionar un subcontracte i una línia de subcontracte específics.

Quan el temps enviat per empleats contractats s'aprova, el cost del projecte es registra amb el percentatge de cost per unitat que està configurat per al recurs de treballador contractat a la secció **Preus de funcions** de la llista de preus de compra del subcontracte.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Càlcul de costos per a despeses subcontractades en projectes
Quan introduïu les despeses contretes en els projectes, podeu seleccionar un subcontracte i una línia de subcontracte a l'entrada de despesa. 

Quan aquesta entrada de despesa s'envia i s'aprova, el cost de la despesa es registra al projecte en funció del cost per unitat que està configurat per a la categoria de transacció a la secció **Preus de categories** de la llista de preus de compra del subcontracte.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Càlcul de costos per a materials subcontractats en projectes
Quan introduïu l'ús de materials en els projectes, podeu seleccionar un subcontracte i una línia de subcontracte al registre d'ús de materials. Quan el registre d'ús de materials s'envia i s'aprova, el cost dels materials es registra al projecte en funció del cost per unitat que està configurat per al producte a la secció **Elements de la llista de preus** de la llista de preus del subcontracte.

L'ús de materials també es pot registrar per a productes fora del catàleg en projectes. Aquest tipus d'ús de materials també es pot enllaçar a un subcontracte i una línia de subcontracte. Quan es registra l'ús de materials per a productes fora del catàleg, heu d'introduir el cost per unitat del producte fora del catàleg. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
