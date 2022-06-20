---
title: Còpia d'un projecte
description: En aquest article s'ofereix informació sobre la còpia de projectes a Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925752"
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
- Llistes de comprovació del projecte
- Cubells del projecte

## <a name="project-properties"></a>Les propietats del projecte

Quan es copia el projecte, es copien els valors dels camps següents.

| Camp | Operacions de projecte Materials no emmagatzemats | Operacions del projecte Lite | Projecte per a la web |
|-------|------------------------------------------|-------------------------|---------------------|
| Nom | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Descripció | :heavy_check_mark: | :heavy_check_mark: | |
| Client | :heavy_check_mark: | :heavy_check_mark: | |
| Plantilla de calendari | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Moneda | :heavy_check_mark: | :heavy_check_mark: | |
| Unitat de contractació | :heavy_check_mark: | :heavy_check_mark: | |
| Empresa propietària | :heavy_check_mark: | | |
| Administrador de projectes | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Estat d'execució | :heavy_check_mark: | :heavy_check_mark: | |
| Estat general del projecte | :heavy_check_mark: | :heavy_check_mark: | |
| Comentaris | :heavy_check_mark: | :heavy_check_mark: | |
| Estimacions | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data d’inici estimada</p><p><strong>Nota:</strong> Aquest camp especifica la data en què es crea el projecte a partir de la còpia. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Data de finalització estimada</p><p><strong>Nota:</strong> La data d'aquest camp s'ajusta en funció de la data d'inici del nou projecte que s'ha fet a partir de la còpia.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Esforç (hores) | :heavy_check_mark: | :heavy_check_mark: | |
| Cost estimat de la mà d’obra | :heavy_check_mark: | :heavy_check_mark: | |
| Cost estimat de les despeses | :heavy_check_mark: | :heavy_check_mark: | |
| Cost estimat del material | | :heavy_check_mark: | |

> [!NOTE]
> Copiar un projecte és una operació de llarga execució. També es copien els registres de projecte, els seus atributs rellevants i moltes entitats relacionades. A causa del caràcter de llarga execució de l'operació, un cop iniciada la còpia, la pàgina del projecte de destinació queda blocada per editar-la fins que l'operació de còpia s'ha completat.

## <a name="work-breakdown-structure"></a>Estructura del desglossament del treball

Quan es copia el projecte, es copia tota l'estructura del desglossament del treball carregada de recursos. Els recursos amb nom se substitueixen per recursos genèrics. Si els recursos amb nom no tenen les mateixes hores de treball que el recurs genèric, la planificació es tornarà a calcular i la durada de les tasques pot canviar.

## <a name="project-team-members"></a>Membres de l'equip del projecte

Quan un equip del projecte es copia des del projecte d'origen, es copien els recursos genèrics. Les assignacions de recursos genèrics també es mantenen com estaven al projecte d'origen. Els recursos amb nom es convertiran en membres de l'equip genèric.

> [!NOTE]
> Els membres de l'equip i les tasques no es copien al Project for the Web.

## <a name="estimates"></a>Estimacions

Quan es copia el projecte, les línies de càlcul de recursos, despeses i materials es copien del projecte d'origen. 

Per obtenir informació sobre com accedir mitjançant programació a Copia el projecte, vegeu [Desenvolupar plantilles de projecte amb Copia el projecte](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Ofertes i contractes

Les ofertes i els contractes no estan vinculats al projecte de destinació.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
