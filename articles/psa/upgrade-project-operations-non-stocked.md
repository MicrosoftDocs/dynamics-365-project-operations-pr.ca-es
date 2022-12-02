---
title: Actualització del Project Service Automation al Project Operations
description: En aquest article es proporciona informació general sobre el procés d'actualització des del Microsoft Dynamics 365 Project Service Automation al Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/11/2022
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: ac2435c99f3aa9b2a6cdb08d7ce5f6628e7f6ac4
ms.sourcegitcommit: bea5f9b4066277344add1da3a1567ed56a0cfd31
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/02/2022
ms.locfileid: "9736654"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualització del Project Service Automation al Project Operations

Ens complau anunciar la segona de tres fases per actualitzar del Microsoft Dynamics 365 Project Service Automation al Microsoft Dynamics 365 Project Operations. En aquest article es proporciona informació general per als clients que s'embarquen en aquest emocionant viatge. 

El programa d'entrega de l'actualització es dividirà en tres fases.

| Entrega de l'actualització | Fase 1 (gener de 2022) | Fase 2 (novembre de 2022) | Fase 3 (abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| Cap dependència en l'estructura del desglossament del treball (WBS) per als projectes | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Una WBS dins dels límits admesos actualment del Project Operations | | :heavy_check_mark: | :heavy_check_mark: |
| Una WBS fora dels límits admesos actualment del Project Operations, incloent-hi la compatibilitat amb el Project Desktop Client | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Característiques del procés d'actualització 

Com a part del procés d'actualització, hem afegit registres d'actualització al mapa del lloc per permetre als administradors diagnosticar més fàcilment els errors. A més de la nova interfície, s'afegiran regles de validació noves per garantir la integritat de les dades després d'una actualització. Les validacions següents s'afegiran al procés d'actualització.

| Validacions | Fase 1 (gener de 2022) | Fase 2 (novembre de 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| La WBS es validarà vigilant les infraccions de la integritat de les dades comunes (per exemple, assignacions de recursos associades amb la mateixa tasca principal, però amb diferents projectes principals). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS es validarà amb els [límits coneguts del Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| La WBS es validarà amb els límits coneguts del Project Desktop Client. | |  | :heavy_check_mark: |
| Els recursos que es poden reservar i els calendaris del projecte s'avaluaran amb les excepcions de regles de calendari incompatibles habituals. | | :heavy_check_mark: | :heavy_check_mark: |

En la fase 2, per als clients que actualitzin al Project Operations s'actualitzaran els projectes existents a una experiència només de lectura per a la planificació de projectes. En aquesta experiència només de lectura, la WBS completa estarà visible a la quadrícula de seguiment. Per editar la WBS, els administradors de projecte poden seleccionar [**Converteix**](/PSA-Upgrade-Project-Conversion.md) a la pàgina principal del projecte. Aleshores, un procés en segon terme actualitza el projecte per tal que admeti l'experiència de planificació del projecte nova des del Project for the Web. Aquesta fase és adient per als clients que tenen projectes que s'ajusten als [límits coneguts del Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

En la fase 3, s'afegirà la compatibilitat amb el Project Desktop Client, en benefici dels clients que vulguin continuar editant els seus projectes des d'aquesta aplicació. No obstant, si els projectes existents es converteixen a la nova experiència de Project for the Web, l'accés al complement estarà inhabilitat per als projectes convertits.

## <a name="prerequisites"></a>Requisits previs

Per optar a l'actualització de la fase 1, heu de complir els criteris següents:

- L'entorn de destinació no pot contenir cap registre de l'entitat **msdyn_projecttask**.
- Cal assignar llicències vàlides del Project Operations a tots els usuaris actius. 
- Heu de validar el procés d'actualització en almenys un entorn no productiu que contingui un conjunt de dades representatiu alineat amb l'entorn de producció.
- L'entorn de destinació s'ha d'actualitzar a la versió 37 de l'actualització del Project Service Automation (V3.10.58.120) o posterior.

Per optar a l'actualització de la fase 2, heu de complir els criteris següents:

- Cal assignar llicències vàlides del Project Operations a tots els usuaris actius. 
- Heu de validar el procés d'actualització en almenys un entorn no productiu que contingui un conjunt de dades representatiu alineat amb l'entorn de producció.
- L'entorn de destinació s'ha d'actualitzar a la versió 37 de l'actualització del Project Service Automation (V3.10.58.120) o posterior.
- Els entorns que contenen tasques (msdyn_projecttask) només estan admesos si el nombre total de tasques per projecte és de 500 o menys.

Els requisits previs per a la fase 3 s'actualitzaran quan s'acosti la data de disponibilitat general.

## <a name="licensing"></a>Llicències

Si teniu llicències actives per al Project Service Automation, podeu instal·lar i utilitzar el Project Operations, que inclou totes les capacitats del Project Service Automation, entre altres. D'aquesta manera, podeu provar les capacitats del Project Operations mentre continueu utilitzant el Project Service Automation en la producció. Quan caduquin les llicències del Project Service Automation, haureu d'habilitar la transició al Project Operations. Quan planifiqueu aquesta transició, heu de tenir en compte que la llicència del Project Operations no inclou la llicència del Project Service Automation. Els clients que tenen escenaris en els quals han implementat el Project Service Automation i que han de continuar utilitzant o augmentar les seves llicències per a PSA però tenen previst passar al Project Operations, poden sol·licitar llicències de PSA temporals basades en llicències adquirides per al Project Operations. S'emetrà una llicència del Project Service Automation per a una llicència del Project Operations. Es poden sol·licitar llicències de PSA temporals mitjançant aquest enllaç: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Proves i refactorització de personalitzacions

Com a punt de partida, importeu totes les personalitzacions en un entorn net del Project Operations (Lite) per confirmar que la importació s'ha completat correctament i que les operacions empresarials es comporten com s'espera.

Aquestes són algunes de les coses que heu de tenir en compte:

- Pot ser que la importació falli a causa de les dependències que falten. En altres paraules, les personalitzacions fan referència a camps o altres components que s'han eliminat al Project Operations. En aquest cas, suprimiu aquestes dependències de l'entorn de desenvolupament.
- Si les solucions no administrades i administrades inclouen components que no estan personalitzats, suprimiu-los de la solució. Per exemple, quan personalitzeu l'entitat **Projecte**, afegiu només la capçalera de l'entitat a la solució. No hi afegiu tots els camps. Si heu afegit anteriorment tots els subcomponents, pot ser que hàgiu de crear manualment una solució nova i afegir-hi els components rellevants.
- És possible que els formularis i les visualitzacions no es mostrin com està previst. En algunes circumstàncies, si heu personalitzat algun dels formularis o visualitzacions estàndard, les personalitzacions podrien impedir que tinguin efecte les actualitzacions noves del Project Operations. Per identificar aquests problemes, us recomanem que reviseu en paral·lel una instal·lació neta del Project Operations i una instal·lació del Project Operations que inclogui les personalitzacions. Compareu els formularis que s'utilitzen més habitualment a l'empresa per confirmar que la versió del formulari encara tingui sentit i no falti res de la versió neta del formulari. Feu el mateix tipus de revisió en paral·lel per a les visualitzacions que heu personalitzat.
- La lògica empresarial pot fallar en temps d'execució. Com que les referències a camps dels complements no es validen en el moment de la importació, la lògica empresarial pot fallar a causa de referències a camps que ja no existeixen i pot ser que rebeu un missatge d'error semblant a aquest exemple: "L'entitat 'Projecte' no conté l'atribut amb nom = 'msdyn_plannedhours' i NameMapping = 'Logical'". En aquest cas, modifiqueu les personalitzacions per tal que utilitzin els camps nous. Si utilitzeu classes de servidor intermedi generades automàticament i referències de tipus fort a la lògica de complement, tingueu en compte la possibilitat de generar aquests servidors intermedis des d'una instal·lació neta. D'aquesta manera, podeu identificar fàcilment tots els llocs on els complements depenen de camps obsolets.

Un cop actualitzades les personalitzacions per importar el Project Operations de manera neta, avanceu als passos següents.

## <a name="end-to-end-testing-in-development-environments"></a>Proves d'extrem a extrem en entorns de desenvolupament

### <a name="initiate-upgrade"></a>Iniciar l'actualització 

1. Al centre d'administració del Power Platform, cerqueu i seleccioneu l'entorn. A continuació, a les aplicacions, cerqueu i seleccioneu el **Dynamics 365 Project Operations**.
2. Seleccioneu **Instal·la** per iniciar l'actualització. El centre d'administració del Power Platform presentarà aquesta instal·lació com una instal·lació nova. Tanmateix, es detectarà la presència d'una versió anterior del Project Service Automation i la instal·lació existent s'actualitzarà.

    Un cop completada l'actualització, l'entorn hauria de mostrar que el Project Operations està instal·lat i que el Project Service Automation no està instal·lat.

    En funció de la quantitat de dades de l'entorn, l'actualització podria trigar unes quantes hores. L'equip principal que gestiona l'actualització hauria de planificar segons correspongui i executar l'actualització durant hores d'inactivitat. En alguns casos, si el volum de dades és gran, l'actualització s'hauria d'executar durant el cap de setmana. La decisió sobre la planificació s'ha de basar en els resultats de les proves en entorns inferiors.

3. Actualitzeu les solucions personalitzades que calgui. En aquest moment, implementeu els canvis que hàgiu fet en les personalitzacions a la secció [Proves i refactorització de personalitzacions](#testing-and-refactoring-customizations) d'aquest article.
4. Aneu a **make.powerapps.com**, seleccioneu l'entorn a la llista desplegable de la part superior dreta del portal, seleccioneu **Solucions** al menú de l'esquerra, seleccioneu la solució **Components obsolets del Project Operations** i **Desinstal·la**.

    Aquesta solució és una solució temporal que conté el model de dades i els components existents durant l'actualització. En suprimir aquesta solució, se suprimeixen tots els camps i els components que ja no s'utilitzen. Això us ajudarà a simplificar la interfície i es facilitarà la integració i l'extensió.
    
### <a name="upgrade-to-project-operations-lite"></a>Actualitzar al Project Operations Lite

Els passos següents descriuen el procés d'actualització i el registre d'errors associat:

1. **Comprovació de la versió de PSA**: per instal·lar el Project Operations, heu de tenir la V3.10.58.120 o superior.
1. **Validació prèvia**: quan un administrador inicia una actualització, el sistema executa una operació de validació prèvia a cada entitat principal de la solució del Project Operations. Aquest pas valida que totes les referències a entitats són vàlides i garanteix que les dades relacionades amb la WBS estiguin dins dels límits publicats del Project for the Web.
1. **Actualització de metadades**: després d'una validació prèvia correcta, el sistema inicia els canvis a l'esquema i crea una solució de components obsolets. Podeu suprimir aquesta solució obsoleta després d'haver completat tota la refactorització necessària de les personalitzacions. Aquest pas és la part més llarga del procés d'actualització i pot trigar fins a quatre hores a completar-se.
1. **Actualització de dades**: quan tots els canvis necessaris a l'esquema s'han completat en el pas de l'actualització de metadades, les dades es migren a l'esquema nou i es duen a terme els nous càlculs i valors per defecte.
1. **Actualització del motor de planificació del projecte**: després d'una actualització de dades correcta, la pestanya **Planifica** a la pàgina principal es canvia amb l'etiqueta **Tasques**. Quan un usuari selecciona aquesta pestanya després de l'actualització, se'ls dirigeix a navegar a la quadrícula de seguiment per veure una versió només de lectura de la WBS. Per editar la WBS, han d'iniciar el [procés de conversió](/PSA-Upgrade-Project-Conversion.md) de la planificació. Tots els projectes sense WBS existent poden utilitzar la nova experiència de planificació directament, sense conversió.
 
### <a name="validate-common-scenarios"></a>Validar escenaris comuns

Quan valideu les personalitzacions específiques, us recomanem que reviseu també els processos de negoci compatibles amb les aplicacions. Aquests processos de negoci inclouen, entre altres, la creació d'entitats de vendes, com ara les ofertes i els contractes, i la creació de projectes que incloguin WBS i l'aprovació dels valors reals.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Canvis principals entre el Project Service Automation i el Project Operations

Aquesta secció proporciona un resum dels canvis principals que podeu esperar entre el Project Service Automation i el Project Operations.

### <a name="project-planning"></a>Planificació del projecte

Les capacitats de planificació del projecte al Project Operations ja no es basen en una combinació de lògica de client i una lògica de servidor. En lloc d'això, el Project Operations utilitza Project for the Web com a motor de planificació. Aquest canvi a les capacitats de planificació permet diverses característiques noves, com ara les visualitzacions del Tauler i del Gràfic de Gantt, la planificació controlada per recursos, els [elements de la llista de verificació de tasques](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i els modes de planificació de projectes. Les noves capacitats de planificació també estan admeses per un conjunt enriquit d'[interfícies de programació d'aplicacions (API)](../project-management/schedule-api-preview.md) noves. Aquestes API estan dissenyades per ajudar a garantir que cap operació programàtica per crear, actualitzar o suprimir una entitat a la WBS malmeti els camps calculats de la planificació.

### <a name="billing-and-pricing"></a>Facturació i preus

Com a part de les inversions continuades al Project Operations, hi ha diverses característiques noves disponibles a Facturació i preus. A continuació trobareu alguns exemples:

- [Registre de l'ús de materials en projectes i tasques de projectes](../material/material-usage-log.md)
- [Administració de subcontractes](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avançaments i contractes de bestreta](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estat que no s'ha de superar del contracte i validacions](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturació basada en tasques

### <a name="resource-management"></a>Administració de recursos

El Project Operations proporcionen compatibilitat opcional amb el tauler del Universal Resource Scheduling (URS) i l'auxiliar de planificació. Aquesta nova experiència serà obligatòria a la fase d'abril de 2023.

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quins tipus d'implementació s'admeten actualment per a l'actualització?

| Font                                                 | Meta                                                    | Estat d'execució                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementació bàsica del Project Operations                        | Admès               |
| Administració de projectes i comptabilitat al Dynamics 365 Finance | Implementació bàsica del Project Operations                        | Actualment no s'admet |
| Administració de projectes i comptabilitat al Finance              | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Project Service Automation 3.x                         | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Project for the Web (entorn dedicat)            | Implementació bàsica del Project Operations                        | Actualment no s'admet |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Com puc instal·lar el Project Operations abans que estiguin disponibles les eines d'actualització?

Hi ha dues opcions per instal·lar el Project Operations abans que les eines d'actualització estiguin disponibles:

- Aprovisionament d'un entorn nou.
- Implementeu el Project Operations per separat a qualsevol organització de vendes on el Project Service Automation no estigui present.

Si el Project Service Automation està instal·lat en una organització, però no s'ha utilitzat, es pot desinstal·lar. Després de suprimir completament el Project Service Automation, podeu instal·lar el Project Operations a la mateixa organització.
