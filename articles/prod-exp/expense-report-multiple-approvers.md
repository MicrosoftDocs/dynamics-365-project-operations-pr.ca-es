---
title: Diversos aprovadors en un informe de despeses
description: Aquest tema proporciona informació sobre els informes de despeses que requereixen l'aprovació de diverses persones.
author: saraschi2
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c745dda957fab5acc464b9d1c774fcdc783cde40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005239"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Diversos aprovadors en un informe de despeses

Segons les normes d'aprovació de despeses de la vostra organització, més d'una persona podria haver d'aprovar un informe de despeses que presenta un empleat. En configurar el procés de flux de treball per a l'aprovació de l'informe de despeses, podeu afegir elements de flux de treball que incloguin tasques o passos per a un o diversos aprovadors de l'informe de despeses. Per exemple, és possible que necessiteu que tots els informes de despeses els aprovin primer el cap del treballador que ha enviat l'informe i després el coordinador de compte a pagar.

Si decidiu que voleu que calguin diversos aprovadors d'informes de despeses, podeu afegir els elements del flux de treball d'una de les maneres següents:

- Afegiu un element d'aprovació que tingui un pas. Per exemple, pot ser que el pas requereixi que s'assigni un informe de despeses a un grup d'usuaris i que l'aprovin un 50 per cent dels membres del grup d'usuaris.
- Afegiu un element d'aprovació que tingui diversos passos. Per exemple, pot ser que l'element d'aprovació tingui els passos següents:

    1. El cap de l'empleat que ha enviat l'informe de despeses l'aprova.
    2. L'empleat de compte a pagar verifica els rebuts i els elements de l'informe de despeses.
    3. El propietari del pressupost aprova l'informe de despeses.

- Afegiu diversos elements d'aprovació, cadascun dels quals tingui un pas. Per exemple, pot ser que afegiu un element d'aprovació independent per a cadascun dels passos següents:

    1. El cap de l'empleat aprova l'informe de despeses.
    2. El propietari del pressupost aprova l'informe de despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]