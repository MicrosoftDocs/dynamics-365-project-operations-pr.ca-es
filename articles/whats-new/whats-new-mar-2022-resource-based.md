---
title: 'Novetats de març de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de març de 2022 de Project Operations per a escenaris basats en recursos / no emmagatzemats.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600730"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de març de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest tema s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.30.0.99 d'operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.25

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

Els per diems ara són compatibles amb el nou i reimaginat espai de treball de despeses modern. Les empreses que utilitzen per diems poden permetre que aquesta funció ofereixi als usuaris una manera fàcil de presentar i ser reemborsats per les seves despeses de per diem. Per a més informació, vegeu [Despeses de Per diem](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La llista següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió de Project Operations march 2022.

| **Assignació d'entitats** | **Versió actualitzada** | **Comentaris** |
| --- | --- | --- |
| Project Operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Assignacions actualitzades per alinear-se amb l'entitat de la línia de factura del proveïdor al Dataverse. <br>No activeu la versió de l'assignació 1.0.0.4. Estarà llest per utilitzar-lo en combinació amb la versió 10.0.26 de l'entorn financer en la propera actualització mensual. |

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions Dataverse de projecte i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema de columnes de la [taula que falten a la secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Temps i despeses | 2388011 | Mostra els comentaris de rebuig als remitents d'entrades de temps durant l'aprovació massiva. |
| Planificació i seguiment de projectes | 2495294 | Els detalls del projecte no s'han d'editar a la pàgina Detalls **de la** tasca. |
| Facturació i preus | 2499605 | Les fites del contracte que es creen a partir de fites de cotització es marquen incorrectament com a només de lectura. |
| Planificació i seguiment de projectes | 2506050 | El conjunt d'operacions romandrà pendent durant una hora si no hi ha cap canvi per desar. El conjunt es marca falsament com a **Fallit**, mentre que s'ha de completar immediatament. |
| Facturació i preus | 2507401 | Les unitats de contractació per defecte no s'han introduït correctament en projectes a causa d'una memòria cau incorrecta. |
| Facturació i preus | 2541660 | **La validació de creació** de comandes de vendes en doble escriptura ha de ser només per a comandes basades en projectes. |
| Facturació i preus | 2552745 | Els impostos no es divideixen entre els clients que han configurat regles de facturació dividides. |
| Facturació i preus | 2558859 | S'han millorat els missatges d'error quan es configuren les dimensions de preus. |
| Facturació i preus | 2558933 | **La importació des de les estimacions** del projecte falla quan **s'afegeix el projecte\_ msdyn** com a dimensió de preus. |
| Facturació i preus | 2559101 | La supressió del paràmetre del projecte no està bloquejada i causa problemes. |
|   Administració d'oportunitats | 2570390 | El connector de doble escriptura força el tipus de compte a les cotitzacions, comandes i oportunitats de ser **client**, fins i tot quan aquest tipus de compte no és correcte. |
| Facturació i preus | 2586097 | Els reals de cost facturat dividits no s'inverteixen quan un projecte s'elimina d'una línia de contracte del projecte. |
| Facturació i preus | 2589619 | L'impost sobre el material d'escriptura es propaga a les vendes reals no facturades i a la factura. |
|   Administració d'oportunitats | 2594015 | Un pressupost no es pot tancar com a guanyat per als clients que tinguin condicions **de pagament Net60**. |
| Planificació i seguiment de projectes | 2595841 | Al Projecte per al web, els usuaris reben un missatge d'error sobre un inici **real de l'msdyn\_ que falta** quan creen una sol·licitud de recurs nova. |
| Temps i despesa | 2602511 | El **camp Rebutjat per** a les entrades de temps mostra **Sistema** en lloc d'un usuari amb nom com a rebutjador. |
| Temps i despesa | 2602528 | Un aprovador de projectes pot aprovar temps en projectes en què no es mostreja com a aprovador. |
| Facturació i preus | 2608550 | Es pot confirmar una factura de correcció encara que no hi hagi canvis en l'original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestió de projectes i comptabilitat sobre Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Hi ha un desajust entre les operacions financeres i de projectes en la longitud permesa del **camp Category ID**. |
| Administració i comptabilitat de projectes | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Els projectes de preus fixos no es poden eliminar quan el camp facturació **a compte s'estableix** en **Guanys i pèrdues** i s'utilitza el **principi de percentatge** completat. |
| Administració i comptabilitat de projectes | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | S'introdueix un grup d'impostos sobre les vendes per defecte incorrecte des de la configuració del projecte a les línies de despeses del diari d'integració d'operacions del projecte. |
| Administració i comptabilitat de projectes | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | No podeu editar les dimensions de la capçalera de la proposta de factura del projecte en una implementació integrada amb les operacions del projecte. |
| Administració i comptabilitat de projectes | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Les factures del proveïdor d'interempresa no s'han d'integrar amb Dataverse. |
| Administració i comptabilitat de projectes | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Hi ha un desajust en la moneda de saldos del client i en la moneda d'informes. |
| Administració i comptabilitat de projectes | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Podeu publicar una factura del projecte encara que el client estigui retint per a totes les factures. |
| Administració i comptabilitat de projectes | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Falta **el botó Suprimeix totes les línies de les** propostes de factures del projecte que tenen les **visualitzacions Capçalera** i **Línies**. |
| Administració i comptabilitat de projectes | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Quan publiqueu una factura de proveïdor, es produeix l'error següent: "La data comptable de la factura ha d'estar en el mateix exercici comptable que la comanda comprada relacionada. Executar el procés de finalització de l'any de l'ordre de compra o canviar la data a l'any comptable actual". |
| Viatge i despesa | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | El cost compromès d'un projecte no es publica després de l'alliberament del cost compromès de la sol·licitud de viatge. |
| Viatge i despesa | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | L'error següent es produeix quan envieu un informe de despeses: "Traça la pila: l'empresa no existeix". |
| Viatge i despesa | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | L'identificador **de projecte per defecte** no s'introdueix als informes de despeses quan se selecciona el paràmetre Requereix activitat **per al diari** al projecte. |
| Viatge i despesa | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | El **botó Despeses** de publicació no funciona correctament a Operacions del projecte per a escenaris de recursos o no emmagatzemats. |
| Viatge i despesa | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Hi ha un problema amb **la tarifa per milla** per a un informe de despeses de quilometratge que inclou els passatgers. |
| Viatge i despesa | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Les taxes de quilometratge de despeses per als empleats no es totalitzen correctament quan s'utilitzen dos tipus de vehicles diferents en la **categoria de despeses de nivells** de taxa de quilometratge. |
| Viatge i despesa | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | La cerca del **camp Projecte** d'una línia de requisa de viatges no retorna la llista correcta de projectes. |
| Viatge i despesa | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **El quilometratge en revisió** mostra un advertiment sobre els informes de despeses. |
| Viatge i despesa | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | El servei de reconeixement òptic de caràcters (OCR) de recepció no funciona a causa d'un problema amb l'URL del servei OCR de despeses. |
| Viatge i despesa | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quan la **funció Capacitat de detallar les despeses recurrents està habilitada ràpidament**, els imports de les línies d'desglossació dels informes de despeses canvien els imports cada vegada que s'obre la **pàgina Element**. |
| Viatge i despesa | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | No podeu suprimir un informe de despeses quan la llista provisional tingui més d'un aprovador. |

## <a name="removed-and-deprecated-features"></a>Característiques eliminades i obsoletes

Les [característiques eliminades o obsoletes del tema Operacions](removed-depreciated-features-project.md) del projecte descriuen les característiques que s'han suprimit o obsolet per a Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Una característica obsoleta no està en desenvolupament actiu i es pot suprimir en una actualització futura.

Apareixerà un anunci de despreocupat a les funcions Eliminades o obsoletes del [tema Operacions](removed-depreciated-features-project.md) del projecte 12 mesos abans que s'elimini cap característica del producte.

Per trencar els canvis que només afecten el temps de compilació, però són binaris compatibles amb sandbox i entorns de producció, el temps d'espera serà inferior a 12 mesos. Normalment, aquests canvis són actualitzacions funcionals que s'han de fer al compilador.
