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
# <a name="expense-home-page"></a><span data-ttu-id="6ee4a-103">Pàgina inicial de despeses</span><span class="sxs-lookup"><span data-stu-id="6ee4a-103">Expense home page</span></span>

<span data-ttu-id="6ee4a-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="6ee4a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="6ee4a-105">El Dynamics 365 Project Operations admet la capacitat de processar les despeses.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="6ee4a-106">El processament de despeses es produeix amb o sense projectes mitjançant l'ús d'un flux de treball personalitzable de polítiques, categories de transaccions i aprovacions.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="6ee4a-107">Al Project Operations, hi ha dos models d'implementació admesos per a les despeses:</span><span class="sxs-lookup"><span data-stu-id="6ee4a-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="6ee4a-108">**Completa**: la implementació completa està disponible per a **Project Operations per a escenaris basats en recursos/sense cotització** o **Project Operations per a escenaris de producció basats en comandes**.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="6ee4a-109">**Bàsica**: la implementació bàsica està disponible per a **Project Operations per a escenaris basats en recursos/sense cotització** i **Implementació bàsica: tracte de facturació proforma**.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="6ee4a-110">Complet</span><span class="sxs-lookup"><span data-stu-id="6ee4a-110">Full</span></span> 
<span data-ttu-id="6ee4a-111">La implementació completa de despeses proporciona un compliment complet de les polítiques i inclou la capacitat de crear polítiques, com ara:</span><span class="sxs-lookup"><span data-stu-id="6ee4a-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="6ee4a-112">Límits de categories de despesa</span><span class="sxs-lookup"><span data-stu-id="6ee4a-112">Expense category limits</span></span>
  - <span data-ttu-id="6ee4a-113">Viatge</span><span class="sxs-lookup"><span data-stu-id="6ee4a-113">Travel</span></span>
  - <span data-ttu-id="6ee4a-114">Per dia</span><span class="sxs-lookup"><span data-stu-id="6ee4a-114">Per diem</span></span>
  - <span data-ttu-id="6ee4a-115">Imports de targeta de crèdit</span><span class="sxs-lookup"><span data-stu-id="6ee4a-115">Credit card imports</span></span>
  - <span data-ttu-id="6ee4a-116">Reconeixement òptic de caràcters de rebuts</span><span class="sxs-lookup"><span data-stu-id="6ee4a-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="6ee4a-117">Bàsic</span><span class="sxs-lookup"><span data-stu-id="6ee4a-117">Basic</span></span> 
<span data-ttu-id="6ee4a-118">L'escenari d'implementació de despeses bàsica només permet enregistrar les despeses bàsiques d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="6ee4a-119">Per obtenir més informació, vegeu [Entrada de despeses (bàsica)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="6ee4a-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="6ee4a-120">Determinació de la implementació de despeses</span><span class="sxs-lookup"><span data-stu-id="6ee4a-120">Determine your Expense deployment</span></span>
<span data-ttu-id="6ee4a-121">Per determinar si executeu la implementació bàsica de l'administració de les despeses, verifiqueu que la URL d'adreça acabi amb **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="6ee4a-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
