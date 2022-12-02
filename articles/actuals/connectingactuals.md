---
title: 'Connexions de transaccions: enllaçar els valors reals de diferents tipus de transaccions'
description: En aquest article s'explica com s'utilitza una connexió de transacció per enllaçar els valors reals de diferents tipus per fer el seguiment de la rendibilitat, el treball pendent de facturació i els càlculs de valors facturats i no facturats.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926074"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Connexions de transaccions: enllaçar els valors reals de diferents tipus de transaccions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els registres de connexió de transacció es creen per enllaçar valors reals de diferents tipus a mesura que el temps, la despesa o l'ús material avancen en el cicle de vida des de la fase d'oferta o la fase de prevendes fins a la fase de contracte, les aprovacions o les retirades, la facturació i la facturació potencialment creditícia o correctiva.

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del Project Operations.

> ![Processar entrades de temps al Project Operations.](media/basic-guide-17.png)

El processament de les entrades de temps en un cicle de vida de projecte del Project Operations segueix aquests passos: 

1. L'enviament d'una entrada de temps provoca la creació de dues línies de llibre diari: una per a cost i una per a vendes no facturades. 
2. L'aprovació final de l'entrada de temps provoca la creació de dos valors reals: un per a cost i un per a vendes no facturades. Aquests 2 valors reals s'enllacen mitjançant connexions de transacció.
3. Quan l'usuari crea una factura de projecte, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades.
4. Quan es confirma la factura, es creen dos valors reals nous: una reversió de vendes sense facturar i un valor real de vendes facturades. La reversió de vendes no facturades i les vendes no facturades originals es connecten mitjançant connexions de transacció de reversió. Les vendes facturades i els valors reals de vendes no facturades originals també es connecten per mostrar els enllaços entre el que era treball pendent o els ingressos del treball en curs (WIP) amb el que són ara ingressos facturats.   

Cada incidència del flux de treball de processament activa la creació de registres a la taula de **Connexió de transacció**. Això ajuda a crear una traça de la relació entre els registres que es creen entre l'entrada de temps, la línia de llibre diari, el valor real i els detalls de la línia de factura.

A la taula següent es mostren els registres de l'entitat **Connexió de transacció** per al flux de treball anterior.

|Incidència                   |Transacció 1                 |Funció de la transacció 1 |Tipus de la transacció 1       |Transacció 2          |Funció de la transacció 2 |Tipus de la transacció 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Enviament d'entrada de temps   |GUID de línia del llibre diari (Vendes)     |Vendes no facturades |msdyn_journalline            |GUID de de línia del llibre diari (cost)     |Cost            |msdyn_journalline  |
|Aprovació de temps           |GUID de valor real no facturat (vendes)  |Vendes no facturades |msdyn_actual                 |GUID del valor real del cost (cost)       |Cost            |msdyn_actual       |
|Creació de la factura        |GUID del detall de la línia de factura      |Vendes facturades   |msdyn_invoicelinetransaction |GUID de valor real de vendes no facturades   |Vendes no facturades  |msdyn_actual       |
|Confirmació de la factura    |GUID del valor real de reversió         |Reversió      |msdyn_actual                 |GUID de vendes no facturades original |Original        |msdyn_actual       |
|                        |GUID de vendes facturades             |Vendes facturades   |msdyn_actual                 |GUID de valor real de vendes no facturades   |Vendes no facturades  |msdyn_actual       |
|Correcció d'esborrany de factura |GUID de transacció de la línia de factura|Reemplaçament      |msdyn_invoicelinetransaction |GUID de vendes facturades            |Original        |msdyn_actual       |
|Correcció de confirmació de factura|GUID de la reversió de vendes facturades  |Reversió      |msdyn_actual                 |GUID de vendes facturades            |Original        |msdyn_actual       |
|                        |Nou GUID de vendes no facturades |Reemplaçament            |msdyn_actual                 |GUID de vendes facturades            |Original        |msdyn_actual       |


A la il·lustració següent es mostren els enllaços que es creen entre els diferents tipus de valors reals en diverses incidències fent servir l'exemple d'entrades de temps del Project Operations.

> ![Com s'enllacen entre si els valors reals de diferents tipus al Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
