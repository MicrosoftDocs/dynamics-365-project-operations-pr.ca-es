---
title: Novetats o canvis a Project Operations, octubre de 2021 per a escenaris basats en la producció
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió d'octubre de 2021 de Project Operations per a escenaris emmagatzemats / basats en la producció.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 449cab5880c29cf110c9c5a266cbb4b102b5fc83
ms.sourcegitcommit: 2e4483d5b88213a9f33109f7adb989108521327d
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2021
ms.locfileid: "7818315"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis a Project Operations, octubre de 2021 per a escenaris basats en la producció

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest tema s'aplica als components i versions següents del Microsoft Dynamics 365 Project Operations:

- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.22
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|--------------|------------------|----------------|
| Administració i comptabilitat de projectes | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Els treballs en procés (WIP) i els imports d'ingressos acumulats no s'inverteixen correctament quan es publica una factura de client interempresativa. |
| Administració i comptabilitat de projectes | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | Evita **el tancament del projecte si hi ha transaccions obertes la funcionalitat no** funciona. |
| Administració i comptabilitat de projectes | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La classificació de facturació d'una factura de text lliure no emplena automàticament les dimensions dels projectes quan aquesta funcionalitat està habilitada. |
| Administració i comptabilitat de projectes | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | En els escenaris no interempresataris, els imports d'ingressos no acumulats i WIP no s'inverteixen correctament quan es publica la factura del projecte. |
| Administració i comptabilitat de projectes | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Els valors de dèbit i crèdit es canvien quan s'utilitza el complement Microsoft Excel amb el diari de despeses del projecte i el **camp Tipus de compte offset està definit com a Projecte** **·**. |
| Administració i comptabilitat de projectes | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | L'import que es publica a les transaccions del projecte està sobreestimat en una ordre de compra del projecte que inclou articles emmagatzemats i que té imports fiscals no deduïbles quan **es marca UseTax.** |
| Administració i comptabilitat de projectes | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | El sistema divideix l'import entre els informes de beneficis i pèrdues del projecte i els informes wip del projecte. |
| Administració i comptabilitat de projectes | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | L'inventari a mà és incorrecte després d'ajustar un requisit d'article parcialment retornat. |
| Administració i comptabilitat de projectes | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Els noms dels recursos es dupliquen a les operacions del projecte quan s'editen al Microsoft Project. |
| Administració i comptabilitat de projectes | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Els informes de despeses d'interempresa que tenen comptes interempresables pendents dels costos de factures del proveïdor es publiquen primer al **tipus de publicació de costos del projecte WIP.** No obstant això, durant el processament, els costos relacionats amb l'estimació es publiquen al **tipus de publicació de costos del projecte en lloc del tipus de publicació de costos** **Intercompany** esperat. |
| Administració i comptabilitat de projectes | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | No es mostren els resultats de retenció del proveïdor en les transaccions de despeses del projecte. |
| Administració i comptabilitat de projectes | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | El full de temps ha d'arrodonir l'import de la transacció en la moneda de transacció a un nombre especificat de posicions decimals en totes les distribucions comptables i entrades generals d'assignació de diaris. |
| Administració i comptabilitat de projectes | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Les quantitats dels requisits de l'element del projecte s'actualitzen automàticament quan es readven les comandes previstes. |
| Administració i comptabilitat de projectes | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | El número de val, el saldo del proveïdor del tipus de transacció i el número de compte no es poden invertir a la factura de pagament per avançat d'una ordre de compra. |
| Administració i comptabilitat de projectes | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La factura del proveïdor d'interempresa es trenca quan s'activa la integració de factures del proveïdor. |
| Administració i comptabilitat de projectes | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Quan creeu un diari de despeses del projecte, l'import del cost es mostra al **camp** Crèdit. |
| Administració i comptabilitat de projectes | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les condicions de pagament de les factures del projecte no funcionen com s'esperava. |
| Administració i comptabilitat de projectes | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Els vals del full d'hores es poden reutilitzar quan la seqüència numèrica es configura com a contínua. |
| Administració i comptabilitat de projectes | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANÇA: la **lògica de l'import de retenció manual** no coincideix amb la lògica **d'import de retenció automàtica** de la proposta de factura del contracte del projecte. |
| Administració i comptabilitat de projectes | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Quan es publica la retenció del proveïdor, la publicació del val té línies addicionals incorrectes. |
| Administració i comptabilitat de projectes | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quan es canvia el **camp Data de la factura de la pàgina Crea una proposta de** **factura**, es pot produir l'error següent: "Referència de l'objecte que no s'estableix en una instància d'un objecte". |
| Administració i comptabilitat de projectes | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Es produeix un error quan intenteu aprovar un full d'hores del flux de **treball TSLine i hi ha una política de** full d'hores per a dissabte i diumenge. |
| Administració i comptabilitat de projectes | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | El tipus d'element del projecte de saldo inicial s'exclou dels resums de **l'operació de la proposta de factura quan es calcula el total de la factura de la proposta** de factura. |
| Administració i comptabilitat de projectes | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Si el cost de consum en un ordre de producció d'un projecte és 0 (zero), es produeix el següent error quan intenteu estimar: "S'ha intentat dividir per zero". |
| Administració i comptabilitat de projectes | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | L'aplicació Project Timesheet Mobile per a Android deixa de respondre. El problema està relacionat amb **TimeEntryDataManager ArgumentNullException**. |
| Administració i comptabilitat de projectes | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | El diari d'integració d'operacions del projecte falla quan el publiqueu perquè falta un compte de dimensions. Tanmateix, el compte que falta a les dimensions no és el compte al que publiqueu. |
| Administració i comptabilitat de projectes | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | El **filtre ToDate** a les cerques no s'esborra quan s'elimina del quadre de diàleg Selecciona a la pàgina De cost **de** **l'entrada.** |
| Administració i comptabilitat de projectes | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Reinicialitza tota la distribució** falla i mostra un error per als fulls d'hores que es creen per a un projecte del tipus només **Hora**. |
| Administració i comptabilitat de projectes | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | La **pestanya** Projecte no es pot editar en una factura pendent del proveïdor quan la categoria d'adquisició s'assigna a l'element. |
| Administració i comptabilitat de projectes | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Falta la subfinestra de navegació si no heu iniciat la sessió al project Operations Dataverse. |
| Administració i comptabilitat de projectes | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Per a les operacions d'ajust de projectes interempresaents, hi ha problemes a l'empresa de destinació. |
| Administració i comptabilitat de projectes | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Els costos compromesos per a un projecte calculen la quantitat i el preu de cost incorrectes si l'ordre de compra es va processar mitjançant **el procés de final d'any de l'ordre de compra al llibre major** general. |
| Administració i comptabilitat de projectes | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Quan una ordre de producció del projecte que té comandes de qualitat s'informa com a finalitzada, es produeix l'error següent: "No hi ha cap transacció virtual marcada amb la transacció d'inventari". |
| Administració i comptabilitat de projectes | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Quan es publica una factura a pagar comptes relacionada amb el projecte, es produeix l'error següent: "Projecte de text enumerat - cost - element no existeix". |
| Administració i comptabilitat de projectes | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Els costos indirectes es dupliquen quan acumuleu manualment els ingressos. |
| Administració i comptabilitat de projectes | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | Acumular ingressos i publicar WIP no produeix transaccions. |
| Administració i comptabilitat de projectes | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | L'activació del preu pendent falla per a un element de cost estàndard quan hi ha una ordre de compra del projecte rebut. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertit per WIP d'una publicació de factura difereix del valor WIP publicat original d'una entrada de temps. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Hi ha un problema de publicació per als ingressos facturats pel projecte en casos de retenció aplicats en què les transaccions del val no es equilibren. |
| Administració i comptabilitat de projectes | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La creació d'una estimació després de publicar una proposta de factura bloqueja la importació de línies de correcció a Les operacions del projecte. |
| Administració i comptabilitat de projectes | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | No hauria de ser possible la modificació d'un registre de fita totalment facturat. |
| Administració i comptabilitat de projectes | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Quan s'utilitzen càrrecs automàtics, no es pot publicar la factura del client entremeses per a un full de temps i es mostra un missatge d'error. |
| Administració i comptabilitat de projectes | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | L'adreça d'un subprojecte no s'ha actualitzat correctament. |
| Administració i comptabilitat de projectes | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | El preu de cost dels requisits de l'article s'actualitza amb el preu de compra de les comandes de compra consolidades. |
| Administració i comptabilitat de projectes | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | El cost publicat no és correcte després d'actualitzar el preu de compra i activar el paràmetre **Activa la gestió del canvi està** habilitat. |
| Viatge i despesa | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Totes les despeses de l'usuari es poden veure quan cerqueu una categoria a l'aplicació mòbil Expense. |
| Viatge i despesa | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Els imports incorrectes en les transaccions del proveïdor i les transaccions d'impostos sobre les vendes es publiquen a partir d'una despesa que s'ha creat a partir d'una transacció amb targeta de crèdit. |
| Viatge i despesa | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Es mostra un missatge d'advertiment irrellevant quan actualitzeu les pàgines de l'informe de despeses. |
| Viatge i despesa | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | L'aprovador provisional incorrecte s'utilitza quan suprimiu un aprovador provisional i torneu a enviar-lo a través del flux de treball. |
| Viatge i despesa | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Es produeix un error de publicació relacionat amb la configuració del quilometratge. |
| Viatge i despesa | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribució no actualitza la persona jurídica quan es torna a afegir una transacció no adjunta a l'informe de despeses sobre una despesa interempresativa. |

### <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions financeres i d'operacions, vegeu [Actualitzacions reguladores](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió a Microsoft Dynamics Serveis de cicle de vida (LCS) i utilitzar l'eina de cerca d'incidències per veure les actualitzacions reguladores previstes. La cerca d'incidències us permet cercar per país o regió, tipus de característica i publicar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
