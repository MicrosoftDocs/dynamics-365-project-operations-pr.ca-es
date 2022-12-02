---
title: Creació i confirmació de llibres diari d'entrada
description: En aquest article es proporciona informació sobre com crear i confirmar diaris d'entrada al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912320"
---
# <a name="create-and-confirm-entry-journals"></a>Creació i confirmació de llibres diari d'entrada

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per utilitzar diaris d'entrada per registrar els valors reals directament al Microsoft Dynamics 365 Project Operations. Quan utilitzeu diaris d'entrada, no cal que introduïu registres de temps, despesa i ús de materials al Project Operations.

Un sol diari d'entrada permet crear diverses línies del llibre diari. Quan es confirma el llibre diari, una línia del llibre diari d'entrada registra el valor real per als detalls següents:

- El cost o els ingressos, en funció del tipus de transacció que s'ha seleccionat.
- La classe de transacció seleccionada. Les classes disponibles són **Temps**, **Despesa**, **Material**, **Bestreta**, **Fita** i **Impostos**.
- El projecte i/o la tasca que se seleccionen a la línia del llibre diari.

Seguiu aquests passos per crear un diari d'entrada al Project Operations.

1. Aneu a **Vendes** \> **Transaccions** \> **Llibres diari**.
2. A la pàgina de llista de **Diaris d'entrada**, a la subfinestra Acció, seleccioneu **Nou** per crear un diari.
3. A la pàgina **Diari nou**, al camp **Descripció**, introduïu una descripció per al diari.
4. Assegureu-vos que el camp **Tipus de diari** està definit com a **Entrada** i seleccioneu **Desa**. Quan es desa el nou diari d'entrada, ha d'aparèixer una pestanya de **Línies de diari** a la pàgina del diari.
5. A la pestanya **Línies de diari**, a la barra d'eines que hi ha a sobre de la quadrícula, seleccioneu **Nou** per crear una línia del llibre diari d'entrada.
6. Al quadre de diàleg **Creació ràpida** per crear una línia del diari d'entrada, definiu els camps com s'indica a la taula següent.

    | Camp | Descripció | Impacte funcional |
    | --- | --- | --- |
    | Classe de la transacció | La línia del llibre diari es pot classificar en una de sis classes de transaccions: **Temps**, **Despesa**, **Material**, **Bestreta**, **Fita** o **Impostos**. | La classe de transacció **Impostos** ha quedat obsoleta al Project Operations. <br> Si creeu una classe de transacció **Impostos**, no es processarà per a la facturació ni en els càlculs de costos o d'ingressos. **Fita** és una classe de transacció només d'ingressos. <br>La classe de transacció **Bestreta** representa un avançament rebut d'un client. Sempre s'ha de crear com un parell de vendes facturades i línies del llibre diari de vendes no facturades. |
    | Tipus de transacció | Els tipus de transacció **Cost**, **Vendes interorganitzatives** i **Cost d'unitat de recursos** s'han d'utilitzar per registrar el cost.<br> Els tipus de transaccions **Vendes no facturades** i **Vendes facturades** s'han d'utilitzar per registrar els ingressos. | La classe de transacció **Bestreta** només funciona amb els tipusde transaccions **Vendes no facturades** i **Vendes facturades**.<br> La classe de transacció **Fita** només funciona amb el tipus de transacció **Vendes facturades**. <br>**Els tipus de transaccions Vendes interorganitzatives** i **Cost d'unitat de recursos** només s'apliquen a la classe de transacció **Temps** i només estan disponibles als llibres diari d'entrada de l'escenari d'implementació bàsica, no en implementar el Project Operations en escenaris de recursos/ no mantinguts en existències. |
    | Seleccioneu el producte | Quan se selecciona la classe de transacció **Material**, aquest camp us permet especificar si la transacció de material que esteu creant per a la línia del llibre diari és un producte existent o un producte fora de catàleg. | Si seleccioneu **Fora de catàleg**, podeu introduir un nom per al producte. |
    | Producte | Referència al producte del catàleg. | |
    | Descripció | Descripció de la línia del llibre diari per ajudar-vos a identificar-la fàcilment. | Per a les línies del llibre diari de vendes no facturades, el valor s'utilitzarà com a descripció quan es creen els detalls de la línia de factura. |
    | Descripció externa | Descripció de la línia del llibre diari que s'utilitza per compartir amb parts interessades externes. | Per a les línies del llibre diari de vendes no facturades, el valor s'utilitzarà com a descripció externa quan es creen els detalls de la línia de factura. També pot aparèixer a la factura que s'envia al client. |
    | Tipus de facturació | Valor que indica si la línia del llibre diari es comptarà com a component imputable, de cortesia o no imputable al projecte. | En un flux normal, el tipus de facturació es deriva dels termes acordats que es configuren al contracte. Tanmateix, quan registreu una línia del llibre diari, podeu introduir un valor en aquest camp. |
    | Data del document | Utilitzeu una data en què es va produir la transacció. | |
    | Data d’inici | Utilitzeu la data en què es va produir la transacció. | Aquest camp s'utilitza per a la comparació amb la data de creació de la factura per a les transaccions del tipus **Vendes no facturades**. Aquesta comparació us ajudarà a decidir si la transacció té data futura o data anterior. Només s'afegiran a la factura les transaccions anteriors. |
    | Data d’acabament | Utilitzeu la data en què es va produir la transacció. | |
    | Data de comptabilitat | Utilitzeu la data en què es registrarà l'impacte comptable. | |
    | Client de línia de contracte | Per defecte, si la línia de contracte només té un client, aquest camp es defineix com a client a la línia de contracte quan es desa la línia del llibre diari. Si la línia de contracte té diversos clients, seleccioneu el client correcte a la línia de contracte. | Si el sistema no pot determinar el client de la línia de contracte a la línia del llibre diari i si està buit al valor real del tipus **Vendes no facturades** creat des de la línia del llibre diari, el valor real no es facturarà. |
    | Project | Seleccioneu el projecte on voleu registrar el valor real. | Segons el projecte, la classe de transacció i la tasca que s'hagin seleccionat, el sistema intentarà determinar el contracte, la línia de contracte i el client de la línia de contracte. |
    | Tasca | Seleccioneu la tasca on voleu registrar el valor real. | Si heu associat tasques amb línies de contracte durant la configuració del contracte, el sistema utilitzarà la tasca seleccionada, juntament amb un projecte i una classe de transacció, per determinar el contracte, la línia de contracte i el client de la línia de contracte. |
    | Categoria de transacció | Seleccioneu la categoria de transacció on voleu registrar el valor real. | Per a les despeses, la categoria de transacció seleccionada determina el preu per defecte que s'introduirà a la línia del llibre diari quan es desi. |
    | Funció | Aquest camp és rellevant per a les línies del llibre diari de temps. Seleccioneu la funció del recurs que ha dedicat temps al projecte i/o a la tasca. | Per a les línies del llibre diari de temps, si utilitzeu la configuració estàndard per a l'entrada de costos de recursos per defecte i percentatges de facturació, la funció seleccionada s'utilitza juntament amb la unitat de recursos per determinar el preu per defecte que s'introduirà a la línia del llibre diari en desar-la. Si utilitzeu una configuració personalitzada per a l'entrada de preus per defecte, heu de revisar aquesta configuració per determinar si el camp **Funció** s'utilitza per introduir els valors de preu per defecte. |
    | Subcontracte | Si la línia del llibre diari representa capacitat subcontractada, despeses o materials subcontractats, seleccioneu el subcontracte rellevant. | Quan es registren les línies del llibre diari de cost, el subcontracte seleccionat determinarà la llista de preus que s'utilitza per introduir el cost per unitat per defecte. |
    | Línia de subcontracte | Si la línia del llibre diari representa capacitat subcontractada, despeses o materials subcontractats, seleccioneu la línia de subcontracte rellevant. | Quan es registren les línies del llibre diari de cost, la línia de subcontracte seleccionada garantirà que es facin correctament els càlculs de capacitats disponibles a la línia de subcontracte. |
    | Mètode de l’import | Aquest camp està definit com a **Multiplica la quantitat pel preu** per defecte. Quan s'utilitzi aquest mètode, l'import es calcularà com a *Quantitat* × *Preu*. L'altre mètode compatible és **Preu fix**. Quan s'utilitzi aquest mètode, el preu es definirà com l'import i la quantitat no s'utilitzarà en el càlcul. | |
    | Planificació d'unitat i unitats | Juntes, la planificació d'unitats i les unitats identifiquen la unitat de la quantitat. | La combinació de la unitat i la categoria de la transacció s'utilitza per introduir preus per defecte per a les despeses. A la configuració per defecte del Project Operations, s'utilitza la combinació de la unitat, la funció i la unitat de recursos per introduir preus per defecte per al temps. Si teniu una configuració personalitzada per a l'entrada de preus per defecte, s'utilitzarà juntament amb la unitat. La combinació del producte i la unitat s'utilitza per introduir preus per defecte per a materials. |
    | Quantitat | Introduïu la quantitat. | |
    | Preu | Si el preu es deixa en blanc quan es crea la línia del llibre diari, els valors rellevants s'utilitzaran per introduir els preus per defecte, en funció de la classe de transacció. Si s'introdueix un preu quan es crea la línia del llibre diari, s'utilitzarà aquest preu. | |
    | Impostos | Introduïu qualsevol import d'impostos. | Segons l'import d'impostos que s'introdueixi, l'import ampliat es calcularà com a *Import* + *Impostos*. |

## <a name="confirm-an-entry-journal"></a>Confirmar un diari d'entrada

Un cop hàgiu introduït totes les línies del llibre diari en un llibre diari d'entrada, podeu confirmar el llibre diari. Aquest procés registrarà cada línia del llibre diari com a valors reals en els projectes adequats.

Després que es confirmi un diari, ja no es podrà editar el diari ni cap de les línies.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Valors reals creats per la confirmació del llibre diari d'entrada

Hi ha algunes diferències clau entre els valors reals que es creen amb la confirmació del llibre diari d'entrada i els valors reals que es creen durant l'aprovació dels registres de temps, despesa i ús de materials i la confirmació de la factura al Project Operations:

- Els llibres diari d'entrada no utilitzen connexions de transacció per enllaçar el valor real de cost amb el valor real de vendes no facturades. Els valors reals que es creen quan s'aproven els registres de temps, despesa i ús de materials sempre utilitzen connexions de transacció per enllaçar el cost i els valors reals de vendes no facturades.
- Els llibres diari d'entrada no utilitzen els orígens de transacció per enllaçar el valor real de cost i els valors reals de vendes no facturades amb cap registre d'origen. Els valors reals que es creen quan s'aproven els registres de temps, despesa i ús de materials sempre utilitzen orígens de transacció per enllaçar el cost i els valors reals de vendes no facturades amb l'entrada de temps d'origen.
- Quan es facturen els valors reals de vendes no facturades que es creen amb la confirmació del llibre diari d'entrada, els valors reals de vendes facturades que es creen durant la confirmació de la factura s'enllacen amb els valors reals de vendes no facturats, de manera semblant als valors reals de vendes no facturades que es creen quan s'aproven els registres de temps, despesa i ús de materials.
- Les línies del llibre diari d'entrada que es creen per al temps que introdueixen els recursos interorganitzatius no fan que es creïn valors reals dels tipus **Cost unitari de recursos** i **Vendes interorganitzatives**. Aquests valors reals s'han de crear manualment. Aquest comportament és diferent del comportament de les entrades de temps registrades per recursos interorganitzatius. En aquest cas, quan s'aprova el temps, l'aplicació crea automàticament valors reals del tipus **Cost** al projecte i els valors reals dels tipus **Cost unitari de recursos** i **Vendes Interorganitzatives** a la divisió propietària del treballador. També utilitza connexions de transacció per enllaçar aquests valors reals entre sí i els orígens de les transaccions per enllaçar-los amb l'entrada de temps original.
- Quan es confirmen els diaris d'entrada, es creen valors reals. No obstant això, els diaris de correcció no es poden utilitzar per corregir aquests valors reals. Aquest comportament és diferent del comportament dels valors reals que es creen quan s'aproven els registres de temps, despesa i ús de materials. En aquest cas, l'aplicació us permet utilitzar diaris de correcció per corregir els valors reals per corregir els errors, sempre que els valors reals encara no s'hagin facturat. Si ja s'han facturat, podeu corregir un valor real si processeu un abonament complet del valor real al client.

> [!NOTE]
> Els diaris d'entrada no apliquen regles per defecte estrictes. Per tant, utilitzeu aquests diaris d'entrada al mínim possible, i aneu amb compte per assegurar-vos que no creeu dades financeres malmeses al sistema. Sempre que pugueu, utilitzeu els registres de temps, despesa i ús de materials, la configuració de fita i bestreta dels contractes del projecte i el procés de confirmació de factures del projecte en comptes dels diaris d'entrada per crear valors reals.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
