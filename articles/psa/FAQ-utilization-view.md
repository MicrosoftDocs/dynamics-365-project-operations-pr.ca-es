---
title: Veure l'ús imputable dels recursos
description: En aquest tema es proporciona informació sobre la visualització d'ús dels recursos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: b07af573bc8d312c45ee4aef50c95942401294fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285921"
---
# <a name="view-chargeable-utilization-for-resources"></a>Veure l'ús imputable dels recursos

[!include [banner](../includes/psa-now-project-operations.md)]
 
La **Visualització d'ús** de la pàgina **Utilització de recursos del Project Service** mostra la utilització imputable per a cada recurs disponible. Com que la visualització es basa en el tauler de planificació, trobareu moltes funcions iguals.

> ![Captura de pantalla de la visualització d'ús](media/FAQ-utilization-1.png)
 

El càlcul d'ús facturable funciona de la següent manera:

   Ús facturable = (hores reals facturables) / (capacitat de recursos)

Les cel·les representen l'ús facturable calculat per al període seleccionat (dies, setmanes o mesos).

Els colors de cada cel·la mostren l'ús facturable d'un recurs en comparació amb la seva utilització facturable objectiu. 

L'objectiu d'ús es pot establir en la funció predeterminada del recurs o en el recurs individual en si. El càlcul primer busca l'objectiu a l'individu, i després a la funció per defecte del recurs.

## <a name="set-target-on-a-resource"></a>Definir l'objectiu en un recurs

1. Aneu a **Recursos** \> **Recursos**. 
2. Seleccioneu un recurs per obrir el registre. 
3. A la pestanya **Project Service**, podeu definir l'objectiu d'ús del recurs.

> ![Captura de pantalla de la utilització del Project Service per definir l'ús objectiu](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Definir l'objectiu d'ús en una funció

1. Aneu a **Recursos** \> **Funcions de recurs**. 
2. Seleccioneu una funció i obriu el registre. 
3. Establiu l'ús objectiu de la funció.

> ![Captura de pantalla de la utilització de funcions de recurs per definir l'ús objectiu](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calcular l'ús imputable d'un recurs

Per calcular l'ús imputable d'un recurs, haureu de completar alguns requisits previs. 

### <a name="set-default-role-for-individual-resource"></a>Definir la funció per defecte del recurs individual

En primer lloc, l'objectiu d'ús s'ha d'establir en el recurs individual o en les funcions dels recursos. Si utilitzeu funcions de recursos per a objectius, cada recurs individual ha de tenir una funció predeterminada. 

1. Per configurar-ho, aneu a **Recursos** \> **Recursos**. 
2. Seleccioneu un recurs, obriu el registre i, a continuació, seleccioneu la pestanya **Project Service**. 
3. A la quadrícula **Funció del recurs**, assegureu-vos que hi hagi una funció per al recurs i que **Per defecte** s'hagi definit com a **Sí**.
 
### <a name="change-billing-type-for-resource-role"></a>Canviar el tipus de facturació d'una funció de recurs

Les funcions de recursos s'han de configurar perquè tinguin un tipus de facturació **Imputable**. 

1. Aneu a **Recursos** \> **Funcions de recurs**. 
2. Obriu el registre que voleu actualitzar i després establiu el tipus de facturació predeterminat a **Imputable**.

### <a name="set-working-hours-for-resource-role"></a>Definir les hores de feina per a la funció de recursos
 
El recurs ha de tenir hores de treball per poder realitzar el càlcul de la capacitat. 

1. Aneu a **Recursos** \> **Recursos**. 
2. Seleccioneu un recurs per obrir el registre i després seleccioneu **Mostra les hores de treball**. 
3. Podeu fer una actualització massiva de la llista de recursos si apliqueu una **Plantilla d'hores de treball** des de la vista **Llista de recursos**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Detecció d'errors a les hores imputables

Les hores reals imputables s'obtenen de l'entitat **Dades reals**. Les dades reals amb el tipus de facturació **Imputable** estan incloses en el càlcul i, per aquest motiu, han de tenir projectes on els valors reals siguin imputables.

Si no esteu veient l'ús facturables, us mostrem algunes coses que podeu comprovar:

- El recurs té hores de treball definides per la capacitat.
- El recurs té un objectiu d'ús definit de forma individual o té una funció predeterminada assignada. La funció té un objectiu d'ús definit.
- Les dades reals tenen un tipus de facturació **Imputable** per al període en què s'espera un càlcul d'ús. Comproveu el següent si veieu valors reals amb tipus de facturació diferents d'Imputable:

  - La funció utilitzada en el valor real té un tipus de facturació predeterminat que no és facturable.
  - La funció en la línia de contracte de projecte que recolza el projecte s'ha establert com no facturable.
  - El projecte no té una línia de contracte associada.



[!INCLUDE[footer-include](../includes/footer-banner.md)]