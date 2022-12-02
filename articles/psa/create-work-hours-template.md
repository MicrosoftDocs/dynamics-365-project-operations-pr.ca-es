---
title: Creació d'una plantilla d'hores de feina
description: Aquest article descriu com crear una plantilla d'hores de treball al Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916046"
---
# <a name="create-a-work-hours-template-project-service"></a>Crear una plantilla d'hores de treball (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Seleccioneu la pestanya **Hores de feina** del recurs i completeu les instruccions de [Definició de les hores de feina per a un recurs](/dynamics365/field-service/set-work-hours-resource) per configurar les regles del calendari.

**Creeu una plantilla de calendari nova**

1. Aneu a **Configuració** \> **Plantilla de calendari**.
2. Seleccioneu **Crea** i introduïu un nom, una descripció i un recurs de plantilla.


> [!NOTE]
> Quan es fa referència a un recurs en una plantilla de calendari, s'associa una còpia del calendari del recurs amb la plantilla de calendari. Si les hores laborables de la plantilla copiada canvien, els canvis no s'emplenen a la plantilla del calendari.


### <a name="see-also"></a>Vegeu també  
 [Configuració de recursos](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
