---
title: "Novetats de l'abril de 2021: implementació bàsica del Project Operations"
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'abril de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009384"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Novetats de l'abril de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.9.0.221 

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Materials no mantinguts en existències per als projectes. Les capacitats principals són:
  - Estimar i calcular preus de materials no mantinguts en existències durant el cicle de venda d'un projecte. Per obtenir més informació, vegeu [Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsica)](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Fer el seguiment de l'ús de materials no mantinguts en existències durant el lliurament del projecte. Per obtenir més informació, vegeu [Registre de l'ús de materials als projectes i les tasques de projecte](../../material/material-usage-log.md).
  - Facturació amb costos de materials no mantinguts en existències. Per obtenir més informació, vegeu [Administració del treball pendent de facturació: bàsica](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Les noves API del Dynamics 365 Dataverse permeten crear, actualitzar i suprimir operacions amb **Entitats de planificació**. Per obtenir més informació, vegeu [Ús de les API de planificació per realitzar operacions amb entitats de Planificació](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2224568 | S'ha afegit lògica per permetre personalitzacions que impliquen la invocació del complement de confirmació de la factura. |
| Facturació i preus | 2101098 | S'ha millorat la lògica dels camps per defecte a la factura proforma: **Adreça de facturació**, **Nom de facturació** i **Condicions de pagament** ara tenen com a valors per defecte els del registre de client de contracte de projecte corresponent. |
| Facturació i preus | 2021413 | S'han actualitzat els camps **Cost real** i **Vendes** de l'entitat **Tasca** per incloure els valors de vendes de les despeses no facturades i facturades en les tasques. |
| Facturació i preus | 2182110 | Quan es copia un contracte de projecte, l'identificador de línia de contracte es torna a generar al contracte del projecte de destinació per assegurar que és únic. |
| Administració d'oportunitats | 2186741 | S'han afegit validacions per assegurar que el camp **Origen** i el **Tipus de transacció** no es poden actualitzar en els detalls de la línia d'oferta existent. |
| Administració d'oportunitats | 2191353 | Les fites no s'han de crear en una línia de contracte de temps i material. |
| Administració d'oportunitats | 2216956 | Problemes corregits amb **Actualitza els preus**. |
| Planificació i seguiment | 2182979 | La funció de còpia del projecte s'ha millorat per garantir que les línies de previsió de la despesa es copien del projecte original. |
| Planificació i seguiment | 2184144 | La funció de còpia del projecte s'ha millorat per garantir que el nom de posició del recurs es copia del projecte original. |
| Planificació i seguiment | 2184799 | Còpia del projecte: s'ha millorat el control per assegurar que la data d'inici prevista no es pot canviar quan la còpia està en curs. |
| Planificació i seguiment | 2185134 | Còpia del projecte: la data d'inici prevista per al projecte de destinació es defineix com la data d'avui. |
| Planificació i seguiment | 2196373 | Còpia del projecte: assegureu-vos que els registres de l'administrador del projecte i dels membres de l'equip no estan duplicats a l'equip del projecte. |
| Planificació i seguiment | 2211833 | Còpia del projecte: les assignacions de recursos es copien des de la tasca de projecte d'origen al projecte de destinació. |
| Planificació i seguiment | 2186541 | Es solucionen problemes a la quadrícula **Estimacions** en agrupar per recurs. |
| Planificació i seguiment | 2166906 | La categoria de transacció d'una tasca s'ha de copiar a l'entitat **Assignació de recursos**. |
| Administració de recursos | 2125362 | S'han corregit problemes a l'hora de crear un membre de l'equip genèric utilitzant un mètode basat en hores. |
| Temps i despesa | 2113603 | S'ha corregit el problema relacionat amb la personalització en suprimir atributs de la pàgina **Entrada de temps**. Ara, el sistema comprova si l'atribut existeix a la pàgina abans d'accedir-hi mitjançant un script. |
| Temps i despesa | 2204377 | Els fulls d'hores copiats s'han de mostrar automàticament quan seleccioneu **Copia la setmana** durant l'entrada de l'hora. |
| Temps i despesa | 2209059 | El camp **Estat** es pot editar per a les entrades de temps del Dynamics 365 Field Service. |
