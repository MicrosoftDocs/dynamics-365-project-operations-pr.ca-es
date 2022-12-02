---
title: Plantilles de projecte
description: En aquest article es proporciona informació sobre com utilitzar les plantilles de projecte per a la configuració ràpida del projecte.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 03cccf8f0201d82db57e52dc1175fcf9a7812a53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930858"
---
# <a name="project-templates"></a>Plantilles de projecte 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Una plantilla de projecte és un marc predefinit que us ajuda a iniciar ràpidament i fàcilment un projecte. Podeu utilitzar una plantilla predefinida per crear un projecte nou amb un sol clic. Pel que fa als projectes, heu de definir els requisits previs per a les plantilles de projecte. Heu de definir un calendari de projecte per a cada plantilla de projecte i les funcions i llistes de preus han d'estar predefinides a l'organització, de manera que els components de la plantilla tinguin dades útils.

Una plantilla de projecte consta de tres components: una planificació, estimacions de projecte i membres de l'equip del projecte.

## <a name="schedule"></a>Planifica

Una planificació d'una plantilla de projecte té el mateix conjunt d'elements que una planificació d'un projecte. Podeu crear una jerarquia de tasques, associar funcions a taques, definir atributs de planificació i definir dependències. Una planificació d'una plantilla de projecte també admet modes de tasca per a cada tasca. Per tant, és compatible amb el motor de planificació. Heu d'associar un calendari de projectes amb el projecte. Quan creeu una planificació de treball, no hi ha cap diferència entre una plantilla de projecte i un projecte.

## <a name="project-estimates"></a>Estimacions del projecte

Les estimacions de projecte d'una plantilla de projecte funcionen de la mateixa manera que les estimacions de projecte en un projecte. No obstant, els preus dels costos i de les vendes s'agrupen en llistes de costos i vendes per defecte definides als paràmetres.

## <a name="creating-a-project-from-a-template"></a>Crear un projecte a partir d'una plantilla
 
Hi ha diverses maneres de crear un projecte a partir d'una plantilla de projecte:

- En crear un projecte a partir d'una oferta, podeu seleccionar una plantilla de projecte al quadre de diàleg **Creació ràpida: projecte**.

> ![Quadre de diàleg Creació ràpida: projecte.](media/project-11.png)

- Quan creeu un projecte seleccionant **Nou projecte**, la pàgina **Projecte** apareix abans que el registre es desi. Al camp **Selecció de plantilla**, seleccioneu una de les plantilles de projecte predefinides a l'organització.
- Utilitzeu **Crea un projecte des d'una plantilla** a la pàgina **Entitat de plantilla**.

## <a name="copying-components-of-template-to-project"></a>Copiar components d'una plantilla a un projecte

Quan copieu els components d'una plantilla de projecte a un projecte, es poden produir unes quantes substitucions, en funció de la configuració del projecte.

### <a name="copying-the-schedule"></a>Copiar la planificació

Quan es copia la planificació d'una plantilla de projecte, si el projecte té un calendari de projecte diferent del de la plantilla, les hores de treball del calendari de projecte s'apliquen a la planificació de tasques. D'aquesta manera, s'ajusta la planificació al calendari del projecte de suport. De la mateixa manera, la primera tasca de la planificació utilitza la data d'inici del projecte, i la planificació de la resta de la planificació de la jerarquia de la tasca s'actualitza segons la duració i les dependències especificades a la plantilla. 

### <a name="copying-project-estimates"></a>Copiar estimacions del projecte 

Quan copieu diverses línies d'estimació del projecte, les llistes de preus s'actualitzen. Per a la llista de preus de cost, aquestes actualitzacions es basen en la unitat propietària del projecte. Per a la llista de preus de vendes, es basen en el client. Per als projectes associats a una entitat de vendes, el cost unitari i els preus de venda són es determinen a partir d'aquestes llistes de preus.

### <a name="copying-a-project-team"></a>Copiar un equip de projecte

En copiar un equip de projecte de la plantilla de projecte al projecte, es copien els recursos genèrics, juntament amb les aptituds i les competències definides a la plantilla. Les assignacions de recursos genèrics també es mantenen com estaven a la plantilla de projecte. Els recursos amb nom no són compatibles amb les plantilles de projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
