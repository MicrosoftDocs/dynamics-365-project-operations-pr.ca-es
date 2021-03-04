---
title: Informació general sobre els modes d'administració de recursos
description: En aquest tema es proporciona informació sobre la funcionalitat d'administració de recursos al Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118506"
---
# <a name="resource-management-modes-overview"></a>Informació general sobre els modes d'administració de recursos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


El Dynamics 365 Project Operations admet dos modes per executar el flux de reserva global. El mode d'administració es defineix com un paràmetre de projecte i es pot modificar si el vostre negoci necessita canvis.    

## <a name="central-mode"></a>Mode central
Per a les organitzacions que centralitzin l'assignació de recursos a projectes, el mode central proporciona una manera d'assegurar-se que els administradors de projectes puguin definir requisits de recursos al nivell de projecte. El compliment dels requisits de recursos es delega en un administrador de recursos. Els administradors de projectes poden acceptar o rebutjar els recursos que proposar l'administrador de recursos.

![Mode central](./media/resource-management-central.png)

Per administrar els recursos amb el mode central, vegeu:

- [Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserva de recursos amb nom a partir dels requisits de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [Enviament d'una sol·licitud de recurs](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [Complir una sol·licitud de recursos](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [Acceptar o rebutjar un recurs del projecte proposat des d'una sol·licitud de recurs](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>Mode híbrid
Per a les organitzacions que requereixin flexibilitat en l'assignació de recursos, el mode híbrid permet que tant els administradors de projectes com els administradors de recursos puguin reservar recursos.

![Mode híbrid](./media/resource-management-hybrid.png)

A més del procés del mode central admès, vegeu els temes següents per administrar tots els altres fluxos de reserva admesos en el mode híbrid:

Reservar un recurs directament a un projecte:
- [Reservar recursos que es poden reservar a un equip de projecte i assignar tasques](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

Reservar un recurs des d'un requisit de recursos:
- [Assignació de recursos genèrics que es poden reservar a una tasca i generació de requisits de recursos](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [Reserva de recursos amb nom a partir dels requisits de recursos](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]