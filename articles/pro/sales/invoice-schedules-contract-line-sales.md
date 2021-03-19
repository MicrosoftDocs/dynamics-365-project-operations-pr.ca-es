---
title: Creació de programacions de facturació en una línia de contracte basada en projecte (bàsic)
description: En aquest tema es proporciona informació sobre la creació de planificacions de factures i fites.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273366"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Creació de programacions de facturació en una línia de contracte basada en projecte (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Podeu adjuntar una planificació de facturació en una línia de contracte basada en projectes. Només es permet la facturació quan es guanya el contracte per crear un contracte de projecte. Les planificacions de factura permeten que es creïn automàticament esborranys de factures per a una línia de contracte basada en projectes. Si teniu previst crear sempre factures manualment, podeu ometre la creació de planificacions de factura en una línia de contracte basada en projectes o en una línia de contracte.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Creació d'una planificació de facturació de temps i material per a una línia de contracte basada en projecte

Quan una línia de contracte basada en el projecte té un mètode de facturació de temps i material, podeu crear una planificació de factures basada en la data. Per generar automàticament una planificació de factura basada en la data, seguiu els passos següents.

1. Aneu a **Configuració** > **Freqüències de factura** per configurar la freqüència de la factura.
2. Obriu el contracte del projecte i, a la pestanya **Resum**, definiu la data de lliurament sol·licitada.
3. Obriu la línia de contracte de temps i material per a la qual voleu crear una planificació de factura basada en la data. 
4. A la pestanya **Planificació de factures**, seleccioneu una data d'inici de facturació i la freqüència de facturació. 
5. A la subquadrícula, seleccioneu **Genera la planificació de facturació**.

    El sistema genera la planificació de factures amb la següent informació de camp:

    - **Data d'execució de la factura** es defineix a la data segons la freqüència de la factura.
    - **Data límit de la transacció** es defineix al dia abans de la **Data d'execució de la factura**.
    - **Estat d'execució** es defineix automàticament a **No executat**. Quan la feina de creació de la factura automàtica s'executa per a una determinada **Data d'execució de la factura**, el camp s'actualitza a **Execució correcta** o **Error d'execució**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Creació d'una planificació de facturació de preu fix per a una línia de contracte basada en projecte

Quan una línia de contracte basada en projectes té un mètode de facturació de preu fix, podeu crear una planificació de factures basada en fites. Completeu els passos següents per generar automàticament una planificació de facturació basada en fites per a un conjunt de fites que es distribuiran equitativament en el període del calendari.

1. Aneu a **Configuració** > **Freqüències de factura** per configurar la freqüència de la factura.
2. Obriu el contracte del projecte i, a la pestanya **Resum**, definiu la data de lliurament sol·licitada.
3. Obriu la línia de contracte de preu fix en la qual heu de crear una planificació de fites. 
4. A la pestanya **Planificació de factures (fites de facturació)**, seleccioneu la data d'inici de facturació i la freqüència de facturació. 
5. A la subquadrícula, seleccioneu **Genera les fites periòdiques**.

    El sistema genera la planificació de factures amb la següent informació de fites.

    - **Nom de la fita** es defineix a la data que està dictada en funció de la freqüència de factura.
    - **Data de la fita** es defineix a la data que està dictada en funció de la freqüència de factura.
    - **Import de la fita** es calcula dividint l'import del contracte a la línia de contracte basada en projectes pel nombre de fites que determinen la freqüència, l'inici de facturació i les dates de lliurament sol·licitades.
    - Si la línia de contracte té un valor en el camp **Import d'impostos estimats** , aquest camp també es divideix en cada fita durant la generació de fites periòdiques.

Les fites de facturació han d'equivaldre el valor contractat de la línia de contracte basada en projectes. Si no són iguals, es produeix un error. Podeu corregir aquest error comprovant que les fites de facturació sumen el valor contractat de la línia creant, editant o suprimint fites. Quan s'hagin fet els canvis, actualitzeu la pàgina.

### <a name="manually-create-milestones"></a>Crear fites manualment

Es poden generar fites de preu fix manualment quan no es divideixen periòdicament. Per crear una fita manualment, completeu els passos següents.

1. Obriu la línia de contracte de preu fix en la qual voleu crear una fita. 
2. A la pestanya **Planificació de factures**, a la subquadrícula, seleccioneu **+ Crea una fita de línia de contracte nova**.
3. Al formulari **Creació de fites**, introduïu la informació necessària segons la taula següent. 

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Nom de la fita | Creació ràpida | Camp de text per al nom de la fita. | Aquest camp s'inclou a la fita de la línia de contracte del projecte i a la factura. |
| Tasca del projecte | Creació ràpida | Si la fita està lligada a una tasca de projecte, utilitzeu aquesta referència per afegir lògica personalitzada i definir l'estat de la fita segons l'estat de la tasca. | No hi ha cap efecte descendent d'aquesta referència a una tasca. |
| Data de la fita | Creació ràpida | Data en què el procés de creació de factures automàtiques hauria de cercar l'estat d'aquesta fita per tenir-la en compte per a la facturació. | S'inclou a la fita de la línia de contracte del projecte i a la factura. |
| Estat de la factura | Creació ràpida | Quan es crea la fita, aquest estat sempre es defineix com a **No preparada per a la facturació** o **No iniciada**. | S'inclou a la fita de la línia de contracte del projecte i a la factura. |
| Import de la línia | Creació ràpida | Import o valor de la fita que es facturarà al client. | Aquest camp s'inclou a la fita de la línia de contracte del projecte i a la factura, |
| Impost | Creació ràpida | Import d'impostos aplicat a la fita. | S'inclou a la fita de la línia de contracte del projecte i a la factura. |

4. Seleccioneu **Desa i tanca**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]