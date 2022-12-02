---
title: Característiques suprimides o obsoletes al Dynamics 365 Project Operations
description: En aquest article es descriuen les característiques que s'han suprimit o que està previst que se suprimeixin del Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028317"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Característiques suprimides o obsoletes al Dynamics 365 Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense existències, implementació bàsica: tracte de facturació proforma i Project Operations per a escenaris amb existències/basats en producció_

En aquest article es descriuen les característiques que s'han suprimit o que està previst que se suprimeixin del Dynamics 365 Project Operations.

- Les característiques *suprimides* deixen d'estar disponibles al producte.
- Les característiques *obsoletes* no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Aquesta llista té com a objectiu ajudar-vos a considerar aquestes funcions suprimides i obsoletes per a la vostra pròpia planificació.

> [!NOTE]
> Trobareu informació detallada sobre els objectes de les aplicacions d'operacions i finances als [**Informes de referència tècnics**](/dynamics/s-e/global/axtechrefrep_61). Podeu comparar les diferents versions d'aquests informes per obtenir informació sobre els objectes que han canviat o s'han eliminat a cada versió de les aplicacions de finances i operacions.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Característiques suprimides o obsoletes a la versió de març de 2022 del Project Operations

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Paràmetre "Crea sempre una transacció d'ajustament" d'Administració de projectes i comptabilitat

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Les transaccions d'ajustament són necessàries per a l'auditoria. Quan quedi obsolet, aquest paràmetre s'amagarà. El sistema sempre crearà transaccions d'ajustament, de la mateixa manera que passa actualment quan el paràmetre s'ha definit com a **Sí**. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations per a escenaris de producció/mantinguts en existències |
| **Estat** | Obsolet: abans de l'1 de març de 2023, amagarem el paràmetre i canviarem el comportament del sistema per tal que sempre es creïn transaccions d'ajustament. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Paràmetre "Utilitza la data d'ajustament com a nova data del projecte" d'Administració de projectes i comptabilitat

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Aquest paràmetre s'utilitzava originalment per permetre els ajustaments quan es tancava un període fiscal. Tanmateix, ja no és necessari, perquè la data de comptabilitat de la transacció es pot canviar a la primera data del període obert, si es configura. La data del projecte no s'ha de canviar, perquè representa la data en què es va produir la transacció. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations per a escenaris de producció/mantinguts en existències |
| **Estat** | Obsolet: abans de l'1 de març de 2023, amagarem el paràmetre i canviarem el comportament del sistema per tal que la data del projecte no es canviï mai amb els ajustaments. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flux de treball de sol·licitud de recursos al Project Operations per a escenaris basats en producció/mantinguts en existències

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsolet a causa de les limitacions pel baix volum d'ús i de transaccions. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations per a escenaris de producció/mantinguts en existències |
| **Estat** | Obsolet: l'1 de març de 2023 s'inhabilitarà l'opció per sol·licitar recursos per al projecte mitjançant el flux de treball. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Pàgina de proposta de factura del projecte sense les visualitzacions Capçalera i Línies

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsolet a causa de les millores en la pàgina que s'han introduït conjuntament amb la clau de característica **Utilitza els formularis de proposta de factura i factura del projecte amb la visualització Capçaleres i Línies**. |
| **Se substitueix per una altra característica?** | Sí |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations per a escenaris de producció/mantinguts en existències; Project Operations per a escenaris de recursos/no mantinguts en existències |
| **Estat** | Obsolet: abans de l'1 de març de 2023, desactivarem la pàgina anterior (heretada) i activarem la clau de la característica **Utilitza els formularis de proposta de factura i diari de facturació del projecte amb la visualització Capçaleres i Línies** per defecte. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Característiques suprimides o obsoletes a la versió de desembre de 2021 del Project Operations

### <a name="collaboration-workspaces"></a>Àrees de treball de col·laboració

[Crear o enllaçar amb una àrea de treball de col·laboració (Projecte)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsolet a causa del baix ús. Els clients que utilitzen el Project Operations per a escenaris de recursos/no mantinguts en existències poden utilitzar la [Col·laboració amb els Office Groups](../project-management/collaboration-groups.md). |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació  |
| **Opció d'implementació** | Project Operations per a escenaris de producció/mantinguts en existències |
| **Estat** | Obsolet: a partir de l'1 de desembre de 2022, està previst que no s'admetin les àrees de treball de col·laboració. |
