---
title: Novetats o canvis de la versió d'actualització 28 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 28.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: fed18ba292943f53965ee518afb5cbb13427ca60f32451edb49f67e6f10d24fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994939"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Novetats o canvis de la versió d'actualització 28 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

Aquest tema enumera les característiques i correccions noves o canviades per al Project Service Automation V3, llançament d'actualització 28 Aquesta versió té el número de compilació V3.10.46.32 i està disponible de manera general a través d'una actualització autoservei el gener de 2021.

## <a name="update-release-28"></a>Versió d'actualització 28

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Els usuaris poden utilitzar **Edició massiva** per actualitzar entrades de temps que s'han aprovat i enviat.

**Administració de projectes**

S'han corregit els problemes següents:

- En els casos en què el GUID de la tasca s'interpreta com un nombre, les tasques no es poden obrir per editar-les mitjançant **Edita la tasca** a la franja de la pàgina **Estructura del desglossament del treball**.

**Sales**

S'han corregit els problemes següents:

- Es genera una excepció de referència nul·la quan s'invoca el complement **GetEstimatesForProject**.
- **Marca a punt per facturar** a la quadrícula de fites només actualitza parcialment els atributs, excepte l'atribut **InvoiceStatus**, que s'actualitza.



[!INCLUDE[footer-include](../includes/footer-banner.md)]