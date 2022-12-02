---
title: 'Novetats de juny del 2022: implementació de la versió bàsica del Project Operations'
description: En aquest article es proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de juny de 2022 de la implementació bàsica del Microsoft Dynamics 365 Project Operations.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031181"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novetats de juny del 2022: implementació de la versió bàsica del Project Operations

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.43.0.77 o 4.43.0.119

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recurs que es pot reservar que no s'emplena amb cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica d'activació del flux de treball per evitar un bucle infinit quan s'actualitzen les tasques de projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades de temps des d'assignacions/reserves han de conservar una referència de recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | La capçalera del document del projecte s'ha de protegir.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per garantir que no es pugui crear un registre de projecte que té caràcters no vàlids al nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtre de la pàgina **Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per evitar que es creïn valors reals de venda facturada si no existeixen valors reals de vendes no facturades de suport. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'especifiqui un nom lògic i s'empleni un nom de camp. |
| Temps i despeses | 2700428 | S'ha millorat la lògica d'aprovació per assegurar que altres conjunts d'aprovació del projecte es puguin processar encara que un dels conjunts d'aprovació estigui encallat en feines del sistema. |
