---
title: Per què no puc suprimir registres de l'entitat Valors reals?
description: Aquest tema proporciona informació sobre els motius pels quals no podeu suprimir registres de l'entitat de valors reals.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 36cd241c7c7a2ff6ae018c94d691bc95d1f0c912
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148946"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="aa2bc-103">Per què no puc suprimir registres de l'entitat Valors reals?</span><span class="sxs-lookup"><span data-stu-id="aa2bc-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aa2bc-104">El Project Service Automation (PSA) no us permet suprimir els valors reals perquè serveixen com a origen de la veritat per a les transaccions que tenen implicacions financeres per a sistemes de nivells inferiors, com ara el llibre major.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="aa2bc-105">Si es poguessin suprimir els valors reals, la integritat de les transaccions d'informació financera podria qüestionar-se.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="aa2bc-106">Per establir una pista d'auditoria, els clients han d'utilitzar diaris per crear transaccions de compensació.</span><span class="sxs-lookup"><span data-stu-id="aa2bc-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

