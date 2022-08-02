---
title: Funcions suprimides o obsoletes de Dynamics 365 Project Operations
description: En aquest article es descriuen les característiques que s'han suprimit o que estan previstes per suprimir-les de Dynamics 365 Project Operations.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Funcions suprimides o obsoletes de Dynamics 365 Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense existències, implementació bàsica: tracte de facturació proforma i Project Operations per a escenaris amb existències/basats en producció_

En aquest article es descriuen les característiques que s'han suprimit o que estan previstes per suprimir-les de Dynamics 365 Project Operations.

- Les característiques *suprimides* deixen d'estar disponibles al producte.
- Les característiques *obsoletes* no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Aquesta llista té com a objectiu ajudar-vos a considerar aquestes funcions suprimides i obsoletes per a la vostra pròpia planificació.

> [!NOTE]
> La informació detallada sobre els objectes de les aplicacions de finances i operacions es pot trobar als informes tècnics de [**referència**](/dynamics/s-e/global/axtechrefrep_61). Podeu comparar les diferents versions d'aquests informes per obtenir informació sobre els objectes que han canviat o s'han eliminat en cada versió de les aplicacions de finances i operacions.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Característiques suprimides o obsoletes a la versió operacions del projecte de març de 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Paràmetre de gestió i comptabilitat de projectes "Crea sempre una transacció d'ajust"

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Les operacions d'ajust són necessàries a efectes d'auditoria. Després de la desactivació, aquest paràmetre quedarà ocult. El sistema sempre crearà transaccions d'ajust, tal com fa actualment quan el paràmetre està definit com a **Sí**. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations for production/stocked scenarios |
| **Estat** | Obsolet: Abans de l'1 de març de 2023, amagarem el paràmetre i canviarem el comportament del sistema perquè sempre es creïn transaccions d'ajust. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Administració de projectes i comptabilitat "Utilitza la data d'ajust com a nova data del projecte"

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Aquest paràmetre es va utilitzar originalment per permetre ajustos quan es tancava un període fiscal. Tanmateix, ja no és necessari, ja que la data comptable de l'operació es pot canviar a la primera data del període obert, si està configurada. La data del projecte no s'ha de canviar, ja que representa la data en què es va produir l'operació. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations for production/stocked scenarios |
| **Estat** | Obsolet: Abans de l'1 de març de 2023, amagarem el paràmetre i canviarem el comportament del sistema perquè la data del projecte no es canviï mai en els ajustos. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flux de treball de sol·licitud de recursos a Project Operations per a escenaris basats en la producció o en estoc

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsolet a causa de les limitacions d'ús i volum de transaccions baixes. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Project Operations for production/stocked scenarios |
| **Estat** | Obsolet: Abans de l'1 de març de 2023, desactivarem l'opció de sol·licitar recursos per al projecte mitjançant el flux de treball. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Pàgina de proposta de factura del projecte sense vistes de capçalera i línies

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | S'ha obsolet a causa de les millores a la pàgina que s'ha introduït juntament amb la proposta de factura del projecte d'ús i els **formularis de diari de factures amb la clau de visualització** Capçalera i Línies. |
| **Se substitueix per una altra característica?** | Sí |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Operacions de projectes per a escenaris de producció / emmagatzemats; Operacions de projecte per a escenaris de recursos / no emmagatzemats |
| **Estat** | Obsolet: abans de l'1 de març de 2023, desactivarem la pàgina anterior (heretada) i activarem els formularis Utilitza la proposta de factura projecte i el **diari de factures amb la tecla de visualització** Capçalera i línies per defecte. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Característiques suprimides o obsoletes a la versió operacions del projecte de desembre de 2021

### <a name="collaboration-workspaces"></a>Espais de treball de col·laboració

[Crear o enllaçar a un espai de treball de col·laboració (Projecte)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsolet a causa del baix ús. Els clients que utilitzen operacions del Projecte per a escenaris de recursos o no emmagatzemats poden aprofitar [la col·laboració amb els grups](../project-management/collaboration-groups.md) de l'Office. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació  |
| **Opció d'implementació** | Project Operations for production/stocked scenarios |
| **Estat** | Obsolet: Abans de l'1 de desembre de 2022, tenim previst deixar de donar suport als espais de treball de col·laboració. |
