---
title: Creació de contractes avançats per a la facturació basada en el progrés
description: Aquest tema explica com crear contractes de projectes de manera que es puguin generar factures per als clients, basades en un percentatge del treball completat.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289492"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Creació de contractes avançats per a la facturació basada en el progrés
[!include [banner](../includes/banner.md)]

Aquest tema explica com crear contractes de projectes de manera que es puguin crear factures per als clients, basades en un percentatge del treball completat. Els imports de la factura es calculen automàticament per a les categories de treball que heu configurat per a un projecte. El temps de la factura s'estableix quan es negocia el contracte del projecte amb el client.

Utilitzeu els procediments d'aquest tema per configurar un contracte, un projecte associat i les regles de facturació que calculen les quantitats de facturació per a les categories de pressupost de treball que heu establert per al projecte.

Després de crear el contracte i el projecte, podeu establir els detalls del projecte. Per exemple, podeu definir activitats i assignar treballadors al projecte.

## <a name="example"></a>Exemple

La vostra organització és una empresa de desenvolupament de programari. Acordeu desenvolupar un paquet de comptabilitat de nòmines per a un client per un total de 20.000 USD. La vostra organització acorda facturar al client a mesura que completeu percentatges específics del projecte. Configureu les següents categories de projectes per al treball, de manera que pugueu utilitzar-les en el procés de facturació:

- Consultoria
- Dissenyeu-ho
- Instal·lació

També configureu regles de facturació que calculen automàticament els imports de la factura per al percentatge de treball del projecte que s'ha completat per a cada categoria.

L'administrador de pressupostos crea un pressupost per a les categories del projecte. L'import del treball completat es calcula automàticament com un percentatge del treball real en comparació amb els imports pressupostats.

## <a name="prerequisites"></a>Requisits previs

Abans de crear un projecte que utilitzi regles de facturació, heu d'establir les seqüències de números per a les regles de facturació i un diari de tarifes que s'utilitza per comptabilitzar factures de progrés.

1. Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres de l'administració de projectes i comptabilitat**.
2. A la pàgina **Paràmetres de l'administració de projectes i comptabilitat**, a la pestanya **Seqüències de números**, configureu la seqüència de números que voleu utilitzar quan es creïn les regles de facturació.
3. Aneu a **Administració de projectes i comptabilitat** \> **Diaris** \> **Tarifa**.
4. A la pàgina **Diari de tarifes**, seleccioneu **Nou** i introduïu el nom del diari.

## <a name="create-a-contract-for-progress-billings"></a>Crear un contracte per a factures de progrés

Utilitzeu aquest procediment per crear un contracte de projecte per a un projecte de preu fix. Creeu una factura de projecte quan el treball completat en el projecte arriba a un percentatge especificat.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Contractes de projecte**.
2. A la pàgina **Contractes de projecte**, seleccioneu **Nou**.
3. En el quadre de diàleg **Nou contracte de projecte**, definiu els següents camps:

    - **Nom**
    - **Tipus de finançament**
    - **Font de finançament**
    - **Moneda de vendes**: per defecte, aquesta moneda s'utilitza per a les factures de client que estan associades amb el contracte del projecte. No obstant això, es pot canviar la moneda de vendes en una factura de client específica.

4. Seleccioneu **D'acord**. La informació es copia a la capçalera de la pàgina **Contractes de projecte**.
5. A la pàgina **Contractes de projecte**, empleneu la resta de la informació necessària per al projecte.

## <a name="create-a-project-for-progress-billings"></a>Crear un projecte per a factures de progrés

Seguiu aquests passos per crear un projecte i qualsevol subprojecte associat a un contracte de projecte.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes**.
2. A la pàgina **Tots els projectes**, seleccioneu **Nou**.
3. En el quadre de diàleg **Nou projecte**, en el camp **Tipus de projecte**, seleccioneu **Temps i material**.
4. Seleccioneu un grup de projectes. Un grup de projectes defineix la informació de comptabilització dels projectes que s'assignen al grup.
5. Seleccioneu **Crea el projecte**.
6. Després de crear el projecte, definiu la fase del projecte a **En procés**.

## <a name="create-a-budget-for-a-project"></a>Crear un pressupost per a un projecte

Les categories pressupostàries s'utilitzen per calcular automàticament els imports de la factura per al percentatge de treball completat per a cada categoria. Seguiu aquests passos per a crear categories pressupostàries per als costos estimats.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes**.
2. A la pàgina **Tots els projectes**, seleccioneu i obriu el projecte que vulgueu.
3. A la pàgina **Projectes**, a la subfinestra d'acció, a la pestanya **Pla**, al grup **Pressupost**, seleccioneu **Pressupost del projecte**.
4. A la pàgina **Pressupost del projecte**, introduïu un cost estimat per a cada categoria del projecte.

## <a name="create-billing-rules-for-progress-billings"></a>Crear regles de facturació per a factures de progrés

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Contractes de projecte**.
2. A la pàgina **Contractes del projecte**, seleccioneu i obriu un contracte de projecte.
3. A la pàgina de contractes del projecte, al FastTab **Regles de facturació**, seleccioneu **Afegeix**.
4. A la pàgina **Regla de facturació**, en el camp **Tipus de línia**, seleccioneu **Progrés**.
5. En el FastTab **Detalls de la línia de la regla de facturació**, en el camp **Valor del contracte**, introduïu el valor total del contracte.
6. En el camp **Categoria**, seleccioneu la categoria a la qual es comptabilitza la tarifa.
7. Al camp **Projecte**, seleccioneu el projecte que utilitza aquesta regla de facturació.
8. Opcional: assigneu la regla de facturació a projectes addicionals. Al FastTab **Projecte**, en la secció **Projectes disponibles**, seleccioneu un projecte i després seleccioneu el botó de fletxa dreta per afegir el projecte a la secció **Projectes seleccionats**.
9. Opcional: calculeu l'import percentual que el client reté dels pagaments d'una factura. Al FastTab **Termes de retenció de pagaments**, seleccioneu la font de finançament i, en el camp **Percentatge de retenció**, introduïu el percentatge de retenció.
10. Repetiu aquests passos per a crear regles de facturació addicionals per al contracte del projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]