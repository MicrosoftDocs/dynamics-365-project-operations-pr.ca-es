---
title: Informació general sobre l'administració de projectes i la comptabilitat
description: La funcionalitat d'administració de projectes i comptabilitat pot utilitzar-se en diversos sectors per oferir un servei, produir un producte o aconseguir un resultat.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 79e12f39589f9cf3f4b1515fa3ab10bb10ffb97f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749510"
---
# <a name="project-management-and-accounting-overview"></a>Informació general sobre l'administració de projectes i la comptabilitat

[!include [banner](../includes/banner.md)]

La funcionalitat d'administració de projectes i comptabilitat pot utilitzar-se en diversos sectors per oferir un servei, produir un producte o aconseguir un resultat.  

Un projecte és un conjunt d'activitats dissenyades per oferir un servei, produir un producte o aconseguir un resultat. Els projectes consumeixen recursos i generen resultats financers en forma d'ingressos o actius.

## <a name="projects-across-industries"></a>Projectes entre sectors
La funcionalitat d'administració de projectes i comptabilitat es pot utilitzar en diversos sectors, com es mostra a la il·lustració següent.

[![Projectes entre sectors](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

En un centre de trucades, es pot utilitzar un cas per descriure el conjunt d'accions que cal dur a terme per resoldre una trucada. Les empreses de consultoria, com ara les organitzacions de gestió o de consultoria tècnica o agències de publicitat, fan referència a les seves activitats com a projectes. En màrqueting, una campanya representa un conjunt de treballs que s'han de lliurar. En la fabricació basada en projectes, una comanda de producció relaciona la feina que cal dur a terme per produir un producte acabat. Sigui com sigui, aquests projectes inclouen recursos, planificacions i costos, i la funcionalitat d'administració de projectes i comptabilitat pot ajudar en la planificació, l'execució i l'anàlisi d'aquests projectes.

## <a name="project-phases"></a>Fases del projecte
Tot i que el flux del procés següent està dirigit a projectes externs, o a un projecte que s'ha completat per a un o més clients, la funcionalitat també s'aplica a projectes interns i només de cost. 

![Les 3 fases d'un projecte](./media/3-stages-of-a-project.png) 

Com es mostra a la il·lustració precedent, l'administració de projectes i la comptabilitat es poden dividir en tres fases:

1.  Inicia
2.  Executa
3.  Analitza

## <a name="initiate-the-project"></a>Iniciar el projecte
Durant l'inici d'un projecte, es produeixen diversos processos clau. Podeu utilitzar un pressupost de projecte per comunicar el treball, les despeses i els materials previstos al client. Podeu registrar els terminis de facturació, els límits i els acords en un contracte de projecte. Podeu utilitzar una estructura del desglossament del treball (WBS) per planificar i estimar la feina. Podeu configurar previsions i pressupostos per guiar l'execució del projecte. A la il·lustració següent es mostra l'estructura d'un projecte.[![estructura d'un projecte](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Creació d'ofertes del projecte

En la fase de vendes inicial d'un projecte, un pressupost del projecte permet oferir a un client una oferta no vinculant. Un pressupost pot incloure elements com ara els articles i els serveis facturats, la informació bàsica de contacte, acords especials de comerç i descomptes i els possibles impostos i sobrecàrrecs.

També podeu trametre una carta de garantia per a una transacció de pressupost d'un projecte entre l'organització i el client. Un cop creat el pressupost del projecte, podeu crear la sol·licitud de carta de garanties del client i enviar-la al banc. Quan el banc hagi aprovat la sol·licitud, es tramet la carta de garantia al client. 

Per obtenir més informació, vegeu [Pressupostos de projecte](project-quotations.md).

### <a name="create-project-contracts"></a>Creació de contractes del projecte

Quan us involucreu en un contracte amb un client o una altra font de finançament per completar un projecte, primer heu de crear un contracte de projecte. A continuació, quan creeu el projecte, l'heu d'assignar al contracte corresponent. El tipus de projecte que es crea per a un contracte de projecte determina el mètode que s'utilitza per facturar els clients del projecte. Podeu modificar un contracte de projecte i el projecte relacionat, però no podeu canviar el tipus de projecte. Per obtenir més informació sobre els tipus de projecte, vegeu la secció "Creació de projectes".

Per obtenir més informació sobre els contractes del projecte, vegeu [Contractes de projecte](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Creació d'estructures del desglossament del treball

El grau de detall d'una WBS depèn del nivell de precisió necessari a les estimacions i el nivell de seguiment que es requereixi per a aquestes estimacions. Els projectes que tenen molt poca tolerància als canvis de terminis o cost solen requerir una WBS més detallada i també requereixen un seguiment diligent del progrés del treball i el cost en relació amb la WBS. 

Per obtenir més informació, vegeu [Informació general de les estructures del desglossament del treball](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Creació de previsions i pressupostos del projecte

Podeu utilitzar les previsions del projecte si l'organització té una perspectiva operativa i se centra en els ingressos i els costos derivats de transaccions específiques. Tanmateix, podeu utilitzar els pressupostos de projecte si l'organització està més centrada en els imports financers. Cada mètode té els seus avantatges. Per obtenir més informació, vegeu [Previsions i pressupostos de projectes](project-forecasts-budgets.md).

### <a name="create-projects"></a>Creació de projectes

Podeu crear sis tipus de projectes al Finance. Cada tipus de projecte es configura de manera diferent per al reconeixement de costos i ingressos. El tipus de projecte que trieu depèn de la finalitat del projecte. A la taula següent es descriu l'ús típic de cada tipus de projecte.
                                                                                                            
<table>
  <tr>
    <td>Tipus de projecte</th>
    <td>Descripció</th>
  </tr>
  <tr>
    <td>Temps i material</td>
    <td>En els projectes de temps i materials, el client es factura per totes les despeses que s'han ocasionat en un projecte. Aquests costos inclouen costos per hores, despeses, articles i honoraris.</td>
  </tr>
  <tr>
    <td>Preu fix</td>
    <td>En projectes de preu fix, les factures consisteixen en transaccions en comptes. Un projecte de preu fix es facturarà segons una planificació de facturació basada en un contracte de projecte. Els ingressos per a un projecte de preu fix es poden calcular i comptabilitzar durant el projecte mitjançant el mètode percentual completat. Alternativament, els ingressos es poden calcular i comptabilitzar quan el projecte s'hagi completat, mitjançant el mètode de contracte completat. Moltes vegades, les empreses poden beneficiar-se de l'ús del valor del treball en curs (WIP) per calcular el grau de finalització d'un projecte o d'un grup de projectes.</td>
  </tr>
  <tr>
    <td>Inversió</td>
    <td>Els projectes d'inversió són projectes que no produeixen ingressos immediats. Normalment s'utilitzen per a projectes interns de llarg termini on els costos s'han de capitalitzar. Només es poden registrar costos per a articles, hores i despeses per a un projecte d'inversió. Els costos d'un projecte d'inversió se segueixen i controlen mitjançant la funcionalitat d'estimació. Els projectes d'inversió poden configurar-se amb una capitalització màxima opcional. A mesura que avança un projecte d'inversió, podeu registrar els costos en comptes de treball en crus, on es retenen els costos fins que es completa el projecte. Quan el projecte s'elimina, transferiu el valor del treball en curs a un actiu fix, un compte del llibre major o un projecte nou. <br></br> <strong>NOTA:</strong> les transaccions dels projectes d'inversió no es mostren a la pàgina <strong>Comptabilitza els costos<strong>, <strong>Acumula els ingressos</strong> ni <strong>Crea propostes de factura</strong>.</td>
  </tr>
  <tr>
    <td>Projecte de cost</td>
    <td>Com els projectes d'inversió, els projectes de cost normalment s'utilitzen per fer el seguiment dels projectes interns i només poden registrar-se hores, despeses i articles. No obstant això, els projectes de cost solen tenir una duració més curta que els projectes d'inversió. A diferència dels projectes d'inversió, els projectes de cost no es poden capitalitzar en comptes de balanç. En lloc d'això, les transaccions del projecte es comptabilitzen només als comptes de resultats i de pèrdues. <br></br> <strong>NOTA:</strong> les transaccions dels projectes de cost no es reflecteixen a la pàgina <strong>Comptabilitza els costos</strong>, <strong>Acumula els ingressos</strong> ni <strong>Crea propostes de factura</strong>. Com que els projectes de cost normalment s'utilitzen per fer el seguiment de projectes interns, normalment no s'han d'associar amb un compte de client. No obstant, si la configuració requereix que es creïn requisits d'articles per a les comandes de compra, heu d'associar el projecte de cost amb un client. Aquesta associació és obligatòria, ja que els requisits d'articles es gestionen com a comandes de vendes i el sistema requereix que s'especifiqui un client. Tanmateix, aquesta configuració no farà que els requisits dels elements es creïn automàticament a partir d'una comanda de compra. Per als projectes de cost, l'opció <strong>Crea un requisit d'article</strong> s'ignora. Si necessiteu un requisit d'article en un projecte de cost, podeu crear-lo manualment, sempre que un client estigui associat amb el projecte.</td>
  </tr>
  <tr>
    <td>Intern</td>
    <td>Els projectes interns s'utilitzen per fer el seguiment dels costos d'un projecte intern a la vostra organització. Els projectes interns poden proporcionar una eina de planificació per administrar el consum de recursos. <br></br><strong>NOTA<strong>: les transaccions dels projectes interns no es reflecteixen a la pàgina <strong>Comptabilitza els costos</strong>, ni <strong>Crea propostes de factura</strong>.</td>
  </tr>
  <tr>
    <td>Hora</td>
    <td>S'utilitzen els projectes de temps per fer el seguiment del temps que s'associa amb activitats no imputables i no productives, com ara un projecte per fer el seguiment del temps de malaltia dels treballadors. Les transaccions en els projectes de temps no es comptabilitzen al llibre major. En lloc d'això, s'inclouen als informes d'ús dels treballadors. Només es poden registrar transaccions d'hores en projectes de temps. Podeu utilitzar una diari d'hores o un full d'hores per registrar aquestes hores al projecte. Després d'haver registrat les hores, apareixen com a transaccions del projecte, però no disposen d'operacions de vals corresponents. <br></br><strong>NOTA:</strong> les transaccions dels projectes de temps no es reflecteixen a la pàgina <strong>Comptabilitza els costos</strong>, <strong>Acumula els ingressos</strong> ni <strong>Crea propostes de factura</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Assignació de treballadors, categories i recursos

Podeu planificar recursos de treballador en funció dels requisits i la planificació d'un projecte o bé en les aptituds i la disponibilitat dels treballadors. Mitjançant les capacitats de planificació de recursos, podeu distribuir els treballadors de l'organització de manera eficient i eficaç. Podeu trobar ràpidament els treballadors més qualificats que estan disponibles per treballar en el vostre projecte. També podeu veure fàcilment com es poden utilitzar els treballadors de manera més eficaç en el transcurs del projecte. 

A continuació, us indiquem algunes de les maneres com podeu utilitzar la funcionalitat de planificació de recursos:

-   Utilitzar informació sobre els atributs d'un treballador, com ara la formació, aptituds, certificacions i experiència del projecte, per fer coincidir el treballador amb els requisits d'un projecte.
-   Utilitzar informació sobre el calendari i la disponibilitat d'un treballador per adaptar l'horari del treballador al calendari del projecte.
-   Revisar la capacitat de cada treballador i determinar com s'utilitza aquesta capacitat. Per exemple, si un treballador s'està infrautilitzat, el treballador es pot assignar a un projecte que s'ajusti a la seva disponibilitat i atributs.
-   Reviseu la disponibilitat d'un treballador per assegurar-vos que no hi hagi cap conflicte de calendari amb les assignacions del treballador.
-   Reviseu la informació sobre la utilització d'un treballador en una visualització de resum (per exemple, per departament o per treballador) o en una visualització detallada (per exemple, pels treballadors d'un departament o per detalls setmanals de cada treballador).
-   Modificar les assignacions de recursos per a diverses unitats de temps, com ara dies, setmanes o mesos, per optimitzar la manera com s'utilitzen els treballadors.

## <a name="execute-the-project"></a>Executar el projecte
Durant l'execució del projecte, els membres de l'equip o els caps registren el treball i les despeses que s'han incorregut, mitjançant l'ús de fulls d'hores, informes de despeses i altres documents empresarials. Els administradors de projectes disposen d'eines que permeten fer el seguiment del consum de quantitats pressupostades per al projecte. Els administradors de projectes també poden ordenar, triar o adquirir materials per a projectes mitjançant comandes de compra i altres documents empresarials. Es preparen i aproven factures de manera que els clients puguin facturar el treball en curs. Finalment, els ingressos es reconeixen durant aquest procés per afectar les finances de l'organització.

### <a name="manage-work-breakdown-structures"></a>Administrar estructures del desglossament del treball

Una WBS és una descripció del treball que es completarà per a un projecte. Una WBS és una jerarquia de tasques. Representa no només el treball de cada tasca, sinó també la mida, el cost i la duració de la tasca. 

Per obtenir més informació, vegeu [Informació general de les estructures del desglossament del treball](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Administració de previsions i pressupostos del projecte

Hi ha dues maneres d'administrar i controlar els vostres projectes: previsions de projecte i pressupostos de projecte. Podeu utilitzar les previsions del projecte si l'organització té una perspectiva operativa i se centra en els ingressos i els costos derivats de transaccions específiques. Tanmateix, podeu utilitzar els pressupostos de projecte si l'organització està més centrada en els imports financers.

Per obtenir més informació, vegeu [Previsions i pressupostos de projectes](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Crear comandes de producció

Una comanda de producció relacionada amb el projecte pot enllaçar-se amb una comanda de vendes o un requisit d'articles mitjançant el mètode d'article acabat o el mètode d'article consumit. A més, si la comanda de producció es crea manualment, no hi ha cap enllaç entre la comanda de producció i la comanda de vendes o requisit d'article (cap enllaç a la comanda). No obstant, si la comanda de producció es crea automàticament per complir una comanda de venda o un requisit d'articles, hi ha un enllaç entre la comanda de producció i la comanda de venda o el requisit d'articles (enllaç a la comanda). 

En funció de les combinacions d'aquests factors, feu servir un dels mètodes següents:

- **Article acabat/enllaç a la comanda**: enllaça el projecte a una comanda de venda o un requisit d'article. Quan utilitzeu aquest mètode, els costos reals del projecte es comptabilitzaran quan la comanda de venda es facturi o quan s'actualitzi l'albarà per al requisit d'article. El cost es comptabilitza com a article acabat.
- **Article acabat/sense enllaç a la comanda**: els costos reals no es poden comptabilitzar fins que el cicle de producció d'un article tingui l'estat **Finalitzat**. El cost per a l'article acabat es comptabilitza com una única transacció.
- **Article consumit/enllaç a la comanda**: enllaça el projecte a un requisit d'article. Mitjançant aquest mètode, podeu visualitzar els costos reals del projecte quan la producció té l'estat **Iniciat** o s'informa com a finalitzada. Els costos es comptabilitzen com a diverses operacions d'article de projecte per a matèries primeres i hores consumides per a la producció. Quan s'actualitza l'albarà per al requisit d'article, no es comptabilitzen els costos del projecte. També podeu definir el nivell en la jerarquia de facturació de materials (BOM) segons la qual es fa el seguiment dels projectes en la producció.
- *<strong><em>Article consumit/sense enllaç a la comanda</em></strong>*: enllaça el projecte a un requisit d'article. Mitjançant aquest mètode, podeu visualitzar els costos reals del projecte quan la producció té l'estat <strong>Iniciat</strong> o s'informa com a finalitzada. Els costos es comptabilitzen com a diverses operacions d'article de projecte per a matèries primeres i hores consumides per a la producció. També podeu definir el nivell en la jerarquia (BOM) segons la qual es fa el seguiment dels projectes en la producció.

### <a name="procure-products-and-services"></a>Compra de productes i serveis

La compra i venda d'articles són activitats prevalents en moltes empreses centrades en projectes.

#### <a name="purchase-orders-for-projects"></a>Comandes de compra per a projectes

La finalitat de la comanda de compra determina quan es consumeix la comanda de compra i, per tant, quan es consumeixen i carregaran els articles en un projecte.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Mètode</th>
<th>Finalitat</th>
<th>Consum d'articles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Crear una ordre de compra directament.</td>
<td>Comprar articles d'un proveïdor extern per al consum en un projecte. Podeu crear la comanda de compra de les maneres següents:
<ul>
<li>Des del projecte en si mateix. En aquest cas, el projecte ja s'ha definit per a la comanda de compra.</li>
<li>Navegant a la comanda de compra del projecte. Heu de seleccionar el proveïdor i el projecte per als quals crear la comanda de compra.</li>
</ul></td>
<td>Els articles es consumeixen en actualitzar la factura del proveïdor.</td>
</tr>
<tr class="even">
<td>Creeu una comanda de compra d'una comanda de vendes.</td>
<td>Comprar articles quan creeu una comanda de vendes d'un projecte.</td>
<td>Els articles es consumeixen quan la comanda de vendes s'ha facturat al client.</td>
</tr>
<tr class="odd">
<td>Creeu una comanda de compra a partir d'un requisit d'articles.</td>
<td>Comprar articles quan creeu un requisit d'articles d'un projecte.</td>
<td>Els articles es consumeixen quan s'actualitza l'albarà de requisits d'articles.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Comandes de vendes per a projectes

A l'administració de projectes i la comptabilitat, podeu registrar el consum d'articles de diverses maneres. Podeu vendre articles o comprar articles d'un projecte o reservar articles per a un projecte. 

Podeu encarregar articles de l'inventari de l'empresa per al consum en un projecte. O bé podeu comprar articles d'un proveïdor extern. Els articles es poden consumir en tots els tipus de projectes tret dels projectes de temps. 

La manera com encarregueu els articles depèn d'on l'encarregueu:

-   Per encarregar articles de l'inventari de l'empresa, heu d'introduir la comanda com a requisit d'article. Si utilitzeu la pàgina **Requisits d'articles**, podeu configurar el requisit per tal que rebeu els articles com a lliuraments parcials. Per tant, podeu ajornar el consum d'una quantitat d'articles fins que els articles siguin necessaris.
-   Per encarregar articles d'un proveïdor extern, heu de crear la comanda com a comanda de compra a la pàgina **Comanda de compra**.

> [!NOTE] 
> L'albarà d'una comanda de vendes relacionada amb el projecte no es pot cancel·lar si els articles ja s'estan marcat per a l'embalatge. 

A la taula següent s'enumeren els mètodes per encarregar articles i es descriu com es consumeixen els articles.

| Mètode            | Finalitat                                                                                                                                                        | Consum de transaccions d'articles                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Comanda de venda       | Introduïu una transacció directament en un projecte de temps i material.                                                                                                   | Les transaccions d'article es consumeixen quan es comptabilitza la factura del client.                                                                               |
| Diari d'inventari | Introduïu ràpidament i manteniu els registres d'articles. Si, per exemple, voleu introduir un requisit d'article basat en una llista impresa, es pot aplicar el diari d'inventari. | Les transaccions d'article es consumeixen quan es comptabilitza el diari.                                                                                        |
| Requisit d'article  | Introduïu els articles que no es consumiran immediatament. Aquest mètode us permet fer un seguiment del nombre d'articles que s'han consumit en un únic registre de requisit d'article.    | Les transaccions d'articles es consumeixen quan s'actualitza l'albarà. En altres paraules, el requisit d'article es crea quan es comptabilitza l'albarà. |
| Ordres de compra   | Introduïu les transaccions en una de les tres ubicacions, en funció del mètode de compra.                                                                              | Les transaccions d'article es consumeixen quan s'actualitza l'albarà o quan es factura al client o el proveïdor.                                      |

### <a name="process-project-invoices"></a>Factures de projectes de procés

El tipus de projecte determina el procediment de facturació que s'ha d'aplicar. Només es poden facturar els dos tipus externs de projectes (temps i material i preu fix). Els projectes de temps i materials i els projectes de preu fix s'adjunten sempre a un contracte de projecte. 

Abans de crear una factura de client per a un projecte, podeu crear una factura preliminar o una proposta de factura. En una proposta de factura, podeu seleccionar transaccions de projecte que s'inclouran a la factura d'un projecte. A continuació, podeu revisar les dades de la factura abans de comptabilitzar la factura del projecte i enviar-la al client o a una altra font de finançament. 


Per obtenir més informació sobre com processar factures de projectes, vegeu [Facturació de projectes](../accounts-payable/project-invoicing.md).


### <a name="calculate-the-cost-to-complete-a-project"></a>Calcular el cost per completar un projecte

Quan creeu una estimació, podeu triar el mètode que s'utilitza per calcular el cost per completar el projecte. Seleccioneu un mètode del camp de **Mètode de cost per completar** a la pàgina **Crea una estimació**. El mètode que trieu s'aplica de manera separada a cada línia de cost en l'estimació del cost. Mentre una línia tingui l'estat **Creat**, podeu canviar el mètode que s'hi aplica a la pàgina **Estimació de costos**. 

A la taula següent es descriuen els mètodes per calcular el cost per completar un projecte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Mètode</th>
<th>Descripció</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Cost total: real</td>
<td>Els costos estimats s'han d'introduir manualment. Després de completar la columna <strong>Cost total</strong> o <strong>Quantitat total</strong> de la pàgina <strong>Estimació de costos</strong>, els costos reals es resten dels totals introduïts per l'usuari. El resultat és el cost de completar el projecte. Normalment, el progrés dels costos no se segueix segons, per exemple, el nombre d'estades en hotels i àpats que es registren en cada període. En canvi. El seguiment sol basar-se en una comparació amb la quantitat total d'hores estimades. Aquest enfocament no requereix un model de previsió i la quantitat total o el cost total es poden canviar manualment. Quan un valor s'introdueix en la columna <strong>Cost total</strong> o <strong>Quantitat total</strong>, el Finance compara aquest valor amb les transaccions reals que s'han comptabilitzat durant el període i, a continuació, disminueix el valor de la columna <strong>Quantitat per completar</strong> o <strong>Cost per completar</strong>.</td>
</tr>
<tr class="even">
<td>Pressupost total: real</td>
<td>Els costos reals es comparen amb el model de previsió que seleccioneu per determinar el cost. Aquest mètode utilitza un model de pressupost total que inclou les transaccions previstes. Per tal d'obtenir una visualització més precisa del projecte, podeu ajustar el model de pressupost en el moment en què el projecte està en curs. Si heu d'ajustar la previsió, seguiu aquest procés general:
<ol>
<li>Copieu les transaccions previstes en un altre model de previsió.</li>
<li>Compareu les transaccions previstes amb les transaccions reals.</li>
<li>Manteniu, reduïu o augmenteu les estimacions per al període següent.</li>
</ol>
El Finance no disminueix automàticament les estimacions previstes. Per tant, és bona idea mantenir un model de previsió original en el projecte de preu fix, per establir una línia de base per a la comparació en completar el projecte. 
<br></br> <strong>Nota:</strong> quan seleccioneu aquest mètode, utilitzeu almenys dos models de previsió. Un model hauria de contenir la previsió original. Per a l'altre model, podeu copiar les transaccions previstes d'un altre model. Aquest mètode només és vàlid per a projectes de preu fix i inversió.</td>
</tr>
<tr class="odd">
<td>Pressupost restant</td>
<td>Aquest mètode utilitza un model de pressupost restant per calcular el cost per completar el projecte. Quan utilitzeu aquest mètode, se sumen els costos reals i els imports previstos a la resta de models de pressupost. El resultat és un cost total. Abans d'utilitzar aquest mètode, s'ha de configurar un model de pressupost restant per poder deduir transaccions en funció de les transaccions reals enregistrades al sistema. A la pàgina <strong>Models de previsió</strong>, assegureu-vos que els camps estiguin marcats al grup <strong>Reducció de la previsió automàtica</strong>. Normalment, un pressupost restant es copia a partir d'un pressupost original. A mesura que es van introduint transaccions, les transaccions en el pressupost restant es redueixen. A mesura que el projecte avança, si determineu que s'ha d'ajustar el pressupost restant, carregueu les transaccions previstes al pressupost restant. <br></br> <strong>NOTA:</strong> aquest mètode només es pot aplicar si s'adjunta un model de previsió a l'estimació.</td>
</tr>
<tr class="even">
<td>Com a estimació prèvia</td>
<td>S'aplica el mateix mètode de estimació que s'utilitzava en el període anterior. Aquest mètode requereix un model de previsió si el període anterior requeria un model de previsió.</td>
</tr>
<tr class="odd">
<td>Defineix el cost per completar a zero</td>
<td>Normalment, aquest mètode s'utilitza abans d'eliminar el projecte d'estimació. Aquest mètode coincideix amb l'estimació total de les transaccions reals que s'han comptabilitzat i esborra la columna <strong>Cost per completar</strong>. El percentatge resultant de finalització és sempre del 100 per cent. El camp <strong>Previsió</strong> no està seleccionat per a cada línia de cost que creeu i l'estimació total es copia de l'estimació de cost anterior. El consum real del període de pressupost es descomptarà del cost per completar el projecte. Aquest mètode no requereix un model de previsió.</td>
</tr>
<tr class="even">
<td>Des de la plantilla de cost</td>
<td>El mètode del cost per completar que està configurat a la plantilla de cost associada amb el projecte d'estimació seleccionat s'aplica.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analitzar el projecte
En el seu nivell més bàsic, s'utilitza un projecte per agrupar les transaccions que registren costos i, a continuació, comptabilitzar aquests costos al llibre major general. 

Normalment, aquestes transaccions són el resultat de documents empresarials, com ara fulls d'hores, informes de despeses, factures de proveïdors o transaccions d'inventari. El cicle de vida d'un projecte sol començar amb estimacions, previsions i pressupostos que ajuden a planificar i anticipar el treball i l'impacte financer del projecte. A mesura que analitzeu un projecte, podeu avaluar les transaccions que s'hagin produït durant el projecte, però també la precisió de les vostres estimacions i previsions, les tarifes d'ús dels membres de l'equip del projecte i l'èxit global del projecte.

### <a name="analyze-cash-flow"></a>Analitzar el flux de caixa

Utilitzeu el seguiment de fluxos de caixa per revisar els fluxos de caixa previstos i els fluxos de caixa reals d'un projecte. Podeu revisar els fluxos de caixa mentre està en marxa un projecte o podeu visualitzar els fluxos de caixa d'un projecte finalitzat. 

Mitjançant la supervisió dels fluxos de caixa, podeu avaluar un únic projecte, utilitzar els informes per veure diversos projectes i transferir fluxos de caixa de projecte a les previsions de flux de caixa al llibre major general.

#### <a name="cash-inflow-forecasting"></a>Predicció del flux d'entrada de caixa

Segons l'organització, podeu preveure els fluxos d'entrada de caixa per a un projecte seleccionat. Per exemple, si la data del projecte és el 5 de març de 2012 i factureu el 31 de març de 2012, us presentem la previsió de la data de venciment i la data prevista de pagament de les vendes:

-   **Data del projecte:** 5 de març de 2012.
-   **Data de la factura:** 31 de març de 2012. Aquesta data es determina a partir de la freqüència de les factures. Per a aquest exemple, definiu la freqüència de factures al mes en curs. Per tant, totes les transaccions que es comptabilitzen al mes de març es facturen l'últim dia del mes.
-   **Data de venciment:** 14 d'abril de 2012. Aquesta data es determina en funció dels terminis de pagament que s'han definit per al projecte. Per a aquest exemple, heu seleccionat un termini de pagament de 14 dies. Per tant, s'afegeixen 14 dies a la data de la factura per poder arribar a una data de venciment del 14 d'abril de 2012.
-   **Data prevista de pagament de la venda:** 27 d'abril de 2012. Aquesta data es calcula afegint el nombre de dies al camp **Dies de marge generals** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat** al nombre de dies del camp **Dies de marge individuals** a la pàgina **Contractes del projecte** i, a continuació, afegint el total al nombre de dies al camp **Data de venciment**. Per a aquest exemple, heu introduït **3** en el camp **Dies de marge generals** i **10** al camp **Dies de marge individuals**. Per tant, se sumen 13 dies a la data de venciment per poder arribar a una data de pagament de vendes esperada del 27 d'abril de 2012.

Els dies de marge generals poden substituir els dies de marge individuals o sumar-hi:

-   Per utilitzar els dies de marge generals com a reemplaçament per als dies de marge individuals, introduïu el nombre mitjà de dies entre la data de venciment i la data de pagament real per als clients.
-   Per sumar els dies de marge generals als dies de marge individuals, al **camp Dies de marge generals**, introduïu l'estimació per al nombre de dies entre el dia en què el client envia el pagament i el dia en què l'organització rep el pagament.

Configureu els dies de marge individuals al contracte del projecte. Els dies es calculen segons la data de venciment tant de la factura de vendes com de l'experiència de l'organització amb el patró de pagament d'un client.

#### <a name="actual-cash-inflow"></a>Flux d'entrada de caixa real

El flux d'entrada de caixa real s'assembla a la previsió, però podeu començar els càlculs des de la primera data de la factura. Aquest és un exemple:

-   **Data de la factura:** 2 de març de 2012.
-   **Data de venciment:** 16 de març de 2012. El termini de pagament es defineix en 14 dies.
-   **Data prevista de pagament de la venda:** 29 de març de 2012. El càlcul inclou tres dies de marge generals i 10 dies de marge individuals.

#### <a name="cost-forecasting"></a>Previsió de costos

Segons els dies definits, la data de pagament de cost pot diferir de la data del projecte. En aquest cas, la data de pagament de cost es calcula sumant el nombre de dies des de la data del projecte al nombre de dies en el termini de pagament. 

Per exemple, la data del projecte de la transacció és el 5 de març de 2012 i es defineixen els terminis de pagament següents:

-   **Hores:** mes actual (**M**)
-   **Despeses:** 14 dies (**D14**)
-   **Articles:** 30 dies (**D30**)

Segons aquesta configuració, aquí teniu la data de pagament per a cada tipus de transacció:

-   **Hores:** 31 de març de 2012, que és l'últim dia del mes seleccionat.
-   **Despeses:** 19 de març,de 2012, que és 14 dies després de la data de la transacció.
-   **Articles:** 4 d'abril,de 2012, que és 30 dies després de la data de la transacció.

> [!NOTE] 
> La data de venciment per a la comanda de compra es basa en la transacció del venedor quan es crea la comanda de compra del projecte. La data de venciment no està determinada per la configuració per defecte. 

La data de pagament de cost no es calcula en dies de marge. Un cop finalitzat el projecte, quan el cost i la facturació s'han completat, tant el cost com les vendes es comptabilitzen als comptes de pèrdues i guanys. 

Quan s'hagin completat totes les factures de vendes i proveïdors, podeu visualitzar la relació entre els camps de la pàgina **Flux de caixa** i els camps de la pàgina **Extractes del projecte**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Pàgina Flux de caixa
        - Fluxos d'entrada de caixa 
        - Fluxos de sortida de caixa
        - Fluxos de caixa nets
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Pàgina Extractes del projecte
        - Ingressos
        - Cost total
        - Marge brut
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Revisar els costos

Podeu supervisar els costos que comporta l'organització durant un projecte a la pàgina **Control de costos**. Si compareu els costos originals pressupostats per al projecte amb els costos reals actuals i els costos compromesos, podeu determinar si el projecte està en bon camí, sobre el pressupost o sota el pressupost. 

> [!NOTE] 
> Quan utilitzeu la pàgina **Control de costos** per visualitzar l'estat actual dels costos del projecte, utilitzeu els models de previsió seleccionats per al pressupost original i restant. Si seleccioneu altres models de previsió quan calculeu els costos, els resultats del càlcul no seran precisos.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Visualitzar els imports pressupostats restants

Si es selecciona **Pressupost restant** com a mètode de control de cost a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**, la pàgina **Control de costos** calcula els costos que no s'han comptabilitzat com a reals o no s'han marcat com a confirmats. En concret, els imports a la pestanya **General** de la subfinestra inferior de la pàgina **Control de costos** es calculen de les maneres següents:

-   **Cost real**: import total que s'ha invertit en el projecte per a la línia de cost seleccionada. L'import de cost real es calcula a la pàgina **Actualitzacions del llibre major**.
-   **Cost confirmat**: la quantitat addicional de despeses que l'entitat jurídica s'ha compromès a pagar. Els imports de cost confirmat específics es calculen a la pàgina **Costos confirmats**.
-   **Pressupost restant**: import de l'import pressupostat original que encara està disponible per a la línia de cost seleccionada. La resta de l'import pressupostat es calcula a la pàgina **Visualització prèvia general del llibre major**.
-   **Cost total**: suma del cost real, el cost confirmat i l'import pressupostat restant.

A la pàgina **Control de costos**, a la pestanya **Desviació**, podeu visualitzar una comparació del cost total esperat amb el pressupost original. Aquesta comparació mostra les diferències entre aquests imports. Per tant, podeu veure on les dades no coincideixen. Els imports de desviació es calculen de les maneres següents:

-   **Pressupost original**: import que originalment s'havia pressupostat per a la línia de cost seleccionada. L'import pressupostat original es calcula a la pàgina **Visualització prèvia general del llibre major**.
-   **Cost total**: suma del cost real, el cost confirmat i l'import pressupostat restant, com s'indica a la pestanya **General**.
-   **Desviació**: diferència entre el cost total i el pressupost original.
-   **Variació en funció de la quantitat**: diferència total entre la previsió original i la previsió total. Aquesta diferència es pot expressar matemàticament com a (Quantitat prevista total) × (Preu mitjà original – Preu mitjà total). Aquest càlcul només s'aplica a les hores del projecte.
-   **Variació en funció del preu**: diferència total entre la previsió original i la previsió total. Aquesta diferència es pot expressar matemàticament com a (Preu previst original) × (Quantitat prevista original – Quantitat prevista total). Aquest càlcul només s'aplica a les hores del projecte.

#### <a name="viewing-the-total-budgeted-amounts"></a>Visualitzar els imports pressupostats totals

Si se selecciona **Pressupost total** com a mètode de control de costos a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**, la pàgina **Control de costos** calcula els costos reals i les despeses totals del projecte per ajudar-vos a detectar qualsevol diferència entre els dos. En concret, a la pàgina **Control de costos,** els imports de les columnes de la subfinestra inferior de la pestanya **General** es calculen de les maneres següents:

-   **Cost total pressupostat**: import pressupostat total per a la línia de cost seleccionada.
-   **Cost real**: import total de costos que ha suposat el projecte fins a la data per a les línies de cost seleccionades.
-   **Cost confirmat**: import total que s'ha confirmat per a la línia de cost seleccionada.
-   **Variació**: diferència entre la suma dels costos reals i confirmats i el cost total. La variació mostra si hi ha costos addicionals que s'han d'especificar per al pressupost total.

A la pàgina **Control de costos**, a la pestanya **Desviació**, podeu visualitzar la diferència entre el pressupost total i el pressupost original consultant els camps següents:

-   **Pressupost original**: import que originalment s'havia pressupostat per a la línia de cost. El pressupost original es calcula a la pàgina **Visualització prèvia general del llibre major**.
-   **Cost pressupostat total**: cost total que originalment s'havia pressupostat per a la línia de cost. El cost pressupostat total es calcula a la pàgina **Visualització prèvia general del llibre major**.
-   **Desviació**: desviació de la línia de cost. Aquest import es calcula restant el cost total al pressupost original.
-   **Variació en funció de la quantitat**: diferència total entre el pressupost original i el pressupost total. Aquest import es calcula restant les hores pressupostades totals a les hores pressupostades originals i, a continuació, multiplicant la diferència pel preu de cost original pressupostat. Aquesta diferència es pot expressar matemàticament com a (Preu de cost original pressupostat) × (Hores pressupostades originals – Hores pressupostades totals). Aquest càlcul només s'aplica a les hores del projecte.
-   **Variació en funció del preu**: aquest import es calcula restant les hores pressupostades totals a les hores pressupostades originals i, a continuació, multiplicant la diferència pel nombre total d'hores consumides. Aquesta diferència es pot expressar matemàticament com a (Hores consumides totals) × (Hores pressupostades originals – Hores pressupostades totals). Aquest càlcul només s'aplica a les hores del projecte.

### <a name="analyze-utilization"></a>Anàlisi d'ús

La relació d'ús és el percentatge de temps que un treballador realitza treball facturable o productiu en un període de treball concret. Les hores facturables són les hores de feina que es poden carregar a un client concret. 

La relació d'ús d'un treballador es calcula dividint el nombre d'hores facturables entre el nombre d'hores de feina d'un període de temps determinat. Per exemple, si un treballador té 30 hores facturables en un període, i el nombre d'hores de feina en el mateix període és 40, el percentatge d'ús del treballador és el 75 per cent. 

Quan calculeu la relació d'ús d'un treballador, podeu calcular la relació facturable o la relació d'eficiència:

-   **Relació facturable**: diferència entre les hores facturables i les hores no facturables o les hores estàndard.
-   **Relació d'eficiència**: diferència entre les hores productives i les hores no productives o les hores estàndard. Les hores productives són les hores que el treballador dedica a contribuir a un projecte concret. Normalment, les hores productives es facturen als clients, a excepció del cas dels projectes interns. Les hores no productives mai no es facturen a un client.

Calculeu les relacions d'utilització a la pàgina **Ús d'hores**. Els càlculs es basen en les preferències per defecte. Aquestes preferències també especifiquen la manera com es calculen les hores assignant **Ús** o **Càrrega** a cada tipus de projecte. Això s'aplica als càlculs de la relació facturable i als càlculs de la relació d'eficiència.

-   **Ús**: les hores que s'informen per al tipus de projecte seleccionat sempre es consideren facturables o d'ús d'eficiència.
-   **Càrrega**: les hores que s'informen per al tipus de projecte seleccionat sempre es consideren no facturables o sense ús d'eficiència.
-   **Segons la propietat de línia**: les propietats de línia d'una transacció d'hores determinada determinen si les hores es consideren per a la utilització facturable o d'eficiència.
-   **No incloses**: les hores no estan incloses en el càlcul d'ús facturable o d'eficiència.

A la pàgina **Ús d'hores**, a més del percentatge d'ús general per a un treballador o per a un projecte, podeu visualitzar el nombre d'hores que s'han utilitzat per als càlculs de la relació d'utilització per a cadascun dels tipus d'hores següents:

-   **Hores no incloses**: aquestes hores no s'inclouen a la relació d'ús d'hores.
-   **Hores incloses**: aquestes hores es calculen sumant les hores d'ús i les hores de càrrega. Aquestes hores s'inclouen a la relació d'ús.
-   **Hores de càrrega**: si esteu calculant una relació facturable, aquestes hores són el mateix que les hores no imputables. Si calculeu una relació d'eficiència, aquestes hores són el mateix que les hores no productives.
-   **Hores d'ús**: si esteu calculant una relació facturable, aquestes hores són el mateix que les hores imputables. Si calculeu una relació d'eficiència, aquestes hores són el mateix que les hores productives.

Quan calculeu la relació d'ús d'un treballador, podeu utilitzar les hores estàndard o les hores incloses. Si utilitzeu hores incloses, heu d'assegurar-vos que els treballadors registren tot el seu temps de treball per als períodes del full d'hores, perquè el càlcul s'expressa com a percentatge de les hores introduïdes. Quan calculeu la relació d'ús d'hores per a un projecte, un contracte de projecte, un registre de client o una categoria, heu d'utilitzar les hores incloses per al càlcul.

### <a name="review-project-statements"></a>revisió dels extractes del projecte

Podeu crear un extracte del projecte per visualitzar una instantània ràpida del progrés d'un projecte. Quan executeu un extracte del projecte, podeu especificar els criteris que s'utilitzen per calcular l'extracte fent seleccions a la pestanya **General** de la pàgina **Extractes del projecte**. Podeu seleccionar incloure o excloure la següent informació:

-   Tipus de projectes
-   Tipus de transaccions
-   Data del projecte/data del llibre major
-   Dades

Després de calcular l'extracte, podeu visualitzar la informació següent a les diverses pestanyes de la pàgina **Extractes del projecte**:

-   **General**: informació general sobre l'estructura bàsica de guanys i pèrdues del projecte.
-   **Guanys i pèrdues**: informació sobre els ingressos acumulats.
-   **Treball en curs**: informació sobre els balanços del comptes de treball en curs.
-   **Consum**: informació sobre el consum d'hores, articles, despeses i transaccions de nòmines.
-   **Factura**: informació sobre les factures i la facturació a compte.
-   **Tarifa per hora**: les tarifes per hora per a les hores que es comptabilitzen als comptes d'ingressos i costos.
