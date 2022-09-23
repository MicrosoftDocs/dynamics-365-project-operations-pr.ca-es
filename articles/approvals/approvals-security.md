---
title: Seguretat i homologacions
description: Aquest article proporciona informació sobre la configuració de seguretat per treballar amb aprovacions a Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525400"
---
# <a name="security-and-approvals"></a>Seguretat i homologacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Microsoft Dynamics 365 Project Operations utilitza dues funcions de seguretat per permetre l'aprovació de les entrades de temps, despeses i material:

- Aprovador del projecte
- Administrador d'aprovació de projectes

## <a name="project-approver"></a>Aprovador del projecte

Heu de tenir el **funció de seguretat d'aprovació** del projecte per aprovar el temps, les despeses i les entrades de material del projecte. També heu de tenir accés a les entitats relacionades pertinents, com **ara Project**. Aquest accés el pot assignar algú que tingui la **funció de gestor** de projectes. A més, heu de ser membre de l'equip del projecte i marcar-lo com a aprovador.

Per aprovar les candidatures que no són de projecte, heu de ser el gestor del remitent.

## <a name="project-approver-admin"></a>Administrador d'aprovació de projectes

> [!NOTE]
> La característica Conjunts [d](approval-sets.md)'aprovació s'ha d'habilitar abans de poder utilitzar la funcionalitat Administració d'aprovació de projectes.

El **funció de seguretat d'administració** d'aprovació de projectes permet als usuaris eludir les polítiques i permet l'aprovació d'entrades en tots els projectes. L'assignació d'aquesta funció evitarà la lògica de validació que requereix la pertinença a l'equip i que es marcarà com a aprovador. Heu de tenir accés a les entitats relacionades pertinents, com **ara Project**. Aquest accés el pot assignar algú que tingui la **funció de gestor** de projectes.

El context d'usuari del SISTEMA evita les validacions de la mateixa manera que el funció de seguretat d'administració d'aprovació de projectes.
