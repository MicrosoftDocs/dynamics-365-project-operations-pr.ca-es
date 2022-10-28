---
title: Actualització del Project Service Automation al Project Operations
description: Aquest article proporciona una visió general del procés per actualitzar de Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
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
ms.openlocfilehash: 06a4de89be8176049d3a14a8c0d6427e228744ba
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709432"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Actualització del Project Service Automation al Project Operations

Estem encantats d'anunciar la segona de les tres fases per a l'actualització des de Microsoft Dynamics 365 Project Service Automation Microsoft Dynamics 365 Project Operations. Aquest article proporciona una visió general per als clients que s'embarquen en aquest emocionant viatge. 

El programa de lliurament d'actualitzacions es dividirà en tres fases.

| Lliurament d'actualitzacions | Fase 1 (gener 2022) | Fase 2 (novembre 2022) | Fase 3 (onada d'abril de 2023)  |
|------------------|------------------------|---------------------------|---------------------------|
| No hi ha dependència de l'estructura de desglossament del treball (WBS) per als projectes | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Un WBS dins dels límits actualment suportats de les operacions de projecte | | :heavy_check_mark: | :heavy_check_mark: |
| Un WBS fora dels límits suportats actualment de Project Operations, incloent suport per al client d'escriptori del projecte | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Funcions del procés d'actualització 

Com a part del procés d'actualització, hem afegit registres d'actualització al mapa del lloc per permetre als administradors diagnosticar més fàcilment els errors. A més de la nova interfície, s'afegiran noves regles de validació per garantir la integritat de les dades després d'una actualització. Les següents validacions s'afegiran al procés d'actualització.

| Validacions | Fase 1 (gener 2022) | Fase 2 (novembre 2022) | Fase 3  |
|-------------|------------------------|---------------------------|---------------------------|
| El WBS es validarà contra violacions comunes de la integritat de les dades (per exemple, assignacions de recursos que estiguin associades a la mateixa tasca principal però que tinguin diferents projectes principals). | | :heavy_check_mark: | :heavy_check_mark: |
| El WBS serà validat contra els [límits coneguts de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| El WBS es validarà contra els límits coneguts del client d'escriptori del projecte. | |  | :heavy_check_mark: |
| Els recursos reservables i els calendaris del projecte s'avaluaran amb excepcions comunes de regles de calendari incompatibles. | | :heavy_check_mark: | :heavy_check_mark: |

A la fase 2, els clients que actualitzin a Project Operations actualitzaran els seus projectes existents a una experiència només de lectura per a la planificació de projectes. En aquesta experiència només de lectura, el WBS complet serà visible a la graella de seguiment. Per editar el WBS, els gestors de projectes poden seleccionar [**Converteix**](/PSA-Upgrade-Project-Conversion.md) a la pàgina principal del projecte. A continuació, un procés en segon pla actualitza el projecte de manera que admeti la nova experiència de planificació de projectes del Project for the Web. Aquesta fase és adequada per a clients que tinguin projectes que encaixin dins dels [límits coneguts de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries).

En la fase 3, s'afegirà suport per al client d'escriptori del projecte, en benefici dels clients que vulguin continuar editant els seus projectes des d'aquesta aplicació. Tanmateix, si els projectes existents es converteixen al nou Projecte per a l'experiència web, l'accés al complement es desactivarà per a cada projecte convertit.

## <a name="prerequisites"></a>Requisits previs

Per poder optar a l'actualització de la Fase 1, heu de complir els criteris següents:

- L'entorn de destinació no ha de contenir cap registre a l'entitat **msdyn_projecttask**.
- Les llicències vàlides del Project Operations s'han d'assignar a tots els usuaris actius. 
- Heu de validar el procés d'actualització en almenys un entorn no productiu que contingui un conjunt de dades representatiu i alineat amb el vostre entorn de producció.
- L'entorn de destinació s'ha d'actualitzar a la versió 37 (V3.10.58.120) o posterior de l'actualització de l'automatització del Project Service Automation.

Per ser elegible per a l'actualització de la Fase 2, heu de complir els criteris següents:

- Les llicències vàlides del Project Operations s'han d'assignar a tots els usuaris actius. 
- Heu de validar el procés d'actualització en almenys un entorn no productiu que contingui un conjunt de dades representatiu i alineat amb el vostre entorn de producció.
- L'entorn de destinació s'ha d'actualitzar a la versió 37 (V3.10.58.120) o posterior de l'actualització de l'automatització del Project Service Automation.
- Els entorns que contenen tasques (msdyn_projecttask) només s'admeten si el nombre total de tasques per projecte és de 500 o menys.

Els requisits previs per a la Fase 3 s'aniran actualitzant a mesura que s'acosti la data de disponibilitat general.

## <a name="licensing"></a>Llicències

Si teniu llicències actives per al Project Service Automation, podeu instal·lar i utilitzar el Project Operations, que inclou totes les capacitats del Project Service Automation i molt més. D'aquesta manera, podeu provar les capacitats del Project Operations mentre continueu utilitzant el Project Service Automation en producció. Un cop caduquin les llicències del Project Service Automation, haureu de fer la transició al Project Operations. Quan planifiqueu aquesta transició, heu de tenir en compte que la llicència del Project Operations no inclou cap llicència del Project Service Automation. Els clients que tinguin escenaris on han desplegat el Project Service Automation i necessitin continuar utilitzant o augmentant les seves llicències per a PSA mentre tenen previst passar a Project Operations, poden sol·licitar llicències temporals de PSA basades en llicències adquirides per Project Operations. S'emetrà una llicència d'Automatització del Project Service per a una llicència d'Operacions de Projecte. Es poden sol·licitar llicències temporals de PSA a través d'aquest enllaç: aka.ms/ineedpsa

## <a name="testing-and-refactoring-customizations"></a>Proves i refactoritzacions de personalitzacions

Com a punt de partida, importeu totes les personalitzacions en un entorn net d'Operacions del Projecte (Lite) per confirmar que la importació té èxit i que les operacions comercials es comporten com s'esperava.

Aquí teniu algunes coses que cal tenir en compte:

- La importació pot fallar a causa de les dependències que falten. En altres paraules, els camps de referència de personalitzacions o altres components que s'han eliminat al Project Operations. En aquest cas, elimineu aquestes dependències de l'entorn de desenvolupament.
- Si les solucions no administrades i no administrades inclouen components que no estan personalitzats, traieu-los de la solució. Per exemple, quan personalitzeu l'entitat **del projecte**, afegiu només la capçalera d'entitat a la solució. No afegiu tots els camps. Si anteriorment heu afegit tots els subcomponents, és possible que hàgiu de crear manualment una solució nova i afegir-hi components rellevants.
- És possible que els formularis i les visualitzacions no apareguin com s'esperava. En algunes circumstàncies, si heu personalitzat algun dels formularis o visualitzacions estàndard, és possible que les personalitzacions impedeixin que es facin efectives noves actualitzacions al Project Operations. Per identificar aquests problemes, us recomanem que feu una revisió paral·d'una instal·lació neta de Project Operations i d'una instal·lació de Project Operations que inclogui les vostres personalitzacions. Compareu els formularis més utilitzats a la vostra empresa per confirmar que la vostra versió del formulari encara té sentit i que no falta res a la versió neta del formulari. Feu el mateix tipus de revisió en paral·lel per a les visualitzacions que hàgiu personalitzat.
- La lògica empresarial pot fallar en temps d'execució. Com que les referències als camps dels connectors no es validen en el moment de la importació, és possible que la lògica empresarial falli a causa de les referències a camps que ja no existeixen i és possible que rebeu un missatge d'error que s'assembli a l'exemple següent: "L'entitat del projecte" no conté atribut amb Nom = "msdyn_plannedhours" i NameMapping = "Lògic". En aquest cas, modifiqueu les personalitzacions perquè utilitzin els camps nous. Si utilitzeu classes proxy generades automàticament i referències de tipus fortes a la lògica del connector, penseu a regenerar aquests servidors intermediaris a partir d'una instal·lació neta. D'aquesta manera, podeu identificar fàcilment tots els llocs on els vostres connectors depenen de camps obsolets.

Després d'actualitzar les personalitzacions per importar netament operacions del Projecte, seguiu els passos següents.

## <a name="end-to-end-testing-in-development-environments"></a>Proves d'extrem a extrem en entorns de desenvolupament

### <a name="initiate-upgrade"></a>Iniciar l'actualització 

1. Al centre d'administració Power Platform, cerqueu i seleccioneu l'entorn. A continuació, a les aplicacions, cerqueu i seleccioneu **Dynamics 365 Project Operations**.
2. Seleccioneu **Instal·la** per iniciar l'actualització. El Power Platform centre d'administració presentarà aquesta instal·lació com una nova instal·lació. No obstant això, es detectarà la presència d'una versió anterior del Project Service Automation i s'actualitzarà la instal·lació existent.

    Un cop finalitzada l'actualització, l'entorn ha de mostrar que el Project Operations està instal·lat i que el Project Service Automation no està instal·lat.

    En funció de la quantitat de dades de l'entorn, l'actualització pot trigar diverses hores. L'equip central que gestiona l'actualització hauria de planificar en conseqüència i executar l'actualització durant l'horari no comercial. En alguns casos, si el volum de dades és gran, l'actualització s'hauria d'executar durant el cap de setmana. La decisió sobre la programació s'ha de basar en els resultats de les proves en entorns més baixos.

3. Actualitzeu les solucions personalitzades segons correspongui. En aquest punt, desplegueu els canvis que hàgiu fet a les personalitzacions a la [secció Proves i personalitzacions](#testing-and-refactoring-customizations) de refactorització d'aquest article.
4. Aneu a Solucions de **configuració** \>**i** seleccioneu desinstal·lar la **solució Components** obsolets d'Operacions del projecte.

    Aquesta solució és una solució temporal que conté el model de dades existent i els components presents durant l'actualització. En suprimir aquesta solució, suprimiu tots els camps i components que ja no s'utilitzen. D'aquesta manera, ajudeu a simplificar la interfície i a facilitar la integració i l'extensió.
    
### <a name="upgrade-to-project-operations-lite"></a>Actualització al Project Operations Lite

Els passos següents descriuen el procés d'actualització i el registre d'errors associat:

1. **Comprovació de la versió de PSA:** per instal·lar Project Operations, heu de tenir V3.10.58.120 o superior.
1. **Prevalidació:** quan un administrador inicia una actualització, el sistema executa una operació de prevalidació a cada entitat que és el nucli de la solució Project Operations. Aquest pas verifica que totes les referències d'entitats són vàlides, i garanteix que les dades relacionades amb el WBS es troben dins dels límits publicats de Project for the Web.
1. **Actualització de metadades:** Després d'una prevalidació correcta, el sistema inicia canvis a l'esquema i crea una solució de components obsolets. Podeu suprimir aquesta solució obsoleta després d'haver completat totes les personalitzacions necessàries. Aquest pas és la part més llarga del procés d'actualització i pot trigar fins a quatre hores a completar-se.
1. **Actualització de dades:** Un cop completats tots els canvis d'esquema necessaris al pas d'actualització de metadades, les dades es migren al nou esquema i es fan els càlculs i els càlculs predeterminats necessaris.
1. **Actualització del motor de planificació del projecte:** després de l'actualització de dades amb èxit, la **pestanya Planificació** de la pàgina principal es torna a etiquetar **Tasques**. Quan un usuari selecciona aquesta pestanya després de l'actualització, se li dirigeix a navegar a la quadrícula de seguiment per veure una versió només de lectura del WBS. Per editar el WBS, han d'iniciar el procés [de conversió de planificació](/PSA-Upgrade-Project-Conversion.md). Tots els projectes sense un WBS preexistent poden utilitzar la nova experiència de planificació directament, sense conversió.
 
### <a name="validate-common-scenarios"></a>Validar escenaris comuns

Quan valideu les personalitzacions específiques, us recomanem que també reviseu els processos de negoci admesos en totes les aplicacions. Aquests processos de negoci inclouen, entre d'altres, la creació d'entitats de venda, com ara pressupostos i contractes, i la creació de projectes que incloguin WBSs i aprovació de reals.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Canvis importants entre Project Service Automation i Project Operations

Aquesta secció proporciona un resum dels principals canvis que podeu esperar entre Project Service Automation i Project Operations.

### <a name="project-planning"></a>Planificació del projecte

Les capacitats de planificació de projectes en Project Operations ja no es basen en una combinació de lògica del costat del client i lògica del servidor. En lloc d'això, Project Operations utilitza project per al web com a motor de planificació. Aquest canvi en les capacitats de planificació permet diverses funcions noves, com ara les visualitzacions de board i gantt, la planificació basada en recursos, [els elements de la llista de comprovació de tasques i els](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) modes de planificació de projectes. Les noves capacitats de planificació també estan suportades per un ric conjunt de noves [interfícies de programació d'aplicacions (API).](../project-management/schedule-api-preview.md) Aquestes API estan destinades a ajudar a garantir que cap operació programàtica per crear, actualitzar o suprimir una entitat del WBS corromp els camps calculats de la planificació.

### <a name="billing-and-pricing"></a>Facturació i preus

Com a part de les inversions contínues en operacions de projecte, hi ha diverses funcions noves disponibles a Facturació i preus. A continuació trobareu alguns exemples:

- [Registre de l'ús de material en projectes i tasques del projecte](../material/material-usage-log.md)
- [Gestió de subcontractes](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avançaments i contractes de bestreta](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estat del contracte i validacions](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturació basada en tasques

### <a name="resource-management"></a>Administració de recursos

Project Operations proporciona suport opcional per a la Universal Resource Scheduling placa (URS) i l'assistent de planificació. Aquesta nova experiència passarà a ser obligatòria en l'onada d'abril de 2023.

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quins tipus d'implementació són compatibles actualment amb l'actualització?

| Font                                                 | Meta                                                    | Estat d'execució                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Project Operations Lite Deployment                        | Admès               |
| Dynamics 365 Finance Administració i Comptabilitat de Projectes | Project Operations Lite Deployment                        | Actualment no s'admet |
| Finances i Gestió de Projectes Comptables              | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Project Service Automation 3.x                         | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Projecte per a la Web (entorn dedicat)            | Project Operations Lite Deployment                        | Actualment no s'admet |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Com puc instal·lar Project Operations abans que les eines d'actualització estiguin disponibles?

Hi ha dues opcions per instal·lar Project Operations abans que les eines d'actualització estiguin disponibles:

- Dotar d'un nou entorn.
- Implementeu el Project Operations per separat en qualsevol organització de vendes on el Project Service Automation no estigui present.

Si el Project Service Automation està instal·lat en una organització, però no s'ha utilitzat, es pot desinstal·lar. Després de suprimir completament el Project Service Automation, el Project Operations es pot instal·lar a la mateixa organització.
