---
title: Aplicació mòbil Project timesheet
description: En aquest tema es proporciona informació sobre l'aplicació mòbil Microsoft Dynamics 365 Project Timesheet. L'aplicació mòbil Project Timesheet permet que els usuaris presentin i aprovin els fulls d'hores per als projectes en el seu dispositiu mòbil.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b9cbd84ecb0d71a99982e158d7e0ea1e236fb369
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072385"
---
# <a name="project-timesheet-mobile-application"></a>Aplicació mòbil Project timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Informació general

L'aplicació mòbil Microsoft Dynamics 365 Project Timesheet permet que els usuaris presentin i aprovin els fulls d'hores per als projectes en el seu dispositiu mòbil (iPhone o Android). Aquesta aplicació mòbil presenta la funcionalitat de fulls d'hores de l'àrea d'administració de projectes i comptabilitat del Dynamics 365 Finance i millora la productivitat i l'eficiència dels usuaris, alhora que permet la introducció oportuna i l'aprovació dels fulls d'hores dels projectes.

## <a name="download-and-install-the-mobile-app"></a>Descarregar i instal·lar l'aplicació mòbil

Baixeu i instal·leu l' aplicació mòbil Microsoft Dynamics 365 Project Timesheet per a l'Android o iPhone des de la botiga mòbil del dispositiu.

## <a name="enable-the-app"></a>Habilitar l'aplicació 

Al Finance, l'aplicació mòbil Project Timesheet ha d'estar habilitada. Per habilitar la funcionalitat, aneu **Paràmetres de l'administració de projectes i comptabilitat \> Fulls d'hores** i seleccioneu el paràmetre **Habilita el Microsoft Dynamics 365 Project Timesheet**.

## <a name="sign-in-to-the-app"></a>Iniciar la sessió a l'aplicació

1.  Inicieu l'aplicació al dispositiu mòbil.

2.  Introduïu l'URL del Finance.

3.  La primera vegada que inicieu la sessió, se us demanarà el vostre nom d'usuari i la vostra contrasenya. Introduïu les vostres credencials.

4.  L'haureu d'iniciar la sessió a l'empresa per defecte.

## <a name="submit-a-project-timesheet"></a>Enviar un full d'hores del projecte

Podeu crear i enviar un full d'hores del projecte a l'aplicació. Podeu basar un nou full d'hores en la informació d'un full d'hores anterior, línies desades o assignacions de projectes. Si se us designa com a delegat, també podeu introduir un full d'hores per a un altre treballador. Per crear un full d'hores com a delegat, seleccioneu el botó **Menú** i, a continuació, seleccioneu un nom de recurs.

La pàgina de full d'hores crearà un nou full d'hores per al període del full d'hores, en funció de la data actual. Es mostrarà la setmana de treball. Si el període de temps del full d'hores cobreix diverses setmanes, podeu seleccionar una altra setmana de treball des de les pestanyes de setmana de treball.
Si hi ha un full d'hores per a la data actual, es mostrarà. Si heu de crear un nou full d'hores en un període de temps diferent, seleccioneu el botó **Menú** i, a continuació, seleccioneu **Full d'hores nou**.

Podeu introduir informació del projecte fent clic a l'acció **Afegeix hores** o l'acció **Copia les hores de**. L'acció **Copia les hores de** copiarà la informació de la línia de projecte, però no les hores. El menú **Copia les hores de** inclou les opcions següents:

- **Copia d'un full d'hores existent** : les línies del full d'hores d'un full d'hores existent.

- **Copia d'un preferit** : creeu les noves línies de full d'hores mitjançant la configuració de full d'hores que heu seleccionat com a preferida.

- **Copia des d'una assignació** : creeu noves línies de full d'hores des dels projectes assignats.

La informació del projecte que es mostra depèn dels paràmetres mòbils que hàgiu definit a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.

Al camp **Entitat jurídica** , seleccioneu l'entitat jurídica per a la qual heu dut a terme el treball del projecte. El camp **Entitat jurídica** només està disponible si s'ha habilitat la compatibilitat amb els fulls d'hores entre empreses per a la vostra entitat jurídica.

Seleccioneu el client que està associat amb el projecte del full d'hores. Per a la versió inicial de l'Android, l'entrada per client no està admesa, ja que primer heu de seleccionar el projecte. Si heu seleccionat primer el projecte, el camp **Client** s'emplena automàticament.

Al camp **Projecte** , seleccioneu el projecte per al qual esteu introduint hores. El camp **Client** s'emplena automàticament.

Les cerques de clients i projectes permeten cercar entre clients i projectes.

Seleccioneu la informació als camps **Categoria** , **Activitat** , **Propietat de la línia** , **Grup d'impostos de vendes** i **Grup d'impostos de vendes d'articles** segons calgui. Aquests camps es poden substituir.

El camp **Propietat de la línia** es definirà en un valor per defecte, segons els paràmetres de l'administració de projectes i la comptabilitat. Quan s'habiliten els paràmetres de projecte/categoria i categoria/recurs, el valor de **Propietat de la línia** es definirà en el valor per defecte que heu definit per a aquesta validació. Quan els paràmetres de projecte/categoria i categoria/recurs no estan habilitats, el valor de **Propietat de la línia** serà per defecte segons el camp **Habilita la propietat de línia per defecte** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**. El valor **Propietat de la línia** es pot substituir.

Seleccioneu un dia per afegir-hi hores. Introduïu el nombre d'hores que heu treballat cada dia.

Per afegir comentaris sobre les hores que esteu introduint, feu clic a **Afegeix comentaris** i, a continuació, introduïu els comentaris per a un públic intern, públic del client o tots dos.
Els comentaris interns els poden visualitzar per administradors de projectes. Els comentaris del client s'inclouen a les factures.

Per desar la línia com a preferida, marqueu la casella de selecció i, a continuació, feu clic a **Desa com a preferida**.

La dimensió financera i la compatibilitat amb els fitxers adjunts no es proporcionen a l'aplicació mòbil.

Continueu afegint línies de projecte segons calgui per completar el vostre full d'hores.

Feu clic a **Envia** per enviar el full d'hores al flux de treball d'aprovació.

## <a name="review-timesheets"></a>Revisar els fulls d'hores

Hi ha disponible una llista dels fulls d'hores que s'han de revisar al menú. Aquesta opció només està disponible si heu estat designat aprovador de fluxos de treball. Es permet l'aprovació de la capçalera i la línia. L'aprovació de nivell de línia ofereix la capacitat de marcar una o diverses línies per a la seva aprovació. Després de revisar la informació del full de temps, feu clic a **Aprova** , **Delega** o **Retorna** per continuar el flux de treball.
