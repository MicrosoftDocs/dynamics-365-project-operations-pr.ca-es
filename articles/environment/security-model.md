---
title: Model de seguretat
description: En aquest tema es proporciona informació sobre el model de seguretat al Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ffcfa8a9c8e31c5665acd3c3919fa90d36a3f3ca
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896719"
---
# <a name="security-model"></a>Model de seguretat

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Microsoft Dynamics 365 Project Operations conté un model de seguretat únic que permet un model de seguretat empresarial basat en funcions que col·labora amb els grups del Microsoft Office. 


## <a name="security-roles"></a>Funcions de seguretat
Les capacitats del marc frontal del Project Operations inclouen les funcions següents:

| Funció                          | Descripció                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Administrador de departament              | Admet els informes entre projectes.                                                                                                            | Unitat de negoci              |
| Aprovador del projecte              | Aprova el temps i les despeses d'un projecte.                                                                                                                              | Unitat de negoci |
| Administrador de facturació del projecte | Crea la proposta de factura.                                                                                                                                                 | Unitat de negoci |
| Administrador de projectes               | Crea el pla del projecte i sol·licita els recursos.                                                                                                                              | Unitat de negoci |
| Recurs del projecte              | Membres de l'equip que es poden reservar i informar del temps.                                                                                                          | Unitat de negoci|
| Administrador de recursos              | Totes les funcions d'administració de recursos, com ara el compliment sol·licituds i reserves de recursos, se separen per admetre la configuració híbrida d'administrador de projectes i administrador de recursos i una funció d'administrador de recursos única i centralitzada. | Unitat de negoci |


El Microsoft Project per al web inclou les funcions següents:
| Funció                          | Descripció                                                                                                          | Scope |                                                       
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| Usuari del Project | Usuari col·laboratiu del Project que pot crear els seus propis projectes i visualitzar els projectes que han compartit altres persones amb ell.| Usuari|
| Sistema del Project | Funció que s'utilitza per al context de l'aplicació. Els clients no han d'utilitzar aquesta funció del sistema. | Global|

## <a name="security-enforcement"></a>Aplicació de seguretat
Les accions que es realitzen al nivell del projecte es realitzen en el context de l'usuari que ha iniciat la sessió. Això vol dir que per tal de crear, obrir o suprimir un projecte, l'usuari ha de tenir accés disponible al CDS. L'accés al CDS es pot concedir mitjançant qualsevol dels possibles mecanismes inclosos a la plataforma. Per exemple, un usuari amb un àmbit més gran pot accedir al projecte o si s'ha dut a terme una acció d'ús compartit del projecte explícita que atorga l'accés de l'usuari.

És important tenir-ho en compte quan es creen projectes al Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Col·laboració en grup moderna amb el Project Operations
El Project per al web i el Project Operations admeten grups moderns per a la col·laboració. Els usuaris afegits al projecte per mitjà d'un grup poden editar el pla del projecte.

El Project per al web afegeix usuaris al grup automàticament durant l'assignació.

Els grups permeten treballar col·laborativament en els permisos del projecte i en admetre els artefactes de col·laboració. El diagrama següent representa els esdeveniments i els canvis d'estat que es produeixen durant el procés d'assignació de grup.

El Project Operations no crea un grup a través d'accions implícites i només ho fa mitjançant l'acció explícita de prémer els grups.

La cerca de membres del grup al quadre de diàleg **Administració de grups** està limitada a aquells que s'han definit com a part del grup de seguretat de l'entorn. Per obtenir més informació, consulteu [Control d'accés dels usuaris a entorns: grups de seguretat i llicències](https://docs.microsoft.com/power-platform/admin/control-user-access).

1. El projecte es crea i és propietat de l'usuari que el crea.
2. El propietari del projecte està actualitzat per a l'equip.
3. L'equip del propietari s'assigna al grup de l'Office especificat o creat.
4. El propietari original del projecte s'afegeix al grup de l'Office.

## <a name="deployment-recommendation"></a>Recomanació d'implementació
A mesura que el model de col·laboració de grups de l'Office evoluciona, s'afegirà funcionalitat per proporcionar controls més detallats al llarg del temps. Recomanem als clients que implementen el Project Operations avui que se centrin en un model de seguretat del Microsoft Dynamics 365 tradicional.

Per obtenir més informació, vegeu [Seguretat al Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Seguretat del Project Operations i Microsoft Dynamics 365 Finance
El Project Operations inclou les funcions següents:

- Administrador de projectes
- Comptable del projecte

Per obtenir més informació sobre la seguretat al Finance, vegeu [Seguretat basada en funcions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


