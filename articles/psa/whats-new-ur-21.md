---
title: Novetats o canvis de la versió d'actualització 21 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 21.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 69b592db7456bf11c2e933256569d726056d1a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280611"
---
# <a name="project-service-automation-update-release-21-v3"></a>Project Service Automation, versió d'actualització 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 21. Aquesta versió té el número de compilació V 3.10.32.50 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.

## <a name="update-release-21"></a>Versió d'actualització 21

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- En allotjar el **control de quadrícula Entrada de temps** als escriptoris digitals, la quadrícula no utilitza l'amplada completa del contenidor de quadrícula d'escriptoris digitals.
- En fusos horaris específiques, el control de quadrícula **Entrada de temps** no mostra registres.
- Les entrades de temps posteriors a les 21:00 apareixen en un dia incorrecte.
- Els usuaris no poden enviar despeses si la categoria de despesa **Rebut de despesa obligatori** no té cap valor.

**Administració de recursos**

S'han corregit els problemes següents:

- Les reserves inactives es mostren a la visualització **Conciliació**.
- Faltava la validació a la gestió de recursos genèrics per garantir que existeixi un estat de reserva vàlid.

**Administració de projectes**

S'han corregit els problemes següents:

- Les quadrícules del formulari **Projecte** (**Assignació de recursos**, **Tasca**, visualització **Conciliació** i **Estimacions de despeses**) es poden continuar editant fins i tot quan un projecte no està actiu.
- Els clients duplicats no es poden combinar amb els clients enllaçats a contractes de projectes confirmats.
- Quan s'afegeix un recurs que no té cap calendari vàlid, el sistema no torna un missatge d'error descriptiu a l'usuari.
- El botó **Afegeix una tasca** de la quadrícula de tasques està habilitat quan el projecte està enllaçat amb el **complement del Microsoft Project**.
- L'esforç creix de manera incontrolable quan s'assigna una tasca amb una categoria a un recurs amb una funció per a la qual hi ha un preu de cost definit.

**Sales**

S'han realitzat les millores següents:

- S'han desplaçat **Freqüència de facturació** i **Inici de facturació** a la pestanya **Planificació de facturació**.

S'han corregit els problemes següents:

- El **Preu de venda total** és zero (0) per a la **Categoria** encara que la **Funció** tingui un preu de venda total que no és zero.
- Els clients no poden canviar el valor del camp **Estat de la factura** a **Preparat per a la facturació** quan un altre procés personalitzat actualitza un camp addicional.
- El botó **Actualitza les línies de factura** pot crear diverses línies duplicades si se selecciona repetidament.
- El botó **Actualitza els preus** no funciona a la subquadrícula **Preus per funció** del formulari **Visualització ràpida**.
- La lògica **Resolució de llistes de preus de vendes** gestiona incorrectament els fusos horaris, la qual cosa deriva en la selecció incorrecta de les llistes de preus.
- El **Cost real total** d'un projecte pot estar rebaixat per un import fraccionat després d'aprovar una sola entrada de temps.
- La lògica **Resolució de preus** no proporciona cap missatge d'error descriptiu a l'usuari si **RolePrice recuperat** no té valors als camps **"Unitat principal"** i **"Preu a la unitat principal"**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]