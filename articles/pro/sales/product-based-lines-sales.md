---
title: Línies d'oportunitat basades en productes (bàsic)
description: Aquest tema proporciona informació sobre els elements de línia d'oportunitat basats en productes al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4f8da5258a1dd0aa4229654c0e1e222b8cf3a21a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272601"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="6326f-103">Línies d'oportunitat basades en productes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="6326f-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="6326f-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="6326f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6326f-105">Les línies d'oportunitat basades en productes són elements de línia de l'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="6326f-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="6326f-106">Aquests elements de línia diferents es troben a la factura eventual que es proporciona al client.</span><span class="sxs-lookup"><span data-stu-id="6326f-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="6326f-107">La factura no inclou cap altre servei addicional.</span><span class="sxs-lookup"><span data-stu-id="6326f-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="6326f-108">No es fa el seguiment de la despesa i el consum associats a les tasques de cap projecte relacionat.</span><span class="sxs-lookup"><span data-stu-id="6326f-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="6326f-109">Les línies basades en productes poden ser elements del catàleg o productes fora del catàleg.</span><span class="sxs-lookup"><span data-stu-id="6326f-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="6326f-110">La major part de la funcionalitat de les línies basades en productes d'una oportunitat segueix la funcionalitat proporcionada per l'aplicació Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6326f-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="6326f-111">Per obtenir més informació sobre les línies d'oportunitat basades en productes, vegeu [Afegir productes a una oportunitat](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="6326f-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="6326f-112">El **pressupost del client** és un concepte específic de les línies d'oportunitat basades en projectes.</span><span class="sxs-lookup"><span data-stu-id="6326f-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="6326f-113">El camp **Pressupost del client** fa el seguiment de l'import que està disposat a pagar el client per l'article.</span><span class="sxs-lookup"><span data-stu-id="6326f-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="6326f-114">Quan el mètode d'ingressos del resum d'oportunitat és **Calculat pel sistema**, els valors del pressupost del client en totes les línies d'oportunitat es resumeixen per calcular els ingressos previstos.</span><span class="sxs-lookup"><span data-stu-id="6326f-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]