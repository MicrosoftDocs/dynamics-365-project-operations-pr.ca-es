---
title: Seguretat i aprovacions
description: En aquest article es proporciona informació sobre la configuració de seguretat per treballar amb aprovacions al Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841911"
---
# <a name="security-and-approvals"></a>Seguretat i aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Microsoft Dynamics 365 Project Operations utilitza dues funcions de seguretat per permetre l'aprovació d'entrades de temps, despesa i materials:

- Aprovador del projecte
- Administrador aprovador del projecte

## <a name="project-approver"></a>Aprovador del projecte

Heu de tenir la funció de seguretat d'**Aprovador del projecte** per aprovar les entrades de temps, despesa i materials del projecte. També heu de tenir accés a les entitats relacionades rellevants, com ara **Projecte**. Algú que té la funció **Administrador de projectes** pot concedir-hi accés. A més, heu de ser membre de l'equip del projecte i estar marcat com a aprovador.

Per aprovar les entrades que no són de projecte, heu de ser l'administrador de la persona que fa l'enviament.

## <a name="project-approver-admin"></a>Administrador aprovador del projecte

> [!NOTE]
> La característica [Conjunts d'aprovació](approval-sets.md) ha d'estar habilitada per poder utilitzar la funcionalitat d'Administrador aprovador del projecte.

La funció de seguretat **Administrador aprovador del projecte** permet als usuaris ignorar les normes i permet l'aprovació d'entrades a tots els projectes. L'assignació d'aquesta funció ometrà la lògica de validació que requereix pertànyer a l'equip i estar marcat com a aprovador. Heu de tenir accés a les taules relacionades rellevants, com ara **Projecte**, a través de les funcions de seguretat que teniu assignades.

El context d'usuari del SISTEMA omet les validacions de la mateixa manera que la funció de seguretat d'Administrador aprovador de projecte.
