---
title: Temps d'enregistrament, despeses i ús de material per a components subcontractats
description: Aquest tema explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrats en projectes de components subcontractats Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902996"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Temps de registre, despeses i ús de material en projectes per a components subcontractats

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest tema explica com Microsoft fa un seguiment del temps, la despesa i l'ús de material registrats en projectes de components subcontractats Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Cost del temps de subcontractació en projectes
En operacions de projectes, els treballadors contractats poden registrar temps en projectes de manera similar als empleats. En entrar en el temps en projectes i/o tasques de projecte, un treballador contractat pot seleccionar una línia de subcontractació i subcontractació específica.

Quan s'aprova el temps presentat pels treballadors contractats, el cost del projecte es registra mitjançant la tarifa de cost unitària que es configura per a aquest recurs de treballador contractat a la **secció Preus de funció de la llista de preus de compra de la** subcontractació.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Cost de les despeses subcontractades en projectes
En introduir les despeses ocasionades en projectes, pots seleccionar una línia de subcontractació i subcontractació a l'entrada de despeses. 

Quan aquesta entrada de despeses s'envia i s'aprova, el cost de la despesa es registra al projecte en funció del cost unitari que es configura per a aquesta categoria de transacció a la **secció Preus de categoria de la llista de preus de compra de la** subcontractació.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Cost de materials subcontractats en projectes
Quan introduïu l'ús de material en projectes, podeu seleccionar una línia de subcontractació i subcontractació al registre d'ús de material. Quan el registre d'ús del material s'envia i s'aprova, el cost del material es registra al projecte en funció del cost unitari que es configura per a aquest producte a la secció Elements de la **llista de preus de la llista de preus de** subcontractació.

L'ús de material també es pot registrar per a productes d'escriptura en projectes. Aquest tipus d'ús de material també es pot vincular a una línia de subcontractació i subcontractació. Quan registreu l'ús de material per a productes d'escriptura, heu d'introduir el cost per unitat del producte d'escriptura. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
