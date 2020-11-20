---
title: Novetats o canvis de la versió d'actualització 19 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 19.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126818"
---
# <a name="project-service-automation-update-release-19-v3"></a>Project Service Automation, versió d'actualització 19, V3

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 19. Aquesta versió té el número de compilació V3.10.30.41 i està disponible de manera general a través d'una actualització automàtica el maig de 2020.

## <a name="update-release-19"></a>Versió d'actualització 19

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents: 

- Els errors derivats de les importacions d'entrades de temps no emergien correctament.
- La quadrícula d'entrada de temps no admet el comportament del camp **Només data**.
- Els recursos del projecte no poden crear una despesa amb un projecte.

**Administració de projectes**

S'han corregit els problemes següents: 

-  La tasca descendent secundària provoca una estimació de l'esforç incorrecta durant el càlcul de la finalització (EAC).

**Sales**

S'han corregit els problemes següents: 

- L'acció **Torna a calcular** no funciona amb els detalls de la línia de contracte de la despesa ni els detalls de la línia d'oferta.
- **Actualitza els preus** falta a l'estimació de la despesa.
-  Els clients no poden seleccionar motius d'estat de contracte personalitzats des de la pàgina **Contracte del projecte**.
- Els clients experimenten un rendiment degradat en crear una llista de preus personalitzada a partir d'una oferta.
- Els clients experimenten una incoherència amb el valor per defecte d'**unitat** a les pàgines **Detalls de la línia d'oferta** i **Detalls de la línia de contracte**.
- L'addició d'elements de categoria no facturables a una línia de contracte facturable no respectarà el tipus de facturació **No facturable** de la categoria de la transacció.
- Els clients no poden utilitzar les funcions i la categoria acabades d'afegir als contractes creats prèviament.
- Els clients experimenten un rendiment degradat per una recuperació innecessària a PreValidateProjectTeamMemberUpdate.cs
- Les funcions configurades com a no facturables a la llista **Categories de recursos** s'han d'afegir a la pestanya **Funcions facturables** com a **No facturables** a la línia de contracte d'un projecte.
- Els clients poden experimentar un rendiment degradat en crear un projecte perquè **GetBookableResourceIdFromUser** recupera totes les columnes de recursos disponibles en comptes de només l'identificador principal.
- L'entitat **TransactionType** no té el complement d'actualització de la prevalidació per impedir que els usuaris ingressin **Unitats** i **Grups d'unitats** que no són vàlids per als tipus de transaccions.
- El pas **Suprimeix** no funciona per a la importació d'entrades de temps.
