---
title: Implementació del Project Operations (bàsic)
description: 'En aquest tema es proporciona informació sobre com instal·lar la implementació bàsica del Project Operations: acord a facturació proforma.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: e33506504665f2e7ef7ad48469082f9f64a2a44b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580720"
---
# <a name="deploy-project-operations---lite"></a>Implementació del Project Operations (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_



El Project Operations admet diversos models d'implementació. Per determinar el millor model d'implementació, vegeu [Tipus d'implementació](determine-deployment-type.md).


> [!IMPORTANT]
> Aquesta implementació, la implementació bàsica: acord a facturació proforma, genera una **implementació del Project Operations només del Dataverse**.

- [Instal·la les operacions del projecte en un entorn nou Dataverse](#new)
- [Instal·lar en un entorn existent Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Instal·la les operacions del projecte a un entorn nou Dataverse

1. [Com a Global o Power Platform Administrador](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència d'Operacions de Projecte, creeu un entorn nou Dataverse al Centre [d'administració del](https://admin.powerplatform.com) PowerPlatform. Assegureu-vos que **Creeu una base de dades per a aquest entorn** i **que les aplicacions** del Dynamics 365 estiguin habilitades. Per obtenir informació, vegeu [Crear i administrar entorns al centre d'administració del Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleccioneu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instal·la les operacions del projecte en un entorn existent Dataverse
1. Assegureu-vos que l'entorn no s'ha configurat amb [doble escriptura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), ja que la instal·lació instal·larà les Operacions del [projecte per a les capacitats d'escenaris basats en recursos/ no emmagatzemats](project-operations-integrated-deployment-overview.md).
2. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, localitzeu l'entorn al [centre d'administració del Power Platform](https://admin.powerplatform.com) on voleu instal·lar el Project Operations.
3. Instal·leu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365. Per obtenir més informació, vegeu [Administrar les aplicacions del Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
