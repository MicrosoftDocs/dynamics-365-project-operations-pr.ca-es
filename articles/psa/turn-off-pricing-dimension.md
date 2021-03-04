---
title: Desactivar una dimensió de preus
description: En aquest tema es mostra com configurar les dimensions de preus a la solució del Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147281"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="dbec3-103">Desactivar una dimensió de preus</span><span class="sxs-lookup"><span data-stu-id="dbec3-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dbec3-104">Pot ser que hàgiu de revisar i actualitzar l'estratègia de preus cada pocs anys.</span><span class="sxs-lookup"><span data-stu-id="dbec3-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="dbec3-105">Pot ser que les actualitzacions que feu exigeixin que desactiveu una dimensió de preus existent i que en creeu una de nova.</span><span class="sxs-lookup"><span data-stu-id="dbec3-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="dbec3-106">Per exemple, pot ser que hàgiu tingut un preu per **Funció**, però ara hàgiu decidit definir preus per **Experiència laboral**.</span><span class="sxs-lookup"><span data-stu-id="dbec3-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="dbec3-107">Potser necessitareu desactivar **Funció** com a dimensió de preus i que creeu **Experiència de treball** com a nova dimensió de preus.</span><span class="sxs-lookup"><span data-stu-id="dbec3-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="dbec3-108">Desactivar una dimensió de preus, independentment de si és personalitzada o per defecte, pot fer-se definint els camps **Aplicable al cost** i **Aplicable a les vendes** de la dimensió de preus com a **No**.</span><span class="sxs-lookup"><span data-stu-id="dbec3-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="dbec3-109">No obstant, en fer-ho, és possible que rebeu el missatge d'error següent.</span><span class="sxs-lookup"><span data-stu-id="dbec3-109">However, when you do this, you might receive the following error message.</span></span>

![Error de procés empresarial probable quan desactiveu una dimensió de preus](media/Business-Process-Error.png)


<span data-ttu-id="dbec3-111">Aquest missatge d'error indica que hi ha registres de preus que abans s'havien configurat per a la dimensió que s'està desactivant.</span><span class="sxs-lookup"><span data-stu-id="dbec3-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="dbec3-112">Tots els registres **Preu per funció** i **Marge comercial de preu per funció** que facin referència a una dimensió s'han de suprimir abans que l'aplicabilitat de la dimensió pugui definir-se com a **No**.</span><span class="sxs-lookup"><span data-stu-id="dbec3-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="dbec3-113">Aquesta regla s'aplica a les dues dimensions de preus per defecte i a les dimensions de preus personalitzades que hàgiu creat.</span><span class="sxs-lookup"><span data-stu-id="dbec3-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="dbec3-114">La raó d'aquesta validació és que el Project Service té una restricció que cada registre **Preu per funció** ha de tenir una combinació única de dimensions.</span><span class="sxs-lookup"><span data-stu-id="dbec3-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="dbec3-115">Per exemple, en una llista de preus anomenada **Tarifes de costos dels EUA 2018**, teniu les files **Preu per funció** següents.</span><span class="sxs-lookup"><span data-stu-id="dbec3-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="dbec3-116">Càrrec estàndard</span><span class="sxs-lookup"><span data-stu-id="dbec3-116">Standard Title</span></span>         | <span data-ttu-id="dbec3-117">Unitat organitzativa</span><span class="sxs-lookup"><span data-stu-id="dbec3-117">Org Unit</span></span>    |<span data-ttu-id="dbec3-118">Unit</span><span class="sxs-lookup"><span data-stu-id="dbec3-118">Unit</span></span>   |<span data-ttu-id="dbec3-119">Preu</span><span class="sxs-lookup"><span data-stu-id="dbec3-119">Price</span></span>  |<span data-ttu-id="dbec3-120">Moneda</span><span class="sxs-lookup"><span data-stu-id="dbec3-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="dbec3-121">Enginyer de sistemes</span><span class="sxs-lookup"><span data-stu-id="dbec3-121">Systems Engineer</span></span>|<span data-ttu-id="dbec3-122">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="dbec3-122">Contoso US</span></span>|<span data-ttu-id="dbec3-123">Hour</span><span class="sxs-lookup"><span data-stu-id="dbec3-123">Hour</span></span>| <span data-ttu-id="dbec3-124">100</span><span class="sxs-lookup"><span data-stu-id="dbec3-124">100</span></span>|<span data-ttu-id="dbec3-125">USD</span><span class="sxs-lookup"><span data-stu-id="dbec3-125">USD</span></span>|
| <span data-ttu-id="dbec3-126">Enginyer de sistemes sènior</span><span class="sxs-lookup"><span data-stu-id="dbec3-126">Senior Systems Engineer</span></span>|<span data-ttu-id="dbec3-127">Contoso EUA</span><span class="sxs-lookup"><span data-stu-id="dbec3-127">Contoso US</span></span>|<span data-ttu-id="dbec3-128">Hour</span><span class="sxs-lookup"><span data-stu-id="dbec3-128">Hour</span></span>| <span data-ttu-id="dbec3-129">150</span><span class="sxs-lookup"><span data-stu-id="dbec3-129">150</span></span>| <span data-ttu-id="dbec3-130">USD</span><span class="sxs-lookup"><span data-stu-id="dbec3-130">USD</span></span>|


<span data-ttu-id="dbec3-131">Quan desactiveu **Càrrec estàndard** com a dimensió de preus, i el motor de preus del Project Service cerqui un preu, només utilitzarà el valor **Unitat organitzativa** del context d'entrada.</span><span class="sxs-lookup"><span data-stu-id="dbec3-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="dbec3-132">Si la **Unitat organitzativa** del context d'entrada és "Contoso US", el resultat serà no determinista perquè ambdues files coincidiran.</span><span class="sxs-lookup"><span data-stu-id="dbec3-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="dbec3-133">Per evitar aquest escenari, quan creeu registres **Preu per funció**, el Project Service valida que la combinació de dimensions és única.</span><span class="sxs-lookup"><span data-stu-id="dbec3-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="dbec3-134">Si la dimensió s'ha desactivat després de crear els registres **Preu per funció**, aquesta restricció es pot violar.</span><span class="sxs-lookup"><span data-stu-id="dbec3-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="dbec3-135">Per tant, és necessari que abans de desactivar una dimensió, suprimiu totes les files **Preu per funció** i **Marge comercial de preu per funció** que tenen aquest valor de dimensió amb valors.</span><span class="sxs-lookup"><span data-stu-id="dbec3-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

