---
title: Crear camps i entitats personalitzats
description: En aquest tema s'explica com crear conjunts d'opcions i entitats a la vostra pròpia solució a la plataforma Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d2fbe6a4061a93ac3186bbc8624bf5d16209cdf9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574372"
---
# <a name="create-custom-fields-and-entities"></a>Crear camps i entitats personalitzats 

[!include [banner](../includes/psa-now-project-operations.md)]

Completeu els passos següents en qualsevol moment que vulgueu crear un conjunt d'opcions o una entitat personalitzada a la plataforma del Power Apps.  
Els procediments d'aquest tema s'han d'emplenar mitjançant la interfície web del Project Service Automation (PSA).

> [!IMPORTANT]
> Us recomanem que realitzeu tots els canvis de dimensió de preus personalitzats en una solució separada. Aquestes pràctiques recomanades importants proporcionen una flexibilitat futura per actualitzar o suprimir els canvis segons calgui, us ajudaran a reutilitzar el vostre treball i facilita la portabilitat d'aquests canvis en una altra instància. Després d'haver fet tots els canvis necessaris, exporteu aquesta solució com a **Solució administrada** i importeu-la a altres instàncies per tornar a utilitzar la configuració dels preus.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Crear camps personalitzats i conjunts d'opcions a la solució de preus de la dimensió

Una dimensió de preus pot ser una conjunt d'opcions o una entitat. Tots dos s'han de crear a la solució de preus. Els passos d'aquest procediment expliquen com crear dimensions basades en una entitat i dimensions basades en un conjunt d'opcions.

### <a name="entity-based-dimensions"></a>Dimensions basades en una entitat

1. Al PSA, feu clic a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats**.
3. Feu clic a **Nou** per crear una entitat nova anomenada **Càrrec estàndard**. Introduïu la informació requerida restant i feu clic a **Desa**.

> ![Definició de l'entitat de càrrec estàndard.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Dimensions basades en un conjunt d'opcions 
Podeu crear dues dimensions basades en un conjunt d'opcions. Utilitzeu **Ubicació de treball del recurs** per fer el seguiment del treball de la ubicació **Casa** i **In situ** i utilitzeu **Hores de treball del recurs** amb els valors **Normals** i **Extres** per aplicar un marge comercial quan s'hagi completat la feina.


1. Al PSA, feu clic a **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Conjunts d'opcions**. 
3. Feu clic a **Nou** per crear un conjunt d'opcions nou, introduïu la informació necessària restant i, a continuació, feu clic a **Desa**.

> ![Dimensió de preus basada en conjunt d'opcions anomenada Ubicació de treball del recurs.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Dimensió de preus basada en conjunt d'opcions anomenada Hores de treball del recurs.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Crear dades per a les dimensions basades en l'entitat

Podeu crear dades per a les dimensions basades en l'entitat manualment o mitjançant una importació del Microsoft Excel o trucades de servei. Utilitzeu els passos d'aquest procediment per crear dos càrrecs estàndard, **Enginyer de sistemes** i **Enginyer de sistemes sènior** per la dimensió basada en l'entitat **Càrrec estàndard**. Si les dades que voleu crear són petites, com a l'exemple següent, podeu utilitzar un formulari estàndard.

1. Al PSA, feu clic a **Cerca avançada**. Seleccioneu l'entitat **Càrrec estàndard** i, a continuació, feu clic a **Resultats**. Es mostraran totes les files de l'entitat **Càrrec estàndard**.
2. Feu clic a **Nou**. Al camp **Nom**, introduïu "Enginyer de sistemes" i, a continuació, feu clic a **Desa**.
3. Tanqueu el formulari. 
4. Repetiu els passos 1-3 per crear un altre càrrec estàndard per a "Enginyer de sistemes sènior".

> ![Dades d'exemple per a l'entitat Càrrec estàndard.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
