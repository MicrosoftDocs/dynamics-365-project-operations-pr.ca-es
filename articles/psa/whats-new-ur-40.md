---
title: Novetats o canvis de la versió d'actualització 40 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions disponibles a la Versió 40 d'actualització Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912780"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Novetats o canvis de la versió d'actualització 40 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article es mostren les característiques i correccions que són noves o s'han canviat per al llançament de l'actualització 40, V3, de Project Service Automation. Aquesta versió té un número de compilació de V3.10.61.61 i està disponible de manera general a través d'una actualització d'autoservei al febrer de 2022.

## <a name="update-release-40"></a>Versió d'actualització 40

### <a name="features"></a>Característiques
La fase 1 de l'actualització des del Project Service Automation al Project Operations - Bàsic es publicarà el febrer de 2022 per a tots els clients. Per comprovar l'elegibilitat, vegeu [Actualització del Project Service Automation al Project Operations](upgrade-project-operations-non-stocked.md). Si l'aplicació no apareix a la vostra instància al Centre d'administració del Power Platform, poseu-vos en contacte amb el servei tècnic i sol·liciteu que s'habiliti l'actualització per als vostres entorns. La sol·licitud ha d'incloure una llista d'ID de entorn on calgui habilitar l'actualització.

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**
- Falta una entrada de nota quan es rebutja o es cancel·la una entrada de temps. 

**Vendes**

- Quan actualitzeu estimacions de cost o de vendes mitjançant complements estàndard, de manera incorrecta no se us permet enviar càrregues JSON que no siguin vàlides fora de la interfície d'usuari.
- Quan actualitzeu línies d'oferta amb la visualització ràpida, podeu activar ofertes.
