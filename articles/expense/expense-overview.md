---
title: Informació general de la despesa
description: En aquest tema es proporciona informació sobre la funcionalitat de despeses al Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d946a8dcbf3b2369631d83e80788eed4904be95d
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764897"
---
# <a name="expense-home-page"></a>Pàgina inicial de despeses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


El Dynamics 365 Project Operations admet la capacitat de processar les despeses. El processament de despeses es produeix amb o sense projectes mitjançant l'ús d'un flux de treball personalitzable de polítiques, categories de transaccions i aprovacions.

Al Project Operations, hi ha dos models d'implementació admesos per a les despeses: 

- **Completa**: la implementació completa està disponible per a **Project Operations per a escenaris basats en recursos/sense cotització** o **Project Operations per a escenaris de producció basats en comandes**.
- **Bàsica**: la implementació bàsica està disponible per a **Project Operations per a escenaris basats en recursos/sense cotització** i **Implementació bàsica: tracte de facturació proforma**.

## <a name="full"></a>Complet 
La implementació completa de despeses proporciona un compliment complet de les polítiques i inclou la capacitat de crear polítiques, com ara:

  - Límits de categories de despesa
  - Viatge
  - Per dia
  - Imports de targeta de crèdit
  - Reconeixement òptic de caràcters de rebuts

## <a name="basic"></a>Bàsic 
L'escenari d'implementació de despeses bàsica només permet enregistrar les despeses bàsiques d'un projecte. 

Per obtenir més informació, vegeu [Entrada de despeses (bàsica)](basic-expense.md)

## <a name="determine-your-expense-deployment"></a>Determinació de la implementació de despeses
Per determinar si executeu la implementació bàsica de l'administració de les despeses, verifiqueu que la URL d'adreça acabi amb **.crm.dynamics.com**. 
