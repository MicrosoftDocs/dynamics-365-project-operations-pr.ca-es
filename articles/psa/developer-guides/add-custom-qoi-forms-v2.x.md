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
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Afegir nous formularis d'entitat personalitzats (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Camp Tipus 

El Dynamics 365 Project Service Automation es basa en el camp **Tipus** (**msdyn\_ordertype**) de les entitats Oportunitat, Oferta, Comanda i Factura per distingir les versions **basades en el treball** d'aquestes entitats de les versions **basades en l'element** i **basades en el servei**. Les versions de treball d'aquestes entitats són gestionades pel PSA. Una gran quantitat de lògica empresarial al costat de client i al costat del servidor de la solució depèn del camp **Tipus**. Per tant, és important que el camp s'inicialitzi amb un valor correcte quan es creïn les entitats. Un valor incorrecte pot provocar comportaments incorrectes i pot ser que la lògica empresarial no s'executi correctament.

## <a name="automatic-form-switching"></a>Commutació automàtica de formulari

Per evitar la corrupció de dades potencial i comportaments inesperats que són causats per la inicialització incorrecta i l'edició dels registres de l'entitat de vendes, el PSA ara inclou una lògica per a la commutació automàtica de formularis en els formularis de fàbrica. Aquesta lògica duu els usuaris al formulari correcte per treballar amb la versió basada en el treball o qualsevol altre tipus d'entitat Oportunitat, Oferta, Comanda o Factura. Quan un usuari obre la versió basada en la feina d'una entitat Oportunitat, Oferta, Comanda o Factura, el formulari canvia a **Informació del projecte**.

La lògica de canvi de formularis automàtic es basa en l'assignació entre el valor **formId** i el camp **msdyn\_ordertype**. Tots els formularis de fàbrica s'ha afegit a l'assignació. No obstant, els formularis personalitzats s'han d'afegir manualment per indicar quina versió de l'entitat pretenen gestionar. Això es basa en el camp **msdyn\_ordertype**. Si el canvi de formulari no és a l'assignació, la lògica canviarà al formulari de fàbrica, segons el valor desat al camp **msdyn\_ordertype** de l'entitat.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Afegir formularis personalitzats i activar la lògica de commutació de formulari

A l'exemple següent es mostra com afegir un formulari personalitzat, **La meva informació de projecte**, per tal que funcioni amb oportunitats basades en el treball. El mateix procés s'utilitza per afegir formularis personalitzats de manera que funcionin amb ofertes, comandes i factures.

Seguiu els passos que es descriuen a continuació per crear una versió personalitzada del formulari **Informació del projecte**.

1. A l'entitat Oportunitat, obriu el formulari **Informació del projecte** i deseu una còpia amb el nom **La meva informació del projecte**.
2. Obriu el formulari nou i, a continuació, a les propietats, assegureu-vos que els scripts d'inicialització del formulari del formulari **Informació del projecte** estiguin presents. 

    > [!IMPORTANT]
    > No suprimiu els scripts. Altrament, pot ser que algunes dades s'inicialitzin incorrectament.

3. Verifiqueu que el camp **Tipus** (**msdyn\_ordertype**) estigui present al formulari. 

    > [!IMPORTANT]
    > No suprimiu aquest camp. Altrament, els scripts d'inicialització fallaran.

4. Cerqueu el valor **formId** del formulari nou. Podeu completar-ho de dues maneres:

    - Exporteu el formulari **La meva informació del projecte** com a part d'una solució no administrada i, a continuació, cerqueu el valor **formId** al fitxer customization.xml de la solució exportada.
    - Obriu el formulari **La meva informació del projecte** a l'editor de formularis i, a continuació, cerqueu l'identificador únic global (GUID) al costat del paràmetre **formId** a l'adreça URL, com a es mostra a la il·lustració següent.

    ![Valor formId del formulari nou a l'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Creeu una assignació **msdyn\_ordertype** per al valor **formId** editant el recurs web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Suprimiu el codi del recurs i, a continuació, substituïu-lo pel codi següent.

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

6. Deseu i publiqueu les personalitzacions.
