---
title: 'Novetats de novembre de 2021: implementació bàsica del Project Operations'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que hi ha disponibles a la implementació bàsica de la versió de novembre de 2021 del Project Operations.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 947e7f6183ddeef3ab9a88d140331956bbcf23bd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913792"
---
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novetats de novembre de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Les interfícies de programació d'aplicacions (API) de Planificació de projectes admeten ara la capacitat de crear i suprimir conjunts de projectes

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-in-dataverse"></a>Project Operations al Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2358236 | La correcció de factures ha de permetre correccions que tinguin línies de preu zero. |
| Administració de recursos | 2410072 | Permetre la configuració d'un recurs que s'ha assignat a la tasca com a administrador del projecte. |
| Facturació i preus | 2430234 | Corregir un problema de càlcul del rendiment de cost. |
| Temps i despesa | 2436978 | Permetre que s'introdueixi l'hora en format hh:mm. |
| Facturació i preus | 2448623 | Permetre que les llistes de preus s'actualitzin després que s'associïn a una unitat organitzativa. |
| Temps i despesa | 2460396 | Permetre suprimir una entrada de temps esborrant la cel·la. |
| Facturació i preus | 2467386 | Permetre suprimir un projecte que té una tasca, encara que la tasca estigui associada a una oferta guanyada. |
| Temps i despesa | 2461744 | La visualització **La meva aprovació fallida** només conté les aprovacions del projecte de la fase **Enviat**. |
| Temps i despesa | 2464082 | Suprimir l'enllaç de les aprovacions del projecte a l'aprovació definida quan coincideix amb un estat de destinació. |
| Temps i despesa | 2468108 | La feina de planificació no ha de definir un estat de **Processament** per al conjunt d'aprovació. |
| Temps i despesa | 2471503 | Suprimir conjunts d'aprovació que tenen set dies d'antiguitat. |
| Facturació i preus | 2480687 | La referència de la línia d'oferta no s'ha d'eliminar quan es crea una fita de línia d'oferta. |
