---
title: Afegir nous formularis d'entitat personalitzats (Project Service Automation 2.x)
description: En aquest tema es proporciona informació sobre com afegir formularis d'entitat personalitzats per a oportunitats, ofertes, comandes o factures al Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144581"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="f1ada-103">Afegir nous formularis d'entitat personalitzats (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="f1ada-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="f1ada-104">Camp Tipus</span><span class="sxs-lookup"><span data-stu-id="f1ada-104">Type field</span></span> 

<span data-ttu-id="f1ada-105">El Dynamics 365 Project Service Automation es basa en el camp **Tipus** (**msdyn\_ordertype**) de les entitats Oportunitat, Oferta, Comanda i Factura per distingir les versions **basades en el treball** d'aquestes entitats de les versions **basades en l'element** i **basades en el servei**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="f1ada-106">Les versions de treball d'aquestes entitats són gestionades pel PSA.</span><span class="sxs-lookup"><span data-stu-id="f1ada-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="f1ada-107">Una gran quantitat de lògica empresarial al costat de client i al costat del servidor de la solució depèn del camp **Tipus**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="f1ada-108">Per tant, és important que el camp s'inicialitzi amb un valor correcte quan es creïn les entitats.</span><span class="sxs-lookup"><span data-stu-id="f1ada-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="f1ada-109">Un valor incorrecte pot provocar comportaments incorrectes i pot ser que la lògica empresarial no s'executi correctament.</span><span class="sxs-lookup"><span data-stu-id="f1ada-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="f1ada-110">Commutació automàtica de formulari</span><span class="sxs-lookup"><span data-stu-id="f1ada-110">Automatic form switching</span></span>

<span data-ttu-id="f1ada-111">Per evitar la corrupció de dades potencial i comportaments inesperats que són causats per la inicialització incorrecta i l'edició dels registres de l'entitat de vendes, el PSA ara inclou una lògica per a la commutació automàtica de formularis en els formularis de fàbrica.</span><span class="sxs-lookup"><span data-stu-id="f1ada-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="f1ada-112">Aquesta lògica duu els usuaris al formulari correcte per treballar amb la versió basada en el treball o qualsevol altre tipus d'entitat Oportunitat, Oferta, Comanda o Factura.</span><span class="sxs-lookup"><span data-stu-id="f1ada-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="f1ada-113">Quan un usuari obre la versió basada en la feina d'una entitat Oportunitat, Oferta, Comanda o Factura, el formulari canvia a **Informació del projecte**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="f1ada-114">La lògica de canvi de formularis automàtic es basa en l'assignació entre el valor **formId** i el camp **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f1ada-115">Tots els formularis de fàbrica s'ha afegit a l'assignació.</span><span class="sxs-lookup"><span data-stu-id="f1ada-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="f1ada-116">No obstant, els formularis personalitzats s'han d'afegir manualment per indicar quina versió de l'entitat pretenen gestionar.</span><span class="sxs-lookup"><span data-stu-id="f1ada-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="f1ada-117">Això es basa en el camp **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="f1ada-118">Si el canvi de formulari no és a l'assignació, la lògica canviarà al formulari de fàbrica, segons el valor desat al camp **msdyn\_ordertype** de l'entitat.</span><span class="sxs-lookup"><span data-stu-id="f1ada-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="f1ada-119">Afegir formularis personalitzats i activar la lògica de commutació de formulari</span><span class="sxs-lookup"><span data-stu-id="f1ada-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="f1ada-120">A l'exemple següent es mostra com afegir un formulari personalitzat, **La meva informació de projecte**, per tal que funcioni amb oportunitats basades en el treball.</span><span class="sxs-lookup"><span data-stu-id="f1ada-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="f1ada-121">El mateix procés s'utilitza per afegir formularis personalitzats de manera que funcionin amb ofertes, comandes i factures.</span><span class="sxs-lookup"><span data-stu-id="f1ada-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="f1ada-122">Seguiu els passos que es descriuen a continuació per crear una versió personalitzada del formulari **Informació del projecte**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="f1ada-123">A l'entitat Oportunitat, obriu el formulari **Informació del projecte** i deseu una còpia amb el nom **La meva informació del projecte**.</span><span class="sxs-lookup"><span data-stu-id="f1ada-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="f1ada-124">Obriu el formulari nou i, a continuació, a les propietats, assegureu-vos que els scripts d'inicialització del formulari del formulari **Informació del projecte** estiguin presents.</span><span class="sxs-lookup"><span data-stu-id="f1ada-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f1ada-125">No suprimiu els scripts.</span><span class="sxs-lookup"><span data-stu-id="f1ada-125">Don't remove the scripts.</span></span> <span data-ttu-id="f1ada-126">Altrament, pot ser que algunes dades s'inicialitzin incorrectament.</span><span class="sxs-lookup"><span data-stu-id="f1ada-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="f1ada-127">Verifiqueu que el camp **Tipus** (**msdyn\_ordertype**) estigui present al formulari.</span><span class="sxs-lookup"><span data-stu-id="f1ada-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="f1ada-128">No suprimiu aquest camp.</span><span class="sxs-lookup"><span data-stu-id="f1ada-128">Don't remove this field.</span></span> <span data-ttu-id="f1ada-129">Altrament, els scripts d'inicialització fallaran.</span><span class="sxs-lookup"><span data-stu-id="f1ada-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="f1ada-130">Cerqueu el valor **formId** del formulari nou.</span><span class="sxs-lookup"><span data-stu-id="f1ada-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="f1ada-131">Podeu completar-ho de dues maneres:</span><span class="sxs-lookup"><span data-stu-id="f1ada-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="f1ada-132">Exporteu el formulari **La meva informació del projecte** com a part d'una solució no administrada i, a continuació, cerqueu el valor **formId** al fitxer customization.xml de la solució exportada.</span><span class="sxs-lookup"><span data-stu-id="f1ada-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="f1ada-133">Obriu el formulari **La meva informació del projecte** a l'editor de formularis i, a continuació, cerqueu l'identificador únic global (GUID) al costat del paràmetre **formId** a l'adreça URL, com a es mostra a la il·lustració següent.</span><span class="sxs-lookup"><span data-stu-id="f1ada-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Valor formId del formulari nou a l'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="f1ada-135">Creeu una assignació **msdyn\_ordertype** per al valor **formId** editant el recurs web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="f1ada-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="f1ada-136">Suprimiu el codi del recurs i, a continuació, substituïu-lo pel codi següent.</span><span class="sxs-lookup"><span data-stu-id="f1ada-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="f1ada-137">Deseu i publiqueu les personalitzacions.</span><span class="sxs-lookup"><span data-stu-id="f1ada-137">Save and then publish the customizations.</span></span>
