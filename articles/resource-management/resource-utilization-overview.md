---
title: Informació general sobre l'ús de recursos
description: En aquest article s'ofereix informació sobre la utilització de recursos a les operacions del projecte.
author: ruhercul
ms.date: 11/05/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 5fbba4c9feaf3b26fba3423e160b09c58e049c70
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918484"
---
# <a name="resource-utilization-overview"></a>Informació general sobre l'ús de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els recursos poden tenir un objectiu d'ús facturable. Aquest objectiu d'ús es defineix com un atribut de la funció per defecte d'un recurs o es defineix al registre del recurs individual que es pot reservar. Els càlculs d'ús es basen en les hores reals que els recursos han informat mitjançant les entrades de temps aprovades.

Les següents fórmules s'utilitzen per calcular l'ús:

  - Ús facturable = Hores reals imputables ÷ Capacitat de recursos
  - Ús no facturable = Temps real amb ID de tipus de facturació = No imputable, Gratuït o No disponible ÷ Capacitat de recursos
  - Intern = Temps real sense contracte de vendes ÷ Capacitat de recursos
  - Capacitat de recursos = Hores de treball - Fora de l'oficina - Dies no hàbils

Podeu cercar la visualització **Ús de recursos** a la subfinestra **Recursos**.

Cada cel·la de la quadrícula representa el percentatge d'ús facturable del recurs en un període, com ara un dia, una setmana o un mes. Les següents fórmules s'utilitzen per acolorir les cel·les:

  - **Verd**: ús facturable> = ús objectiu dels recursos
  - **Groc**: ús objectiu - 20 <= ús facturable < ús objectiu
  - **Vermell**: ús facturable < ús de l'objectiu - 20

Com que la visualització **Ús de recursos** està basada en el tauler de planificació, podeu utilitzar les capacitats de filtratge del tauler de planificació per filtrar els resultats.

La quadrícula requereix que definiu un objectiu d'ús en la funció o en el recurs individual. Per configurar-ho, aneu a **Recursos** > **Funcions de recurs**.

A més, cal assignar una funció per defecte a cadascun dels recursos que es pot reservar. Aneu a **Recursos** > **Recursos**. A la pestanya **Project Service**, comproveu que es defineix una funció de recurs i que el camp **Per defecte** està definit com a **Sí**. Podeu afegir funcions addicionals on **Per defecte** = **No**. La funció on **Per defecte** = **Sí** s'utilitza per avaluar l'ús del recurs en relació amb l'objectiu per a aquesta funció.

A la pestanya **Project Service** també podeu definir un objectiu d'ús individual per al recurs. A continuació, el càlcul d'ús utilitza l'objectiu d'ús per avaluar l'objectiu del recurs en comptes de l'objectiu de la funció per defecte del recurs.

L'ús es mostra només per a un recurs si aquest recurs té temps aprovat imputable durant el període que es mostra a la quadrícula.


[!INCLUDE[footer-include](../includes/footer-banner.md)]