---
title: Tipus de períodes
description: En aquest article es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930950"
---
# <a name="period-types"></a>Tipus de períodes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Un tipus de període defineix la freqüència amb què es calculen els ingressos d'un projecte. En aquest article es proporciona informació sobre com configurar els tipus de períodes per a l'estimació dels ingressos. 

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