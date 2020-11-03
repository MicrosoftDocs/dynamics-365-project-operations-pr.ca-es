---
title: Creació d'una factura proforma manual
description: Aquest tema proporciona informació sobre la creació d'una factura proforma manual al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "4072441"
---
# <a name="creating-a-manual-proforma-invoice"></a>Creació d'una factura proforma manual

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Al Dynamics 365 Project Operations, les factures proforma es poden crear manualment segons sigui necessari. Podeu crear manualment una factura proforma des de la pàgina de llista **Contractes del projecte** o la pàgina de detalls **Contracte del projecte**.

##  <a name="project-contracts-list-page"></a>Pàgina de llista Contractes del projecte

Des de la pàgina de llista **Contractes del projecte** , seleccioneu un o més contractes de projecte i creeu factures per a tots els registres seleccionats.

El sistema comprova quin dels contractes de projecte seleccionats té un registre **A punt per facturar** amb data abans d'avui. A partir d'aquests contractes, el sistema crea esborranys de factures proforma. Si un contracte de projecte té diversos clients, pot haver-hi una factura creada per client i diverses factures per contracte de projecte.

Totes les factures de projecte creades estan disponibles a la pàgina **Factura** a la secció **Facturació** de l'àrea **Vendes**.

## <a name="project-contract-details-page"></a>Pàgina de detalls Contracte del projecte

També es pot crear una factura proforma des de la pàgina de detalls **Contracte del projecte** , que crea la factura d'aquest contracte de projecte específic. El sistema verifica que el contracte del projecte té un registre **A punt per facturar** amb data abans d'avui. A partir d'aquests contractes, el sistema crea esborranys de factures proforma en funció del nombre de clients en cada línia de contracte.

Quan es crea una única factura proforma, s'obre la pàgina **Factura**. Si hi ha diverses factures creades per aquest contracte de projecte, llavors la pàgina de llista **Factures** s'obre per mostrar totes les factures creades.
