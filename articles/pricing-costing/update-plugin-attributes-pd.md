---
title: Actualització dels atributs de complement amb noves dimensions de preus
description: En aquest tema s'ofereix informació sobre com actualitzar atributs de complement per a les dimensions de preus.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988324"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Actualitzar els atributs de complement amb noves dimensions de preus

En aquest tema s'ofereix informació sobre com actualitzar atributs de complement per a les dimensions de preus.

> [!NOTE]
> Aquest tema només és aplicable a les característiques de l'oferta i el contracte del Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Requisits previs
Abans de completar els passos d'aquest tema, heu d'haver completat els procediments en els temes següents:

  - [Creació de camps i entitats personalitzats](create-custom-fields-entities-pricing-dimensions.md) 
  - [Addició de camps personalitzats a la configuració de preus i a entitats transaccionals ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configuració de camps personalitzats com a dimensions de preus](set-up-custom-fields-pricing-dimensions.md). 
  
Si no heu completat aquests procediments, aneu enrere per completar-los i torneu a aquest tema.

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