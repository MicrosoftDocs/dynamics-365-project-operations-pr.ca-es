---
title: Configurar els costos estàndard per al treball i les despeses
description: En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749586"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar els costos estàndard per al treball i les despeses

[!include [task guide banner](../../includes/task-guide-banner.md)]

En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte. Aquesta tasca utilitza el conjunt de dades d'USSI.

1. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (hora)**.
2. Seleccioneu **Crea**.
3. En el camp **Data d'efectivitat**, introduïu una data.
4. Al camp **Preu de cost**, introduïu un número. Podeu configurar un preu de cost estàndard per a la categoria del projecte o bé podeu configurar un preu de cost per número de treballador, número de projecte, categoria, data o qualsevol combinació d'aquests valors. El preu de cost que s'aplica és el preu de cost amb el nivell màxim de detall.  
5. Seleccioneu **Desa**.
6. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (hora)**.
7. Seleccioneu **Crea**.
8. En el camp **Data d'efectivitat**, introduïu una data.
9. Seleccioneu una opció al camp **Vàlid durant**.
10. Al camp **Preu**, introduïu un número. Podeu configurar un preu de venda estàndard per a transaccions per hora o per a una categoria de projecte. També podeu configurar els preus de les vendes per número de treballador, número de projecte, categoria, data de la transacció o qualsevol combinació d'aquests valors. El preu de vendes real, que s'aplica quan un treballador introdueix una transacció al diari Hora, és el preu de vendes amb el nivell de detall més alt. Per exemple, si es configuren tant un preu de vendes general com un preu de vendes específic del treballador, el preu de vendes específic del treballador s'utilitza.  
11. Seleccioneu **Desa**.
12. Tanqueu la pàgina.
13. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (despesa)**.
14. Seleccioneu **Crea**.
15. En el camp **Data d'efectivitat**, introduïu una data.
16. Al camp **Preu de cost**, introduïu un número. Es poden emplenar diversos camps, però aquest és el mínim necessari per desar el registre.  
17. Seleccioneu **Desa**.
18. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (despesa)**.
19. Seleccioneu **Crea**.
20. En el camp **Data d'efectivitat**, introduïu una data.
21. Seleccioneu una opció al camp **Vàlid durant**.
22. Al camp **Preu**, introduïu un número. El preu de vendes real, que s'aplica quan un treballador introdueix transaccions en un diari de despeses, és el preu de vendes amb el nivell de detall més alt. Per exemple, si es configuren tant un preu de vendes general com un d'específic del treballador, el preu de vendes específic del treballador s'utilitza.  
23. Seleccioneu **Desa**.

