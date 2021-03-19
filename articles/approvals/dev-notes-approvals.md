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
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290257"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="51620-103">Notes del desenvolupador per a aprovacions</span><span class="sxs-lookup"><span data-stu-id="51620-103">Developer notes for Approvals</span></span>

<span data-ttu-id="51620-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="51620-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51620-105">El Dynamics 365 Project Operations inclou una lògica de validació que assegura la transició correcta del registre per les fases d'aprovació.</span><span class="sxs-lookup"><span data-stu-id="51620-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="51620-106">Les transicions de registre correctes asseguren que:</span><span class="sxs-lookup"><span data-stu-id="51620-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="51620-107">Totes les files de suport es creen en taules relacionades, com diaris i valors reals.</span><span class="sxs-lookup"><span data-stu-id="51620-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="51620-108">L'aprovador està marcat com a **Aprovador de projectes** abans de continuar.</span><span class="sxs-lookup"><span data-stu-id="51620-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]