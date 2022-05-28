---
title: Novetats o canvis de la versió d'actualització 30 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 30.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: f99d2df3f9f6c0752109c39132c2401e0130d5df
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723528"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Novetats o canvis de la versió d'actualització 30 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 30. Aquesta versió té el número de compilació V3.10.51.61 i està disponible de manera general a través d'una actualització automàtica l'abril de 2021.

## <a name="update-release-30"></a>Versió d'actualització 30

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Es produeix un error quan creeu i deseu una entrada de temps a la pàgina **Creació ràpida** si el camp **Funció** s'elimina.
- El filtre Entrada de temps aplica l'operador de filtre erroni.
- Els fulls de temps copiats no es visualitzen automàticament quan seleccioneu **Copia la setmana** al control d'entrada de l'hora.

**Administració de recursos**

S'han corregit els problemes següents:

- Quan amplieu una reserva, l'estat de la reserva assignat a la reserva ferma no és correcte. L'extensió d'una reserva respecta l'estat de la reserva definit com a **Compromès** a les metadades de configuració de la reserva.
- Quan no s'especifica un estat de reserva vàlid, el missatge d'error no es localitza correctament.

**Administració de projectes**

S'han corregit els problemes següents:

- Els projectes no es poden crear en una moneda i incloure-hi tasques relacionades en una altra moneda.

**Vendes**

S'han corregit els problemes següents:

- Quan es copia una llista de preus, els preus no s'actualitzen.
- El tancament d'una oferta com a guanyada falla quan el detall del cost té un valor d'origen.
- A l'entitat **Tasca de projecte**, el **Cost previst** s'ha canviat a **Cost previst (base)**.
- Es genera una excepció de referència nul·la quan es creen o se suprimeixen factures.
