---
title: Còpia d'un projecte
description: En aquest tema es proporciona informació sobre la còpia de projectes al Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131781"
---
# <a name="copy-a-project"></a>Còpia d'un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Amb el Dynamics 365 Project Operations, podeu crear ràpidament nous projectes seleccionant **Copia el projecte** al formulari **Projectes**. Per copiar un projecte, obriu el projecte que voleu copiar i seleccioneu **Copia el projecte**. L'acció copiarà:

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

Per obtenir informació sobre com accedir mitjançant programació a Copia el projecte, vegeu [Desenvolupar plantilles de projecte amb Copia el projecte](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]