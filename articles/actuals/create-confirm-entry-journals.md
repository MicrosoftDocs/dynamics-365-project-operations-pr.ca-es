---
title: Creació i confirmació de llibres diari d'entrada
description: En aquest article s'ofereix informació sobre com crear i confirmar les revistes d'entrada a Microsoft Dynamics 365 Project Operations.
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

Utilitzeu els diaris d'entrada per registrar els reals directament a Microsoft Dynamics 365 Project Operations. Quan utilitzeu els diaris d'entrada, no heu d'introduir registres d'ús de temps, despesa i material a Operacions del projecte.

Un únic diari d'entrada us permet crear diverses línies de diari. Quan es confirma la revista, una línia de diari d'entrada registra el real per als detalls següents:

- El cost o els ingressos, en funció del tipus de transacció que s'hagi seleccionat.
- La classe de transacció seleccionada. Les classes disponibles són **Temps**, **Despesa**, **Material**, **Retenidor**, **Fita** i **Impostos**.
- El projecte i/o una tasca que se selecciona a la línia de diari.

Seguiu aquests passos per crear un diari d'entrada a Les operacions del projecte.

1. Aneu **a** \> **Revistes de transaccions** \> **de vendes.**
2. A la **pàgina Llista de revistes** d'entrada, a la subfinestra d'acció, seleccioneu **Crea** per crear un diari.
3. A la **pàgina Nova del diari**, al **camp Descripció**, introduïu una descripció de la revista.
4. Assegureu-vos que el **camp tipus** Diari estigui definit com a Entrada **i, a** continuació, seleccioneu **Desa**. Després de desar el nou diari d'entrada, hauria d'aparèixer una **pestanya Línies** de diari a la pàgina del diari.
5. A la **pestanya Línies** del diari, a la barra d'eines que hi ha a sobre de la quadrícula, seleccioneu **Crea** per crear una línia de diari d'entrada.
6. Al quadre de **diàleg Creació** ràpida per crear una línia de diari d'entrada, definiu els camps tal com es descriu a la taula següent.

    | Camp | Descripció | Impacte funcional |
    | --- | --- | --- |
    | Classe de la transacció | La línia de diari es pot classificar en una de les sis classes de transaccions: **Temps**, **Despesa**, **Material**, **Retenidor**, **Fita** o **Impost**. | La **classe de transacció d'impostos** ha quedat obsoleta a Les operacions del projecte. <br> Si creeu una **classe de transacció d'impostos**, no es processaran mitjançant la facturació ni en els càlculs de costos o ingressos. **Milestone** és una classe de transacció només d'ingressos. <br>La **classe de transacció Retainer** representa un avanç que s'ha rebut d'un client. Sempre s'ha de crear com un parell de vendes facturades i línies de diari de vendes no facturades. |
    | Tipus de transacció | Els **tipus de transaccions de costos** unitàries de cost de **cost**, interorg **i** recursos s'han d'utilitzar per registrar el cost.<br> Els **tipus de transaccions vendes** no facturades i **vendes** facturades s'han d'utilitzar per registrar els ingressos. | La **classe de transacció Retainer** només funciona amb els **tipus de transaccions Vendes** no facturades i **vendes** facturades.<br> La **classe de transacció Milestone** només funciona amb el **tipus de transacció Vendes** facturades. <br>Els **tipus de transaccions de costos** unitaris De vendes **i** recursos Interorg només s'apliquen a la **classe de transacció Time** i només es poden aviar a les revistes d'entrada al scneario de desplegament de Lite i no quan es despleguen operacions de projecte en els escenaris de recursos / no emmagatzemats. |
    | Seleccioneu el producte | Quan se selecciona la **classe de transacció Material**, aquest camp us permet especificar si la transacció material per a la qual esteu creant la línia de diari és un producte existent o un producte d'escriptura. | Si seleccioneu **Producte d'escriptura**, podeu introduir un nom per al producte. |
    | Producte | Una referència al producte del catàleg. | |
    | Descripció | Una descripció de la línia del diari per ajudar a facilitar la identificació. | Per a les línies de diari de vendes no facturades, el valor s'utilitzarà com a descripció quan es creï el detall de la línia de factura. |
    | Descripció externa | Una descripció de la línia de la revista que es pot utilitzar per compartir amb grups d'interès externs. | Per a les línies de diari de vendes no facturades, el valor s'utilitzarà com a descripció externa quan es creïn els detalls de la línia de factura. També pot aparèixer a la factura que s'envia al client. |
    | Tipus de facturació | Valor que indica si la línia de diari es comptabilitzarà com a component carregador, complementari o no cobrable del projecte. | En un flux típic, el tipus de facturació es deriva dels termes acordats que s'estableixen al contracte. Tanmateix, quan registreu una línia de diari, podeu introduir un valor en aquest camp. |
    | Data del document | Utilitzeu una data en què s'ha produït la transacció. | |
    | Data d’inici | Utilitzeu la data en què s'ha produït la transacció. | Aquest camp s'utilitza per comparar amb la data de creació de factures per a transaccions del **tipus Vendes** no facturades. Aquesta comparació us ajudarà a decidir si la transacció és futura o amb data passada. Només s'afegiran transaccions datades a la factura. |
    | Data d’acabament | Utilitzeu la data en què s'ha produït la transacció. | |
    | Data de comptabilitat | Utilitzeu la data en què es registrarà l'impacte comptable. | |
    | Client de la línia de contracte | Per defecte, si la línia de contracte només té un client, aquest camp s'estableix al client de la línia de contracte quan es desa la línia de diari. Si la línia de contracte té diversos clients, seleccioneu el client correcte a la línia de contracte. | Si el sistema no pot determinar el client de la línia de contracte a la línia de diari i si està en blanc sobre el tipus de **vendes** no facturades que es crea a partir de la línia de diari, el real no es facturarà. |
    | Project | Seleccioneu el projecte en què voleu enregistrar-ne l'actual. | En funció del projecte seleccionat, la classe de transacció i la tasca, el sistema intentarà determinar el contracte, la línia de contracte i el client de la línia de contracte. |
    | Tasca | Seleccioneu la tasca on voleu enregistrar el real. | Si heu associat tasques amb línies de contracte durant la configuració del contracte, el sistema utilitzarà la tasca seleccionada, juntament amb una classe de projecte i transacció, per determinar el contracte, la línia de contracte i el client de la línia de contracte. |
    | Categoria de transacció | Seleccioneu la categoria de transacció on voleu registrar-ne l'actual. | Per a les despeses, la categoria de transacció seleccionada determina el preu per defecte que s'introduirà a la línia de diari quan es desi. |
    | Funció | Aquest camp és rellevant per a les línies del diari Time. Seleccioneu la funció del recurs que ha dedicat temps al projecte i/o a la tasca. | Per a les línies de diari de Time, si utilitzeu la configuració desastrós per a l'entrada dels costos de recursos predeterminats i les taxes de factura, la funció seleccionada s'utilitza juntament amb la unitat de recursos per determinar el preu per defecte que s'introduirà a la línia de diari quan es desi. Si utilitzeu una configuració personalitzada per a l'entrada de preus per defecte, hauríeu de revisar aquesta configuració per determinar si el camp Funció **s'utilitza** per introduir valors de preu predeterminats. |
    | Subcontracte | Si la línia de diari representa capacitat subcontractada, o despeses o materials subcontractats, seleccioneu la subcontractació corresponent. | Quan es registren les línies del diari de cost, la subcontractació seleccionada determinarà la llista de preus que s'utilitza per introduir el cost unitari per defecte. |
    | Línia subcontractada | Si la línia de diari representa capacitat subcontractada, o despeses o materials subcontractats, seleccioneu la línia de subcontractació corresponent. | Quan es registren les línies de diari de cost, la línia de subcontractació seleccionada garantirà que els càlculs de capacitat disponibles a la línia de subcontractació es calculin correctament. |
    | Mètode de l’import | Per defecte, aquest camp està definit com a **Multiplica la quantitat per preu**. Quan s'utilitzi aquest mètode, l'import es calcularà com a *quantitat* × *preu*. L'altre mètode compatible és **el preu** fix. Quan s'utilitzi aquest mètode, el preu s'establirà en l'import i la quantitat no s'utilitzarà en el càlcul. | |
    | Planificació i unitat d'unitats | Junts, la unitat de planificació i unitat identifiquen la unitat de la quantitat. | La combinació de la unitat i la categoria de transacció s'utilitza per introduir preus predeterminats per a les despeses. A la configuració per defecte de les operacions del projecte, la combinació de la unitat, la funció i la unitat de recursos s'utilitza per introduir preus predeterminats durant el temps. Si teniu una configuració personalitzada per a l'entrada de preus predeterminats, s'utilitzarà juntament amb la unitat. La combinació del producte i la unitat s'utilitza per introduir preus predeterminats per als materials. |
    | Quantitat | Introduïu la quantitat. | |
    | Preu | Si el preu es deixa en blanc quan es crea la línia de diari, s'utilitzaran els valors rellevants per introduir els preus predeterminats, depenent de la classe de transacció. Si s'introdueix un preu quan es crea la línia del diari, s'utilitzarà aquest preu. | |
    | Impostos | Introduïu qualsevol import d'impostos. | En funció de l'import de l'impost que s'introdueixi, l'import prorrogat es calcularà com a *Import* + *De l'Impost*. |

## <a name="confirm-an-entry-journal"></a>Confirmar un diari d'entrada

Després d'haver introduït totes les línies del diari en un diari d'entrada, podeu confirmar el diari. Aquest procés registrarà cada línia de diari com a reals en els projectes adequats.

Després de confirmar-se un diari, ja no podeu editar-lo ni cap de les seves línies.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Reals creats per la confirmació del diari d'entrada

Hi ha algunes diferències clau entre els reals que es creen mitjançant la confirmació del diari d'entrada i els reals que es creen durant l'aprovació dels registres d'ús de temps, despesa i material i la confirmació de factures a les operacions del projecte:

- Els diaris d'entrada no utilitzen connexions de transacció per enllaçar el cost real amb les vendes nobilades reals. Els reals que es creen quan s'aproven els registres d'ús de temps, despesa i material sempre utilitzen connexions de transacció per enllaçar el cost i les vendes no facturades reals.
- Els diaris d'entrada no utilitzen els orígens de les transaccions per enllaçar els reals de cost reals i els reals de vendes nobilats a cap registre originat. Els reals que es creen quan s'aproven els registres de temps, despesa i ús de material sempre utilitzen els orígens de la transacció per enllaçar el cost i les vendes no facturades reals a l'entrada de temps d'origen.
- Quan es facturen els reals de vendes no facturats que es creen mitjançant la confirmació del diari d'entrada, els reals de vendes facturats que es creen durant la confirmació de la factura estan vinculats als reals de vendes no facturats, de manera similar als reals de vendes no facturats que es creen quan s'aproven els registres d'ús de temps, despesa i material.
- Les línies de diari d'entrada creades durant el temps que introdueixen els recursos interorganitzatius no fan que els reals del cost de la **unitat de recursos i** els tipus de vendes **d'Interorg es creïn** automàticament. Aquests reals s'han de crear manualment. Aquest comportament difereix del comportament de les entrades de temps que es registren mitjançant recursos interorganitzatius. En aquest cas, quan s'aprova el temps, l'aplicació crea automàticament reals del tipus de **cost del projecte i reals del cost** de la **unitat de recursos i** els tipus de vendes **d'Interorg a la divisió propietària de l'empleat**. A continuació, utilitza connexions de transacció per enllaçar aquests reals i els orígens de la transacció per enllaçar-los amb l'entrada de temps d'origen.
- Quan es confirmen els diaris d'entrada, creen reals. No obstant això, els diaris de correcció no es poden utilitzar per corregir aquests reals. Aquest comportament difereix del comportament dels registres d'ús de temps, despesa i material. En aquest cas, l'aplicació us permet utilitzar revistes de correcció per corregir els reals per corregir els errors, sempre que aquests reals encara no s'hagin facturat. Si ja s'han facturat, encara podeu corregir un real si processeu un crèdit complet d'aquest real al client.

> [!NOTE]
> Els diaris d'entrada no apliquen regles estrictes de per defecte. Per tant, utilitzeu aquests diaris d'entrada el menys possible i tingueu precaució i tingueu cura per assegurar-vos que no creeu dades financeres corruptes al vostre sistema. Sempre que pugueu, utilitzeu els registres d'ús de temps, despesa i material, la configuració de fites i retenció als contractes del projecte i el procés de confirmació de factures del projecte en lloc de revistes d'entrada per crear reals.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
