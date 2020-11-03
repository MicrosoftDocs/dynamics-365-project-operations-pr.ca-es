---
title: Definició de calendaris de recursos
description: En aquest tema es proporciona informació sobre com definir els calendaris d'horaris de treball per als recursos al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072060"
---
# <a name="define-resource-calendars"></a><span data-ttu-id="84353-103">Definició de calendaris de recursos</span><span class="sxs-lookup"><span data-stu-id="84353-103">Define resource calendars</span></span>

<span data-ttu-id="84353-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="84353-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="84353-105">Tots els recursos reservables en un projecte han de tenir un calendari d'horari de treball per definir la seva disponibilitat.</span><span class="sxs-lookup"><span data-stu-id="84353-105">Each bookable resource working on a project must have a calendar of working hours to define their availability.</span></span> <span data-ttu-id="84353-106">Les hores de feina d'un recurs es poden definir de dues maneres:</span><span class="sxs-lookup"><span data-stu-id="84353-106">Workings hours for a resource can be defined in two ways:</span></span> 

   - <span data-ttu-id="84353-107">Definir regles de calendari individuals per a un recurs</span><span class="sxs-lookup"><span data-stu-id="84353-107">Define individual calendar rules for a resource</span></span>
   - <span data-ttu-id="84353-108">Aplicar una plantilla de calendari existent per al recurs</span><span class="sxs-lookup"><span data-stu-id="84353-108">Apply an existing calendar template for the resource</span></span>

## <a name="define-a-resources-working-hours"></a><span data-ttu-id="84353-109">Definir les hores de feina d'un recurs</span><span class="sxs-lookup"><span data-stu-id="84353-109">Define a resource's working hours</span></span>

1. <span data-ttu-id="84353-110">Al menú **Recursos** , seleccioneu **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="84353-110">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="84353-111">A la visualització de quadrícula, seleccioneu el **recurs reservable** aplicable.</span><span class="sxs-lookup"><span data-stu-id="84353-111">From the grid view, select the applicable **Bookable Resource**.</span></span>
3. <span data-ttu-id="84353-112">A la pàgina **Detalls del recurs** , seleccioneu la pestanya **Hores de feina**. Per defecte, el calendari de recursos reservables aplica per defecte les hores de feina de la plantilla d'hores de feina per defecte definida per a l'organització.</span><span class="sxs-lookup"><span data-stu-id="84353-112">On the **Resource Details** page, select the **Working Hours** tab. By default, the bookable resources calendar defaults to the working hours of the default work hour template that is defined for the organization.</span></span>
4. <span data-ttu-id="84353-113">Per actualitzar les hores de feina, feu clic amb el botó dret sobre la data d'inici de la regla de calendari proposada que es definirà.</span><span class="sxs-lookup"><span data-stu-id="84353-113">To update the working hours, right-click on the start date of the proposed calendar rule to be defined.</span></span> <span data-ttu-id="84353-114">Utilitzeu el menú de regla de calendari per definir una regla de calendari per a un dia concret, la resta de la sèrie o el calendari complet.</span><span class="sxs-lookup"><span data-stu-id="84353-114">Use the calendar rule menu to define a calendar rule for a specific day, the remainder of the series, or the entire calendar.</span></span>
5. <span data-ttu-id="84353-115">Després de seleccionar l'opció, podeu definir:</span><span class="sxs-lookup"><span data-stu-id="84353-115">After the option is selected, you can then define:</span></span>

    - <span data-ttu-id="84353-116">El dia de la setmana en què s'aplicaran les hores de feina.</span><span class="sxs-lookup"><span data-stu-id="84353-116">The day of the week where the working hours will apply.</span></span>
    - <span data-ttu-id="84353-117">Les hores de feina en cada dia.</span><span class="sxs-lookup"><span data-stu-id="84353-117">The working times within each day.</span></span>
    - <span data-ttu-id="84353-118">El fus horari de la regla de calendari.</span><span class="sxs-lookup"><span data-stu-id="84353-118">The time zone for the calendar rule.</span></span>
    - <span data-ttu-id="84353-119">Si escau, el temps sense treball també es pot especificar per a la regla.</span><span class="sxs-lookup"><span data-stu-id="84353-119">If applicable, non-working time can also be specified for the rule.</span></span>

## <a name="applying-a-calendar-template-to-a-resource"></a><span data-ttu-id="84353-120">Aplicar una plantilla de calendari a un recurs</span><span class="sxs-lookup"><span data-stu-id="84353-120">Applying a calendar template to a resource</span></span>

1. <span data-ttu-id="84353-121">Al menú **Recursos** , seleccioneu **Recursos**.</span><span class="sxs-lookup"><span data-stu-id="84353-121">On the **Resources** menu, select **Resources**.</span></span>
2. <span data-ttu-id="84353-122">Des de la visualització de quadrícula, seleccioneu fins a 25 **recursos reservables** que actualitzareu.</span><span class="sxs-lookup"><span data-stu-id="84353-122">From the grid view, select up to 25 **Bookable Resources** to update.</span></span>
3. <span data-ttu-id="84353-123">Seleccioneu **Defineix el calendari** i un diàleg us mostrarà una llista de plantilles d'hores de feina disponibles.</span><span class="sxs-lookup"><span data-stu-id="84353-123">Select **Set Calendar** and a dialog will prompt you with a list of available work hour templates.</span></span>
4. <span data-ttu-id="84353-124">Seleccioneu la plantilla que voleu utilitzeu i seleccioneu **Aplica**.</span><span class="sxs-lookup"><span data-stu-id="84353-124">Select the template you want to use, and then select **Apply**.</span></span>
