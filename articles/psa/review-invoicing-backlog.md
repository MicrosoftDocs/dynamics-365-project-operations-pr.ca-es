---
title: Revisar el registre de facturació dels projectes i dels contractes del projecte
description: En aquest article s'ofereix informació sobre com es poden revisar els registres de temps, despeses i productes, i com marcar-los com a preparats per a la facturació.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 833ace7fd6285191f4b023a029286cd36b5de8f4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928880"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Revisar el registre de facturació dels projectes i dels contractes del projecte

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Quan una transacció està preparada per tenir una factura creada i processada, la transacció s'ha de marcar com a **Llesta per facturar**. Aquest article descriu els tipus de transaccions que es poden crear.

## <a name="review-the-time-and-material-billing-backlog"></a>Revisar el registre de facturació de temps i material

Quan s'envia una entrada de temps o de la despesa i s'aprova per a un projecte, el PSA crea un valor real de projecte. Si la combinació de la classe de projecte i transacció s'assignen a una línia de contracte per a un projecte de temps i materials, dos valors reals es creen quan s'aprova l'entrada:

- Valor real de cost 
- Valor real de vendes no facturades

Els valors reals de vendes no facturades representen el registre de facturació i l'estat de facturació s'ha de definir com a **Llest per facturar**. Quan es crea una factura de projecte, els valors reals de vendes que no s'han facturat que s'han marcat com a **Llest per facturar** es copien com a detalls de la línia de factura.

Per revisar el registre de facturació per temps i materials, aneu a **Vendes** \> **Facturació** \> **Registre de facturació de temps i material**. Seleccioneu tots els valors reals de vendes no facturades que estiguin preparats per a facturar i, a continuació, seleccioneu **Llest per facturar**. L'estat de facturació d'aquests valors reals canvia a **Llest per facturar**.

![Treball pendent de facturació de temps i material.](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Revisar el registre de facturació de producte

Al PSA, quan un contracte de projecte té línies de contracte basades en productes, aquestes línies es tenen en compte per a la facturació cada vegada que es crea una factura per al contracte del projecte. Qualsevol producte que tingui línies de contracte marcades com a **Llest per facturar** es copia a la factura de projecte com a línies de factura de projecte.

Per revisar el registre d'entrada de facturació dels productes, aneu a **Vendes** \> **Facturació** \> **Registre de facturació de productes**. Seleccioneu totes les línies de vendes basades en productes que estiguin preparades per a facturar i, a continuació, seleccioneu **Llest per facturar**. L'estat de facturació d'aquestes línies canvia a **Llest per facturar**.

![Treball pendent de facturació de producte.](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Revisar les fites de facturació dels contractes de preu fix

Cada línia de contracte de projecte que té un mètode de facturació de preu fix ha de definir fites del contracte. Aquestes fites dels contractes només es poden facturar si es marquen com a **Llest per facturar**. 

Per revisar les fites de facturació, aneu a **Vendes** \> **Facturació** \> **Fites de preu fix**. Seleccioneu totes les fites que estiguin preparades per a facturar i, a continuació, seleccioneu **Llest per facturar**. L'estat de facturació d'aquestes fites canvia a **Llest per facturar**.

![Fites de preu fix.](media/FPBacklog.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
