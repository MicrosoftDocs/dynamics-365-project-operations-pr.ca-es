---
title: "Novetats de l'abril de 2022: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió d'abril de 2022 del Microsoft Dynamics 365 Project Operations per a escenaris basats en recursos/no mantinguts en existències.
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

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.41.0.45
- Administració de projectes i comptabilitat en un entorn del Dynamics 365 Finance, versió 10.0.26

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

Les categories de proveïment es poden utilitzar en comandes de compra de projectes i en factures de proveïdors pendents. Per obtenir més informació, vegeu [Utilitzar les categories de proveïment amb comandes de compra de projectes i factures de proveïdors pendents](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

A la taula següent es mostren les assignacions de doble escriptura que s'han modificat o afegit a la versió de març de 2022 del Project Operations.

| Assignació d'entitats | Versió actualitzada | Comentaris |
| -------------- | ------------------- | ------------|
| Entitat d'exportació de la línia de factura del proveïdor del projecte de la integració del Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Aquesta assignació admet l'ús de categories de proveïment amb comandes de compra i factures de proveïdors pendents. |

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu visualitzar la versió activa de l'assignació a la columna **Versió** de la pàgina **Escriptura doble**. Per activar una versió nova de l'assignació, seleccioneu **Versions de l'assignació de la taula**, seleccioneu la versió més recent i després deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema quan inicieu l'assignació, seguiu les instruccions de la secció [Problemes de columnes de la taula que falten](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de detecció d'errors de doble escriptura.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| ------------ | ---------------- | -------------- |
| Temps i despeses | 2573900 | La característica **Aprovació moderna** ha d'estar habilitada per defecte. |
| Facturació i preus | 2603313 | S'ha corregit un error de registre duplicat que impedia que s'afegissin línies d'oferta i de contracte que tenien un producte. |
| Implementació i configuració | 2611368 | Els clients han de poder afegir fins a cinc entitats personalitzades a la solució utilitzant el dissenyador d'aplicacions modern. |
| Temps i despeses | 2628285 | S'ha corregit un problema que afectava la capacitat de definir la categoria de recursos correcta durant la importació d'entrades de temps. |
|   Administració d'oportunitats| 2628815 | Actualitzeu el límit de caràcters de la descripció dels detalls de la línia d'oferta per tal que coincideixi amb el límit de caràcters del tema de la tasca, de manera que la importació es faci correctament per a les tasques en què el tema tingui una llargada de més de 100 caràcters. |
| Temps i despeses| 2629547 | El camp **Enviat per** de les aprovacions de projecte ha d'assenyalar a l'usuari que ha enviat el registre. |
| Temps i despeses| 2629865 | Camp **Copia la categoria** a les tasques en copiar els projectes. |
| Temps i despeses| 2636463 | S'han corregit els filtres de les aprovacions als formularis d'aprovació moderns. |
| Planificació i seguiment de projectes | 2648300 | S'ha corregit un problema que impedia que es canviés el propietari del projecte. |
| Facturació i preus | 2563000 | No s'han de permetre les línies del llibre diari d'una venda no facturada si la moneda és diferent de la moneda del contracte. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

Per obtenir informació sobre les correccions d'errors incloses en aquesta actualització, inicieu la sessió al Microsoft Dynamics Lifecycle Services (LCS) i vegeu l'[article de la KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
