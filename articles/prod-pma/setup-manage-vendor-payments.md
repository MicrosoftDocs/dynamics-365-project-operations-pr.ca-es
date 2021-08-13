---
title: Configuració i ús dels pagaments dels proveïdors després del cobrament
description: Aquest tema explica com crear termes de pagament després del pagament (PWP) de manera que pugueu alliberar pagaments parcials de proveïdors, en funció dels pagaments del client.
author: RadhikaRS
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 9976dadf57f1c84bf3f295ff3c8359c16e4849a3bf887f8bd33e46a04e2a5952
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008844"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Configuració i ús dels pagaments dels proveïdors després del cobrament

[!include [banner](../includes/banner.md)]

Quan aproveu que un venedor treballi com a subcontractista, potser voleu retenir el pagament al venedor fins que el client us pagui pel projecte. Per admetre aquest escenari, podeu establir termes de pagament després del pagament (PWP) quan configureu la comanda de compra (PO) amb el venedor.

Per exemple, quan un client paga una quantitat en una factura de projecte, podeu alliberar una part o tot l'import de la factura del proveïdor. Simplement configureu els termes de PWP que especifiquin que es pagarà al proveïdor després de rebre un percentatge del pagament relacionat del client. Si rebeu un pagament parcial d'un client, podeu alliberar manualment algunes de les factures del proveïdor relacionades per al pagament.

El següent exemple descriu el procés quan s'utilitzen termes de PWP.

## <a name="example"></a>Exemple

La vostra organització accepta proporcionar a un client 100 ordinadors que tinguin instal·lat programari, per un preu de 150,00 USD per ordinador. Llavors contracteu un proveïdor per proporcionar-vos els ordinadors que tenen instal·lat el programari. Segons l'acord, el client ha d'aprovar la qualitat dels ordinadors abans de pagar a la vostra organització. La norma de la vostra organització és retenir el pagament als proveïdors fins que el client us hagi pagat. Per tant, heu configurat el projecte perquè tingui un percentatge de PWP del 100 per cent.

El venedor us envia els 100 ordinadors que tenen el programari instal·lat, juntament amb una factura de 10.000,00 USD. Com que els termes de PWP estan configurats per al vostre projecte, no pagueu al proveïdor després de rebre els ordinadors. En comptes d'això, envieu els ordinadors al client, juntament amb una factura de 15.000,00. El client inspecciona els ordinadors i aprova l'import complet de la factura del projecte.

Després de rebre el pagament complet del client, pagueu al proveïdor 10.000,00, l'import complet de la factura del proveïdor.

## <a name="set-up-pwp-terms-for-a-project"></a>Configurar els termes de PWP per a un projecte

Quan configureu els termes de PWP per a un projecte, heu d'especificar, com a percentatge, l'import mínim que un client ha de pagar pel projecte abans de pagar al proveïdor. L'import de llindar es calcula automàticament en les factures de client del projecte. Seguiu aquests passos per establir el percentatge del llindar per als termes de PWP.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes**.
2. Cerqueu i obriu el projecte per al qual voleu establir els termes de PWP.
3. Al FastTab **Acords de proveïdors**, seleccioneu **Afegeix una línia**.
3. En el camp **Codi del compte**, seleccioneu una de les següents opcions:

    - **Taula**: els termes de PWP s'apliquen a un sol proveïdor.
    - **Grup**: els termes de PWP s'apliquen a tots els proveïdors d'un grup de proveïdors.
    - **Tots**: els termes de PWP s'apliquen a tots els proveïdors.

4. Si seleccioneu **Taula** o **Grup** en el pas anterior, en el camp **Proveïdor/Grup de proveïdors**, seleccioneu el proveïdor o el grup de proveïdors al qual s'apliquen els termes de PWP. Si seleccioneu **Tots** en el pas anterior, el camp **Proveïdor/Grup de proveïdors** no es pot editar.
5. Si hi ha termes de retenció de proveïdors establerts per al proveïdor en el projecte, en el camp **Termes de retenció de proveïdor**, seleccioneu l'ID de regla per als termes de retenció.
6. En el camp **Percentatge de llindar de PWP**, introduïu el percentatge de llindar per al projecte. El percentatge que introduïu per al projecte defineix l'import mínim que el client ha de pagar abans de pagar al proveïdor.

## <a name="create-a-po-that-has-pwp-terms"></a>Crear una comanda de compra que tingui termes de PWP

Quan comptabilitzeu una factura d'un proveïdor, si el proveïdor està subjecte a termes de PWP, aquests termes es mostren en les línies de la comanda de compra. Per crear una comanda de compra que tingui termes de PWP, seguiu aquests passos.

1. Aneu a **Contractació i proveïment** \> **Comandes de compra** \> **Totes les comandes de compra**.
2. A la subfinestra d'acció, seleccioneu **Nou**. Llavors, en el quadre de diàleg **Creació de la comanda de compra**, introduïu la informació necessària i seleccioneu **D'acord**.

    Alternativament, obriu una comanda de compra existent a la pàgina de llista **Totes les comandes de compra**.

4. A la pàgina **Comanda de compra**, al FastTab **Línies de la comanda de compra**, reviseu els detalls de la línia de la comanda de compra per al proveïdor. L'opció **Pagament després del cobrament** se selecciona automàticament i el valor en el camp **Percentatge de llindar de PWP** es copia automàticament del camp **Percentatge de llindar de PWP** de la pàgina **Projectes**.
6. Si no voleu aplicar termes de PWP al proveïdor per a una línia de comanda de compra, desactiveu l'opció **Pagament després del cobrament**. En aquest cas, el camp **Percentatge de llindar de PWP** per a la línia de la comanda de compra es restablirà a 0 (zero).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Actualitzar un pagament de client i pagar al proveïdor

Quan un proveïdor completa el seu treball en un projecte i us envia una factura, heu de revisar l'estat del projecte i les factures del client per determinar si els termes de PWP s'han complert per al projecte. Si es compleixen els termes de PWP per al proveïdor, podeu determinar quines línies de la factura de proveïdor pagareu, en funció dels pagaments al client del projecte. Si decidiu pagar al proveïdor tot i que els termes de PWP no es van complir, podeu substituir els termes de PWP en la pàgina **Factura de proveïdor amb pagament després del cobrament**.

1. Aneu a **Administració de projectes i comptabilitat** \> **Consultes i informes** \> **Consultes de retenció** \> **Factura de proveïdor amb pagament després del cobrament**.
2. A la pàgina **Factures de proveïdor amb pagament després del cobrament**, en el camp de cerca, introduïu valors per trobar la factura de proveïdor que voleu revisar i seleccioneu **Cerca**.
3. Al FastTab **Línies de factura de proveïdor**, seleccioneu les línies que voleu canviar.
4. Si es compleixen les condicions de **Pagament després del cobrament** per a la línia de factura, seleccioneu **Allibera el pagament del proveïdor**. L'opció **Pagament després del cobrament** s'esborra i el valor del camp **A punt per al pagament** canvia a **Sí**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]