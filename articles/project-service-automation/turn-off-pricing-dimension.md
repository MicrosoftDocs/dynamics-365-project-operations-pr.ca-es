---
title: Desactivar una dimensió de preus
description: En aquest tema es mostra com configurar les dimensions de preus a la solució del Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749533"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="83e4d-103">Desactivar una dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="83e4d-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="83e4d-104">Pot ser que hàgiu de revisar i actualitzar l'estratègia de preus cada pocs anys.</span><span class="sxs-lookup"><span data-stu-id="83e4d-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="83e4d-105">Pot ser que les actualitzacions que feu exigeixin que desactiveu una dimensió de preus existent i que en creeu una de nova.</span><span class="sxs-lookup"><span data-stu-id="83e4d-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="83e4d-106">Per exemple, pot ser que hàgiu tingut un preu per **Funció**, però ara hàgiu decidit definir preus per **Experiència laboral**.</span><span class="sxs-lookup"><span data-stu-id="83e4d-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="83e4d-107">Potser necessitareu desactivar **Funció** com a dimensió de preus i que creeu **Experiència de treball** com a nova dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="83e4d-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="83e4d-108">Desactivar una dimensió de preus, independentment de si és personalitzada o per defecte, pot fer-se definint els camps **Aplicable al cost** i **Aplicable a les vendes** de la dimensió de preus com a **No**.</span><span class="sxs-lookup"><span data-stu-id="83e4d-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="83e4d-109">No obstant, en fer-ho, és possible que rebeu el missatge d'error següent.</span><span class="sxs-lookup"><span data-stu-id="83e4d-109">However, when you do this, you might receive the following error message.</span></span>

![Error de procés empresarial probable quan desactiveu una dimensió de preus](media/Business-Process-Error.png)


<span data-ttu-id="83e4d-111">Aquest missatge d'error indica que hi ha registres de preus que abans s'havien configurat per a la dimensió que s'està desactivant.</span><span class="sxs-lookup"><span data-stu-id="83e4d-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="83e4d-112">Tots els registres **Preu per funció** i **Marge comercial de preu per funció** que facin referència a una dimensió s'han de suprimir abans que l'aplicabilitat de la dimensió pugui definir-se com a **No**.</span><span class="sxs-lookup"><span data-stu-id="83e4d-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="83e4d-113">Aquesta regla s'aplica a les dues dimensions de preus per defecte i a les dimensions de preus personalitzades que hàgiu creat.</span><span class="sxs-lookup"><span data-stu-id="83e4d-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="83e4d-114">La raó d'aquesta validació és que el Project Service té una restricció que cada registre **Preu per funció** ha de tenir una combinació única de dimensions.</span><span class="sxs-lookup"><span data-stu-id="83e4d-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="83e4d-115">Per exemple, en una llista de preus anomenada **Tarifes de costos dels EUA 2018**, teniu les files **Preu per funció** següents.</span><span class="sxs-lookup"><span data-stu-id="83e4d-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="83e4d-116">Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="83e4d-116">Standard Title</span></span>         | <span data-ttu-id="83e4d-117">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="83e4d-117">Org Unit</span></span>    |<span data-ttu-id="83e4d-118">Unit</span><span class="sxs-lookup"><span data-stu-id="83e4d-118">Unit</span></span>   |<span data-ttu-id="83e4d-119">Preu</span><span class="sxs-lookup"><span data-stu-id="83e4d-119">Price</span></span>  |<span data-ttu-id="83e4d-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="83e4d-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="83e4d-121">Enginyer de sistemes</span><span class="sxs-lookup"><span data-stu-id="83e4d-121">Systems Engineer</span></span>|<span data-ttu-id="83e4d-122">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="83e4d-122">Contoso US</span></span>|<span data-ttu-id="83e4d-123">Hour</span><span class="sxs-lookup"><span data-stu-id="83e4d-123">Hour</span></span>| <span data-ttu-id="83e4d-124">100</span><span class="sxs-lookup"><span data-stu-id="83e4d-124">100</span></span>|<span data-ttu-id="83e4d-125">USD</span><span class="sxs-lookup"><span data-stu-id="83e4d-125">USD</span></span>|
| <span data-ttu-id="83e4d-126">Enginyer de sistemes sènior</span><span class="sxs-lookup"><span data-stu-id="83e4d-126">Senior Systems Engineer</span></span>|<span data-ttu-id="83e4d-127">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="83e4d-127">Contoso US</span></span>|<span data-ttu-id="83e4d-128">Hour</span><span class="sxs-lookup"><span data-stu-id="83e4d-128">Hour</span></span>| <span data-ttu-id="83e4d-129">150</span><span class="sxs-lookup"><span data-stu-id="83e4d-129">150</span></span>| <span data-ttu-id="83e4d-130">USD</span><span class="sxs-lookup"><span data-stu-id="83e4d-130">USD</span></span>|


<span data-ttu-id="83e4d-131">Quan desactiveu **Càrrec estàndard** com a dimensió de preus, i el motor de preus del Project Service cerqui un preu, només utilitzarà el valor **Unitat organitzativa** del context d'entrada.</span><span class="sxs-lookup"><span data-stu-id="83e4d-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="83e4d-132">Si la **Unitat organitzativa** del context d'entrada és "Contoso US", el resultat serà no determinista perquè ambdues files coincidiran.</span><span class="sxs-lookup"><span data-stu-id="83e4d-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="83e4d-133">Per evitar aquest escenari, quan creeu registres **Preu per funció**, el Project Service valida que la combinació de dimensions és única.</span><span class="sxs-lookup"><span data-stu-id="83e4d-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="83e4d-134">Si la dimensió s'ha desactivat després de crear els registres **Preu per funció**, aquesta restricció es pot violar.</span><span class="sxs-lookup"><span data-stu-id="83e4d-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="83e4d-135">Per tant, és necessari que abans de desactivar una dimensió, suprimiu totes les files **Preu per funció** i **Marge comercial de preu per funció** que tenen aquest valor de dimensió amb valors.</span><span class="sxs-lookup"><span data-stu-id="83e4d-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

