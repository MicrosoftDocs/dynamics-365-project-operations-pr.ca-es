---
title: Per què no puc suprimir registres de l'entitat Valors reals?
description: Aquest tema proporciona informació sobre els motius pels quals no podeu suprimir registres de l'entitat de valors reals.
author: JPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f47e7ccd46642dc6129fbb3beac3c9490160d046
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072338"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="098ef-103">Per què no puc suprimir registres de l'entitat Valors reals?</span><span class="sxs-lookup"><span data-stu-id="098ef-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="098ef-104">El Project Service Automation (PSA) no us permet suprimir els valors reals perquè serveixen com a origen de la veritat per a les transaccions que tenen implicacions financeres per a sistemes de nivells inferiors, com ara el llibre major.</span><span class="sxs-lookup"><span data-stu-id="098ef-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="098ef-105">Si es poguessin suprimir els valors reals, la integritat de les transaccions d'informació financera podria qüestionar-se.</span><span class="sxs-lookup"><span data-stu-id="098ef-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="098ef-106">Per establir una pista d'auditoria, els clients han d'utilitzar diaris per crear transaccions de compensació.</span><span class="sxs-lookup"><span data-stu-id="098ef-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

