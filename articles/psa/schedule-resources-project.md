---
title: Planificar recursos per a un projecte
description: Com planificar recursos per a un projecte al Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583112"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Planificar recursos per a un projecte (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Podeu comprovar la disponibilitat de recursos per obtenir una vista general de com estan reservats els vostres recursos, o podeu filtrar la visualització per habilitats, equip, ubicació i altres opcions.  
  
El tauler de planificació mostra una llista de recursos i la seva disponibilitat. Seleccioneu un mode de visualització per mostrar la disponibilitat per **hores**, **dia**, **setmana** o **mes**.  
  
Abans d'utilitzar el tauler de planificació, és important configurar-lo. Per obtenir-ne més informació, consulta [Configura el tauler la planificació (Field Service o Project Service Automation)](/dynamics365/field-service/configure-schedule-board).
  
Si utilitzeu una versió anterior, per veure la disponibilitat dels recursos, consulteu [Visualització de la disponibilitat de recursos](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Per utilitzar la funcionalitat de reserva de tauler de planificació, la geocodificació i els serveis d'ubicació, cal activar els mapes.  
> 
> 1. Des del menú principal, seleccioneu **Planificació de recursos** > **Administració**.  
> 2. Feu clic a **Paràmetres de planificació**.  
> 3. Obriu un registre i desplaceu-vos fins a la secció **Resource Scheduling Optimization**.  
> 4. Al camp **Connecta't als mapes**, seleccioneu **Sí**.  
> 5. Accepteu les condicions i guardeu el registre.  
> 6. Des del menú principal, seleccioneu **Project Service** > **Tauler de planificació**. A partir d'aquí, hi ha diverses maneres de planificar manualment un requisit de reserva. Escolliu el mètode que més us convingui.
  
## <a name="find-available-resources"></a>Cerca recursos disponibles

1.  Des de la llista **Requisits de la reserva**, feu clic amb el botó dret a una reserva sense planificar i trieu-ne una de les següents:  
  
- Trieu **Cerca la disponibilitat: recursos actuals** per cercar un recurs disponible de la llista del tauler de planificació.  
- Trieu **Cerca la disponibilitat: tots els recursos** per cercar un recurs disponible dels recursos del sistema  
   > [!NOTE]
   >  Després, els filtres mostraran les opcions del requisit de la reserva seleccionat.  
  
2. Quan vegeu una franja de temps disponible, feu clic-hi amb el botó dret al tauler de planificació i trieu **Reserva aquí**. O bé, arrastreu i deixeu anar el requisit de la reserva a la franja de temps disponible.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Reservar un recurs amb la visualització diària i veure qui ha realitzat reserves
  
1.  Al tauler de planificació, seleccioneu **Mode de visualització** i seleccioneu **Dies**.  
  
    Es mostrarà una vista de quadrícula amb el nombre d'hores de reserva d'un recurs per dia i els dies que està lliure.  
  
2.  Feu clic al nom del recurs que voleu reservar i, a continuació, seleccioneu **Reserva**.  
  
3.  Al quadre de diàleg **Reserves de recursos (crear)**, trieu el projecte del qual voleu reservar el recurs juntament amb el mètode de reserva i les hores d'inici i finalització.  
  
4.  Quan hàgiu acabat, seleccioneu **Reserva**.  
  
## <a name="view-to-the-schedule-board"></a>Visualitza-ho al tauler la planificació
  
1.  Seleccioneu un requisit de reserva sense planificar a la part inferior de la llista.  
  
2.  Arrossegueu el requisit de reserves a una franja de recurs/temps disponible al tauler de planificació.  
  
3.  Quan hàgiu acabat, seleccioneu **Reserva**.  
  
### <a name="additional-resources"></a>Recursos addicionals  
 [Guia de l'administrador de recursos](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
