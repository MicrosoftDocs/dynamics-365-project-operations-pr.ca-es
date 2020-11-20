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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127146"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a>Per què no puc suprimir registres de l'entitat Valors reals?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

El Project Service Automation (PSA) no us permet suprimir els valors reals perquè serveixen com a origen de la veritat per a les transaccions que tenen implicacions financeres per a sistemes de nivells inferiors, com ara el llibre major. Si es poguessin suprimir els valors reals, la integritat de les transaccions d'informació financera podria qüestionar-se. Per establir una pista d'auditoria, els clients han d'utilitzar diaris per crear transaccions de compensació.

