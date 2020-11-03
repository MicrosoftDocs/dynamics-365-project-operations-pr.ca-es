---
title: Creació i confirmació de diaris de correcció
description: En aquest tema es proporciona informació sobre com crear i confirmar un diari de correcció.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072209"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="42916-103">Creació i confirmació de diaris de correcció</span><span class="sxs-lookup"><span data-stu-id="42916-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="42916-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="42916-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="42916-105">De vegades, pot ser que s'introdueixi una entrada de temps o de despesa incorrectament.</span><span class="sxs-lookup"><span data-stu-id="42916-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="42916-106">Per exemple, un consultor podria seleccionar una data incorrecta en el moment de crear una entrada de temps o podria transposar els números en introduir una despesa.</span><span class="sxs-lookup"><span data-stu-id="42916-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="42916-107">Si un consultor no pot fer les actualitzacions a les entrades enviades, un administrador pot corregir directament l'entrada d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="42916-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="42916-108">Per completar els procediments d'aquest tema, necessitareu permisos d'administrador.</span><span class="sxs-lookup"><span data-stu-id="42916-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="42916-109">Correcció de les entrades de temps aprovades</span><span class="sxs-lookup"><span data-stu-id="42916-109">Correct approved time entries</span></span>     

<span data-ttu-id="42916-110">Completeu els passos següents per corregir una o diverses entrades de temps d'un projecte.</span><span class="sxs-lookup"><span data-stu-id="42916-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="42916-111">A l'àrea **Vendes'** , seleccioneu **Transaccions** i, a continuació, seleccioneu **Temps aprovat**.</span><span class="sxs-lookup"><span data-stu-id="42916-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="42916-112">A la llista **Temps aprovat** , localitzeu i seleccioneu una o diverses entrades de temps aprovades per corregir.</span><span class="sxs-lookup"><span data-stu-id="42916-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="42916-113">Podeu utilitzar el filtre per cercar entrades relacionades.</span><span class="sxs-lookup"><span data-stu-id="42916-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="42916-114">Per exemple, podeu aplicar el filtre segons un ID de projecte i seleccionar totes les entrades de temps aprovades amb l'identificador del projecte.</span><span class="sxs-lookup"><span data-stu-id="42916-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="42916-115">Seleccioneu **Entrades correctes**.</span><span class="sxs-lookup"><span data-stu-id="42916-115">Select **Correct entries**.</span></span> <span data-ttu-id="42916-116">Es crearà automàticament un diari de correcció nou amb el tipus assignat **Correcció de temps**.</span><span class="sxs-lookup"><span data-stu-id="42916-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="42916-117">Les entrades que heu seleccionat s'afegiran al diari.</span><span class="sxs-lookup"><span data-stu-id="42916-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="42916-118">A la pàgina **Diari nou** , introduïu una **descripció** per al diari de correcció i, a continuació, seleccioneu la pestanya **Correccions d'entrades de temps**.</span><span class="sxs-lookup"><span data-stu-id="42916-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="42916-119">A la secció **Valors nous per a les entrades de temps** , actualitzeu els camps amb la informació correcta segons calgui.</span><span class="sxs-lookup"><span data-stu-id="42916-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="42916-120">Per exemple, podeu canviar el projecte assignat o el recurs que es pot reservar.</span><span class="sxs-lookup"><span data-stu-id="42916-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="42916-121">Seleccioneu **Visualització prèvia**.</span><span class="sxs-lookup"><span data-stu-id="42916-121">Select **Preview**.</span></span> <span data-ttu-id="42916-122">Al quadre de diàleg, seleccioneu **Accepta**.</span><span class="sxs-lookup"><span data-stu-id="42916-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="42916-123">A la pestanya **Línies del llibre diari** , podeu visualitzar una llista dels valors reals originals relacionats amb les entrades de temps seleccionades que s'han invertit i les línies corresponents corregides que s'han creat.</span><span class="sxs-lookup"><span data-stu-id="42916-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="42916-124">Si s'han de fer correccions addicionals, repetiu els passos 5 i 6.</span><span class="sxs-lookup"><span data-stu-id="42916-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="42916-125">Tots els valors reals corregits tindran els mateixos valors que heu seleccionat a la secció **Valors nous per a les entrades de temps**.</span><span class="sxs-lookup"><span data-stu-id="42916-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="42916-126">Si les correccions es mostren segons el previst, seleccioneu **Confirma**.</span><span class="sxs-lookup"><span data-stu-id="42916-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="42916-127">Al quadre de diàleg, seleccioneu **Accepta**.</span><span class="sxs-lookup"><span data-stu-id="42916-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="42916-128">Torneu a l'àrea **Vendes** , seleccioneu **Projectes** i, a continuació, obriu el projecte per al qual acabeu d'actualitzar les entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="42916-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="42916-129">A la pàgina **Projectes** , de la pestanya **Valors reals** , visualitzeu els canvis que heu fet.</span><span class="sxs-lookup"><span data-stu-id="42916-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="42916-130">Si la pestanya **Valors reals** no està visible, seleccioneu **Relacionat** > **Valors reals**.</span><span class="sxs-lookup"><span data-stu-id="42916-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="42916-131">A la llista **Visualització associada de valors reals** , podeu veure que les entrades de temps originals que s'han invertit encara es mostren, així com les entrades de temps corregides corresponents.</span><span class="sxs-lookup"><span data-stu-id="42916-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="42916-132">Per exemple, en el gràfic següent hi ha dos elements de línia amb una quantitat de 8,00 que tenen dèbits enumerats a la columna Import.</span><span class="sxs-lookup"><span data-stu-id="42916-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="42916-133">A més, hi ha dos elements de línia amb una quantitat de -8,00 que mostren els imports dels crèdits a la columna Import.</span><span class="sxs-lookup"><span data-stu-id="42916-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="42916-134">Aquestes correccions aporten la quantitat a zero.</span><span class="sxs-lookup"><span data-stu-id="42916-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="42916-135">Correcció de les entrades de despeses aprovades</span><span class="sxs-lookup"><span data-stu-id="42916-135">Correct approved expense entries</span></span>

<span data-ttu-id="42916-136">Seguiu aquests passos per corregir una o diverses entrades de despeses.</span><span class="sxs-lookup"><span data-stu-id="42916-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="42916-137">A l'àrea **Vendes** , a la subfinestra de navegació esquerra, a **Transaccions** , seleccioneu **Despeses aprovades**.</span><span class="sxs-lookup"><span data-stu-id="42916-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="42916-138">A la llista **Despeses aprovades** , seleccioneu el projecte que voleu corregir i, a continuació, seleccioneu **Entrades correctes**.</span><span class="sxs-lookup"><span data-stu-id="42916-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="42916-139">Es crearà automàticament un diari de correcció nou amb el tipus assignat **Correcció de despesa**.</span><span class="sxs-lookup"><span data-stu-id="42916-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="42916-140">A la pàgina **Diari nou** , introduïu una **descripció** per a la correcció i, a la pestanya **Correcció de despeses** , a la secció **Valors nous per a les despeses** , seleccioneu els camps de dades que voleu corregir a les línies de despesa seleccionades.</span><span class="sxs-lookup"><span data-stu-id="42916-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="42916-141">Per exemple, podeu assignar la despesa a un altre **Projecte** , o bé corregir les opcions **Categoria de despesa** , **Data de la despesa** o **Recurs que es pot reservar**.</span><span class="sxs-lookup"><span data-stu-id="42916-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="42916-142">Seleccioneu **Visualització prèvia**.</span><span class="sxs-lookup"><span data-stu-id="42916-142">Select **Preview**.</span></span> <span data-ttu-id="42916-143">Al quadre de diàleg, seleccioneu **Accepta**.</span><span class="sxs-lookup"><span data-stu-id="42916-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="42916-144">Verifiqueu les correccions a la pestanya **Línies del llibre diari**. Podeu visualitzar una llista dels valors reals originals relacionats amb les entrades de despeses seleccionades que s'han invertit i les línies corresponents corregides que s'han creat.</span><span class="sxs-lookup"><span data-stu-id="42916-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="42916-145">Si els valors corregits es mostren segons el previst, seleccioneu **Confirma**.</span><span class="sxs-lookup"><span data-stu-id="42916-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="42916-146">Al quadre de diàleg, seleccioneu **Accepta**.</span><span class="sxs-lookup"><span data-stu-id="42916-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="42916-147">Si els valors no es mostren com s'esperava, seleccioneu **Cancel·la** per tornar a la llista **Despeses aprovades**.</span><span class="sxs-lookup"><span data-stu-id="42916-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="42916-148">Repetiu els passos del 2 al 5.</span><span class="sxs-lookup"><span data-stu-id="42916-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="42916-149">Els valors reals corregits tindran els mateixos valors que heu seleccionat a la secció **Valors nous per a les despeses**.</span><span class="sxs-lookup"><span data-stu-id="42916-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="42916-150">Després de confirmar el diari de correcció, torneu al projecte o als projectes que heu actualitzat, per visualitzar els canvis.</span><span class="sxs-lookup"><span data-stu-id="42916-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="42916-151">A la pàgina del projecte, a la pestanya **Valors reals** , reviseu **Visualització associada de valors reals**.</span><span class="sxs-lookup"><span data-stu-id="42916-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="42916-152">Les entrades originals i les corregides es mostren a la llista.</span><span class="sxs-lookup"><span data-stu-id="42916-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="42916-153">En el següent gràfic es mostren els imports d'entrada de despeses originals i les quantitats d'entrada de despeses corregides corresponents.</span><span class="sxs-lookup"><span data-stu-id="42916-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


