---
title: Dietes
description: En aquest article s'ofereix informació sobre les regles de per diem que s'utilitzen en la gestió de despeses.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930168"
---
# <a name="per-diems"></a>Dietes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Una dieta és una assignació que es paga a un treballador que viatja per feina. A l'administració de despeses, podeu crear regles de dietes per a diverses situacions de viatge. Els percentatges de les dietes es poden basar en l'època de l'any, en la ubicació del viatge o tots dos. Quan creeu una regla de dieta, podeu especificar que un percentatge de la tarifa de la dieta es retindrà si un treballador rep àpats o serveis gratuïts. També podeu definir un nombre mínim i màxim d'hores en què el percentatge de dieta es pot aplicar als viatges d'un treballador.

## <a name="configuration"></a>Configuració 

1. Per afegir ubicacions de dietes, aneu a **Configura** > **Càlculs i codis** > **Ubicacions de dietes**.
2. Per a cadascuna de les ubicacions afegides anteriorment, seleccioneu una tarifa de dieta i la moneda que sigui vàlida entre una data d'inici i d'acabament específica per a hotels, àpats i altres despeses. Les tarifes de dietes i les monedes es configuren a **Configura** > **Càlculs i codis** > **Dietes**.
3. A la pàgina **Ubicacions de dietes**, configureu els nivells de tarifes de dietes. Els nivells de tarifes de dietes us permeten definir el percentatge dividit d'un proveïment diari per a hotels, àpats i altres despeses. 
4. Per especificar la reducció dels percentatges d'àpats per a l'esmorzar, el dinar o el sopar, actualitzeu els camps de la pàgina **Paràmetres d'administració de despeses** a la pestanya **Dietes**. 
    
## <a name="submit-expenses-using-per-diem"></a>Enviar despeses mitjançant una dieta
Per enviar les despeses que utilitzen les dietes, utilitzeu la categoria de despesa **Dieta** quan creeu un informe de despeses. Introduïu la **Data d'inici de la dieta**, **Data de finalització de la dieta** i **Ubicació de la dieta**. L'import es calcularà en funció de les tarifes de dieta per a la ubicació seleccionada i es calcularà la reducció dels àpats en funció dels nivells de tarifes de dietes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]