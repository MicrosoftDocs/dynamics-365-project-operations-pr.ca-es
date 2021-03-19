---
title: Planificacions de facturació en línies d'oferta basades en projectes
description: En aquest tema es proporciona informació sobre la creació e planificacions i fites de facturació per a línies d'oferta.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 506de5217de48814d6b8f03a10c7c8648c575198
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278271"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a>Planificacions de facturació en línies d'oferta basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Una línia d'oferta basada en projectes proporciona la capacitat d'expressar una planificació de factura. Això és opcional durant la fase d'oferta perquè l'aplicació no admet la facturació d'un projecte quan està lligat a una línia d'oferta. Només es permet la facturació després de guanyar l'oferta. L'únic impacte descendent de la creació d'una planificació de factura durant la fase d'oferta és que aquesta planificació de factura es copiarà a la línia de contracte basada en projectes. Si no creeu cap planificació de factura durant la fase d'oferta, podreu fer-ho en la línia de contracte basada en projectes.

En general, la finalitat de les planificacions de factura és permetre la creació automàtica d'esborranys de factures per a una línia de contracte basada en projectes. 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a>Crear una planificació de factura de temps i materials per a una oferta basada en projectes

Quan el mètode de facturació d'una línia d'oferta basada en projectes és de temps i material, el sistema genera una planificació de factura basada en la data. Per generar automàticament una planificació de factura basada en la data, seguiu els passos següents.

1. Aneu a **Configuració** > **Freqüències de factura** i configureu una freqüència de factura.
2. A la pàgina **Ofertes**, obriu l'oferta del projecte i, a la pestanya **Resum**, definiu una data de lliurament sol·licitada.
3. Obriu la línia d'oferta de temps i material per a la qual heu de crear una planificació de factura basada en la data. 
4. A la pestanya **Planificació de factures**, seleccioneu valors als camps **Inici de la facturació** i **Freqüència de facturació**. 
5. A la subquadrícula, seleccioneu **Genera la planificació de facturació**.
6. L'aplicació genera la planificació de la factura amb els camps **Data d'execució de la factura**, **Data límit de la transacció** i **Estat d'execució** definits de la següent manera:

    - **Data d'execució de la factura** es defineix a la data que s'especifica a partir de la freqüència de la factura.
    - **Data límit de la transacció** es defineix al dia abans de la **Data d'execució de la factura**.
    - **Estat d'execució** es defineix automàticament a **No executat**. Quan la feina de creació de la factura automàtica s'executa per a una determinada data d'execució de la factura, s'actualitzarà aquest camp a **Execució correcta** o **Error d'execució**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a>Crear una planificació de factura de preu fix per a una línia d'oferta basada en projectes

Quan la línia d'oferta basada en projectes té un mètode de facturació **Fix**, el sistema crea una planificació de factura basada en fites. Completeu els passos següents per generar automàticament aquesta planificació per a un conjunt fix de fites que es distribueixen de manera equitativa per al període de calendari.

1. Aneu a **Configuració** > **Freqüències de factura** i configureu una freqüència de factura.
2. A la pàgina **Ofertes**, obriu l'oferta del projecte i, a la pestanya **Resum**, definiu una data de lliurament sol·licitada.
3. Obriu la línia d'oferta de preu fix per a la qual heu de crear una planificació de fites. 
4. A la pestanya **Planificació de factures**, seleccioneu valors als camps **Inici de la facturació** i **Freqüència de facturació**. 
5. A la subquadrícula, seleccioneu **Genera les fites periòdiques**.
6. L'aplicació genera la planificació de factura amb un nom, una data i una quantitat de fites.

    - El nom de la fita es defineix a la data que s'especifica a partir de la freqüència de la factura.
    - La data de la fita es defineix a la data que s'especifica a partir de la freqüència de la factura.
    - L'import de la fita es calcula dividint l'import de l'oferta a la línia d'oferta basada en el projecte pel nombre de fites que dicten la freqüència i les dates d'inici de la facturació i d'entrega sol·licitades.
    - Si la línia d'oferta també té un import d'impostos previst, aquest valor es divideix entre cada fita de manera equitativa en generar fites periòdiques.

### <a name="manually-create-milestones"></a>Crear fites manualment

Les fites de preu fix també es poden generar manualment quan no es divideixen periòdicament. Per crear una fita manualment:

Obriu la línia d'oferta de preu fix en què heu de crear una fita. A la pestanya **Planificació de factures**, a la subquadrícula, seleccioneu **+ Crea una nova fita de línia d'oferta** i introduïu la informació necessària segons la taula següent.

| **Camp** | **Ubicació** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Nom de la fita | Creació ràpida | Nom de la fita. | Es propaga a la fita de la línia de contracte del projecte i a la factura |
| Tasca del projecte | Creació ràpida | Si la fita està lligada a una tasca del projecte, podeu utilitzar aquesta referència per afegir una lògica personalitzada per definir l'estat de la fita segons l'estat de la tasca. | L'aplicació no té cap efecte descendent d'aquesta referència a una tasca. |
| Data de la fita | Creació ràpida | Definiu la data en què el procés de creació de la factura automàtica hauria de cercar l'estat d'aquesta fita per considerar-la per a la facturació. | Es propaga a la fita de la línia de contracte del projecte i a la factura. |
| Estat de la factura | Creació ràpida | Quan es crea una fita, aquest estat sempre es defineix com a **No preparat per a la facturació**. | Es propaga a la fita de la línia de contracte del projecte i a la factura. |
| Import de la línia | Creació ràpida | Import o valor de la fita que es facturarà al client. | Es propaga a la fita de la línia de contracte del projecte i a la factura. |
| Impost | Creació ràpida | Import de l'impost que s'aplicarà a la fita. | Es propaga a la fita de la línia de contracte del projecte i a la factura. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]