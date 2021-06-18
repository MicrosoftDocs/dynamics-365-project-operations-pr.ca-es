---
title: Configuració de la integració del Project Operations per entitat jurídica
description: Aquest tema proporciona informació sobre la configuració de la integració per entitat jurídica al Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000064"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="90790-103">Configuració de la integració del Project Operations per entitat jurídica</span><span class="sxs-lookup"><span data-stu-id="90790-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="90790-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="90790-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="90790-105">Aquest tema us guia pels passos necessaris a l'hora de configurar el Dynamics 365 Project Operations per entitat legal.</span><span class="sxs-lookup"><span data-stu-id="90790-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="90790-106">Habilitar les claus de característiques al Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="90790-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="90790-107">Completeu els passos següents per habilitar les característiques necessàries.</span><span class="sxs-lookup"><span data-stu-id="90790-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="90790-108">Al Dynamics 365 Finance, aneu a l'àrea de treball **Administració de característiques**.</span><span class="sxs-lookup"><span data-stu-id="90790-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="90790-109">A **Llista de característiques**, cerqueu i habiliteu les següents característiques:</span><span class="sxs-lookup"><span data-stu-id="90790-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="90790-110">**Habilitar diverses línies de contracte per a un projecte**</span><span class="sxs-lookup"><span data-stu-id="90790-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="90790-111">**Habilitar el Project Operations al Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="90790-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="90790-112">Si no veieu **Claus de característiques** a la llista, comproveu que la vostra versió del Finance compleix el requisit mínim de versió (versió 10.0.13 de l'aplicació amb totes les actualitzacions de qualitat aplicades o superior).</span><span class="sxs-lookup"><span data-stu-id="90790-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="90790-113">Seleccioneu **Comprova si hi ha actualitzacions** per actualitzar la llista de característiques.</span><span class="sxs-lookup"><span data-stu-id="90790-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="90790-114">Definir l'escenari d'implementació del Project Operations per a una entitat jurídica</span><span class="sxs-lookup"><span data-stu-id="90790-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="90790-115">Podeu habilitar el Project Operations al Dynamics 365 Customer Engagement a nivell d'entitat jurídica.</span><span class="sxs-lookup"><span data-stu-id="90790-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="90790-116">Podeu tenir una entitat jurídica utilitzant el Project Operations al Dynamics 365 Customer Engagement per a escenaris basats en recursos/sense existències.</span><span class="sxs-lookup"><span data-stu-id="90790-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="90790-117">En el mateix entorn, podeu tenir una altra entitat jurídica que utilitzi el Project Operations per a escenaris amb existències/producció.</span><span class="sxs-lookup"><span data-stu-id="90790-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="90790-118">Al Dynamics 365 Finance, aneu a **Administració de projectes i comptabilitat** > **Configuració** > **Paràmetres globals de l'administració de projectes i comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="90790-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="90790-119">A llista d'entitats jurídiques disponibles, seleccioneu les entitats on s'habilitaran les característiques de diverses línies de contracte i el Project Operations al Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="90790-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="90790-120">Deixa sense seleccionar les entitats jurídiques que utilitzaran el Project Operations per a escenaris amb existències/producció.</span><span class="sxs-lookup"><span data-stu-id="90790-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="90790-121">Només es pot seleccionar una entitat jurídica si no té cap projecte existent.</span><span class="sxs-lookup"><span data-stu-id="90790-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="90790-122">Configuració dels paràmetres de la comptabilitat i l'administració de projectes</span><span class="sxs-lookup"><span data-stu-id="90790-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="90790-123">Cada entitat legal que utilitza el Project Operations al Dynamics 365 Customer Engagement necessita un conjunt de paràmetres per defecte.</span><span class="sxs-lookup"><span data-stu-id="90790-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="90790-124">Aquests paràmetres estan configurats a la pestanya **Project Operations** a la pestanya **Paràmetres de l'administració de projectes i comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="90790-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="90790-125">Els paràmetres són:</span><span class="sxs-lookup"><span data-stu-id="90790-125">The parameters are:</span></span>

  - <span data-ttu-id="90790-126">**Valors per defecte de tipus de facturació**: el Project Operations utilitza un conjunt fix de valors per defecte de tipus de facturació que s'han d'assignar a les propietats de línia del Finance.</span><span class="sxs-lookup"><span data-stu-id="90790-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="90790-127">Creeu un registre per a cada tipus de facturació: **No especificada**, **Imputable**, **No imputable**, **Complementària** i **No disponible**.</span><span class="sxs-lookup"><span data-stu-id="90790-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="90790-128">**Valors per defecte de categoria del projecte**: seleccioneu les categories de projecte per defecte que s'utilitzaran per a cada tipus d'operació.</span><span class="sxs-lookup"><span data-stu-id="90790-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="90790-129">Aquests valors per defecte s'utilitzaran al **Diari d'integració del Project Operations** i en estimacions on no s'especifiqui cap categoria de transacció per al valor real del projecte.</span><span class="sxs-lookup"><span data-stu-id="90790-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="90790-130">**Previsions**: seleccioneu el model de previsió que s'utilitzarà per a les estimacions de temps i despeses.</span><span class="sxs-lookup"><span data-stu-id="90790-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]