---
title: Novetats o canvis de la versió d'actualització 16 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 16.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 1f3bb4442ce1d06807f264003c930dbbee19a5c7
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280881"
---
# <a name="project-service-automation-update-release-16-v3"></a>Project Service Automation, versió d'actualització 16, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.  Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lació, actualització o supressió d'una solució preferida](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 16. Aquesta versió té el número de compilació V3.10.6.34 i està disponible de forma general a través d'una actualització automàtica el gener de 2020.


## <a name="update-release-16"></a>Versió d'actualització 16

### <a name="bug-fixes"></a>Correccions d'errors

-   Temps i despesa

    -   Correcció: els usuaris que intentaven enviar entrades de despesa i de temps suprimits per a les aprovacions rebran ara missatges d'error pertinents.

-   Administració de projectes

    -   Correcció: les unitats de recursos definides per als membres de l'equip a les plantilles es respecten amb les plantilles que s'apliquen a un nou projecte.

    -   Correcció: s'ha millorat la gestió de la reassignació de la propietat del registre.

    -   Correcció: els projectes que estan en procés de copiar-se no es podran copiar fins que s'hagin completat totes les operacions de còpia.

-   Administració de recursos

    -   Correcció: el perllongament de les reserves ara gestiona la duració curta correctament i ja no es crea el valor de zero hores per a reserves prolongades.

    -   Correcció: la visualització de conciliació ara es mostra quan el fus horari del projecte és +5:30 GMT i el de l'usuari és diferent.

-   Sales

    -   Correcció: quan un projecte que s'ha assignat a una línia de contracte se suprimeix i s'assigna un projecte nou, significa que els registres reals del projecte nou no s'estaven reavaluant basant-se en les regles de facturació i de preus definides a la línia de contracte. S'ha solucionat en aquesta versió. Els preus i els registres reals del projecte acabat d'assignar s'invertiran i es tornaran a crear correctament basant-se en les regles de preus i de facturació de la línia de contracte. Els registres reals del projecte no assignat també es tornaran a avaluar i crear com a conseqüència.

    -   Correccions: s'ha afegit una validació addicional al camp **Import** de la línia d'estimació per garantir que no s'hagin persistit els valors nuls.

    -   Correcció: quan s'han actualitzat els valors reals en un projecte, s'afegeix un botó d'actualització al formulari principal del projecte per permetre als usuaris tornar a sincronitzar els valors reals.

    -   Correcció: quan els usuaris facin l'actualització de 2.X a 3.X, es permetran projectes amb un valor NULL per al nom del projecte.



[!INCLUDE[footer-include](../includes/footer-banner.md)]