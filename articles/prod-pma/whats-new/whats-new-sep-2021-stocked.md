---
title: Novetats o canvis en operacions de projectes, setembre de 2021 per a escenaris basats en la producció
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles al llançament de setembre de 2021 d'Operacions de projecte per a escenaris emmagatzemats / basats en la producció.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: andchoi
ms.openlocfilehash: 7016d702719b2d432ec929aaca8d609ebf6e996b
ms.sourcegitcommit: abdd6cb3461ebb12fd2ca7ea78439c29aecd0a94
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/16/2021
ms.locfileid: "7815819"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis en operacions de projectes, setembre de 2021 per a escenaris basats en la producció

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest tema s'aplica als components i versions següents del Microsoft Dynamics 365 Project Operations:

- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.21
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|---|---|---|
| Administració i comptabilitat de projectes | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Si la funció de gestor de compres té accés a una persona jurídica, també accedeix a tots els projectes de totes les persones jurídiques. |
| Administració i comptabilitat de projectes | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Es produeix una arrodoniment de l'impost sobre el valor afegit (IVA) mentre es liquida una nota de crèdit amb una factura original del projecte. |
| Administració i comptabilitat de projectes | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilitzeu un pressupost alternatiu del projecte per a la verificació del pressupost. |
| Administració i comptabilitat de projectes | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | El **grup de preus de venda per hora no es calcula a** l'estructura de desglossament del treball per a les cotitzacions del projecte. |
| Administració i comptabilitat de projectes | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | L'eliminació de l'estimació falla quan la moneda del **contracte Habilita per al projecte per a la característica de càlcul** d'estimacions està habilitada. |
| Administració i comptabilitat de projectes | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La factorització de l'impost sobre les vendes per quantitat s'afegeix a l'import del preu de venda quan s'utilitza l'impost d'ús al grup d'impostos sobre les vendes del diari de despeses del projecte. |
| Administració i comptabilitat de projectes | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | L'impost condicional no es calcula correctament per a l'últim pagament quan s'aplica la retenció i el pagament per avançat del proveïdor a les factures de comandes de compra. |
| Administració i comptabilitat de projectes | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | La traça d'ajust no funciona per a les revistes de balanç inicial. |
| Administració i comptabilitat de projectes | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **L'assignació de revisió del pressupost del projecte per període** es divideix en tots els períodes pressupostaris. Quan s'envia l'assignació, el registre no s'esborra. |
| Administració i comptabilitat de projectes | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Les publicacions de treball en procés (WIP) al llibre major general tenen una quantitat incorrecta. |
| Administració i comptabilitat de projectes | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | L'aprovació del diari de l'hora del projecte no funciona. |
| Administració i comptabilitat de projectes | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | El preu de venda d'ajust del projecte no s'actualitza amb els costos indirectes quan el límit de finançament no està marcat. |
| Administració i comptabilitat de projectes | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | No es pot crear un requisit d'element quan es factura la capçalera de la taula Sales i s'ha finalitzat l'ordre de compra de còpia de suport de les línies existents. |
| Administració i comptabilitat de projectes | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | L'import de retenció d'una regla de facturació que té una fita per a un projecte diferent no es publica a l'identificador del projecte corresponent que s'ha seleccionat per a la fita. En lloc d'això, es publica amb el primer projecte. |
| Administració i comptabilitat de projectes | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quan seleccioneu **Dimensió financera establerta en una proposta de** factura, es produeix l'error següent: "No es pot emetre l'objecte del tipus 'Dynamics.AX. Application.FormIntControl" per escriure "Dynamics.AX. Application.FormStringControl'." |
| Administració i comptabilitat de projectes | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | **L'informe de factures del projecte** omet les línies. |
| Administració i comptabilitat de projectes | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Es produeix un error quan es calcula el control de costos d'un projecte d'inversió. |
| Administració i comptabilitat de projectes | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | El **mètode ProjTable::InitFromCustTable - canDeletePostalAddress** provoca un problema de rendiment. |
| Administració i comptabilitat de projectes | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | El missatge d'error ha de ser més clar que "Error inesperat". |
| Administració i comptabilitat de projectes | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | La factura del projecte publica els processos de treball per lots i publica la proposta de factura encara que no s'hagin generat les línies de factura. |
| Administració i comptabilitat de projectes | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Un problema d'arrodoniment es produeix quan la clau de configuració de llicències del sector públic està desactivada. Es genera un cost incorrecte o un preu de venda en les hores de full de temps dels contractes que tenen múltiples fonts fundacionals. |
| Administració i comptabilitat de projectes | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | El preu de venda del projecte en una comanda de compra del projecte facturat es calcula incorrectament quan el model de preu de venda és **relació de contribució**. |
| Administració i comptabilitat de projectes | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | El sistema no té en compte els dies actius entremig quan calcula la taxa de treball efectiva per a un empleat. |
| Administració i comptabilitat de projectes | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Es produeix un error de publicació al full d'hores interempresa a causa del següent error de validació: "No hi ha cap soci comercial configurat per a una persona jurídica". |
| Administració i comptabilitat de projectes | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La descripció d'una ordre de compra que té una categoria de despeses no es recupera a la llista de transaccions del projecte publicat. |
| Administració i comptabilitat de projectes | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hi ha una conversió incorrecta a les revistes d'elements que es publiquen a un projecte. |
| Administració i comptabilitat de projectes | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Pots confirmar una comanda de compra encara que s'hagi superat el límit de finançament. |
| Administració i comptabilitat de projectes | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La **secció Correcció/Cancel·la la factura** d'una factura de text lliure desapareix quan se selecciona un identificador de projecte. |
| Administració i comptabilitat de projectes | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hi ha problemes de rendiment quan es publica una proposta de factura del projecte des d'una ordre de venda de projectes que inclou un element emmagatzemat. |
| Administració i comptabilitat de projectes | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Les factures de compra del projecte no es poden publicar perquè s'ha produït l'error següent: "La funció AccDistProcessorProjectExtension.createForProjectRevenueLine s'ha cridat incorrectament". |
| Administració i comptabilitat de projectes | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualització a la creació de treballs per lots d'estimació de projectes per donar suport a l'execució de diverses subtasques. |
| Administració i comptabilitat de projectes | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | L'estat d'un full d'hores no es pot actualitzar a **Esborrany quan el flux de treball està** encallat en un **estat** cancel·lat. |
| Administració i comptabilitat de projectes | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Els imports de retenció no es calculen a la proposta de factura de la nota de crèdit si hi ha diverses línies. |
| Administració i comptabilitat de projectes | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Quan intentes canviar l'import d'una factura generada a partir d'una comanda de compra, es produeix l'error següent: "Les transaccions del bo no s'equilibren segons XX/XX/XXXX. (moneda comptable: 0.00 - moneda d'informes: 0.01)." |
| Administració i comptabilitat de projectes | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Hi ha un problema de rendiment quan es publica una proposta de factura del projecte en mode per lots, a causa de la unió amb **GeneralJournalAccountEntry**. |
| Administració i comptabilitat de projectes | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hi ha problemes de rendiment quan es publica un full d'hores. |
| Administració i comptabilitat de projectes | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La jerarquia d'estimacions de costos de l'estructura de desglossament del treball no s'alinea correctament després d'expandir totes les tasques o després d'expandir manualment una sola tasca. |
| Administració i comptabilitat de projectes | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | La plantilla de cotització del projecte de l'Excel no es pot afegir al **menú Obre a l'Excel.** |
| Administració i comptabilitat de projectes | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | El número exempt d'impostos d'una persona jurídica no s'inclou a la factura impresa del projecte. |
| Administració i comptabilitat de projectes | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | No s'actualitzen dades financeres a l'error de la unitat d'inventari quan s'ajusta un projecte en relació amb les línies de crèdit. |
| Administració i comptabilitat de projectes | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Després d'aplicar kb 461935, no podeu publicar estimacions si canvieu a seqüències de nombres continus. |
| Administració i comptabilitat de projectes | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** fa que l'aplicació mòbil del full de temps del projecte per a Android deixi de respondre. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertit per WIP d'una publicació de factura difereix del valor WIP publicat originalment des de l'entrada de l'hora. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | En els casos de retenció aplicats, les transaccions d'un val no es equilibren quan es publiquen els ingressos facturats d'un projecte. |
| Administració i comptabilitat de projectes | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quan la **característica de millora del rendiment de planificació de recursos del projecte està** habilitada, els valors decimals s'arrodoneixen incorrectament per a la disponibilitat i la capacitat dels recursos. |
| Administració i comptabilitat de projectes | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quan s'habilita la **funció Crea estimacions del projecte mitjançant diverses tasques per** lots, la creació d'estimacions en un lot que té diverses subtasques només funciona per al període actual. |
| Viatge i despesa | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | S'ignora una política de requisa de viatges i s'aprova el flux de treball sense errors. |
| Viatge i despesa | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>L'aplicació Despesa mòbil no guarda la informació següent a la línia de despeses:</p><ul><li>L'identificador del projecte</li><li>Si la despesa és facturable</li><li>El número d'activitat</li></ul> |
| Viatge i despesa | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | El **camp rebuts adjunts** s'estableix a **Sí encara que no** s'adjunti cap rebut a la línia de despeses. |
| Viatge i despesa | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Es produeix un error quan canvieu la categoria de despesa a **Personal**. |
| Viatge i despesa | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | No podeu adjuntar un rebut i editar la despesa principal després que una transacció amb targeta de crèdit es divideixi en una despesa personal. |
| Viatge i despesa | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | La política de despeses per a operacions interempresasables que tinguin un identificador de projecte no funciona correctament. |
| Viatge i despesa | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta la informació de la data publicada per als informes de despeses publicats. |
| Viatge i despesa | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Hi ha problemes amb la forma de pagament a l'aplicació mòbil Expense. |
| Viatge i despesa | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Una sol·licitud de viatge que es crea per a un treballador es pot utilitzar per a l'informe de despeses d'un altre treballador abans de la data del delegat. |
| Viatge i despesa | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quan creeu una despesa, els canvis en els valors de les dimensions financeres no s'actualitzen correctament al nivell de distribució comptable de **l'àrea de treball Gestió de** despeses. |
| Viatge i despesa | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | L'estat d'aprovació de la línia de despeses principal no se sincronitza amb l'estat d'aprovació del flux de treball de línia desglossat. |
| Viatge i despesa | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Es produeix un error si publiqueu un informe de despeses i s'habilita la recuperació d'impostos. |
| Viatge i despesa | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegat no pot suprimir documents de despeses per a un empleat finalitzat. |
| Viatge i despesa | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | L'eliminació d'una línia de despeses triga més del que s'esperava i afecta el rendiment. |
| Viatge i despesa | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoca un registre **d'Impostos no oficial** orfe, perquè només se suprimeix **SourceDocumentLine.** |
| Viatge i despesa | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId() no** **respecta trvExpTrans.ReferenceDataAreaId** per crear la nova seqüència numèrica. |

## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions financeres i d'operacions, vegeu [Actualitzacions reguladores](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió a Microsoft Dynamics Serveis de cicle de vida (LCS) i utilitzar l'eina de cerca d'incidències per veure les actualitzacions reguladores previstes. La cerca d'incidències us permet cercar per país o regió, tipus de característica i publicar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
