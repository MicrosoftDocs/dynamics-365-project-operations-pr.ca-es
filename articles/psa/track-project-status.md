---
title: Seguiment de l'estat d'un projecte
description: Com fer un seguiment de l'estat d'un projecte al Project Service
author: ruhercul
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
ms.openlocfilehash: 58274886a9f9ce6ae49c64c1d7ac491e29c7d06c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593370"
---
# <a name="track-a-projects-status-project-service"></a>Seguiment de l'estat d'un projecte (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Utilitzeu l'[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] per fer el seguiment del progrés del projecte d'un client.  

A mesura que la participació avança, les fases del projecte s'actualitzen per reflectir la fase de la participació:  

| Tasca | Descripció | 
|------------|----------|
| **New** | Quan creeu un projecte, la fase es defineix a **Nou**. Si heu creat el projecte des d'una plantilla, en aquesta fase el projecte pot tenir una planificació, estimacions i dades d'equip. En cas contrari, serà l'esquema del projecte i haureu d'introduir manualment la resta de components del projecte. |
| **Oferta** |  Quan associeu un projecte a una oferta o el creeu a partir d'una oferta, la fase del projecte està configurada com a **Oferta** i les dates d'inici i finalització estimades també s'actualitzen. Quan el projecte està en la fase d'oferta, els detalls de l'oferta es visualitzen a la pestanya **Vendes** de la pàgina **Projecte**. |
| **Pla** |  Quan guanyeu una oferta associada amb un projecte, i quan la participació avança a la fase de contracte, la fase de projecte s'actualitza a **Pla**. Els detalls del contracte es visualitzen a la pestanya **Vendes** de la pàgina **Projecte**. |
| **Complet** | Quan la feina del projecte finalitza, podeu canviar la fase a **Completat**. Quan la fase del projecte es defineix com a completada, se suposa que el treball està 100 % completat, però el projecte es manté obert per a qualsevol entrada de temps o despesa pendent que calgui registrar. |
| **Tanca** | Quan totes les transaccions s'han registrat en el projecte i no teniu previst que se'n registri cap més, podeu definir manualment la fase com a **Tancament**. Quan el projecte es defineix com a **Tancament**, no podreu registrar cap transacció més al projecte i el projecte passarà a ser de només de lectura. |

## <a name="to-track-a-projects-status"></a>Per fer el seguiment de l'estat d'un projecte  

1.  Aneu a **Project Service > Projectes**.  

2.  Feu clic al projecte en el qual voleu treballant.  

3.  A la barra que hi ha a la part superior de la pantalla, seleccioneu la fletxa avall al costat del nom de projecte i, a continuació, feu clic a **Seguiment del projecte**.  

4.  Seleccioneu **Seguiment de l'esforç** o **Seguiment del cost** a la llista desplegable situada a la part superior de la llista de tasques.  

5.  Feu doble clic a qualsevol tasca per editar-la. També podeu moure o canviar de mida de les barres del gràfic de Gantt per canviar el temps i el progrés d'una tasca.  

### <a name="see-also"></a>Vegeu també  
 [Guia d'administrador de projectes](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
