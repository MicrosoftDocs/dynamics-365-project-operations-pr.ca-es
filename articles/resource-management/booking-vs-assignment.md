---
title: Reserves en comparació amb assignacions
description: En aquest tema es proporciona informació sobre les diferències entre les reserves de recursos i les assignacions de recursos.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012754"
---
# <a name="bookings-vs-assignments"></a>Reserves en comparació amb assignacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les reserves són l'assignació fixa o flexible de recursos a un projecte. Les reserves fixes consumeixen la capacitat d'un recurs. Les reserves representen conceptes organitzatius per als equips perquè puguin entendre com es dedicaran els recursos entre diversos projectes. El Dynamics 365 Project Operations considera les reserves un concepte a nivell de projecte. 

A diferència de les reserves, les assignacions són el compromís de recursos a tasques de projecte a la planificació del projecte. Els recursos poden tenir nom o ser genèrics.  Quan un requisit de recurs deriva de les assignacions de tasques del projecte, el Project Operations utilitza els contorns d'esforç de l'assignació de recursos per crear els contorns dels detalls del requisit de recursos. No obstant això, no es manté cap refència a les assignacions de recursos. Les actualitzacions de les reserves derivades del requisit de recursos no actualitzen cap assignació de recursos.

Normalment, la suma de les reserves d'un recurs equivaldrà a la suma de les assignacions del recurs en una o moltes tasques. No obstant, el Project Operations no obliga a aplicar aquesta concordança. La visualització **Conciliació** mostra llocs a l'administrador del projecte on les reserves i les assignacions d'un recurs no coincideixen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]