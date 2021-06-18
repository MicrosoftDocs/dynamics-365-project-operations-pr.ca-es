---
title: Integració de l'administració de despeses
description: Aquest tema proporciona informació sobre la integració de l'informe de despeses al Project Operations mitjançant doble escriptura.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7fff69f062bf09fe7ceca61d951b535d2e010bfd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999974"
---
# <a name="expense-management-integration"></a>Integració de l'administració de despeses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema proporciona informació sobre la integració d'informes de despeses al Project Operations [implementació total de despeses](../expense/expense-overview.md) mitjançant doble escriptura.

## <a name="expense-categories"></a>Categories de despesa

En una implementació total de les despeses, es creen i es mantenen les categories de despesa a les aplicacions del Finance and Operations. Per crear una categoria de despesa nova, seguiu aquests passos:

1. Al Microsoft Dataverse, creeu una categoria de **Transacció**. La integració amb doble escriptura sincronitzarà aquesta categoria de transacció a les aplicacions del Finance and Operations. Per obtenir més informació, vegeu [Configuració de les categories de projecte](/dynamics365/project-operations/project-accounting/configure-project-categories) i [Configuració del Project Operations i integració de dades de configuració](resource-dual-write-setup-integration.md). Com a resultat d'aquesta integració, el sistema crea quatre registres de categoria compartida a les aplicacions del Finance and Operations.
2. A Finances, aneu a **Administració de despeses** > **Configuració** > **Categories compartides** i seleccioneu una categoria compartida amb una classe de transacció **Despesa**. Definiu el paràmetre **Es pot utilitzar en despesa** com a **Cert** i definiu el tipus de despesa que s'utilitzarà.
3. Amb aquest registre de categoria compartida, creeu una categoria de despesa nova anant a **Administració de despeses** > **Configuració** > **Categories de despeses** i seleccionant **Crea**. Quan el registre es desa, la doble escriptura utilitza l'assignació de taules **Entitat d'exportació de categories de despeses del projecte d'integració del Project Operations (msdyn\_despesescategories)** per sincronitzar aquest registre amb el Dataverse.

  ![Integració de categories de despesa](./media/DW6ExpenseCategories.png)

Les categories de despesa de les aplicacions del Finance and Operations són específiques de l'empresa o de l'entitat jurídica. Hi ha registres específics d'entitats jurídiques corresponents i separades al Dataverse. Quan un administrador del projecte calcula les despeses, no pot seleccionar les categories de despeses creades per a un projecte que és propietat d'una empresa diferent de l'empresa propietària del projecte en què estan treballant. 

## <a name="expense-reports"></a>Informes de despeses

Els informes de despeses es creen i s'aproven a les aplicacions del Finance and Operations. Per obtenir més informació, vegeu [Crear i processar informes de despeses al Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Després que l'administrador del projecte aprovi l'informe de despeses, s'envia al registre general. Al Project Operations, les línies d'informe de despeses relacionades amb el projecte es publiquen mitjançant regles de publicació especials:

  - El cost relacionat amb el projecte (incloent-hi els impostos que no es poden recuperar) no es publica immediatament al compte de cost del projecte en un registre general, sinó que es publica al compte d'integració de despeses. Aquest compte es configura a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i la pestanya de **Project Operations al Dynamics 365 Customer Engagement**.
  - La doble escriptura se sincronitza amb el Dataverse mitjançant l'assignació de taules **Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses)**.
  - El subllibre de comptabilitat d'impostos, el subllibre de comptabilitat de proveïdors i les altres publicacions financeres es registren segons calgui en el moment de publicar l'informe de despeses.

  ![Integració d'informes de despeses](./media/DW6ExpenseReports.png)

Quan s'escriu un registre a l'entitat **Despesa** al Dataverse, el sistema activa el procés d'aprovació automatitzada del registre. Si cal, l'estat del procés d'aprovació automatitzada es pot revisar al Dataverse anant a **Configuració avançada** > **Sistema** > **Feines del sistema**. Un cop completada l'aprovació, es creen registres de classes de transacció de despeses a l'entitat **Valors reals**.

A continuació, els valors reals relacionats amb les despeses es processen amb l'assignació de taules de doble escriptura **Valors reals d'integració del Project Operations (msdyn\_reals)**. Per obtenir més informació, vegeu [Estimacions i valors reals del projecte](resource-dual-write-estimates-actuals.md).

El procés periòdic **Importació des de la còpia intermèdia** crea línies del llibre diari relacionades amb l'informe de despeses al llibre diari d'integració del Project Operations. El compte de desplaçament es defineix per defecte al compte d'integració de despeses. El llibre diari d'integració de les publicacions esborra el balanç del compte de la transacció de despeses i desplaça l'import de la despesa al compte de cost del projecte. El sistema també crea subllibres de comptabilitat del projecte amb finalitats de facturació descendent i de reconeixement d'ingressos.
