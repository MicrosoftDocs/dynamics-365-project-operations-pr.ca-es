---
title: Línies d'oportunitat basades en productes (bàsic)
description: Aquest tema proporciona informació sobre els elements de línia d'oportunitat basats en productes al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176306"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="b0bb2-103">Línies d'oportunitat basades en productes (bàsic)</span><span class="sxs-lookup"><span data-stu-id="b0bb2-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="b0bb2-104">_**S'aplica a:** implementació bàsica: tracte de facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="b0bb2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b0bb2-105">Les línies d'oportunitat basades en productes són elements de línia de l'oportunitat.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="b0bb2-106">Aquestes línies es lliuren al client com a elements de línia diferents de la factura eventual sense cap altre servei de valor afegit.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="b0bb2-107">No es fa el seguiment de la despesa i el consum associats a les tasques de cap projecte relacionat.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="b0bb2-108">Les línies basades en productes poden ser elements del catàleg o productes fora del catàleg.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="b0bb2-109">La major part de la funcionalitat de les línies basades en productes d'una oportunitat segueix la funcionalitat proporcionada per l'aplicació Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="b0bb2-110">Per obtenir més informació sobre les línies d'oportunitat basades en productes, vegeu [Afegir productes a una oportunitat](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="b0bb2-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="b0bb2-111">Un concepte de línies d'oportunitat basades en productes que és específic per a les oportunitats basades en projectes és el **Pressupost del client**.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="b0bb2-112">Utilitzeu aquest camp per fer el seguiment de l'import que el client està disposat a pagar per l'element de línia.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="b0bb2-113">Si el mètode d'ingrés del resum de l'oportunitat està definit com a **Calculat pel sistema**, els valors del pressupost del client a les línies de producte i de projecte es resumiran per calcular els ingressos previstos.</span><span class="sxs-lookup"><span data-stu-id="b0bb2-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
