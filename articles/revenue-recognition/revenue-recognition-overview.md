---
title: Informació general del reconeixement d'ingressos
description: En aquest tema es proporciona informació sobre el reconeixement d'ingressos a Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531362"
---
# <a name="revenue-recognition-overview"></a>Informació general del reconeixement d'ingressos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Al Dynamics 365 Project Operations, els principis de reconeixement d'ingressos varien en funció del mètode de facturació seleccionat per a un projecte o una part del projecte. En aquest tema es proporciona informació sobre el reconeixement d'ingressos a Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transaccions comptabilitzades amb el mètode de facturació de temps i material

- El reconeixement de costos i ingressos està connectat. El cost de la transacció i les vendes no facturades es comptabilitzen a través del [diari d'integració de Project Operations](../project-accounting/project-operations-integration-journal.md).
- El perfil de costos i ingressos del projecte determina si les transaccions de vendes no facturades es comptabilitzen al llibre general. Si se selecciona **Meritar beneficis**, el sistema utilitza el **Valor de venda WIP** i els comptes de **Valor de vendes d'ingressos meritat** durant la comptabilització. A continuació us mostrem un exemple d'aquest mètode.  

  | Tipus de transacció | Dèbit/Crèdit | Import |
  | --- | --- | --- |
  | Valor de vendes WIP | Dèbit | 100 |
  | Valor de vendes d'ingressos acumulats | Crèdit | 100 |

- Els ingressos es reconeixen durant la facturació. El sistema utilitza el compte **Ingressos facturats** durant la comptabilització. A continuació us mostrem un exemple d'aquest mètode.  

  | Tipus de transacció | Dèbit/Crèdit | Import |
  | --- | --- | --- |
  | Saldo de client | Dèbit | 120 |
  | Impost sobre les vendes a pagar | Crèdit | 20 |
  | Ingressos facturats | Crèdit | 100 |

- Si els ingressos s'han acumulat en comptabilitzar les vendes no facturades, el sistema revertirà els ingressos meritats a facturació.

  | Tipus de transacció | Dèbit/Crèdit | Import |
  | --- | --- | --- |
  | Valor de vendes WIP | Crèdit | 100 |
  | Valor de vendes d'ingressos acumulats | Dèbit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transaccions comptabilitzades amb el mètode de facturació de preu fix

- El reconeixement de costos i ingressos està separat. El cost de la transacció es comptabilitza a través del [diari d'integració de Project Operations](../project-accounting/project-operations-integration-journal.md). Les transaccions de vendes no facturades no es creen.
- Els ingressos es poden reconèixer durant la facturació si el perfil de costos i ingressos del projecte té **Principi utilitzat per als càlculs de compleció de projectes** establert en **Sense WIP**. Utilitzeu només aquest mètode per a projectes senzills a curt termini.
- Els ingressos es poden reconèixer mitjançant estimacions d'ingressos de preu fix, amb el **Contracte completat** o el mètode de **Reconeixement d'ingressos de finalització en percentatge**.

## <a name="additional-resources"></a>Recursos addicionals
[Article Configuració de la comptabilitat per a projectes facturables](../project-accounting/configure-accounting-billable-projects.md)

[Projectes d'estimació d'ingressos de preu fix](rev-rec-percentage-completion-method.md)

[Administració de les estimacions d'ingressos](rev-rec-completed-contract-method.md)

[Mètodes de càlcul de costos per a la finalització](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]