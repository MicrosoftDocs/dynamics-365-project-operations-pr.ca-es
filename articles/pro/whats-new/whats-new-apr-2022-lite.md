---
title: "Novetats de l'abril de 2022: implementació bàsica del Project Operations"
description: En aquest article es proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió d'abril de 2022 de la implementació bàsica del Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 6d6fc52d535244b339e43f88e85797a957d98b89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927454"
---
# <a name="whats-new-april-2022---project-operations-lite-deployment"></a>Novetats de l'abril de 2022: implementació bàsica del Project Operations

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.41.0.45

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
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
