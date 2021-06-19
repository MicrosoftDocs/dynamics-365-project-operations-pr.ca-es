---
title: Àrea de treball mòbil Entrada de temps del projecte
description: En aquest tema es proporciona informació sobre l'àrea de treball mòbil Entrada de temps del projecte. Aquesta àrea de treball permet als usuaris introduir i desar el temps d'un projecte mitjançant el seu dispositiu mòbil.
author: Yowelle
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f087e15780272fd376a14b42ed9e00420f86a61f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009919"
---
# <a name="project-time-entry-mobile-workspace"></a>Àrea de treball mòbil Entrada de temps del projecte

[!include [banner](../includes/banner.md)]

En aquest tema es proporciona informació sobre l'àrea de treball mòbil **Entrada de temps del projecte**. Aquesta àrea de treball permet als usuaris introduir i desar el temps d'un projecte mitjançant el seu dispositiu mòbil.

Aquesta àrea de treball mòbil està dissenyada per utilitzar-se amb l'aplicació mòbil Dynamics 365 Unified Ops. 

## <a name="overview"></a>Informació general
Com a part del seu treball diari, els recursos del projecte sovint són in situ o desplaçant-se. L'àrea de treball mòbil **Entrada de temps del projecte** permet que els usuaris introdueixin el seu temps facturable o no facturable d'un projecte al dispositiu mòbil de la seva elecció. Per tant, els recursos del projecte poden registrar entrades de temps en qualsevol moment i en qualsevol lloc. També poden visualitzar entrades de temps que ja s'han enregistrat. 

En concret, a l'àrea de treball mòbil **Entrada de temps del projecte**, els usuaris poden dur a terme aquestes tasques:

-   Per a qualsevol data seleccionada, introduir el nombre d'hores que heu dedicat a una tasca concreta.
-   Cercar el nom del projecte o el client per trobar el projecte per al qual voleu introduir temps.
-   Especificar la categoria i l'activitat del temps que heu dedicat.
-   Enregistrar el temps com a facturable o no facturable per al projecte.
-   Opcionalment, introduir comentaris externs o interns.

## <a name="prerequisites"></a>Requisits previs
Els prerequisits difereixen, segons la versió del Microsoft Dynamics 365 que s'hagi implementat per a la vostra organització.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisits previs si utilitzeu el Dynamics 365 Finance
Si el Finance s'ha implementat per a la vostra organització, l'administrador del sistema ha de publicar l'àrea de treball mòbil **Entrada de temps del projecte**. Per obtenir instruccions, vegeu [Publicar una àrea de treball mòbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Requisits previs si utilitzeu la versió 1611 amb l'actualització de la plataforma 3 o posterior
Si la versió 1611 amb l'actualització de la plataforma 3 o posterior s'ha implementat per a la vostra organització, l'administrador del sistema ha de completar els requisits previs següents. 

<table>
<thead>
<tr class="header">
<th>Requisit previ</th>
<th>Funció</th>
<th>Descripció</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementeu la 4018050 KB.</td>
<td>Administrador del sistema</td>
<td>La KB 4018050 és una actualització d'X++ o correcció de les metadades que conté l'àrea de treball mòbil <strong>Entrada de temps del projecte</strong>. Per implementar la 4018050 KB, l'administrador del sistema ha de seguir aquests passos.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Baixeu la correcció de metadades del Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instal·leu la correcció de metadades</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Creeu un paquet implementable</a> que contingui els models <strong>ApplicationSuite</strong> i <strong>ProjectMobile</strong> i, a continuació, carregueu el paquet implementable al LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apliqueu el paquet implementable</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiqueu l'àrea de treball mòbil <strong>Entrada de temps del projecte</strong>.</td>
<td>Administrador del sistema</td>
<td>Vegeu <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar una àrea de treball mòbil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Descarregar i instal·lar l'aplicació mòbil

Descarregueu i instal·leu l'aplicació mòbil Finance and Operations:

-   [Per a telèfons Android](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Per a iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar la sessió a l'aplicació mòbil
1.  Inicieu l'aplicació al dispositiu mòbil.
2.  Introduïu l'URL del Dynamics 365.
3.  La primera vegada que inicieu la sessió, se us demanarà el vostre nom d'usuari i la vostra contrasenya. Introduïu les vostres credencials.
4.  Després d'iniciar la sessió, es mostren les àrees de treball disponibles per a la vostra empresa. Heu de tenir en compte que si l'administrador del sistema publica una àrea de treball nova més tard, haureu d'actualitzar la llista d'àrees de treball mòbils.

[![Llisca avall per actualitzar](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Introduir el temps mitjançant l'àrea de treball mòbil Entrada de temps del projecte
1.  Al dispositiu mòbil, seleccioneu l'àrea de treball **Entrada de temps del projecte**.
2.  Seleccioneu **Entrada de temps**. Es mostren les dates del calendari de la setmana actual.
3.  Per a una data seleccionada, seleccioneu **Accions** &gt; **Entrada nova**.
4.  Introduïu el nombre d'hores que voleu enregistrar.
5.  Seleccioneu el projecte per a l'entrada de temps. Una llista mostra els projectes que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, vegeu [Plataforma mòbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
6.  Si el projecte no es troba a la llista, seleccioneu **Cerca**. Cerqueu per nom, o canvieu a la cerca per nom del projecte o per client.
7.  Seleccioneu una categoria. Una llista mostra les categories que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, vegeu [Plataforma mòbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
8.  Si la categoria no es troba a la llista, seleccioneu **Cerca**. Cerqueu per categoria o canvieu a la cerca per nom de la categoria.
9.  Seleccioneu una activitat. Una llista mostra les activitats que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, vegeu [Plataforma mòbil](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page).
10. Si l'activitat no es troba a la llista, seleccioneu **Cerca**. Cerqueu el número de l'activitat o canvieu a la cerca per propòsit.

11. Seleccioneu la propietat de línia.
12. Opcional: introduïu comentaris externs o interns.
13. Seleccioneu **Fet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]