---
title: Configuració de les tarifes de cost i de vendes per als materials
description: En aquest article s'ofereix informació sobre com configurar les taxes de cost i venda dels materials utilitzats en projectes.
author: rumant
ms.date: 03/21/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0a7d84c2dcaa228e06add2f3cb06a530b29e0e35
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911768"
---
# <a name="set-up-cost-and-sales-rates-for-materials"></a>Configuració de les tarifes de cost i de vendes per als materials

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu configurar els preus de cost i de vendes per als productes del Dynamics 365 Project Operations. Els preus de cost i de vendes dels productes només es poden enumerar en una moneda, que ha de ser la moneda de la capçalera de la llista de preus.

Per configurar les tarifes de cost i de vendes dels productes, seguiu aquests passos: 

1. Aneu a **Vendes** > **Clients** > **Llistes de preus** i seleccioneu **Nou** per crear una llista de preus nova. 
2. Als **Elements de la llista de preus**, al menú de subquadrícula, seleccioneu **Element de llista de preus nou**. 
3. A la pàgina **Creació ràpida**, introduïu el producte i la unitat per a la qual esteu creant el preu nou.

Per obtenir més informació sobre com definir els preus dels articles del catàleg, vegeu [Definir els preus dels productes amb llistes de preus i elements](/dynamics365/sales/create-price-lists-price-list-items-define-pricing-products) de llista de preus i [precisió decimal en moneda i preus](/dynamics365/sales/decimal-precision-currency-pricing).
> [!NOTE]
> Dynamics 365 Project Operations no admet tots els mètodes de preus dels productes com a Vendes del Dynamics 365. L'únic mètode de preus compatible amb els productes que s'utilitzaran en projectes és *l'import de la moneda*.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
