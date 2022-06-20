---
title: Valors reals
description: En aquest article s'ofereix informació sobre com treballar amb reals a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924786"
---
# <a name="actuals"></a>Valors reals

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els valors reals representen el progrés financer revisat i aprovat i la planificació en un projecte. Es creen quan s'aproven les entrades de temps, despesa i ús de material, entrades de diari i factures.

> [!IMPORTANT]
> Els reals no s'han d'editar ni suprimir del sistema. En cas contrari, la integritat financera i qualsevol integració amb altres sistemes financers i comptables es podrien veure afectades negativament. Microsoft Dynamics 365 Project Operations us permet utilitzar la inversió i la substitució de reals per editar els reals en diversos punts del cicle de vida del procés de negoci dels vostres projectes.

## <a name="recording-actuals-based-on-project-events"></a>Enregistrament de valors reals a partir d'esdeveniments de projecte

Project Operations registra les transaccions financeres que es produeixen durant el cicle de vida del compromís del projecte com a reals. La creació de reals en diversos esdeveniments del cicle de vida varia, depenent de si el compromís del projecte utilitza el model de facturació de temps i materials o el model de facturació de preus fixos, i si es troba en fase de prevenda o és un projecte intern.

Els articles següents expliquen l'impacte a la taula Des de fets en diversos esdeveniments per a diferents variacions:

- [Impacte real en un compromís de temps i materials](ActualsonTM.md)
- [Impacte real en un compromís de preu fix](ActualonFP.md)
- [Impacte real durant la fase de prevenda d'un compromís](ActualonPreSales.md)
- [Impacte real d'un projecte intern](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
