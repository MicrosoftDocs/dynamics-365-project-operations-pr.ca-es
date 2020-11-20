---
title: Notes del desenvolupador per a aprovacions
description: Aquest tema proporciona informació addicional al desenvolupador sobre com treballar amb aprovacions.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483936"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="1656b-103">Notes del desenvolupador per a aprovacions</span><span class="sxs-lookup"><span data-stu-id="1656b-103">Developer notes for Approvals</span></span>

<span data-ttu-id="1656b-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="1656b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1656b-105">El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="1656b-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="1656b-106">Les transicions de registre correctes asseguren que:</span><span class="sxs-lookup"><span data-stu-id="1656b-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="1656b-107">Totes les files de suport es creen en taules relacionades, com diaris i valors reals.</span><span class="sxs-lookup"><span data-stu-id="1656b-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="1656b-108">L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.</span><span class="sxs-lookup"><span data-stu-id="1656b-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
