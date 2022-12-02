---
title: Novetats o canvis d'octubre de 2021 al Project Operations per a escenaris basats en producció/mantinguts en existències
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament d'octubre de 2021 del Project Operations per a escenaris basats en producció/ mantinguts en existències.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029931"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis d'octubre de 2021 al Project Operations per a escenaris basats en producció/mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.22
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|--------------|------------------|----------------|
| Administració i comptabilitat de projectes | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | El treball en procés (WIP) i els ingressos acumulats no s'inverteix correctament quan es comptabilitza una factura de client entre empreses. |
| Administració i comptabilitat de projectes | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | La funcionalitat **Evita el tancament del projecte si hi ha transaccions obertes** no funciona. |
| Administració i comptabilitat de projectes | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La classificació de facturació d'una factura de text lliure no emplena automàticament les dimensions dels projectes quan aquesta funcionalitat està habilitada. |
| Administració i comptabilitat de projectes | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En els escenaris que no són entre empreses, el WIP i els ingressos acumulats no s'inverteixen correctament quan es comptabilitza la factura del projecte. |
| Administració i comptabilitat de projectes | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Els valors de dèbit i abonament es canvien quan s'utilitza el complement del Microsoft Excel amb el llibre diari de despeses del projecte i el camp **Tipus de compte de desplaçament** està definit com a **Projecte**. |
| Administració i comptabilitat de projectes | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | L'import que es comptabilitza en les transaccions de projecte s'infla en una comanda de compra de projecte que inclou elements en existències i que té imports d'impostos no deduïbles quan s'ha marcat **UseTax**. |
| Administració i comptabilitat de projectes | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | El sistema divideix la quantitat entre els informes de guanys i pèrdues del projecte i els informes de WIP del projecte. |
| Administració i comptabilitat de projectes | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | L'inventari manual no és correcte després d'ajustar un requisit d'element retornat parcialment. |
| Administració i comptabilitat de projectes | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Els noms de recurs es dupliquen al Project Operations quan s'editen al Microsoft Project. |
| Administració i comptabilitat de projectes | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Els informes de despeses entre empreses que tenen costos de factura de proveïdor pendents de compte a pagar entre empreses de factura del proveïdor es comptabilitzen primer al tipus de comptabilització **Cost de WIP del projecte**. Tanmateix, durant el processament, els costos relacionats amb l'estimació es comptabilitzen en el tipus de comptabilització **Costdel projecte** en comptes del tipus de comptabilització **Cost entre empreses**. |
| Administració i comptabilitat de projectes | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Els resultats de retenció del proveïdor a les transaccions de despeses del projecte no es mostren. |
| Administració i comptabilitat de projectes | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | El full d'hores ha d'arrodonir l'import de la transacció en la moneda de la transacció a un nombre especificat de posicions decimals a totes les distribucions comptables i entrades d'assignació del llibre diari general. |
| Administració i comptabilitat de projectes | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Les quantitats dels requisits d'elements de projecte s'actualitzen automàticament quan se signen les comandes planificades. |
| Administració i comptabilitat de projectes | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | El número de val, el saldo del proveïdor de tipus de transaccions i el número de compte no es poden revertir a la factura de pagament previ d'una comanda de compra. |
| Administració i comptabilitat de projectes | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveïdor entre empreses falla quan la integració de factures del proveïdor està activada. |
| Administració i comptabilitat de projectes | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quan creeu un llibre de despeses del projecte, l'import de cost es mostra al camp **Crèdit**. |
| Administració i comptabilitat de projectes | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les condicions de pagament de les factures del projecte no funcionen com està previst. |
| Administració i comptabilitat de projectes | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Els vals del full d'hores es poden reutilitzar quan la seqüència de números es configura com a contínua. |
| Administració i comptabilitat de projectes | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANÇA: la lògica d'**Import de retenció manual** no coincideix amb la lògica d'**Import de retenció automàtic** a la proposta de factura del contracte del projecte. |
| Administració i comptabilitat de projectes | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quan s'allibera la retenció a proveïdors, la comptabilització de vals té línies addicionals incorrectes. |
| Administració i comptabilitat de projectes | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quan es canvia el camp **Data de la factura** a la pàgina **Crea una proposta de factura**, es pot produir l'error següent: "La referència d'objecte no s'ha definit com a instància d'un objecte". |
| Administració i comptabilitat de projectes | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Es produeix un error quan s'intenta aprovar un full d'hores del flux de treball **TSLine** i hi ha una norma de full d'hores per a dissabte i diumenge. |
| Administració i comptabilitat de projectes | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | El tipus d'element de projecte de saldo inicial s'exclou dels **resums de transaccions de proposta de factura** quan es calcula el total de la factura de la proposta de factura. |
| Administració i comptabilitat de projectes | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Si el cost del consum d'una comanda de producció del projecte és 0 (zero), l'error següent es produeix quan intenteu fer l'estimació: "S'ha intentat dividir per zero". |
| Administració i comptabilitat de projectes | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | L'aplicació del full d'hores del projecte per a Android deixa de respondre. El problema està relacionat amb **TimeEntryDataManager ArgumentNullException**. |
| Administració i comptabilitat de projectes | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | El diari d'integració del Project Operations falla quan el comptabilitzeu perquè falten dimensions en un compte. Tanmateix, el compte al qual falten les dimensions no és el compte al qual esteu comptabilitzant. |
| Administració i comptabilitat de projectes | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | El filtre **ToDate** en les cerques no s'esborra quan s'elimina del quadre de diàleg **Selecció** de la pàgina **Comptabilitza el cost**. |
| Administració i comptabilitat de projectes | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Restableix tota la distribució** falla i mostra un error per als fulls d'hores creats per a un projecte del tipus **Només temps**. |
| Administració i comptabilitat de projectes | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La pestanya **Projecte** no es pot editar en una factura del proveïdor pendent quan la categoria de proveïment està assignada a l'element. |
| Administració i comptabilitat de projectes | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta la subfinestra de navegació si no heu iniciat la sessió al Project Operations Dataverse. |
| Administració i comptabilitat de projectes | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Per a les transaccions d'ajustament del projecte entre empreses, hi ha problemes a l'empresa de destinació. |
| Administració i comptabilitat de projectes | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Els costos compromesos per a un projecte calculen una quantitat i preu de cost erronis si la comanda de compra s'ha processat amb **Processament de final d'any de la comanda de compra** al llibre de comptabilitat general. |
| Administració i comptabilitat de projectes | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quan s'informa que ha finalitzat una ordre de producció del projecte que té comandes de qualitat, es produeix l'error següent: "No hi ha cap transacció virtual marcada amb la transacció d'inventari". |
| Administració i comptabilitat de projectes | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quan es comptabilitza una factura de compte a pagar relacionada amb el projecte, es produeix l'error següent: "Projecte de text enumerat: cost: l'element no existeix". |
| Administració i comptabilitat de projectes | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Els costos indirectes es dupliquen quan s'acumulen manualment els ingressos. |
| Administració i comptabilitat de projectes | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | La comptabilitat d'ingressos acumulats i WIP no produeix transaccions. |
| Administració i comptabilitat de projectes | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | L'activació del preu pendent falla per a un article de cost estàndard quan hi ha una comanda de compra de projecte rebuda. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor revertit de WIP d'una comptabilització de factures és diferent del valor de WIP comptabilitzat original d'una entrada de temps. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Es produeix un error de comptabilització dels ingressos facturats del projecte en els casos en què s'aplica una bestreta quan les transaccions del val no es compensen. |
| Administració i comptabilitat de projectes | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creació d'una estimació després de comptabilitzar una proposta de factura bloqueja la importació de línies de correcció al Project Operations. |
| Administració i comptabilitat de projectes | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No hauria de ser possible modificar un registre de fita totalment facturat. |
| Administració i comptabilitat de projectes | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quan s'utilitzen càrrecs automàtics, la factura de client entre empreses d'un full d'hores no es pot comptabilitzar i es mostra un missatge d'error. |
| Administració i comptabilitat de projectes | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | L'adreça d'un subproject no s'actualitza correctament. |
| Administració i comptabilitat de projectes | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | El preu de cost dels requisits d'elements s'actualitza amb el preu de compra de les comandes de compra consolidades. |
| Administració i comptabilitat de projectes | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | El cost comptabilitzat no és correcte després d'actualitzar el preu de compra i habilitar el paràmetre **Activa l'administració de canvis**. |
| Viatge i despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Totes les despeses de l'usuari es poden veure en cercar una categoria a l'aplicació mòbil de despesa. |
| Viatge i despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Els imports incorrectes de les transaccions de proveïdors i d'impostos de la venda es comptabilitzen des d'una despesa creada a partir d'una transacció de targeta de crèdit. |
| Viatge i despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Quan actualitzeu la pàgina d'informe de despeses, es mostra un missatge d'advertiment irrellevant. |
| Viatge i despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | S'utilitza l'aprovador temporal erroni quan suprimiu un aprovador temporal i, a continuació, el torneu a enviar a través del flux de treball. |
| Viatge i despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es produeix un error de comptabilització relacionat amb la configuració del quilometratge. |
| Viatge i despesa | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribució no actualitza l'entitat legal quan es torna a afegir una transacció no adjunta a l'informe de despeses en una despesa entre empreses. |

### <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reglamentàries de les aplicacions de finances i operacions, vegeu [Actualitzacions reglamentàries](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar la sessió al Microsoft Dynamics Lifecycle Services (LCS) i utilitzar l'eina de cerca de problemes per visualitzar les actualitzacions normatives planificades. La cerca de problemes us permet cercar per país o regió, tipus de funció i llançament.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
