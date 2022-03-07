---
title: Per què no puc suprimir registres de l'entitat Valors reals?
description: Aquest tema proporciona informació sobre els motius pels quals no podeu suprimir registres de l'entitat de valors reals.
author: JPBurrows
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
ms.openlocfilehash: d60a3586fd1f0f688bcd2626d039ebc1aa6b0925c90d676f0e716400d8e8d6dd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002859"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Per què no puc suprimir registres de l'entitat Valors reals?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

El Project Service Automation (PSA) no us permet suprimir els valors reals perquè serveixen com a origen de la veritat per a les transaccions que tenen implicacions financeres per a sistemes de nivells inferiors, com ara el llibre major. Si es poguessin suprimir els valors reals, la integritat de les transaccions d'informació financera podria qüestionar-se. Per establir una pista d'auditoria, els clients han d'utilitzar diaris per crear transaccions de compensació.



[!INCLUDE[footer-include](../includes/footer-banner.md)]