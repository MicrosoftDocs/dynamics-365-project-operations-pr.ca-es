---
title: Concessions del projecte
description: Aquest tema explica com crear o modificar una subvenció.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
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
ms.openlocfilehash: dfd91e859244cc03b9b358b057bded79eeea0182
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289357"
---
# <a name="project-grants"></a>Concessions del projecte

[!include [banner](../includes/banner.md)]

Una subvenció és un regal monetari per a un propòsit o projecte específic. En general, hi ha restriccions sobre com es pot gastar una subvenció. A Administració de projectes i comptabilitat, podeu introduir i fer un seguiment de les subvencions i definir les seves relacions amb projectes i contractes de projectes. Per exemple, podeu realitzar les següents tasques:

- Associar subvencions amb projectes i fonts de finançament a través d'enllaços a les pàgines **Projecte** i **Detalls del contracte del projecte**.
- Introduir i fer un seguiment dels canvis d'una subvenció mentre passa d'un estat a un altre.
- Introduir i fer un seguiment dels costos, els imports sol·licitats i els imports concedits.
- Crear subvencions mestres i associar-hi subvencions secundàries.

Podeu crear una subvenció introduint tots els detalls en un nou registre o podeu copiar els detalls d'una subvenció existent i després actualitzar-los.

## <a name="create-a-new-grant"></a>Crear una subvenció nova

1. Aneu a **Administració de projectes i comptabilitat** \> **Subvencions** \> **Subvencions**.
2. Seleccioneu **Nova** \> **Subvenció**.
3. A la pàgina de detalls de la subvenció, al FastTab **General**, al camp **ID de subvenció**, introduïu un identificador alfanumèric per a la subvenció.
4. En el camp **Nom de la subvenció**, introduïu un nom per a la subvenció.
5. Al camp **Descripció**, afegiu detalls sobre la nova subvenció.

    La majoria dels altres camps de la pàgina són opcionals i podeu introduir tanta informació com vulgueu.

    La següent llista descriu la informació que s'especifica a cada FastTab de detalls de la subvenció:

    - **General**: introduïu el nom de la subvenció, estat, descripció, propòsit i import.
    - **Informació de contacte**: introduïu detalls sobre els membres del personal, el departament que administra la subvenció i el client de la subvenció o la font d'organització de la subvenció. També podeu indicar si la vostra organització és una entitat de traspàs que rep la subvenció i després la transfereix a un altre destinatari. Seleccioneu **Afegeix** per afegir informació de contacte com ara números de telèfon i adreces de correu electrònic per a l'organització que proporciona la subvenció.
    - **Dates i terminis**: introduïu les dates relacionades amb la concessió i la sol·licitud de la subvenció. Alguns exemples inclouen la data de venciment de la sol·licitud, la data de presentació i la data en què la subvenció és aprovada o rebutjada.
    - **Projectes i contractes de projecte associats**: podeu introduir informació en aquest FastTab només si el camp **Estat de la subvenció** al FastTab **General** està definit a **Activa** o **Concedida**. Seleccioneu entre les següents opcions per completar la tasca relacionada:

        - **Afegeix una font de finançament**: afegiu una nova font de finançament per a la subvenció. Ara podeu introduir tots els detalls, o podeu utilitzar la informació per defecte i actualitzar-la més tard.
        - **Afegeix un contracte de projecte**: afegiu o actualitzeu la informació del contracte del projecte.
        - **Afegeix un projecte**: afegiu o actualitzeu els detalls del projecte.

    - **Configura**: introduïu els detalls sobre els fons coincidents, si aquesta informació és necessària. Moltes organitzacions que concedeixen subvencions requereixen que els destinataris gastin una quantitat específica dels seus propis diners o recursos que coincideixi amb l'import que es concedeix en la subvenció. En el camp **ID de projecte local o de seguiment**, podeu introduir un identificador que sigui diferent de l'identificador del projecte.

        > [!NOTE]
        > Si part de la subvenció es concedeix a una organització diferent, definiu l'opció **Subvenció secundària** a **Sí**. Per a les subvencions concedides als Estats Units, podeu especificar si una subvenció serà concedida sota un mandat estatal o un mandat federal.

    - **Detalls de rebuig**: afegiu o actualitzeu la informació sobre la freqüència amb què es poden retirar, facturar o gastar els fons.

## <a name="create-a-new-grant-from-a-copy"></a>Crear una subvenció nova a partir d'una còpia

1. Aneu a **Administració de projectes i comptabilitat** \> **Subvencions** \> **Subvencions**.
2. Seleccioneu **Nou** \> **Copia d'una concessió**.
3. Introduïu un identificador alfanumèric i un nom per a la nova subvenció i seleccioneu **D'acord**.
4. A la pàgina de detalls de la subvenció, reviseu els detalls de la subvenció copiada i feu qualsevol canvi que sigui necessari. La majoria dels camps de la pàgina són opcionals.

## <a name="view-or-modify-grant-details"></a>Veure o modificar els detalls de la subvenció

1. Aneu a **Administració de projectes i comptabilitat** \> **Subvencions** \> **Subvencions**.
2. Seleccioneu la subvenció que voleu modificar.
3. A la subfinestra d'acció, a la pestanya **Subvenció**, al grup **Manteniment**, seleccioneu **Edita**.
4. Reviseu els detalls de la subvenció i feu qualsevol canvi que sigui necessari.


[!INCLUDE[footer-include](../includes/footer-banner.md)]