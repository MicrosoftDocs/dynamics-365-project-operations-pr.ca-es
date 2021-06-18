---
title: Manteniment dels membres de l'equip
description: En aquest tema es proporciona informació sobre la reserva de recursos amb nom a equips de projecte i assignar-los a tasques.
author: ruhercul
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 00312c5a701768e0042e7e0236477c192690ded3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998624"
---
# <a name="maintain-team-members"></a>Manteniment dels membres de l'equip

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu afegir un recurs amb nom a l'equip del projecte reservant-lo directament a l'equip.

1. Al Dynamics 365 Project Operations, aneu a **Projectes** i seleccioneu el projecte obert al qual voleu fer la reserva.
2. A la pàgina **Projecte**, a la pestanya **Equip**, seleccioneu **Nou**. 
3. Al quadre de diàleg **Creació ràpida de membre de l'equip**, seleccioneu el recurs que es pot reservar. El camp **Funció** s'emplenarà amb la funció per defecte del recurs si en té assignada una. Podeu canviar la funció. 
4. Seleccioneu les dates d'origen i finalització en què es necessitaran els recursos i seleccioneu el mètode d'assignació de la capacitat del recurs. 
5. Si voleu que el membre de l'equip sigui un aprovador de projecte, seleccioneu **Sí** al camp **Aprovador de projectes**. El membre de l'equip pot aprovar les entrades de despesa i de despeses enviades per a aquest projecte. 
6. Seleccioneu **Desa**.

Ara podeu assignar el recurs reservat a les tasques del projecte. A la pàgina **Projecte**, a la pestanya **Planificació**, assigneu tasques al recurs nou. El selector de recursos que s'inicia des del camp **Recursos** de la quadrícula de tasques mostrarà els membres de l'equip que podeu seleccionar.


Al Project Operations, les reserves de recursos i assignacions de tasques no es vinculen estretament. Quan utilitzeu el selector de recursos de la planificació, podeu assignar tasques als membres de l'equip durant més hores de les cobertes per les reserves en el projecte.

Les diferències entre les reserves dels membres de l'equip i les assignacions es mostren a les pestanyes **Equip** i **Conciliació de recursos**. També podeu conciliar les diferències entre reserves i tasques per als recursos en un nivell més detallat.

Utilitzeu el selector de recursos a la pestanya **Planificació** per cercar i seleccionar altres recursos que encara no formen part de l'equip del projecte. Aquests recursos es mostren al selector de recursos com a **Altres recursos**.

En fer una selecció, el recurs s'afegeix a l'equip del projecte i se l'assigna a la tasca, però no es genera cap reserva.

Podeu utilitzar la capacitat d'ampliació de la reserva de la pestanya **Conciliació** o el **Tauler de planificació** per reservar la capacitat del recurs al projecte.

Després d'haver reservat un membre de l'equip al vostre projecte, podeu utilitzar **Mantén les reserves** o el **Tauler de planificació** directament per administrar les seves reserves.


[!INCLUDE[footer-include](../includes/footer-banner.md)]