---
title: Novetats o canvis de la versió d'actualització 41 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a Microsoft Dynamics 365 Project Service Automation Update Release 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930536"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novetats o canvis de la versió d'actualització 41 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per a la versió 41, V3. Aquesta versió té el número de compilació V3.10.62.162 i està disponible de forma general a través d'una actualització automàtica el març de 2022.

## <a name="update-release-41"></a>Versió d'actualització 41

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Administració de projectes**
- Quan intenteu crear un projecte a partir d'una plantilla basada en un projecte creat a partir del complement de l'escriptori, es mostra l'error següent: "Validació del camp treball planificat de l'assignació de recursos: la data de finalització de cada temps d'assignació de recursos no ha de ser anterior a la data d'inici".

**Temps i despesa**
- Quan intenteu suprimir una entrada de temps, es mostra el missatge d'error següent: "Es produeix un error inesperat del codi ISV".

**Vendes**
- Quan creeu una factura per a una fita de preu fix, els **camps Descripció** i **Descripció** externa no s'emplenen. 
