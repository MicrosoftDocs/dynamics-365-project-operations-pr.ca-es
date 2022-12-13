---
title: Crear un avançament ad hoc d'un contracte de projecte
description: Aquest article proporciona informació sobre la creació d'un avançament en un contracte segons sigui necessari.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 62e41e5faeb5e40143e26e2cdf48c1279941a6b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824810"
---
# <a name="create-an-ad-hoc-advance-on-a-project-contract"></a>Crear un avançament ad hoc d'un contracte de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Microsoft Dynamics 365 Project Operations admet escenaris de facturació que impliquin prepagaments i avançaments. El procés d'ús d'**Avançaments** al **Project Operations** és similar als contractes de **Bestreta**. 

Completeu els passos següents per facturar al client un avançament.

1. Aneu a la pàgina **Contracte de projecte** i, a continuació, seleccioneu la pestanya **Avançaments i bestretes**.
2. A la subquadrícula que enumera tots els avançaments i prepagaments registrats anteriorment, seleccioneu **+ Nova bestreta de contracte de projecte**. 

    El formulari **Creació ràpida** s'obre per registrar un prepagament o avançament.
    
3. A la taula següent s'enumeren els camps per registrar un avançament i les consideracions que cal tenir en compte quan en creeu de nous:

    | Camp | Descripció | Impacte descendent |
    | --- | --- | --- |
    | **Client de contracte de projecte** | En aquest camp s'indica a quin client del contracte es facturarà aquest avançament. | Si teniu diversos clients en el contracte i voleu facturar a cadascun un import específic de bestreta o avançament, creeu un avançament per a cada client individualment. |
    | **Descripció** | Descripció de la finalitat o el calendari de l'avançament per ajudar a identificar aquest avançament. | Aquesta descripció es mostra a la línia de facturació d'aquest avançament. |
    | **Import** | Import del prepagament o avançament. | Aquest import es mostra a la línia de facturació d'aquest avançament. |
    | **Data de la factura** | Data en què es factura aquest avançament al client. | És la data per al procés de creació de factures automatitzada per crear una línia de factura per a aquest avançament. |
    | **Estat de la factura** | Es tracta d'una opció que indica si aquest avançament s'afegeix a un esborrany de factura per a aquest client. Els valors possibles són:</br>- **No preparat per a la facturació**</br>- **Preparat per a la factura** | Quan un avançament o prepagament es marca com a **A punt per facturar**, s'afegeix com a línia de temps en un esborrany de factura. Només es pot utilitzar un avançament completament facturat per conciliar les despeses del projecte per al següent període de facturació. |

4. Seleccioneu **Desa i tanca** al quadre de diàleg creació ràpida per registrar l'avançament o prepagament.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
