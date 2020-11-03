---
title: Creació i aplicació de les condicions de retenció de pagaments de proveïdors
description: Aquest tema proporciona informació sobre com establir i mantenir els termes de retenció de pagaments de proveïdors.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072349"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="bb165-103">Creació i aplicació de les condicions de retenció de pagaments de proveïdors</span><span class="sxs-lookup"><span data-stu-id="bb165-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="bb165-104">La configuració de termes de retenció de pagaments de proveïdors per a un projecte és útil quan la vostra organització vol retenir part dels pagaments realitzats a un proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="bb165-105">Per exemple, quan voleu retenir el pagament al proveïdor fins que els productes lliurats compleixin les vostres expectatives.</span><span class="sxs-lookup"><span data-stu-id="bb165-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="bb165-106">Els termes de retenció de pagaments del proveïdor es poden especificar quan negocieu un contracte de proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="bb165-107">Crear termes de retenció de pagaments de proveïdors</span><span class="sxs-lookup"><span data-stu-id="bb165-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="bb165-108">Podeu introduir el percentatge de pagament del proveïdor per a la retenció i el percentatge dels imports retinguts prèviament que s'alliberaran.</span><span class="sxs-lookup"><span data-stu-id="bb165-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="bb165-109">Els imports es retenen automàticament en factures de proveïdors fins que el contracte arribi a l'estat de finalització especificat.</span><span class="sxs-lookup"><span data-stu-id="bb165-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="bb165-110">Després d'establir els termes de retenció, els podeu aplicar a qualsevol projecte per a aquest proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="bb165-111">Utilitzeu els passos següents per establir i mantenir els termes de retenció per als pagaments de proveïdors.</span><span class="sxs-lookup"><span data-stu-id="bb165-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="bb165-112">Aneu a **Administració de projectes i comptabilitat** > **Retenció** > **Termes de retenció de pagaments de proveïdors**.</span><span class="sxs-lookup"><span data-stu-id="bb165-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="bb165-113">Seleccioneu **Nou** per afegir un nou terme de retenció de proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="bb165-114">El valor **ID de regla** per al nou terme s'introdueix automàticament.</span><span class="sxs-lookup"><span data-stu-id="bb165-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="bb165-115">Introduïu una breu descripció en el camp **Descripció** i, en el FastTab **Termes** , seleccioneu **Afegeix una línia** per introduir valors de termes per al següent:</span><span class="sxs-lookup"><span data-stu-id="bb165-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="bb165-116">**Percentatge d'unitats lliurades** : introduïu un percentatge de finalització per al terme.</span><span class="sxs-lookup"><span data-stu-id="bb165-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="bb165-117">Els imports es retenen automàticament en factures de proveïdors fins que la fase de finalització del projecte és igual al percentatge especificat.</span><span class="sxs-lookup"><span data-stu-id="bb165-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="bb165-118">Per exemple, si introduïu 50,00, els imports es retenen fins que el projecte estigui completat al 50%.</span><span class="sxs-lookup"><span data-stu-id="bb165-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="bb165-119">**Percentatge de retenció** : introduïu un percentatge de l'import de la factura del proveïdor que es retindrà.</span><span class="sxs-lookup"><span data-stu-id="bb165-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="bb165-120">Per exemple, si introduïu 10,00, llavors el 10 per cent de l'import d'una factura de proveïdor es reté fins que el projecte arriba al percentatge de finalització establert en el camp **Percentatge d'unitats lliurades**.</span><span class="sxs-lookup"><span data-stu-id="bb165-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="bb165-121">**Percentatge per a l'alliberament** : seleccioneu **Afegeix una línia** per introduir un percentatge dels imports retinguts prèviament que s'han d'alliberar per al nivell seleccionat de finalització del projecte.</span><span class="sxs-lookup"><span data-stu-id="bb165-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="bb165-122">Si teniu més d'una fita per a diferents nivells de finalització del projecte, introduïu una línia separada de terme de retenció de proveïdors per a cada regla de retenció.</span><span class="sxs-lookup"><span data-stu-id="bb165-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="bb165-123">Cada línia pot especificar un percentatge de retenció diferent i un percentatge de llançament diferent per a cada nivell designat de finalització del projecte.</span><span class="sxs-lookup"><span data-stu-id="bb165-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="bb165-124">Després de crear els termes de retenció de proveïdors per a un proveïdor, podeu aplicar els termes a un projecte.</span><span class="sxs-lookup"><span data-stu-id="bb165-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="bb165-125">Aplicar els termes de retenció del proveïdor a un projecte</span><span class="sxs-lookup"><span data-stu-id="bb165-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="bb165-126">Aneu a **Administració de projectes i comptabilitat** > **Projectes** > **Tots els projectes** i obriu un projecte de la pàgina de llista de projectes.</span><span class="sxs-lookup"><span data-stu-id="bb165-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="bb165-127">Al FastTab **Acords de proveïdors** , seleccioneu **Afegeix una línia**.</span><span class="sxs-lookup"><span data-stu-id="bb165-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="bb165-128">En el camp **Codi del compte** , seleccioneu una de les següents opcions:</span><span class="sxs-lookup"><span data-stu-id="bb165-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="bb165-129">**Taula** : els termes de retenció del proveïdor s'apliquen a un sol proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="bb165-130">**Grup** : els termes de retenció del proveïdor s'apliquen a tots els proveïdors d'un grup de proveïdors.</span><span class="sxs-lookup"><span data-stu-id="bb165-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="bb165-131">**Tots** : els termes de retenció del proveïdor s'apliquen a tots els proveïdors.</span><span class="sxs-lookup"><span data-stu-id="bb165-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="bb165-132">En el camp **Proveïdor/Grup de proveïdors** , seleccioneu el proveïdor o grup de proveïdors al qual s'apliquen els termes de retenció del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="bb165-133">Si seleccioneu **Tots** en el pas anterior, aquest camp no està disponible.</span><span class="sxs-lookup"><span data-stu-id="bb165-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="bb165-134">En el camp **Termes de retenció del proveïdor** , seleccioneu els termes de retenció que heu creat en el procediment anterior.</span><span class="sxs-lookup"><span data-stu-id="bb165-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="bb165-135">Si el projecte també té termes de pagament després del cobrament (PWP) establerts per al proveïdor, introduïu el percentatge de llindar per al projecte en el camp **Percentatge de llindar de PWP**.</span><span class="sxs-lookup"><span data-stu-id="bb165-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="bb165-136">Els termes de retenció del proveïdor també es mostren a les comandes de compra que creeu per al proveïdor.</span><span class="sxs-lookup"><span data-stu-id="bb165-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
