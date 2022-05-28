---
title: "Novetats de l'abril de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió d'abril de 2022 de Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos / no emmagatzemats.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613317"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de l'abril de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.41.0.45 d'operacions del projecte en una Dataverse versió d'entorn
- Gestió de projectes i comptabilitat en un entorn Dynamics 365 Finance versió 10.0.26

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

Les categories d'adquisició es poden utilitzar en ordres de compra de projectes i factures pendents de proveïdor. Per obtenir més informació, vegeu [Utilitzar les categories d'adquisició amb ordres de compra de projectes i factures pendents de proveïdor](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

La taula següent mostra els mapes de doble escriptura que s'han modificat o afegit a la versió de març de 2022 de Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| -------------- | ------------------- | ------------|
| Project Operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Aquest mapa admet l'ús de categories de contractació amb ordres de compra i factures pendents de proveïdor. |

Executeu sempre la versió més recent del mapa al vostre entorn i habiliteu tots els mapes de taula relacionats a mesura que actualitzeu la solució d'operacions Dataverse de projecte i la versió de la solució de finançament. És possible que algunes funcions i capacitats no funcionin correctament si l'última versió del mapa no està activada. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si has personalitzat un mapa de taula fora de caixa, torna a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si trobeu un problema quan inicieu el mapa, seguiu les instruccions del problema de columnes de la [taula que falten a la secció mapes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de resolució de problemes de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| ------------ | ---------------- | -------------- |
| Temps i despeses | 2573900 | La **característica Aprovació** moderna s'ha d'habilitar per defecte. |
| Facturació i preus | 2603313 | S'ha corregit un error de registre duplicat que ha impedit que s'hagin afegit les línies d'oferta i de contracte que tenen un producte. |
| Implementació i configuració | 2611368 | Els clients han de poder afegir fins a cinc entitats personalitzades a la solució mitjançant el dissenyador d'aplicacions modern. |
| Temps i despeses | 2628285 | S'ha corregit un problema que afectava la capacitat d'establir la categoria de recursos correcta durant la importació d'entrada de temps. |
|   Administració d'oportunitats| 2628815 | Actualitzeu el límit de caràcters de la descripció del detall de la línia d'oferta perquè coincideixi amb el límit de caràcters del tema de la tasca, de manera que la importació tingui èxit per a tasques on el tema tingui més de 100 caràcters. |
| Temps i despeses| 2629547 | El **camp Enviat per** les aprovacions del projecte ha d'apuntar a l'usuari que ha enviat el registre. |
| Temps i despeses| 2629865 | El **camp Copia la categoria** a les tasques quan es copien els projectes. |
| Temps i despeses| 2636463 | S'han corregit els filtres de les aprovacions en formularis d'aprovació moderns. |
| Planificació i seguiment de projectes | 2648300 | S'ha solucionat un problema que impedeix que es canviï el propietari del projecte. |
| Facturació i preus | 2563000 | No s'han de permetre les línies de diari per a una venda nobilificada en què la moneda difereixi de la moneda del contracte. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestió de projectes i comptabilitat en Dynamics 365 Finance

Per obtenir informació sobre les correccions d'errors que s'inclouen en aquesta actualització, inicieu la sessió a Microsoft Dynamics Lifecycle Services (LCS) i visualitzeu l'article de la [KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
