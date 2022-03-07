---
title: Millora de l'automatització del project service a les operacions del projecte
description: Aquest tema proporciona una visió general del procés a actualitzar des de Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/05/2022
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
ms.openlocfilehash: 9363fd5a06b6b1ba023961b03228e13a53a82002
ms.sourcegitcommit: 5789766efae1e0cb513ea533e4f9ac1e553158a5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7954288"
---
# <a name="upgrade-from-project-service-automation-to-project-operations"></a>Millora de l'automatització del project service a les operacions del projecte

Estem encantats d'anunciar la primera de les tres fases per actualitzar des de Microsoft Dynamics 365 Project Service Automation a Dynamics 365 Project Operations. Aquest tema proporciona una visió general per als clients que s'embarquen en aquest emocionant viatge. Els temes futurs inclouran consideracions per als desenvolupadors i detalls sobre les millores de funcions. No només us proporcionaran orientació per ajudar-vos a preparar l'actualització a les operacions del projecte, sinó que també explicaran què podeu esperar després d'haver actualitzat.

El programa de lliurament d'actualitzacions es dividirà en les tres fases.

| Actualitza el lliurament | Fase 1 (gener 2022) | Fase 2 (onada d'abril de 2022) | Fase 3 (onada d'abril de 2022) |
|------------------|------------------------|---------------------------|---------------------------|
| Sense dependència de l'estructura de desglossament de l'obra (WBS) per a projectes | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| El WBS dins dels límits actualment admesos de les operacions del projecte | | :heavy_check_mark: | :heavy_check_mark: |
| El WBS fora dels límits compatibles actualment de les operacions del projecte, inclòs el suport per al client d'escriptori project | | | :heavy_check_mark: |

## <a name="upgrade-process-features"></a>Actualitza les característiques del procés 

Com a part del procés d'actualització, hem afegit registres d'actualització al mapa del lloc, de manera que els administradors poden diagnosticar més fàcilment els errors. A més de la nova interfície, s'afegiran noves regles de validació per garantir la integritat de les dades després d'una actualització. S'afegiran les validacions següents al procés d'actualització.

| Validacions | Fase 1 (gener 2022) | Fase 2 (onada d'abril de 2022) | Fase 3 (onada d'abril de 2022) |
|-------------|------------------------|---------------------------|---------------------------|
| El WBS es validarà contra violacions comunes de la integritat de dades (per exemple, assignacions de recursos que estan associades amb la mateixa tasca principal però que tenen projectes pares diferents). | | :heavy_check_mark: | :heavy_check_mark: |
| El WBS es validarà contra els [límits coneguts de Project for the Web](/project-for-the-web/project-for-the-web-limits-and-boundaries). | | :heavy_check_mark: | :heavy_check_mark: |
| El WBS es validarà contra els límits coneguts del client d'escriptori Project. | | :heavy_check_mark: | :heavy_check_mark: |
| Els recursos que es poden reservar i els calendaris de projectes s'avaluaran amb excepcions de regles de calendari incompatibles comunes. | | :heavy_check_mark: | :heavy_check_mark: |

En la fase 2, els clients que actualitzin a Project Operations tindran els seus projectes existents actualitzats a una experiència de només lectura per a la planificació de projectes. En aquesta experiència de només lectura, el WBS complet serà visible a la quadrícula de seguiment. Per editar el WBS, els gestors de projectes poden seleccionar **Converteix a la pàgina principals de** **projectes**. A continuació, un procés de fons actualitzarà el projecte de manera que admeti la nova experiència de planificació de projectes del Project for the Web. Aquesta fase és adequada per als clients que disposen de projectes que encaixin dins [dels límits coneguts de Project for the](/project-for-the-web/project-for-the-web-limits-and-boundaries) Web.

En la fase 3, s'afegirà suport per al client d'escriptori project, en benefici dels clients que vulguin continuar editant els seus projectes des d'aquesta aplicació. Tanmateix, si els projectes existents es converteixen al nou Projecte per a l'experiència web, l'accés al complement es desactivarà per a cada projecte convertit.

## <a name="prerequisites"></a>Requisits previs

Per poder optar a l'actualització de fase 1, un client ha de complir els criteris següents:

- L'entorn de destinació no pot contenir cap registre a **l**'entitat msdyn_projecttask.
- Les llicències vàlides d'operacions de projecte s'han d'assignar a tots els usuaris actius del client. 
- El client ha de validar el procés d'actualització en almenys un entorn de no producció que tingui un conjunt de dades representatiu alineat amb les dades de producció.
- L'entorn de destinació s'ha d'actualitzar a la versió 38 o posterior del Project Service Automation.

Els requisits previs per a la fase 2 i la fase 3 s'aniran actualitzant a mesura que s'acostin les dates generals de disponibilitat.

## <a name="licensing"></a>Llicències

Si teniu llicències actives per al Project Service Automation, podeu instal·lar i utilitzar Project Operations, que inclou totes les capacitats del Project Service Automation i molt més. D'aquesta manera, podeu provar les capacitats de Project Operations mentre continueu utilitzant project service automation en producció. Quan caduquin les llicències d'automatització del Project Service, haureu de passar a les operacions del projecte. Quan planifiqueu aquesta transició, heu de tenir en compte que la llicència Operacions del projecte no inclou una llicència d'automatització del Project Service.

## <a name="testing-and-refactoring-customizations"></a>Proves i refacció de personalitzacions

Com a punt de partida, importeu totes les personalitzacions en un entorn net d'operacions del projecte (lite) per confirmar que la importació té èxit i que les operacions empresarials es comporten com s'esperava.

Aquí hi ha algunes coses a tenir en compte:

- Pot ser que la importació falli a causa de les dependències que falten. En altres paraules, els camps de referència de personalitzacions o altres components que s'han suprimit a Les operacions del projecte. En aquest cas, elimineu aquestes dependències de l'entorn de desenvolupament.
- Si les solucions no administrades i administrades inclouen components que no estan personalitzats, suprimiu-los de la solució. Per exemple, quan personalitzeu **l**'entitat Projecte, afegiu només la capçalera d'entitat a la solució. No afegiu tots els camps. Si heu afegit tots els subcomponents anteriorment, és possible que hàgiu de crear manualment una solució nova i afegir-hi components rellevants.
- És possible que els formularis i les visualitzacions no apareguin com a inesperats. En algunes circumstàncies, si heu personalitzat algun dels formularis o visualitzacions desescatades, és possible que les personalitzacions impedeixin que les actualitzacions noves de les operacions del projecte 50% vinguin a l'efecte. Per identificar aquests problemes, us recomanem que feu una revisió colze a colze d'una instal·lació neta d'operacions de projecte i una instal·lació d'operacions de projecte que inclogui les vostres personalitzacions. Compara els formularis més utilitzats a la teva empresa per confirmar que la versió del formulari encara té sentit i que no li falta res de la versió neta del formulari. Feu el mateix tipus de revisió colze a colze per a les visualitzacions que hàgiu personalitzat.
- La lògica empresarial pot fallar en temps d'execució. Com que les referències als camps dels connectors no es validen en el moment de la importació, és possible que la lògica empresarial falli a causa de les referències a camps que ja no existeixen i és possible que rebeu un missatge d'error que s'assembli a l'exemple següent: l'entitat "'Projecte' no conté atribut amb Nom = 'msdyn_plannedhours' i Mapa de noms = 'Lògic'". En aquest cas, modifiqueu les personalitzacions perquè utilitzin els camps nous. Si utilitzeu classes de servidor intermediari generades automàticament i referències de tipus fort a la lògica del connector, considereu regenerar aquests servidors intermediaris a partir d'una instal·lació neta. D'aquesta manera, podeu identificar fàcilment tots els llocs on els vostres connectors depenen de camps obsolets.

Després d'actualitzar les personalitzacions per importar netament les operacions del projecte, passa als passos següents.

## <a name="end-to-end-testing-in-lower-environments"></a>Proves d'extrem a extrem en entorns inferiors

### <a name="run-the-upgrade-in-production"></a>Executar l'actualització en la producció

1. Al Power Platform centre d'administració, cerqueu i seleccioneu el vostre entorn. A continuació, a les aplicacions, cerqueu i seleccioneu **Dynamics 365 Project Operations**.
2. Seleccioneu **Instal**·la per iniciar l'actualització. El Power Platform centre d'administració presentarà aquesta instal·lació com una instal·lació nova. Tanmateix, es detectarà la presència d'una versió anterior del Project Service Automation i s'actualitzarà la instal·lació existent.

    Un cop finalitzada l'actualització, l'entorn ha de mostrar que les operacions del projecte estan instal·lades i que el Project Service Automation no està instal·lat.

    > [!NOTE]
    > Depenent de la quantitat de dades de l'entorn, l'actualització pot trigar diverses hores. L'equip principal que gestiona l'actualització ha de planificar en conseqüència i executar l'actualització durant l'horari no comercial. En alguns casos, si el volum de dades és gran, l'actualització s'ha d'executar durant el cap de setmana. La decisió sobre la planificació s'ha de basar en els resultats de les proves en entorns inferiors.

3. Actualitzeu les solucions personalitzades segons convingui. En aquest punt, implementeu els canvis que hàgiu fet a les personalitzacions a la [secció Prova i refacció de personalitzacions](#testing-and-refactoring-customizations) d'aquest tema.
4. Aneu a **Solucions de configuració i** \> **seleccioneu** per desinstal·lar la solució Components obsolets de les **operacions del** projecte.

    Aquesta solució és una solució temporal que conté el model de dades existent i els components que estan presents durant l'actualització. Si suprimiu aquesta solució, suprimiu tots els camps i components que ja no s'utilitzen. D'aquesta manera, ajudeu a simplificar la interfície i facilitar la integració i l'extensió.

## <a name="major-changes-between-project-service-automation-and-project-operations"></a>Canvis importants entre l'automatització de serveis del projecte i les operacions de projectes

Aquesta secció proporciona un resum dels canvis principals que podeu esperar entre l'automatització de serveis del Projecte i les operacions de projectes.

### <a name="project-planning"></a>Planificació del projecte

Les capacitats de planificació del projecte a Project Operations ja no es basen en una lògica combinada del costat del client i la lògica del servidor. En lloc d'això, Project Operations utilitza el Projecte per al Web com a motor de planificació. Aquest canvi en les capacitats de planificació permet diverses característiques noves, com ara visualitzacions board i Gantt, planificació basada en recursos, elements de [la llista de comprovació de tasques](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c) i modes de planificació de projectes. Les noves capacitats de planificació també estan suportades per un conjunt ric de noves interfícies de [programació d'aplicacions](../project-management/schedule-api-preview.md) (API). Aquestes API estan destinades a ajudar a garantir que cap operació programàtica per crear, actualitzar o suprimir una entitat del WBS corromp els camps calculats de la planificació.

## <a name="billing-and-pricing"></a>Facturació i preus

Com a part de les inversions contínues en operacions de projectes, hi ha diverses capacitats noves disponibles a Facturació i preus. A continuació trobareu alguns exemples:

- [Enregistrament de l'ús de material en projectes i tasques del projecte](../material/material-usage-log.md)
- [Gestió de subcontractacions](../pro/subcontracting/managing-subcontracts-overview.md)
- [Avançaments i contractes de bestreta](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Estat de no superació del contracte i validacions](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- Facturació basada en tasques

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="which-deployment-types-are-currently-supported-for-upgrade"></a>Quins tipus de desplegament s'admeten actualment per a l'actualització?

| Font                                                 | Meta                                                    | Estat d'execució                  |
|--------------------------------------------------------|-----------------------------------------------------------|-------------------------|
| Project Service Automation                             | Implementació de Lite d'operacions del projecte                        | Admès               |
| Dynamics 365 Finance Gestió de Projectes i Comptabilitat | Implementació de Lite d'operacions del projecte                        | Actualment no s'admet |
| Gestió i Comptabilitat de Projectes Financers              | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Gestió i Comptabilitat de Projectes Financers              | Project Operations per a escenaris mantinguts en existències/d’ordre de producció | Actualment no s'admet |
| Automatització de serveis de projectes 3.x                         | Project Operations per a escenaris de recursos/no mantinguts en existències     | Actualment no s'admet |
| Projecte per a la web (entorn dedicat)            | Implementació de Lite d'operacions del projecte                        | Actualment no s'admet |

### <a name="how-can-i-install-project-operations-before-the-upgrade-tooling-is-available"></a>Com puc instal·lar operacions del projecte abans que l'eina d'actualització estigui disponible?

Hi ha dues opcions per instal·lar operacions del projecte abans que l'eina d'actualització estigui disponible:

- Proporcionar un nou entorn.
- Implementa les operacions del projecte per separat a qualsevol organització de vendes on el Project Service Automation no estigui present.

> [!NOTE]
> Si el Project Service Automation està instal·lat en una organització, però no s'ha utilitzat, es pot desinstal·lar. Després de suprimir completament el Project Service Automation, les operacions del projecte es poden instal·lar a la mateixa organització.
