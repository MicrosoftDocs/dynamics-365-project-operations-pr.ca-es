---
title: Novetats a la versió d'actualització 14 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 14 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749493"
---
# <a name="project-service-automation-v3-update-release-14"></a>Project Service Automation V3, versió d'actualització 14
Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA). Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al PSA V3, versió d'actualització 14. Aquesta versió té el número de compilació V3.10.4.21 i està disponible segons la planificació següent:

- **Disponibilitat general (actualització automàtica):** gener de 2020
- **Actualització automàtica:** febrer de 2020

## <a name="update-release-14"></a>Versió d'actualització 14

### <a name="enhancements"></a>Millores

- Sales

     - Els valors de camp personalitzats de **Detalls de la línia d'oferta** es copien a **Detalls de la línia de contracte del projecte** quan s'actualitza una oferta a **Tancada com a guanyada**.
     - Els projectes confirmats es poden **Tancar com a perduts**.

- Administració de recursos

     - En ampliar les reserves, es demanarà als usuaris amb un quadre de diàleg de confirmació que resumeixin els resultats de la reserva i proporcionin un enllaç per mantenir les reserves.


### <a name="bug-fixes"></a>Correccions d'errors

- Temps i despesa

     - Correcció: s'ha millorat l'experiència de l'usuari quan l'usuari no ha seleccionat cap entrada per corregir-la.

- Administració de recursos

     - Correcció: si es reserva un recurs diverses vegades es desborda el nom del recurs reservable.

- Sales

     - Correcció: el preu total de venda no es calcula fins que l'usuari també introdueix un preu de cost per a l'estimació de despeses en un projecte.
     - Correcció: el tancament d'una oferta com a **Guanyada** falla si el contracte del projecte associat no està en estat **Esborrany**.

