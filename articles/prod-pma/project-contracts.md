---
title: Contractes del projecte
description: En aquest tema es proporcionen exemples dels contractes del projecte que podeu crear per a diversos tipus de projectes i fonts de finançament, i com podeu administrar els contractes i facturar els clients del projecte.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b92668c38071e8b1afdee9a79fd4a25190248ada30380bfb79054a6dc587f95
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001014"
---
# <a name="project-contracts"></a>Contractes del projecte

[!include [banner](../includes/banner.md)]

En aquest article es proporcionen exemples dels contractes del projecte que podeu crear per a diversos tipus de projectes i fonts de finançament, i com podeu administrar els contractes i facturar els clients del projecte.

El tipus de projecte que es crea per a un contracte de projecte determina el mètode que s'utilitza per facturar els clients del projecte. Podeu canviar un contracte de projecte i el projecte relacionat, però no podeu canviar el tipus de projecte. 

En utilitzar un contracte de projecte, podeu facturar un o més projectes al mateix temps. El contracte de projecte també us ajuda a garantir un procediment de facturació coherent per a cada subprojecte en una estructura de projecte. 

Cada projecte que s'ha de facturar ha d'estar associat amb un contracte de projecte. La configuració d'un contracte de projecte s'aplica a tots els projectes i subprojectes associats amb el contracte del projecte. 

Un contracte de projecte pot especificar una o diverses fonts de finançament. Per tant, podeu dividir la facturació entre diversos finançadors, configurar límits de finançament per tal que les fonts de finançament no es facturin en més d'una quantitat especificada i configurar regles de finançament per a la càrrega de despeses.

## <a name="funding-for-project-contracts"></a>Finançament per a contractes de projectes
Alguns contractes de projecte especifiquen que diverses parts comparteixen la responsabilitat de finançar els costos del projecte. A continuació trobareu alguns exemples:

-   Un client gran que té diverses divisions sol·licita que el finançament d'un projecte es divideixi.
-   La vostra empresa comparteix els costos d'un projecte gran amb una organització externa.
-   Un projecte de carretera està cofinançat per dos municipis.
-   Un projecte de pont està finançat per una subvenció governamental i una corporació privada.

Al Dynamics 365 Finance, podeu dividir la facturació d'una única transacció o d'un projecte sencer entre diversos clients, subvencions o organitzacions. 

En projectes que tinguin diversos finançadors, totes les parts que contribueixin al finançament d'un projecte de finançament avançat s'anomenen fonts de finançament. Després que un client, una organització o una subvenció es defineixi com a font de finançament, es pot assignar a una o diverses regles de finançament. Les regles de finançament contenen els criteris que determinen la manera com es destinen els càrrecs a les diverses fonts de finançament d'un projecte. 

Com que els articles en estoc, com els que apareixen a les requisicions de compra i les comandes de compra, no es poden dividir, l'import del cost no es pot dividir entre diverses fonts de finançament a l'hora de la distribució. Per tant, el valor de la font de finançament segueix sent 0 (zero) fins que es comptabilitzi l'inventari. Quan es comptabilitzi l'inventari, l'import de la despesa es distribueix segons les regles de distribució del compte per al projecte.

A continuació, us indiquem alguns passos que podeu dur a terme per fer més fàcil la divisió de la facturació entre diverses fonts de finançament:

-   Especifiqueu que totes les transaccions que s'introdueixen per a un projecte utilitzin la mateixa moneda de vendes en el contracte del projecte.
-   Configureu els límits de finançament, de manera que no es facturi cap font de finançament més d'un import especificat en un projecte.
-   Configureu les regles de finançament i els límits de finançament de cada treballador, article, categoria, grup de categories i tipus de transacció (o per a tots els tipus de transaccions).
-   Seleccioneu dates d'inici i d'acabament opcionals per definir el període en què cada regla de finançament és vàlida.
-   Especifiqueu el percentatge del qual és responsable cada font de finançament.
-   Especifiqueu quina font de finançament s'encarrega de les diferències d'arrodoniment causades pels càlculs d'assignació de finançament.
-   Configureu regles que determinin com els costos de projecte es facturen a clients externs i es carreguen a organitzacions internes.
-   Registreu les transaccions en un compte de finançament de retenció fins que es pugui obtenir finançament addicional o fins que decidiu suportar les despeses internament.

Per determinar quin grup d'impostos s'ha d'associar amb una transacció, se cerca una assignació de grup d'impostos al projecte. Si no s'ha fet cap assignació de grup d'impostos en el mateix nivell de projecte, se cerca en el contracte del projecte.

### <a name="example-multiple-funding-sources-simple"></a>Exemple: diverses fonts de finançament (simple)

A la taula següent es proporcionen escenaris per administrar l'assignació de finançament entre diverses fonts de finançament. Aquests escenaris es basen en els següents supòsits:

-   La configuració de prioritat s'ha traduït a l'assignació de fons abans que s'apliquin altres criteris de regla de finançament.
-   No s'ha especificat cap interval de dates per definir el període quan la regla de finançament és vàlida.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Escenari</strong></td>
<td><strong>Font de finançament</strong></td>
<td><strong>Percentatge d'assignació</strong></td>
<td><strong>Prioritat d'assignació</strong></td>
</tr>
<tr class="even">
<td>Voleu assignar costos a una font de finançament fins que s'esgotin els seus recursos, assignar costos a una segona font de finançament fins que s'esgotin els seus diners i, finalment, assignar els costos restants a una tercera font de finançament.</td>
<td><ul>
<li>Font de finançament 1</li>
<li>Font de finançament 2</li>
<li>Font de finançament 3</li>
</ul></td>
<td><ul>
<li>100 %</li>
<li>100 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Voleu assignar el 75 per cent dels costos a una font de finançament i el 25 per cent a una segona font de finançament. Quan alguna d'aquestes fonts de finançament s'esgoti, voleu pagar els costos restants amb una tercera font de finançament.</td>
<td><ul>
<li>Font de finançament 1</li>
<li>Font de finançament 2</li>
<li>Font de finançament 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Voleu assignar el 75 per cent dels costos a una font de finançament i el 25 per cent a una segona font de finançament. Quan alguna d'aquestes fonts de finançament s'esgoti, voleu dividir els costos restants entre una tercera font de finançament i una quarta.</td>
<td><ul>
<li>Font de finançament 1</li>
<li>Font de finançament 2</li>
<li>Font de finançament 3</li>
<li>Font de finançament 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Voleu assignar el primer 25 per cent dels costos a una font de finançament i la resta a una segona font de finançament.</td>
<td><ul>
<li>Font de finançament 1</li>
<li>Font de finançament 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemple: diverses fonts de finançament (complex)

Teniu tres fonts de finançament que voleu utilitzar en l'ordre següent:

1.  Utilitzar la font de finançament 2 i la font de finançament 3 per igual fins que la font de finançament 2 estigui esgotada.
2.  Continuar utilitzant la font de finançament 3 fins que s'esgoti.
3.  Utilitzar la font de finançament 1 després que s'esgoti la font de finançament 3.

Per aconseguir aquest objectiu, heu de fer el següent:

-   Configureu els límits de finançament per a la font de finançament 2 i la font de finançament 3, per a les seves quantitats respectives.
-   Creeu les regles de finançament següents:
    -   Regla 1 (prioritat 1): assigneu un 50 per cent de les transaccions a la font de finançament 2 i un 50 per cent a la font de finançament 3.
    -   Regla 2 (prioritat 2): assigneu un 100 per cent de les transaccions a la font de finançament 3.
    -   Regla 3 (prioritat 3): assigneu un 100 per cent de les transaccions a la font de finançament 1.

Aquesta configuració funciona perquè les transaccions es comproven amb les regles i els límits per determinar si s'apliquen a la transacció. Si no s'aplica cap norma o límit específic a la transacció, la regla Totes les transaccions s'aplicarà. La regla Totes les transaccions coincideix amb totes les transaccions. 

Si es troba una regla que coincideix amb una transacció, primer s'aplica el percentatge que s'ha assignat en aquesta regla, però només quan es comproven les coincidències amb qualsevol límit que s'hagi configurat. Si s'ha complert un límit i s'han esgotat els fons de la font de finançament, la regla de finançament associada amb el límit de finançament s'ignora i el programa comprova la següent regla que s'aplica. 

En alguns casos, només es pot assignar una part d'una transacció en virtut d'una regla. Això podria passar perquè el límit s'ha assolit quan s'ha assignat la transacció. En aquest cas, només s'assigna un import determinat segons aquesta regla, com ara el 50 per cent a cada font de finançament. Aquest és el cas de la regla 1, que es descriu abans en aquesta secció. La resta s'assigna d'acord amb la regla següent a la seqüència. 

A la taula següent s'examina més detalladament aquest escenari.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Focus</strong></td>
<td><strong>Detalls</strong></td>
</tr>
<tr class="even">
<td>Regles de finançament</td>
<td><ul>
<li>Regla 1 (prioritat 1): totes les transaccions. Assigna la font de finançament 2 al 50 % i la font de finançament 3 al 50 %.</li>
<li>Regla 2 (prioritat 2): totes les transaccions. Assigna la font de finançament 3 al 100 %.</li>
<li>Regla 3 (prioritat 2): totes les transaccions. Assigna la font de finançament 1 al 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Límits de finançament</td>
<td><ul>
<li>Límit de la font de finançament 1 = 10.000,00</li>
<li>Límit de la font de finançament 2 = 500,00</li>
<li>Límit de la font de finançament 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transacció 1</td>
<td><strong>Import de la transacció:</strong> 100,00<strong>Finançament:</strong> la transacció es paga només segons la regla 1, perquè l'operació s'abona íntegrament després que s'apliqui la regla 1. La transacció es finança equitativament entre la font de finançament 2 i la font de finançament 3.
<ul>
<li>Font de finançament 2: 50,00</li>
<li>Font de finançament 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transacció 2</td>
<td><strong>Import de la transacció:</strong> 5.000,00<strong>Finançament:</strong> la transacció es paga segons les tres regles. <strong>Regla 1</strong>
<ul>
<li>Font de finançament 2: 450,00</li>
<li>Font de finançament 3: 450,00</li>
</ul>
<strong>Regla 2</strong>
<ul>
<li>Font de finançament 3: 250,00 (= 750,00 - 50,00 - 450,00)</li>
</ul>
<strong>Regla 3</strong>
<ul>
<li>Font de finançament 1: 3.850,00 (= 5.000,00 - 450,00 - 450,00 - 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total de fons que es distribueixen per a cada font de finançament</td>
<td><ul>
<li>Font de finançament 1: 3.850,00</li>
<li>Font de finançament 2: 500,00</li>
<li>Font de finançament 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Regles de facturació
Quan negocieu un contracte de projecte amb un client, heu de definir com i quan podeu facturar el client per treballar en un projecte. Després de configurar el contracte del projecte i el projecte, podeu configurar les regles de facturació del projecte. Les regles de facturació es basen en les condicions del projecte que s'especifiquen al contracte del projecte. Les regles de facturació que creeu depenen de les condicions del contracte del projecte i del tipus de projecte, com ara temps i material o de preu fix, que associeu amb la regla de facturació. Podeu crear més d'una regla de facturació per a un contracte de projecte. També podeu assignar una regla de facturació a diversos projectes associats amb el mateix contracte de projecte i tenir termes de facturació similars. 

Podeu configurar els tipus següents de regles de facturació:

-   **Unitat de lliurament**: factureu un client quan completeu una unitat de lliurament. Definiu les unitats de lliurament al contracte.
-   **Progrés**: factureu un client quan completeu un percentatge especificat del projecte. Podeu configurar una regla de facturació per calcular automàticament el percentatge de treball completat, o podeu calcular manualment el percentatge de treball completat i l'import per facturar al client.
-   **Fita**: factureu un client l'import total d'un fita de projecte quan s'assoleixi la fita.
-   **Taxa**: factureu un client pels vostres serveis, a més d'una taxa d'administració, que sol ser un percentatge del cost dels serveis.
-   **Temps i material**: factureu un client pel valor del temps i els materials que s'utilitzen en un projecte.

Per a tots els tipus de regles de facturació, podeu especificar un percentatge de retenció que es dedueix de les factures del client fins que un projecte arribi a una fase consensuada. El percentatge de retenció de pagament s'especifica al contracte del projecte. L'import es calcula i es resta en funció del valor total de les línies d'una factura de client. 

Per a les regles de facturació **Temps i de materials** i **Progrés**, podeu assignar categories imputables. Les categories imputables indiquen les transaccions que s'han d'incloure a les factures de client. 

Quan estigueu a punt per facturar el client, l'import de la factura del projecte es calcula segons les regles de facturació i es genera una proposta de factura de projecte. 

A les seccions següents s'ofereixen exemples que mostren la configuració i l'administració de les regles de facturació d'un projecte.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemple: crear una regla de facturació basada en el nombre d'unitats entregades

La vostra organització entra en un acord per proporcionar un total de cinc sessions formatives als empleats d'un client amb un cost de 10.000 USD per sessió formativa. Factureu al client després de cada sessió formativa. 

Quan configureu les regles de facturació per al contracte, s'utilitzen els valors següents:

-   La unitat de lliurament és una sessió formativa.
-   El preu unitari és de 10.000 per sessió formativa.
-   El nombre total d'unitats és de cinc sessions formatives.

Quan hàgiu completat una sessió formativa, podeu crear una factura de 10.000, per a la primera unitat que s'ha lliurat i enviar la factura al client.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemple: crear una regla de facturació basada en un percentatge especificat de finalització del projecte (càlcul manual)

La vostra organització, una firma de consultoria de programari, entra en un acord amb un client per desenvolupar part d'un producte que el client està desenvolupant. L'organització accepta el lliurament del codi de programari durant un període de sis mesos. El client es compromet a pagar a la vostra organització un total de 100.000 pel treball. Creeu una regla de facturació per facturar al client en funció del percentatge de treball que s'hagi completat al projecte, tal com s'especifica al contracte.

-   Al final del primer mes, us trobeu amb el client per determinar el percentatge de feina completada. Després de revisar el projecte amb el client, decidiu que el projecte s'ha completat un 15 per cent.
-   Es crea una factura per a 15.000 (15 per cent de 100.000) i s'envia al client.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemple: crear una regla de facturació basada en un percentatge especificat de finalització del projecte (càlcul automàtic)

La vostra organització, una firma de desenvolupament de programari, accepta desenvolupar un paquet de comptabilitat de nòmines d'un client per 30.000. El client es compromet a pagar a la vostra organització en funció del percentatge de feina completada. Estimeu que els costos del projecte són 20.000. El contracte del projecte especifica les categories de treball que utilitzeu en el procés de facturació. Configureu regles de facturació que calculen automàticament els imports de la factura per al percentatge de treball que s'ha completat per a cada categoria. Configureu un pressupost per a cada categoria:

-   **Desenvolupament**: cost de 15.000 i ingressos de 20.000
-   **Instal·lació**: cost de 5.000 i ingressos de 10.000

Quan creeu una factura del client per primer cop, l'import de la factura es calcula automàticament segons la informació següent:

-   Després d'un mes, el treballador del projecte envia un full d'hores per al projecte. El cost de les hores del treballador és de 5.000 per al desenvolupament i 1.000 per a la instal·lació. El treball de desenvolupament està completat en un 33 per cent (5.000 cost real/15.000 cost pressupostat), i el treball d'instal lació està completat en un 20 per cent (1.000 cost real/5.000 cost pressupostat).
-   El import de la factura de 8.667 es calcula automàticament (33 per cent de 20.000 + 20 per cent de 10.000).
-   Es crea una factura per 8.667 i s'envia al client.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemple: crear una regla de facturació basada en les fites acordades

La vostra organització, una consultora de gestió, accepta dur a terme una investigació de mercat per a un producte de consum que el client té previst vendre. El client es compromet a utilitzar els vostres serveis durant un període de tres mesos, començant pel març, i es compromet a pagar 50.000 a la vostra seva organització. El projecte té tres fites:

-   Fita 1: recopilar dades dels consumidors, 31 de març
-   Fita 2: analitzar les dades dels consumidors, 30 d'abril
-   Fita 3: presentar una proposta de viabilitat del producte, 31 de maig

El client es compromet a pagar a la vostra organització 10.000 per la primera fita, 20.000 per la segona fita i 20.000 per la tercera fita. 

Quan configureu el contracte del projecte, accepteu que factureu al client segons la fita que s'hagi completat. La configuració de la regla de facturació inclou els passos següents:

-   Definir les fites del projecte.
-   Definir l'import per facturar al client quan s'hagi completat cada fita.

Quan la primera fita es completa el 31 de març, es marca la fita com a completada i, a continuació, es crea una factura per 10.000 i s'envia al client. No podeu crear una factura per a una fita fins que no hàgiu marcat la fita com a completada.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemple: crear una regla de facturació basada en els serveis més una taxa d'administració

La vostra organització, una consultora de gestió, accepta dur a terme una investigació de mercat per avaluar la viabilitat d'un producte que el client, una empresa minorista, està desenvolupant. Els termes de l'acord especifiquen que proporcioneu els serveis dels tres principals consultors d'administració, els quals dirigeixen la recerca segons temps i materials. El client acorda pagar 100 per hora, a més d'una taxa d'administració del 10 per cent per a les hores de consultoria que es carregaran en el projecte. 

Quan configureu el contracte del projecte, creeu una regla de facturació per afegir una taxa d'administració del 10 per cent a les hores de consultoria que es carregaran al projecte. 

Quan creeu una factura per al client, es factura al client un 10 per cent de taxa d'administració i el cost de les hores de consultoria. Per exemple, si els tres consultors han treballat un total de 200 hores en el projecte, es crea una factura de 22.000 segons el càlcul següent:

-   200 hores a 100 per hora = 20.000
-   Taxa d'administració del 10 per cent = 2.000
-   Import total de la factura = 22.000

Si les taxes estan imposades a un client i seleccioneu un grup d'impostos de vendes al contracte del projecte, el grup d'impostos de vendes s'introdueix automàticament en una regla de facturació per a les taxes.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemple: crear una regla de facturació per al valor del temps i els materials

La vostra organització, una consultora de programari, accepta proporcionar cinc consultors tècnics per treballar en un projecte de desenvolupament de programari per a un client durant els pròxims sis mesos. El client es compromet a pagar 150 per cada hora de consultoria, a més del cost dels subministraments de l'oficina. La vostra organització envia una factura al client al final de cada mes. 

Quan configureu el contracte del projecte, accepteu facturar al client cada mes pel temps i els materials del projecte. Creeu una regla de facturació que inclou la següent informació:

-   El període del contracte és de sis mesos.
-   El temps de consulta es calcula a una relació de 150 per hora.
-   Els subministraments d'oficina es facturen a un cost i el cost total del projecte no pot superar els 10.000.
-   Creeu una factura del client al final de cada mes natural durant el projecte.

Durant el primer mes, es registren un total de 800 hores pels consultors del projecte. El cost dels subministraments d'oficina que es carrega en el projecte és de 2.000. Per tant, al final del mes, es crea una factura de 122.000, que es calcula com a 800 hores a 150 per hora, més 2.000 per subministraments d'oficina.





[!INCLUDE[footer-include](../includes/footer-banner.md)]