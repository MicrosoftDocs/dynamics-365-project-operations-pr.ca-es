---
title: "Novetats d'octubre de 2022: implementació bàsica del Project Operations"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'octubre de 2022 de la implementació del Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806721"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Novetats d'octubre de 2022: implementació bàsica del Project Operations

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.57.0.176

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

| Àrea de característiques | Nom de la característica | Més informació |
| --- | --- | --- |
| Planificació i seguiment de projectes | **Planificació externa d'operacions del projecte**<br>El mode de planificació externa permet als clients crear, actualitzar i suprimir de forma nativa entitats relacionades amb les estructures del desglossament del treball (WBS) mitjançant l'ús de les API natives Dataverse , sense els límits actuals que el Project for the Web aplica. | [Programació externa](/dynamics365/project-operations/project-management/external-scheduling) |
| Implementació i configuració | <p>**Permetre als clients triar el tipus d'implementació**<br>Les actualitzacions basades en el producte (PDU) de Project Operations s'utilitzen per instal·lar automàticament la solució de doble escriptura del Project Operations quan s'instal·len solucions de nucli i orquestració de doble escriptura a l'entorn.</p><p>Aquesta característica introdueix un paràmetre de comportament **d'actualització de la solució nou** als paràmetres del projecte. Quan aquest paràmetre només **s'estableix com a** Lite, els PUD ja no instal·laran automàticament la solució Project Operations Dual-write, fins i tot si les solucions de nucli i orquestració de doble escriptura estan instal·lades a l'entorn. Aquest comportament beneficiarà els clients que tinguin previst utilitzar solucions d'escriptura dual per integrar comandes de vendes a les aplicacions de finances i operacions, però vulguin utilitzar Project Operations en mode Lite (és a dir, sense integració a les aplicacions de finances i operacions).</p> | |

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2316317 | El sistema permet crear factures que no tinguin transaccions repercutibles. |
| Facturació i preus | 2737300 | Valideu la disponibilitat dels camps Client abans d'accedir al formulari. |
| Facturació i preus | 2744948 | Afegiu una comprovació nul·la per al mètode de facturació. |
| Facturació i preus | 2763515 | Gestió d'errors de referència nul·la quan falti el contracte de compravenda de la factura. |
| Facturació i preus | 2844301 | La creació de factures per lots falla a causa d'un error. |
| Facturació i preus | 2845869 | Emmagatzematge incorrecte del Servei de l'Organització. |
| Facturació i preus | 2853729 | Els detalls de la funció i del preu s'actualitzen quan es modifica el tipus de facturació. |
| Facturació i preus | 2940350 | Quan els reals tenen un preu, només s'han d'introduir automàticament les llistes de preus actives. |
| Implementació i configuració | 3001206 | L'entitat msdyn\_ replaylogheader està impedint les actualitzacions de les organitzacions de clients. |
| Administració d'oportunitats | 2755582 | Les excepcions de referència nul·les es gestionen a l'ajudant de la regla de facturació dividida. |
| Administració d'oportunitats | 2761477 | Quan s'utilitza la facturació dividida, la supressió d'una fita (capçalera) deixa fites òrfenes. |
| Administració d'oportunitats | 2767595 | Quan s'obre un registre d'ús de material al formulari principal, el recurs que es pot reservar per al registre es canvia a l'usuari que ha iniciat la sessió. |
| Planificació i seguiment de projectes | 2790384 | El temps d'espera pendent d'OperacióSet és massa curt. |
| Administració de recursos | 2751560 | Unitats d'organització preferides inconsistents en requisit de recursos. |
| Subcontractació | 2907231 | La fase de procés de les factures dels proveïdors no es pot avançar. |
| Temps i despesa | 2867363 | Els registres no queden fora de la visualització Absències / Vacances per a l'aprovació quan estan a la cua per a la seva aprovació. |
| Temps i despesa | 2894405 | TESA: El directori POC no utilitzat està causant problemes de compliment. |
