---
title: "Novetats d'agost del 2021: implementació de la versió bàsica del Project Operations"
description: En aquest tema es proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'agost de 2021 de la implementació bàsica del Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3cb6f92bfb28dc64f0f689e0070b0506644c2320
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586424"
---
# <a name="whats-new-august-2021---project-operations-lite-deployment"></a>Novetats d'agost del 2021: implementació de la versió bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.13.0.152

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- **Conjunts d'aprovació**: els conjunts d'aprovació agrupen sol·licituds d'aprovació de temps, despeses o ús de materials en subconjunts d'operacions més petits. Aquest agrupament permet processar les aprovacions en un ordre específic per projecte i tornar a provar i seqüenciar. L'agrupació de les sol·licituds millora la fiabilitat i la traçabilitat del processament d'aprovacions per a grans volums d'aprovacions. Per obtenir més informació, [Conjunts d'aprovació](../../approvals/approval-sets.md).

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2295625 | La fita s'ha de copiar des de la planificació de facturació al detall de la línia de factura. |
| Facturació i preus | 2316323 | El descompte no s'ha de poder editar en una factura proforma al Project Operations per a escenaris basats en recursos. |
|   Administració d'oportunitats | 2338619 | Les regles de negocis **Oportunitat** i **Oferta** només s'han d'invocar a les pàgines. |
| Administració de recursos | 2316523 | L'ús d'**Envia la sol·licitud** d'un requisit de recursos que té una funció adjunta no hauria de mostrar un error. |
| Administració de recursos | 2326885 | La creació d'un requisit de recursos a través d'un projecte no hauria de mostrar un error. |
| Temps i despeses | 2335584 | Fluxos de tasca obsolets a l'entrada de temps. |
| Temps i despeses | 2336884 | El botó **Copia l'hora de la setmana** ha de funcionar per a més que l'usuari actual. |
