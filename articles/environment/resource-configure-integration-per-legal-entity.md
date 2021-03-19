---
title: Configuració de la integració del Project Operations per entitat jurídica
description: Aquest tema proporciona informació sobre la configuració de la integració per entitat jurídica al Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ccdbdce6b7d006adc9be2b5f3573dd8e79dd2b8d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276966"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a>Configuració de la integració del Project Operations per entitat jurídica 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema us guia pels passos necessaris a l'hora de configurar el Dynamics 365 Project Operations per entitat legal.

## <a name="enable-feature-keys-in-dynamics-365-finance"></a>Habilitar les claus de característiques al Dynamics 365 Finance

Completeu els passos següents per habilitar les característiques necessàries.

1. Al Dynamics 365 Finance, aneu a l'àrea de treball **Administració de característiques**.
2. A **Llista de característiques**, cerqueu i habiliteu les següents característiques:
  
    - **Habilitar diverses línies de contracte per a un projecte**
    - **Habilitar el Project Operations al Dynamics 365 Customer Engagement**

> [!NOTE]
> Si no veieu **Claus de característiques** a la llista, comproveu que la vostra versió del Finance compleix el requisit mínim de versió (versió 10.0.13 de l'aplicació amb totes les actualitzacions de qualitat aplicades o superior). Seleccioneu **Comprova si hi ha actualitzacions** per actualitzar la llista de característiques.

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a>Definir l'escenari d'implementació del Project Operations per a una entitat jurídica

Podeu habilitar el Project Operations al Dynamics 365 Customer Engagement a nivell d'entitat jurídica. Podeu tenir una entitat jurídica utilitzant el Project Operations al Dynamics 365 Customer Engagement per a escenaris basats en recursos/sense existències. En el mateix entorn, podeu tenir una altra entitat jurídica que utilitzi el Project Operations per a escenaris amb existències/producció.

1. Al Dynamics 365 Finance, aneu a **Administració de projectes i comptabilitat** > **Configuració** > **Paràmetres globals de l'administració de projectes i comptabilitat**.
2. A llista d'entitats jurídiques disponibles, seleccioneu les entitats on s'habilitaran les característiques de diverses línies de contracte i el Project Operations al Dynamics 365 Customer Engagement. Deixa sense seleccionar les entitats jurídiques que utilitzaran el Project Operations per a escenaris amb existències/producció.

> [!NOTE]
> Només es pot seleccionar una entitat jurídica si no té cap projecte existent.

## <a name="configure-project-management-and-accounting-parameters"></a>Configuració dels paràmetres de la comptabilitat i l'administració de projectes

Cada entitat legal que utilitza el Project Operations al Dynamics 365 Customer Engagement necessita un conjunt de paràmetres per defecte. Aquests paràmetres estan configurats a la pestanya **Project Operations** a la pestanya **Paràmetres de l'administració de projectes i comptabilitat**. Els paràmetres són:

  - **Valors per defecte de tipus de facturació**: el Project Operations utilitza un conjunt fix de valors per defecte de tipus de facturació que s'han d'assignar a les propietats de línia del Finance. Creeu un registre per a cada tipus de facturació: **No especificada**, **Imputable**, **No imputable**, **Complementària** i **No disponible**.
  - **Valors per defecte de categoria del projecte**: seleccioneu les categories de projecte per defecte que s'utilitzaran per a cada tipus d'operació. Aquests valors per defecte s'utilitzaran al **Diari d'integració del Project Operations** i en estimacions on no s'especifiqui cap categoria de transacció per al valor real del projecte.
  - **Previsions**: seleccioneu el model de previsió que s'utilitzarà per a les estimacions de temps i despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]