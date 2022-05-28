---
title: 'Connexions de transacció: enllaça reals de diferents tipus de transaccions'
description: En aquest tema s'explica com s'utilitza una connexió de transacció per enllaçar reals de diferents tipus per ajudar a fer un seguiment de la rendibilitat, el registre de facturació i els càlculs d'ingressos facturats en comparació amb els ingressos no facturats.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2e8d75a69e27619e6a21f0fe61e2c656e94017b0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580766"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Connexions de transacció: enllaça reals de diferents tipus de transaccions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els registres de connexió de transacció es creen per enllaçar reals de diferents tipus a mesura que el temps, la despesa o l'ús de material es mou en el seu cicle de vida des de la fase d'oferta o prevenda fins a la fase de contractació, aprovacions i / o retirades, facturació i facturació potencialment creditícia o correctiva.

A l'exemple següent es mostra el processament típic de les entrades de temps en un cicle de vida de projecte del Project Operations.

> ![Entrades de temps de processament a les operacions del projecte.](media/basic-guide-17.png)

El processament d'entrades de temps en un cicle de vida del projecte d'operacions de projecte segueix aquests passos: 

1. L'enviament d'una entrada de temps fa que es creï dues línies de diari: una per al cost i una altra per a les vendes no blanques. 
2. L'aprovació definitiva de l'entrada de temps fa que es creï dos reals: un per al cost i un altre per a les vendes nobilades. Aquests 2 reals estan enllaçats mitjançant connexions de transacció.
3. Quan l'usuari crea una factura de projecte, la transacció de línia de factura es crea mitjançant les dades del valor real de vendes no facturades.
4. Quan es confirma la factura, això crea dues novetats reals: una inversió de vendes no facturada i una venda facturada real. La inversió de vendes nobilada i les vendes originals nobilades reals es connecten mitjançant connexions de transacció invertides. Les vendes facturades i les vendes originals no facturades també estan connectades per mostrar els vincles entre el que abans era backlog o els ingressos de work in progress (WIP) amb el que ara es factura als ingressos.   

Cada esdeveniment del flux de treball de processament activa la creació de registres a la **taula De connexió** transacció. Això ajuda a crear un rastre de les relacions entre els registres que es creen a través dels detalls de l'entrada de temps, la línia de diari, la línia real i la línia de factura.

A la taula següent es mostren els registres de l'entitat **Connexió** transacció del flux de treball anterior.

|Incidència                   |Transacció 1                 |Funció de la transacció 1 |Tipus de la transacció 1       |Transacció 2          |Funció de la transacció 2 |Tipus de la transacció 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Enviament d'entrada de temps   |GUID de línia del llibre diari (Vendes)     |Vendes no facturades |msdyn_journalline            |GUID de de línia del llibre diari (cost)     |Cost            |msdyn_journalline  |
|Aprovació de temps           |GUID de valor real no facturat (vendes)  |Vendes no facturades |msdyn_actual                 |GUID del valor real del cost (cost)       |Cost            |msdyn_actual       |
|Creació de la factura        |GUID del detall de la línia de factura      |Vendes facturades   |msdyn_invoicelinetransaction |GUID de valor real de vendes no facturades   |Vendes no facturades  |msdyn_actual       |
|Confirmació de la factura    |GUID del valor real de reversió         |Reversió      |msdyn_actual                 |GUID de vendes no facturades original |Original        |msdyn_actual       |
|                        |GUID de vendes facturades             |Vendes facturades   |msdyn_actual                 |GUID de valor real de vendes no facturades   |Vendes no facturades  |msdyn_actual       |
|Correcció d'esborrany de factura |GUID de transacció de la línia de factura|Reemplaçament      |msdyn_invoicelinetransaction |GUID de vendes facturades            |Original        |msdyn_actual       |
|Correcció de confirmació de factura|GUID de la reversió de vendes facturades  |Reversió      |msdyn_actual                 |GUID de vendes facturades            |Original        |msdyn_actual       |
|                        |Crea un GUID de vendes nobilitzat |Reemplaçament            |msdyn_actual                 |GUID de vendes facturades            |Original        |msdyn_actual       |


La il·lustració següent mostra els enllaços que es creen entre diferents tipus de reals en diversos esdeveniments utilitzant l'exemple d'entrades de temps a les operacions del projecte.

> ![Com els reals de diferents tipus estan vinculats entre si a les operacions del projecte.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
