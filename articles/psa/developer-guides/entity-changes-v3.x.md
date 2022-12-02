---
title: Canvis d'entitat, control i interfície d'usuari (Project Service Automation 3.x)
description: En aquest article s'expliquen els canvis a les solucions per al Microsoft Dynamics Project Service Automation 3.x.
author: makk
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f54d263666c4fb999464f98c0138fc008dbbbd2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926856"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Canvis d'entitat, control i interfície d'usuari (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]


Amb el llançament del Microsoft Dynamics Project Service Automation (PSA) 3.x, s'han fet molts canvis a les entitats, els controls, les visualitzacions i la interfície d'usuari. Aquest article proporciona informació sobre aquests canvis importants.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relacions principal-secundari per a les entitats de documents de vendes, línia de documents de vendes, detalls de línies de documents de vendes
En versions del Dynamics 365 Project Service Automation (PSA) publicades abans de la versió 3.0, algunes de les relacions entre les entitats de documents de vendes, línies de documents de vendes i detall de línies de documents de vendes es van implementar a través de camps de cadenes de text que tindrien una representació de cadena de text de GUID de l'entitat relacionada. Això es devia a les limitacions de la plataforma que requerien un codi personalitzat significatiu al costat del servidor i del client de la solució per fer que aquestes relacions funcionessin de manera similar a les relacions d'entitat típiques del Dynamics CRM i per fer que els camps de cadena de text actuessin com a camps de cerca.

El PSA 3.0 s'ha actualitzat per aprofitar les noves relacions d'entitat entre el les entitats de document de vendes i línies de documents de vendes.

Com que ara els camps de cerca es poden utilitzar per indicar referències a entitats, els camps que contenien el valor de cadena de text del GUID de l'entitat relacionada en versions anteriors ja no són necessaris i, per tant, són obsolets. El codi personalitzat del costat del client i del servidor que controla les relacions definides pels camps de cadena de text heretats també són obsolets.

### <a name="entity-schema-changes"></a>Canvis d'esquema d'entitat
A la taula següent es proporciona una llista un a un dels camps de cadena de text obsolets i els camps de cerca nous per a les entitats. 

 Entitat |   Camp obsolet (cadena de text) | Camp nou (cerca)
--- | --- | ---
invoicedetail (línia de factura) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (valor real) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (planificació de facturació de la línia de contracte del projecte) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (fita de línia de contracte de projecte) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (fet) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (detall de la línia de factura) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (línia del llibre diari) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (categoria del recurs de línia de contracte del projecte) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (detall de línia de contracte del projecte) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (categoria de transacció de línia de contracte del projecte) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (classificació de transacció de línia de contracte del projecte) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (planificació de facturació de la línia d'oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (categoria de recursos de línia d'oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (fita de la línia d'oferta) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (detall de la línia d'oferta) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (categoria de la transacció de línia d'oferta) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (classificació de la transacció de la línia d'oferta) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetai (línia de comanda) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Visualitzacions i controls personalitzats obsolets
Les visualitzacions i els controls personalitzats següents, i els seus artefactes relacionats, són obsolets.

- Visualització de la imputabilitat.
- Controls de quadrícula personalitzats per mostrar els detalls de la línia d'oferta a la pàgina **Informació del projecte** de la línia d'oferta.
- Controls de quadrícula personalitzats per mostrar els detalls de la línia d'e contracte del projecte a la pàgina **Informació del projecte** de la línia de comanda de vendes.

> [!NOTE]
> Per veure la llista completa de recursos obsolets, vegeu [Recursos web obsolets al Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Mòdul de l'aplicació de la interfície de client unificada
Amb la introducció dels mòduls de l'aplicació de la interfície de client unificada (UCI), les entrades del mapa del lloc del PSA s'ha eliminat del sistema.  
La funcionalitat relacionada amb el canvi de formularis per Oportunitat, Oferta, Comanda i Factura és obsoleta ja que ja no és necessària perquè el mòdul d'aplicacions d'UCI només inclou les versions del PSA dels formularis.  

Els recursos web següents són obsolets:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Per veure la llista completa de recursos obsolets, vegeu [Recursos web obsolets al Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
