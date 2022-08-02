---
title: Novetats o canvis a Project Operations (octubre de 2021) per a escenaris basats en la producció o en estoc
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'octubre de 2021 d'Operacions del projecte per a escenaris basats en estoc o en producció.
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
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis a Project Operations (octubre de 2021) per a escenaris basats en la producció o en estoc

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.22
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|--------------|------------------|----------------|
| Administració i comptabilitat de projectes | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Els imports de treball en procés (WIP) i els imports d'ingressos acumulats no es reverteixen correctament quan es publica una factura de client entre empreses. |
| Administració i comptabilitat de projectes | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | La **funcionalitat Evita el tancament del projecte si hi ha transaccions obertes** no funciona. |
| Administració i comptabilitat de projectes | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La classificació de facturació d'una factura de text lliure no emplena automàticament les dimensions dels projectes quan aquesta funcionalitat està habilitada. |
| Administració i comptabilitat de projectes | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En escenaris que no siguin empreses, wip i imports d'ingressos acumulats no s'inverteixen correctament quan es publica la factura del projecte. |
| Administració i comptabilitat de projectes | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Els valors de dèbit i crèdit es canvien quan el complement s'utilitza Microsoft Excel amb el diari de despeses del projecte i el **camp Tipus de** compte Offset es defineix com a **Projecte**. |
| Administració i comptabilitat de projectes | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | L'import que es comptabilitza a les transaccions del projecte s'exagera en una ordre de compra del projecte que inclou articles emmagatzemats i que té imports fiscals no deduïbles quan **es marca UseTax**. |
| Administració i comptabilitat de projectes | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | El sistema divideix l'import entre els informes de pèrdues i guanys del projecte i els informes WIP del projecte. |
| Administració i comptabilitat de projectes | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | L'inventari a mà no és correcte després d'ajustar un requisit d'article parcialment retornat. |
| Administració i comptabilitat de projectes | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Els noms dels recursos es dupliquen al Project Operations quan s'editen al Microsoft Project. |
| Administració i comptabilitat de projectes | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Els informes de despeses entre empreses que tenen comptes a pagar entre empreses pendents de costos de factures de proveïdors es publiquen primer al **tipus de publicació de costos** del projecte WIP. Tanmateix, durant el processament, els costos relacionats amb l'estimació es publiquen al **tipus de publicació de costos** del projecte en lloc del tipus de publicació de costos **interempresarials esperat**. |
| Administració i comptabilitat de projectes | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Els resultats de retenció de proveïdors en les transaccions de despeses del projecte no es mostren. |
| Administració i comptabilitat de projectes | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | El full d'hores ha d'arrodonir l'import de la transacció en la moneda de transacció a un nombre determinat de decimals en totes les distribucions comptables i assentaments generals d'assignació de diaris. |
| Administració i comptabilitat de projectes | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Les quantitats de requisits dels elements del projecte s'actualitzen automàticament quan es reafirmen les comandes previstes. |
| Administració i comptabilitat de projectes | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | El número de val, el saldo del proveïdor tipus de transacció i el número de compte no es poden revertir a la factura de prepagament d'una comanda de compra. |
| Administració i comptabilitat de projectes | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveïdor entre empreses es trenca quan s'activa la integració de factures del proveïdor. |
| Administració i comptabilitat de projectes | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quan creeu un diari de despeses del projecte, l'import del cost es mostra al **camp Crèdit**. |
| Administració i comptabilitat de projectes | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les condicions de pagament de les factures del projecte no funcionen com s'esperava. |
| Administració i comptabilitat de projectes | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Els vals de full d'hores es poden reutilitzar quan la seqüència de números es configura com a contínua. |
| Administració i comptabilitat de projectes | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANÇA: La lògica d'import **de** retenció manual no coincideix amb la lògica d'import **de** retenció automàtica de la proposta de factura del contracte del projecte. |
| Administració i comptabilitat de projectes | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quan s'allibera la retenció del proveïdor, la publicació del val té línies addicionals incorrectes. |
| Administració i comptabilitat de projectes | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quan es canvia el **camp Data** de factura de la **pàgina Crea una proposta** de factura, es pot produir l'error següent: "La referència de l'objecte no està definida en una instància d'un objecte". |
| Administració i comptabilitat de projectes | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Es produeix un error quan intenteu aprovar un full de temps del flux de treball de TSLine **i hi ha una política de** full d'hores per a dissabte i diumenge. |
| Administració i comptabilitat de projectes | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | El tipus d'element del projecte de saldo inicial s'exclou dels resums **de transacció de** proposta de factura quan es calcula el total de la factura de la proposta de factura. |
| Administració i comptabilitat de projectes | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Si el cost de consum d'una comanda de producció del projecte és 0 (zero), es produeix l'error següent quan intenteu estimar: "S'ha intentat dividir per zero". |
| Administració i comptabilitat de projectes | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | L'aplicació Project Timesheet Mobile per a Android les parades de resposta. El problema està relacionat **amb TimeEntryDataManager ArgumentNullException**. |
| Administració i comptabilitat de projectes | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | El diari d'integració del Project Operations falla quan el publiqueu, perquè a un compte li falten dimensions. Tanmateix, el compte que no té les dimensions no és el compte al qual publiqueu. |
| Administració i comptabilitat de projectes | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | El **filtre ToDate** a les cerques no s'esborra quan se suprimeix del quadre de diàleg Selecciona **de la** pàgina Cost **d'entrada**. |
| Administració i comptabilitat de projectes | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Restableix tots els errors de distribució** i mostra un error per als fulls d'hores que es creen per a un projecte del **tipus Només** hora. |
| Administració i comptabilitat de projectes | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La **pestanya Projecte** no es pot editar en una factura pendent del proveïdor quan s'assigna la categoria de contractació a l'element. |
| Administració i comptabilitat de projectes | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta la subfinestra de navegació si no heu iniciat la sessió al Project Operations Dataverse. |
| Administració i comptabilitat de projectes | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Per a les transaccions d'ajust de projectes entre empreses, hi ha problemes a l'empresa de destinació. |
| Administració i comptabilitat de projectes | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Els costos compromesos d'un projecte calculen la quantitat i el preu de cost incorrectes si l'ordre de compra s'ha processat mitjançant **el procés** de final d'any de l'ordre de compra al llibre major general. |
| Administració i comptabilitat de projectes | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quan s'informa d'una ordre de producció del projecte que té comandes de qualitat com a finalitzades, es produeix l'error següent: "No hi ha cap transacció virtual marcada amb una transacció d'inventari". |
| Administració i comptabilitat de projectes | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quan es comptabilitza una factura a pagar de Comptes relacionats amb el projecte, es produeix l'error següent: "El text enumerat Projecte - cost - element no existeix". |
| Administració i comptabilitat de projectes | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Els costos indirectes es dupliquen quan acumuleu ingressos manualment. |
| Administració i comptabilitat de projectes | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Acumuleu ingressos i la publicació de WIP no produeix transaccions. |
| Administració i comptabilitat de projectes | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | L'activació del preu pendent falla per a un element de cost estàndard quan hi ha una ordre de compra de projecte rebuda. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertit per WIP d'una publicació de factura difereix del valor WIP publicat original d'una entrada de temps. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Hi ha un problema de comptabilització dels ingressos facturats pel projecte en els casos de retenció aplicats en què les transaccions del val no s'equilibren. |
| Administració i comptabilitat de projectes | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creació d'un pressupost després de la comptabilització d'una proposta de factura bloqueja la importació de línies de correcció en operacions de projecte. |
| Administració i comptabilitat de projectes | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No hauria de ser possible la modificació d'un registre de fites totalment facturades. |
| Administració i comptabilitat de projectes | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quan s'utilitzen càrrecs automàtics, no es pot publicar la factura entre empreses d'un full d'hores i es mostra un missatge d'error. |
| Administració i comptabilitat de projectes | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | L'adreça d'un subprojecte no s'actualitza correctament. |
| Administració i comptabilitat de projectes | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | El preu de cost dels requisits dels articles s'actualitza amb el preu de compra de les comandes de compra consolidades. |
| Administració i comptabilitat de projectes | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | El cost publicat no és correcte després d'actualitzar el preu de compra i habilitar el paràmetre **Activa la gestió de** canvis. |
| Viatge i despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Totes les despeses de l'usuari es poden veure quan cerqueu una categoria a l'aplicació mòbil Despesa. |
| Viatge i despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Els imports incorrectes de les transaccions de proveïdors i de les transaccions de l'impost sobre les vendes es publiquen a partir d'una despesa creada a partir d'una transacció amb targeta de crèdit. |
| Viatge i despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Es mostra un missatge d'advertència irrellevant quan actualitzeu les pàgines de l'informe de despeses. |
| Viatge i despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | L'aprovador provisional incorrecte s'utilitza quan suprimiu un aprovador provisional i, a continuació, torneu a enviar-lo mitjançant el flux de treball. |
| Viatge i despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es produeix un error de publicació relacionat amb la configuració del quilometratge. |
| Viatge i despesa | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribució no actualitza la persona jurídica quan es torna a afegir una transacció no ajustada a l'informe de despeses d'una despesa entre empreses. |

### <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions de finances i operacions, vegeu [Actualitzacions normatives](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió a Microsoft Dynamics Lifecycle Services (LCS) i utilitzar l'eina de cerca de problemes per veure les actualitzacions normatives previstes. La cerca de problemes us permet cercar per país o regió, tipus de característica i versió.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
