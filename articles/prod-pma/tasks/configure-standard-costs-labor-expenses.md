---
title: Configurar els costos estàndard per al treball i les despeses
description: En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte.
author: Yowelle
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
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072269"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar els costos estàndard per al treball i les despeses

[!include [banner](../../includes/banner.md)]

En aquest tema s'explica la manera de configurar els costos estàndard per al treball i les despeses d'un projecte. Aquesta tasca utilitza el conjunt de dades d'USSI.

1. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (hora)**.
2. Seleccioneu **Crea**.
3. En el camp **Data d'efectivitat** , introduïu una data.
4. Al camp **Preu de cost** , introduïu un número. Podeu configurar un preu de cost estàndard per a la categoria del projecte o bé podeu configurar un preu de cost per número de treballador, número de projecte, categoria, data o qualsevol combinació d'aquests valors. El preu de cost que s'aplica és el preu de cost amb el nivell màxim de detall.  
5. Seleccioneu **Desa**.
6. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (hora)**.
7. Seleccioneu **Crea**.
8. En el camp **Data d'efectivitat** , introduïu una data.
9. Seleccioneu una opció al camp **Vàlid durant**.
10. Al camp **Preu** , introduïu un número. Podeu configurar un preu de venda estàndard per a transaccions per hora o per a una categoria de projecte. També podeu configurar els preus de les vendes per número de treballador, número de projecte, categoria, data de la transacció o qualsevol combinació d'aquests valors. El preu de vendes real, que s'aplica quan un treballador introdueix una transacció al diari Hora, és el preu de vendes amb el nivell de detall més alt. Per exemple, si es configuren tant un preu de vendes general com un preu de vendes específic del treballador, el preu de vendes específic del treballador s'utilitza.  
11. Seleccioneu **Desa**.
12. Tanqueu la pàgina.
13. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de cost (despesa)**.
14. Seleccioneu **Crea**.
15. En el camp **Data d'efectivitat** , introduïu una data.
16. Al camp **Preu de cost** , introduïu un número. Es poden emplenar diversos camps, però aquest és el mínim necessari per desar el registre.  
17. Seleccioneu **Desa**.
18. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Configuració > Preus > Preu de vendes (despesa)**.
19. Seleccioneu **Crea**.
20. En el camp **Data d'efectivitat** , introduïu una data.
21. Seleccioneu una opció al camp **Vàlid durant**.
22. Al camp **Preu** , introduïu un número. El preu de vendes real, que s'aplica quan un treballador introdueix transaccions en un diari de despeses, és el preu de vendes amb el nivell de detall més alt. Per exemple, si es configuren tant un preu de vendes general com un d'específic del treballador, el preu de vendes específic del treballador s'utilitza.  
23. Seleccioneu **Desa**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]