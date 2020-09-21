---
title: Novetats a la versió d'actualització 12 del Project Service Automation, V3
description: En aquest tema es proporciona informació sobre les novetats a la versió d'actualització 12 del Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749495"
---
# <a name="project-service-automation-v3-update-release-12"></a>Project Service Automation V3, versió d'actualització 12
Ens complau anunciar la darrera actualització de l'aplicació Dynamics 365 Project Service Automation (PSA). Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 12. Aquesta versió té el número de compilació V3.10.2.34 i està disponible de forma general a través d'una actualització automàtica l'octubre de 2019.

## <a name="update-release-12"></a>Versió d'actualització 12

### <a name="bug-fixes"></a>Correccions d'errors

- Temps i despesa

    - Correcció: s'ha actualitzat la missatgeria d'errors d'entrada de temps amb un context més rellevant.
    - Correcció: la quadrícula d'entrada de temps i la planificació mostren correctament la barra de desplaçament vertical quan cal.
    - Correcció: les entrades de despeses i temps enviades es poden aprovar.
    - Correcció: el missatge del diàleg de confirmació de cancel·lació de l'aprovació s'ha corregit per reflectir l'estat d'aprovació quan s'ha canviat d'**Aprovat** a **Enviat**.
    - Correcció: els camps **Preu**, **Unitat** i **Quantitat** ara es bloquegen al registre Despesa després d'haver-se aprovat.

- Administració de projectes

    - Correcció: s'ha suprimit l'acció **Nova** en el formulari principal **Membre de l'equip**.
    - Correcció: les assignacions de recursos s'ha actualitzat per tenir en compte errors d'arrodoniment inexactes que condueixen a un canvi de la data de finalització d'una tasca.
    - Correcció: a la quadrícula de tasques, els errors importants del servidor es mostraran a l'usuari.
    - Correcció: el nom del membre de l'equip ara es mostra al selector de persones de la tasca en comptes del nom del càrrec.

- Administració de recursos

    - Correcció: els detalls dels requisits dels recursos dels projectes creats a partir d'una plantilla utilitzen ara el calendari del projecte.
    - Correcció: les aptituds i les competències ara s'obtenen per defecte de les dades mestres de la funció al requisit del recurs creat per a aquesta funció.

- Sales

    - Correcció: s'han trobat identificadors d'objecte duplicats trobats al formulari **Contracte principal**.
    - Correcció: s'ha actualitzat la lògica per fer visible la pestanya **Anàlisi de l'oferta** perquè es visualitzi la configuració de les metadades de la pestanya.
    - Correcció: la data comptable en el registre actual prové de la data de l'entrada de temps o despesa i no la data de l'aprovació.
