---
title: Assignació de recursos a projectes
description: Aquest tema proporciona informació sobre l'assignació de recursos a projectes.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9352465f83abe19097945dd34eada365cd03b8f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749431"
---
# <a name="project-resourcing"></a>Assignació de recursos a projectes

[!include [banner](../includes/banner.md)]

Aquest tema proporciona informació sobre l'assignació de recursos a projectes.

Un dels reptes dels administradors de projectes i administradors de recursos de la fase de planificació del projecte és l'assignació de recursos, on han de determinar i reservar el recurs correcte per treballar en un projecte. Al Dynamics 365 Finance, les capacitats d'assignació de recursos per als projectes us permeten definir funcions que es tracten com a recursos temporals que es poden reservar per a un compromís específic o com a part d'un compromís. Aquest tipus d'assignació de recursos permet als administradors de projecte i els administradors de recursos completar les tasques següents:

- Definiu una funció que tingui les competències necessàries, de manera que sigui fàcil fer coincidir els recursos.
- Utilitzar funcions per definir una planificació inicial de la interacció basada en recursos reservats.
- Estimar els costos i determinar un pressupost inicial, basat en les funcions i recursos assignats per a un projecte.
- Utilitzar funcions per calcular el nombre de reserves de recursos necessàries per a cada interacció.
- Calcular el nombre de recursos necessaris per a tot el cicle de vida d'un projecte.
- Fer un esborrany d'una estructura del desglossament del treball (WBS) mitjançant les assignacions de recursos inicials.

[![Cicle de vida del projecte](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

A mesura que avança la planificació del projecte, els recursos planificats poden substituir-se per recursos de personal. L'administrador de projectes també pot tornar enrere i actualitzar les reserves de recursos durant qualsevol fase del projecte.

## <a name="set-up-project-resources"></a>Configuració dels recursos del projecte
Heu de configurar un calendari i associar-lo a un empleat o a un treballador. El calendari s'utilitza per planificar el projecte i el temps de treball dels recursos que es reserven per al projecte. Durant la configuració del calendari, els administradors del projecte poden fer un anivellament de recursos com a part de l'optimització de recursos. Segons la planificació de calendari, es poden posar restriccions als recursos. Podeu configurar un calendari a la pàgina **Calendaris**.

Quan configureu un treballador com a recurs de projecte, podeu seleccionar els treballadors que treballen a l'empresa per a la qual configureu els recursos. Si ho preferiu, podeu seleccionar treballadors d'altres empreses a l'organització. Aquests treballadors s'anomenen recursos entre empreses.

En els procediments següents s'explica com es configura un treballador com a recurs de projecte a l'empresa i com es configura un recurs de projecte entre empreses.

### <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un treballador com a recurs de projecte

1. A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el treballador que voleu afegir com a recurs del projecte i obriu el registre del treballador.
2. A la subfinestra d'acció, seleccioneu **Projecte** &gt; **Configuració** &gt; **Configuració del projecte**.
3. Seleccioneu un calendari i, a continuació, tanqueu la pàgina.

També podeu especificar projectes per defecte per a un recurs com a tipus d'assignació prèvia. Les assignacions prèvies es poden utilitzar quan l'administrador de recursos o l'administrador del projecte sap en quins projectes treballarà el recurs amb antelació. Les assignacions prèvies també poden basar-se en la sol·licitud d'un patrocinador o client del projecte. Per assignar prèviament un projecte abans, a la pàgina **Assigna els projectes**, a la pestanya **Projectes**, a la llista **Projectes restants**, seleccioneu el projecte adient.

### <a name="set-up-an-intercompany-resource"></a>Configurar un recurs entre empreses

Quan configureu un treballador com a recurs entre empreses, heu d'emplenar la configuració tant de l'empresa prestadora com de l'empresa prestatària.

**A l'empresa prestadora**

1. Al Finance, comproveu que l'empresa prestadora està seleccionada i, a continuació, completeu el procediment a la secció anterior, "Configurar un treballador com a recurs del projecte".
2. A la pàgina **Comptabilitat entre empreses**, seleccioneu **Nova**.
3. Al camp **ID de l'entitat jurídica**, seleccioneu l'empresa prestadora. Empleneu els camps restants segons calgui i seleccioneu **Desa**.
4. A la pàgina **Transferència de preus**, seleccioneu **Nova**.
5. Al camp **Entitat jurídica prestatària**, seleccioneu l'empresa adequada.
6. Per prestar a l'empresa prestatària només el recurs que heu creat a l'inici d'aquesta secció, al camp **Recurs**, seleccioneu el nom del recurs que heu creat. Per fer que tots els recursos de l'empresa prestadora estiguin disponibles per a l'empresa prestatària, deixeu el camp **Recurs** en blanc.
7. A la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**, a la pestanya **Entre empreses**, definiu l'opció **Habilita la planificació de recursos i els fulls d'hores entre empreses** a **Sí**.

**A l'empresa prestatària**

- A la pàgina **Llista de recursos**, al filtre de cerca, introduïu el nom del recurs que heu creat per a l'empresa prestadora, per comprovar que el nom s'inclou a la llista de recursos de l'empresa prestatària.

## <a name="manage-resource-competencies"></a>Administració de competències de recursos
Les competències de recursos són una part essencial de l'administració de recursos. Les competències poden utilitzar-se com a línia de base per determinar els recursos que tenen l'equilibri correcte de destreses, formació, certificació i experiència de projectes. Heu de configurar aquesta informació per a cada recurs i actualitzar-la periòdicament. D'aquesta manera, podeu maximitzar la capacitat quan les competències de recursos específiques coincideixin durant l'assignació de recursos del projecte.

[![Exemples d'habilitats, certificacions, formació i experiència de projectes](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

En els procediments següents s'explica com es configuren algunes de les competències d'un recurs.

Per configurar les competències per a un treballador, podeu utilitzar la pàgina de llista **Treballadors** de recursos humans o la pàgina de llista **Recursos** a Administració de projectes i comptabilitat. Per als procediments següents, s'utilitza la pàgina de llista **Treballadors** de recursos humans.

### <a name="set-up-competencies-certificates"></a>Configurar competències: certificats

1. A la pàgina de llista **Treballadors**, seleccioneu la línia per al treballador per afegir-hi la informació del certificat.
2. A la subfinestra d'acció, a la pestanya **Treballador**, al grup **Competències**, seleccioneu **Certificats**.
3. Seleccioneu **Nou** i, a continuació, al camp **Tipus de certificat**, seleccioneu **PMP**.
4. Al camp **Data d'inici**, seleccioneu **1/10/2015** i, a continuació, seleccioneu **Desa**.

### <a name="set-up-competencies-skills"></a>Configurar competències: habilitats

1. A la pàgina de llista **Treballadors**, assegureu-vos que el treballador que heu utilitzat en el procediment anterior encara està seleccionat. A continuació, a la subfinestra d'acció, a la pestanya **Treballador**, al grup **Competències**, seleccioneu **Habilitats**.
2. Seleccioneu **Crea**.
3. Al camp **Habilitat**, seleccioneu **Administració de projectes**.
4. Al camp **Nivell**, seleccioneu **5 Expert**.
5. Al camp **Data del nivell**, seleccioneu **14/1/2014**.
6. En el camp **Anys d'experiència**, introduïu **10**.
7. Seleccioneu **Desa** i, a continuació, tanqueu la pàgina.

## <a name="create-a-new-project"></a>Crear un projecte nou
1. A la pàgina **Administració de projectes**, seleccioneu **Projecte nou** i introduïu els valors següents:

    - **Tipus de projecte:** temps i material
    - **Nom del projecte:** Fase 2 d'actualització d'XYZ
    - **Grup de projectes:** TM\_WIP
    - **Identificador de contracte de projecte**: 00000002

2. Seleccioneu **Crea el projecte**.

### <a name="assign-a-resource-to-a-project"></a>Assignació d'un recurs a un projecte

1. A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el registre del treballador per al qual heu configurat les competències anteriorment i obriu el registre del treballador.
2. A la subfinestra d'acció, a la pestanya **projecte**, al grup **Configuració**, seleccioneu **Assigna projectes**.
3. A la pàgina **Assignacions de projecte de validació de recursos**, a la pestanya **Projectes**, al camp **Afegeix el projecte als projectes seleccionats**, filtreu el projecte **Fase 2 d'actualització d'XYZ**.
4. A la subfinestra **Projectes restants**, seleccioneu un projecte i, a continuació, seleccioneu el botó de fletxa per afegir-lo a la subfinestra **Projectes seleccionats**.

També podeu assignar categories per a un recurs a mesura que les necessiteu. El tipus de categoria és **Cost** o **Ingrés**. El tipus de categoria ve determinat per la vostra organització. Si no s'assigna cap categoria a un recurs, el Finance cerca la categoria per defecte a preus per hora per als costos i els ingressos.

### <a name="set-up-project-resource-and-role-characteristics"></a>Configurar els recursos del projecte i les característiques de la funció

Un administrador de projectes pot utilitzar la funcionalitat de recursos de projecte per crear les funcions necessàries per al projecte. Es poden utilitzar funcions si els recursos confirmats es desconeixen quan es reserven els recursos. Les funcions es poden reservar temporalment com a recursos planificats per tal de poder continuar la fase de planificació del projecte.

[![Exemple d'una funció](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenari:** Contoso ha estat contractat per completar un projecte d'hora i material que té una carta de projectes aprovada. L'administrador de projectes júnior encara està completant l'àmbit del projecte. L'administrador de recursos està identificant actualment els recursos específics que es reservaran per treballar en el nou projecte. A causa del caràcter crític del projecte, el patrocinador del projecte ha sol·licitat l'administrador de projectes sènior com una de les funcions. L'administrador de recursos ha d'adquirir el recurs nou i definir la funció en el sistema en cas que l'administrador de projectes júnior requereixi la informació del recurs durant la planificació del projecte.

Els passos següents mostren com l'administrador de recursos pot configurar la funció Administrador de projectes sènior i associar-hi les característiques del recurs. Més endavant, la funció es pot utilitzar per cercar recursos disponibles que coincideixin amb les competències de recursos necessàries.

1. A la pàgina **Configura les funcions**, seleccioneu **Nou** i introduïu els valors següents:

    - **Identificador de funció:** administrador de projectes sènior
    - **Descripció:** administrador de projectes sènior

2. Seleccioneu **Crea**.
3. Seleccioneu la funció **Administrador de projectes sènior** i, a continuació, seleccioneu **Configura les característiques**.
4. Al camp **Tipus de característiques**, seleccioneu **Habilitat**.
5. Al camp **Característiques disponibles**, introduïu l'habilitat que voleu cercar.
6. Al camp **Tipus de característiques**, seleccioneu **Certificat**.
7. Al camp **Característiques disponibles**, introduïu el tipus de certificat que voleu cercar.

### <a name="assign-a-project-resource-to-a-project"></a>Assignació d'un recurs de projecte a un projecte

1. A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.
2. A la pestanya **Equip del projecte i planificació**, seleccioneu **Afegeix**.
3. Al camp **Funció**, seleccioneu **Membre de l'equip**.
4. Seleccioneu **Reserva des del calendari**.
5. A la pàgina **Disponibilitat de recursos**, seleccioneu **Visualitza la configuració**.
6. A la pàgina **Ajusta la configuració de visualització**, introduïu els valors següents:

    - **Format per a la visualització d'interval de dates:** dia
    - **Mostra les descripcions de disponibilitat:** Sí
    - **Mostra la capacitat restant:** Sí

7. Seleccioneu un recurs de la llista de recursos.
8. Seleccioneu **Reserva fixa** i **Capacitat completa**.


### <a name="assign-a-resource-to-a-default-role"></a>Assignar un recurs a una funció per defecte

Per ajudar els administradors de projecte o de recursos, podeu desglossar els recursos que es poden reservar per a un projecte. Podeu associar una funció per defecte amb un recurs existent o un recurs adquirit recentment. Per exemple, quan Daniel va ser contractat, tenia l'experiència i les habilitats necessàries per cobrir la funció d'analista de negocis. L'administrador de recursos ha assignat aquesta funció com a funció per defecte del Daniel. Per tant, l'administrador de recursos ha afegit en Daniel a un grup d'analistes de negoci que estan disponibles per treballar en projectes.

Durant la reserva de recursos, els administradors de projectes poden filtrar els recursos de la funció que estan disponibles per treballar en projectes. Poden utilitzar aquesta informació com un criteri quan realitzen una anàlisi de decisió de diversos criteris durant el compliment dels recursos. També poden afegir altres característiques de recursos al filtre per cercar recursos que tinguin habilitats, formació i experiència específics per a un projecte concret.

**Escenari:** s'ha iniciat un projecte aprovat i la funció Administrador de projectes sènior s'ha reservat com a recurs planificat durant la fase de planificació del projecte. L'administrador de recursos ha adquirit un recurs per cobrir la funció Administrador de projectes sènior.

1. A la pàgina **Llista de recursos**, seleccioneu **Daniel Goldschmidt**.
2. A la pàgina **Funció del recurs**, seleccioneu **Nova** i introduïu els valors següents:

    - **Efectivitat:** introduïu la data actual.
    - **Venciment:** introduïu **Mai**.
    - **Funció:** introduïu **Administrador de projectes sènior**.

3. Seleccioneu **Desa** i, a continuació, tanqueu la pàgina.
4. A la pestanya **Competències**, afegiu l'habilitat **ProjectMgmt** i el certificat **PMP**.

## <a name="set-up-role-based-pricing"></a>Configurar els preus basats en funcions
Tots els preus de cost, de vendes i de transferència es poden configurar per a funcions.

1. A la pàgina **Preu de vendes (hora)**, seleccioneu **Nou** i introduïu una data d'efectivitat.
2. A la columna **Funció**, seleccioneu una funció.
3. A la columna **Preus**, introduïu un preu per a la funció de recurs seleccionada.

## <a name="form-a-project-team"></a>Formar un equip de projecte
Per utilitzar les funcions que s'han configurat prèviament en un projecte, un administrador de projectes ha d'associar les funcions amb el projecte. Es poden assignar diverses funcions per a un projecte. Per evitar confusions, aquestes funcions s'etiqueten automàticament a la reserva. Per exemple, si l'administrador de projectes requereix tres enginyers de programari, es generen automàticament tres funcions Enginyer de programari que tenen les etiquetes **Enginyer de programari 1**, **Enginyer de programari 2** i **Enginyer de programari 3**. Si abans s'havien definit característiques de funció per a la funció, s'apliquen com a filtre durant les cerques d'un recurs. Les característiques addicionals es poden afegir com a necessàries per refinar la cerca.

La configuració de la visualització també es pot personalitzar per oferir una millor visualització de la disponibilitat dels recursos. Hi ha opcions per mostrar la disponibilitat horària, diària, setmanal, mensual, trimestral i anual. També hi ha una opció per mostrar la capacitat disponible i restant dels recursos. Aquesta opció és útil per a l'administració de temps, quan estimeu el temps disponible per a activitats o la disponibilitat dels recursos.

L'administrador del projecte pot seleccionar una funció a la pàgina i, a continuació, si hi ha un recurs disponible que s'ajusta al requisit, seleccionar la reserva d'un recurs per emplenar la funció. Heu de tenir en compte que els recursos no s'hauran de reservar en aquest moment a la fase de planificació. Quan creeu una WBS, podeu substituir les funcions per recursos de personal per al projecte. Si les funcions se substitueixen amb els recursos de personal a la WBS, la configuració del recurs actualitza automàticament la llista i la planificació de l'equip del projecte.

[![Llista de l'equip del projecte que inclou les funcions i els recursos reals](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

L'administrador de projectes té diverses opcions per reservar un recurs per a un projecte, com ara **Capacitat restant**, **Capacitat completa**, **Percentatge de capacitat** i **Especifica les hores**. Aquestes opcions de reserva es poden cancel·lar en qualsevol moment si canvien les assignacions de recursos. S'admeten dos tipus de reserves:

- **Reserva fixa**: la reserva de recursos s'ha aprovat i confirmat per treballar en la implicació durant la duració especificada.
- **Reserva flexible**: la reserva de recursos s'ha definit provisionalment per treballar en la implicació durant la duració especificada.

El següent procés explica com crear un equip de projecte.

### <a name="create-a-project-team"></a>Creació d'un equip de projecte

1. A la pàgina de llista **Tots els projectes**, seleccioneu un projecte i, a continuació, seleccioneu **Edita**.
2. A la pestanya **Equip del projecte i planificació**, al camp **Data de finalització de la planificació**, introduïu la data d'inici de la planificació més un mes. Per exemple, si la data d'inici de la planificació és el 24 de juny de 2017 (24/06/2017), introduïu **24/07/2017**.
3. Seleccioneu **Afegeix**.
4. A la subfinestra **Afegeix funcions al projecte**, al camp **Funció**, seleccioneu **Administrador de projectes sènior**.
5. Seleccioneu **Competències necessàries**.
6. A la pàgina **Trieu les característiques**, les característiques que prèviament heu definit per a la funció Administrador de projectes sènior se seleccionen per defecte. Seleccioneu **D'acord**.
7. A la pàgina **Afegiu funcions al projecte**, al camp **Nombre de recursos**, introduïu **1**.
8. Al camp **Recurs**, la cerca mostra tots els recursos que tenen les competències necessàries. Seleccioneu **Daniel Goldschmidt** i, a continuació, seleccioneu **Crea**.
9. A la pàgina **Projecte**, seleccioneu **Afegeix**.
10. A la subfinestra **Afegeix funcions al projecte**, al camp **Funció**, seleccioneu **Membre de l'equip**. En el camp **Nombre de recursos**, introduïu **5**.
11. Seleccioneu **Crea**.
12. A la pàgina **Projectes**, seleccioneu **Completa el recurs**.

## <a name="resource-capacity-synchronization"></a>Sincronització de la capacitat de recursos
Els processos per a la sincronització de recursos ajuden a garantir que la informació del calendari i el calendari base es transfereix en la planificació de recursos del projecte. Si el calendari canvia, els processos fan les actualitzacions necessàries a la planificació de recursos del projecte. Els processos també ajuden a millorar el rendiment, ja que la informació de recursos del calendari se sincronitza amb antelació. Per tant, les actualitzacions de la informació de planificació de recursos ocorren amb més rapidesa. Us recomanem que planifiqueu els processos com un lot en comptes d'un en un cada vegada. Altrament, hi ha un risc que algú oblidi les dates inclusives quan la informació s'ha sincronitzat per última vegada. Si no es fan servir dates inclusives, poden produir-se llacunes durant la sincronització de les dates.

![Sincronització del calendari](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Sincronització de la consolidació de capacitat de recursos

El procés de sincronització està dissenyat per sincronitzar tota la informació del calendari de recursos. Aquesta informació inclou informació del calendari base sobre qualsevol canvi que hi hagi a la taula de capacitat de calendari de recursos del projecte. Si s'afegeixen recursos nous al projecte, la sincronització ajuda a garantir que la informació actualitzada del calendari estigui disponible. Aquesta sincronització es pot fer en qualsevol moment.

Es recomana utilitzar un lot. Hi ha disponibles les opcions durant la sincronització de les reserves de capacitat.

1. Seleccioneu **Administració de projectes i comptabilitat** &gt; **Periòdic** &gt; **Sincronització de capacitat** &gt; **Sincronitza les consolidacions de capacitat de recursos**.
2. Definiu les opcions a la taula següent.

    | Opció      | Descripció |
    |-------------|-------------|
    | Codi de període | Opcionalment, seleccioneu el codi d'interval de dates del llibre major general per definir les dates d'inici i d'acabament per al procés de sincronització per a les consolidacions de capacitat de recursos. |
    | Data d'inici  | Introduïu la data d'inici del procés de sincronització per a la consolidació de capacitat de recursos. |
    | Data de finalització    | Introduïu la data de finalització del procés de sincronització per a la consolidació de capacitat de recursos. |

[![Procés de sincronització](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Configurar funcions a les plantilles de WBS
Els administradors de projectes poden configurar les plantilles de WBS que poden aplicar-se quan creen una WBS per a nous projectes. Els administradors de projectes poden afegir funcions quan creen una plantilla. Utilitzeu el procediment següent per assignar una funció a una plantilla de WBS.

1. Seleccioneu **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Projectes** &gt; **Plantilles d'estructura del desglossament del treball**.
2. Seleccioneu **Detalls** per a una plantilla de WBS seleccionada.
3. Seleccioneu una tasca a la llista i, a continuació, al camp **Funció**, seleccioneu una funció per assignar a la tasca.

### <a name="work-with-a-wbs"></a>Treballar amb una WBS

Podeu crear una WBS nova o bé copiar una WBS d'una plantilla de WBS existent. Un administrador de projectes pot administrar fàcilment els recursos assignant funcions a tasques noves a la WBS. Les funcions es poden reemplaçar bé després que s'hagi adquirit un recurs o després que s'identifiqui un recurs confirmat per treballar en la tasca. Aquesta flexibilitat permet que els administradors de projectes duguin a terme les tasques següents:

- Identificar el nombre de recursos necessaris per als paquets de treball de WBS.
- Estimar els costos dels projectes.
- Determinar un pressupost preliminar.
- Estimar la duració de l'activitat, segons les funcions i els recursos.
- Desenvolupar plans d'administració de projectes, segons la informació disponible del projecte.

S'ha afegit més opcions a la WBS per utilitzar millor la funcionalitat de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opció</th>
<th>Descripció</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Assignacions de recursos</td>
<td>Visualitzeu els recursos, les dates, el nombre d'hores i el tipus de reserva de les tasques a la WBS.</td>
</tr>
<tr class="even">
<td>Genera automàticament un equip</td>
<td>Afegiu automàticament recursos planificats mitjançant funcions que estan associades a una tasca. L'assignació suggereix automàticament els recursos planificades mitjançant una anàlisi de decisions de diversos criteris que es basa en funcions. Després que les funcions i l'esforç (hores) s'hagin definit per a les tasques en una WBS i després que s'hagi publicat l'estructura, seleccioneu <strong>Genera automàticament un equip</strong>. El nombre necessari de recursos planificats s'afegeix a la WBS i a la pestanya <strong>Planificació d'equips i projectes</strong>.</td>
</tr>
<tr class="odd">
<td>Recurs (llista desplegable)</td>
<td>A la pàgina <strong>Inicia l'assignació de recursos</strong>, podeu seleccionar recursos per reservar de manera fixa o flexible, segons la duració especificada. Podeu ajustar la configuració de visualització per veure i definir la duració de les activitats dels recursos. Podeu seleccionar i assignar recursos al nivell de paquet de treball mitjançant les opcions següents:
<ul>
<li><strong>Accepta</strong>: confirma els canvis al recurs que s'assigna a una tasca.</li>
<li><strong>Cancel·la</strong>: cancel·la els canvis al recurs que s'assigna a una tasca.</li>
<li><strong>Assigna automàticament</strong>: un recurs disponible de personal que té una funció coincident se selecciona automàticament i s'assigna a la tasca seleccionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.
2. Seleccioneu **Planificació** &gt; **Activitats** &gt; **Estructura del desglossament del treball**.
3. Seleccioneu **Nou** per afegir les següents opcions de nivell u per a la WBS:

    - Inici
    - Planificació
    - S'està executant
    - Supervisió i control
    - Tanca 

4. Definiu les dates i l'esforç (hores), com es mostra a la il·lustració següent.

    [![Definir les dates i l'esforç](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccioneu la línia de tasca **Inici** i, a continuació, al camp **Funció**, seleccioneu **Administrador de projectes sènior**.
6. Seleccioneu **Publica**.
7. A la mateixa línia, al camp **Recurs**, seleccioneu **Daniel Goldschmidt** i, a continuació, seleccioneu **Accepta**.
8. Seleccioneu la línia de tasques **Planificació** i, a continuació, al camp **Funció**, seleccioneu **Analista de negoci**.
9. Seleccioneu **Publica** i, a continuació, seleccioneu **Genera automàticament l'equip**.
10. Al quadre de missatge que apareix, seleccioneu **Sí**.
11. Al camp **Recurs**, comproveu que el valor és **Analista de negoci 1**.
12. Per al recurs **Analista de negoci 1**, obriu la cerca i seleccioneu **Inicia les assignacions de recursos**. A continuació, seleccioneu un treballador per a la tasca.
13. Seleccioneu **Assignació flexible** &gt; **Capacitat completa**.

    > [!NOTE] 
    > No rebeu cap advertiment que el recurs especificat és ara 2, perquè el nombre de recursos continua sent 1.

14. A la pàgina **Estructura del desglossament del treball**, valideu l'assignació de recursos a la WBS i, a continuació, seleccioneu **Desa**.

## <a name="resource-fulfillment-for-planned-resources"></a>Compliment de recursos per a recursos planificats
Un administrador de projectes pot planificar les funcions de recursos necessàries per a un projecte. L'administrador de recursos veurà aquests recursos planificats com a sol·licituds a la pàgina **Compliment de recursos** i pot assignar els recursos reals.

1. A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.
2. Seleccioneu **Projecte** i, a continuació, **Edita**.
3. A la pestanya **Equip del projecte i planificació**, seleccioneu **Afegeix**.
4. Al quadre de diàleg **Afegeix funcions**, seleccioneu la funció **Desenvolupador de programari**.
5. Seleccioneu **Crea** i, a continuació, tanqueu la pàgina del projecte.
6. A la pàgina **Compliment de recursos**, seleccioneu **Desenvolupador de programari 1** per al projecte **Fase 2 del projecte d'actualització d'XYZ**.
7. Seleccioneu un treballador i, després, **Assigna**.
8. Verifiqueu que s'hagi suprimit la línia **Desenvolupador de programari 1** per al projecte **Fase 2 del projecte d'actualització d'XYZ**.
9. A la pestanya **Equip del projecte i planificació**, per al projecte **Fase 2 d'actualització d'XYZ**, comproveu que el treballador que heu seleccionat al pas anterior s'hagi afegit com a **Desenvolupador de programari**.

## <a name="requests-for-project-resources"></a>Sol·licituds de recursos del projecte
La funcionalitat per a la planificació de recursos de projectes només permet distribuir els recursos de personal a compromisos o projectes. Per habilitar aquesta funcionalitat, completeu les tasques següents o verifiqueu que s'hagin completat:

- Configureu les seqüències de números.
- Configureu l'administració de projectes i els fluxos de treball de comptabilitat.
- Habiliteu els fluxos de treball de sol·licitud de recursos.

Quan s'hagin completat les tasques anteriors, podreu completar les tasques següents segons calgui:

- Crear una sol·licitud de recurs des d'un recurs de personal reservat de manera flexible.
- Supervisar les sol·licituds de recursos.
- Complir les sol·licituds de recursos.
- Sol·licitar un recurs de personal d'una WBS.
- Reservar recursos en un projecte sense necessitat de tenir una sol·licitud de recurs de personal.

## <a name="monitor-project-teams"></a>Supervisar els equips del projecte
1. A la pàgina **Tots els projectes**, seleccioneu l'enllaç **Identificador del projecte** per al projecte **Fase 2 d'actualització d'XYZ**.
2. Al FastTab **Equip del projecte i planificació**, comproveu que els recursos del projecte que es mostren siguin correctes.
