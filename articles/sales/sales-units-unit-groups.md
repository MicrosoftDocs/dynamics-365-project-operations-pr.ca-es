---
title: Unitats i grups d'unitats
description: En aquest tema es proporciona informació sobre com crear unitats i grups d'unitat al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898744"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="254c5-103">Unitats i grups d'unitats</span><span class="sxs-lookup"><span data-stu-id="254c5-103">Units and unit groups</span></span>

<span data-ttu-id="254c5-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="254c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="254c5-105">Les unitats són les quantitats o mesures en les quals vendreu els productes o serveis.</span><span class="sxs-lookup"><span data-stu-id="254c5-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="254c5-106">Per exemple, si veneu materials per a jardineria, els podeu vendre en unitats de paquets, caixes i palets.</span><span class="sxs-lookup"><span data-stu-id="254c5-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="254c5-107">Un grup d'unitats és un conjunt d'aquestes unitats diferents.</span><span class="sxs-lookup"><span data-stu-id="254c5-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="254c5-108">Per completar els passos d'aquest tema, assegureu-vos que se us hagi assignat la funció Administrador del sistema o Administrador del Sales Professional o que tingueu permisos equivalents.</span><span class="sxs-lookup"><span data-stu-id="254c5-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="254c5-109">Crear un grup d'unitats</span><span class="sxs-lookup"><span data-stu-id="254c5-109">Create a unit group</span></span>

1. <span data-ttu-id="254c5-110">En el mapa del lloc, seleccioneu **Unitats**.</span><span class="sxs-lookup"><span data-stu-id="254c5-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="254c5-111">Seleccioneu **Nou** i, al quadre de diàleg **Crea un grup d'unitats**, introduïu el nom de la unitat.</span><span class="sxs-lookup"><span data-stu-id="254c5-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="254c5-112">Al camp **Unitat principal**, introduïu la unitat de mesura comuna més baixa en què es vendrà el producte.</span><span class="sxs-lookup"><span data-stu-id="254c5-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="254c5-113">Per exemple, podeu introduir "peça" o "unça".</span><span class="sxs-lookup"><span data-stu-id="254c5-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="254c5-114">Seleccioneu **D'acord**.</span><span class="sxs-lookup"><span data-stu-id="254c5-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="254c5-115">Afegir unitats a un grup d'unitats</span><span class="sxs-lookup"><span data-stu-id="254c5-115">Add units to a unit group</span></span>

1. <span data-ttu-id="254c5-116">Obriu un grup d'unitats i, a la pestanya **Relacionat**, seleccioneu **Unitats**.</span><span class="sxs-lookup"><span data-stu-id="254c5-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="254c5-117">Veureu que la unitat principal ja s'ha afegit.</span><span class="sxs-lookup"><span data-stu-id="254c5-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="254c5-118">Seleccioneu **Afegeix una unitat nova** i a la pàgina **Creació ràpida: unitat**, al camp **Nom**, introduïu el nom de la unitat.</span><span class="sxs-lookup"><span data-stu-id="254c5-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="254c5-119">Al camp **Quantitat**, introduïu la quantitat que contindrà la unitat.</span><span class="sxs-lookup"><span data-stu-id="254c5-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="254c5-120">Per exemple, si una caixa conté dues peces, introduïu "2".</span><span class="sxs-lookup"><span data-stu-id="254c5-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="254c5-121">Al camp **Unitat de base**, seleccioneu una unitat de base per establir la unitat de mesura més baixa per a la unitat.</span><span class="sxs-lookup"><span data-stu-id="254c5-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="254c5-122">Per exemple, podeu seleccionar "peça".</span><span class="sxs-lookup"><span data-stu-id="254c5-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="254c5-123">Seleccioneu **Desa**:</span><span class="sxs-lookup"><span data-stu-id="254c5-123">Select **Save**:</span></span>
