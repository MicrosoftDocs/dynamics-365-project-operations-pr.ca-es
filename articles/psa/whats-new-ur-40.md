---
title: Novetats o canvis de la versió d'actualització 40 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a Microsoft Dynamics 365 Project Service Automation Update Release 40, V3.
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

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per a la versió 40, V3. Aquesta versió té un número de compilació de V3.10.61.61 i està disponible de manera general a través d'una actualització d'autoservei al febrer de 2022.

## <a name="update-release-40"></a>Versió d'actualització 40

### <a name="features"></a>Característiques
Fase 1 de l'actualització de Project Service Automation a Project Operations - Lite es llançarà al febrer de 2022 a tots els clients. Per comprovar si hi ha elegibilitat, vegeu [Actualització de Project Service Automation a Project Operations](upgrade-project-operations-non-stocked.md). Si l'aplicació no apareix a la instància al Centre d'administració, poseu-vos en contacte amb el Power Platform servei d'assistència i sol·liciteu que el vol estigui habilitat per als vostres entorns. La sol·licitud ha d'incloure una llista d'identificadors d'entorn on s'ha d'habilitar el vol.

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**
- Falta una entrada de nota quan es rebutja o es cancel·la una entrada d'hora. 

**Vendes**

- Quan actualitzeu les estimacions de costos o vendes mitjançant connectors fora de la caixa, se us permet enviar càrregues útils JSON que no són vàlides fora de la interfície d'usuari.
- Quan actualitzeu les línies d'oferta mitjançant la visualització ràpida, podeu activar les ofertes.
