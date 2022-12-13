---
title: Deploy Project Operations Lite
description: 'En aquest article es proporciona informació sobre com instal·lar la implementació bàsica del Project Operations: acord a facturació proforma.'
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810966"
---
# <a name="deploy-project-operations-lite"></a>Deploy Project Operations Lite

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_



El Project Operations admet diversos models d'implementació. Per determinar el millor model d'implementació, vegeu [Tipus d'implementació](determine-deployment-type.md).


> [!IMPORTANT]
> Aquesta implementació, la implementació bàsica: acord a facturació proforma, genera una **implementació del Project Operations només del Dataverse**.

- [Instal·lar el Project Operations en un entorn nou del Dataverse](#new)
- [Instal·lació en un entorn existent del Dataverse](#existing)
- [Instal·lar en un entorn existent Dataverse que tingui components d'escriptura dual](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a> Instal·leu Project Operations Lite a un entorn nou Dataverse 

1. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, creeu un entorn nou del Dataverse al [centre d'administració del Power Platform](https://admin.powerplatform.com). Assegureu-vos que s'ha habilitat **Crear una base de dades per a aquest entorn** i **Aplicacions del Dynamics 365**. Per obtenir informació, vegeu [Crear i administrar entorns al centre d'administració del Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Seleccioneu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a> Instal·leu project Operations Lite a un entorn existent Dataverse  
1. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, localitzeu l'entorn al [centre d'administració del Power Platform](https://admin.powerplatform.com) on voleu instal·lar el Project Operations.
1. Instal·leu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365. Per obtenir més informació, vegeu [Administrar les aplicacions del Dynamics 365](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Instal·leu Project Operations Lite a un entorn existent Dataverse on les solucions d'escriptura dual ja estan presents

Si voleu continuar executant Project Operations en mode de desplegament Lite, heu de seguir aquests passos:

1. Com a [administrador global o del Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) amb una llicència del Project Operations, localitzeu l'entorn al [centre d'administració del Power Platform](https://admin.powerplatform.com) on voleu instal·lar el Project Operations.
1. Instal·leu **Microsoft Dynamics 365 Project Operations** des de la llista d'implementació de les aplicacions del Dynamics 365. Per obtenir més informació, vegeu [Administrar les aplicacions del Dynamics 365](/power-platform/admin/manage-apps).
1. Com que el vostre entorn té components d'escriptura dual que ajuden a la integració a les aplicacions de finances i operacions instal·lades, la instal·lació del Project Operations també instal·larà les capacitats i extensions necessàries per integrar les dades relacionades amb el projecte a les aplicacions de finances i operacions. Com que voleu executar operacions del projecte en la implementació de Lite, aquests components d'integració s'han d'eliminar, ja que crearan restriccions i despeses generals per als escenaris de desplegament de Lite. Desinstal·leu manualment les solucions **Dynamics 365 Project Operations Dual Write** i **Dynamics 365 Project Operations Dual Write Entity Maps** per eliminar aquests components.
1. Aneu a **Project Operations -> Settings -> Parameters**. Obriu la **pàgina de detalls del paràmetre** de projecte i definiu el camp Comportament d'actualització de **la** solució a **Lite Only**. Això garanteix que les actualitzacions posteriors de Project Operations no tornin els components d'integració a les Operacions del Projecte.  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
