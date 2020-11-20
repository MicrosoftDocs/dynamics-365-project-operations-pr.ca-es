---
title: Informació general de les dimensions de preus
description: En aquest tema es proporciona informació sobre les dimensions de preus al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128451"
---
# <a name="pricing-dimensions-overview"></a>Informació general de les dimensions de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les dimensions que s'utilitzen en els recursos humans per configurar els preus i els costos es divideixen en dues categories:

- Persones
- Feina planejada

A causa d'això, hi ha dos tipus de valors de dimensió de preus disponibles:

- **Conjunts d'opcions**: dimensions que són enumeracions fixes per a un conjunt de valors.
- **Valors basats en l'entitat**: dimensions que poden ser un conjunt variat de valors.

## <a name="pricing-dimensions"></a>Dimensions de preus

El Dynamics 365 Project Operations inclou un conjunt per defecte de dimensions de preus. Podeu visualitzar aquestes dimensions de preus anant a **Project Operations** > **Paràmetres**. Al registre de paràmetre, a la pestanya **Dimensions de preus basades en l'import**, comproveu que la funció **msdyn_resourcecategory** i la unitat organitzativa de recursos **msdyn_organizationalunit** tinguin els camps **Aplicable a les vendes** i **Aplicable al cost** definits com a **Sí**. Amb aquests camps habilitats, podeu configurar el preu i el cost de cada combinació de funció i unitat organitzativa.

Si heu de posar un preu o un cost als recursos mitjançant atributs addicionals, podeu crear camps, entitats i dimensions personalitzats.

## <a name="pricing-human-resource-time"></a>Posar preu al temps de recursos humans
Com una organització posa preu al temps de recursos humans és sovint una consideració estratègica important que afecta directament la rendibilitat de l'organització. Treballeu amb els equips de finances i els caps de pràctiques quan la vostra organització estigui a punt per identificar com vol configurar la tarifa de facturació i el cost per al temps de recursos humans.

Altres consideracions sobre el preu inclouen la reutilització de camps o entitats que no són actualment dimensions de preus però que s'apliquen com una dimensió de preus per a la vostra organització. Els camps com ara **Categoria de transacció** (**msdyn_transactioncategory**) i **Recursos que es poden reservar** (**bookableresource**) són exemples de dimensions candidates. 

Tingueu en compte si la dimensió de preus ha de ser una taula o un conjunt d'opcions. Si preveieu canvis dels valors d'una dimensió que excedirà els 10 o 12 i necessiteu atributs addicionals sobre aquests valors, podeu crear una entitat en comptes d'un conjunt d'opcions. El manteniment d'un conjunt d'opcions, com afegir o eliminar valors, requereix un administrador o un desenvolupador, mentre que la majoria d'usuaris poden afegir una fila nova a una taula.

A l'exemple següent es mostren les tarifes de facturació que estan configurades en funció de la funció i de la unitat organitzativa de recursos a la qual pertany el recurs. Els percentatges de costos normalment es basen en la banda de salari de l'empleat i en la unitat organitzativa a la qual pertanyen. En aquest exemple, les taules de tarifes de facturació i de percentatge de cost s'assemblen al següent.

**Tarifes de facturació d'exemple**

| Funció        | Unitat organitzativa    |Unit      |Preu      |Moneda  |
| ------------|-------------|----------|----------:|----------|
| Desenvolupador   | Contoso EUA  |Hour | 200|USD     |
| Desenvolupador   | Contoso India |Hour|   112|USD     |


**Percentatge de costos d'exemple**

| Banda de salari     | Unitat organitzativa    |Unit      |Preu      |Moneda  |
| ----------------|-------------|----------|----------:|----------|
| La meva empresa_banda1 | Contoso EUA  |Hour | 145|USD     |
| La meva empresa_banda2 | Contoso India |Hour|   67|USD     |
