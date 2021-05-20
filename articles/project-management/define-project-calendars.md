---
title: Definició dels calendaris del projecte
description: En aquest tema es proporciona informació sobre com aplicar una plantilla de calendari a un projecte per fer el seguiment de la planificació del projecte.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981288"
---
# <a name="define-project-calendars"></a>Definició dels calendaris del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per crear i administrar un projecte, heu d'aplicar una plantilla de calendari al projecte. La plantilla de calendari defineix els atributs de projecte següents:

- Hores de feina, incloent-hi l'hora d'inici i d'acabament
- Dies feiners
- Excepcions del calendari, com ara dies que no són feiners

La plantilla de calendari que s'aplica a un projecte és una còpia de la plantilla de calendari definida a la configuració de l'organització.

> [!NOTE]
> Si canvieu la plantilla de calendari, els canvis no s'emplenen a les hores de feina del projecte. Per canviar les hores de feina del projecte, cal aplicar una plantilla nova.

Per crear una plantilla de calendari per a l'organització, cal tenir dos requisits clau:

- Definiu les hores de feina desitjades de la plantilla mitjançant un recurs que es pot reservar nou o existent.
- Creeu una plantilla de calendari nova i associeu-la amb el recurs que es pot reservar.

**Definiu les hores laborables de la plantilla**

1. Aneu a **Recursos** \> **Recursos**.
2. Creeu un recurs nou al qual es fa referència a la plantilla de calendari o seleccioneu un recurs existent.
3. Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) per configurar les regles del calendari.

**Creeu una plantilla de calendari nova**

1. Aneu a **Configuració** \> **Plantilla de calendari**.
2. Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.

> [!NOTE]
> Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari. Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.

Ara podeu associar la plantilla de treball amb una plantilla de calendari de projectes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

