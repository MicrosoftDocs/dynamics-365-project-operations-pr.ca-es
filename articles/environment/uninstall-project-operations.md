---
title: Desinstal·lar el Dynamics 365 Project Operations
description: En aquest article s'ofereix informació sobre com desinstal·lar Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911952"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Desinstal·lar el Dynamics 365 Project Operations 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Per desinstal·lar el Dynamics 365 Project Operations, heu de tenir assignada la funció d'administrador.

1. Aneu a **Configuració** > **Solucions**.

    ![Pàgina Configuració.](./media/uninstall-proj-ops-solutions.png)
  
2. Suprimiu les solucions en l'ordre exacte que apareixen a la taula següent. 

    | Pas | Nom de la solució                                    | Nota                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 2 | ProjectOperations_Anchor                           | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 5 | ProjectService                                     | Sense notes addicionals.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Sense notes addicionals.                                                                         |
    | 7 | ProjectServiceCore                                 | Sense notes addicionals.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 9 | FieldServiceCommon                                 | Necessari per a la doble escriptura amb Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Necessari per a la doble escriptura amb Dynamics 365 Finance o Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Camp obligatori per al Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 19 | Dynamics365Notes                                   | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 21 | DualWriteCore                                      | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 23 | Dynamics365AssetManagement                         | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 26 | HCMCommon                                          | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 28 | Grup                                              | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 29 | Dynamics365Company                                 | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 30 | CurrencyExchangeRates                              | Si no la trobeu, ometeu aquesta solució.                                                            |
    | 31 | AssetCommon                                        | Si no la trobeu, ometeu aquesta solució.                                                            |
