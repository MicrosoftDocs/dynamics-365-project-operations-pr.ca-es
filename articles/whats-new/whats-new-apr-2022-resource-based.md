---
title: "Novetats de l'abril de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'abril de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110872"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de l'abril de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.41.0.45
- Administració i comptabilitat de projectes en un entorn Dynamics 365 Finance versió 10.0.26

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

Les categories de contractació es poden utilitzar en comandes de compra de projectes i factures de proveïdors pendents. Per obtenir més informació, vegeu [Utilitzar categories de contractació amb ordres de compra de projectes i factures de proveïdors pendents](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La taula següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió de març de 2022 de Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| -------------- | ------------------- | ------------|
| Project Operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Aquest mapa admet l'ús de categories d'aprovisionament amb comandes de compra i factures pendents de proveïdor. |

Executeu sempre la versió més recent del mapa al vostre entorn i activeu tots els mapes de taula relacionats a mesura que actualitzeu la versió de la solució Project Operations Dataverse i la versió de la solució Finance. És possible que algunes funcions i capacitats no funcionin correctament si la versió més recent del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat un mapa de taula estàndard, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema en iniciar el mapa, seguiu les instruccions del problema Falten columnes de taula a la [secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| ------------ | ---------------- | -------------- |
| Temps i despeses | 2573900 | La **funció Aprovació** moderna ha d'estar habilitada per defecte. |
| Facturació i preus | 2603313 | S'ha corregit un error de registre duplicat que impedia afegir línies de pressupost i contracte que tenen un producte. |
| Implementació i configuració | 2611368 | Els clients han de poder afegir fins a cinc entitats personalitzades a la solució mitjançant el dissenyador d'aplicacions modern. |
| Temps i despeses | 2628285 | S'ha solucionat un problema que afectava la possibilitat d'establir la categoria de recursos correcta durant la importació d'entrades de temps. |
|   Administració d'oportunitats| 2628815 | Actualitzeu el límit de caràcters de la descripció detallada de la línia de cotització perquè coincideixi amb el límit de caràcters del tema de la tasca, de manera que la importació tingui èxit per a les tasques en què el tema tingui més de 100 caràcters. |
| Temps i despeses| 2629547 | El **camp Enviat per** aprovacions de projectes ha d'assenyalar a l'usuari que ha enviat el registre. |
| Temps i despeses| 2629865 | El **camp Copia la categoria** de les tasques quan es copien els projectes. |
| Temps i despeses| 2636463 | S'han corregit els filtres de les aprovacions als formularis d'aprovació moderns. |
| Planificació i seguiment de projectes | 2648300 | S'ha solucionat un problema que impedeix canviar el propietari del projecte. |
| Facturació i preus | 2563000 | No s'han de permetre línies de diari per a una venda no autoritzada on la moneda difereixi de la moneda del contracte. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració i comptabilitat de projectes en Dynamics 365 Finance

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article [de la](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864) KB.
