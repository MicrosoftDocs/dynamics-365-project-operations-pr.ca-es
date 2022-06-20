---
title: Registrar temps, despeses i ús de materials dels components subcontractats
description: En aquest article s'explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrats en projectes de components subcontractats Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c05b941fb51c8b56422e3b5d3868c9b69197187
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927638"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Temps de registre, despeses i ús de material en projectes per a components subcontractats

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest article s'explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrats en projectes de components subcontractats Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Cost del temps de subcontractació en projectes
En operacions de projectes, els treballadors contractats poden registrar temps en projectes de manera similar als empleats. En entrar en el temps en projectes i/o tasques de projecte, un treballador contractat pot seleccionar una línia de subcontractació i subcontractació específica.

Quan s'aprova el temps presentat pels treballadors contractats, el cost del projecte es registra mitjançant la tarifa de cost unitària que es configura per a aquest recurs de treballador contractat a la **secció Preus** de funció de la llista de preus de compra de la subcontractació.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Cost de les despeses subcontractades en projectes
En introduir les despeses ocasionades en projectes, pots seleccionar una línia de subcontractació i subcontractació a l'entrada de despeses. 

Quan aquesta entrada de despeses s'envia i s'aprova, el cost de la despesa es registra al projecte en funció del cost unitari que es configura per a aquesta categoria de transacció a la **secció Preus de categoria** de la llista de preus de compra de la subcontractació.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Cost de materials subcontractats en projectes
Quan introduïu l'ús de material en projectes, podeu seleccionar una línia de subcontractació i subcontractació al registre d'ús de material. Quan el registre d'ús del material s'envia i s'aprova, el cost del material es registra al projecte en funció del cost unitari que es configura per a aquest producte a la secció Elements **de la** llista de preus de la llista de preus de subcontractació.

L'ús de material també es pot registrar per a productes d'escriptura en projectes. Aquest tipus d'ús de material també es pot vincular a una línia de subcontractació i subcontractació. Quan registreu l'ús de material per a productes d'escriptura, heu d'introduir el cost per unitat del producte d'escriptura. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
