---
title: Configurar els costos estàndard per al treball i les despeses
description: En aquest article s'explica com configurar els costos estàndard per a la mà d'obra i les despeses d'un projecte.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a51eee8d2eb960b6f24b6511dab7b7a27303dddb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919496"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurar els costos estàndard per al treball i les despeses

[!include [banner](../../includes/banner.md)]

En aquest article s'explica com configurar els costos estàndard per a la mà d'obra i les despeses d'un projecte. Aquesta tasca utilitza el conjunt de dades d'USSI.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]