---
title: Desactivació d'una dimensió de preus
description: En aquest tema, podreu obtenir informació sobre com desactivar dimensions de preus.
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
ms.openlocfilehash: d2e10c9ce782697fa4cbbe6eb63491ebb573a6f6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274716"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="95b72-103">Desactivació d'una dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="95b72-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="95b72-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="95b72-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="95b72-105">Pot ser que hàgiu de revisar i actualitzar l'estratègia de preus cada pocs anys.</span><span class="sxs-lookup"><span data-stu-id="95b72-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="95b72-106">Pot ser que les actualitzacions que feu exigeixin que desactiveu una dimensió de preus existent i que en creeu una de nova.</span><span class="sxs-lookup"><span data-stu-id="95b72-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="95b72-107">Per exemple, pot ser que hàgiu tingut un preu per **Funció**, però ara hàgiu decidit definir preus per **Experiència laboral**.</span><span class="sxs-lookup"><span data-stu-id="95b72-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="95b72-108">Potser necessitareu desactivar **Funció** com a dimensió de preus i que creeu **Experiència de treball** com a nova dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="95b72-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="95b72-109">Desactivar una dimensió de preus, independentment de si és personalitzada o per defecte, pot fer-se definint els camps **Aplicable al cost** i **Aplicable a les vendes** de la dimensió de preus com a **No**.</span><span class="sxs-lookup"><span data-stu-id="95b72-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="95b72-110">No obstant, en fer-ho, pot ser que rebeu el missatge d'error **La dimensió de preus no es pot actualitzar ni suprimir si hi ha registres de preu associats.**</span><span class="sxs-lookup"><span data-stu-id="95b72-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Error de procés empresarial probable quan desactiveu una dimensió de preus](media/Business-Process-Error.png)

<span data-ttu-id="95b72-112">Aquest missatge d'error indica que hi ha registres de preus que abans s'havien configurat per a la dimensió que s'està desactivant.</span><span class="sxs-lookup"><span data-stu-id="95b72-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="95b72-113">Tots els registres **Preu per funció** i **Marge comercial de preu per funció** que facin referència a una dimensió s'han de suprimir abans que l'aplicabilitat de la dimensió pugui definir-se com a **No**.</span><span class="sxs-lookup"><span data-stu-id="95b72-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="95b72-114">Aquesta regla s'aplica a les dues dimensions de preus per defecte i a les dimensions de preus personalitzades que hàgiu creat.</span><span class="sxs-lookup"><span data-stu-id="95b72-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="95b72-115">La raó d'aquesta validació és que cada registre **Preu per funció** ha de tenir una combinació única de dimensions.</span><span class="sxs-lookup"><span data-stu-id="95b72-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="95b72-116">Per exemple, en una llista de preus anomenada **Tarifes de costos dels EUA 2018**, teniu les files **Preu per funció** següents.</span><span class="sxs-lookup"><span data-stu-id="95b72-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="95b72-117">Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="95b72-117">Standard Title</span></span>         | <span data-ttu-id="95b72-118">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="95b72-118">Org Unit</span></span>    |<span data-ttu-id="95b72-119">Unit</span><span class="sxs-lookup"><span data-stu-id="95b72-119">Unit</span></span>   |<span data-ttu-id="95b72-120">Preu</span><span class="sxs-lookup"><span data-stu-id="95b72-120">Price</span></span>  |<span data-ttu-id="95b72-121">Moneda</span><span class="sxs-lookup"><span data-stu-id="95b72-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="95b72-122">Enginyer de sistemes</span><span class="sxs-lookup"><span data-stu-id="95b72-122">Systems Engineer</span></span>|<span data-ttu-id="95b72-123">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="95b72-123">Contoso US</span></span>|<span data-ttu-id="95b72-124">Hour</span><span class="sxs-lookup"><span data-stu-id="95b72-124">Hour</span></span>| <span data-ttu-id="95b72-125">100</span><span class="sxs-lookup"><span data-stu-id="95b72-125">100</span></span>|<span data-ttu-id="95b72-126">USD</span><span class="sxs-lookup"><span data-stu-id="95b72-126">USD</span></span>|
| <span data-ttu-id="95b72-127">Enginyer de sistemes sènior</span><span class="sxs-lookup"><span data-stu-id="95b72-127">Senior Systems Engineer</span></span>|<span data-ttu-id="95b72-128">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="95b72-128">Contoso US</span></span>|<span data-ttu-id="95b72-129">Hour</span><span class="sxs-lookup"><span data-stu-id="95b72-129">Hour</span></span>| <span data-ttu-id="95b72-130">150</span><span class="sxs-lookup"><span data-stu-id="95b72-130">150</span></span>| <span data-ttu-id="95b72-131">USD</span><span class="sxs-lookup"><span data-stu-id="95b72-131">USD</span></span>|


<span data-ttu-id="95b72-132">Quan desactiveu **Càrrec estàndard** com a dimensió de preus, i el motor de preus cerqui un preu, només utilitzarà el valor **Unitat organitzativa** del context d'entrada.</span><span class="sxs-lookup"><span data-stu-id="95b72-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="95b72-133">Si la **Unitat organitzativa** del context d'entrada és "Contoso US", el resultat serà no determinista perquè ambdues files coincidiran.</span><span class="sxs-lookup"><span data-stu-id="95b72-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="95b72-134">Per evitar aquest escenari, quan creeu registres **Preu per funció**, el sistema valida que la combinació de dimensions és única.</span><span class="sxs-lookup"><span data-stu-id="95b72-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="95b72-135">Si la dimensió s'ha desactivat després de crear els registres **Preu per funció**, aquesta restricció es pot violar.</span><span class="sxs-lookup"><span data-stu-id="95b72-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="95b72-136">Per tant, és necessari que abans de desactivar una dimensió, suprimiu totes les files **Preu per funció** i **Marge comercial de preu per funció** que tenen aquest valor de dimensió amb valors.</span><span class="sxs-lookup"><span data-stu-id="95b72-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]