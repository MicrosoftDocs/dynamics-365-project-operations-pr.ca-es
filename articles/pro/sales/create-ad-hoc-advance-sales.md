---
title: Creació d'un avançament ad hoc en un contracte (bàsic)
description: Aquest tema proporciona informació sobre la creació d'un avançament en un contracte segons sigui necessari.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181350"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Creació d'un avançament ad hoc en un contracte (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

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