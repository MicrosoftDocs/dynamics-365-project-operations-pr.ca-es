---
title: Despeses per dia
description: En aquest article s'ofereix informació sobre com treballar amb les despeses de per diem.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923176"
---
# <a name="per-diem-expenses"></a>Despeses per dia

> [!IMPORTANT] 
> La funcionalitat que es descriu en aquest article està disponible per als usuaris orientats com a part d'una versió de visualització prèvia.

Un pagament per diem és una assignació diària fixa i predeterminada que una empresa paga als seus empleats per allotjament (hotels), menjars i despeses incidentals en què incorren aquests empleats mentre viatgen per feina. L'empresa paga aquesta assignació als empleats en lloc de pagar les despeses reals de viatge. Els empleats poden utilitzar la seva **franquícia incidentals / altres** per diem per cobrir consells, servei d'habitacions, bugaderia o serveis de rentatge en sec per a reunions de negocis importants. La tarifa per diem pot variar, depenent de si l'empresari opta per reemborsar el cost combinat de l'allotjament i els àpats, o només pel cost dels àpats i les despeses addicionals.

Els percentatges de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos. Quan creeu una regla de per diem, podeu especificar que es retindrà un percentatge de la taxa per diem si un empleat rep àpats o serveis gratuïts. També pots establir un nombre mínim d'hores i un nombre màxim d'hores que la tarifa per diem es pot aplicar al viatge d'un empleat.

El per diem es calcula com l'assignació total que s'ofereix per dia menys la reducció de menjar (cost dels àpats gratuïts) que es proporciona al treballador.

## <a name="configure-per-diems"></a>Configure per diems

Per configurar les despeses de per diem, seguiu aquests passos.

1. Aneu als **paràmetres** de gestió general \>**de** despeses de gestió \>**·** \> **de** despeses.
2. A la **pestanya Per diem**, a la Calcula la **reducció dels àpats per** camp, seleccioneu com s'han de calcular els diems:

    - **Tipus d'àpat per viatge** – Calculeu el per diem en funció del tipus de menjar que s'introdueix (esmorzar, dinar o sopar) i de la reducció de menjar que s'especifica per a cada tipus de menjar per a la franquícia per diem durant la durada del viatge.
    - **Tipus de menjar per dia** : Calculeu el per diem en funció del tipus de menjar que s'introdueix i de la reducció de menjar que s'especifica per a cada tipus de menjar per a la franquícia per diem per dia.
    - **Nombre d'àpats per dia** - Calculeu el per diem en funció del nombre d'àpats que s'introdueixen al dia i de la reducció dels àpats per al nombre d'àpats que es proporcionen cada dia.

3. Aneu a **Càlculs de configuració de gestió** \> **de** \> **despeses i codis** \> **Ubicacions** per diem.
4. Afegiu ubicacions on es pugui utilitzar per diems.
5. Per a cada ubicació que afegiu, a la **pestanya Per diems**, seleccioneu la tarifa per diem i la moneda que són vàlides entre dates d'inici i finalització específiques per a l'allotjament, els àpats i altres despeses. Per configurar les tarifes i les monedes per diem, aneu a **Càlculs de configuració de** \> **gestió** \> **de despeses i codis** \> **Per diems.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Per diems a la interfície de despeses reimaginada

La característica per diem és compatible amb l'espai de treball de gestió de **despeses reimaginat** en Microsoft Dynamics 365 Finance versió 10.0.25 i posteriors.

Per habilitar per diems, seguiu aquests passos.

1. A l'àrea **de treball Gestió de** funcions, cerqueu i seleccioneu la **característica Informes de despeses reimaginada** a la llista i, a continuació, seleccioneu **Habilita ara**.
2. Cerqueu i seleccioneu la funció d'interfície **per**-diem per a l'informe de despeses a la llista i, a continuació, seleccioneu **Habilita ara**.

## <a name="how-the-feature-works"></a>Com funciona la característica

Aquesta secció proporciona exemples per a tres escenaris de configuració. Per a cada exemple, el Valora la **reducció de menjar per** camp s'estableix en un valor diferent. Per als tres exemples, l'import total que s'ha de pagar és el mateix fins que s'aplica la reducció del menjar. Després d'aquest punt, l'import total a pagar difereix per a cada exemple.

Per crear la despesa per diem que s'utilitza per als tres exemples, seguiu aquests passos.

1. Aneu a Gestió de despeses d'espais **de treball** \> **.**
2. Seleccioneu **Informe de despeses** nou o seleccioneu un informe de despeses existent.
3. Afegiu-hi una nova despesa. **Al camp Categoria**, seleccioneu **Per diem**. Seleccioneu la ubicació i les dates d'inici i finalització del viatge. El per diem per allotjament, menjars i incidentals (altres despeses) es calcula en funció de la bonificació diària que s'estableix per a la ubicació seleccionada.

    Per exemple, seleccioneu **Redmond (EUA)** com a ubicació. L'assignació diària per a aquesta ubicació és de 150 dòlars nord-americans (150 dòlars) per a allotjament, USD 75 per als àpats i USD 5 per a incidents. La data d'inici és el 10 de gener i la data de finalització és el 14 de gener. Per tant, la durada seleccionada és de cinc dies quan la configuració seleccionada és de dies naturals amb hora, i l'hora seleccionada comença i acaba a les 12:00 en les dates d'inici i finalització. Aquests són els càlculs:

    - Import total a pagar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Menjar i part incidental de l'import total = 5 × (75 + 5) = USD 400

Si durant el viatge es proporcionaven esmorzars, dinars i sopars, aquests àpats s'han de tenir en compte com a reducció de menjar.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemple 1: Per diem on les reduccions de menjar es basen en el tipus de menjar per viatge

En aquest exemple, la reducció dels àpats és del 30% per a l'esmorzar, del 30% per al dinar i del 40% per al sopar. A la **pàgina Paràmetres** de gestió de despeses, la reducció de menjar per **camp s'estableix** en **tipus de menjar per viatge**. Aquests són els càlculs si es van proporcionar tres esmorzars, dos dinars i sopars zero a l'empleat:

- Reducció de menjar = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Àpats i incidentals = 400 – 112,50 = USD 287.50
- Import total a pagar = Assignació total – Reducció de menjar = 1.150 – 112,50 = USD 1,037.50

![Despesa per diem en què la reducció del menjar es basi en el tipus de menjar per viatge.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemple 2: Per diem on les reduccions dels àpats es basen en el tipus de menjar per dia

En aquest exemple, la reducció dels àpats és del 30% per a l'esmorzar, del 30% per al dinar i del 40% per al sopar. A la **pàgina Paràmetres** de gestió de despeses, la **reducció de menjar per** camp es defineix en **tipus àpat per dia**. En aquest cas, a la **quadrícula Àpats** del quadre de diàleg Edita les **despeses**, des clearu les caselles de selecció per indicar quins àpats se us han proporcionat durant el viatge.

Per exemple, aquí teniu els càlculs si l'esmorzar es va proporcionar durant els tres primers dies del viatge:

- Reducció diària de l'àpat per a cada un dels tres primers dies = 75 × 30% = USD 22.50
- Reducció total dels àpats = 3 × 22,50 = USD 67.50
- Menjars i incidentals per als dies 1 a 3 = 75 - 22,50 = USD 57.50
- Menjars totals i incidentals = Suma d'àpats i incidents al llarg de cinc dies = 400 - 67,50 = USD 332.50
- Import total a pagar = Import total – Reducció del menjar = 1.150 – 67,50 = USD 1,082.50

![Despesa per diem quan la reducció del menjar es basa en el tipus de menjar per dia.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemple 3: Per diem on les reduccions de menjar es basen en el nombre d'àpats al dia

En aquest exemple, la reducció dels àpats es calcula en funció del nombre d'àpats que es van proporcionar per dia (és a dir, la pàgina Calcula la **reducció dels àpats per** camp a la **pàgina Paràmetres** de gestió de despeses s'estableix en **Nombre d'àpats per dia**). A la **quadrícula Àpats** del quadre de **diàleg Edita la despesa**, des clearu les caselles de selecció per indicar quins àpats s'han proporcionat.
En aquest cas, la reducció de l'àpat es basa només en el # dels àpats proporcionats, i no en el tipus de menjar (Esmorzar / dinar / sopar) proporcionat.

Aquests són els càlculs per diems quan es USD 150 l'assignació diària per a l'allotjament, USD 75 per als àpats i USD 5 per a incidents:

- **Import total a** pagar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Un àpat:** Reducció dels àpats = 20% = USD 15
- **Dos àpats:** Reducció de menjar = 50% = USD 37.50
- **Tres àpats:** Reducció de menjars = 100% = USD 75

Aquests són els càlculs de la bonificació **d'àpats** i incidències, que inclou USD 5 per a incidents:

- Dia 1 - S'ofereixen dos àpats = (75 – 37.50) + 5 = 37.50 + 5 = USD 42.50
- Dia 2 - S'ofereixen dos àpats = (75 – 37.50) + 5 = 37.50 + 5 = USD 42.50
- Dia 3 - Un àpat proporcionat = (75 – 15) + 5 = 60 + 5 = USD 65
- Dia 4 - Àpats nuls proporcionats = (75-0) + 5 = 75 + 5 = USD 80
- Dia 5 - Tres àpats proporcionats = (75 – 75) + 5 = 0 + 5 = USD 5

- Total d'àpats i incidents = Àpats i incidents per al dia 1 + dia 2 + dia 3 + dia 4 + dia 5 = USD 235
- Reducció total dels àpats = Reducció de menjar per al dia 1 + dia 2 + dia 3 + dia 4 + dia 5 = 37.5 + 37.5 + 15 + 0 + 75 = USD 165
- Import total a pagar = Assignació total – Reducció total del menjar = USD 1,150 - USD 165 = USD 985

![Despesa per diem quan la reducció del menjar es basa en el nombre d'àpats per dia.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir de la versió 10.0.23 de Finances, si utilitzeu la interfície de despeses reimaginada, no podeu crear despeses per diem que tinguin dates superposades. Si ho intenteu, rebreu un missatge d'error.
