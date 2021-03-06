---
title: Entrada de despesa (bàsica)
description: En aquest tema es proporciona informació sobre com treballar amb l'entrada de despesa en una implementació bàsica.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965733"
---
# <a name="expense-entry-lite"></a>Entrada de despesa (bàsica)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Bàsica, l'administració de despeses és la capacitat de registrar les despeses simples. Podeu registrar les despeses en un projecte i, a continuació, l'aprovador del projecte les revisarà i aprovarà.

Per obtenir més informació sobre les capacitats de despesa del Dynamics 365 Project Operations, vegeu [Descripció general de les despeses](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturar una despesa bàsica

Podeu capturar les despeses per enviar-les a l'aprovador.

1. Aneu a **Despeses** i seleccioneu **Nova**.
2. A la pàgina **Despesa nova**, introduïu la informació de despesa necessària i, a continuació, seleccioneu **Desa**.

## <a name="submit-a-basic-expense"></a>Enviar una despesa bàsica

Després d'haver acabat de capturar totes les despeses i que estigueu a punt per aprovar-les, haureu d'enviar-les.

1. Aneu a **Despeses** i seleccioneu una despesa. O bé, seleccioneu totes les despeses mitjançant la casella de selecció de la capçalera.
2. Seleccioneu **Envia**. El sistema processa les entrades seleccionades i crea sol·licituds d'aprovació de despeses.

## <a name="recall-a-basic-expense"></a>Recuperar una despesa bàsica

Quan envieu una despesa per equivocació, podeu recuperar-la. El temps necessari per recuperar una entrada de despesa depèn de la fase d'aprovació.  Si l'aprovador encara no ha aprovat l'entrada, pot ser que la recuperació es produeixi immediatament. No obstant, si l'entrada ja ha estat aprovada, es demana a l'aprovador que aprovi la recuperació i reverteixi les transaccions.

1. Aneu a **Despeses** i, a continuació, a la llista de despeses, seleccioneu la despesa que voleu recuperar.
2. Seleccioneu **Recupera**. Si l'entrada de la despesa encara no s'ha aprovat, el sistema la recupera immediatament. Si l'entrada de la despesa ja s'ha aprovat, una sol·licitud de recuperació es crea per notificar a l'aprovador que voleu revertir la despesa. A continuació, l'aprovador confirmarà que la reversió es pot fer i es recuperarà l'entrada.

## <a name="delete-a-basic-expense"></a>Suprimir una despesa bàsica

Les despeses que encara no s'han enviat es poden suprimir. Per suprimir una despesa que ja s'ha enviat, primer heu de recuperar-la.

## <a name="see-also"></a>Consulteu també

- [Informació general de les aprovacions](../approvals/approvals-overview.md)
