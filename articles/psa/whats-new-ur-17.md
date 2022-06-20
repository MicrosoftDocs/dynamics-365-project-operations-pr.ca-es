---
title: Novetats o canvis de la versió d'actualització 17 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a la versió 17, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c8486ef689f0d8ab014c2248fc6e5d0fddc937e7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915678"
---
# <a name="project-service-automation-update-release-17-v3"></a>Project Service Automation, versió d'actualització 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat.  Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per pSA V3, Actualització versió 17. Aquesta versió té el número de compilació V3.10.6.34 i està disponible de forma general a través d'una actualització automàtica el març de 2020.


## <a name="update-release-17"></a>Versió d'actualització 17

### <a name="bug-fixes"></a>Correccions d'errors

**General**

- Correcció: actualitza el Project Service Automation per aplicar les llicències dels membres de l'equip (el centre de recursos de projecte inclourà les metadades 3.x del pla del servei membre d'equip)
 
**Temps i despesa**

- Correcció: no és possible canviar una estimació de despesa d’un preu diferent de zero a zero (0). El canvi s’ignora.

**Administració de projectes**

- Correcció: s’ha afegit una comprovació de valors nuls al nom de posició d’un membre de l’equip.
- Correcció: el camp **msdyn_userresourceid** de l'entitat **msdyn_resourceassignment** ha quedat obsolet.
- Correcció: l’actualització de 2.x a 3.x ara controla els contorns d’esforç buits a les assignacions de tasques.

**Sales**

- Correcció: **Invoice.PreValidateInvoiceUpdate** ara gestiona l'escenari de reassignació dels propietaris de registres correctament.
- Correcció: quan la classe de transacció és **Time**, **UnitGroup** no es pot editar per a les entitats que inclouen **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** i **ContractLineDetails**. Això no obstant, **Unit** no es pot editar només per a **JournalLine** i **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
