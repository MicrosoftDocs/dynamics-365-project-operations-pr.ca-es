---
title: Valors reals
description: En aquest article es proporciona informació sobre com treballar amb valors reals al Microsoft Dynamics 365 Project Operations.
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

Els valors reals representen el progrés financer revisat i aprovat i la planificació en un projecte. Es creen quan s'aproven entrades de temps, despesa, ús de materials i llibre diari i factures.

> [!IMPORTANT]
> Els valors reals no s'han d'editar ni suprimir des del sistema. Altrament, la integritat financera i la integració amb altres sistemes financers i de comptabilitat podrien veure's afectades negativament. El Microsoft Dynamics 365 Project Operations us permet revertir i substituir valors reals per editar valors reals en diversos punts del cicle de vida del procés de negoci dels vostres projectes.

## <a name="recording-actuals-based-on-project-events"></a>Enregistrament de valors reals a partir d'esdeveniments de projecte

El Project Operations registra les transaccions financeres que es produeixen durant el cicle de vida de compromís de projecte com a valors reals. La creació de valors reals en diverses incidències del cicle de vida varia en funció de si el compromís de projecte utilitza el model de facturació de temps i materials o el model de facturació de preu fix, i de si es troba en la fase de prevendes o és un projecte intern.

Als articles següents s'explica l'impacte sobre la taula Valors reals en diverses incidències per a diferents variacions:

- [Impacte real en una interacció amb el temps i els materials](ActualsonTM.md)
- [Impacte real en una interacció amb els preus fixos](ActualonFP.md)
- [Impacte real durant la fase de pre-vendes d'una interacció](ActualonPreSales.md)
- [Impacte real per a un projecte intern](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
