---
title: Administració d'una factura proforma basada en projecte
description: Aquest tema proporciona informació sobre com administrar i treballar amb factures proforma basades en projecte.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c61b0d887ae35988f1765d40de0447aa5fd7efd4
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593738"
---
# <a name="manage-a-proforma-project-based-invoice"></a>Administració d'una factura proforma basada en projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Al Dynamics 365 Project Operations, les factures proforma són una extensió de les factures del Dynamics 365 Sales. No obstant això, hi ha moltes diferències en el procés de facturació entre el Sales i el Project Operations quan es tracta de la facturació. Per exemple, no és possible crear una factura nova des de la pàgina **Llista de factures** al Project Operations, però és possible fer-ho al Sales. Aquestes diferències i extensions existeixen per permetre processos de facturació de projectes diferents d'una factura típica d'una comanda de vendes.

> [!IMPORTANT]
> A causa de les diferències, no utilitzeu factures al Sales i al Project Operations indistintament.

## <a name="invoice-header"></a>Capçalera de la factura

La informació següent està disponible en una capçalera de factura proforma al Project Operations.

| Camp | Location | Descripció |
| --- | --- | --- | 
| **ID de factura** | Pestanya **Resum** | Identificador que es genera automàticament quan es crea una factura proforma. Camp només de lectura que no es pot editar. Aquest camp s'utilitza com a referència per a cada factura proforma. |
| **Nom** | Pestanya **Resum** | Es defineix al nom del contracte del projecte per defecte. Aquest camp es pot editar. | 
| **Moneda** | Pestanya **Resum** | Es defineix a la moneda del contracte del projecte per defecte. Camp només de lectura que no es pot editar. |
| **Llista de preus** | Pestanya **Resum** | Es defineix a la llista de preus del contracte del projecte per defecte. Camp només de lectura que no es pot editar. | 
| **Oportunitat** | Pestanya **Resum** | Referència a l'oportunitat enllaçada. Camp només de lectura que no es pot editar. | 
| **Contracte** | Pestanya **Resum** | Referència al contracte de projecte enllaçat. Camp només de lectura que no es pot editar. | 
| **Client** | Pestanya **Resum** | Referència al contracte de projecte enllaçat. Camp només de lectura que no es pot editar. |
| **Descripció** | Pestanya **Resum** | Camp de text que descriu la factura. Aquest camp es pot editar. | 
| **Facturació a** i camps relacionats | **Pestanya Resum** | Els valors per defecte s'estableixen a partir del client del contracte del projecte. Aquest camp es pot editar.  | 
| **Estat** | Pestanya **Resum** | Defineix les opcions següents: **Activa**, **Tancada**, **Pagada** i **Cancel·lada** i es pot editar. Els estats no admesos pel Project Operations són **Tancat** i **Cancel·lat**. </br> L'estat es defineix a **Actiu** quan es crea la factura. </br>L'estat s'ha de definir a **Pagat** només un cop confirmada la factura.  | 
| **Estat de la factura del projecte** | Pestanya **Resum** | Defineix les opcions següents: **Esborrany**, **En revisió** i **Confirmat**, i es pot editar. Tant en els estats **Esborrany** com **En revisió**, la factura es pot editar. La factura no es pot editar un cop confirmada. | 
| **Import detallat** | Pestanya **Resum** | Suma dels imports en totes les línies de facturació després dels avançaments i deduccions. Camp només de lectura que no es pot editar.  Aquest camp s'utilitza per calcular l'import final. | 
| **Descompte (%)** | Pestanya **Resum** | Aquest camp es pot editar per introduir un percentatge de descompte. Aquesta opció no és compatible amb la funcionalitat del Project Operations. No s'admet aquest camp.|  
| **Import del descompte** | Pestanya **Resum** | Aquest camp es pot editar per introduir l'import de descompte. Aquesta opció no és compatible amb la funcionalitat del Project Operations. No s'admet aquest camp. |  
| **Import sense transport** | **Pestanya Resum** | Import total de la factura un cop aplicats els descomptes. Camp només de lectura que no es pot editar. Aquest camp s'utilitza per calcular l'import final.  | 
| **Import del transport** | Pestanya **Resum** | Aquest camp es pot editar per introduir l'import de transport. Aquesta opció no és compatible amb la funcionalitat del Project Operations. No s'admet aquest camp. |
| **Impost total** | Pestanya **Resum** | Impost total de totes les línies de facturació de la factura. Camp només de lectura que no es pot editar. | 
| **Import total** | Pestanya **Resum** | Suma de l'import després dels descomptes i impostos. La suma és l'import que el client ha de pagar. | 

## <a name="project-based-invoice-lines"></a>Línies de contracte basades en el projecte

Al Project Operations, sempre hi ha una línia de facturació per a cada línia de contracte del projecte. La línia de facturació es crea encara que no hi hagi cap valor real. La informació següent està disponible en una línia de factura proforma.

| Camp | Location | Descripció | 
| --- | --- | --- |
| **ID de factura** | Pestanya **General** | Referència a l'identificador de factura. Camp només de lectura que no es pot editar. L'enllaç de l'identificador de factura es pot utilitzar per tornar a la capçalera de la factura. | 
| **Nom** | Pestanya **General** | Nom de la línia de factura definit per defecte a partir del nom de la línia de contracte. Aquest camp es pot editar. |
| **Project** | Pestanya **General** | Projecte de la línia de contracte de projecte relacionada. Camp només de lectura que no es pot editar. L'enllaç del projecte es pot utilitzar per navegar al projecte. | 
| **Mètode de facturació** | Pestanya **General** | Mètode de facturació de la línia de contracte de projecte relacionada. Camp només de lectura que no es pot editar. |
| **Import de la línia de contracte** | Pestanya **General** | Import del contracte a la línia de contracte del projecte relacionada. Camp només de lectura que no es pot editar. | 
| **Facturat fins a la data** | Pestanya **General** | Suma d'imports en tots els detalls de la línia de facturació d'aquesta factura. Camp només de lectura que no es pot editar. | 
| **Import** | Pestanya **General** | Suma d'imports en tots els detalls de la línia de facturació imputables d'aquesta factura. Camp només de lectura que no es pot editar. Aquest camp s'utilitza per calcular l'import final a la capçalera de la factura. | 
| **Impost** | Pestanya **General** | Suma d'imports d'impostos en tots els detalls de la línia de facturació d'aquesta línia de facturació. Camp només de lectura que no es pot editar. Aquest camp s'utilitza per calcular l'import d'impostos final a la capçalera de la factura. | 
| **Import ampliat** | Pestanya **General** | Suma d'imports totals (**Impostos + Imports**) en tots els detalls de la línia de facturació imputables d'aquesta línia de facturació. Camp només de lectura que no es pot editar. Aquest camp s'utilitza per calcular l'import final a la capçalera de la factura. |

## <a name="invoice-line-details"></a>Detalls de la línia de factura

Cada línia de factura d'una factura del projecte inclou detalls de la línia de factura. Aquests detalls de línia estan relacionats amb els valors reals de vendes sense facturar i les fites relacionades amb la línia de contracte a la qual fa referència la línia de facturació. Totes aquestes transaccions estan marcades com a **A punt per facturar**.

Per a una línia de **Factura de temps i material**, els detalls de la línia de factura s'agrupen en **Imputables**, **No imputables** i **Gratuïts** a la pàgina **Línia de factura**. Els detalls de **Línia de factura imputable** se sumen al total de la línia de factura. **Complementari** i **Valors reals no imputables** no sumen al total de la línia de factura.

Per a una línia de **Factura de preu fix**, els detalls de la línia de factura es creen a partir de les fites marcades com a **Preparat per a la factura** a la línia de contracte relacionada. Després de crear el detall de la línia de factura a partir d'una fita, l'estat de facturació de la fita s'actualitza a **Factura del client creada**.

### <a name="edit-invoice-line-details"></a>Editar els detalls de la línia de factura

Els camps següents estan disponibles al detall de la línia de factura basat en un valor real de vendes sense facturar.

| Camp | Descripció |
| --- | --- | 
| **Línia de factura** | Referència a l'**identificador de línia de factura**. Aquest camp només és de lectura i està bloquejat per a l'edició. Aquest enllaç es pot utilitzar per tornar a la capçalera de la factura. | 
| **Descripció** | Descripció del detall de la línia de factura. Es defineix per defecte a partir del camp **Comentaris interns** de l'**entrada de temps** i el camp **Descripció** de l'**entrada de despesa**. El camp es pot editar.| 
| **Descripció externa** | Descripció del detall de la línia de factura. Es defineix per defecte a partir del camp **Comentaris externs** de l'**entrada de temps** i el camp **Descripció** de l'**entrada de despesa**. El camp es pot editar. Aquesta descripció es pot utilitzar per determinar quins elements han d'aparèixer a la factura impresa que s'enviarà al client. Al Project Operations, una factura proforma no té tota la funcionalitat necessària per configurar els paràmetres d'impressió d'una factura. | 
| **Data d’inici** | És un camp només de lectura que té per defecte el valor real d'origen. |
| **Project** | És un camp només de lectura que es defineix per defecte des del valor real d'origen al projecte de la línia de contracte relacionada. |  
| **Tasca** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |
| **Categoria de la transacció** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Funció** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |  
| **Recurs que es pot reservar** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Empresa de dotació de recursos** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Unitat de recursos** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Quantitat** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |  
| **Planificació d'unitat** | Per al detall de la línia de factura d'hora, sempre es defineix a l'hora i no es pot editar. Per a les despeses, es defineix per defecte a partir del valor real de despesa d'origen. Camp només de lectura que no es pot editar. | 
| **Unitat** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |  
| **Preu** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |
| **Moneda** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Import** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Impostos** | Es defineix per defecte a partir del valor real d'origen. El camp es pot editar.| 
| **Import ampliat** | Camp calculat, calculat com a **Import + impostos**. Camp només de lectura que no es pot editar. | 
| **Tipus de facturació** | Es defineix per defecte a partir del valor real d'origen. El camp es pot editar. Si seleccioneu **Imputable** s'afegeix la línia al total de la línia de factura. **Complementari** i **No imputable** l'exclouen del total de la línia de factura.| 
| **Seleccioneu el producte** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |
| **Producte** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 
| **Nom del producte** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |  
| **Descripció de producte fora de catàleg** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. |
| **Tipus de transacció** | És un camp només de lectura que es defineix per defecte des del valor real d'origen a **Vendes facturades**. |  
| **Classe de la transacció** | Es defineix per defecte a partir del valor real d'origen. Camp només de lectura que no es pot editar. | 

Els camps següents estan disponibles al detall de la línia de factura basat en una fita.

| Camp | Descripció |
| --- | --- | 
| **Línia de factura** | Referència a l'**identificador de línia de factura**. Camp només de lectura que no es pot editar. L'enllaç es pot utilitzar per tornar a la capçalera de la factura.  | 
| **Descripció** | Descripció del detall de la línia de factura. Es defineix per defecte a partir de la descripció de la fita d'origen. | 
|**Descripció externa** | Descripció del detall de la línia de factura que es defineix per defecte a la descripció de la fita d'origen. Aquest camp es pot utilitzar per determinar quins elements han d'aparèixer a la factura impresa que s'enviarà al client. Al Project Operations, una factura proforma no té tota la funcionalitat necessària per configurar els paràmetres d'impressió d'una factura. | 
| **Data d'inici** | Es defineix per defecte a partir de la data de la **fita** a la fita d'origen. Camp només de lectura que no es pot editar. | 
| **Project** | Es defineix per defecte a partir de la fita d'origen. Camp només de lectura que no es pot editar. |
| **Tasca** | Es defineix per defecte a partir de la fita d'origen. Camp només de lectura que no es pot editar. | 
| **Categoria de la transacció** | Camp només de lectura que no es pot editar. |
| **Funció** | Camp només de lectura que no es pot editar. | 
| **Recurs que es pot reservar** | Camp només de lectura que no es pot editar. | 
| **Unitat de recursos** | Camp només de lectura que no es pot editar. | 
| **Planificació d'unitat** | Camp només de lectura que no es pot editar. | 
| **Unit** | Camp només de lectura que no es pot editar. | 
| **Preu** | Es defineix per defecte a partir de l'import de la fita d'origen. Camp només de lectura que no es pot editar. |
| **Moneda** | Es defineix per defecte a partir de la fita d'origen. Camp només de lectura que no es pot editar. |
| **Import** | Es defineix per defecte a partir de l'import de la fita d'origen. Camp només de lectura que no es pot editar. | 
| **Impost** | Es defineix per defecte a partir de l'import d'impostos de la fita d'origen. Camp només de lectura que no es pot editar. |
| **Import ampliat** | Es defineix per defecte a partir de l'import ampliat de la fita d'origen. El camp es pot editar. | 
| **Tipus de facturació** | Sempre es defineix per defecte a **Imputable**. Camp només de lectura que no es pot editar. |
| **Tipus de transacció** | Es defineix per defecte a partir de la fita d'origen. Camp només de lectura que no es pot editar. | 
| **Classe de la transacció** | Es defineix per defecte a partir de la fita d'origen. Camp només de lectura que no es pot editar. | 

## <a name="refresh-invoice-transactions"></a>Actualitzar les transaccions de la factura

Si teniu valors reals incorporats després de crear la factura, podeu incloure aquests valors reals a la factura.

1. A la **visualització de treball pendent de facturació**, marqueu les dades com a **A punt per facturar**.   
2. Obriu la factura proforma de l'esborrany i, a la franja **Accions**, seleccioneu **Actualitza les transaccions de la línia de factura**.

  Els detalls de la línia de factura es creen per a qualsevol valor real que tingui una data anterior i estigui marcat com a **Preparat per a la factura**, però no s'inclou a la factura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
