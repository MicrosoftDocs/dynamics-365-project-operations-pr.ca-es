---
title: 'Novetats de juny del 2021: implementació de la versió bàsica del Project Operations'
description: En aquest tema es proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juny de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 06ea83152e4f601ef842a0f8d975c16c2be95612
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583894"
---
# <a name="whats-new-june-2021---project-operations-lite-deployment"></a>Novetats de juny del 2021: implementació de la versió bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en un entorn del Dataverse, versió 4.11.0.156 o 4.11.0.164.

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2281417 | S'ha corregit el problema relacionat amb l'error de l'acció de creació automàtica de factures mitjançant la planificació de factures. |
| Facturació i preus | 2287835 |   S'ha millorat el rendiment de la confirmació de factures. |
| Administració d'oportunitats | 2222555 | La imputabilitat de les estimacions dels materials s'ha de copiar correctament als detalls de la línia d'oferta quan s'utilitza **Importa des de l'estimació del projecte**. |
| Administració d'oportunitats | 2223427 | Les personalitzacions es permeten ara per a l'acció **GenerateRetainersFromRetainerScheduleOptions**. |
| Administració d'oportunitats | 2277528 | S'ha corregit el càlcul de valors de fites de facturació per a les línies de contracte de projectes amb diversos clients. |
| Planificació i seguiment de projectes | 2226110 | S'ha corregit el problema intermitent amb la funció **Genera el requisit** a la quadrícula **Equip del projecte**. |
| Planificació i seguiment de projectes | 2208109 | Els usuaris no poden crear un projecte en una moneda amb tasques relacionades en una altra moneda. |
| Planificació i seguiment de projectes | 2258228 | S'ha actualitzat la llista de camps que es poden modificar amb les entitats **Planificació** que utilitzen l'API de planificació. |
| Planificació i seguiment de projectes | 2293989 | La llengua i la configuració regional correctes s'han de passar a la quadrícula **Tasques del projecte**.|
| Administració de recursos | 2220493 | S'ha corregit l'experiència de l'usuari a la quadrícula **Tasca** quan es marca ràpidament una sol·licitud de recurs com a completada. |
| Administració de recursos | 2330496 | S'ha corregit el problema de càrrega del **Tauler de planificació**. (L'actualització de qualitat està disponible a la versió 4.11.0.164) |
| Temps i despesa | 2194431 | La quadrícula **Entrada de temps** ha de tenir l'inici de la setmana definit igual que a la **Configuració del sistema**. |
| Temps i despesa | 2277311 | Després de suprimir el valor d'una cel·la a la quadrícula **Entrada de temps**, el cursor es queda a la quadrícula. |
