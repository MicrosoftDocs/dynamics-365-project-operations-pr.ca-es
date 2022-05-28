---
title: Novetats o canvis de la versió d'actualització 41 del Project Service Automation, V3
description: En aquest tema s'enumeren les característiques i les correccions disponibles a la Versió 41 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
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
ms.openlocfilehash: 649d8bca36fda0a09dc7230ee4d742cadb32f3b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580904"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Novetats o canvis de la versió d'actualització 41 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 41, V3, de Project Service Automation. Aquesta versió té el número de compilació V3.10.62.162 i està disponible de forma general a través d'una actualització automàtica el març de 2022.

## <a name="update-release-41"></a>Versió d'actualització 41

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Administració de projectes**
- Quan intenteu crear un projecte a partir d'una plantilla basada en un projecte creat a partir del complement de l'escriptori, es mostra l'error següent: "Validació del camp treball planificat de l'assignació de recursos: la data de finalització de cada temps d'assignació de recursos no ha de ser anterior a la data d'inici".

**Temps i despesa**
- Quan intenteu suprimir una entrada de temps, es mostra el missatge d'error següent: "Es produeix un error inesperat del codi ISV".

**Vendes**
- Quan creeu una factura per a una fita de preu fix, els **camps Descripció** i **Descripció** externa no s'emplenen. 
