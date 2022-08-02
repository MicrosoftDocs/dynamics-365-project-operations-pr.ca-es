---
title: Novetats o canvis en operacions de projecte, setembre de 2021 per a escenaris basats en la producció o en estoc
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de setembre de 2021 de Project Operations per a escenaris basats en estoc o producció.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: be0f397df4a3e1973e1f5546e43b2cf9578950a0
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029840"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis en operacions de projecte, setembre de 2021 per a escenaris basats en la producció o en estoc

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.21
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|---|---|---|
| Administració i comptabilitat de projectes | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Si la funció de gestor de compres té accés a una persona jurídica, també té accés a tots els projectes de totes les persones jurídiques. |
| Administració i comptabilitat de projectes | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Es produeix un problema d'arrodoniment de l'impost sobre el valor afegit (IVA) mentre es liquida una nota de crèdit contra una factura original del projecte. |
| Administració i comptabilitat de projectes | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilitzeu un pressupost alternatiu del projecte per a la verificació del pressupost. |
| Administració i comptabilitat de projectes | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | El **grup de preus hora del preu de** venda no es calcula a l'estructura del desglossament del treball per a les ofertes del projecte. |
| Administració i comptabilitat de projectes | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | L'eliminació de l'estimació falla quan la moneda del contracte Habilita el **projecte per a la funció de càlcul** d'estimacions està habilitada. |
| Administració i comptabilitat de projectes | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La factorització de l'impost sobre les vendes per quantitat s'afegeix a l'import del preu de venda quan s'utilitza l'impost d'ús al grup de l'impost sobre les vendes del diari de despeses del projecte. |
| Administració i comptabilitat de projectes | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | L'impost condicional no es calcula correctament per a l'últim pagament quan s'apliquen la retenció i el pagament per avançat del proveïdor a les factures de comandes de compra. |
| Administració i comptabilitat de projectes | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | La traça d'ajust no funciona per als diaris d'equilibri inicial. |
| Administració i comptabilitat de projectes | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **L'assignació de revisió del pressupost del projecte per períodes** es divideix en tots els períodes pressupostaris. Quan s'envia l'assignació, el registre no s'esborra. |
| Administració i comptabilitat de projectes | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Les publicacions de treball en procés (WIP) al llibre major general tenen una quantitat incorrecta. |
| Administració i comptabilitat de projectes | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | L'aprovació del diari d'hores del projecte no funciona. |
| Administració i comptabilitat de projectes | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | El preu de venda de l'ajust del projecte no s'actualitza amb els costos indirectes quan no es marca el límit de finançament. |
| Administració i comptabilitat de projectes | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | No es pot crear un requisit d'element quan es factura la capçalera de la taula Sales i s'ha finalitzat l'ordre de compra de còpia de seguretat de les línies existents. |
| Administració i comptabilitat de projectes | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | L'import de retenció d'una regla de facturació que té una fita per a un projecte diferent no es publica a l'identificador de projecte corresponent que s'ha seleccionat per a la fita. En canvi, es publica amb el primer projecte. |
| Administració i comptabilitat de projectes | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quan seleccioneu **Dimensió financera definida** en una proposta de factura, es produeix l'error següent: "No es pot emetre l'objecte del tipus Dynamics".AX Application.FormIntControl' per escriure 'Dynamics.AX. Application.FormStringControl'." |
| Administració i comptabilitat de projectes | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | L'informe **de factures** del projecte omet línies. |
| Administració i comptabilitat de projectes | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Es produeix un error en calcular el control de costos d'un projecte d'inversió. |
| Administració i comptabilitat de projectes | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | El **mètode ProjTable:: InitFromCustTable - canDeletePostalAddress** causa un problema de rendiment. |
| Administració i comptabilitat de projectes | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | El missatge d'error ha de ser més clar que "Error inesperat". |
| Administració i comptabilitat de projectes | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | La factura del projecte publica els processos de treball per lots i publica la proposta de factura encara que no s'hagin generat les línies de factura. |
| Administració i comptabilitat de projectes | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Un problema d'arrodoniment es produeix quan la clau de configuració de llicències del sector públic està desactivada. Es genera un cost o un preu de venda incorrectes a les hores del full d'hores dels contractes que tenen diverses fonts fundadores. |
| Administració i comptabilitat de projectes | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | El preu de venda del projecte en una comanda de compra de projecte facturada es calcula incorrectament quan el model de preu de venda és **ràtio de contribució**. |
| Administració i comptabilitat de projectes | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | El sistema no considera els dies actius entremig quan calcula la taxa efectiva de treball per a un empleat. |
| Administració i comptabilitat de projectes | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Es produeix un error de publicació al full d'hores entre empreses a causa del següent error de validació: "Cap soci comercial està configurat per a una persona jurídica". |
| Administració i comptabilitat de projectes | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La descripció d'una ordre de compra que té una categoria de despesa no es recupera a la llista de transaccions de projecte publicades. |
| Administració i comptabilitat de projectes | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hi ha una conversió incorrecta a les revistes d'elements que es publiquen a un projecte. |
| Administració i comptabilitat de projectes | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Pots confirmar una ordre de compra encara que s'hagi superat el límit de finançament. |
| Administració i comptabilitat de projectes | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La **secció Correcció/Cancel·lació de factura** d'una factura de text lliure desapareix quan se selecciona un identificador de projecte. |
| Administració i comptabilitat de projectes | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hi ha problemes de rendiment quan es publica una proposta de factura de projecte a partir d'una comanda de venda del projecte que inclou un article emmagatzemat. |
| Administració i comptabilitat de projectes | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Les factures de compra del projecte no es poden publicar perquè es produeix l'error següent: "La funció AccDistProcessorProjectExtension.createForProjectRevenueLine s'ha anomenat incorrectament". |
| Administració i comptabilitat de projectes | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualització per a la creació de treballs per lots d'estimació de projectes per donar suport a l'execució de múltiples subtasques. |
| Administració i comptabilitat de projectes | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | L'estat d'un full d'hores no es pot actualitzar a **Esborrany** quan el flux de treball està bloquejat en un **estat cancel·lat**. |
| Administració i comptabilitat de projectes | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Els imports de retenció no es calculen a la proposta de factura de la nota d'abonament si hi ha diverses línies. |
| Administració i comptabilitat de projectes | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Quan intenteu canviar l'import d'una factura generada a partir d'una ordre de compra, es produeix l'error següent: "Les transaccions en val no s'equilibren segons XX/XX/XXXX. (moneda comptable: 0.00 - moneda d'informes: 0.01)." |
| Administració i comptabilitat de projectes | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Hi ha un problema de rendiment quan una proposta de factura del projecte es publica en mode lot, a causa de la unió amb **GeneralJournalAccountEntry**. |
| Administració i comptabilitat de projectes | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hi ha problemes de rendiment quan es publica un full d'hores. |
| Administració i comptabilitat de projectes | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La jerarquia d'estimacions de costos de l'estructura del desglossament del treball no s'alinea correctament després d'ampliar totes les tasques o després d'ampliar manualment una sola tasca. |
| Administració i comptabilitat de projectes | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | La plantilla de cotització del projecte de l'Excel no es pot afegir al menú Obre a l'Excel **·**. |
| Administració i comptabilitat de projectes | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | El número exempt d'impostos d'una persona jurídica no s'inclou a la factura impresa del projecte. |
| Administració i comptabilitat de projectes | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | No s'actualitzen dades financeres a l'error de la unitat d'inventari quan s'ajusta un projecte en relació amb les línies de crèdit. |
| Administració i comptabilitat de projectes | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Després d'aplicar KB 461935, no podeu publicar estimacions si canvieu a seqüències de números continus. |
| Administració i comptabilitat de projectes | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** fa que l'aplicació mòbil del full d'hores Android del projecte deixi de respondre. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor invertit per WIP d'una publicació de factures difereix del valor WIP publicat originalment de l'entrada de l'hora. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | En els casos de retenció aplicats, les transaccions d'un val no s'equilibren quan es publiquen els ingressos facturats d'un projecte. |
| Administració i comptabilitat de projectes | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quan la característica de millora **del** rendiment de planificació de recursos del projecte està habilitada, els valors decimals s'arrodoneixen incorrectament per a la disponibilitat i la capacitat dels recursos. |
| Administració i comptabilitat de projectes | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quan la funció Crea estimacions de projecte mitjançant diverses tasques **per lots està habilitada, la** creació d'estimacions en un lot que té diverses subtasques només funciona per al període actual. |
| Viatge i despesa | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | S'ignora una política de requisició de viatges i s'aprova el flux de treball sense errors. |
| Viatge i despesa | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>L'aplicació Despesa mòbil no desa la informació següent a la línia de despeses:</p><ul><li>L'identificador del projecte</li><li>Si la despesa és facturable</li><li>El número d'activitat</li></ul> |
| Viatge i despesa | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | El **camp Rebuts adjunts** està definit com a **Sí** encara que no s'adjunti cap rebut a la línia de despeses. |
| Viatge i despesa | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Es produeix un error quan canvieu la categoria de despeses a **Personal**. |
| Viatge i despesa | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | No podeu adjuntar un rebut i editar la despesa principal després que una transacció amb targeta de crèdit es divideixi en una despesa personal. |
| Viatge i despesa | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | La política de despeses per a transaccions entre empreses que tenen un identificador de projecte no funciona correctament. |
| Viatge i despesa | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta la informació de la data publicada per als informes de despeses publicats. |
| Viatge i despesa | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Hi ha problemes amb la forma de pagament a l'aplicació mòbil Expense. |
| Viatge i despesa | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Una sol·licitud de viatge que es crea per a un treballador es pot utilitzar per a l'informe de despeses d'un altre treballador abans de la data del delegat. |
| Viatge i despesa | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quan creeu una despesa, els canvis en els valors de la dimensió financera no s'actualitzen correctament al nivell de distribució comptable a l'espai **de treball Gestió** de despeses. |
| Viatge i despesa | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | L'estat d'aprovació de la línia de despeses principal no se sincronitza amb l'estat d'aprovació del flux de treball de línia desglossat. |
| Viatge i despesa | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Es produeix un error si publiqueu un informe de despeses i la recuperació d'impostos està activada. |
| Viatge i despesa | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegat no pot suprimir documents de despeses per a un empleat finalitzat. |
| Viatge i despesa | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | La supressió d'una línia de despeses triga més del previst i afecta el rendiment. |
| Viatge i despesa | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** causa un registre taxuncommitted **orfe**, perquè només **se suprimeix SourceDocumentLine**. |
| Viatge i despesa | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** no respecta **trvExpTrans.ReferenceDataAreaId** per crear la nova seqüència numèrica. |

## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions de finances i operacions, vegeu [Actualitzacions normatives](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió a Microsoft Dynamics Lifecycle Services (LCS) i utilitzar l'eina de cerca de problemes per veure les actualitzacions normatives previstes. La cerca de problemes us permet cercar per país o regió, tipus de característica i versió.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
