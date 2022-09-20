---
title: Crear factures de proveïdors
description: En aquest article es descriu el concepte de factures de proveïdors i s'explica com crear-les a Microsoft Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Crear factures de proveïdors

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per utilitzar la funcionalitat que es descriu en aquest article, heu d'habilitar la funció Habilita el **processament de realitats subcontractades amb Project Operations per a escenaris basats** en recursos a l'espai de treball d'administració **de** funcions.

La facturació de proveïdors a Microsoft Dynamics 365 Project Operations es pot utilitzar per registrar els costos derivats d'enviaments de serveis i/o materials en un projecte que els proveïdors completen.

Quan els serveis i/o materials són subcontractats a un venedor, un subcontractista representa l'acord contractual amb aquest venedor. A mesura que el proveïdor lliura els serveis, o a mesura que els materials es reben i s'utilitzen en les tasques del projecte, els costos es registren al projecte. A continuació, el venedor envia periòdicament factures. Aquestes factures es verifiquen i coincideixen amb els costos que es registren al projecte. Un cop finalitzat el procés de verificació, la factura del proveïdor es confirma i es publica per al pagament.

## <a name="scenarios-for-use"></a>Escenaris d'ús

Les factures de proveïdors del Project Operations es poden utilitzar per admetre dos escenaris diferents:

- Els clients utilitzen les experiències completes de subcontractació.
- Els clients no utilitzen les experiències completes de subcontractació, però volen tenir una visió unificada dels costos dels projectes en operacions de projecte.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Els clients utilitzen les experiències completes de subcontractació

Les experiències de factures dels proveïdors proporcionen una manera de verificar les entrades de temps, l'ús de material i els assentaments de despeses que fan referència als components subcontractats i els coincideixen amb les línies de factures dels proveïdors. Aquest procés es pot utilitzar per verificar l'exactitud de les línies de factura del proveïdor. Un cop finalitzat el procés de verificació i confirmada la factura del proveïdor, el sistema inverteix els reals registrats pels registres de temps, despeses i ús de material aprovats i, a continuació, crea nous reals de costos mitjançant les línies de factures del proveïdor.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Els clients no utilitzen les experiències completes de subcontractació, però volen tenir una visió unificada dels costos dels projectes en operacions de projecte

Si feu un seguiment del procés de subcontractació en un sistema de tercers, podeu registrar els costos d'aquest sistema de tercers a Project Operations creant factures de proveïdors que no facin referència a subcontractes. D'aquesta manera, els vostres gestors de projectes poden tenir una visió única i unificada de tots els costos d'un projecte determinat.

## <a name="create-vendor-invoices-in-project-operations"></a>Crear factures de proveïdors a Project Operations

Les factures dels proveïdors es creen en Dynamics 365 Finance, mitjançant el **mòdul Comptes a pagar**. No podeu crear factures de proveïdor directament a Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Configurar la verificació de factures del proveïdor

Si la factura del venedor està destinada a un subcontractista en Dataverse, s'ha d'habilitar el **paràmetre Verificació manual per PM**. La configuració de l'opció determina si la factura del proveïdor s'ha de confirmar automàticament a Dataverse, o si requereix confirmació manual. La capçalera de cada factura del proveïdor del projecte inclou una opció del mateix nom. Per defecte, l'opció de la capçalera de totes les factures de proveïdor del projecte s'estableix al valor que definiu aquí. Tanmateix, podeu actualitzar el valor segons calgui a la capçalera de les factures individuals dels proveïdors.

Si l'opció està definida com a **Sí**, la factura del proveïdor que es crea a Finances i se sincronitza amb l'estat Dataverse **Esborrany**. La factura ha de ser validada i verificada pel gestor del projecte, i confirmada, abans de ser processada i comptabilitzada al projecte específic i als comptes comptables de Finances.

Si l'opció està definida com a **No**, la factura del proveïdor es confirma automàticament. No cal fer més accions.

Per configurar la verificació de factures del proveïdor, seguiu aquests passos.

1. A Finances, aneu a **Gestió de projectes i configuració** \> **comptable** \> **De gestió de projectes i paràmetres comptables.**
1. A la pestanya Financer **, definiu l'opció** Verificació manual per PM és necessària **a** Sí **si la** política de l'empresa requereix la verificació de les factures dels proveïdors subcontractistes. Si no cal Dataverse la verificació per part de l'administrador del projecte, deixeu el conjunt d'opcions al **núm**. Per defecte, la configuració s'utilitzarà a la **pàgina Factura** de proveïdor pendent.

> [!NOTE]
> Les factures de proveïdors que es creen per a subcontractes només Dataverse es poden processar correctament si l'opció **Verificació manual per PM es defineix** com a **Sí**. Els reals de temps, material i costos de despeses que creen els subcontractistes poden coincidir manualment amb les línies de factures del proveïdor pel gestor del projecte només si aquesta opció està definida com a **Sí**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurar un compte d'integració d'adquisicions per a factures de proveïdors

Quan es publica una factura de proveïdor a Finance for Project Operations – Entorn integrat (sense existències), les finances es publiquen al compte d'integració de compres. El sistema genera el cores in Dataverse per a la factura comptabilitzada. Aquests reals es publiquen a Finances mitjançant la revista d'integració de projectes. La publicació del diari d'integració de projectes publica el cost real i inverteix el compte d'integració de compres.

Per configurar un compte d'integració d'adquisicions per a factures de proveïdor, seguiu aquests passos.

1. A Finances, aneu a **Gestió de projectes i configuració** \> **comptable** \> **De gestió de projectes i paràmetres comptables.**
1. A la **pestanya Operacions del projecte al Dynamics 365 Customer Engagement**, seleccioneu **Compte d'integració** \> **de l'adquisició de materials.**

### <a name="create-and-post-subcontract-vendor-invoices"></a>Crear i publicar factures de proveïdors subcontractats

Quan un empleat de Comptes a pagar rep una factura del subcontractista, es crea una nova factura a Finances.

1. A Finances, aneu a Comptes a **pagar Factures** \> **pendents** \> **de proveïdor**.
1. A la subfinestra **d**'accions, seleccioneu **Crea** per crear una factura de proveïdor.
1. A la capçalera de la factura, al camp Compte **de** factura, seleccioneu **Subcontractista**.
1. Seleccioneu la data de factura.
1. A la **pestanya Capçalera**, definiu l'opció **Verificació manual per PM és necessària** a **Sí**. La configuració predeterminada d'aquesta opció prové de la **pàgina Administració de projectes i paràmetres comptables**. No obstant això, es pot canviar a nivell de factura del proveïdor.
1. A la **línia** De factura FastTab, seleccioneu **Afegeix una línia** per crear una línia de factures de proveïdor.
1. Seleccioneu la categoria de contractació que s'ha creat per a línies de subcontractació i introduïu el preu unitari, la unitat de mesura i la quantitat.
1. A l'apartat línies de factures del proveïdor, a la **pestanya Projecte**, seleccioneu el projecte contra el qual el subcontractista comparteix la factura subcontractada.
1. Seleccioneu la categoria de projecte. Pot ser de qualsevol tipus d'article **·**, **despesa**, **materials** o **hores**.
1. Seleccioneu la funció només si la categoria de projecte seleccionada és del **tipus Hora**.
1. Seleccioneu **Publica** per publicar la factura del proveïdor.

Com a alternativa, podeu crear una factura de proveïdor anant a Comptes a **pagar** \> **Factures** \> **obertes factures** de proveïdor i seleccionant **Crea.**

Quan es publica la factura del proveïdor, estarà disponible per a la Dataverse verificació i el processament del gestor de projectes.

## <a name="vendor-invoice-processing-in-dataverse"></a>Processament de factures de proveïdors a Dataverse

En la factura del venedor que es crea en Dataverse, alguns valors de camp provenen de la factura del venedor que es registra en Finances. Altres valors són valors per defecte que provenen de la subcontractació.

Els següents camps i registres relacionats es copiaran de la subcontractació a la capçalera de la factura de venedor:

- Moneda
- Unitat de contractació
- Condicions de pagament

A les línies de factures de proveïdors, Project Operations utilitza els valors de camp següents per introduir la referència per defecte de la línia de subcontractació i subcontractació:

- Classe de la transacció
- Funció
- Categoria de la transacció
- Camps de producte
- Project
- Tasca

> [!NOTE]
> Les línies de subcontractació de preu fix no s'admeten a Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
