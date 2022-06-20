---
title: Configuració de la integració del Project Operations per entitat jurídica
description: En aquest article s'ofereix informació sobre la configuració de la integració per persona jurídica a Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3f33e641ee0932655282618c99a26e2603660059
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914666"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configuració de la integració del Project Operations per entitat jurídica 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article us guiarà pels passos necessaris per configurar Dynamics 365 Project Operations per persona jurídica.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Habilita les tecles de característiques a Dynamics 365 Finance

Completeu els passos següents per habilitar les característiques necessàries.

1. Al Dynamics 365 Finance, aneu a l'àrea **de treball Gestió de** funcions.
2. A **Llista de característiques**, cerqueu i habiliteu les següents característiques:
  
    - **Habilitar diverses línies de contracte per a un projecte**
    - **Habilita les operacions del projecte a Dynamics 365 Customer Engagement**

> [!NOTE]
> Si no veieu **Claus de característiques** a la llista, comproveu que la vostra versió del Finance compleix el requisit mínim de versió (versió 10.0.13 de l'aplicació amb totes les actualitzacions de qualitat aplicades o superior). Seleccioneu **Comprova si hi ha actualitzacions** per actualitzar la llista de característiques.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir l'escenari d'implementació del Project Operations per a una entitat jurídica

Podeu habilitar les operacions del projecte a Dynamics 365 Customer Engagement a nivell d'entitat jurídica. Podeu tenir una entitat jurídica mitjançant Project Operations on Dynamics 365 Customer Engagement per a escenaris basats en recursos o no emmagatzemats. En el mateix entorn, podeu tenir una altra entitat jurídica que utilitzi el Project Operations per a escenaris amb existències/producció.

1. En Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **global de projectes de gestió i paràmetres comptables**.
2. A la llista d'entitats jurídiques disponibles, seleccioneu entitats on s'habilitaran diverses línies de contracte i Operacions de projecte sobre Dynamics 365 Customer Engagement característiques. Deixa sense seleccionar les entitats jurídiques que utilitzaran el Project Operations per a escenaris amb existències/producció.

> [!NOTE]
> Només es pot seleccionar una entitat jurídica si no té cap projecte existent.

## <a name="configure-project-management-and-accounting-parameters"></a>Configuració dels paràmetres de la comptabilitat i l'administració de projectes

Cada entitat jurídica que utilitza Project Operations on Dynamics 365 Customer Engagement necessita un conjunt de paràmetres per defecte. Aquests paràmetres estan configurats a la pestanya **Project Operations** a la pestanya **Paràmetres de l'administració de projectes i comptabilitat**. Els paràmetres són:

  - **Valors per defecte de tipus de facturació**: el Project Operations utilitza un conjunt fix de valors per defecte de tipus de facturació que s'han d'assignar a les propietats de línia del Finance. Creeu un registre per a cada tipus de facturació: **No especificada**, **Imputable**, **No imputable**, **Complementària** i **No disponible**.
  - **Valors per defecte de categoria del projecte**: seleccioneu les categories de projecte per defecte que s'utilitzaran per a cada tipus d'operació. Aquests valors per defecte s'utilitzaran al **Diari d'integració del Project Operations** i en estimacions on no s'especifiqui cap categoria de transacció per al valor real del projecte.
  - **Previsions**: seleccioneu el model de previsió que s'utilitzarà per a les estimacions de temps i despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]