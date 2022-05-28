---
title: Informació general sobre els modes d'administració de recursos
description: En aquest tema es proporciona informació sobre la funcionalitat d'Administració de recursos al Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: f30bac95b2beb92345cbe25332963c58d2bde4bb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585044"
---
# <a name="resource-management-modes-overview"></a>Informació general sobre els modes d'administració de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


El Dynamics 365 Project Operations admet dos modes per executar el flux de reserva global. El mode d'administració es defineix com un paràmetre de projecte i es pot modificar si el vostre negoci necessita canvis.    

## <a name="central-mode"></a>Mode central
Per a les organitzacions que centralitzin l'assignació de recursos a projectes, el mode central proporciona una manera d'assegurar-se que els administradors de projectes puguin definir requisits de recursos al nivell de projecte. El compliment dels requisits de recursos es delega en un administrador de recursos. Els administradors de projectes poden acceptar o rebutjar els recursos que proposar l'administrador de recursos.

![Mode central.](./media/resource-management-central.png)

Per administrar els recursos amb el mode central, vegeu:

- [Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserva de recursos amb nom a partir dels requisits de recursos](/dynamics365/project-service/book-named-resource)
- [Enviament d'una sol·licitud de recurs](/dynamics365/project-service/submit-resource-request)
- [Complir una sol·licitud de recursos](/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptar o rebutjar un recurs del projecte proposat des d'una sol·licitud de recurs](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mode híbrid
Per a les organitzacions que requereixin flexibilitat en l'assignació de recursos, el mode híbrid permet que tant els administradors de projectes com els administradors de recursos puguin reservar recursos.

![Mode híbrid.](./media/resource-management-hybrid.png)

A més del procés del mode central admès, vegeu els temes següents per administrar tots els altres fluxos de reserva admesos en el mode híbrid:

Reservar un recurs directament a un projecte:
- [Reservar recursos que es poden reservar a un equip de projecte i assignar tasques](/dynamics365/project-service/assign-named-bookable-resource)

Reservar un recurs des d'un requisit de recursos:
- [Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos](/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserva de recursos amb nom a partir dels requisits de recursos](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]