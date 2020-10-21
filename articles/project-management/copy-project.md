---
title: Còpia d'un projecte
description: En aquest tema es proporciona informació sobre la còpia de projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907901"
---
# <a name="copy-a-project"></a>Còpia d'un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Amb el Dynamics 365 Project Operations, podeu crear ràpidament nous projectes mitjançant l'acció **Copia el projecte** al formulari **Projectes**. Per copiar un projecte, seleccioneu un projecte i, a continuació, seleccioneu **Copia**. L'acció copiarà:

- Les propietats del projecte
- L'estructura del desglossament del treball
- Membres de l'equip del projecte
- Estimacions del projecte
- Estimacions de despesa del projecte

## <a name="project-properties"></a>Propietats del projecte

Quan el projecte es copia, es copien els valors dels camps següents:

- Nom
- Descripció
- Client
- Plantilla de calendari
- Moneda
- Unitat de contractació
- Administrador de projectes
- Estat
- Estat general del projecte
- Comentaris
- Estimacions
- Data d’inici estimada
- Data de finalització
- Esforç (hores)
- Cost estimat de la mà d’obra
- Cost estimat de les despeses

## <a name="work-breakdown-structure"></a>Estructura del desglossament del treball

Quan es copia el projecte, es copia tota l'estructura del desglossament del treball carregada de recursos. Els recursos amb nom se substitueixen per recursos genèrics. Si els recursos amb nom no tenen les mateixes hores de feina que el recurs genèric, la planificació es tornarà a calcular i les duracions de les tasques poden canviar.

## <a name="project-team-members"></a>Membres de l'equip del projecte

Quan un equip del projecte es copia des del projecte d'origen, es copien els recursos genèrics. Les assignacions de recursos genèrics també es mantenen com estaven al projecte d'origen. Els recursos amb nom es convertiran en membres de l'equip genèric.

## <a name="estimates"></a>Estimacions

Quan el projecte es copia, les línies d'estimació de recursos i de despesa es copien des del projecte d'origen.