---
title: 'Facturació del proveïdor: concepte i creació'
description: En aquest article es descriu el concepte de factures de proveïdors, els escenaris d'ús i com crear factures de proveïdors a Microsoft Dynamics 365 Project Operations.
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

La facturació de proveïdors a Microsoft Dynamics 365 Project Operations es pot utilitzar per registrar els costos derivats d'enviaments de serveis i/o materials en un projecte per part dels proveïdors.

Quan els serveis i/o materials són subcontractats a un venedor, un subcontractista representa l'acord contractual amb aquest venedor. A mesura que el proveïdor lliura els serveis o els materials es reben i s'utilitzen en les tasques del projecte, els costos es registren al projecte. Periòdicament, el proveïdor envia factures verificades i coincidents amb els costos que es registren al projecte. Un cop finalitzat el procés de verificació, la factura del proveïdor es confirma i es publica per al pagament.

## <a name="scenarios-for-use"></a>Escenaris d'ús

Les factures de proveïdors del Project Operations es poden utilitzar per admetre dos escenaris diferents.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Els clients utilitzen les experiències completes de subcontractació

Les experiències de factures dels proveïdors proporcionen una manera de verificar i fer coincidir les entrades de temps, l'ús de material i les entrades de despeses que fan referència als components subcontractats amb les línies de factures dels proveïdors. Aquest procés es pot utilitzar per verificar l'exactitud de les línies de factura del proveïdor. Un cop finalitzat el procés de verificació i confirmada la factura del proveïdor, l'aplicació revertirà els reals registrats pels registres de temps, despeses i ús de material aprovats i crearà nous reals de costos mitjançant les línies de factures del proveïdor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Els clients no utilitzen les experiències completes de subcontractació, però volen tenir una visió unificada dels costos dels projectes en operacions de projecte

Si feu un seguiment del procés de subcontractació en un sistema de tercers, podeu registrar els costos d'aquest sistema de tercers a Project Operations creant factures de proveïdors que no facin referència a subcontractes. D'aquesta manera, els vostres gestors de projectes poden tenir una visió única i unificada de tots els costos d'un projecte determinat.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Creació de factures de proveïdors en Project Operations

Les factures dels proveïdors es poden crear de dues maneres:

- Des de la pàgina de llista de factures del proveïdor o la pàgina de detalls d'una factura d'un sol proveïdor
- Des de la pàgina de llistat de subcontractes o la pàgina de dades d'un únic subcontractista

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Creació des de la pàgina o detalls de la llista de factures del proveïdor

1. Aneu a **Factures de proveïdors de** \> **compres**.
2. A la pàgina llista de factures de proveïdor o a la pàgina detalls d'una factura d'un sol proveïdor, seleccioneu **Crea** per crear una factura de proveïdor nova.

Les factures dels venedors que es creen d'aquesta manera també poden fer referència a un subcontractista.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Creació des de la pàgina de llista de subcontractes o pàgina de detalls

1. Aneu a **Subcontractes** de \>**compres**.
2. Seleccioneu una o més subcontractes.
3. A la pàgina de llista de subcontractistes o a la pàgina de detalls d'un únic subcontractista, seleccioneu **Crea una factura** de proveïdor per crear una factura de proveïdor nova.

Es crea una nova factura de proveïdor en **estat Esborrany** per a cada subcontracta que heu seleccionat.

Les factures de proveïdors que creeu d'aquesta manera sempre fan referència al subcontractista a la capçalera de la factura del proveïdor. Cada línia de la subcontractació que tingui un mètode de facturació de temps i material farà que es creï una línia a la factura del proveïdor. Cada línia de la subcontracta que tingui un mètode de facturació de preu fix farà que es creï una línia a la factura del venedor per cada fita de línia de subcontractació que tingui un estat de **Ready to invoice**.

Els següents camps i registres relacionats es copiaran de la subcontractació a la capçalera de la factura de venedor:

- Venedor.
- Les llistes de preus relacionades es copiaran a la factura del proveïdor com a llistes de preus.
- Moneda.
- Unitat de contractació.
- Condicions de pagament.

Per a les línies de subcontractació de temps i material, es copiaran els següents camps i registres relacionats des de la línia de subcontractació fins a la línia de factures del proveïdor:

- Referències de línies de subcontractació i subcontractació
- Classe de la transacció
- Funció
- Categoria de la transacció
- Camps de producte
- Project
- Tasca
- Recurs que es pot reservar

Per a les línies de subcontractació de preu fix, es copiaran els següents camps de la línia de subcontractació i línia de subcontractació a la línia de factures del proveïdor:

- Referències de línies de subcontractació i subcontractació.
- Classe de transacció. Per defecte, el valor serà **Milestone**.
- El nom i l'import de la fita es copiaran de la fita de la línia de subcontractació relacionada.
- L'usuari podrà seleccionar un projecte i una tasca a la línia de factura del proveïdor.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
