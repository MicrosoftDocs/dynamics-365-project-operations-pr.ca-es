---
title: Desactivació de llistes de preus
description: En aquest tema s'explica com desactivar o suprimir llistes de preus no usades o antigues.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701910"
---
# <a name="deactivate-price-lists"></a>Desactivació de llistes de preus 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per suprimir llistes de preus antigues o no utilitzades del Dynamics 365 Project Operations, heu de completar dos passos. 

1. Elimineu o suprimiu la llista de preus de pàgines específiques.
2. Desactiveu o suprimiu la llista de preus de les llistes de preus actives de la pàgina **Llistes de preus**.

>[!IMPORTANT]
> Heu de completar els dos passos per suprimir completament una llista de preus. No n'hi ha prou amb realitzar només el pas 2, que és suprimir o desactivar directament la llista de preus de la visualització Llistes de preus actives. També heu de suprimir l'associació d'aquesta llista de preus de tots els llocs esmentats al pas 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Suprimir la llista de preus de pàgines específiques.
1. Per suprimir una llista de preus del Project Operations, aneu a les pàgines següents:  

      - Pàgina **Paràmetres de projecte** > pestanya **Llistes de preus**
      - Pàgina **Unitat organitzativa** > quadrícula **Llistes de preus**
      - Pàgina **Compte** > quadrícula **Llistes de preus del projecte**
      - Pàgina **Ofertes del projecte** > quadrícula **Llistes de preus del projecte**: s'aplica a totes les ofertes actives del projecte.
      - Pàgina **Contractes del projecte** > quadrícula **Llistes de preus del projecte**: s'aplica a tots els contractes actius del projecte.

 2. Per a cada pàgina, heu de seleccionar la llista de preus que voleu suprimir i, a continuació, seleccionar **Suprimeix**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Suprimiu o desactiveu la llista de preus de la pàgina Llistes de preus
 
1. Per suprimir una llista de preus de les llistes de preus actives, aneu a **Vendes** > **Clients** > **Llistes de preus**. 
2. Seleccioneu la llista de preus que voleu suprimir i, a continuació, seleccioneu **Suprimeix**. Si es fa referència a la llista de preus en qualsevol transacció existent, no la podreu suprimir. Si això passa, podeu desactivar la llista de preus perquè no aparegui en cap visualització. 
3. Per desactivar la llista de preus, torneu a seleccionar-la i, a continuació, seleccioneu **Desactiva**.   
