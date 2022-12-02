---
title: 'Facturació del proveïdor: concepte i creació'
description: En aquest article es descriu el concepte de factures de proveïdor, els escenaris d'ús i la manera com es creen factures de proveïdor al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261922"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturació del proveïdor: concepte i creació

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La facturació del proveïdor al Microsoft Dynamics 365 Project Operations es pot utilitzar per registrar els costos dels lliuraments de serveis i/o materials d'un projecte per part de proveïdors.

Quan els serveis i/o els materials se subcontracten a un proveïdor, un subcontracte representa l'acord contractual amb aquest proveïdor. Quan el proveïdor proporciona els serveis, o els materials es reben i s'utilitzen en les tasques del projecte, els costos es registren en el projecte. Periòdicament, el proveïdor envia factures que es verifiquen i es fan coincidir amb els costos registrats al projecte. Un cop completat el procés de verificació, la factura del proveïdor es confirma i s'allibera per al pagament.

## <a name="scenarios-for-use"></a>Escenaris d'ús

Les factures de proveïdor al Project Operations es poden utilitzar per donar suport a dos escenaris diferents.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Els clients utilitzen totes les experiències de subcontractació

Les experiències de factura del proveïdor proporcionen una manera de verificar i aparellar les entrades de temps, ús de materials i despesa que fan referència a components subcontractats amb les línies de factura del proveïdor. Aquest procés es pot utilitzar per verificar l'exactitud de les línies de factura del proveïdor. Un cop completat el procés de verificació i confirmada la factura del proveïdor, l'aplicació invertirà els valors reals registrats amb registres de temps, despesa i ús de materials aprovats i crearà noves dades de cost mitjançant línies de factura del proveïdor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Els clients no utilitzen les totes les experiències de subcontractació, però volen tenir una visualització unificada dels costos dels projectes al Project Operations

Si feu el seguiment del procés del subcontracte en un sistema de tercers, podeu registrar els costos d'aquest sistema de tercers al Project Operations creant factures de proveïdor que no facin referència a subcontractes. D'aquesta manera, els administradors de projecte poden tenir una visualització unificada de tots els costos d'un projecte determinat.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creació de factures de proveïdor al Project Operations

Les factures de proveïdor es poden crear de dues maneres:

- Des de la pàgina de llista de factures del proveïdor o la pàgina de detalls d'una factura de proveïdor
- Des de la pàgina de llista de subcontracte o la pàgina de detalls d'un sol subcontracte

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creació des de la pàgina de llista de factures del proveïdor o la pàgina de detalls

1. Aneu a **Compres** \> **Factures de proveïdor**.
2. A la pàgina de la llista de factures del proveïdor o la pàgina de detalls d'una factura de proveïdor, seleccioneu **Nova** per crear una factura de proveïdor nova.

Les factures de proveïdor creades d'aquesta manera també poden fer referència a un subcontracte.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creació des de la pàgina de llista de subcontracte o la pàgina de detalls

1. Aneu a **Compres** \> **Subcontractes**.
2. Seleccioneu un o diversos subcontractes.
3. A la pàgina de la llista de subcontractes o la pàgina de detalls d'un subcontracte, seleccioneu **Crea una factura de proveïdor** per crear una factura de proveïdor nova.

Es crea una factura de proveïdor nova en estat d'**Esborrany** per a cada subcontracte que heu seleccionat.

Les factures de proveïdor que creeu d'aquesta manera sempre fan referència al subcontracte de la capçalera de la factura del proveïdor. Cada línia del subcontracte que té un mètode de facturació de Temps i materials farà que es creï una línia a la factura del proveïdor. Cada línia del subcontracte que té un mètode de facturació de Preu fix farà que es creï una línia a la factura del proveïdor per a cada fita de línia de subcontracte que tingui l'estat de **Preparat per a la factura**.

Els camps següents i els registres relacionats es copiaran des del subcontracte a la capçalera de la factura del proveïdor:

- Proveïdor.
- Les llistes de preus relacionades es copiaran a la factura del proveïdor com a llistes de preus.
- Moneda.
- Unitat de contractació.
- Condicions de pagament.

Per a les línies de subcontracte de temps i materials, els camps següents i els registres relacionats es copiaran des de la línia de subcontracte a la línia de factura del proveïdor:

- Referències de subcontracte i línia de subcontracte
- Classe de la transacció
- Funció
- Categoria de la transacció
- Camps de producte
- Project
- Tasca
- Recurs que es pot reservar

Per a les línies de subcontracte de Preu fix, els camps següents es copiaran des de la línia de subcontracte i la fita de línia de subcontracte a la línia de factura del proveïdor:

- Referències de subcontracte i línia de subcontracte.
- Classe de la transacció. Per defecte, el valor serà **Fita**.
- El nom de la fita i l'import es copiaran des de la fita de línia de subcontracte relacionada.
- L'usuari podrà seleccionar un projecte i una tasca a la línia de factura del proveïdor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
