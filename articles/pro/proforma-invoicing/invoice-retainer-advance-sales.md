---
title: Facturació d'una bestreta o avançament
description: Aquest tema proporciona informació sobre com facturar una bestreta o avançament al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c53e39a8c6fb27deff5e7a05d5cca3a4215466
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274131"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Facturació d'una bestreta o un avançament

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations admet contractes sobre bestreta i avançaments únics. En un contracte de projecte, podeu registrar una planificació de bestretes o un avançament únic. No obstant això, l'enregistrament a nivell de contracte del projecte no fa que una bestreta o un avançament estiguin disponibles immediatament per al seu ús. Per utilitzar una bestreta o avançament en una factura que realment cobra al client, primer s'ha de facturar la bestreta o avançament.

Completeu els passos següents per facturar una bestreta o avançament.

1. Seleccioneu **Vendes** > **Facturació** > **Bestretes i avançaments**. 
2. A la pàgina **Avançaments i bestretes**, utilitzeu el filtre per seleccionar la bestreta o avançament específic per facturar-lo i marqueu-lo com a **A punt per facturar**.
3. Creeu una factura manualment des de pàgina de llista o de detalls **Contracte del projecte**. La bestreta o avançament es mostra a l'esborrany de la factura en la secció **Avançaments i bestretes** de la **Factura**.
4. Confirmeu la factura. D'aquesta manera, es podrà utilitzar la bestreta o avançament. Podeu verificar la factura a la pàgina de llista **Bestretes i avançaments**. Per a un avançament o bestreta facturat, la quantitat disponible es mostra a la quadrícula.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Crear una bestreta o avançament des de la quadrícula de factures

Podeu crear una bestreta o avançament directament en una factura.

1. En un esborrany de factura, a la subquadrícula **Avançaments i bestretes**, seleccioneu **Nou** per crear una nova bestreta o avançament. 
2. A la pàgina **Creació ràpida**, afegiu la informació necessària i seleccioneu **Desa**. La bestreta o avançament es crea en el contracte del projecte relacionat amb la factura. La bestreta o avançament es marca automàticament com a **A punt per facturar** i després s'afegeix a la subquadrícula **Avançaments i bestretes** de la pàgina **Factura**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Conciliar una bestreta o avançament facturat

Després de facturar una bestreta o avançament, es pot utilitzar o conciliar en una factura amb temps, despeses, fites o altres càrrecs basats en projectes. El client veurà l'import de la factura reduït en l'import de la bestreta o avançament utilitzat en aquesta factura.

En cada factura que es genera per a un contracte de projecte que té bestretes o avançaments facturats, el Projecte Operations aplica automàticament la bestreta o avançament a la factura.

Això es pot veure a la quadrícula **Bestretes i avançaments aplicats** a la pàgina **Factura**. La taula següent proporciona informació sobre els camps de la quadrícula **Bestretes i avançaments aplicats** de la pàgina **Factura del projecte**.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Descripció | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte** |Aquest camp de només lectura proporciona una descripció de la bestreta o avançament utilitzat en aquesta factura. Aquest valor no es pot canviar a la factura. Aquest valor es pot actualitzar a la subquadrícula de la pàgina **Contracte del projecte**. | Aquest camp es pot mostrar al client a la factura impresa per indicar quina bestreta o avançament s'aplica a la factura. |
| Lliurat el | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte**  | Aquest camp de només lectura proporciona la data de factura de la bestreta o avançament utilitzat en aquesta factura. Aquest valor no es pot canviar a la factura. Aquest valor es pot actualitzar a la subquadrícula de la pàgina **Contracte del projecte**. | Aquest camp es pot mostrar al client a la factura impresa per indicar la data en què es va facturar per primera vegada la bestreta o avançament al client. |
| Import | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte**  | Aquest camp de només lectura proporciona l'import de la bestreta o avançament utilitzat en aquesta factura. Aquest valor no es pot canviar a la factura. Aquest valor es pot actualitzar a la subquadrícula de la pàgina **Contracte del projecte**. | Aquest camp es pot mostrar al client a la factura impresa per indicar la data en què el client va pagar l'import original de la bestreta o avançament. |
| Import utilitzat | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte**  | Aquest camp de només lectura proporciona el valor calculat que resumeix l'import de la bestreta o avançament que s'ha utilitzat. | Aquest camp es pot mostrar al client a la factura impresa per indicar l'import d'aquesta bestreta o avançament que ja s'ha utilitzat. |
| Import ampliat | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte**  | Aquest camp editable proporciona l'import de la bestreta o avançament que s'està utilitzant en aquesta factura de projecte. Aquest import no pot ser superior al disponible a l'avançament. El sistema ho calcula automàticament com la diferència entre els camps **Import** i **Import utilitzat** a la quadrícula. Podeu reduir aquest import per utilitzar menys del que hi ha disponible però no podeu augmentar l'import per utilitzar més del que hi ha disponible. | Aquest camp es pot mostrar al client a la factura impresa per indicar l'import d'aquesta bestreta o avançament que s'està utilitzant a la factura. |
| Import del saldo de la bestreta. | Quadrícula **Avançaments i bestretes aplicats** a la pàgina **Factura del projecte**  | Aquest camp de només lectura proporciona l'import de bestreta o avançament que quedarà després de confirmar la factura. | Aquest camp es pot mostrar al client en la factura impresa per indicar l'import que quedarà d'aquesta bestreta o avançament després que la factura es confirmi i pagui. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]