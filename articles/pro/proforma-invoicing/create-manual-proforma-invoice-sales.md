---
title: Creació d'una factura proforma manual (bàsic)
description: Aquest tema proporciona informació sobre la creació d'una factura proforma manual al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274176"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Creació d'una factura proforma manual (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Al Dynamics 365 Project Operations, les factures de proforma es poden crear manualment segons calgui. Podeu crear manualment una factura proforma des de la pàgina de llista **Contractes del projecte** o la pàgina de detalls **Contracte del projecte**.

##  <a name="project-contracts-list-page"></a>Pàgina de llista Contractes del projecte

Des de la pàgina de llista **Contractes del projecte**, seleccioneu un o més contractes de projecte i creeu factures per a tots els registres seleccionats.

El sistema comprova quin dels contractes de projecte seleccionats té un registre **A punt per facturar** amb data abans d'avui. A partir d'aquests contractes, el sistema crea esborranys de factures proforma. Si un contracte de projecte té diversos clients, pot haver-hi una factura creada per client i diverses factures per contracte de projecte.

Totes les factures de projecte creades estan disponibles a la pàgina **Factura** a la secció **Facturació** de l'àrea **Vendes**.

## <a name="project-contract-details-page"></a>Pàgina de detalls Contracte del projecte

També es pot crear una factura de proforma des de la pàgina de detalls **Contracte del projecte**. El sistema verifica que el contracte de projecte té un registre **A punt per facturar** amb data abans d'avui. A partir d'aquests contractes, el sistema crea esborranys de factures proforma en funció del nombre de clients en cada línia de contracte.

Quan es crea una única factura proforma, s'obre la pàgina **Factura**. Si es creen diverses factures per al contracte del projecte, s'obrirà la pàgina de llistes **Factures** per mostrar totes les factures creades.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]