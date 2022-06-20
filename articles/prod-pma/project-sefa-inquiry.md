---
title: Consulta de la Planificació de despeses per a concessions federals
description: Aquest article proporciona informació sobre el calendari de despeses de la investigació dels premis federals.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: johnmichalak
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 00f9e97b9a6b3e8fe5e9cf9143e670612869b84c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916644"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Consulta de la Planificació de despeses per a concessions federals

[!include [banner](../includes/banner.md)]

Segons la circular A-133 de l'Oficina d'administració i pressupost, les agències que reben fons federals estan subjectes a requisits d'auditoria, que també es coneixen com a auditories individuals. El procés d'auditoria s'utilitza per a informar sobre els ingressos i despeses de les subvencions federals de manera recurrent. Part de l'informe d'auditoria individual inclou la Planificació de despeses de concessions federals (SEFA).

La consulta de Planificació de despeses de concessions federals inclou el títol i número del Catàleg d'assistència nacional federal (CFDA), el número de subvenció, l'any de la subvenció, el nom de l'agència federal que proporciona els fons i el nom de l'entitat de traspàs. La consulta és per a un període concret. En general, aquest període és el mateix que el període de declaració financera, que és un any fiscal.

La investigació inclou subvencions que tenen dates de projecció a l'interval de dates seleccionat. La columna **Agència que rep la subvenció** de la consulta mostra el client de la subvenció o, per a una subvenció de traspàs, l'agència que rep la subvenció. Per a una subvenció de traspàs, la columna **Agència de traspàs** mostra el client de subvenció. Si la subvenció no és una subvenció de traspàs, la columna **Agència de traspàs** està en blanc.

## <a name="set-up-the-cfda-clusters"></a>Configurar els grups de CFDA

Heu d'establir els grups de CFDA que es poden associar amb els números de CFDA a la consulta de la Planificació de despeses de concessions federals.

1. Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Grups del Catàleg d'assistència nacional federal**.
2. Seleccioneu **Nou** per crear un grup de CFDA.
3. Introduïu el nom del grup.
4. Seleccioneu **Desa** per desar els canvis.

## <a name="set-up-cfda-numbers"></a>Configurar els números de CFDA

Heu de configurar els números de CFDA que es poden afegir a les subvencions i incloure a la consulta de la Planificació de despeses de concessions federals.

1. Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Números del Catàleg d'assistència nacional federal**.
2. Seleccioneu **Nou** per crear un número de CFDA.
3. A la columna **Número**, introduïu el número de CFDA.
4. Premeu la tecla **Tab**.
5. A la columna **Descripció**, introduïu el títol de CFDA.
6. Premeu la tecla **Tab**.
7. Opcional: en el camp **Grup del programa**, afegiu el grup de CFDA corresponent.
8. Seleccioneu **Desa** per desar els canvis.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Configurar subvencions per informar-ne a la consulta de la Planificació de despeses de concessions federals

1. Aneu a **Administració de projectes i comptabilitat \> Subvencions \> Subvencions** i seleccioneu una subvenció existent.
2. Al FastTab **Configuració**, en el camp **Catàleg d'assistència nacional federal**, assigneu el número de CFDA. El número de CFDA a la subvenció determina el grup de CFDA per als informes.
3. Al FastTab **Informació del contacte**, introduïu la informació de qui rebrà la subvenció seguint aquests passos:

    1. En el camp **Client de la subvenció**, introduïu el client responsable de la subvenció. Per a una subvenció existent, aquesta informació ja podria estar introduïda.
    2. Indiqueu si el client de la subvenció és el finançador. Si el client de la subvenció és el finançador, deixeu la casella de selecció **Traspàs** sense marcar. Si un altre client és el finançador i el client de la subvenció és responsable de gastar i fer el seguiment dels diners, marqueu la casella de selecció **Traspàs**.

4. Si marqueu la casella de selecció **Traspàs** en el pas anterior, en el camp **Agència que proporciona la subvenció**, introduïu el client que va proporcionar la subvenció. L'agència que proporciona la subvenció i el client de la subvenció no poden ser el mateix client.

Aquí teniu un exemple de subvenció de traspàs:

El govern federal va finançar un projecte d'infraestructura per a un estat. El govern federal va donar els diners a l'estat perquè els gastés. En aquest cas, el govern federal és l'agència que proporciona la subvenció i l'estat és el client de la subvenció.

> [!NOTE] 
> Quan inicieu per primera vegada la funció, els números inicials de CFDA s'introduiran utilitzant els números existents en les subvencions.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Excloure subvencions de l'informe de SEFA en funció del tipus de subvenció

1. Aneu a **Administració de projectes i comptabilitat \> Configuració \> Subvencions \> Tipus de subvenció**.
2. Al FastTab **Informació per defecte**, marqueu la casella de selecció **Exclou de la Planificació de despeses de concessions federals**.
3. Seleccioneu **Desa** per desar els canvis.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Executar la consulta de la Planificació de despeses per a concessions federals

1. Aneu a **Administració de projectes i comptabilitat \> Consultes i informes \> Consulta de subvenció \> Planificació de despeses de concessions federals**.
2. A la secció **Paràmetres**, seguiu aquests passos:

    1. En el camp **Interval de dates**, seleccioneu el codi per a l'interval de dates. Alternativament, en els camps **Data d'inici** i **Data de finalització**, definiu l'interval de dates.
    2. Opcional: per incloure només les transaccions facturades com a ingressos en la consulta, establiu l'opció **Inclou només els ingressos facturats** a **Sí**.

## <a name="columns"></a>Columnes

La consulta de la Planificació de despeses de concessions federals inclou les següents columnes:

- Nom del grup del Catàleg d'assistència nacional federal
- Agència que proporciona la subvenció
- Agència de traspàs
- Nom de la subvenció
- ID de subvenció
- ID de sol·licitud de la subvenció
- Catàleg d'assistència nacional federal
- Rebuts
- Despeses


[!INCLUDE[footer-include](../includes/footer-banner.md)]