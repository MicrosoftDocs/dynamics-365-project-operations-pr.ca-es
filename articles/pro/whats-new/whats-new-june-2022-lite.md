---
title: 'Novetats de juny del 2022: implementació de la versió bàsica del Project Operations'
description: En aquest article s'ofereix informació sobre les actualitzacions de qualitat disponibles a la versió de juny de 2022 de la implementació de Microsoft Dynamics 365 Project Operations lite.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959602"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Novetats de juny del 2022: implementació de la versió bàsica del Project Operations

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.43.0.77 d'operacions del projecte en una Dataverse versió d'entorn

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recurs que es pot reservar on no s'emplena cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica activadora del flux de treball per ajudar a evitar un bucle infinit quan s'actualitzen les tasques del projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades d'hora de les tasques o les reserves han de conservar una referència de recursos que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | Cal protegir la capçalera del document del projecte.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per assegurar-vos que no es pot crear un registre de projecte que tingui caràcters no vàlids al seu nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtratge de la **pàgina Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per ajudar a evitar que es creïn reals de venda facturada si no existeixen còpies de suport de vendes no facturades. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'ompli un nom lògic i un nom de camp. |
| Temps i despeses | 2700428 | S'ha millorat la lògica de les aprovacions per assegurar-se que altres conjunts d'aprovació del projecte es poden processar fins i tot si un dels conjunts d'aprovació està atrapat en les feines del sistema. |
