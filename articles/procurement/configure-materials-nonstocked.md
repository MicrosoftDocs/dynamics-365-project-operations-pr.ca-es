---
title: Configuració de materials sense existències i de factures pendents del proveïdor
description: En aquest tema s'explica com s'han d'habilitar els materials sense existències i les factures pendents del proveïdor.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9b55d959228062fc3577cf7f12d8926f51e9791f98c73fdc4b78251312a8a77a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003219"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Configuració de materials sense existències i de factures pendents del proveïdor

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="minimum-version-requirement"></a>Requisit mínim de la versió

Per utilitzar materials sense existències i factures pendents del proveïdor per a escenaris basats en recursos o sense existències per al Dynamics 365 Project Operations requereix aquestes versions:

Solucions del Dynamics 365 Dataverse:

- Project Operations 4.9.0.221 o una versió posterior
- Solució d'orquestració d'aplicacions de doble escriptura 2.2.2.23 o una versió posterior

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) o una versió posterior. Assegureu-vos que l'entorn de Finances estigui actualitzat i que totes les actualitzacions de qualitat s'apliquin segons els requisits mínims de versió.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Executar assignacions de doble escriptura per a la integració de materials sense existències i de factures del proveïdor

Aquesta secció proporciona informació sobre les assignacions específiques necessàries per als materials sense existències i les factures de proveïdors. Verifiqueu que les assignacions de requisits previs que s'enumeren al tema [Proveïment d'un entorn nou](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) s'estiguin executant al vostre entorn.

1. Aneu a Lifecycle Services (LCS), aneu al projecte LCS i aneu a la pàgina **Detalls de l'entorn**.
2. A la secció **Informació de l'entorn Common Data Service**, seleccioneu **Enllaça amb CDS per a aplicacions**. Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.
3. Assegureu-vos que s'estiguin executant les assignacions següents. Si no s'estan executant, inicieu-les i assegureu-vos d'incloure totes les assignacions de taules relacionades.

    - Diferents productes publicats amb CDS (productes)
    - Proveïdors v2 (msdyn_vendors)
    - Taula del Project Operations per a estimacions de materials (msdyn_estimatelines)
    - Entitat d'exportació de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoices)
    - Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations (msdyn_projectvendorinvoicelines)
    - Valors reals d'integració del Project Operations (msdyn_actuals). Assegureu-vos que esteu executant la versió d'assignació 1.0.0.14 o una de posterior. Podeu veure la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versió de l'assignació de la taula** i després deseu la versió seleccionada.

Si utilitzeu dades de demostració estàndard, pot ser que també hàgiu d'aturar i reiniciar les assignacions d'entitat següents amb la sincronització inicial:
  - Dies de pagament en CDS V2 (msdyn_paymentdays)
  - Planificació de pagaments (msdyn_paymentschedules)
  - Condicions de pagament (msdyn_paymentterms)
  - Grups de proveïdors (msdyn_vendorgroups)
  - Unitats (uom)

> [!NOTE]
> La sincronització inicial per a grups de proveïdors i unitats pot fallar en alguns registres del conjunt de dades de demostració existent. Podeu ignorar els errors perquè no us privaran d'utilitzar dades de demostració amb el Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Configuració dels requisits previs al Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Activació del flux de treball per crear comptes basats en una entitat de proveïdor

La solució Dual Write Orchestration proporciona [Integracó del patró de proveïdors](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping)Proveïdors. Com a requisit previ per a aquesta característica, les dades del proveïdor s'han de crear a l'entitat **Comptes**. Activació d'un procés de flux de treball de plantilla per crear proveïdors a la taula **Comptes**, segons s'explica a [Canvia entre els dissenys del proveïdor](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch).

### <a name="set-products-to-be-created-as-active"></a>Definiu que els productes es creïn com a actius

Els materials sense existències s'han de configurar com a **Productes publicats** a Finances. La solució Dual Write Orchestration proporciona una [Integració de productes publicats a punt per a utilitzar al catàleg de productes del Dataverse](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Per defecte, els productes de Finances se sincronitzen amb el Dataverse en estat d'esborrany. Per sincronitzar el producte amb un estat actiu per tal que es pugui utilitzar directament en documents d'ús de materials o en factures de proveïdor pendents, aneu a **Sistema** > **Administració** > **Administració del sistmea** > **Configuració del sistema** i, a la pestanya **Vendes**, definiu **Creació de productes en estat actiu** en **Sí**.

## <a name="configure-prerequisites-in-finance"></a>Configuració dels requisits previs a Finances

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>Habilitació de la clau de característica per a les factures del proveïdor pendents

Completeu els passos següents per habilitar la funcionalitat per afegir detalls del projecte a les línies de factura del proveïdor pendents.

1. A Finances, aneu a l'espai de treball **Administració de característiques**.
2. A la llista de característiques, cerqueu la característica **Habilita les factures del proveïdor pendents al Project Operations per a escenaris basats en recursos o sense existències** i seleccioneu **Habilita**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Definició de grups de categories i categories de projecte per als elements

Configureu com a mínim un grup de categories per al tipus de transacció **Element**, i com a mínim una categoria de projecte utilitzant aquest grup. Per obtenir més informació, vegeu [Configuració de categories de projecte](../project-accounting/configure-project-categories.md#category-groups).

Reviseu els perfils de cost i ingressos del projecte i configureu la configuració de publicació de missatges per a les transaccions d'articles. Per obtenir més informació, vegeu [Configuració de la comptabilitat per a projectes facturables](../project-accounting/configure-accounting-billable-projects.md).

### <a name="set-up-a-write-in-product"></a>Configuració d'un producte fora de catàleg

Al Project Operations, podeu registrar les estimacions i l'ús de materials dels productes del catàleg que es configuren al catàleg de productes publicats i als productes fora de catàleg. Per utilitzar productes fora de catàleg cal un únic producte publicat que s'ha configurat a Finances amb aquesta finalitat. Completeu els passos següents per configurar un producte fora de catàleg. Repetiu aquests passos a cada entitat legal que utilitzi el Project Operations per a escenaris de recursos o sense existències.

1. A Finances, aneu a **Administració de la informació dels productes** > **Productes** > **Productes publicats**, i seleccioneu **Crea**.
2. Al camp **Tipus de producte**, seleccioneu **Element** i al camp **Subtipus de producte** seleccioneu **Producte**.
3. Introduïu el número del producte (WRITEIN) i el nom del producte (Producte fora de catàleg).
4. Seleccioneu el grup del model d'elements. Assegureu-vos que el grup del model d'elements que seleccioneu té el camp **Producte en existències de la política d'inventari** en **Fals**.
5. Seleccioneu valors als camps **Grup d'elements**, **Grup de mesures d'emmagatzematge** i **Grup de mesures de seguiment**. Utilitzeu la **Mesura d'emmagatzematge** només per al **Lloc** i, al camp **Mesures de seguiment**, seleccioneu **Cap**.
6. Seleccioneu valors al camp **Unitat d'inventari**, **Unitat de compra** i **Unitat de vendes** i, a continuació, deseu els canvis.
7. A la pestanya **Pla**, definiu la configuració de comanda per defecte i, a la pestanya **Inventari**, definiu el lloc per defecte i el magatzem.
8. Aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i obriu **Project Operations al Dynamics 365 Dataverse**. 
9. A la pestanya **Materials**, al camp **Producte fora de catàleg**, seleccioneu el producte que heu creat.
10. Al vostre entorn del Dataverse, al mapa del lloc, obriu l'entitat **Productes** i cerqueu el registre de producte fora de catàleg. 
11. Obriu els detalls del registre i definiu l'estat de producte com a **Retirat**. Aquest estat del producte impedeix que algú pugui utilitzar accidentalment aquest registre directament en les estimacions de materials i en els documents d'ús.

### <a name="set-up-a-procurement-integration-account"></a>Configuració d'un compte d'integració de proveïment

El compte d'integració de proveïment s'utilitza com a compte de neteja quan es publica una factura del proveïdor pendent amb línies atribuïdes a un projecte.

Quan el sistema publica una factura de proveïdor pendent, aquest compte s'utilitza per a l'import de cost del projecte. Els detalls de la factura del proveïdor es processen al Dataverse i es crea un valor real del projecte corresponent. La informació del valor real del projecte s'afegeix al llibre diari d'integració del Project Operations. Quan publiqueu el llibre diari d'integració, la quantitat s'esborra del compte d'integració del proveïment i es registra al cost del projecte.

1. Per configurar un compte d'integració del proveïment, aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte** i obriu **Project Operations al Dynamics 365 Dataverse**. 
2. Seleccioneu la pestanya **Materials** i seleccioneu un valor al camp **Compte d'integració del proveïment**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Configuració per defecte de les categories de projecte per a un element

1. A Finances, aneu a **Administració i comptabilitat del projecte** > **Configuració** > **Paràmetres d'administració i comptabilitat del projecte**, i obriu **Project Operations al Dynamics 365 Dataverse**. 
2. A la pestanya **Valors per defecte de la categoria del projecte**, al camp **Element**, seleccioneu un valor. Aquesta categoria de projecte s'utilitza per a transaccions materials si la categoria de projecte no s'ha definit al registre de valors reals del projecte.
