---
title: Novetats o canvis al Project Service Automation versió 3
description: En aquest tema es proporciona informació sobre les novetats i els canvis a la versió 3 del Project Service Automation.
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 15925cb88cc413f9a23a25e89ddd29668e9171de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581640"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Novetats o canvis al Project Service Automation versió 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]



En aquest tema es proporciona informació sobre els canvis en la interfície d'usuari (UI), la funcionalitat i la terminologia al Project Service Automation entre la versió 2 o la versió 1 i la versió 3.

## <a name="project-scheduling"></a>Planificació de projectes
La planificació del projecte, que es coneixia com a estructura de desglossament de treball (WBS) en versions anteriors, ha canviat el nom a planificació i s'hi accedeix fent clic a la pestanya **Planificació**. 

![Planificació del projecte.](media/psa-schedule-01.png)

La planificació ara té una nova superfície per a la interacció que és moderna i accessible. No obstant, el motor de planificació del Project Service Automation subjacent no ha canviat. Els botons de control de la franja de la quadrícula de planificació us permeten interactuar amb la planificació de manera similar a la versió anterior del Project Service Automation. Els canvis addicionals a la planificació inclouen:

- **Diagrama de Gantt**: el diagrama de Gantt ja no està present. Una visualització de Gannt nova tornarà en una actualització futura.
- **Capçaleres de columna**: podeu amagar les capçaleres de columna de la quadrícula fent clic a l'indicador cap avall al costat del títol de la columna. 
- **Columnes**: podeu mostrar les columnes amagades fent clic a **Afegeix columna**. 
- **Categoria de la transacció**: una cerca de **Categoria la de transacció** s'ha afegit a la quadrícula de planificació i es mostra per defecte. 
 
## <a name="project-templates"></a>Plantilles de projecte
S'han fet canvis següents a la funcionalitat de la plantilla del projecte.

### <a name="create-a-project-template"></a>Crear una plantilla de projecte 
Podeu crear una plantilla de projecte a la versió 3 semblant a les versions anteriors del Project Service Automation. La plantilla només pot contenir una planificació i la planificació pot incloure assignacions, però no són necessàries. Si la planificació té assignacions, només poden ser per a recursos genèrics. Podeu generar requisits de recurs per als recursos genèrics, però no es poden reservar amb recursos reals a la plantilla. No podeu reservar un recurs real a un equip d'una plantilla. 

### <a name="create-a-template-from-an-existing-template"></a>Crear una plantilla a partir d'una plantilla existent
Quan creeu una nova plantilla de projecte a partir d'una plantilla existent a la versió 3 del Project Service Automation, passa el següent: 

- La planificació del projecte d'origen es copia a la plantilla. 
- Els recursos genèrics es copien a l'equip i es copien les assignacions de recursos genèrics. Els requisits dels recursos genèrics no es copien. 

### <a name="create-a-template-from-an-existing-project"></a>Crear una plantilla a partir d'un projecte existent
Quan creeu una nova plantilla de projecte a partir d'un projecte existent, passa el següent: 

- La planificació del projecte d'origen es copia a la plantilla. 
- Els recursos genèrics es copien a l'equip i es conserven les assignacions de recursos genèrics. Els requisits dels recursos genèrics no es copien.    
- Els recursos amb nom, tant assignats com no assignats, s'eliminen de l'equip i se substitueixen per recursos genèrics.
- Si està present, se suprimeix la informació del client. 
- Si està present, les referències a ofertes i contractes se suprimeixen. 

### <a name="create-a-project-from-a-template"></a>Crear un projecte a partir d'una plantilla
Quan creeu una nova plantilla de projecte a partir d'una plantilla existent a la versió 3 del Project Service Automation, passa el següent:

- La planificació, l'equip i les assignacions es copien al nou projecte.   
- La data d'inici és o bé la data de còpia o la data seleccionada per l'usuari.   
- Per als membres de l'equip genèrics que tenen requisits de recurs a la plantilla, els requisits no es copien ni es generen automàticament. Haureu de generar-los. 

## <a name="copy-a-project"></a>Copiar un projecte
A la versió 3 del Project Service Automation, en copiar un projecte, passa el següent: 

- La data prevista d'inici es copia, però es pot canviar.  
- La planificació del projecte i les tasques es copien. 
- Els recursos genèrics i les seves assignacions es copien. Els requisits de recurs dels recursos genèrics no es copien. Haureu de tornar a generar-los. 
- Els recursos reals i les seves assignacions no es copien. En comptes d'això, es substitueixen per recursos genèrics. 
- Els valors reals no es copien al nou projecte. 

## <a name="move-a-scheduled-project"></a>Desplaçar un projecte planificat
Quan moveu la planificació d'un projecte existent cap endavant, passa el següent: 

- Les dates de les tasques es mouen automàticament per correspondre's amb el període de moviment. 
- Els recursos genèrics assignats romanen assignats.   
- Si es generen abans que el projecte s'hagi mogut, els requisits per al recurs genèric es conserven i no es tornen a generar automàticament. Haureu de tornar a generar-los per reflectir les noves assignacions a causa del moviment de tasques. 
- Les assignacions sobre recursos reals canvien per correspondre amb el moviment de la data de la tasca. Les reserves en recursos reals no canvien. Caldrà que modifiqueu les reserves mitjançant la visualització de conciliació. 
- Els recursos de l'equip amb reserves però sense assignacions no canvien. 
- Els valors reals no es mouen. 

## <a name="estimates"></a>Estimacions
Les estimacions s'han dividit en dues pestanyes, **Assignació de recursos** i **Estimacions**. La pestanya **Assignació de recursos** conté les estimacions d'esforç i mostra les assignacions de recursos de les tasques en una visualització per temps. Podeu editar les estimacions en funció del que ha generat el motor de planificació.

![Pestanya Assignacions de recursos mostrant les estimacions d'esforç i assignacions de recursos per a les tasques.](media/resource-assignments-tab-02.png)

A la pestanya **Estimacions** es mostren els imports de costos i de vendes de les assignacions de recursos. Els imports són només de lectura. El preu de costos i de vendes estan ara basats en les assignacions dels membres de l'equip a la planificació. Això vol dir que si teniu una tasca sense assignació, la tasca es mostrarà sota el dipòsit no assignat. Això també significa que sense **funció**, que és una dimensió de preus per defecte, no hi haurà cap cost o venda aproximada si teniu un client o un contracte/oferta associat amb el projecte. 

![Pestanya d'estimacions mostrant els imports de cost i vendes.](media/estimates-tab-03.png)
  
També s'admet una categoria a les tasques a la visualització de planificació. L'agrupament per categoria a la visualització per temps de les estimacions proporcionarà una millor experiència, especialment quan també teniu estimacions de despesa en el projecte. Les estimacions de despesa s'introdueixen mitjançant una quadrícula en una pestanya separada. 

Les estimacions de despesa es poden introduir a la quadrícula a la pestanya **Estimacions de despesa**. 

![Pestanya d'estimacions de despesa mostrant la quadrícula d'estimacions de despesa.](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Administració de recursos
A la versió 3 del Project Service Automation, amb la nova interfície unificada del client i els canvis en la relació entre reserves i assignacions, afegir personal a un projecte amb recursos genèrics o reals ha canviat enormement de la versió 2 i de la versió 1. No obstant això, els conceptes de recursos que es poden reservar, tant **reals** com **genèrics**, continuen sent els mateixos, igual que els membres de l'equip, els requisits, les assignacions i les reserves.   

![Utilitzar el selector de recursos.](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Assignar un recurs real que es pot reservar 
A la versió 3 del Project Service Automation, les reserves i assignacions de tasques no estan tan estretament entrellaçades com en versions anteriors del Project Service Automation. Podeu utilitzar la quadrícula de l'equip per reservar un membre de l'equip **real**, similar al dins del mercat.

Mitjançant el selector de recursos de la planificació, podeu seleccionar el membre de l'equip creat a la visualització de l'equip i després assignar-los a tasques. Podeu continuar assignant-los tasques, fins i tot més enllà de les seves reserves. Utilitzeu la pestanya **Conciliació** per conciliar els membres de l'equip que tenen diferències en les reserves i les assignacions.

El selector de recursos mostrarà els membres de l'equip per al projecte. També podeu utilitzar el selector de recursos per cercar i visualitzar altres recursos que no formen part de l'equip del projecte. Podeu assignar-los a una tasca i passaran a formar part de l'equip del projecte. Haureu de reservar-los mitjançant la pestanya **Tauler de planificació** o **Conciliació**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Assignar un recurs genèric que es poden reservar a un equip de tasques i projectes i, a continuació, complir-lo amb un recurs real mitjançant el tauler de planificació 
A la versió 3 del Project Service Automation, la funcionalitat de generació d'equips no s'utilitza per als recursos genèrics. En lloc d'això, podeu crear i assignar directament un recurs genèric des de la planificació escrivint el nom del càrrec del recurs genèric a la cel·la de recursos de la planificació. O bé, podeu seleccionar la icona de recurs a la cel·la i, a continuació, utilitzant el selector de recursos, escriure el nom del recurs genèric que voleu crear. S'obrirà una subfinestra de creació ràpida que us permet definir la unitat de funció i organització del membre de l'equip de recursos genèric. Després de crear el recurs, s'assigna a la tasca i podeu continuar assignant aquest recurs genèric a altres tasques de la planificació.    
 
Quan hagueu assignat el recurs a totes les tasques adequades, podeu generar un requisit de recurs i, a continuació, complir-lo per reserva directa amb el **Tauler de planificació** o mitjançant la presentació d'una sol·licitud de recursos. També podeu afegir recursos genèrics directament a la quadrícula de membres de l'equip. 

Els recursos genèrics s'afegeixen a l'equip del projecte sense requisits de recurs i amb les dates d'inici/finalització del projecte fins que es genera un requisit de recursos. Per generar un requisit, seleccioneu el recurs genèric i feu clic a **Genera**. L'enllaç de requisit es visualitza ara i les hores requerides s'emplenaran amb les hores assignades. Podeu fer clic a l'enllaç per obrir i actualitzar el requisit.
  
Quan la reserva s'hagi completat i complert totalment per un recurs amb nom, el recurs genèric se substitueix pel recurs amb nom i l'assignació de la planificació s'actualitza amb el recurs amb nom. 

Els recursos proposats per als requisits ara s'emmagatzemen en una pestanya en comptes d'una secció separada.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Diversos recursos amb nom que compleixen un recurs genèric
Quan s'ha complert un requisit amb diversos recursos, el recurs genèric es manté a l'equip i s'assigna a la tasca. Els membres de l'equip amb nom que estan reservats no s'assignaran com a part del càrrec. L'administrador del projecte pot assignar la feina segons calgui als recursos reals.  La visualització **Conciliació** proporciona un desglossament de les reserves en diversos recursos a diverses assignacions de tasques. Això no es fa de manera automàtica perquè en escenaris més complicats, com ara un on teniu un paquet de tasques que constitueixen el requisit, cal suposar la intenció de com vol assignar-ho l'administrador del projecte. Com que el sistema no pot entendre la intenció, és probable que les hipòtesis siguin diferents del previst i que es produeixi un resultat incorrecte o impredictible. El resultat predictible és que el recurs genèric es manté assignat fins que l'administrador del projecte assigna deliberadament els recursos mitjançant la visualització **Conciliació**.

### <a name="reconciliation"></a>Conciliació
A la pestanya **Conciliació** es mostren les reserves i totes les assignacions de cada membre de l'equip del projecte. La visualització mostra les hores a les cel·les que poden representar punts de temps de mesos a dies. Aquesta visualització permet als administradors de projectes conciliar les reserves dels membres de l'equip i els seus treballs per a l'equip del projecte. Això és útil perquè les reserves i assignacions de tasques no estan estretament acoblades, la qual cosa permet més flexibilitat en la planificació d'un projecte. 

![Pestanya Conciliació mostrant les reserves i assignacions dels membres de l'equip del projecte.](media/resource-reconciliation-tab-06.png)

Per a cada recurs, la visualització pren la diferència entre les reserves d'un membre de l'equip i un informe de les assignacions de tasques i mostra les dues diferències següents que poden ocórrer amb les reserves i les assignacions d'un projecte: 

- **Manca de reserves**: les manques de reserves es produeixen quan un recurs té més assignacions que reserves. Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot corregir-ho ampliant les reserves del recurs fins a cobrir el dèficit. 
- **Excés de reserves** un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques.  Això pot ser una ocurrència acceptable, per exemple, si el recurs s'ha reservat abans de l'assignació de tasques. No obstant, en altres casos, pot ser que el recurs no estigui pensat per assignar-se i l'administrador del projecte hauria de considerar la possibilitat de cancel·lar les reserves del recurs per permetre l'ús de la capacitat en un altre projecte. 

Quan teniu assignacions de tasques per a un recurs sense reserves (una manca de reserves), podeu seleccionar la manca de reserves agregada i fer clic a **Estén la reserva**. Des d'aquí, podeu visualitzar la reserva necessària per fer front a la manca del recurs i a la seva disponibilitat. 
 
## <a name="time-and-expense"></a>Temps i despesa
En aquesta secció es proporciona informació sobre els canvis en el temps, la despesa i l'aprovació a la versió 3 del Project Service Automation. Com a part de la solució del Dynamics 365 Project Service Automation, s'ha actualitzat la característica **Entrada de temps** per aprofitar el marc de la interfície unificada. Això permet el lliurament d'una interfície d'usuari coherent i homogènia que segueix el disseny responsiu per a una òptima visualització en qualsevol mida de pantalla o dispositiu. 

### <a name="landing-page"></a>Pàgina de destinació
L'experiència d'entrada de temps personalitzada no extensible ha quedat obsoleta a la versió 3. En lloc d'això, ara hi ha una experiència de quadrícula nativa extensible i accessible. Podeu accedir a la funcionalitat d'entrada de l'hora mitjançant el mapa del lloc de l'esquerra. Amb aquest canvi, ja no podreu introduir el temps d'una setmana a la vegada. En lloc d'això, haureu de crear una entrada de temps per a cada dia a la quadrícula. Després de crear un parell d'entrades de temps, els usuaris poden crear de manera massiva les entrades de temps amb la funció **Copia** explicada més endavant en aquest tema. 

![Pàgina de destinació d'entrada de temps.](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Crear entrades de temps noves 
Feu clic a **Nova** a la franja per obrir una pàgina de creació ràpida per a una entrada de temps en la qual introduïu la duració en minuts, hores o dies. Per fer-ho, comenceu a escriure h, m o d juntament amb la quantitat.  

![Creació ràpida d'entrades de temps.](media/quick-create-time-entry-08.png)

Els camps de cerca es basen en visualitzacions del sistema. Per exemple, després d'introduir la informació d 'un projecte, el camp **Tasca del projecte** el defineix per defecte la visualització **Les meves tasques de projecte obertes**. Per crear entrades de temps per a les tasques que no s'assignen a l'usuari, feu clic a **Canvia la visualització** a la cerca i seleccioneu **Totes les tasques de projecte actives**. Després d'haver creat l'entrada de temps i que es mostri a la quadrícula, podeu editar tots els valors de la línia directament a la quadrícula.  

### <a name="bulk-createcopy"></a>Creació/còpia massiva 
Després de crear algunes d'entrades de temps, podeu utilitzar la funcionalitat de còpia per crear entrades de temps addicionals massivament. Feu clic a **Copia** per obrir el diàleg **Copia**. A **Del període: data d'inici**, definiu l'interval de dates des del qual s'han de copiar els períodes de temps. A **Al període: data d'inici**, especifiqueu la data per a la qual s'han de crear les entrades de temps. Feu clic a **Copia** per copiar les entrades de temps al dia corresponent de la setmana indicat a **Al període**. Per exemple, l'entrada de temps del dilluns de la setmana passada es copiarà al dilluns de la setmana indicada a **Al període**. 

![Copiar entrades de temps massivament.](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importa dades 
Les assignacions i els intercanvis segueixen el mateix patró de la interfície d'usuari, cosa que permet a l'usuari especificar l'interval de dates des del moment en què s'han d'importar. A continuació, heu de triar explícitament les reserves que s' han de copiar en entrades de temps en **Esborrany**. A la versió 3, ja no podeu veure el patró de les entrades de temps **Suggerida** a la quadrícula i el calendari.  

### <a name="change-in-calendar-control"></a>Canvia al control de calendari
A la versió 3, hem abandonat el control de calendari personalitzat i ara s'utilitza el calendari UC per mostrar les entrades de temps de la setmana. Amb aquest calendari, podeu visualitzar el dia, la setmana i el mes. 

> [!NOTE]
> Una limitació del calendari és que aquest control no admet accions sobre els elements de calendari individuals. Per exemple, no podreu seleccionar un o diversos elements de calendari i enviar o suprimir aquests elements. En fer clic en un element del calendari s'obrirà la pàgina **Entitat d'entrada de temps** per a les accions addicionals. 

### <a name="extensibility"></a>Capacitat d'ampliació
**Captura dades dels camps personalitzats només a les entitats de temps i de despesa**: l'entrada de temps utilitza una quadrícula editable, una quadrícula només de lectura i controls de calendari de la plataforma. Tots aquests controls són natius i, per tant, seran compatibles amb les personalitzacions. A la versió 3 del Project Service Automation, podeu afegir camps addicionals personalitzats, configurar camps de cerca i donar-los suport amb visualitzacions personalitzades. També podeu definir una lògica empresarial personalitzada en funció dels valors seleccionats dels camps personalitzats.  

**Captura dades dels camps personalitzats a l'entrada de temps i de despeses i difon-les per mitjà d'entitats que suportin el flux d'enviament i d'aprovació**: el processament típic de les entrades de temps es mostra al diagrama següent.

![Processament d'entrades de temps.](media/process-time-entries-10.png)

Si els requisits de negoci estipulen que les entitats de temps i de despeses han de capturar dimensions de preus personalitzades i propagar els valors definits per un temps i un recurs d'entrada a la dimensió de preus personalitzats a través de totes les entitats del gràfic anterior, vegeu [Configurar els camps personalitzats com a dimensions de preus](set-up-pricing-dimensions.md)

Per donar suport als requisits empresarials en què les entitats de temps i de costos han de capturar dimensions que no són de preus personalitzades i de propagar els valors, podeu utilitzar les dimensions de la configuració de preus i expressar les dimensions personalitzades com a dimensions de preus sense cost ni tarifa de facturació. Un altre escenari seria afegir un camp personalitzat a cadascuna de les entitats, amb el mateix nom de camp a totes les entitats. Els complements de personalització es poden crear per relacionar els registres de les entitats que participen al flux de presentació i aprovació mitjançant les entitats d'origen de la transacció i connexió de la transacció.  

### <a name="delegate-time-and-expense-entry"></a>Delegar entrades de temps i despeses
La plataforma del Common Data Service no permet que un usuari en suplanti a un altre, la qual cosa significa que en la versió 3 del Project Service Automation no hi ha cap suport per a entrades de temps i despeses delegades. No obstant, els associats i els clients tenen una solució activa per habilitar la compatibilitat amb les experiències d'entrada de temps delegades a la versió 3. Es tracta només d'una solució alternativa i no d'una solució completa, per la qual cosa és important entendre les limitacions i només utilitzar aquest enfocament si les limitacions són acceptables. 

> [!IMPORTANT]
> Aquesta informació només s'hauria de considerar una orientació suggerida per a la implementació personalitzada d'un associat o client. L'equip del producte no ofereix assistència formal per a aquesta funcionalitat a través de cap dels nostres canals de suport.

### <a name="customization-details"></a>Detalls de personalització 
La personalització us permet afegir **Recursos que es poden reservar** a les experiències de creació i edició, la qual cosa permetrà a l'usuari actuar com a delegat canviant el camp **Recurs de reserva** a un altre usuari per al qual s'han de registrar les entrades de temps i de despesa. En els passos següents es cobreix la delegació d'entrada de temps. La mateixa informació s'aplica a la delegació de l'entrada de despeses. 
 
1.  Assegureu-vos que l'usuari delegat tingui accés de seguretat global a projectes i tasques de projecte. 
1.  Com que el **Recurs que es pot reservar**, que és un camp de l'entitat **Entrada de temps**, no s'exposa a la pàgina **Creació ràpida**, heu d'afegir-la.

    -o bé-

    Creeu una visualització personalitzada que inclogui la columna **Recurs reservable** per visualitzar només les entrades de temps creades per al recurs. Publiqueu les personalitzacions al dissenyador de mòduls de l'aplicació perquè aquesta visualització es mostri al **Selector de visualització** a la pàgina **Entrades de temps**. Hi ha dos complements que gestionen la configuració de l'administrador per a entrades de temps que no són del projecte:

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Creeu un complement nou per sobreescriure el camp **Administrador** amb l'administrador de l'usuari assignat al camp **Recurs que es pot reservar**. Utilitzeu la mateixa **Fase d'execució** que la del complement (prevalidació) fora de banda (OOB) i l utilitzeu un **Ordre d'execució** més alt que els complements OOB (més gran que 1). Això assegurarà que el complement personalitzat s'executi després dels complements OOB.  
 
### <a name="end-user-experience"></a>Experiència de l'usuari final
1.  Quan creeu una entrada de temps a la pàgina de creació ràpida, introduïu el projecte i els detalls de la tasca de projecte i, a continuació, trieu l'usuari en el camp **Recurs que es pot reservar** per al qual cal registrar les entrades de temps. 
2.  Per defecte, aquest camp s'aplica a l'usuari amb la sessió iniciada, però tenint en compte que l'usuari ha substituït aquest camp, ara es crea l'entrada de temps per al **Recurs que es pot reservar** que s'ha seleccionat.
3.  Quan envieu les entrades de temps que heu creat per a aquests registres, les entrades s'afegiran a la cua per a l'aprovador al projecte tal com s'esperava. 
4.  Quan es recuperin les entrades de temps creades per a l'altre usuari, les entrades de temps es tornaran a l'estat **Esborrany** amb el camp **Recurs que es pot reservar** definit a l'altre usuari. 
5.  Opcionalment, podeu canviar a la visualització personalitzada per filtrar les entrades de temps creades per a l'altre usuari. 
 
### <a name="limitations"></a>Limitacions
La funcionalitat **Copia** i **Importa** només funciona en el context de l'usuari que ha iniciat la sessió. Això vol dir que no és possible copiar o importar entrades de temps que es creen per a l'usuari que ha iniciat la sessió com a recurs que es pot reservar.

Les entrades de temps que no són per a un projecte seran encaminades per a l'aprovació de l'administrador del recurs que es pot reservar només si pas 4 a la secció **Detalls de personalització** anterior s'ha completat. Altrament, les entrades de temps que no són del projecte per a l'altre usuari es dirigiran incorrectament a l'administrador de l'usuari que ha iniciat la sessió. 

### <a name="other-changes"></a>Altres canvis 
La funcionalitat **Reserves i tasques** s'ha eliminat. 

## <a name="multidimensional-pricing"></a>Preus multidimensionals
Per maximitzar la flexibilitat i complir diferents requisits empresarials, la versió 3 del Project Service Automation admet l'aplicació discreta dels conjunts de dimensions de preus per a les tarifes de cost i de facturació. Els valors de les dimensions es poden definir com a per defecte i després propagar-los pel procés de costos i preus de generació de perfils de recursos a l'entrada de temps per projectar valors reals. La configuració específica del client i la modificació o extensió aprofita la infraestructura de personalització estàndard.

El Project Service Automation inclou un conjunt per defecte de dimensions i funcions de preus i unitats de recursos, i permet la configuració dels preus i els costos per a cada combinació de funció i unitat organitzativa.

Per als clients del Project Service Automation que volen continuar utilitzant aquests camps de fàbrica com a dimensions de preus a la versió 3, no hi haurà cap canvi observable. Podeu continuar utilitzant el Project Service Automation com de costum. Tanmateix, si heu de tenir un preu o un cost per als recursos que utilitzen altres atributs addicionals, la versió 3 permet afegir les vostres pròpies dimensions de preus personalitzades al Project Service Automation. L'extensió de les dimensions de preu personalitzades és una experiència de configuració complicada. 

## <a name="quotes-and-contracts"></a>Ofertes i contractes
A la versió 3 del Project Service Automation, s'han canviat aspectes d'organització i gestió per a ofertes i contractes. A les seccions següents es proporciona informació més detallada.

### <a name="set-up-chargeability-options"></a>Configurar les opcions d'imputabilitat
A les versions 1 i 2, la configuració de la imputabilitat per a les funcions i les categories d' ofertes i contractes específics es feia mitjançant la visualització **Imputabilitat** que es trobava a la part superior de navegació d'una línia d'oferta o d'una línia de contracte. També era on podíeu configurar els preus d'aquestes funcions i de les categories de despeses.

A partir de la versió 3, la configuració de les opcions d'imputabilitat per categoria de funció i de despesa es realitzarà a nivell d'oferta o de línia de contracte. La configuració de preus és independent de la configuració de la imputabilitat. Podreu trobar **Funcions imputables** i **Categories imputables** com a pestanyes a les pàgines **Línia d'oferta** i **Línia de contracte** sense haver d'utilitzar la navegació superior.

![Funcions imputables.](media/chargeable-12.png)
 
La configuració de les funcions i categories imputables també aprofita el control de quadrícula editable per defecte. Per a cada funció i categoria, les opcions admeses per a tipus de facturació durant la fase d'ofertes i de contractació es mantenen inalterades des de les versions anteriors com a **Imputable** i **No imputable**. **Gratuït** no és un tipus permès durant la fase de d'oferta o de contractació. **Gratuït** només s'admet durant l'aprovació de temps o despesa.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Crear i editar els preus personalitzats d'una oferta i d'un contracte de projecte del Project Service Automation
A les versions 1 i 2, l'ús de la llista de preus personalitzades per a ofertes i contractes específics es feina mitjançant **Edita els preus** a la visualització **Imputabilitat**. La visualització **Imputabilitat** es situava a la navegació superior d'una línia d'oferta o d'una línia de contracte. També era on podíeu configurar les opcions d'imputabilitat de funcions o categories de despeses.

A partir de la versió 3, la creació i l'ús d'una llista de preus de projecte personalitzada en una oferta del Project Service Automation i un contracte de projecte del Project Service Automation s'ha separat de la configuració d'imputabilitat. Els contractes d'oferta del Project Service Automation i de projecte del Project Service Automation tenen una pestanya nova anomenada **Llistes de preus del projecte**. En aquesta pestanya es mostra una visualització associada de totes les llistes de preus del projecte que s'adjunten al contracte de l'oferta o del projecte del Project Service Automation. Per crear una llista de preus personalitzada a partir d'una llista de preus existent que ja està associada a l'oferta o el contracte del projecte, feu clic a **Crea preus personalitzats**. Això farà una còpia de totes les llistes de preus associades i l'adjuntarà a l'oferta o el contracte. Ara podeu obrir la llista de preus i editar el preu de la categoria de la funció o de la despesa per tal que els canvis de preus només s'apliquin a aquesta oferta o contracte. 
  
La gràfica següent és abans que s'hagin creat llistes de preus personalitzades.

![Abans de les llistes de preus personalitzades.](media/before-custom-price-lists-13.png)

La gràfica següent és després que s'hagin creat llistes de preus personalitzades.

![Després de llistes de preus personalitzades.](media/after-custom-price-lists-14.png)

> [!NOTE]
> Pot ser que es produeixi un retard breu entre quan feu clic a **Crea preus personalitzats** i quan es crea la llista de preus personalitzada. Es recomana refrescar la quadrícula en comptes de fer clic diverses vegades. S'ha creat una llista de preus personalitzada si el nom de la llista de preus associada té el nom de l'oferta o el nom del contracte del projecte afegit.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
