---
title: Actualitzar els atributs de complement per incloure noves dimensions de preus
description: En aquest tema s'ofereix informació sobre l'actualització d'atributs de complement per a les dimensions de preus.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: d04561fb6bcbc64f6ad3ea922bff1912824be64c6bb2b18cddd95e9b1b5c7850
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988774"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Actualitzar els atributs de complement per incloure noves dimensions de preus

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Si no utilitzeu el les característiques d'oferta i contractació del Project Service Automation (PSA), podeu ometre aquest tema.

En aquest tema s'assumeix que heu completat els procediments dels temes [Crear camps i entitats personalitzats](create-custom-fields-entities.md), [Afegir camps personalitzats a la configuració de preus i les entitats transaccionals](field-references.md) i [Configurar camps personalitzats com a dimensions de preus](set-up-pricing-dimensions.md). Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema.

Quan es crea un detall de la línia d'oferta a la pàgina **Línia d'oferta** d'una línia d'oferta de projecte, el sistema crea dues línies d'estimació en segon terme, una línia per a la part del cost de l'estimació i una per a la part de les vendes. Això és el mateix per a les línies de contracte del projecte.

Quan feu un canvi a la quantitat o un camp a la part del cost, aquest canvi es propaga a la part de vendes. Això és possible a causa dels complements següents que s'han de tornar a registrar després d'haver passat el canvi a les dimensions de preus.

- PreOperationContractLineDetailUpdate - Actualitzacions **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Actualitzacions **msdyn_quotelinetransaction**.

En els passos següents s'explica el procés per registrar els complements.

1. Obriu el **Plugin Registration Tool** i connecteu-vos a la instància en línia.
2. Feu clic a **Cerca** i cerqueu el complement que voleu actualitzar.

 ![Captura de pantalla de l'arbre de cerca.](media/PRT-1.png)

3. Un cop s'hagi trobat el complement, seleccioneu-lo i, a continuació,feu clic a **Selecciona al formulari principal**.

4. Seleccioneu el pas del complement que voleu actualitzar, feu clic amb el botó dret i, a continuació, seleccioneu **Actualitza**.

 ![Captura de pantalla del complement que s'actualitzarà.](media/PRT-2.png)
 
5. A la finestra de l'actualització, feu clic als punts suspensius (**...**) als atributs de filtratge.

 ![Captura de pantalla de la informació de configuració d'actualització d'un pas existent.](media/PRT-3.png)
 
6. Seleccioneu les caselles de selecció de l'atribut de preus.

 ![Captura de pantalla que mostra la casella de selecció dels atributs de preus.](media/PRT-4.png)

7. Feu clic a **D'acord** per tancar la pàgina i, a continuació, seleccioneu **Actualitza el pas**.

 ![Captura de pantalla que mostra el botó "Actualitza el pas".](media/PRT-5.png)
 
8. Repetiu aquest procés per al segon complement, **PreOperationQuoteLineDetail - Actualització de msdyn_quotelinetransaction**.

9. Tanqueu el Plugin Registration Tool.



[!INCLUDE[footer-include](../includes/footer-banner.md)]