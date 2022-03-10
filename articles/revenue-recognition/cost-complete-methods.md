---
title: Mètodes de càlcul de costos per a la finalització
description: En aquest tema es proporciona informació sobre els mètodes que s'utilitzen per calcular el cost per completar un projecte.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fe42ea0e1a5c562ec648fbf2a2924648af80381b9db8ffe0c209cb5247bb2ba2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997954"
---
# <a name="cost-to-complete-methods"></a>Mètodes de càlcul de costos per a la finalització

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest tema es proporciona informació sobre els mètodes que s'utilitzen per calcular el cost per completar un projecte. Hi ha diversos mètodes que podeu utilitzar per calcular el cost per completar un projecte. 

Quan creeu una estimació per a un projecte, a la pàgina **Crear una estimació**, al camp **Mètode de cost per completar**, podeu seleccionar un dels mètodes de cost per completar següents.

| Mètode de cost per completar    | Descripció                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cost total: real            | Introduïu manualment els costos estimats als camps **Cost total** o **Quantitat total** mitjançant el botó **Estimació de costos** a la pàgina **Estimació**. El sistema resta els costos reals dels totals que heu introduït. El total és el cost de completar el projecte. Aquest mètode no utilitza les estimacions de despeses i les assignacions de recursos introduïdes a Project Operations integrat al Microsoft Dataverse. El cost o la quantitat total es pot actualitzar manualment segons calgui.  |
| Previsió total: real        | Les assignacions de recursos i estimacions de despeses s'utilitzen per determinar l'import total previst del projecte. Els costos reals es comparen amb aquesta previsió per calcular el cost que s'ha de completar.                                                                                                                                                                                                                                                                          |
| Com a estimació prèvia         | Els mateixos mètodes d'estimació que es van utilitzar en el període anterior s'utilitzen aquí. Aquest mètode requereix un model de previsió si el període anterior requeria un model de previsió.                                                                                                                                                                                                                                                                                                                           |
| Defineix el cost per completar a zero | Aquest mètode, que normalment s'utilitza abans de suprimir el projecte d'estimació, compara l'estimació total amb les transaccions reals comptabilitzades i esborra la columna **Cost per completar**. Quan es completa, el resultat sempre és del 100 per cent. Per a cada línia de cost que creeu, s'esborra la casella de selecció per a la **Previsió** i es copia l'estimació total de l'estimació de costos anterior. El consum real del període de pressupost es descomptarà del cost per completar el projecte.              |
| Des de la plantilla de cost           | El mètode del cost per completar que s'hagi definit a la plantilla de costos associada amb el projecte d'estimació seleccionat.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]