---
title: Definició dels calendaris del projecte
description: En aquest tema es proporciona informació sobre com aplicar una plantilla de calendari a un projecte per fer el seguiment de la planificació del projecte.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998984"
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
3. Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](/dynamics365/field-service/set-work-hours-resource.md) per configurar les regles del calendari.

**Creeu una plantilla de calendari nova**

1. Aneu a **Configuració** \> **Plantilla de calendari**.
2. Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.

> [!NOTE]
> Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari. Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.

Ara podeu associar la plantilla de treball amb una plantilla de calendari de projectes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

