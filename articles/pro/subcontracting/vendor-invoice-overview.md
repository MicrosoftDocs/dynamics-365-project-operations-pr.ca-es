---
title: 'Facturació del proveïdor: concepte i creació'
description: En aquest article es descriu el concepte de factures de proveïdor, escenaris d'ús i com crear factures de proveïdor a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911446"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturació del proveïdor: concepte i creació

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La facturació del proveïdor a Microsoft Dynamics 365 Project Operations es pot utilitzar per registrar els costos dels lliuraments de serveis i / o materials d'un projecte per part dels proveïdors.

Quan els serveis i / o materials són subcontractats a un proveïdor, una subcontracta representa l'acord contractual amb aquest proveïdor. A mesura que el proveïdor lliura els serveis, o els materials es reben i s'utilitzen en tasques del projecte, els costos es registren en el projecte. Periòdicament, el venedor envia factures verificades i coincidents amb els costos que es registren en el projecte. Un cop finalitzat el procés de verificació, la factura del proveïdor es confirma i es publica per al pagament.

## <a name="scenarios-for-use"></a>Escenaris per utilitzar

Les factures del proveïdor a les operacions del projecte es poden utilitzar per suportar dos escenaris diferents.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Els clients utilitzen les experiències completes de subcontractació

Les experiències de factures del proveïdor proporcionen una manera de verificar i fer coincidir les entrades de temps, l'ús de material i les entrades de despeses que fan referència als components subcontractats amb les línies de factura del proveïdor. Aquest procés es pot utilitzar per verificar la precisió de les línies de factura del proveïdor. Un cop completat el procés de verificació i confirmat la factura del proveïdor, l'aplicació revertirà els reals que es van registrar mitjançant registres de temps, despeses i ús de materials aprovats i crearà nous costos reals mitjançant les línies de factura del proveïdor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Els clients no utilitzen les experiències completes de subcontractació, però volen tenir una visió unificada dels costos dels projectes en operacions de projectes

Si feu un seguiment del procés de subcontractació en un sistema de tercers, podeu registrar els costos d'aquest sistema de tercers a Les operacions del projecte creant factures de proveïdor que no fan referència a subcontractacions. D'aquesta manera, els gestors de projectes poden tenir una visió única i unificada de tots els costos d'un projecte determinat.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creació de factures de proveïdors en operacions de projectes

Les factures del proveïdor es poden crear de dues maneres:

- Des de la pàgina de la llista de factures del proveïdor o des de la pàgina detalls d'una sola factura de proveïdor
- Des de la pàgina de llista de subcontractes o la pàgina de detalls per a una única subcontractació

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creació des de la pàgina o la pàgina de detalls de la llista de factures del proveïdor

1. Aneu a **Factures de proveïdors de** \> **compra**.
2. A la pàgina de la llista de factures del proveïdor o a la pàgina detalls d'una sola factura de proveïdor, seleccioneu **Crea** per crear una factura de proveïdor nova.

Les factures de proveïdor que es creen d'aquesta manera també poden fer referència a una subcontracta.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creació des de la pàgina de la llista de subcontractes o la pàgina de detalls

1. Anar a **subcontractes de compra** \> **·**.
2. Seleccioneu una o més subcontractacions.
3. A la pàgina de la llista de subcontractacions o a la pàgina detalls d'una sola subcontracta, seleccioneu **Crea una factura** de proveïdor per crear una factura de proveïdor nova.

Es crea una factura de proveïdor nova a l'estat **Esborrany** per a cada subcontractació que hàgiu seleccionat.

Les factures de proveïdor que creeu d'aquesta manera sempre fan referència a la subcontractació de la capçalera de la factura del proveïdor. Cada línia de la subcontracta que tingui un mètode de facturació de temps i material farà que es creï una línia a la factura del proveïdor. Cada línia de la subcontracta que tingui un mètode de facturació de preu fix farà que es creï una línia a la factura del proveïdor per a cada fita de la línia de subcontractació que tingui un estat de **Llest per facturar**.

Els camps següents i els registres relacionats es copiaran de la subcontracta a la capçalera de la factura del proveïdor:

- Venedor.
- Les llistes de preus relacionades es copiaran a la factura del proveïdor com a llistes de preus.
- Moneda.
- Unitat de contractació.
- Condicions de pagament.

Per a les línies de subcontractació de temps i material, es copiaran els camps i registres relacionats següents de la línia de subcontractació a la línia de factura del proveïdor:

- Referències de línies de subcontractació i subcontractació
- Classe de la transacció
- Funció
- Categoria de la transacció
- Camps de producte
- Project
- Tasca
- Recurs que es pot reservar

Per a les línies de subcontractació de preus fixos, es copiaran els camps següents de la línia de subcontractació i la fita de la línia de subcontractació a la línia de factura del proveïdor:

- Referències de línies de subcontractació i subcontractació.
- Classe de transacció. Per defecte, el valor serà **Milestone**.
- El nom i l'import de la fita es copiaran de la fita de la línia de subcontractació relacionada.
- L'usuari podrà seleccionar un projecte i una tasca a la línia de factura del proveïdor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
