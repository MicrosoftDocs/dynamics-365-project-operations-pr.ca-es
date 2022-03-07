---
title: Crear una plantilla de projecte
description: Com crear una plantilla de projecte al Project Service
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
ms.openlocfilehash: 1423dfedccfdc471662581707b4441c9ed477f7c0811ccf3905af8c59f774f77
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990844"
---
# <a name="create-a-project-template-project-service"></a>Crea una plantilla de projecte (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Les plantilles de projecte us ajuden a estalviar temps si la vostra empresa presenta freqüentment tipus de projectes similars. Ofereixen un conjunt estàndard de funcions i hores estimades per a un tipus de projecte. Els administradors de comptes i de projectes poden crear projectes basats en una plantilla de projecte o poden copiar la plantilla i fer-ne una de pròpia.  
  
## <a name="components-of-project-template"></a>Components de la plantilla de projecte
 Una plantilla de projecte consta de tres components:  
  
- **Estructura del desglossament del treball**: una estructura del desglossament del treball d'una plantilla de projecte té el mateix conjunt d'elements que el projecte. Podeu crear una jerarquia de tasca, associar funcions a taques, definir atributs de planificació, definir dependències i visualitzar totes les dades al gràfic de Gantt. L'estructura del desglossament de treball de les plantilles de projecte també admet modes de tasca per a cada tasca. No hi ha cap diferència entre una plantilla de projecte i un projecte quan es crea la planificació de treball.  
  
- **Estimacions de projecte**: les estimacions de projecte de les plantilles funcionen de la mateixa manera que amb els projectes, excepte la llista de preus utilitzada per definir que el cost i els preus de venda per defecte siguin sempre les llistes de preus de vendes i costos definides als paràmetres de l'[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. La resta de funcions són les mateixes que al projecte.  
  
- **Formació de l'equip del projecte**: en formar un equip de projecte per a una plantilla de projecte, no podeu reservar un recurs amb nom d'una plantilla. Podeu utilitzar **Generar equip de projecte** a l'estructura del desglossament del treball per generar un conjunt de recursos genèrics. També podeu especificar les aptituds i competències necessàries per als recursos genèrics. Podeu substituir un recurs genèric per un recurs que es pot reservar a les plantilles de projecte.  
  
## <a name="create-a-project-from-a-template"></a>Crear un projecte a partir d'una plantilla  
 Podeu crear un projecte a partir d'una plantilla de les formes següents:  
  
-   En crear un projecte a partir d'una oferta, podeu triar una plantilla de projecte al formulari de creació ràpida de projectes.  
  
-   Quan es crea un projecte fent clic a **Projecte nou**, el formulari de projecte es mostra abans de desar el registre. Des d'aquí, podeu fer clic al camp **Tria una plantilla** per triar-ne una de la llista de plantilles de projecte predefinides de la vostra organització.  
  
-   Feu clic a **Crea un projecte a partir d'una plantilla** a la pàgina **Plantilla de projecte** per crear un projecte a partir d'una plantilla.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Copiar components d'una plantilla a un projecte  
 Quan es copien components d'una plantilla a un projecte, hi ha algunes coses que cal saber.  
  
 **Copiar una estructura del desglossament del treball**: quan es copia una estructura del desglossament del treball d'una plantilla de projecte, si el projecte té un calendari de projecte diferent del de la plantilla, les hores de treball del calendari de projecte s'aplicaran a la planificació de tasques. Això ajusta la planificació al calendari de projecte de suport. De la mateixa manera, la primera tasca de l'estructura del desglossament del treball utilitza la data d'inici del projecte, així la resta de la planificació de la jerarquia de la tasca s'actualitza segons la duració i les dependències especificades a l'estructura del desglossament del treball de la plantilla.  
  
 **Copiar estimacions de projecte**: en copiar línies d'estimació del projecte, les llistes de preus s'actualitzen segons la unitat propietària del projecte per a la llista de preus de cost i el client per a la llista de preus de venda. El cost unitari i els preus de venda són es determinen a partir de la llista de preus dels projectes associats a l'entitat de vendes.  
  
 **Copiar un equip de projecte**: en copiar l'equip de projecte de la plantilla al projecte, es copien els recursos genèrics amb les aptituds i les competències definides a la plantilla. Les assignacions de recursos genèrics també es mantenen com a la plantilla de projecte.  
  
### <a name="see-also"></a>Vegeu també  
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]