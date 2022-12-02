---
title: Unitats organitzatives
description: En aquest article es descriu el concepte d'unitats organitzatives i s'explica com es creen i es mantenen les unitats organitzatives al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 1/31/2022
ms.topic: article
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
ms.openlocfilehash: a20a37b61db68d70869a11e10bef5d30c422b1eb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921612"
---
# <a name="organizational-units-overview"></a>Informació general de les unitats organitzatives

Al Microsoft Dynamics 365 Project Operations, una *unitat organitzativa* és un grup o divisió diferent en una empresa de serveis professionals que empra recursos imputables que tenen tarifes de costos.

Per a les empreses de serveis professionals que empren recursos tècnics en diferents àrees de pràctiques o línies de negoci, el cost d'emplenar una funció pot variar segons l'àrea de pràctica o la línia de negoci on es cobreix la funció. En aquest escenari, el concepte d'unitats organitzatives ajuda proporcionant una manera d'agrupar un conjunt de funcions facturables en una divisió d'una empresa que tingui una estructura de costos diferent per a aquestes funcions.

## <a name="the-concept-of-organizational-units-in-project-operations"></a>Concepte d'unitats organitzatives al Project Operations

Al Project Operations, una unitat organitzativa té una moneda específica i una llista de preus de cost específics.

La moneda d'una unitat organitzativa és la moneda principal que s'utilitza per fer el seguiment dels costos.

Es poden adjuntar una o diverses llistes de preus de cost a cada unitat organitzativa. El Project Operations posa les següents limitacions a les llistes de preus que es poden adjuntar a una unitat organitzativa:

- Les llistes de preus han d'estar en la moneda de la unitat organitzativa.
- Les llistes de preus han de tenir llistes de preus de cost.

A més, l'entitat Recurs inclou un atribut per a la unitat organitzativa. Cada recurs només es pot assignar a una unitat organitzativa.

### <a name="roles-of-organizational-units"></a>Funcions de les unitats organitzatives

La unitat organitzativa té dues funcions al Project Operations:

- **Unitat de contractació**: unitat organitzativa que representa el grup d'empreses o la divisió que s'encarrega principalment de guanyar la venda i administrar el lliurament de treballs i serveis al client. La unitat de contractació s'identifica pel camp **Unitat de contractació** a la secció de capçalera de les pàgines **Oportunitat**, **Oferta**, **Contracte del projecte** i **Projecte**.
- **Unitat de recursos**: unitat organitzativa a la qual pertany un recurs o s'assigna. Aquesta unitat organitzativa pot proporcionar els seus recursos per a algunes funcions sobre les declaracions de treball (SOW) i els projectes que siguin propietat de la unitat de contractació.

![Unitats de contractació i unitats de recursos.](media/OrgUnits.png)

### <a name="organizational-unit-faq"></a>PMF sobre la unitat organitzativa

A continuació teniu les preguntes que els usuaris formulen més sovint sobre les unitats organitzatives.

#### <a name="how-is-the-organizational-unit-entity-in-project-operations-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Com es relaciona l'entitat Unitat organitzativa al Project Operations amb l'entitat de Organització que ja existeix al Dynamics 365?

L'entitat Organització del Dynamics 365 representa el nom d'una instància global del Dynamics 365. Aquest nom sol ser el nom de l'empresa global.

L'entitat Unitat organitzativa representa un grup o divisió a l'empresa global. Aquest grup o divisió té un conjunt de funcions i una llista de preus de cost per a aquestes funcions, i aquestes funcions i la llista de preus es diferencien de les funcions i de la llista de preus d'altres grups o divisions de l'empresa.

Quan s'instal·la el Project Operations, es crea una unitat organitzativa per defecte basada en l'organització. Tots els recursos existents s'assignen a la unitat organitzativa per defecte. Si s'importen nous usuaris o recursos de l'Active Directory al Dynamics 365, el procés d'importació d'usuari els assigna a la unitat organitzativa per defecte al Project Operations.

#### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Com es diferencia l'entitat d'unitat organitzativa de l'entitat d'unitat de negoci?

Al Dynamics 365, l'entitat Unitat de negoci és una construcció de seguretat. L'associació d'un usuari amb una unitat de negoci determina les entitats i els registres d'entitat als quals té accés l'usuari. També determina els permisos (creació, lectura, escriptura, supressió, annexió, annexió a un altre element, assignació o ús compartit) que l'usuari té per als registres de l'entitat.

L'entitat Unitat organitzativa representa un grup d'empreses o una divisió que té percentatges de costos diferents per als empleats que hi estan assignats. L'associació d'un recurs amb una unitat organitzativa determina el cost del recurs en un compromís de projecte.

Quan implementeu el Dynamics 365, optimitzeu l'autorització de seguretat per a la jerarquia d'unitats de negoci i l'assignació d'usuaris a unitats de negoci. Assigneu tots els usuaris que normalment han d'accedir al mateix conjunt de registres a la mateixa unitat de negoci. La unitat organitzativa no té cap efecte sobre l'autorització de seguretat ni l'accés.

**Exemple que mostra una diferència potencial en el modelatge d'unitats organitzatives i unitats de negoci**

Contoso, Ltd. té una pròspera pràctica de tecnologia de Microsoft. L'Eudald i la Clàudia són desenvolupadors de C\#, però la Clàudia és als Estats Units, mentre que l'Eudald és a l'Índia. La major part del projecte exigeix recursos tant de Contoso India com de Contoso US, i l'Eudald i la Clàudia requereixen el mateix nivell d'accés a projectes en aquesta àrea de pràctica. No obstant, el cost dels desenvolupadors de Contoso India difereix significativament del cost dels desenvolupadors de Contoso US.

Aquesta és una manera òptima de dissenyar per a aquest escenari mitjançant el Dynamics 365 i el Project Operations.

1. Creeu la pràctica de tecnologia de Microsoft com a unitat de negoci, i associeu-hi l'Eudald i la Clàudia. D'aquesta manera, us ajudem a garantir que tots dos empleats tenen el mateix nivell d'accés de seguretat als projectes en aquesta àrea de pràctiques. Tots dos seran capaços de comprovar el progrés i informar de temps, despeses, ús de materials i actualitzacions de tasques.
2. Creeu dues unitats organitzatives per ajudar a garantir que el cost del projecte es reflecteixi correctament.
3. Associeu la Clàudia amb Contoso US i l'Eudald amb Contoso India.
4. Assigneu les llistes de preus de cost adequades a ambdues unitats organitzatives. D'aquesta manera, ajudeu a garantir que els costos que es registren en el projecte de l'Eudald i la Clàudia reflecteixen amb precisió la diferència de costos entre Contoso US i Contoso India.

#### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Les unitats organitzatives estan relacionades amb les zones de vendes del Dynamics 365?

No hi ha cap associació o relació entre zones de vendes i unitats organitzatives. Una zona de vendes normalment és una àrea geogràfica en la qual es produeixen les vendes. Una llista de preus de vendes es pot associar a cada zona de vendes.

Una unitat organitzativa és un grup o divisió interna de l'empresa que segueix els costos d'un conjunt de funcions que ven a altres divisions o a clients externs.

**Exemple que mostra una diferència potencial en el modelatge d'unitats organitzatives i territoris de vendes**

Contoso, Ltd. té dos centres de desenvolupament: Contoso US i Contoso India. El cost dels recursos difereix en gran mesura entre aquests dos centres de desenvolupament. Contoso ven els seus serveis de tecnologies de la informació (TI) a molts mercats internacionals, com ara l'Amèrica Llatina, l'Amèrica del Nord, Àsia-Pacífic, l'Europa occidental i l'Orient Mitjà. Les tarifes de facturació d'aquestes mateixes funcions del projecte poden variar àmpliament en aquests mercats. Contoso US i Contoso India haurien de configurar-se com a unitats organitzatives, i cada unitat organitzativa hauria de tenir la seva pròpia llista de preus de costos. Àsia-Pacífic, l'Amèrica Llatina, l'Amèrica del Nord, l'Europa occidental, i l'Orient Mitjà s'han de configurar com a zones de vendes, i cada zona de vendes hauria de tenir la seva pròpia llista de preus de vendes.

#### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Per què hi ha una restricció a l'associació de llistes de preus amb unitats organitzatives?

Els preus de vendes normalment són exclusius de les àrees geogràfiques o mercats en què es venen serveis. Les divisions internes d'una empresa no acostumen a tenir els seus propis preus de vendes per al mateix tipus de serveis. No obstant això, les divisions internes tenen un cost diferent dels béns venuts (COGS), en funció de les aptituds de les persones que contractin i de les condicions de treball de la regió on operen. Com que les unitats organitzatives estan modelades com a divisions internes d'una empresa, només poden tenir llistes de preus de cost.

#### <a name="why-cant-we-associate-sales-price-lists-with-organizational-units"></a>Per què no es pot associar la llista de preus de vendes a unitats organitzatives?

Al Project Operations, les llistes de preus de vendes poden associar-se amb els clients i les zones de vendes. Les entitats transaccionals com ara Oportunitat, Oferta, Contracte de projecte i Projecte utilitzen llistes de preus de vendes que s'adjunten al compte de clients o a la zona de vendes per determinar les tarifes de facturació i els possibles ingressos en el compromís del projecte.

Les llistes de preus de cost estan associades amb unitats organitzatives. Les entitats transaccionals com ara Oportunitat, Oferta, Contracte de projecte i Projecte utilitzen llistes de preus de cost que s'adjunten a la unitat de contractació per determinar els costos d'un compromís de projecte.

#### <a name="are-organizational-units-hierarchical-in-project-operations"></a>Les unitats organitzatives estan jerarquitzades al Project Operations?

No. A la versió actual del Project Operations, les unitats organitzatives no estan jerarquitzades. Per tant, no podeu realitzar les següents tasques:

- Configurar un patró per introduir preus de cost per defecte que travessin una jerarquia.
- Informar dels ingressos o els costos que tenen lloc en diferents nivells de la jerarquia d'unitats de l'organització.

#### <a name="were-a-big-multinational-firm-that-has-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Som una gran empresa multinacional que té una jerarquia complexa i multinivell de centres de cost, divisions i oficines de facturació. Com es pot utilitzar millor el concepte d'unitats organitzatives en la versió actual del Project Operations?

Quan teniu una jerarquia complexa de centres de cost, divisions, oficines de facturació, etc.,, configureu els nodes fulla d'aquesta jerarquia com a unitats organitzatives diferents.

A l'exemple següent es mostra una jerarquia típica.

**Contoso India**

- Pràctica SAP

    - Consultors tècnics
    - Consultors funcionals

- Pràctica de tecnologia de Microsoft

    - Consultors tècnics
    - Consultors funcionals

**Contoso EUA**

- Pràctica SAP

    - Consultors tècnics
    - Consultors funcionals

- Pràctica de tecnologia de Microsoft

    - Consultors tècnics
    - Consultors funcionals

Si la vostra jerarquia s'assembla a la d'aquest exemple, heu de configurar-la com una llista plana, com es mostra aquí:

- Contoso India - Pràctica SAP - Consultors tècnics
- Contoso India - Pràctica SAP - Consultors funcionals
- Contoso India - Pràctica de tecnologia de Microsoft - Consultors funcionals
- Contoso India - Pràctica de tecnologia de Microsoft - Consultors funcionals
- Contoso US - Pràctica SAP - Consultors tècnics
- Contoso US - Pràctica SAP - Consultors funcionals
- Contoso US - Pràctica de tecnologia de Microsoft - Consultors tècnics
- Contoso US - Pràctica de tecnologia de Microsoft - Consultors funcionals

#### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-concept-of-organizational-units-in-the-current-version-of-project-operations"></a>Som una petita empresa de serveis professionals que només opera com una divisió. Com es pot utilitzar millor el concepte d'unitats organitzatives en la versió actual del Project Operations?

Si la vostra empresa funciona com una unitat que té una llista de preus de cost, no cal que configureu cap unitat organitzativa. La instal·lació del Project Operations crea una unitat organitzativa per defecte que té el mateix nom que l'organització. Per defecte, tots els usuaris s'assignen a aquesta unitat organitzativa. Sempre que el sistema requereixi que es seleccioni una unitat organitzativa, aquesta unitat organitzativa se selecciona per defecte.

#### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-what-is-the-default-contracting-unit-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract"></a>Quan es crea un projecte des d'una oferta o d'una línia de contracte del projecte, la unitat de contractació per defecte procedeix del contracte d'oferta o de projecte. Quina és la unitat de contractació per defecte si es crea un projecte abans que les entitats de vendes, com ara Oferta o Contracte de projecte?

Quan es crea un projecte pel seu compte, la unitat de contractació per defecte del projecte es basa en l'usuari que la crea. Aquest usuari també és l'administrador del projecte per defecte. Si el projecte s'assigna a una entitat de vendes, com ara una oferta o un contracte de projecte, la unitat de contractació del projecte es basa en l'entitat de vendes en el seu lloc. En aquest cas, les estimacions de projecte es poden tornar a calcular, ja que la llista de preus de cost s'utilitza per calcular els canvis d'estimació de costos si es modifica la unitat de contractació. La llista de preus de vendes s'utilitza per calcular les estimacions de vendes que es canviaran de manera que estiguin sincronitzades amb la llista de preus del projecte de l'oferta.

Els camps **Unitat de contractació** i **Moneda** del projecte estan blocats per editar-se, ja que han d'estar sincronitzats amb els valors de l'entitat de vendes (oferta o contracte de projecte) a la qual s'assigna el projecte.

## <a name="create-and-maintain-organizational-units-in-project-operations"></a>Crear i mantenir unitats de l'organització al Project Operations

Seguiu aquests passos per crear una unitat organitzativa al Project Operations.

1. Aneu a **Configuració \> Unitats organitzatives**.
2. Seleccioneu **Crea**.
3. A l'àrea **General**, al camp **Nom**, introduïu un nom per a la unitat organitzativa. A continuació, definiu els altres camps segons calgui.
4. Seleccioneu **Desa** per crear el registre per tal que el pugueu continuar editant.
5. A **Llistes de preus de cost**, seleccioneu el signe de més (**+**) per afegir una llista de preus. Aquí només podeu afegir llistes de preus que tinguin el context **Cost**.
6. Al camp **Nom**, seleccioneu el botó **Cerca** i seleccioneu una llista de preus que vulgueu que estigui disponible per a la unitat organitzativa. Continueu afegint llistes de preus segons sigui necessari.
7. Quan hagueu acabat d'afegir llistes de preus, seleccioneu la icona **Desa** a la cantonada inferior dreta de la pàgina.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
