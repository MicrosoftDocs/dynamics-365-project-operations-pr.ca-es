---
title: Capçalera d'oportunitat
description: Aquest tema proporciona informació sobre la informació general sobre les ofertes basades en el projecte i les línies d'oportunitat basades en el projecte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072140"
---
# <a name="opportunity-header"></a>Capçalera d'oportunitat

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La capçalera d'oportunitat captura la informació general sobre un acord basat en projectes que s'aplica a totes les línies de l'oportunitat basada en projectes.

Les oportunitats basades en projectes al Dynamics 365 Project Operations són extensions de les oportunitats del Dynamics 365 Sales. Aquestes extensions proporcionen funcionalitats addicionals específiques i necessàries per a les oportunitats basades en projectes. Aquestes extensions poden incloure nous camps i accions de la franja disponibles a les oportunitats basades en projectes. Potser trobareu que alguns camps, funcionalitat i lògica de valors per defecte disponibles al Sales no està disponible al Project Operations.

A la taula següent s'inclouen els camps d'una oportunitat basada en projectes que són únics per al Project Operations o que tenen canvis importants en el comportament de les oportunitats del Sales.

| **Camp** | **Ubicació** | **Rellevància, propòsit i orientació** | **Impacte descendent** |
| --- | --- | --- | --- |
| Type | Pestanya General (ocult) | Aquest camp de conjunt d'opcions té les opcions següents:</br>- Basat en treball (disponible només amb el Project Operations)</br>- Basat en elements (disponible només quan s'instal·len el Project Operations i el Sales)</br>- Basat en el manteniment del servei (disponible quan el Field Service està instal·lat) | Quan utilitzeu el Project Operations, aquest valor de camp es defineix automàticament com a **Basat en el treball** , que classifica l'oportunitat com a basada en projectes. Una oportunitat ha d'estar basada en projectes per habilitar totes les extensions i funcionalitats específiques del projecte al procés de venda descendent per a aquest acord. |
| Contacte | Pestanya General | Referència al contacte principal del client per a aquest acord. | |
| Compte | Pestanya General | Referència al registre d'empresa o compte del client. | |
| Administrador de comptes | Pestanya General | Nom de l'administrador del compte per a aquesta oportunitat basada en projectes. | L'administrador del compte s'encarrega d'administrar la relació amb el client per mitjà de la finalització d'aquest projecte. En funció del registre de recurs reservable vinculat a l'administrador de comptes, es determina el valor per defecte de la unitat contractant. |
| Unitat de contractació | Pestanya General | La unitat de l'organització responsable del lliurament del projecte o projectes associats amb aquest acord. | La unitat de contractació és la divisió de l'empresa que completarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda, i aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant el projecte. |

Per a la resta de camps i seccions de la pestanya **Resum** de l'oportunitat, vegeu [Crear o editar oportunitats (Sales i Centre de vendes)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)
