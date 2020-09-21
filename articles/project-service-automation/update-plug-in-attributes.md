---
title: Actualitzar els atributs de complement per incloure noves dimensions de preus
description: En aquest tema s'ofereix informació sobre l'actualització d'atributs de complement per a les dimensions de preus.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749532"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="6045f-103">Actualitzar els atributs de complement per incloure noves dimensions de preus</span><span class="sxs-lookup"><span data-stu-id="6045f-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="6045f-104">Si no utilitzeu el les característiques d'oferta i contractació del Project Service Automation (PSA), podeu ometre aquest tema.</span><span class="sxs-lookup"><span data-stu-id="6045f-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="6045f-105">En aquest tema s'assumeix que heu completat els procediments dels temes [Crear camps i entitats personalitzats](create-custom-fields-entities.md), [Afegir camps personalitzats a la configuració de preus i les entitats transaccionals](field-references.md) i [Configurar camps personalitzats com a dimensions de preus](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="6045f-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="6045f-106">Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema.</span><span class="sxs-lookup"><span data-stu-id="6045f-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="6045f-107">Quan es crea un detall de la línia d'oferta a la pàgina **Línia d'oferta** d'una línia d'oferta de projecte, el sistema crea dues línies d'estimació en segon terme, una línia per a la part del cost de l'estimació i una per a la part de les vendes.</span><span class="sxs-lookup"><span data-stu-id="6045f-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="6045f-108">Això és el mateix per a les línies de contracte del projecte.</span><span class="sxs-lookup"><span data-stu-id="6045f-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="6045f-109">Quan feu un canvi a la quantitat o un camp a la part del cost, aquest canvi es propaga a la part de vendes.</span><span class="sxs-lookup"><span data-stu-id="6045f-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="6045f-110">Això és possible a causa dels complements següents que s'han de tornar a registrar després d'haver passat el canvi a les dimensions de preus.</span><span class="sxs-lookup"><span data-stu-id="6045f-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="6045f-111">PreOperationContractLineDetailUpdate - Actualitzacions **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6045f-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="6045f-112">PreOperationQuoteLineDetailUpdate - Actualitzacions **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6045f-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="6045f-113">En els passos següents s'explica el procés per registrar els complements.</span><span class="sxs-lookup"><span data-stu-id="6045f-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="6045f-114">Obriu el **Plugin Registration Tool** i connecteu-vos a la instància en línia.</span><span class="sxs-lookup"><span data-stu-id="6045f-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="6045f-115">Feu clic a **Cerca** i cerqueu el complement que voleu actualitzar.</span><span class="sxs-lookup"><span data-stu-id="6045f-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Captura de pantalla de l'arbre de cerca](media/PRT-1.png)

3. <span data-ttu-id="6045f-117">Un cop s'hagi trobat el complement, seleccioneu-lo i, a continuació,feu clic a **Selecciona al formulari principal**.</span><span class="sxs-lookup"><span data-stu-id="6045f-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="6045f-118">Seleccioneu el pas del complement que voleu actualitzar, feu clic amb el botó dret i, a continuació, seleccioneu **Actualitza**.</span><span class="sxs-lookup"><span data-stu-id="6045f-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Captura de pantalla del complement que s'actualitzarà](media/PRT-2.png)
 
5. <span data-ttu-id="6045f-120">A la finestra de l'actualització, feu clic als punts suspensius (**...**) als atributs de filtratge.</span><span class="sxs-lookup"><span data-stu-id="6045f-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Captura de pantalla de la informació de configuració d'actualització d'un pas existent](media/PRT-3.png)
 
6. <span data-ttu-id="6045f-122">Seleccioneu les caselles de selecció de l'atribut de preus.</span><span class="sxs-lookup"><span data-stu-id="6045f-122">Select the pricing attribute check boxes.</span></span>

 ![Captura de pantalla que mostra la casella de selecció dels atributs de preus](media/PRT-4.png)

7. <span data-ttu-id="6045f-124">Feu clic a **D'acord** per tancar la pàgina i, a continuació, seleccioneu **Actualitza el pas**.</span><span class="sxs-lookup"><span data-stu-id="6045f-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Captura de pantalla que mostra el botó "Actualitza el pas"](media/PRT-5.png)
 
8. <span data-ttu-id="6045f-126">Repetiu aquest procés per al segon complement, **PreOperationQuoteLineDetail - Actualització de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="6045f-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="6045f-127">Tanqueu el Plugin Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="6045f-127">Close the plug-in registration tool.</span></span>

