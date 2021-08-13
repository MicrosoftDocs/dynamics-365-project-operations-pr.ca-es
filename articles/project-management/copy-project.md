---
title: Còpia d'un projecte
description: Aquest tema proporciona informació sobre la còpia de projectes al Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007179"
---
# <a name="copy-a-project"></a>Còpia d'un projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Amb el Dynamics 365 Project Operations, podeu crear projectes nous ràpidament seleccionant **Copia el projecte** al formulari **Projectes**. Per copiar un projecte, obriu el projecte que voleu copiar i seleccioneu **Copia el projecte**. L'acció copiarà el següent:

- Les propietats del projecte 
- Estructura del desglossament del treball
- Membres de l'equip del projecte
- Estimacions del projecte
- Estimacions de despesa del projecte
- Estimacions de materials del projecte

## <a name="project-properties"></a>Les propietats del projecte

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
- Data d'inici prevista: aquesta és la data de creació del projecte a partir de la còpia.
- Data de finalització prevista: aquesta data s'ajusta segons la data d'inici del nou projecte que s'ha fet a partir de la còpia.
- Esforç (hores)
- Cost estimat de la mà d’obra
- Cost estimat de les despeses
- Cost estimat del material

> [!NOTE]
> Copiar un projecte és una operació de llarga execució. També es copien els registres de projecte, els seus atributs rellevants i moltes entitats relacionades. A causa del caràcter de llarga execució de l'operació, un cop iniciada la còpia, la pàgina del projecte de destinació queda blocada per editar-la fins que l'operació de còpia s'ha completat.

## <a name="work-breakdown-structure"></a>Estructura del desglossament del treball

Quan es copia el projecte, es copia tota l'estructura del desglossament del treball carregada de recursos. Els recursos amb nom se substitueixen per recursos genèrics. Si els recursos amb nom no tenen les mateixes hores de feina que el recurs genèric, la planificació es tornarà a calcular i les duracions de les tasques poden canviar.

## <a name="project-team-members"></a>Membres de l'equip del projecte

Quan un equip del projecte es copia des del projecte d'origen, es copien els recursos genèrics. Les assignacions de recursos genèrics també es mantenen com estaven al projecte d'origen. Els recursos amb nom es convertiran en membres de l'equip genèric.

## <a name="estimates"></a>Estimacions

Quan es copia el projecte, les línies de càlcul de recursos, despeses i materials es copien del projecte d'origen. 

Per obtenir informació sobre com accedir mitjançant programació a Copia el projecte, vegeu [Desenvolupar plantilles de projecte amb Copia el projecte](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
