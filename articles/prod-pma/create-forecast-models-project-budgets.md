---
title: Creació de models de predicció per als pressupostos del projecte
description: Aquest tema descriu com crear un model de previsió per als pressupostos restants.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271026"
---
# <a name="create-forecast-models-for-project-budgets"></a>Creació de models de predicció per als pressupostos del projecte 

[!include [banner](../includes/banner.md)]

Aquest tema descriu com crear un model de previsió per als pressupostos restants. Un projecte que està subjecte al control pressupostari utilitza dos tipus de pressupostos: original i restant. Quan creeu un pressupost de projecte, heu d'especificar els models de previsió del pressupost original i restant que es van crear en la pàgina **Models de previsió**. Els pressupostos del projecte basats en els models especificats es creen quan publiqueu el pressupost del projecte.

> [!NOTE]
> Un model de previsió que s'utilitza per al control pressupostari no pot tenir un submodel o utilitzar-se com a submodel.

1. Seleccioneu **Administració de projectes i comptabilitat** > **Configuració** > **Previsions**  > **Models de previsió**.
2. Seleccioneu **Nou** per crear un nou model de previsió i introduïu un número ID de model i un nom per al nou model. 
3. Definiu l'opció **Aturat** a **Sí** per evitar qualsevol canvi a les línies de previsió per al model de previsió. 
4. Si les línies de previsió amb les quals està associat el model haurien de generar previsions de flux de caixa en el llibre major general, definiu **Inclou en les previsions de flux de caixa** a **Sí.** 
5. Per utilitzar la data del projecte com a data de la factura, definiu **Preveu la data de la factura** a **Sí**. 
6. En el camp **Tipus de pressupost**, seleccioneu un dels següents tipus de model:

   - **Pressupost original**: utilitza els imports pressupostaris originals que s'han publicat quan es crea i aprova el pressupost inicial.
   - **Pressupost restant**: utilitza els imports pressupostaris restants durant la vida del projecte. Els saldos d'aquest model de previsió es redueixen per transaccions reals i augmenten o disminueixen per revisions pressupostàries.
   - **Transfereix**: utilitza els imports de transferència del pressupost per al projecte. La transferència és un procés opcional que pot executar-se per a transferir imports no utilitzats del pressupost d'un any fiscal a un altre.

7. Definiu les opcions següents segons sigui necessari:

   - Habiliteu **Preveu la data de la factura** per utilitzar la data del projecte com a data de la factura.
   - Habiliteu **Previsió amb WIP** per fer la previsió segons el treball en curs (WIP) i seleccioneu el tipus de WIP. 
   - Podeu mantenir el **Tipus de pressupost** per defecte com a **Cap** o introduir un nou tipus. El tipus de pressupost no es pot canviar després de canviar un registre.     
    > [!NOTE]
    > Si canvieu el tipus de pressupost per defecte, totes les altres opcions no estaran disponibles per a les actualitzacions i no podeu reutilitzar aquest model de previsió. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]