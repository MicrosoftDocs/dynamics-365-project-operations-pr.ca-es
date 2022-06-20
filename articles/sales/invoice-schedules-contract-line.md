---
title: Creació d'una programació de facturació en una línia de contracte basada en projecte
description: En aquest article s'ofereix informació sobre com crear planificacions de factures i fites a les línies de contracte.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914988"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Creació d'una programació de facturació en una línia de contracte basada en projecte 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Podeu afegir una planificació de factures a una línia de contracte basada en projectes. La facturació només es permet després de guanyar el contracte i que creeu un contracte de projecte. Una planificació de factures permet crear automàticament esborranys de factures per a una línia de contracte basada en projectes. No obstant això, si només creeu factures manualment, podeu ometre la creació de factures en línies de contracte.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Crear una planificació de factures de temps i material per a una línia de contracte

Quan una línia de contracte basada en el projecte té un mètode de facturació de temps i material, podeu crear una planificació de factures basada en la data. Per generar automàticament una planificació de factura basada en la data, seguiu els passos següents.

1. Aneu a **Configuració** > **Freqüències de facturació** i configureu una freqüència de facturació.
2. Aneu al registre del contracte del projecte i, en el camp **Resum**, en la pestanya **Data de lliurament sol·licitada**, seleccioneu una data.
3. Obriu la línia de contracte **Temps i material** per a la qual esteu creant la planificació de factures basada en la data. 
4. A la pestanya **Planificació de la factura**, seleccioneu la data d'inici de facturació i la freqüència de facturació.
5. A la subquadrícula, seleccioneu **Genera la planificació de facturació**. La planificació de facturació es genera amb els camps **Data d'execució de la factura**, **Data límit de la transacció** i **Estat d'execució** definits de la següent manera:

    - **Data d'execució de la factura** aquesta data ve dictada per la freqüència de la factura.
    - **Data límit de la transacció**: dia abans de la data d'execució de la factura.
    - **Estat d'execució**: es defineix automàticament a **No executat**. Quan la feina de creació de la factura automàtica s'executa per a una determinada data d'execució de la factura, el camp s'actualitza a **Execució correcta** o **Error d'execució**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Crear una planificació de factura de preu fix per a una línia de contracte

Quan la línia de contracte té un mètode de facturació fix, es pot crear una planificació de factures basada en fites. 

> [!NOTE]
> Les fites no es poden crear en una línia de contracte si no hi ha cap projecte assignat a la línia de contracte.

Completeu els passos següents per generar una planificació de factures basada en fites per a un conjunt fix de fites distribuïdes de manera equitativa per al període de calendari.

1. Aneu a **Configuració** > **Freqüències de facturació** i configureu una freqüència de facturació.
2. Aneu al registre del contracte del projecte i, en el camp **Resum**, en la pestanya **Data de lliurament sol·licitada**, seleccioneu una data.
3. Obriu la línia de contracte **Preu fix** per a la qual esteu creant la planificació de les fites. A la pestanya **Fites de facturació**, seleccioneu la data d'inici de facturació i la freqüència de la factura. 
4. A la subquadrícula, seleccioneu **Genera les fites periòdiques**. La planificació de la factura es genera amb els camps **Nom de la fita**, **Data de la fita** i **Import de la fita** definits de la manera següent:

    - **Nom de la fita**: Aquest nom està dictat per la freqüència de la factura.
    - **Data de la fita**: aquesta data ve dictada per la freqüència de la factura.
    - **Import de la fita**: aquest import es calcula dividint l'import del contracte en la línia de contracte pel nombre de fites dictades per la freqüència, l'inici de facturació i les dates de lliurament sol·licitades.

    Si la línia de contracte té un valor en el camp **Import d'impostos estimat**, llavors aquest camp també es reparteix a cada fita per igual quan es generen fites periòdiques.

Les fites de facturació han d'igualar el valor contractat de la línia de contracte. Si no ho fan, rebreu un error a la pàgina **Línia de contracte**. Podeu esmenar l'error verificant que les fites de facturació sumin en total el valor contractat de la línia creant, editant o suprimint fites. Després dels canvis, actualitzeu la pàgina per eliminar l'error.

### <a name="manually-create-milestones"></a>Crear fites manualment

Podeu generar manualment fites de preu fix quan no es divideixen periòdicament. Completeu els passos següents per crear manualment una fita.

1. Obriu la línia de contracte de preu fix per a la qual esteu creant una fita i, a la pestanya **Planificació de facturació**, a la subquadrícula, seleccioneu **+ Crea una nova fita de línia de contracte**. 
2. A la pàgina **Creació de fita**, introduïu la informació necessària en funció de la taula següent.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Nom de la fita | Creació ràpida | Camp de text per al nom de la fita. | Es transfereix a la fita de la línia de contracte del projecte i a la factura. |
| Tasca del projecte | Creació ràpida | Si la fita està lligada a una tasca del projecte, utilitzeu aquesta referència per afegir una lògica personalitzada per definir l'estat de la fita segons l'estat de la tasca. | L'aplicació no té cap efecte descendent d'aquesta referència a una tasca. |
| Data de la fita | Creació ràpida | Definiu la data en què el procés de creació de la factura automàtica hauria de cercar l'estat d'aquesta fita per considerar-la per a la facturació. | Es transfereix a la fita de la línia de contracte del projecte i a la factura. |
| Estat de la factura | Creació ràpida | Quan es crea una fita, aquest estat sempre s'estableix a **No està a punt per a la facturació** o **No s'ha començat**. | Es transfereix a la fita de la línia de contracte del projecte i a la factura. |
| Import de la línia | Creació ràpida | Import o valor de la fita que es facturarà al client. | Es transfereix a la fita de la línia de contracte del projecte i a la factura. |
| Impost | Creació ràpida | Import d'impostos aplicat a la fita. | Es transfereix a la fita de la línia de contracte del projecte i a la factura. |

3. Seleccioneu **Desa i tanca**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]