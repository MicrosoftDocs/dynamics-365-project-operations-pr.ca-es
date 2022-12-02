---
title: Integració d'escriptura doble del Project Operations
description: En aquest article es proporciona una descripció general de la integració d'escriptura doble del Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927960"
---
# <a name="project-operations-dual-write-integration-overview"></a>Descripció general de la integració d'escriptura doble del Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

El Project Operations utilitza [capacitats de doble escriptura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) per sincronitzar dades a través del Microsoft Dataverse i del Dynamics 365 Finance.

A la il·lustració següent es mostra la manera que se sincronitzen les dades com a part d'aquesta integració entre el Dataverse i Finances.

![Descripció general sobre els fluxos de dades del Project Operations.](./media/ProjectOperationsFlows.jpg)

El Project Operations al Dataverse proporciona una interfície d'usuari (IU) moderna i extensibilitat senzilla sense codi o de baix codi mitjançant capacitats del Power Platform. Els administradors de projectes, els administradors de recursos, els membres de l'equip del projecte i altres persones d'atenció al públic duen a terme les seves activitats al Project Operations del Dataverse.

El Project Operations a Finances proporciona suport de comptabilitat del projecte i de reconeixement d'ingressos. El Project Operations es connecta al marc financer de Finances per al càlcul de l'impost de vendes, els tipus de canvi de moneda, els informes de condicions financeres, etc. Les experiències del comptable del projecte són principalment en Finances.

La integració del Project Operations consisteix en la integració de components següent:


- [Configuració del Project Operations i integració de les dades de configuració](resource-dual-write-setup-integration.md) 
- [Valors reals i estimacions del projecte](resource-dual-write-estimates-actuals.md)
- [Factures del projecte](resource-dual-write-project-invoice.md)
- [Administració de despeses](resource-dual-write-expense.md)
- [Factura del proveïdor](resource-dual-write-vendor-invoice.md)
