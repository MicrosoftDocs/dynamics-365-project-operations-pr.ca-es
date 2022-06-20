---
title: Actualització dels atributs de complement amb noves dimensions de preus
description: En aquest article s'ofereix informació sobre com actualitzar els atributs de complement per a les dimensions dels preus.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2ae502fea533d9f199ef5ee1cc85b623f08cbd84
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920002"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualitzar els atributs de complement amb noves dimensions de preus

En aquest article s'ofereix informació sobre com actualitzar els atributs de complement per a les dimensions dels preus.

> [!NOTE]
> Aquest article només s'aplica a les funcions d'oferta i contracte del Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Requisits previs
Abans de completar els passos d'aquest article, heu d'haver completat els tràmits en els articles següents:

  - [Creació de camps i entitats personalitzats](create-custom-fields-entities-pricing-dimensions.md) 
  - [Addició de camps personalitzats a la configuració de preus i a entitats transaccionals ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configuració de camps personalitzats com a dimensions de preus](set-up-custom-fields-pricing-dimensions.md). 
  
Si no heu completat aquests procediments, completeu-los i torneu a aquest article.

## <a name="register-a-plug-in"></a>Registrar un complement
Quan es crea un detall de línia d'oferta a la pàgina **Línia d'oferta** d'una línia d'oferta de projecte, el sistema crea dues línies d'estimació. Una línia és per al costat de l'estimació del cost i l'altra línia és per al costat de les vendes. Això és el mateix per a les línies de contracte del projecte.

Quan feu un canvi a la quantitat o un camp a la part del cost, aquest canvi es propaga a la part de vendes. Això és possible perquè els complements de PreOperation a les entitats de detall Quotelinedetail i contractline connecten atributs específics al costat del cost amb el costat de venda la transacció. Si necessiteu que els canvis als valors de la dimensió de preus de la banda de vendes es facin també al costat del cost, els complements següents s'han de tornar a registrar després de fer canvis en una dimensió de preus.

Aquests són els complements que s'han d'actualitzar i tornar a registrar:

- PreOperationContractLineDetailUpdate - **Actualitzar msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Actualitzar msdyn_quotelinetransaction**

Completeu els passos següents per actualitzar i tornar a registrar els complements.

1. Obriu **PluginRegistrationTool** i connecteu-vos a l'entorn de Dataverse de Project Operations.
2. Seleccioneu **Cerca** i escriviu les primeres lletres del complement que voleu actualitzar.
3. Un cop s'hagi trobat el complement, seleccioneu-lo i, a continuació, feu clic a **Selecciona al formulari principal**.
4. Seleccioneu el pas **Actualitzar msdyn_orderlinetransaction**, feu clic amb el botó dret i, a continuació, seleccioneu **Actualitza**.
5. Al quadre de diàleg **Actualització**, seleccioneu els punts suspensius (**...**) als atributs de filtratge.
6. La finestra d'atributs de filtratge s'obre i proporciona una llista de tots els atributs de l'entitat i les dimensions de preus. Activeu les caselles de selecció dels atributs de dimensió de preus.
7. Seleccioneu **D'acord** per tancar la pàgina i, a continuació, seleccioneu **Actualitza el pas**.
8. Repetiu els passos del 2 al 7 per al segon complement **PreOperationQuoteLineDetail**. Per a aquest complement, heu d'actualitzar el pas **Actualització de msdyn_quotelinetransaction**.
9. Tanqueu **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]