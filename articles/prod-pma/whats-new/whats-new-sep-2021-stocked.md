---
title: Novetats o canvis del setembre de 2021 a Project Operations per a escenaris basats en producció/mantinguts en existències
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de setembre de 2021 del Project Operations per a escenaris basats en producció/ mantinguts en existències.
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
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Novetats o canvis del setembre de 2021 a Project Operations per a escenaris basats en producció/mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.21
 
## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
|---|---|---|
| Administració i comptabilitat de projectes | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Si es dona la funció d'Administrador de compres a una entitat jurídica, també obté accés a tots els projectes de totes les entitats jurídiques. |
| Administració i comptabilitat de projectes | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Es produeix un problema d'arrodoniment de l'impost de valor afegit (IVA) en liquidar una factura original del projecte. |
| Administració i comptabilitat de projectes | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilitzeu un dipòsit de projectes alternatiu per a la verificació del dipòsit. |
| Administració i comptabilitat de projectes | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | El grup de preus **Preu de venda per hora** no es calcula a l'estructura del desglossament del treball per a les ofertes del projecte. |
| Administració i comptabilitat de projectes | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | L'eliminació de l'estimació falla quan la característica **Habilita la moneda del contracte del projecte per al càlcul d'estimacions** està habilitada. |
| Administració i comptabilitat de projectes | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La factorització de l'impost de vendes per quantitat s'afegeix a l'import del preu de venda quan s'utilitza l'impost de venda del grup d'impostos de vendes del llibre diari de despeses del projecte. |
| Administració i comptabilitat de projectes | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | L'impost condicional no es calcula correctament per a l'últim pagament quan s'aplica la retenció i el pagament previ del proveïdor a les factures de comanda de compra. |
| Administració i comptabilitat de projectes | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | El seguiment de l'ajustament no funciona per als llibres diari de balanç inicials. |
| Administració i comptabilitat de projectes | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | **La revisió del pressupost del projecte per període** es divideix en tots els períodes del pressupost. Quan s'envia l'assignació, el registre no s'esborra. |
| Administració i comptabilitat de projectes | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Les comptabilitzacions de treball en curs (WIP) al llibre major tenen una quantitat incorrecta. |
| Administració i comptabilitat de projectes | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | L'aprovació del diari d'hores del projecte no funciona. |
| Administració i comptabilitat de projectes | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | El preu de venda d'ajustament del projecte no s'actualitza amb els costos indirectes quan el límit de finançament es desmarca. |
| Administració i comptabilitat de projectes | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | No es pot crear un requisit d'element quan la capçalera de la taula Vendes està facturada i s'ha finalitzat l'ordre de compra de suport per a les línies existents. |
| Administració i comptabilitat de projectes | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | L'import de retenció d'una regla de facturació que té una fita d'un projecte diferent no està comptabilitzada en l'ID de projecte corresponent que s'ha seleccionat per a la fita. En lloc d'això, s'ha comptabilitzat amb el primer projecte. |
| Administració i comptabilitat de projectes | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Quan seleccioneu **Conjunt de dimensions financeres** en una proposta de factura, es produeix l'error següent: "No es pot convertir l'objecte de tipus 'Dynamics.AX.Application.FormIntControl' al tipus 'Dynamics.AX.Application.FormStringControl'." |
| Administració i comptabilitat de projectes | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | L'informe **Factura del projecte** omet línies. |
| Administració i comptabilitat de projectes | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Es produeix un error quan calculeu el control de cost d'un projecte d'inversió. |
| Administració i comptabilitat de projectes | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | El mètode **ProjTable::InitFromCustTable - canDeletePostalAddress** provoca un problema de rendiment. |
| Administració i comptabilitat de projectes | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | El missatge d'error hauria de ser més clar que "Error inesperat". |
| Administració i comptabilitat de projectes | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | El treball per lots de comptabilització de factures del projecte processa i comptabilitza la proposta de factura encara que les línies de la factura no s'hagin generat. |
| Administració i comptabilitat de projectes | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Es produeix un problema d'arrodoniment quan la clau de configuració de llicència del sector públic està desactivada. Es genera un cost o un preu de venda incorrecte en les hores del full d'hores per als contractes que tenen diverses fonts de finançament. |
| Administració i comptabilitat de projectes | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | El preu de venda del projecte en una comanda de compra de projecte facturat es calcula incorrectament quan el model de preu de venda és **Relació de contribució**. |
| Administració i comptabilitat de projectes | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | El sistema no té en compte els dies actius entremig quan calcula la taxa de treball efectiva per a un empleat. |
| Administració i comptabilitat de projectes | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | S'ha produït un error de comptabilització a la fulla d'hores entre empreses a causa del següent error de validació: "No hi ha cap proveïdor comercial configurat per a l'entitat jurídica". |
| Administració i comptabilitat de projectes | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La descripció d'una comanda de compra que té una categoria de despesa no es recupera a la llista de transaccions de projecte comptabilitzades. |
| Administració i comptabilitat de projectes | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Hi ha una conversió incorrecta als diaris d'articles que es comptabilitzen en un projecte. |
| Administració i comptabilitat de projectes | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Una comanda de compra es pot confirmar encara que s'hagi superat el límit de finançament. |
| Administració i comptabilitat de projectes | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La secció **Correcció/Cancel·la la factura** d'una factura de text lliure desapareix quan se selecciona un ID del projecte. |
| Administració i comptabilitat de projectes | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Hi ha problemes de rendiment quan una proposta de factura del projecte es comptabilitza des d'una comanda de vendes del projecte que inclou un article en existències. |
| Administració i comptabilitat de projectes | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Les factures de compra del projecte no es poden comptabilitzar perquè es produeix l'error següent: "S'ha cridat incorrectament la funció AccDistProcessorProjectExtension.createForProjectRevenueLine". |
| Administració i comptabilitat de projectes | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Actualitzeu a la creació de treballs per lots d'estimació del projecte per ajudar en l'execució de diverses subtasques. |
| Administració i comptabilitat de projectes | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | L'estat d'un full d'hores no es pot actualitzar a **Esborrany** quan el flux de treball està encallat en l'estat **Cancel·lat**. |
| Administració i comptabilitat de projectes | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Els imports de retenció no es calculen a la proposta de factura d'abonament si hi ha diverses línies. |
| Administració i comptabilitat de projectes | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Quan intenteu canviar l'import d'una factura generada a partir d'una comanda de compra, es produeix l'error següent: "Les transaccions del val no s'equilibren com el XX/XX/XXXX. (moneda comptable: 0.00 - moneda d'informes: 0.01)." |
| Administració i comptabilitat de projectes | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Hi ha un problema de rendiment quan una proposta de factura del projecte es comptabilitza en el mode per lots, a causa de la unió amb **GeneralJournalAccountEntry**. |
| Administració i comptabilitat de projectes | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Hi ha problemes de rendiment quan es comptabilitza un full d'hores. |
| Administració i comptabilitat de projectes | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La jerarquia d'estimacions de cost de l'estructura del desglossament del treball no s'alinea correctament després d'expandir totes les tasques o després d'expandir una única tasca manualment. |
| Administració i comptabilitat de projectes | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | La plantilla de l'Excel d'oferta del projecte no es pot afegir al menú **Obre a l'Excel**. |
| Administració i comptabilitat de projectes | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | El número exempt d'impostos d'una entitat jurídica no s'inclou a la factura de projecte impresa. |
| Administració i comptabilitat de projectes | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Error No s'actualitzen les dades financeres a la unitat d'inventari quan s'ajusta un projecte en relació amb línies d'abonament. |
| Administració i comptabilitat de projectes | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Després d'aplicar KB 461935, no podeu comptabilitzar estimacions si canvieu a seqüències de nombres continus. |
| Administració i comptabilitat de projectes | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoca que l'aplicació mòbil de full d'hores del projecte per a Android deixi de respondre. |
| Administració i comptabilitat de projectes | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | El valor revertit de WIP d'una comptabilització de factures és diferent del valor de WIP comptabilitzat originalment de l'entrada de temps. |
| Administració i comptabilitat de projectes | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | En els casos amb bestreta aplicada, les transaccions amb val no es compensen quan es comptabilitzen els ingressos facturats d'un projecte. |
| Administració i comptabilitat de projectes | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quan la característica **Millora del rendiment de planificació de recursos del projecte** està habilitada, els valors decimals s'arrodoneixen incorrectament per a la disponibilitat i la capacitat de recursos. |
| Administració i comptabilitat de projectes | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quan la característica **Crea estimacions de projecte utilitzant diverses tasques per lots** està habilitada, la creació d'estimacions en un lot que té diverses subtasques funciona només per al període actual. |
| Viatge i despesa | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Una política de peticions de viatges s'ignora i el flux de treball s'aprova sense errors. |
| Viatge i despesa | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>L'aplicació de despesa mòbil no desa la informació següent a la línia de despesa:</p><ul><li>ID del projecte</li><li>Si la despesa es pot facturar</li><li>Número de l'activitat</li></ul> |
| Viatge i despesa | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | El camp **Rebuts adjunts** s'ha definit com a **Sí**, encara que no s'hagi adjuntat cap rebut a la línia de despesa. |
| Viatge i despesa | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Es produeix un error quan canvieu la categoria de despesa per **Personal**. |
| Viatge i despesa | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | No es pot adjuntar un rebut i editar la despesa principal després de dividir una transacció de targeta de crèdit en una despesa de personal. |
| Viatge i despesa | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | La política de despeses de les transaccions entre empreses que tenen un ID de projecte no funciona correctament. |
| Viatge i despesa | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | Falta la informació de la data de comptabilització per als informes de despeses comptabilitzades. |
| Viatge i despesa | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Hi ha problemes amb el mètode de pagament a l'aplicació mòbil de despeses. |
| Viatge i despesa | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Un requisit de viatge que s'ha creat per a un treballador es pot utilitzar per a l'informe de despeses d'un altre treballador abans de la data delegada. |
| Viatge i despesa | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Quan creeu una despesa, els canvis en els valors de la dimensió financera no s'actualitzen correctament al nivell de distribució comptable de l'àrea de treball **Administració de despeses**. |
| Viatge i despesa | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | L'estat d'aprovació de línia de despesa principal no se sincronitza amb l'estat d'aprovació de flux de treball de la línia detallada. |
| Viatge i despesa | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Es produeix un error si comptabilitzeu un informe de despeses i la recuperació de l'impost està habilitada. |
| Viatge i despesa | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un delegat no pot suprimir documents de despeses per a un empleat finalitzat. |
| Viatge i despesa | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | La supressió d'una línia de despesa triga més del que s'esperava i afecta el rendiment. |
| Viatge i despesa | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoca un registre **TaxUncommitted** orfe perquè només se suprimeix **SourceDocumentLine**. |
| Viatge i despesa | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** no permet que **trvExpTrans.ReferenceDataAreaId** creï la nova seqüència de números. |

## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reglamentàries de les aplicacions de finances i operacions, vegeu [Actualitzacions reglamentàries](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar la sessió al Microsoft Dynamics Lifecycle Services (LCS) i utilitzar l'eina de cerca de problemes per visualitzar les actualitzacions normatives planificades. La cerca de problemes us permet cercar per país o regió, tipus de funció i llançament.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
