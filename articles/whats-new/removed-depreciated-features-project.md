---
title: Característiques suprimides o obsoletes a Dynamics 365 Project Operations
description: Aquest tema descriu les característiques que s'han suprimit o que estan planificades per suprimir-les del Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61bb84b94274762636eb8532f09634db1109e969
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601558"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Característiques suprimides o obsoletes a Dynamics 365 Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense existències, implementació bàsica: tracte de facturació proforma i Project Operations per a escenaris amb existències/basats en producció_

Aquest tema descriu les característiques que s'han suprimit o que estan planificades per suprimir-les del Dynamics 365 Project Operations.

- Les característiques *suprimides* deixen d'estar disponibles al producte.
- Les característiques *obsoletes* no estan en desenvolupament actiu i podrien suprimir-se en una actualització futura.

Aquesta llista té com a objectiu ajudar-vos a considerar aquestes funcions suprimides i obsoletes per a la vostra pròpia planificació.

> [!NOTE]
> Podeu trobar informació detallada sobre els objectes de les aplicacions finances i operacions als informes tècnics de [**referència**](/dynamics/s-e/global/axtechrefrep_61). Pots comparar les diferents versions d'aquests informes per obtenir informació sobre els objectes que han canviat o s'han suprimit a cada versió de les aplicacions Finances i Operacions.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Característiques eliminades o obsoletes a la versió d'operacions del projecte març de 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Gestió de projectes i comptabilitat paràmetre "Crea sempre una operació d'ajust"

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Les operacions d'ajust són necessàries a efectes d'auditoria. Després de l'obsoleta, aquest paràmetre s'ocultarà. El sistema sempre crearà transaccions d'ajust, tal com ho fa actualment quan el paràmetre està definit com a **Sí**. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Operacions de projecte per a escenaris de producció / estoc |
| **Estat** | Obsolet: A partir de l'1 de març de 2023, ocultarem el paràmetre i canviarem el comportament del sistema de manera que sempre es creïn transaccions d'ajust. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Gestió de projectes i comptabilitat "Utilitza la data d'ajust com a nova data del projecte" paràmetre

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Aquest paràmetre es va utilitzar originalment per permetre ajustos quan es va tancar una període fiscal. No obstant això, ja no és necessari, ja que la data comptable de l'operació es pot canviar a la primera data del període obert, si està configurada. La data del projecte no s'ha de canviar perquè representa la data en què es va produir la transacció. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Operacions de projecte per a escenaris de producció / estoc |
| **Estat** | Obsolet: L'1 de març de 2023, ocultarem el paràmetre i canviarem el comportament del sistema perquè la data del projecte no es canviï mai en els ajustos. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Flux de treball de sol·licitud de recursos a les operacions del projecte per a escenaris emmagatzemats/basats en la producció

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsoleta a causa de les limitacions de baix ús i volum de transaccions. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Operacions de projecte per a escenaris de producció / estoc |
| **Estat** | Obsolet: L'1 de març de 2023, desactivarem l'opció de sol·licitar recursos per al projecte mitjançant el flux de treball. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Pàgina de la proposta de factura del projecte sense visualitzacions de capçalera i línies

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsoleta a causa de les millores a la pàgina que s'ha introduït juntament amb la proposta de factura Del projecte d'ús **i els formularis de diari de factures amb la clau de característica De visualització capçalera i línies**. |
| **Se substitueix per una altra característica?** | Sí |
| **Àrees del producte afectades** | Aplicació |
| **Opció d'implementació** | Operacions de projecte per a escenaris de producció / estoc; Operacions del projecte per a escenaris de recursos/ no emmagatzemats |
| **Estat** | Obsolet: l'1 de març de 2023, desactivarem la pàgina anterior (heretada) i activarem la proposta de factura Del projecte d'ús **i els formularis de diari de factures amb la clau de característica De la visualització** capçalera i línies de manera predeterminada. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Característiques eliminades o obsoletes a la versió d'operacions del projecte de desembre de 2021

### <a name="collaboration-workspaces"></a>Espais de treball de col·laboració

[Crear o enllaçar a un espai de treball de col·laboració (projecte)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Motiu per a l'obsolescència/supressió** | Obsoleta a causa del baix ús. Els clients que utilitzen operacions de projecte per a escenaris de recursos o no emmagatzemats poden aprofitar la [col·laboració amb grups](../project-management/collaboration-groups.md) de l'Office. |
| **Se substitueix per una altra característica?** | No |
| **Àrees del producte afectades** | Aplicació  |
| **Opció d'implementació** | Operacions de projecte per a escenaris de producció / estoc |
| **Estat** | Obsolet: Per a l'1 de desembre de 2022, tenim previst deixar de donar suport als espais de treball de col·laboració. |
