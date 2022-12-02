---
title: Configurar l'administració de despeses
description: Aquest article descriu les consideracions i les decisions que heu de prendre durant el procés de planificació abans de configurar l'administració de despeses al Microsoft Microsoft Dynamics 365 Finance.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9424b8aaf867254bde085cffaa649c846920cc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933986"
---
# <a name="configure-expense-management"></a>Configurar l'administració de despeses

Aquest article descriu les consideracions i les decisions que heu de prendre durant el procés de planificació abans de configurar l'administració de despeses. A l'administració de despeses, es pot emmagatzemar informació sobre els mètodes de pagament, les sol·licituds de viatge, els informes de despeses, les normes, etc.

Com que moltes de les decisions que preneu quan planifiqueu la vostra configuració per a l'administració de despeses es basen en la jerarquia i l'estructura financera de la vostra organització, cal que consulteu els documents de planificació per a aquestes àrees.

## <a name="intercompany-expenses"></a>Despeses entre empreses

Quan habiliteu les despeses entre empreses, permeteu que entitats jurídiques i empleats incorrin despeses en nom d'una altra entitat jurídica, i recapteu el pagament des de l'entitat jurídica d'ocupació de la vostra organització. Per exemple, un empleat de l'entitat jurídica A completa un projecte per a l'entitat jurídica B, i el projecte incorre en despeses relacionades amb els viatges. Si les despeses entre empreses estan habilitades, l'empleat pot presentar un informe de despeses que comptabilitzarà la despesa a l'entitat jurídica B i la despesa s'haurà de pagar l'entitat jurídica A. Si la vostra organització no té diverses entitats legals, no cal que habiliteu les despeses entre empreses.

**Decisió:** voleu habilitar les despeses entre empreses?

## <a name="financial-management"></a>Administració financera

L'administració de despeses està estretament integrada amb l'administració financera de la vostra organització. Bona part de la configuració per a l'administració de despeses es basarà en les decisions que heu pres sobre les finances de la vostra organització. Les següents seccions descriuen les diverses àrees que requereixen planificació i decisions, en funció de les decisions financeres de la vostra organització i les pautes del vostre equip de lideratge.

### <a name="per-diems"></a>Dietes

Heu de definir les dietes per a empleats que proporciona la vostra organització. Com que les dietes s'utilitzen normalment per cobrir despeses com ara àpats, allotjament i altres despeses incidentals, es poden crear regles per a les dietes que ofereix la vostra organització. Les tarifes de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos. Quan definiu una regla de dieta, podeu especificar que un percentatge de la tarifa de la dieta es retindrà si un treballador rep àpats o serveis gratuïts. També podeu definir nivells de dietes per establir el nombre mínim i màxim d'hores en què la tarifa de dieta es pot aplicar als viatges d'un treballador.

**Decisions:**

- Regles predeterminades de dietes per al primer i l'últim dia:

    - Quin és el nombre mínim d'hores que un empleat pot reclamar per a un dia i rebre una dieta?
    - Hi ha una reducció de l'import que s'ofereix per als àpats durant el primer dia i l'últim dia? Si hi ha una reducció, quin és el percentatge de la reducció?
    - Hi ha una reducció de l'import que s'ofereix per a un hotel durant el primer dia i l'últim dia? Si hi ha una reducció, quin és el percentatge de la reducció?
    - Hi ha una reducció de l'import que s'ofereix per a altres despeses incorregudes durant el primer dia i l'últim dia? Si hi ha una reducció, quin és el percentatge de la reducció?

- Regles de dietes per defecte:

    - Hi ha una reducció percentual de les dietes per a cada àpat si, per exemple, l'àpat és complementari? Si hi ha una reducció, quin és el percentatge de reducció de cada àpat?
    - Es calcula la reducció d'àpats per dia, per viatge o per nombre d'àpats al dia?
    - S'han d'arrodonir els imports de les dietes de manera normal o arrodonir-los cap amunt?
    - Es calculen les dietes en un període de 24 hores o en un dia de calendari?

- Regles de dietes que es basen en la ubicació:

    - Les tarifes de les dietes varien segons la ubicació? Quines ubicacions s'inclouen?
    - Si les tarifes de les dietes varien segons la ubicació, per a cada ubicació, quina quantitat percentual es proporciona per als següents tipus de despeses:

        - Àpats
        - Hotels
        - Altres despeses

### <a name="expense-management-journals-and-accounts"></a>Diaris i comptes d'administració de despeses

L'administració de despeses requereix que utilitzeu diversos diaris i comptes. Heu de decidir, per exemple, si s'utilitza el mateix compte per als avançaments d'efectiu i les disputes de targetes de crèdit.

**Decisions:**

- A quin llibre diari es comptabilitzen els informes de despeses aprovats?
- Quin compte s'utilitza per als avançaments d'efectiu?
- Cal comptabilitzar immediatament els avançaments d'efectiu?

### <a name="payment-methods"></a>Mètodes de pagament

Quan es permet als empleats incórrer despeses en nom del seu negoci, cal definir els mètodes de pagament que poden utilitzar els empleats. Per exemple, es podria permetre als empleats utilitzar diners en efectiu o una targeta de crèdit corporativa. També es podria permetre que els empleats utilitzessin targetes de crèdit personals i després reemborsar als empleats. Heu de prendre les següents decisions per a cada mètode de pagament que permeteu.

**Decisions:**

- Quins mètodes de pagament es permeten?
- Qui és el propietari del mètode de pagament?
- Hi ha un tipus de compte de desplaçament? Si hi ha un tipus de compte de desplaçament, quin és?
- Si hi ha un compte de desplaçament, quin és el compte?
- Si el mètode de pagament és una targeta de crèdit, hauria d'utilitzar-se el mètode de pagament únicament amb transaccions importades?

### <a name="expense-categories-and-shared-categories"></a>Categories de despeses i categories compartides

Quan els empleats creen un informe de despeses, cada despesa que registren s'ha d'associar amb una categoria de despesa. Les categories de despeses es deriven de les categories compartides que es poden compartir amb els organismes jurídics de l'organització. Aquestes categories també es poden compartir a l'administració de projectes i la comptabilitat, en funció de la forma com es defineixi la vostra organització. Segons la definició de l'organització i de l'orientació de l'equip d'implementació, cal que determineu si les categories que s'utilitzen a l'administració de despeses només s'utilitzaran a l'administració de despeses o si s'han de compartir entre l'administració de projectes i la comptabilitzat i l'administració de despeses. Tingueu en compte que aquestes categories es poden compartir entre el projecte i la despesa i el projecte i producció, però no entre la despesa i producció. Heu de prendre les següents decisions per a cada categoria de despeses.

**Decisions:**

- Quina és la categoria de despesa? Alguns exemples són categories per a vols, hotels o quilometratge.
- La categoria de despesa també pot utilitzar-se en l'administració de projectes i la comptabilitat?
- Quin és el tipus de despesa?
- Què és el mètode de pagament per defecte per a la categoria de despesa?
- Les despeses de la categoria de despesa s'hauran de desglossar?
- Què és el compte per defecte principal per a la categoria de despesa?
- Què és el grup d'impostos de vendes de l'element per a la categoria de despeses?
- Es permeten mètodes de pagament addicionals per a la categoria de despeses? Si es permeten mètodes de pagament addicionals, quins són?
- Hi ha subcategories en aquesta categoria de despeses? Si hi ha subcategories, també heu de prendre les següents decisions:

    - S'exclou cap subcategoria de la recuperació d'impostos?
    - Quin és el grup d'impostos de vendes de l'element de les subcategories?

Si la categoria de despeses també s'utilitza a l'administració de projectes i la comptabilitat, responeu les preguntes restants. En cas contrari, passeu a la següent secció.

- Quins comptes de cost s'utilitzaran per a les despeses següents?

    - Cost
    - Assignació de nòmines
    - En curs: valor de cost
    - Cost: article
    - En curs: valor de cost: article
    - Pèrdua acumulada
    - En curs: pèrdua acumulada

- Quins comptes d'ingressos s'utilitzaran per al següent?

    - Ingressos facturats
    - Ingressos acumulats: valor de vendes
    - En curs: valor de vendes
    - Ingressos acumulats: producció
    - En curs: producció
    - Ingressos acumulats: beneficis
    - En curs: beneficis
    - Ingressos acumulats: subscripció
    - En curs: subscripció

### <a name="taxes"></a>Impostos

Per als impostos relacionats amb les despeses, cal determinar què s'inclou o està habilitat als informes de despeses.

**Decisions:**

- S'inclou l'impost sobre les vendes en els imports de les despeses?
- S'hauria d'habilitar la recuperació de despeses a les despeses?

    > [!NOTE]
    > Quan vau planificar el llibre major, si vau decidir aplicar l'impost de vendes dels EUA i utilitzar regles d'impostos, no podeu habilitar la recuperació d'impostos sobre les despeses. (Per aplicar l'impost de vendes dels EUA i utilitzar regles d'impostos, definiu l'opció **Aplica les regles dels impostos de vendes** a **Sí**.)

## <a name="policies"></a>Normes

Mitjançant la creació de normes d'informe de despeses, podeu ajudar a la vostra organització a estalviar temps i diners quan els empleats incorren despeses en el seu nom. Les normes ajuden a garantir que els empleats es mantenen dins del pressupost, proporcionen tota la informació necessària i gasten diners només quan ho requereixen. Heu de prendre les següents decisions per a cada norma d'informe de despeses i cada norma d'aprovació de l'informe de despeses que creeu.

**Decisions:**

- Quin és el nom de la norma?
- Per a què serveix la norma de despeses?
- Si prèviament heu decidit permetre les despeses entre empreses, a quines empreses de la vostra organització s'aplicarà aquesta norma?
- Quan serà efectiva la norma?
- Quan venç la norma?
- Quina és la regla de la norma?
- Quin és el resultat de la regla de la norma?


[!INCLUDE[footer-include](../includes/footer-banner.md)]