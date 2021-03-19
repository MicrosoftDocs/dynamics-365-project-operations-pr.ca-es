---
title: Tipus de períodes
description: En aquest tema es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287271"
---
# <a name="period-types"></a>Tipus de períodes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Un tipus de període defineix la freqüència amb què es calculen els ingressos d'un projecte. En aquest tema es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos. 

## <a name="create-and-work-with-period-types"></a>Crear i treballar amb tipus de períodes
Per crear i treballar amb tipus de períodes, seguiu aquests passos:

1. A l'entorn del Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Estimacions** > **Tipus de períodes**.
2. Seleccioneu **Crea** per crear un tipus de període nou. Introduïu un nom i una descripció.
3. Al camp **Freqüència**, seleccioneu un valor:

    - Si seleccioneu **Setmana**, **Quinzena**, **Semimensual**, **Mes**, **Dia**, **Trimestre** o **Any**, el calendari s'utilitzarà per generar els períodes. 
    - Si seleccioneu **Període comptable**, els períodes comptables de la configuració del llibre general s'utilitzaran per generar períodes.
    - Si seleccioneu **Il·limitat**, podeu especificar períodes personalitzats.
4. Seleccioneu el registre del tipus de període i, a continuació, seleccioneu **Genera períodes** per crear períodes per al tipus de període. Segons la freqüència del període que hàgiu seleccionat, pot ser que tingueu l'opció d'especificar una data d'inici o el nombre de períodes que cal generar.
5. Seleccioneu **Períodes** per revisar els períodes generats.



[!INCLUDE[footer-include](../includes/footer-banner.md)]