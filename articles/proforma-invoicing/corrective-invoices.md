---
title: Factures corregides
description: Aquest tema proporciona informació sobre les factures corregides.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287811"
---
# <a name="corrected-invoices"></a><span data-ttu-id="ae8fa-103">Factures corregides</span><span class="sxs-lookup"><span data-stu-id="ae8fa-103">Corrected invoices</span></span>

<span data-ttu-id="ae8fa-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="ae8fa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae8fa-105">Es poden editar les factures confirmades.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="ae8fa-106">Quan editeu una factura confirmada, es crea un esborrany de la factura corregida.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="ae8fa-107">Com que s'assumeix que voleu revertir totes les transaccions i quantitats de la factura original, la factura corregida inclou totes les transaccions de la factura original i totes les quantitats que hi ha són zero.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="ae8fa-108">Quan alguna transacció no requereix correcció, podeu eliminar-la de l'esborrany de factura correctiva.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="ae8fa-109">Per revertir o retornar només una quantitat parcial, podeu editar el camp Quantitat al detall de la línia.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="ae8fa-110">Si obriu el detall de la línia de factura, podeu veure la quantitat original de la factura.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="ae8fa-111">A continuació, podeu editar la quantitat de la factura actual de manera que sigui inferior o superior a la quantitat original de la factura.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="ae8fa-112">Quan es confirma una factura correctiva, es reverteix el valor real de vendes facturades original i es crea un nou valor real de vendes facturades.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="ae8fa-113">Si la quantitat s'ha reduït, la diferència provocarà que també s'hagi creat un nou valor real de venda no facturada.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="ae8fa-114">Per exemple, si les vendes facturades originals eren de vuit hores, i el detall de la línia de factura corregida té una quantitat menor de sis hores, es reverteix la línia de vendes facturades originals i es creen dos nous valors reals:</span><span class="sxs-lookup"><span data-stu-id="ae8fa-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="ae8fa-115">Un valor de vendes facturades durant sis hores.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="ae8fa-116">Un valor de vendes no facturades per a les dues hores restants.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="ae8fa-117">Aquesta transacció es pot facturar més tard o marcar com a no imputable, en funció de les negociacions amb el client.</span><span class="sxs-lookup"><span data-stu-id="ae8fa-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]