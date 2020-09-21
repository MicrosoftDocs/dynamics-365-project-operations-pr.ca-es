---
title: Novetats a la versió d'actualització 13 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 13 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749494"
---
# <a name="project-service-automation-v3-update-release-13"></a>Project Service Automation V3, versió d'actualització 13
Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA). Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 13. Aquesta versió té el número de compilació V3.10.3.18 i està disponible segons la planificació següent:

- **Disponibilitat general (actualització automàtica):** novembre de 2019
- **Actualització automàtica:** desembre de 2019


## <a name="update-release-13"></a>Versió d'actualització 13 

### <a name="bug-fixes"></a>Correccions d'errors

- Temps i despesa

     - Correcció: la funcionalitat de cerca de la pàgina **Aprovació de despeses** no funciona en fer una cerca per finalitat de la despesa.

- Administració de recursos

     - Correcció: els números de la conciliació s'ha actualitzat per tal que es justifiquin a la dreta.
     - Correcció: els recursos amb nom no es poden assignar a tasques a través de la pestanya **Planificació**.

- Administració de projectes

     - Correcció: excepció de referència nul·la en assignar un membre d'un equip quan falta la informació de configuració de **TransactionType** per a **Unitat** i **DefaultGroup**.

- Sales

     - Correcció: els registres de tipus de transacció duplicats retornen un error quan es creen registres de preu de funció.
     - Correcció: els botons addicionals per a **Nova oportunitat**, **Oferta**, **Línia de comanda** i **Afegeix un producte** són visibles a les ordres per a Oportunitats, Ofertes, Productes de la comanda i la subquadrícula Línies basada en el projecte.


