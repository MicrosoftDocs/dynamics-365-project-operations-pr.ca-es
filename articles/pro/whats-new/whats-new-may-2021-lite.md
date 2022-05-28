---
title: 'Novetats del maig de 2021: implementació bàsica del Project Operations'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de maig de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 854a8c2290281b4d11a045321a334d8866806041
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583664"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Novetats del maig de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

   - Project Operations en l'entorn del Dataverse versió 4.10.0.186.

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- [Modes de planificació](../../project-management/scheduling-modes.md): els administradors de projectes ara poden definir si un projecte s'ha d'administrar amb el mode de planificació de duració fixa, treball fix o unitats fixes.

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2224568 | S'ha afegit lògica per permetre personalitzacions que impliquen la invocació del complement de confirmació de la factura. |
| Facturació i preus | 2101098 | S'ha millorat la lògica dels camps per defecte a la factura proforma. Aquests camps inclouen, **Adreça de facturació**, **Nom de facturació** i **Termes de pagament**. Ara, els camps són per defecte el registre de client de contracte del projecte corresponent. |
| Facturació i preus | 2021413 | S'han actualitzat els camps **Cost real** i **Vendes** de l'entitat **Tasca** per incloure els valors de vendes de les despeses no facturades i facturades en les tasques. |
| Facturació i preus | 2182110 | Quan es copia un contracte de projecte, l'identificador de línia de contracte es torna a generar al contracte del projecte de destinació per assegurar que és únic. |
| Administració d'oportunitats | 2186741 | S'han afegit validacions per assegurar que el camp **Origen** i el tipus de transacció no es poden actualitzar en els detalls de la línia d'oferta existent. |
| Administració d'oportunitats | 2191353 | La creació de fites no s'han de permetre en una línia de contracte de temps i material. |
| Administració d'oportunitats | 2216956 | Problemes corregits amb **Actualitza els preus**. |
| Planificació i seguiment | 2182979 | La funció de còpia del projecte s'ha millorat per garantir que les línies de previsió de la despesa es copien del projecte original. |
| Planificació i seguiment | 2184144 | La funció de còpia del projecte s'ha millorat per garantir que el nom de posició del recurs es copia del projecte original. |
| Planificació i seguiment | 2184799 | S'ha millorat el control en copiar un projecte per assegurar que la data d'inici prevista no es pot canviar quan la còpia està en curs. |
| Planificació i seguiment | 2185134 | Durant la còpia d'un projecte, la data d'inici prevista per al projecte de destinació es defineix a la data d'avui. |
| Planificació i seguiment | 2196373 | S'assegura que els registres de l'administrador del projecte i dels membres de l'equip no estan duplicats a l'equip del projecte en copiar un projecte. |
| Planificació i seguiment | 2211833 | Les assignacions de recursos es copien des de la tasca de projecte d'origen al projecte de destinació. |
| Planificació i seguiment | 2186541 | Es solucionen problemes a la quadrícula **Estimacions** en agrupar per **recurs**. |
| Planificació i seguiment | 2166906 | La categoria de transacció d'una tasca s'ha de copiar a l'entitat **Assignació de recursos**. |
| Administració de recursos | 2125362 | S'han corregit problemes a l'hora de crear un membre de l'equip genèric utilitzant un mètode basat en hores. |
| Temps i despesa | 2113603 | S'ha corregit el problema relacionat amb la personalització en suprimir atributs de la pàgina **Entrada de temps**. El sistema comprova si l'atribut existeix a la pàgina abans d'accedir a l'atribut mitjançant un script. |
| Temps i despesa | 2204377 | Els fulls d'hores copiats s'han de mostrar automàticament quan seleccioneu **Copia la setmana**. |
| Temps i despesa | 2209059 | El camp **Estat** es pot editar per a les entrades de temps del Dynamics 365 Field Service. |
