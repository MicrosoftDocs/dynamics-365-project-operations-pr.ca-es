---
title: Novetats de novembre de 2021 - Desplegament de lite d'operacions de projectes
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de novembre de 2021 de la implementació lite d'operacions del projecte.
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
# <a name="whats-new-november-2021---project-operations-lite-deployment"></a>Novetats de novembre de 2021 - Desplegament de lite d'operacions de projectes

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- Operacions del projecte en una Dataverse versió d'entorn 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
  
## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Les interfícies de programació d'aplicacions de planificació de projectes (API) ara admeten la possibilitat de crear i eliminar cubs del projecte

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-in-dataverse"></a>Operacions del projecte a Dataverse

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2358236 | La correcció de factures ha de permetre correccions que tinguin línies de preu zero. |
| Administració de recursos | 2410072 | Permet la configuració d'un recurs assignat a la tasca com a administrador de projectes. |
| Facturació i preus | 2430234 | Solucionar un problema de càlcul del rendiment dels costos. |
| Temps i despesa | 2436978 | Permet que el temps s'introdueixi en format hh:mm. |
| Facturació i preus | 2448623 | Permet que les llistes de preus s'actualitzin després d'associar-se amb una unitat organitzativa. |
| Temps i despesa | 2460396 | Permet que se suprimeixi una entrada de temps esborrant la cel·la. |
| Facturació i preus | 2467386 | Permet que se suprimeixi un projecte que té una tasca, fins i tot quan la tasca està associada amb una oferta guanyada. |
| Temps i despesa | 2461744 | La **visualització d'aprovació** El meu error només conté aprovacions de projectes a la **fase Enviada**. |
| Temps i despesa | 2464082 | Suprimiu l'enllaç de les aprovacions del projecte al conjunt d'aprovació quan coincideixi un estat de destinació. |
| Temps i despesa | 2468108 | La feina De planificació no ha de definir un **estat de processament** per al conjunt d'aprovació. |
| Temps i despesa | 2471503 | Suprimeix els conjunts d'aprovació que falten set dies. |
| Facturació i preus | 2480687 | La referència de la línia d'oferta no s'ha de suprimir quan es crea una fita de línia d'oferta. |
