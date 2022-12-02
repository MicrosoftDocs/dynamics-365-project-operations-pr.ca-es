---
title: Despeses per dia
description: En aquest article es proporciona informació sobre com treballar amb les despeses per dia.
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
> La funcionalitat que es descriu en aquest article està disponible per als usuaris de destinació com a part d'una versió preliminar.

Un pagament per dia és una cobertura diària fixa i predeterminada que una empresa paga als seus empleats per a l'allotjament (hotels), els àpats i les despeses incidentals en què els empleats incorren mentre viatgen per feina. L'empresa paga aquesta provisió als empleats en comptes de pagar les despeses reals del viatge. Els empleats poden utilitzar la seva provisió per dia d'**Incidentals/Altres** per cobrir propines, servei d'habitacions, bugaderia o serveis de rentat en sec per a reunions de negocis importants. La taxa per dia pot variar, en funció de si l'empleat tria de reemborsar el cost combinat de l'allotjament i els àpats o només el cost dels àpats i les despeses incidentals.

Els percentatges de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos. Quan creeu una regla per dia, podeu especificar que un percentatge de la tarifa per dia es retindrà si un empleat rep àpats o serveis gratuïts. També podeu definir un nombre mínim i màxim d'hores en què el percentatge per dia es pot aplicar als viatges d'un treballador.

Les dietes es calculen com la provisió total que s'ofereix per dia menys la reducció per àpats (cost dels àpats gratuïts) que es proporciona al treballador.

## <a name="configure-per-diems"></a>Configurar dietes

Per configurar despeses de dietes, seguiu aquests passos.

1. Aneu a **Administració de despeses** \> **Configuració** \> **General** \> **Paràmetres d'administració de despeses**.
2. A la pestanya **Dieta**, al camp **Calcula la reducció d'àpats per**, seleccioneu com s'han de calcular les dietes:

    - **Tipus d'àpat per viatge**: calculeu la dieta segons el tipus d'àpat que s'introdueix (esmorzar, dinar o sopar) i, a la reducció d'àpats que s'especifica per a cada tipus de provisió per dietes per a la durada del viatge.
    - **Tipus d'àpat per dia**: calculeu la dieta segons el tipus d'àpat que s'introdueix i, a la reducció d'àpats que s'especifica per a cada tipus de provisió per dietes per dia.
    - **Nombre d'àpats per dia** : calculeu la dieta a partir del nombre d'àpats que s'introdueixen al dia i la reducció d'àpats per al nombre d'àpats que es proporcionen cada dia.

3. Aneu a **Administració de despeses** \> **Configuració** \> **Càlculs i codis** \> **Ubicacions de dietes**.
4. Afegiu les ubicacions on es pot utilitzar les dietes.
5. Per a cadascuna de les ubicacions que afegiu, a la pestanya **Dietes**, seleccioneu una tarifa de dieta i la moneda que sigui vàlida entre les dates d'inici i d'acabament específiques per a allotjament, àpats i altres despeses. Per configurar les tarifes de dietes i les monedes, aneu a **Administració de despeses** \> **Configuració** \> **Càlculs i codis** \> **Dietes**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dietes a la nova interfície de despeses

La característica de dietes està admesa a la nova àrea de treball **Administració de despeses** del Microsoft Dynamics 365 Finance versió 10.0.25 i posterior.

Per habilitar les dietes, seguiu aquests passos.

1. A l'àrea de treball **Administració de característiques**, cerqueu i seleccioneu la característica **Nous informes de despeses** a la llista i, a continuació, seleccioneu **Habilita ara**.
2. Cerqueu i seleccioneu la característica **Nova interfície d'informe de dietes per a despeses** a la llista i, a continuació, seleccioneu **Habilita ara**.

## <a name="how-the-feature-works"></a>Com funciona la característica

Aquesta secció proporciona exemples de tres escenaris de configuració. Per a cada exemple, el camp **Calcula la reducció d'àpats per** es defineix com un valor diferent. Per als tres exemples, l'import total que es paga és el mateix fins que s'aplica la reducció d'àpats. Després d'aquest moment, l'import total que es pot paga és diferent per a cada exemple.

Per crear la despesa de dietes que s'utilitza per als tres exemples, seguiu aquests passos.

1. Aneu a **Àrees de treball** \> **Administració de despeses**.
2. Seleccioneu **Nou informe de despeses** o seleccioneu un informe de despeses existent.
3. Afegiu una despesa nova. Al camp **Categoria**, seleccioneu **Dieta**. Seleccioneu la ubicació i les dates d'inici i d'acabament del viatge. Les dietes per a allotjament, àpats i incidentals (altres despeses) es calculen segons la provisió diària que s'estableixi per a la ubicació seleccionada.

    Per exemple, seleccioneu **Redmond (EUA)** com a ubicació. La provisió diària d'aquesta ubicació és de 150 dòlars EUA (150 USD) per a l'allotjament, 75 USD per a àpats i 5 USD per a incidentals. La data d'inici és el 10 de gener i la data d'acabament és el 14 de gener. Per tant, la durada seleccionada és de cinc dies quan la configuració seleccionada són dies naturals amb temps, i el temps seleccionat comença i acaba a les 12:00 del matí a les dates d'inici i d'acabament. Els càlculs són els següents:

    - Import total per pagar = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
    - Part d'àpats i incidentals de l'import total = 5 × (75 + 5) = 400 USD

Si s'ha ofert l'esmorzar, el dinar i el sopar durant el viatge, aquests àpats s'han de comptar com una reducció d'àpats.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemple 1: Dieta on les reduccions d'àpats es basen en el tipus d'àpat per viatge

En aquest exemple, la reducció d'àpats és del 30 per cent per als esmorzars, el 30 per cent per als dinars i el 40 per cent per als sopars. A la pàgina **Paràmetres d'administració de despeses**, el camp **Calcula la reducció d'àpats per** es defineix com **Tipus d'àpat per viatge**. A continuació es mostren els càlculs si s'han ofert tres esmorzars, dos dinars i cap sopar a l'empleat:

- Reducció d'àpats = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Àpats i incidentals = 400 – 112,50 = 287,50 USD
- Import total per pagar = Provisió total – Reducció d'àpats = 1.150 – 112,50 = 1.037,50 USD

![Despesa en dietes on la reducció d'àpats es basa en el tipus d'àpat per viatge.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemple 2: Dieta on les reduccions d'àpats es basen en el tipus d'àpat per dia

En aquest exemple, la reducció d'àpats és del 30 per cent per als esmorzars, el 30 per cent per als dinars i el 40 per cent per als sopars. A la pàgina **Paràmetres d'administració de despeses**, el camp **Calcula la reducció d'àpats per** es defineix com **Tipus d'àpat per dia**. En aquest cas, a la quadrícula **Àpats** del quadre de diàleg **Edita la despesa**, desactiveu les caselles de selecció per indicar quins àpats se us han ofert durant el viatge.

Per exemple, aquí teniu els càlculs si s'ha ofert esmorzar els tres primers dies del viatge:

- Reducció d'àpats diària per als tres primers dies = 75 × 30% = 22,50 USD
- Reducció total d'àpats = 3 × 22,50 = 67,50 USD
- Àpats i incidentals els dies 1 a 3 = 75 – 22,50 = 57,50 USD
- Total d'àpats i incidentals = Suma d'àpats i incidentals en cinc dies = 400 – 67,50 = 332,50 USD
- Import total per pagar = Import total – Reducció d'àpats = 1.150 – 67,50 = 1.082,50 USD

![Despesa en dietes on la reducció d'àpats es basa en el tipus d'àpat per dia.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemple 3: Dieta on les reduccions d'àpats es basen en el nombre d'àpats per dia

En aquest exemple, la reducció d'àpats es calcula segons el nombre d'àpats que s'han ofert per dia (és a dir, el camp **Calcula la reducció d'àpats per** de la pàgina **Paràmetres d'administració de despeses** es defineix com a **Nombre d'àpats per dia**). A la quadrícula **Àpats** del quadre de diàleg **Edita la despesa**, desactiveu les caselles de selecció per indicar quins àpats se us han ofert.
En aquest cas, la reducció d'àpats es basa únicament en el nombre d'àpats oferts i no en el tipus d'àpats (esmorzar/dinar/sopar) ofert.

A continuació es mostren els càlculs de les dietes quan la provisió diària és de 150 USD per a l'allotjament, 75 USD per a als àpats i 5 USD per a incidentals:

- **Import total per pagar** = 5 × (150 + 75 + 5) = 5 × 230 = 1.150 USD
- **Un àpat**: reducció d'àpats = 20% = 15 USD
- **Dos àpats**: reducció d'àpats = 50% = 37,50 USD
- **Tres àpats**: reducció d'àpats = 100% = 75 USD

Aquests són els càlculs de la **provisió per a àpats i incidentals**, que inclou 5 USD per a incidentals:

- Dia 1 - Dos àpats oferts = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dia 2 - Dos àpats oferts = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Dia 3 - Un àpat ofert = (75 – 15) + 5 = 60 + 5 = 65 USD
- Dia 4 - Cap àpat ofert = (75-0) + 5 = 75 + 5 = 80 USD
- Dia 5 - Tres àpats oferts = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total d'àpats i incidentals = Àpats i incidentals per al dia 1+ dia 2 + dia 3+ dia 4 + dia 5 = 235 USD
- Reducció d'àpats total = Reducció d'àpats per al dia 1+ dia 2 + dia 3 + dia 4 + dia 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Import total per pagar = Provisió total – Reducció d'àpats total = 1.150 USD – 165 USD = 985 USD

![Despesa en dietes on la reducció d'àpats es basa en el nombre d'àpats per dia.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> A partir de la versió 10.0.23 del Finance, si utilitzeu la nova interfície de despeses, no podeu crear despeses de dietes que tinguin dates superposades. Si proveu de fer-ho, rebreu un missatge d'error.
