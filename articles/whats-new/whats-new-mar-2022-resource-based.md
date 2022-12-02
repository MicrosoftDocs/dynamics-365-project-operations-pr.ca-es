---
title: 'Novetats de març de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de març de 2022 del Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910894"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de març de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.30.0.99
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.25

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

Les dietes s'admeten ara a la nova àrea de treball moderna de despeses. Les empreses que utilitzen dietes poden habilitar aquesta característica per oferir als usuaris una manera senzilla d'enviar i reemborsar les despesa de dietes. Per obtenir-ne més informació, consulteu [Despeses de dietes](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

A la llista següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de març de 2022 del Project Operations.

| **Assignació d'entitats** | **Versió actualitzada** | **Comentaris** |
| --- | --- | --- |
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Assignacions actualitzades per alinear-les amb l'entitat de línia de factura del proveïdor al Dataverse. <br>No activeu l'assignació a la versió 1.0.0.4. Estarà a punt per utilitzar-se conjuntament amb la versió 10.0.26 de l'entorn del Finance a la propera actualització mensual. |

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Temps i despeses | 2388011 | Mostra els comentaris de rebuig a les persones que envien les entrades de temps durant l'aprovació massiva. |
| Planificació i seguiment de projectes | 2495294 | Els detalls del projecte no s'han de poder editar a la pàgina de **Detalls de la tasca**. |
| Facturació i preus | 2499605 | Les fites de contracte creades a partir de les fites d'oferta estan marcades incorrectament com a només de lectura. |
| Planificació i seguiment de projectes | 2506050 | El conjunt d'operacions continua pendent durant una hora si no hi ha cap canvi per desar. El conjunt s'ha marcat erròniament com a **Error**, però s'hauria d'haver completat immediatament. |
| Facturació i preus | 2507401 | Les unitats de contracte per defecte s'introdueixen incorrectament en projectes a causa de l'emmagatzematge incorrecte a la memòria cau. |
| Facturació i preus | 2541660 | La **Validació de creació de comanda de venda** en mode de doble escriptura ha de ser només per a comandes basades en projectes. |
| Facturació i preus | 2552745 | Els impostos no es divideixen entre els clients que han configurat regles de facturació amb divisió. |
| Facturació i preus | 2558859 | S'han millorat els missatges d'error en la configuració de les dimensions de preus. |
| Facturació i preus | 2558933 | **Importa des d'estimacions del projecte** falla quan s'afegeix **msdyn\_project** com a dimensió de preus. |
| Facturació i preus | 2559101 | La supressió de paràmetres de projecte no està bloquejada i provoca problemes. |
|   Administració d'oportunitats | 2570390 | El complement de doble escriptura aplica el tipus de compte **Client** a les ofertes, comandes i oportunitats, encara que aquest tipus de compte no sigui correcte. |
| Facturació i preus | 2586097 | Els valors reals de cost facturats fraccionats no es reverteixen quan s'elimina un projecte d'una línia de contracte del projecte. |
| Facturació i preus | 2589619 | L'impost sobre el material fora de catàleg es propaga als valors reals de vendes no facturades i a la factura. |
|   Administració d'oportunitats | 2594015 | L'oferta no es pot tancar com a guanyada per als clients que tenen condicions de pagament **Net60**. |
| Planificació i seguiment de projectes | 2595841 | A Project for the Web, els usuaris reben un missatge d'error sobre un fitxer **msdyn\_actualstart** que falta quan creen una sol·licitud de recurs nova. |
| Temps i despesa | 2602511 | El camp **Rebutjat per** a les entrades de temps mostra **Sistema** en comptes d'un usuari amb nom com a persona que les rebutja. |
| Temps i despesa | 2602528 | Un aprovador del projecte pot aprovar el temps dels projectes en què no apareix com a aprovador. |
| Facturació i preus | 2608550 | Es pot confirmar una factura de correcció encara que no hi hagi canvis en l'original. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Hi ha una manca de coincidència entre el Finance i el Project Operations en la longitud permesa del camp **ID de categoria**. |
| Administració i comptabilitat de projectes | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Els projectes de preu fix no es poden eliminar quan el camp **Facturació per compte** es defineix com a **Guanys i pèrdues** i s'utilitza el principi de **Percentatge completat**. |
| Administració i comptabilitat de projectes | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | S'introdueix un grup d'impostos per defecte incorrecte de la configuració del projecte a les línies de despesa del llibre diari d'integració del Project Operations. |
| Administració i comptabilitat de projectes | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | No podeu editar les dimensions de la capçalera de la proposta de factura del projecte en una implementació integrada amb el Project Operations. |
| Administració i comptabilitat de projectes | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Les factures de proveïdor entre empreses no s'han d'integrar amb el Dataverse. |
| Administració i comptabilitat de projectes | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Hi ha una manca de coincidència entre la moneda dels saldos de client i la moneda dels informes. |
| Administració i comptabilitat de projectes | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Podeu comptabilitzar una factura del projecte encara que el client estigui retingut per a totes les factures. |
| Administració i comptabilitat de projectes | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Falta el botó **Suprimeix totes les línies** de les propostes de factura del projecte que tenen les visualitzacions **Capçalera** i **Línies**. |
| Administració i comptabilitat de projectes | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Quan comptabilitzeu una factura de proveïdor, es produeix l'error següent: "La data de comptabilitat de la factura ha de ser al mateix any comptable que la comanda comprada relacionada. Executeu el procés d'acabament de l'any de la comanda de compra o canvieu la data a l'exercici comptable actual". |
| Viatge i despesa | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | El cost confirmat d'un projecte no es comptabilitza després d'alliberar un cost compromès de la petició de viatge. |
| Viatge i despesa | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | L'error següent es produeix quan envieu un informe de despesa: "Seguiment de pila: l'empresa no existeix". |
| Viatge i despesa | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | L'**ID de projecte** per defecte no s'introdueix als informes de despesa quan se selecciona el paràmetre **Requereix una activitat per al diari** al projecte. |
| Viatge i despesa | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | El botó **Comptabilitza les despeses** no funciona correctament al Project Operations per als escenaris de recursos / no mantinguts en existències. |
| Viatge i despesa | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Hi ha un problema amb **Tarifa per milla** per a un informe de despeses de quilometratge que inclou passatgers. |
| Viatge i despesa | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Les tarifes de quilometratge de despeses per als empleats no es totalitzen correctament quan s'utilitzen dos tipus de vehicles diferents a la categoria de despeses **Nivells de la taxa de quilometratge**. |
| Viatge i despesa | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | La cerca per al camp **Projecte** en una línia de petició de viatge no retorna la llista de projectes correcta. |
| Viatge i despesa | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Quilometratge en revisió** mostra un advertiment als informes de despeses. |
| Viatge i despesa | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | El servei de reconeixement òptic de caràcters (OCR) del rebut no funciona a causa d'un problema amb l'adreça URL del servei d'OCR de la despesa. |
| Viatge i despesa | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Quan la característica **Capacitat de desglossar les despeses periòdiques ràpidament** està habilitada, els imports de les línies de desglossament dels informes de despesa canvien els imports cada vegada que s'obre la pàgina **Desglossa**. |
| Viatge i despesa | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | No podeu suprimir un informe de despesa quan la llista temporal té més d'un aprovador. |

## <a name="removed-and-deprecated-features"></a>Característiques suprimides i obsoletes

L'article [Característiques eliminades o obsoletes del Project Operations](removed-depreciated-features-project.md) descriu les característiques que s'han eliminat o que són obsoletes per al Dynamics 365 Project Operations.

- Les característiques suprimides deixen d'estar disponibles al producte.
- Les característiques obsoletes no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Un anunci d'obsolescència apareixerà a l'article [Característiques eliminades o obsoletes del Project Operations](removed-depreciated-features-project.md) 12 mesos abans que se suprimeixi qualsevol característica del producte.

Per als canvis que només afecten el temps de compilació, però que són compatibles binaris amb entorns aïllats i de producció, el temps d'obsolescència serà inferior a 12 mesos. Normalment, aquests canvis són actualitzacions funcionals que s'han de fer al compilador.
