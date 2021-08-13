---
title: Rendiment de planificació dels recursos del projecte
description: Aquest tema proporciona informació sobre com millorar el rendiment de la planificació dels recursos per a un gran nombre de projectes.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007269"
---
# <a name="project-resource-scheduling-performance"></a>Rendiment de planificació dels recursos del projecte

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Els problemes de rendiment relacionats amb la planificació de recursos poden ocórrer quan el nombre de projectes arriba als milers. Per millorar el rendiment de la planificació de recursos, hi ha una característica disponible que permet als usuaris reduir el temps que es tarda a iniciar el formulari de disponibilitat de recursos. Específicament, això elimina el procés de sincronització d'informes de capacitat de recursos i utilitza la taula **ResProjectResource** per accelerar la cerca de recursos. Tingueu en compte que la taula **ResRollup** ja no s'utilitzarà.

> [!IMPORTANT]
> Si hi ha una dependència del procés de sincronització d'informes de capacitat de recursos o de la taula **ResProjectResource**, no utilitzeu aquesta funció.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Habilitar la millora del rendiment de la planificació de recursos
Per permetre la millora del rendiment de la planificació de recursos, completeu els passos següents.

1. Aneu a **Administració de característiques** > **Tot** i, a la llista de característiques, cerqueu **Habilita la característica de millora de la planificació de recursos del projecte**.
2. Seleccioneu **Habilita ara**.

> [!NOTE]
> Si no podeu trobar la característica a la llista, seleccioneu **Comprova si hi ha actualitzacions** per actualitzar la llista.

3. Actualitzeu el vostre navegador i aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Recursos del projecte** > **Sincronitza la capacitat dels calendaris de recursos entre totes les empreses**.
4. Establiu **Suprimeix els registres de capacitat existents** a **Sí** per suprimir dades anteriors. Si voleu generar dades incrementals, definiu-ho a **No**.
5. En el camp **Codi de període**, seleccioneu el període en què s'han de generar les dades. Si seleccioneu un codi de període, no cal definir una data d'inici i finalització.
6. Si deixeu el camp **Codi de període** en blanc, seleccioneu dates específiques d'inici i finalització per generar les dades.
7. Seleccioneu **D'acord**.

 > [!NOTE]
 > Això distribuirà les dades generals a la taula **ResCalendarCapacity** entre totes les empreses del vostre entorn, de manera que el treball per lots només s'ha d'executar en una entitat jurídica. Les dades d'aquest treball per lots són necessàries per calcular la capacitat dels recursos a través del calendari associat.

8. Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Recursos del projecte** > **Emplena els recursos del projecte entre totes les empreses** i seleccioneu **D'acord**. Aquest és l'script d'actualització de dades per a dades generals a les taules **ResProjectResourceResource**, **ResCalendarDateTimeRange** i **ResEffectiveDateTimeRange**. Els valors per al camp **PSAPRojSchedRole.RootActivity** també s'actualitzen. Si això no s'executa, rebreu un avís quan intenteu executar operacions de planificació de recursos.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Desactivar la millora del rendiment de la planificació de recursos

1. Aneu a **Administració de característiques** > **Tot** i cerqueu **Habilita la característica de millora de la planificació de recursos del projecte**.
2. Seleccioneu la característica i seleccioneu el botó **Inhabilita**.
3. Actualitzeu el navegador.
4. Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Sincronització de capacitat** > **Sincronitza les consolidacions de capacitat de recursos**.
5. A la pàgina **Sincronització d'informes de capacitat**, establiu **Suprimeix els registres de capacitat existents** a **Sí** per suprimir dades anteriors. Si voleu generar dades incrementals, definiu-ho a **No**.
6. En el camp **Codi de període**, seleccioneu el període en què s'han de generar les dades. Si seleccioneu un codi de període, no cal definir una data d'inici i finalització.
7. Si deixeu el camp **Codi de període** en blanc, seleccioneu dates específiques d'inici i finalització per generar les dades.
8. Seleccioneu **D'acord**.

> [!NOTE]
> Això distribuirà les dades generals a la taula **ResRollup** entre totes les empreses del vostre entorn, de manera que el treball per lots només s'ha d'executar en una entitat jurídica. Aquest treball per lots és necessari per a totes les visualitzacions de **Disponibilitat de recursos**. Si aquest treball per lots no s'executa, les dades de **ResRollup** es generaran sobre la marxa, cosa que pot tardar temps.


[!INCLUDE[footer-include](../includes/footer-banner.md)]