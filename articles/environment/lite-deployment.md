---
title: Implementació del Project Operations (bàsic)
description: 'En aquest article es proporciona informació sobre com instal·lar la implementació bàsica del Project Operations: acord a facturació proforma.'
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930306"
---
# <a name="deploy-project-operations---lite"></a>Implementació del Project Operations (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_



El Project Operations admet diversos models d'implementació. Per determinar el millor model d'implementació, vegeu [Tipus d'implementació](determine-deployment-type.md).


> [!IMPORTANT]
> Aquesta implementació, la implementació bàsica: acord a facturació proforma, genera una **implementació del Project Operations només del Dataverse**.

- [Instal·lar el Project Operations en un entorn nou del Dataverse](#new)
- [Instal·lació en un entorn existent del Dataverse](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>Instal·lar el Project Operations en un entorn nou del Dataverse

1. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, creeu un entorn nou del Dataverse al [centre d'administració del Power Platform](https://admin.powerplatform.com). Assegureu-vos que s'ha habilitat **Crear una base de dades per a aquest entorn** i **Aplicacions del Dynamics 365**. Per obtenir informació, vegeu [Crear i administrar entorns al centre d'administració del Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Seleccioneu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>Instal·lar el Project Operations en un entorn existent del Dataverse
1. Assegureu-vos que l'entorn no s'ha configurat amb [doble escriptura](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) perquè si és així durant la instal·lació s'instal·laran les capacitats del [Project Operations per a escenaris basats en recursos/sense existències](project-operations-integrated-deployment-overview.md).
2. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, localitzeu l'entorn al [centre d'administració del Power Platform](https://admin.powerplatform.com) on voleu instal·lar el Project Operations.
3. Instal·leu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365. Per obtenir més informació, vegeu [Administrar les aplicacions del Dynamics 365](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
