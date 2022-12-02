---
title: Crea factures del proveïdor
description: En aquest article es descriu el concepte de factures de proveïdor i s'explica com crear-ne al Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475458"
---
# <a name="create-vendor-invoices"></a>Crea factures del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per utilitzar la funcionalitat descrita en aquest article, heu d'habilitar la característica **Habilita el processament de valors reals de subcontracte amb el Project Operations per a escenaris basatsen recursos** a l'àrea de treball **Administració de característiques**.

La facturació del proveïdor al Microsoft Dynamics 365 Project Operations es pot utilitzar per registrar els costos dels lliuraments de serveis i/o materials d'un projecte completat pels proveïdors.

Quan els serveis i/o els materials se subcontracten a un proveïdor, un subcontracte representa l'acord contractual amb aquest proveïdor. Quan el proveïdor proporciona els serveis, o els materials es reben i s'utilitzen en les tasques del projecte, els costos es registren en el projecte. El proveïdor envia periòdicament factures. Aquestes factures es verifiquen i es fan coincidir amb els costos registrats al projecte. Un cop completat el procés de verificació, la factura del proveïdor es confirma i s'allibera per al pagament.

## <a name="scenarios-for-use"></a>Escenaris d'ús

Les factures de proveïdor al Project Operations es poden utilitzar per donar suport a dos escenaris diferents:

- Els clients utilitzen totes les experiències de subcontractació.
- Els clients no utilitzen les totes les experiències de subcontractació, però volen tenir una visualització unificada dels costos dels projectes al Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Els clients utilitzen totes les experiències de subcontractació

Les experiències de factura del proveïdor proporcionen una manera de verificar les entrades de temps, ús de materials i despesa que fan referència a components subcontractats i comparar-les amb les línies de factura del proveïdor. Aquest procés es pot utilitzar per verificar l'exactitud de les línies de factura del proveïdor. Un cop completat el procés de verificació i confirmada la factura del proveïdor, el sistema reverteix els valors reals registrats amb registres de temps, despesa i ús de materials aprovats i crea noves dades de cost mitjançant línies de factura del proveïdor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Els clients no utilitzen les totes les experiències de subcontractació, però volen tenir una visualització unificada dels costos dels projectes al Project Operations

Si feu el seguiment del procés del subcontracte en un sistema de tercers, podeu registrar els costos d'aquest sistema de tercers al Project Operations creant factures de proveïdor que no facin referència a subcontractes. D'aquesta manera, els administradors de projecte poden tenir una visualització unificada de tots els costos d'un projecte determinat.

## <a name="create-vendor-invoices-in-project-operations"></a>Crear factures de proveïdor al Project Operations

Les factures de proveïdor es creen al Dynamics 365 Finance mitjançant el mòdul **Comptes a pagar**. No podeu crear factures de proveïdor directament al Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar la verificació de factures de proveïdor

Si la factura del proveïdor està pensada per a un subcontracte al Dataverse, heu d'habilitar el paràmetre **Cal la verificació manual del PM**. La configuració de l'opció determina si la factura del proveïdor s'ha de confirmar automàticament al Dataverse, o si requereix una confirmació manual. La capçalera de cada factura del proveïdor del projecte inclou una opció amb el mateix nom. Per defecte, l'opció de la capçalera de totes les factures de proveïdor del projecte està definida amb el valor que heu definit aquí. Tanmateix, podeu actualitzar el valor segons calgui a la capçalera de les factures de proveïdor individuals.

Si aquesta opció està definida com a **Sí**, la factura del proveïdor que es crea a Finance i se sincronitza amb el Dataverse té l'estat **Esborrany**. A continuació, la factura l'ha de validar i verificar l'administrador del projecte i l'ha de confirmar abans que es processi i comptabilitzi als comptes de projecte i de llibre de comptabilitat del Finance específics.

Si l'opció es defineix com a **No**, la factura del proveïdor es confirma automàticament. No cal realitzar cap més acció.

Seguiu aquests passos per configurar la verificació de factures del proveïdor.

1. Al Finance, aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres d'administració de projectes i comptabilitat**.
1. A la pestanya **Financer**, definiu l'opció **Cal la verificació manual del PM** en **Sí** si la política de l'empresa requereix la verificació de les factures del proveïdor de subcontractista. Si la verificació per part de l'administrador del projecte no és necessària al Dataverse, deixeu el conjunt d'opcions en **No**. Per defecte, la configuració s'utilitzarà a la pàgina **Factura de proveïdor pendent**.

> [!NOTE]
> Les factures de proveïdor creades per a subcontractes al Dataverse només es poden processar correctament si l'opció **Cal la verificació manual del PM** està definida com a **Sí**. Els valors reals de cost de temps, materials i despeses que els subcontractistes creen es poden aparellar manualment amb les línies de factura del proveïdor per part de l'administrador del projecte només si aquesta opció està finida com a **Sí**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurar un compte d'integració de proveïment per a factures de proveïdor

Quan una factura de proveïdor es comptabilitza al Finance per al Project Operations – Entorn integrat (no existències), les finances es comptabilitzen al compte d'integració de Compres. El sistema genera els valors reals al Dataverse per a la factura comptabilitzada. Aquests valors reals es publiquen al Finance mitjançant el diari d'integració del projecte. El fet de comptabilitzar el llibre diari d'integració del projecte fa que es comptabilitzi el cost real i es reverteixi el compte d'integració de compres.

Per configurar un compte d'integració de compres per a factures de proveïdor, seguiu aquests passos.

1. Al Finance, aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres d'administració de projectes i comptabilitat**.
1. A la pestanya **Project Operations al Dynamics 365 Customer Engagement**, seleccioneu **Materials** \> **Compte d'integració de compres**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crear i comptabilitzar factures de proveïdor de subcontracte

Quan un empleat de Comptes a pagar rep una factura del subcontractista, es crea una factura nova al Finance.

1. Al Finance, aneu a **Compte a pagar** \> **Factures** \> **Factures del proveïdor pendents**.
1. A la **subfinestra Acció**, seleccioneu **Crea** per crear una factura de proveïdor.
1. A la capçalera de la factura, al camp **Compte de la factura**, seleccioneu **Subcontractista**.
1. Seleccioneu la data de factura.
1. A la pestanya **Capçalera**, definiu l'opció **Cal la verificació manual del PM** com a **Sí**. La configuració per defecte d'aquesta opció prové de la pàgina **Paràmetres d'administració de projectes i comptabilitat**. Tanmateix, es pot canviar en el nivell de factura de proveïdor.
1. A la FastTab **Línia de factura**, seleccioneu **Afegeix una línia** per crear una línia de factura de proveïdor.
1. Seleccioneu la categoria de compra que s'ha creat per a les línies de subcontracte i introduïu el preu per unitat, la unitat de mesura i la quantitat.
1. A la secció de línies de factura de proveïdor, a la pestanya **Projecte**, seleccioneu el projecte amb el qual el subcontractista comparteix la factura del subcontracte.
1. Seleccioneu la categoria de projecte. Pot ser de qualsevol tipus d'**Article**, **Despesa**, **Materials** o **Hores**.
1. Seleccioneu la funció només si la categoria de projecte seleccionada és de tipus **Hora**.
1. Seleccioneu **Publica** per publicar la factura del proveïdor.

O bé, podeu crear una factura de proveïdor anant a **Compte a pagar** \> **Factures** \> **Factures de proveïdor pendents** i seleccioneu **Crea**.

Quan la factura de proveïdor es publica, passa a estar disponible al Dataverse per a la verificació de l'administrador del projecte i el processament.

## <a name="vendor-invoice-processing-in-dataverse"></a>Processament de factures de proveïdor al Dataverse

A la factura de proveïdor creada al Dataverse, alguns valors de camp provenen de la factura de proveïdor que es registra al Finance. Altres valors són els valors per defecte que provenen del subcontracte.

Els camps següents i els registres relacionats es copiaran des del subcontracte a la capçalera de la factura del proveïdor:

- Moneda
- Unitat de contractació
- Condicions de pagament

A les línies de factura de proveïdor, el Project Operations utilitza els valors de camp següents per introduir la referència de línia de subcontracte i subcontracte per defecte:

- Classe de la transacció
- Funció
- Categoria de la transacció
- Camps de producte
- Project
- Tasca

> [!NOTE]
> Les línies de subcontracte de preu fix no estan admeses al Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
