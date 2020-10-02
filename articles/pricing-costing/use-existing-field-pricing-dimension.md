---
title: Camps del Project Operations com a dimensions de preus
description: En aquest tema es proporciona informació sobre l'ús de camps com a dimensions de preus al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 3ddf3098e45fdc9b99067b64df05e2adc0b6ad05
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896404"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a>Camps del Project Operations com a dimensions de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

L'entitat **Valors reals** té diversos camps que es poden utilitzar com a dimensions de preus per a la fixació de preus basats en recursos. Per exemple, un camp comú és un **Recurs que es pot reservar**. Les empreses més petites que tenen menys de 20-30 recursos facturables poden trobar que tenir taxes de factura i cost específiques per a cada recurs és una aproximació més simple. No obstant això, a mesura que la força de treball creix, podria ser poc realista mantenir tarifes específiques per recurs. El cost dels recursos i les tarifes de facturació comencen a variar a mesura que els recursos reben ascensos, guanyen més experiència o adquireixen un conjunt d'habilitats diferent. 

Un altre exemple és el de la categoria de transacció. Els clients i els executors han utilitzat la categoria de transacció per classificar el treball i utilitzen el camp per posar el preu i el cost basat en la categoria de treball.
