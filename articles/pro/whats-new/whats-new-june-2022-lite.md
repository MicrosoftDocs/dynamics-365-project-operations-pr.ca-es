---
title: 'Novetats de juny del 2022: implementació de la versió bàsica del Project Operations'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juny de 2022 de la implementació del Microsoft Dynamics 365 Project Operations lite.
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

Aquest article s'aplica als components i versions de Microsoft Dynamics 365 Project Operations següents:

- Project Operations en una Dataverse versió d'entorn 4.43.0.77 o 4.43.0.119

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Subcontractació | 2708885 | S'ha corregit el missatge d'error que apareix quan un usuari crea un registre de capçalera de reserva de recursos que es pot reservar on no s'emplena cap recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2629441 | S'ha corregit la lògica d'activació del flux de treball per ajudar a evitar un bucle infinit quan s'actualitzen les tasques del projecte. |
| Temps i despeses | 2641209 | Les importacions d'entrades de temps de les tasques/reserves han de conservar una referència de recurs que es pot reservar. |
| Planificació i seguiment de projectes | 2651148 | S'ha de custodiar la capçalera del document del projecte.|
| Planificació i seguiment de projectes | 2653145 | S'han afegit validacions per garantir que no es pugui crear un registre de projecte que tingui caràcters no vàlids al seu nom. |
| Temps i despeses | 2654710 | S'ha corregit el filtratge a la **pàgina Aprovacions**. |
| Facturació i preus | 2667805 | S'han afegit validacions per ajudar a evitar que es creïn reals de venda facturats si no existeixen còpies de seguretat reals de vendes no regulades. |
| Facturació i preus | 2668378 | S'han afegit validacions per evitar que s'afegeixi una dimensió de preus personalitzada tret que s'empleni un nom lògic i un nom de camp. |
| Temps i despeses | 2700428 | S'ha millorat la lògica d'aprovacions per garantir que es puguin tramitar altres conjunts d'aprovació del projecte encara que un dels conjunts d'aprovació estigui encallat en els treballs del sistema. |
