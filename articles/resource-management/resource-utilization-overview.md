---
title: Informació general sobre l'ús de recursos
description: En aquest tema es proporciona informació sobre l'ús dels recursos al Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8b85464dbb68523b122116225a604f67e7236f3e
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401364"
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