---
title: Supressió d'una estimació de projecte
description: Aquest tema proporciona informació sobre la supressió d'una estimació del projecte després que s'hagi completat.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684078"
---
# <a name="eliminate-a-project-estimate"></a>Supressió d'una estimació de projecte

[!include [banner](../includes/banner.md)]

Les estimacions de projecte proporcionen informació visual financera del treball que està previst i planificat per a un projecte. Per treballar amb les estimacions d'un projecte, heu d'adjuntar el projecte a un projecte estimat. Un projecte estimat es basa sempre en un projecte existent, però diversos projectes poden fer referència a un únic projecte estimat. Només es poden adjuntar projectes de preu fix i d'inversió a projectes estimats i aquests projectes han de pertànyer al mateix grup de projectes que el projecte estimat.

Per suprimir un projecte estimat, s'ha de completar. Els passos següents expliquen com suprimir una estimació.

1. Aneu a **Administració de projectes i comptabilitat** > **Tots els projectes** i obriu el projecte. 
2. A la pestanya **Administra**, seleccioneu **Estimacions** i, a la pàgina **Estimació**, seleccioneu **Elimina**.
3. A la pestanya **Elimina l'estimació** a la pestanya **General**, definiu les següents opcions:

   - **Codi de període**: seleccioneu el codi del període per triar els projectes estimats pertinents. 
   - **Data estimada**: seleccioneu la data estimada apropiada per a l'eliminació.
   - **Avisos d'eliminació amb WIP**: habiliteu aquesta opció per proporcionar una notificació quan s'elimini una estimació associada amb un treball en curs (WIP). Quan aquesta opció no està habilitada, l'eliminació no pot continuar si existeixen transaccions no estimades. 
   > [!NOTE]
   > Aquesta opció només està disponible quan s'aplica l'eliminació a un projecte estimat. No està disponible si utilitzeu comptabilitzacions periòdiques. Aquest paràmetre funciona amb els paràmetres de la pestanya **Estimació** a la pestanya **Paràmetres del projecte**, al grup de camps **Permet l'eliminació quan hi ha transaccions no estimades**.
   - **Defineix la fase a Finalitzat**: habiliteu aquesta opció per establir la fase del projecte estimat a **Finalitzat** després d'executar l'eliminació.
   - **Imprimeix la llista d'estimació**: seleccioneu la informació que s'inclourà quan s'imprimeixi la llista d'estimació.
   - **Mostra el registre d'informació**: habiliteu aquesta opció per mostrar el registre d'informació.
   - **Data de comptabilització**: trieu la data de comptabilització al llibre major de l'estimació.

4.  Seleccioneu **D'acord**.
5. Després de completar el procés d'eliminació, el projecte estimat eliminat es mostra amb un valor negatiu. 

Si no teniu la intenció d'eliminar una estimació, podeu seleccionar l'estimació eliminada i seleccionar **Desfés l'eliminació**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]