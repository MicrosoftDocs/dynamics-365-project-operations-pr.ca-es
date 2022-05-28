---
title: Novetats o canvis de la versió d'actualització 22 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 22.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 2718509a21c76c12427ec1d78e287df2274f4d72
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588770"
---
# <a name="project-service-automation-update-release-22-v3"></a>Project Service Automation, versió d'actualització 22, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 22. Aquesta versió té el número de compilació V 3.10.33.48 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.

## <a name="update-release-22"></a>Versió d'actualització 22

### <a name="bug-fixes"></a>Correccions d'errors



**Temps i despesa**

S'han corregit els problemes següents:

- Les **Entrades de temps** no s'afegeixen automàticament a la planificació d'entrades de temps després de la importació.
- El selector de data de la quadrícula **Entrada de temps** no reconeix la configuració regional d'un usuari.

**Administració de recursos**

S'han corregit els problemes següents:

- Al mode manual, els canvis als contorns de l'opció **Assignació de recursos** no es reconeixen en generar **Requisits de recursos**.
- Les **Sol·licituds de recursos** no admeten els estats de sol·licituds personalitzades.

**Administració de projectes**

S'han corregit els problemes següents:

- L'ús del doble clic a EstimateGridControl no analitza correctament els números en format neerlandès.
- Les hores assignades no s'actualitzen correctament quan es canvien les assignacions mitjançant el complement del client d'escriptori del Microsoft Project.
- Les quadrícules Estimacions i Seguiment del projecte mostren un codi de moneda de vendes incorrecte quan la moneda del contracte és diferent de la moneda del client i l'organització està configurada per mostrar codis de moneda en comptes de símbols monetaris.
- La data de finalització d'un membre de l'equip afegirà un dia si la planificació d'hores de feina és de 24 hores al dia.
- A la Planificació del projecte, si s'afegeix una Categoria de transacció a una tasca, no es dispara el desament automàtic.
- L'error següent es mostra quan s'afegeix un membre de l'equip a la Plantilla de projecte: "Els requisits de recursos no es poden associar amb plantilles de projecte". 
- L'script de la regla de la franja "msdyn.Approval.CanApproveOrReject" mostra un error del temps d'espera.

**Sales**

S'han corregit els problemes següents:

- No es mostra el missatge d'error de validació quan se selecciona una Llista de preus de cost a la cerca Llista de preus al formulari o entitat "Nova llista de preus de projecte d'ofertes".
- El tancament de l'oferta com a guanyada no dirigeix al contracte creat si un BPF adjunt a l'oferta és a la fase final.
- Revertir les **Vendes no facturades** s'enllaça al cost original quan es recupera una entrada de temps.
- Després de seleccionar el botó **Confirma**, l'estat de la factura no canvia a **Confirmada** si no s'actualitza la factura.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
