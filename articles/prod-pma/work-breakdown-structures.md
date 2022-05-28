---
title: Informació general de les estructures del desglossament del treball
description: Una estructura del desglossament del treball (WBS) és una descripció del treball que es farà per a un projecte. Es tracta d'una jerarquia de tasques que representa la comprensió de l'equip del projecte sobre la composició del treball, la mida, el cost i la duració de cada component o tasca.
author: Yowelle
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e69d7cc97e3a7a59bdba387282fe19d12f5780
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683348"
---
# <a name="work-breakdown-structures-overview"></a>Informació general de les estructures del desglossament del treball

[!include [banner](../includes/banner.md)]

Una estructura del desglossament del treball (WBS) és una descripció del treball que es farà per a un projecte. Es tracta d'una jerarquia de tasques que representa la comprensió de l'equip del projecte sobre la composició del treball, la mida, el cost i la duració de cada component o tasca. Una WBS té tres propòsits principals:

-   Descriure el desglossament o la composició del treball en tasques.
-   Planificar la feina del projecte.
-   Estimar el cost de cada tasca.

El grau de detall d'una WBS depèn del nivell de precisió necessari a les estimacions i el nivell de seguiment que es requereixi per a aquestes estimacions. Els projectes que tenen molt poca tolerància als canvis de terminis o cost solen requerir una WBS més detallada i un seguiment diligent del progrés del treball i el cost en relació amb la WBS. Aquest tipus de projecte és habitual en els sectors de la construcció i l'enginyeria. 

Per contra, els projectes en sectors com ara els mitjans de comunicació i la publicitat, el programari i la infraestructura de TI tendeixen a ser propis, i la productivitat és relativa a l'experiència i la competència de la persona que està duent a terme la tasca. Per tant, aquests sectors utilitzen una WBS per aconseguir una aproximació de la mida d'un projecte i no fer un seguiment del progrés del projecte en detall. 

La creació d'una WBS és un procés intensiu que sol fer-se durant un llarg període, i que requereix la col·laboració i la informació d'una gran varietat de persones. En aquest tema es descriu com podeu utilitzar millores de WBS per satisfer els vostres requisits per a les estimacions i el seguiment.

## <a name="prerequisites-for-creating-a-wbs"></a>Requisits previs per crear una WBS
Per crear una WBS, heu de poder crear una planificació del treball i estimar el cost del treball.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Requisits previs per crear una planificació de treball

Per utilitzar les capacitats de planificació completes de les característiques de la WBS, completeu la configuració següent:

1.  Configureu un calendari per defecte i un calendari de projecte:
    1.  Feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Paràmetres de l'administració de projectes i comptabilitat** &gt; **Planificació**. Al camp **Calendari de treball per defecte**, especifiqueu un calendari per defecte. Aquest serà el calendari de treball per defecte per a qualsevol projecte nou que es creï.
    2.  Podeu canviar el calendari per defecte d'un projecte concret. Feu clic a la pàgina de detalls del projecte i, a continuació, al FastTab **Equip del projecte i planificació**, actualitzeu el camp **Calendari de planificació** seleccionant un altre calendari.

2.  Configureu els dies laborables estàndard i les hores de feina. El calendari que definiu com a calendari de treball per al vostre projecte s'utilitzarà a la WBS per determinar la següent informació:

-   Dies laborables i festius
-   Nombre d'hores de feina en un dia

Per configurar els dies laborables i les hores de feina per a un calendari o per crear un calendari nou, feu clic a **Administració de l'organització** &gt; **Comú** &gt; **Calendaris**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Requisits previs per a l'estimació del cost del treball

Per utilitzar les capacitats completes d'estimació de costos de la WBS, heu de configurar els costos i els preus de les vendes dels treballadors, les categories de personal, les despeses i honoraris i els articles.

-   Per configurar el preu del cost i de venda de les categories de personal, despeses i honoraris, feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Preus**.
-   Per configurar el preu de cost i de vendes dels articles, utilitzeu la pàgina **Acords comercials** per a cada element de la pàgina de llista **Productes al mercat** a Administració de la informació del producte.

## <a name="creating-a-wbs"></a>Crear una WBS
La creació d'una WBS implica tres activitats:

1.  **Descomposició del treball:** crear un desglossament de treball en fragments o tasques gestionables.
2.  **Calendari de treball**: estimació del temps que es requereix per completar una tasca, definició d'interdependències de tasques i selecció de les dates d'inici i d'acabament per a les tasques.
3.  **Estimació de costos**: estimació de costos de cada tasca.

A les seccions següents es tracta la manera com les capacitats de WBS poden ajudar amb cadascuna d'aquestes activitats.

### <a name="work-decomposition"></a>Descomposició del treball

La creació d'un desglossament o descomposició del treball sol ser el primer pas en el procés de creació d'una WBS. La funcionalitat de WBS admet les construccions bàsiques següents per al desglossament o la descomposició del treball. 

**Tasca arrel del projecte**: la tasca arrel del projecte és la tasca de resum de nivell superior d'un projecte. Totes les altres tasques de projecte es creen a sota. El nom de la tasca arrel sempre és el nom de projecte. L'esforç, les dates i la duració del node arrel resumeixen els valors de les tasques sota la tasca arrel. No podeu modificar les propietats de node arrel ni suprimir-lo.

**Tasques de resum o contenidor**: una tasca de resum és una tasca que té subtasques o tasques constituents per sota. Una tasca de resum no té cap esforç de treball ni el cost propi. En el seu lloc, l'esforç de treball i el cost d'una tasca de resum són la suma de l'esforç de treball i el cost de les seves tasques constituents. La primera data d'inici de les tasques constituents s'utilitza com a data d'inici de la tasca de resum i l'última data de finalització de les tasques constituents s'utilitza com a data de finalització. Podeu modificar el nom d'una tasca de resum, però no podeu modificar les propietats de planificació per l'esforç, les dates i la duració. Si suprimiu una tasca de resum, també heu de suprimir totes les tasques constituents. 

**Tasques de nodes fulla**: una tasca de node fulla representa el paquet de treball més granular del projecte. Un node fulla té un esforç previst, un nombre de recursos planificat, dates d'inici i final planificades i una durada. 

Podeu completar les operacions de jerarquia següents per habilitar la creació d'una jerarquia de treball o una descomposició per a un projecte. 

**Tasca nova**: qualsevol tasca nova que creeu s'afegeix automàticament sota el node arrel i un número de WBS s'assigna automàticament a la tasca. El número de WBS representa el nivell de la tasca a la jerarquia. Per a les tasques del primer nivell sota la tasca arrel del projecte, s'utilitza un esquema de numeració d'1, 2, 3, i així successivament. Per a les tasques sota el primer nivell, s'utilitza un esquema de numeració d'1.1, 1.2, 1.3, i així successivament. Per a cada nivell que s'afegeix a partir d'un nivell anterior, s'afegirà una nova sèrie de números amb punts. 

Actualment, no es pot personalitzar la numeració de la WBS. 

**Sagna la tasca**: en sagnar una tasca, es converteix en secundària de la tasca que la precedeix. El número de WBS de la tasca secundària nova es torna a calcular automàticament segons el número de la WBS del nou element principal. La tasca principal és ara una tasca de contenidor o de resum i, per tant, es converteix en una consolidació de les seves tasques constituents. 

> [!NOTE] 
> Quan sagneu les tasques en una tasca que era un node de fulla abans de l'operació de sagnat, la tasca resum que s'acaba de crear perd les seves pròpies dates, esforç i nombre de recursos. Ara s'utilitza un resum dels valors de les seves noves tasques constituents. 

**Elimina el sagnat de la tasca**: quan s'elimina el sagnat d'una tasca, ja no és una tasca constituent de la principal. El número de WBS d'aquesta tasca es torna a calcular automàticament per reflectir el nivell nou de la tasca a la jerarquia. L'esforç, el cost i les dates de la tasca principal anterior es tornen a calcular per tal que excloguin aquesta tasca. 

**Desplaça amunt i Desplaça avall**: quan feu clic a **Desplaça amunt** i **Desplaça avall**, canvieu la posició d'una tasca dins de la jerarquia de la principal. La posició d'una tasca no afecta l'esforç, cost, data o duració de la tasca. No obstant, el número de WBS de la tasca es torna a calcular automàticament per reflectir la nova posició de la tasca.

### <a name="schedule-estimation"></a>Estimació de la planificació

L'estimació de la programació sol ser el segon pas per crear una WBS. Com a pràctica recomanada, heu de completar l'estimació de la planificació després de crear les tasques. La pàgina **Estructura del desglossament del treball** del Finance té dues seccions. La subfinestra superior està dissenyada per a l'estimació de la planificació i la subfinestra inferior inclou la pestanya **Costos i ingressos estimats** que podeu utilitzar per a l'estimació de costos. 
**Dependències de tasques**: en una WBS, podeu crear una relació de predecessor entre tasques. Quan s'assignen tasques predecessores a una tasca, la tasca només pot començar quan s'hagin completat totes les tasques predecessores. La data d'inici planificada de la tasca es defineix automàticament com a l'última data de totes les predecessores. 

**Planificació de tasques**: els factors següents determinen la planificació de tasques del node de fulla:

-   Predecessors
-   Esforç
-   Nombre de recursos
-   Dates d'inici i d'acabament

La data d'inici d'una tasca de node fulla que no té un predecessor es defineix automàticament a la data d'inici de la planificació del projecte. La durada d'una tasca de node fulla sempre es calcula com el nombre de dies feiners entre les dates d'inici i final. 

*<strong><em>Regles de planificació</em></strong>*: quan s'activa l'ajuda automàtica de planificació, les regles següents s'apliquen a la planificació de tasques per al node de fulla:

-   Les dates d'inici i final de la tasca sempre han de ser dies hàbils segons el calendari de planificació del projecte.
-   La data d'inici d'una tasca que té predecessores es defineix automàticament a l'última data de finalització de les seves predecessores.
-   L'esforç d'una tasca es calcula automàticament de la següent manera:

Nombre de persones × Duració × Nombre d'hores en un dia laborable estàndard del calendari del projecte. 

En alguns casos potser heu de desviar aquestes regles. Podeu desactivar la planificació automàtica per impedir que el Finance defineixi automàticament o corregeixi qualsevol propietats de les tasques dels nodes fulla. Quan introduïu informació per a una tasca que ocasioni una infracció de qualsevol norma, es mostra una icona d'error de planificació per a la tasca. Si no voleu que es mostrin els errors de planificació, feu clic a **Es mostren els errors de planificació** per desactivar la característica. 

> [!NOTE] 
> Els valors d'una tasca de resum o contenidor se segueixen calculant com la suma dels valors de les tasques constituents, independentment de si l'ajuda automàtica de planificació està activada o desactivada. 

**Correcció d'errors de planificació**: quan el sistema de planificació automàtica està activat, és poc probable que es produeixin errors de planificació. No obstant, si desactiveu l'ajuda de planificació automàtica i, a continuació, la torneu a activar més endavant, podria ser que apareguessin icones d'error de planificació a la WBS. 

**Correcció d'errors de planificació per tasca**: quan feu doble clic a la icona d'error de planificació per a una tasca concreta, un quadre de diàleg mostrarà tots els errors de planificació per a aquella tasca. Podeu decidir quins errors de planificació voleu corregir per a la tasca. 

**Correcció de tots els errors de planificació**: si voleu que el Finance corregeixi tots els errors de planificació a la WBS, a la subfinestra d'acció, feu clic a **Corregeix totes les discrepàncies de planificació**. 

> [!NOTE] 
> Aquesta característica pot generar modificacions significatives a la WBS. Els errors es corregeixen en l'ordre següent:

1.  Els esforços previstos en totes les tasques es modifiquen de manera que siguin iguals a la capacitat definida al calendari del projecte.
2.  La data d'inici de cada tasca es modifica de manera que la tasca s'iniciï després que finalitzin totes les tasques predecessores.
3.  La data d'inici de cada tasca es modifica per eliminar buits a les dates d'inici de les tasques predecessores.

### <a name="cost-estimation"></a>Estimació de costos

Com s'ha esmentat abans en aquest document, heu d'introduir l'estimació de costos per a cada tasca de node fulla mitjançant la pestanya **Costos i ingressos estimats** a la subfinestra inferior de la pàgina **Estructura del desglossament del treball**. 

> [!NOTE] 
> No podeu modificar l'estimació de costos per a una tasca de resum o contenidor. L'estimació de costos per a una tasca de resum és igual a la suma de l'estimació de costos de les seves tasques de node fulla. El cost total estimat per a cada tasca es calcula com la suma dels imports de cost estimats per als tipus de transacció següents:

-   Treball
-   Article o material
-   Despeses

S'utilitza un tipus de transacció **Taxa** per calcular els ingressos basats en taxes. Aquest tipus de transacció no té un component de cost i, per tant, no es té en compte quan s'estimen els costos. 

S'utilitza un tipus de transacció **A compte** per registrar el valor de venda contractat en un tipus de projecte de valor fix. Aquest tipus de transacció tampoc no es té en compte quan s'estimen els costos. 

Quan calculeu els costos per al personal, els materials i les despeses de cada tasca, heu d'assignar una categoria de projecte al cost estimat. 

**Estimació de costos de personal**: per a cada node fulla, assigneu un esforç de treball en hores i una categoria per defecte. Per tant, en configurar una planificació per a una tasca, l'estimació del cost de personal per a aquesta tasca s'afegeix automàticament a la categoria per defecte per al personal. Aquesta estimació de costos es mostra a la pestanya **Costos i ingressos estimats** a la quadrícula **Detalls de la línia** per a aquella tasca. Si necessiteu més estimacions de costos de personal, podeu afegir-les en aquesta pestanya. Si augmenteu o disminuïu les hores de l'estimació del cost del personal, es torna a calcular automàticament la planificació de la tasca. 

**Estimació de costos de despeses i materials**: la pestanya **Costos i ingressos estimats** també us permet estimar costos de despeses i materials per a una tasca, si necessiteu estimacions. 

El preu del cost i de vendes de cada línia d'estimació de personal o de despesa es basa en la configuració que es defineix per a cada categoria a les taules de preus a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Preus**. Per als articles, el preu de cost i de vendes s'afegeix per defecte de l'article o dels acords comercials de la pàgina de llista **Productes al mercat** a Administració de la informació del producte.

## <a name="tracking-progress-on-the-wbs"></a>Seguiment del progrés a la WBS
Alguns sectors segueixen el progrés d'un projecte amb una WBS a un nivell molt granular, mentre que d'altres fan el seguiment del progrés en un nivell superior de la WBS. Aquesta secció descriu com podeu utilitzar el seguiment de la WBS per als vostres requisits del projecte. 

El Finance té tres visualitzacions per a la WBS d'un projecte: la visualització Planificació, la visualització Seguiment d'esforços i la visualització Seguiment de costos.

### <a name="planning-view"></a>Visualització Planificació

La visualització Planificació mostra l'estimació planificada o de línia de la informació de planificació i de cost. Tot i que no hi ha cap funció per fer el seguiment de la versió i la línia de base per a la WBS d'un projecte, els valors d'aquesta visualització pretenen representar la versió de línia de base. Les seccions Estimació de la planificació i Estimació de costos d'aquest tema descriuen aquesta visualització i com s'utilitza per crear una WBS.

### <a name="effort-tracking-view"></a>Vista Seguiment de l'esforç

La visualització Seguiment de l'esforç mostra el seguiment del progrés de les tasques a la WBS. Compara les hores d'esforç reals acumulades per a una tasca amb les hores d'esforç planificades. Les fórmules següents proporcionen els valors de la visualització Seguiment de l'esforç:

-   Percentatge de progrés = Esforç real fins al moment ÷ Esforç planificat per a la tasca
-   Esforç restant (també conegut com a Estimació per completar \[ETC\]) = Esforç planificat – Esforç real fins al moment
-   Estimació per completar (EAC) = Esforç restant + Esforç real fins al moment
-   Variació d'esforç previst = Esforç planificat – EAC

La visualització Seguiment de l'esforç mostra una projecció de la variació de l'esforç per a la tasca en funció de si l'EAC és major o menor que l'esforç planificat:

-   Si l'EAC és major que l'esforç planificat, es preveu que la tasca comporti més temps del que s'havia planejat originalment i duu retard.
-   Si l'EAC és menor que l'esforç planificat, es preveu que la tasca comporti menys temps del que s'havia planejat originalment i va avançada.

**Nova projecció d'esforç de l'administrador de projectes**: de tant en tant, l'administrador del projecte o una altra persona que està seguint el progrés d'un projecte haurà de revisar les estimacions originals en una tasca. Pot ser que la tasca s'estigui movent més ràpidament o més lentament del que s'havia anticipat per diverses raons. Per exemple, l'àmbit s'ha reduït, o els treballadors tenen menys experiència que el previst inicialment. Les projeccions són la percepció de les estimacions d'un administrador de projecte, en funció de l'estat actual del projecte. En general, no recomanem canviar els números de la línia de base, ja que la línia de base del projecte representa un document ben publicat de les estimacions de la planificació i el cost del projecte que han acordat totes les parts interessades en el projecte. 

Hi ha dues maneres que els administradors de projectes modifiquin l'esforç de les tasques:

-   Modificar l'esforç restant que està definit automàticament per actualitzar l'esforç restant real a la tasca.
-   Modificar el percentatge de progrés que està definit automàticament per actualitzar el progrés real a la tasca.

Les dues aproximacions provoquen un nou càlcul a la tasca de l'ETC, l'EAC i el percentatge de progrés, i la variació de l'esforç projectat d'una tasca. També es torna a calcular l'EAC, l'ETC i el percentatge de progrés de les tasques de resum, i s'actualitza la variació la variació d'esforç projectat. 

**Esforç modificat en tasques de resum**: podeu modificar l'esforç en tasques de resum o contenidor. Independentment de modifiqueu aquests valors amb l'esforç restant o el percentatge de progrés de les tasques de resum, els càlculs es produeixen automàticament en l'ordre següent:

1.  El valor de l'EAC, l'ETC i el percentatge de progrés de la tasca es calculen.
2.  El nou EAC es distribueix cap a les tasques secundàries en la mateixa proporció que l'import d'EAC original.
3.  L'EAC nou en cada tasca de node fulla es calcula.
4.  L'esforç restant i el percentatge de progrés es tornen a calcular per a totes les tasques secundaris afectades, segons el nou valor de l'EAC. També es torna a calcular la variació de l'esforç de les tasques.
5.  L'EAC de les tasques resum també es torna a calcular des dels nodes fulla.

Feu clic a **Expandeix al nivell** a la visualització Seguiment de l'esforç per definir el nivell al qual fer el seguiment i mantenir la WBS. La WBS s'expandeix automàticament al nivell de la visualització Seguiment de l'esforç cada vegada que l'obriu.

### <a name="cost-tracking-view"></a>Visualització de seguiment del cost

A la visualització Seguiment de costos es mostra el seguiment del consum de costos per a una tasca. En aquesta visualització, el cost real que s'ha invertit en una tasca fins al moment es compara amb el cost planificat per a la tasca. Les fórmules següents proporcionen els valors de la visualització Seguiment de costos:

-   Percentatge de cost consumit = Cost real fins al moment ÷ Cost planificat per a la tasca
-   Cost per completar (CTC) = Cost planificat - Cost real fins al moment
-   Estimació per completar (EAC) = CTC + Cost real fins al moment
-   Variació de costos projectats = Cost previst – EAC

La visualització Seguiment de costos mostra una projecció de la variació dels costos per a la tasca en funció de si l'EAC és major o menor que el cost planificat:

-   Si l'EAC és major que el cost planificat, es preveu que la tasca costi més diners del que s'havia planejat originalment i està per sobre del pressupost.
-   Si l'EAC és menor que el cost planificat, es preveu que la tasca costi menys diners del que s'havia planejat originalment i està per sota del pressupost.

**Nova projecció del costo dels administradors de projectes**: els administradors de projectes han d'utilitzar el CTC per revisar l'estimació original del cost en una tasca. L'administrador del projecte pot modificar el valor del CTC al cost necessari per completar la tasca. Si modifiqueu el valor del CTC, el CTC de la tasca, l'EAC i el percentatge de cost consumit i la variació de costos projectada sobre una tasca es tornen a calcular. També es torna a calcular l'EAC, l'ETC i el percentatge de cost consumit de les tasques de resum, i s'actualitza la variació la variació de cost projectat. 

> [!NOTE] 
> Quan reviseu l'esforç d'una tasca de WBS a la visualització Seguiment de l'esforç, el CTC de la tasca, l'EAC, el percentatge de cost consumit i la variació de costos projectada es tornen a calcular a la visualització Seguiment de costos. No obstant, les revisions de costos no afecten els valors de la visualització Seguiment de l'esforç, ja que no es revisa el cost per tipus de transacció (personal, material o despesa) o categoria de projecte. 

**Revisió de la projecció per als costos en tasques de resum**: podeu revisar els costos en tasques de resum i els càlculs es produeixen automàticament en l'ordre següent:

1.  L'EAC, el CTC i el percentatge de cost consumit a la tasca es tornen a calcular.
2.  El nou EAC es distribueix a les tasques secundàries en la mateixa proporció que l'EAC original a les tasques.
3.  Es calcula el nou EAC per a cada tasca.
4.  El CTS i el percentatge de cost consumit es tornen a calcular per a les tasques secundàries afectades, segons el valor de l'EAC. També es torna a calcular la variació de cost de les tasques.
5.  L'EAC per a totes les tasques de resum es torna a calcular segons aquest canvi.

Feu clic a **Expandeix al nivell** a la visualització Seguiment de costos per definir el nivell al qual fer el seguiment i mantenir la WBS. La WBS s'expandeix al nivell de la visualització Seguiment de costos cada vegada que l'obriu.

### <a name="earned-value-management"></a>Administració de valor guanyat

Podeu utilitzar el mètode de valor guanyat (EVM) per fer el seguiment del progrés d'un projecte. Podeu visualitzar les mètriques de valor guanyat al Centre de funcions de l'administrador del projecte. El component de gràfic de valor guanyat mostra els valors per temps del valor planificat i el cost real. El valor guanyat a partir de la data actual es mostra com un punt. Actualment, les dades per temps per al valor guanyat no estan disponibles. 

La fase de temps del gràfic de valors guanyats es mostra per setmana o mes. Aquesta secció descriu els tres pilars de l'EVM: valor planificat, valor guanyat i cost real. 

**Valor planificat**: la teoria d'EVM afirma que el gràfic de valor planificat representa la velocitat a la qual l'equip del projecte ha planificat obtenir valor en el projecte. 

El Finance utilitza la regla d'obtenció de 0:100 quan dibuixa el valor planificat. En aquesta regla, el valor de la tasca es comptabilitza a la tasca a la data d'acabament. No es comptabilitza cap valor fins que la tasca està completada al 100 per cent. 

A Administració de projectes i comptabilitat, introduïu la data d'acabament dels nodes fulla i el cost planificat. Quan el gràfic de valor planificat es mostra per setmana, el valor planificat es resumeix a la setmana per a totes les tasques de nodes fulla durant la duració del projecte. 

**Valor obtingut**: la teoria d'EVM afirma que el gràfic de valor obtingut representa la velocitat a la qual l'equip del projecte està obtenint realment el valor en el projecte. 

El Finance utilitza la regla d'obtenció de 0:100 quan dibuixa el valor obtingut. En aquesta regla, el valor de la tasca es comptabilitza a la tasca a la data d'acabament. No es comptabilitza cap valor fins que la tasca està completada al 100 per cent. 

Quan es calcula el valor obtingut, es considerarà el percentatge de progrés de cada tasca. Sota la regla d'obtenció de 0:100, només les tasques que s'han completat en un període determinat es consideren per al càlcul del valor obtingut a partir del final del període. El valor obtingut en el projecte es calcula per a totes les tasques que s'hagin completat quan es crea el gràfic. 

> [!NOTE] 
> Actualment, el sistema per al seguiment de la WBS no té estructures de dades per emmagatzemar els percentatges de progrés històrics a cada tasca. Per tant, el valor obtingut només es pot notificar a mesura que es processa el cub. Processeu el cub periòdicament per actualitzar les dades de valor obtingut que es mostren al Centre de funcions. 

**Cost real**: la teoria d'EVM indica que la gràfica de cost real representa la velocitat a la qual s'estan gastant diners en el projecte. 

Les transaccions que es comptabilitzen en un projecte s'utilitzen per traçar la línia de cost real. Els costos es resumeixen per data. Aquestes dades s'utilitzen després per crear un gràfic dels costos reals per setmana o mes al gràfic de valor obtingut.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Com utilitzar els conceptes de valor planificat, valor obtingut i cost real

**Variació de planificació**: durant la planificació, es crea una previsió per treballar en una cronologia. Per tant, el valor planificar és la velocitat a la qual els planificadors del projecte creien que es completaria el treball en el projecte. Quan un projecte està en curs, el treball s'ha completat i el projecte proporciona valor. Si compareu el valor planificat amb el valor obtingut, podeu veure el progrés del treball en un projecte. El resultat d'aquesta comparació s'anomena variació de planificació. 

Si el valor planificat per a un període és superior al valor obtingut, la quantitat de treball que s'ha fet en un projecte és inferior al que s'ha planificat. Per tant, el projecte duu retard. Com que el valor planificat i el valor obtingut s'expressen en termes monetaris, al temps de retard en el projecte també se li dona un valor monetari. 

Si el valor planificat per a un període és inferior al valor obtingut, la quantitat de treball que s'ha fet en un projecte és superior al que s'ha planificat. Per tant, el projecte va avançat. A aquest temps d'avançament també se li dona un valor monetari.

**Variació de cost**: com que el valor obtingut utilitza el preu de cost com a multiplicador, el valor obtingut indica el cost del treball que es fa en un projecte. A mesura que avança un projecte, el registre de transaccions proporciona un registre dels diners que es gasten en el projecte. Si compareu el valor aconseguit amb el cost real, podeu visualitzar la quantitat de diners que s'estan gastant i el valor que s'obté. El resultat d'aquesta comparació s'anomena variació de cost. 

Si el cost real que es gasta durant un període és superior al valor obtingut, s'han gastat més diners que els obtinguts. Per tant, el projecte està per sobre del pressupost. 

Si el cost real que es gasta durant un període és inferior al valor obtingut, s'han obtingut més diners que els gastats. Per tant, el projecte està per sota del pressupost.

## <a name="wbs-templates"></a>Plantilles de WBS
Podeu utilitzar la funcionalitat de plantilles de WBS per crear plantilles estàndard per als projectes. Si els projectes que ofereix la vostra empresa impliquen molta feina repetible, heu de tenir en compte la creació d'una plantilla de WBS. 

Podeu crear una plantilla de WBS des de la WBS d'un projecte existent, de manera que els coneixements i les bones pràctiques que s'hagin recopilat durant la planificació del projecte puguin tornar-se a utilitzar en projectes semblants en el futur. No obstant això, de vegades, pot ser que no tingui sentit desar tota la WBS com a plantilla. Per tant, també podeu crear plantilles a partir de les parts de la WBS per a un projecte.

### <a name="saving-a-projects-wbs-as-a-template"></a>Desar la WBS d'un projecte com a plantilla

Després de crear una plantilla, podeu importar-la a la WBS d'un altre projecte al node arrel o bé en qualsevol tasca de la WBS del projecte.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importar una plantilla de WBS en la WBS d'un projecte

Quan importeu tasques, les tasques de la plantilla s'organitzen segons la data d'inici de la tasca a la qual s'importen. Durant la importació, les relacions de predecessors de les tasques de la plantilla s'utilitzen per calcular les dates d'inici de les tasques importades. El calendari de treball estàndard del projecte de destinació s'aplica per calcular les dates finals de les tasques importades, de manera que es conserven els dies laborables i les hores de feina habituals definides al calendari de treball del projecte actual. 

Els imports de costos i els preus de venda de les línies estimades s'apliquen per garantir que els preus específics per al projecte o el contracte de projecte tinguin dates vàlides.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Diferències entre la WBS d'un projecte i una plantilla de WBS

-   Les tasques d'una plantilla de WBS no tenen dates d'inici i d'acabament.

Els dies laborables i no hàbils no es defineixen per a les plantilles de WBS.

-   Les plantilles de WBS sempre utilitzen el calendari de planificació que es configura com a calendari per defecte per a tots els projectes.

El calendari de planificació per defecte només s'utilitza per esbrinar les hores en un dia hàbil normal.

-   Les relacions de predecessor no es copien a una plantilla de WBS.

Com que les plantilles de WBS no tenen dates, la lògica de data d'inici basada en la data de finalització del predecessor no és necessària.

-   Una línia d'estimació del cost de personal es crea automàticament quan es crea una tasca en una plantilla de WBS. El preu de venda i l'import de la despesa es copien al treballador seleccionat.

Els costos de despeses i articles es poden crear manualment, de la mateixa manera que la WBS d'un projecte.

-   Els errors de planificació es mostren quan hi ha desviacions de la següent fórmula:

Esforç = Nombre de recursos × Duració × Nombre d'hores en un dia hàbil normal 

Podeu corregir tots els errors de planificació a la vegada fent clic a **Corregeix tots els errors de planificació**. 

Alternativament, podeu corregir els errors de planificació individualment fent clic a la icona d'advertiment per a cada tasca.





[!INCLUDE[footer-include](../includes/footer-banner.md)]