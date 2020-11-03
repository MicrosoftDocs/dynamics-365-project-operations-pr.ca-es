---
title: Recuperació de l'IVA
description: En aquest tema s'explica com recuperar reemborsaments en transaccions amb impost sobre el valor afegit (IVA).
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1be96521cdb486dd5a702cded615d3e1015b364
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072254"
---
# <a name="vat-recovery"></a>Recuperació de l'IVA 

[!include [banner](../includes/banner.md)]

Per rebre reemborsament a les operacions amb impost sobre el valor afegit (IVA), una empresa o organització ha d'identificar, recopilar, verificar i enviar informació precisa. Aquest procés inclou diverses tasques i, en funció de la mida de l'empresa, pot incloure diversos empleats o funcions.

Per recuperar l'IVA amb l'administració de despeses, cal completar els requisits previs següents:

- S'han de crear codis d'impostos per als països/regions que s'assignen a les categories de despeses.
- Cal crear un grup de l'impost de vendes per cada codi d'impostos.
- Cal crear un codi d'impost de vendes per cada grup d'impostos de vendes.

Quan s'hagin completat els requisits previs, els empleats segueixen aquests passos per sol·licitar la devolució de les transaccions amb IVA.

1. A l'informe de despeses, introduïu la informació tributària sobre les transaccions amb targeta de crèdit per identificar els possibles reembossaments d'IVA.
2. Assegureu-vos que tota la informació tributària estigui completa i, a continuació, comptabilitzeu l'informe de despeses.
3. Processeu les despeses que compleixin els requisits per a la recuperació de l'IVA internacional.
4. Envieu les dades de recuperació de l'IVA al proveïdor de tercers per poder presentar la devolució internacional.
5. Processeu les despeses per a la recuperació de l'IVA nacional.

A les seccions següents s'ofereixen exemples que mostren com els empleats de Contoso completen cada pas.

## <a name="on-an-expense-report-enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>A l'informe de despeses, introduïu la informació tributària sobre les transaccions amb targeta de crèdit per identificar els possibles reembossaments d'IVA

La Montse, una representant de vendes de Contoso que es troba als Estats Units, ha tornat recentment d'un viatge de vendes al Regne Unit. Durant el viatge, va incórrer en algunes despeses personals de targeta de crèdit per als àpats. La Montse ara ha de crear un informe de despeses per conciliar les despeses.

Quan la Montse introdueix la informació a l'informe de despeses, selecciona **Regne Unit** al camp **País o regió** de la pàgina **Edita l'informe de despeses**. La llista de grups d'impostos de vendes es filtra després per tal que només es mostrin els grups que s'apliquen al Regne Unit. La Montse selecciona el grup d'impostos de vendes **Regne Unit 001** i, a continuació, selecciona el grup d'impostos de vendes de l'element **Àpats**. A continuació, afegeix una nova transacció per a l'allotjament. Com que només hi ha un grup d'impostos de vendes i un element grup de l'impost de vendes per a l'allotjament al Regne Unit, aquesta informació s'emplena automàticament per a l'informe de despeses de la Montse.

Segons la política de Contoso, totes les despeses han de tenir un rebut coincident. Per tant, quan la Montse desa l'informe de despeses, rep un missatge que indica que ha d'adjuntar un justificant per a cada transacció que figuri a l'informe de despeses. La Montse verifica que s'ha adjuntat una imatge digital de cada rebut de transacció a l'informe de despeses i després envia l'informe per a la seva aprovació. A continuació, envia els rebuts en paper a l'equip d'operacions. Aquest equip enviarà les dades de recuperació de l'IVA al proveïdor de tercers que sol·licita la recuperació internacional de l'IVA per a Contoso.

## <a name="make-sure-that-all-tax-information-is-complete-and-then-post-the-expense-report"></a>Assegureu-vos que tota la informació tributària estigui completa i, a continuació, comptabilitzeu l'informe de despeses

L'April, coordinadora del compte a pagar de Contoso, ha d'introduir tota la informació d'impostos que falti d'un informe de despeses abans que es pugui comptabilitzar. Obre la pàgina **Detalls de l'informe de despeses** i veu l'informe de despeses aprovat de la Montse. L'April obre l'informe de despeses per visualitzar els detalls de les transaccions. Veu que la Montse no va introduir un grup d'impost de vendes d'element per a una de les transaccions. Com que aquesta informació no es proporciona, l'April no pot comptabilitzar l'informe de despeses. Per tant, l'April consulta la pàgina **Configuracions d'impostos** a l'administració de despeses i troba el grup d'impostos de vendes de l'element adient per al país o regió i el tipus de transacció. L'April pot comptabilitzar l'informe de despeses al registre general.

Quan l'April comptabilitza l'informe de despeses, es crea un element de treball d'IVA recuperable. Aquest element de treball s'assigna a un membre de l'equip de processament d'operacions. L'April rep un missatge que confirma que la comptabilització s'ha realitzat correctament. Aquest missatge també mostra el nombre de transaccions amb IVA que s'han identificat per a la recuperació.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Processar les despeses que compleixin els requisits per a la recuperació de l'IVA internacional

L'Arnie, membre de l'equip de processament d'operacions de Contoso, és responsable de confirmar que s'inclou la informació necessària per a la recuperació de l'IVA als informes de despeses. Obre la pàgina **Recuperació de l'impost de despeses** i selecciona l'informe de despeses que ha enviat la Montse. A continuació, l'Arnie verifica que s'adjunten tots els rebuts necessaris i que s'han introduït el grup d'impost de vendes i els codis d'impost de vendes de l'article correctes.

Quan l'Arnie rebi rep rebuts en paper de la Montse, verifica els rebuts en paper amb els rebuts digitals i després canvia l'estat de l'informe de despeses a **A punt per a la recuperació**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor-to-file-international-recovery-returns"></a>Envieu les dades de recuperació de l'IVA al proveïdor de tercers per poder presentar la devolució internacional

Quan l'Arnie és a punt per enviar les dades de l'informe de despeses al proveïdor de tercers que presentarà la recuperació de l'IVA, obre la pàgina **Recuperació d'impostos de despeses**. Filtra la pàgina per tal que només mostri els informes de despeses que es marquen com a **A punt per a la recuperació**. A continuació, l'Arnie selecciona **Fitxer** &gt; **Exporta a l'Excel**. La informació de l'IVA dels informes de despeses s'exporta a un full de càlcul del Microsoft Excel. L'Arnie envia aquest full de càlcul al proveïdor de tercers i inclou un missatge que indica que els rebuts en paper s'han enviat per missatger.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Processar les despeses per a la recuperació de l'IVA nacional

L'Arnie ha de comprovar que les transaccions de l'informe de despesa són aptes per a la recuperació de l'IVA i que els rebuts digitals s'adjunten als informes. Per començar a processar les despeses elegibles per a la recuperació nacional, l'Arnie obre la pàgina **Recuperació d'impostos de despeses** i selecciona l'informe de despeses que requereix la verificació. Verifica que els rebuts estan en nom de l'empresa en comptes de l'empleat. Per a la recuperació de l'IVA, els ingressos han d'estar en nom de l'empresa. L'Arnie confirma que s'han aplicat el grup d'impostos de vendes i els codis d'impostos de vendes d'articles correctes.

Quan l'Arnie rep els rebuts en paper, canvia l'estat de l'informe de despeses a **A punt per a la recuperació**. A continuació, pot presentar la devolució a l'autoritat tributària adequada. En aquest cas, l'autoritat fiscal adequada als Estats Units és el Servei d'ingressos interns (IRS).