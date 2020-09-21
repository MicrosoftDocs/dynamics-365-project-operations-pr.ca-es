---
title: Per què no puc suprimir registres de l'entitat Valors reals?
description: Aquest tema proporciona informació sobre els motius pels quals no podeu suprimir registres de l'entitat de valors reals.
author: JPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.prod: Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: ff504c34-7337-474f-89e8-d8afdd1e0a98
ms.author: Jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5817940933c161dccac0fe549fabacbe57e7077a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749448"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="c1ffe-103">Per què no puc suprimir registres de l'entitat Valors reals?</span><span class="sxs-lookup"><span data-stu-id="c1ffe-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c1ffe-104">El Project Service Automation (PSA) no us permet suprimir els valors reals perquè serveixen com a origen de la veritat per a les transaccions que tenen implicacions financeres per a sistemes de nivells inferiors, com ara el llibre major.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="c1ffe-105">Si es poguessin suprimir els valors reals, la integritat de les transaccions d'informació financera podria qüestionar-se.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="c1ffe-106">Per establir una pista d'auditoria, els clients han d'utilitzar diaris per crear transaccions de compensació.</span><span class="sxs-lookup"><span data-stu-id="c1ffe-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

