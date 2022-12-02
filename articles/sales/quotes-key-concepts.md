---
title: 'Ofertes: conceptes clau'
description: En aquest article s'ofereix informació sobre les ofertes de projectes i ofertes de vendes disponibles al Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c0598b9ec276741f1f62e0cfc1717a3fd622cd7c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912504"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Conceptes únics per a ofertes basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Al Dynamics 365 Project Operations, hi ha dos tipus d'ofertes, de projectes i de vendes. Els dos tipus d'ofertes es diferencien de les maneres següents:

- **Quadrícules per a elements de línia**: en una oferta de vendes, només hi ha una quadrícula per als elements de línia. En una oferta de projecte hi ha dues quadrícules per als elements de línia. Una quadrícula és per a les línies de projecte i l'altra és per a les línies de productes.
- **Activació i revisions**: les ofertes de vendes admeten l'activació i les revisions. Aquests processos no estan admesos en una oferta de projecte.
- **Ofertes adjuntes**: podeu adjuntar diverses comandes a una oferta de vendes. Podeu adjuntar només un contracte de projecte a una oferta de projecte.
- **Guanyar una oferta**: quan guanyeu una oferta de vendes, l'oportunitat relacionada pot romandre oberta. Quan es guanya una oferta de projecte, l'oportunitat relacionada es tanca.
- **Camps i conceptes**: una oferta de vendes no inclou els camps i els conceptes inclosos en una oferta de projecte. Els camps inclouen **Unitat de contractació**, **Administrador de comptes** i **Nom del contacte de la factura**.  
- **Tipus**: les ofertes de vendes i d'ofertes de projectes també s'identifiquen pel camp basat en conjunt d'opcions, **Tipus**. Per a una oferta de vendes, aquest camp té el valor **Basada en un element**. Per a una oferta de projecte, té el valor **Basada en el treball**.

Aquest article es centra en els detalls de les ofertes del projecte.

Una oferta de projecte al Project Operations pot tenir diversos elements de línia o línies d'oferta. De fet, una oferta de projecte té dues quadrícules per als elements de línia. Una quadrícula és per a les línies basades en projectes que permeten estimacions detallades. L'altra quadrícula és per a les línies basades en productes que utilitzen un preu d'unitat senzill i un enfocament basat en la quantitat.

- **Basada en el projecte**: el valor ofert es determina després d'estimar la quantitat de treball necessari. Podeu estimar el treball en un nivell alt i directament com a detalls de la línia a sota de cada línia d'oferta o segons estimacions des de zero, mitjançant un projecte i un pla de projecte. Les línies d'oferta basades en projectes només es troben en ofertes basades en projectes que es creen mitjançant el Project Operations. Aquest tipus de línia d'oferta és una forma personalitzada de les línies d'oferta que hi ha disponibles al Microsoft Dynamics 365 Sales.

- **Basada en un producte**: el valor ofert es determina segons la quantitat d'unitats venudes i el preu de venda de les unitats. El producte d'una línia basada en productes pot provenir d'un catàleg de productes del Sales o pot ser un producte que definiu. Aquest tipus de línia d'oferta també està disponible a les ofertes basades en el projecte que es creen mitjançant el Project Operations.

L'import d'una oferta és el total de totes les línies basades en productes i les línies basades en el projecte.

> [!NOTE]
> Les ofertes i les línies d'oferta no són necessàries al Project Operations. Podeu iniciar el procés del projecte amb un contracte de projecte (projecte venut). No obstant, una oportunitat és sempre necessària, independentment de si comenceu amb una oferta o un contracte de projecte.

## <a name="project-based-quote-lines"></a>Línies d'oferta basades en el projecte

Una línia d'oferta basada en el projecte al Project Operations té els següents mètodes de facturació:

- Temps i material
- Preu fix

### <a name="time-and-material"></a>Temps i material

El mètode de facturació de temps i els materials es basa en el consum. En seleccionar aquest mètode de facturació, es facturarà al client a mesura que el projecte generi costos. Les factures es creen en una freqüència periòdica basada en la data. Durant el procés de vendes, el valor de cotització d'un component de temps i materials només proporciona una estimació del cost final per al client. El proveïdor no es compromet a completar el projecte exactament amb el valor de l'oferta. Els components de temps i materials augmenten el risc del client. És possible que els clients vulguin negociar clàusules de no-superació addicionals per minimitzar-ne el risc. El Project Operations no admet la configuració de les clàusules de no-superació.

### <a name="fixed-price"></a>Preu fix

En el mètode de facturació de preu fix, un venedor es compromet a lliurar el projecte a un cost fix per al client. Es facturarà al client el valor de cotització de la línia d'oferta de preu fix, independentment dels costos que el proveïdor tingui per entregar aquesta línia d'oferta. El valor de la línia d'oferta de preu fix es factura d'una de les maneres següents: 

- Com a quantitat d'import únic a l'inici o al final del projecte o quan s'assoleix un fita de projecte. 
- En una freqüència basada en la data d'un termini igual al valor fix de la línia d'oferta. Aquests terminis es coneixen com a fites periòdiques.
- En terminis que tenen un valor monetari que s'ajusta a la progressió del treball o de les fites específiques que es van aconseguint en el projecte. En aquest cas, el valor de cada termini pot variar, però tots han de sumar-se al valor fixat de la línia d'oferta.

El Project Operations és compatible amb els tres tipus de planificacions de factura per a les línies d'oferta de preu fix.

## <a name="transaction-classification"></a>Classificació de transacció

Normalment, les organitzacions de servei d'atenció al client fan ofertes i facturen els seus clients per classificació de costos. Els costos estan representats per les següents classificacions de transaccions:

- **Temps**: aquesta classificació representa el temps de les despeses del treball o recursos humans en un projecte.
- **Despeses**: aquesta classificació representa tots els altres tipus de despeses d'un projecte. Com que les despeses es poden classificar àmpliament, la majoria d'organitzacions creen subcategories, com ara viatge, lloguer de cotxes, hotel o subministraments d'oficina.
- **Taxa**: aquesta classificació representa diverses sobrecàrregues, sancions i altres elements que es cobren al client. 
- **Impost**: aquesta classificació representa els imports de l'impost que els usuaris afegeixen mentre introdueixen les despeses.
- **Transacció de materials**: aquesta classificació representa els valors reals de les línies de producte en una factura de projecte confirmada.
- **Fita**: aquesta classificació s'utilitza per la lògica de facturació de preu fix.

Una o més d'aquestes classificacions de transacció es poden associar a cada línia d'oferta. Quan es guanya una oferta, es transfereix l'assignació entre la classificació de transaccions i la línia d'oferta a la línia de contracte.
  
Per exemple, pot ser que una oferta contingui les dues línies d'oferta següents: 

- Treball de consultoria amb un mètode de facturació en temps i materials en què s'apliquen classificacions de transaccions de temps i taxes. Per exemple, totes les transaccions de temps i de taxes del projecte d'exemple **Implementació del Dynamics AX** es facturen al client segons el temps i els materials que s'utilitzin. 
- Despeses de desplaçament relacionades que utilitzen un mètode de facturació de preu fix. Per exemple, totes les despeses de desplaçament del projecte d'exemple **Implementació del Dynamics AX** es facturen a un valor monetari fix.

> [!NOTE]
> La combinació de les classificacions de projectes i transaccions **de** temps **,** despeses i **honoraris** que estan associats amb una línia d'oferta o línia de contracte ha de ser única. Si la mateixa combinació de la classe de projecte i transacció està associada amb més d'una línia de contracte o amb una línia d'oferta, el Project Operations no funcionarà correctament.

## <a name="billing-types"></a>Tipus de facturació

El camp **Tipus de facturació** defineix el concepte d'imputabilitat. És un conjunt d'opcions que té els següents valors possibles:

- **Imputable**: el cost que s'ha acumulat en aquesta funció/categoria és un cost directe que impulsa l'execució del projecte i el client pagarà per aquest treball. El pagament es pot administrar en règim de temps i material o fix. No obstant això, l'empleat que gasti aquest temps rebrà el crèdit corresponent pel seu ús facturable.
- **No imputable**: el cost que s'ha acumulat en aquesta funció/categoria es considera un cost directe que impulsa l'execució del projecte, tot i que el client no ho reconeix i no pagarà per aquest treball. L'empleat que gasti aquest temps no rebrà el crèdit d'ús facturable per això.
- **Gratuïta**: el cost que s'ha acumulat en aquesta funció/categoria es considera un cost directe que impulsa l'execució del projecte i el client ho reconeix. L'empleat que gasti aquest temps rebrà el crèdit d'ús facturable per això. No obstant, aquest cost no es cobra al client.
- **No disponible**: les despeses que es generen en projectes interns que no exigeixen un seguiment d'ingrés se segueixen mitjançant aquesta opció.

## <a name="invoice-schedule"></a>Planificació de facturació

Una planificació de facturació és una sèrie de dates en què es realitza una facturació per a un projecte. Opcionalment, podeu crear una planificació de facturació en una línia d'oferta. Cada línia d'oferta pot tenir la seva pròpia planificació de facturació. Per crear una planificació de la facturació, heu d'aportar els valors d'atribut següents:

- Una data d'inici de facturació 
- Data d'entrega que representa la data final de la facturació en el projecte
- Una freqüència de facturació

S'utilitzen aquests tres valors d'atribut per generar un conjunt provisional de dates per establir la facturació.

## <a name="invoice-frequency"></a>Freqüència de facturació

La freqüència de facturació és una entitat que emmagatzema els valors d'atribut que ajuden a expressar la freqüència de creació de factures. Els atributs següents expressen o defineixen l'entitat Freqüència de la factura:

- **Període**: s'admeten períodes mensuals, quinzenals i setmanals. 
- **Execucions per període**: per als períodes setmanals i quinzenals, només es pot definir una execució per període. Per als períodes mensuals, podeu definir entre una i quatre execucions per període. 
- **Dies d'execució**: els dies en què s'ha d'executar la facturació. Podeu configurar aquest atribut de dues maneres:
  - **Feiners**: per exemple, podeu especificar que la facturació s'executi cada dilluns o cada dos dilluns. Els clients que hagin de definir que s'executi la facturació en un dia feiner podrien preferir aquest tipus de configuració. 
  - **Dies de calendari**: per exemple, podeu especificar que la facturació s'executa el setè i el vint-i-unè dia de cada mes. Algunes organitzacions poden preferir aquest tipus de configuració, perquè ajuda a garantir que la facturació s'executa seguint una planificació fixa cada mes.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Planificació de la factura d'una línia d'oferta a un preu fix

Per a una línia d'oferta de preu fix, podeu utilitzar la quadrícula **Planificació de facturació** per crear fites de facturació que equivalen al valor de la línia d'oferta.

- Per crear fites de facturació que estiguin dividits de manera equitativa, seleccioneu una freqüència de facturació, introduïu la data d'inici de la facturació a la línia d'oferta i seleccioneu **Data d'acabament sol·licitada** per a l'oferta a la secció **Resum** de la capçalera de l'oferta. A continuació , seleccioneu **Genera fites periòdiques** per crear fites dividides equitativament en funció de la freqüència seleccionada per a la facturació. 
- Per crear un fita de facturació d'una suma global, creeu una fita i, a continuació, introduïu el valor de la línia d'oferta com a import de la fita.
- Per crear fites de facturació que es basin en tasques específiques del pla del projecte, creeu una fita i assigneu-la a l'element de la programació del projecte a la interfície d'usuari de fita de facturació.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
