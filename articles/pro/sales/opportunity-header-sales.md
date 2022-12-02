---
title: Configuració de les oportunitats (bàsic)
description: Aquest article proporciona informació sobre els acords basats en projectes i les línies d'oportunitat basades en projectes.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e2a95c57bff326237fb97a6cf432096833369eb8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934400"
---
# <a name="header-details-for-project-opportunities"></a>Detalls de la capçalera per a les oportunitats de projectes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

La capçalera d'oportunitat captura la informació general sobre un acord basat en projectes que s'aplica a totes les línies de l'oportunitat basada en projectes.

Les oportunitats basades en projectes al Dynamics 365 Project Operations són extensions d'oportunitats al Dynamics 365 Sales. Aquestes extensions proporcionen funcionalitats addicionals específiques i necessàries per a les oportunitats basades en projectes. Aquestes extensions poden incloure nous camps i accions de la franja disponibles a les oportunitats basades en projectes. Potser trobareu que alguns camps, funcionalitat i lògica de valors per defecte disponibles al Sales no està disponible al Project Operations.

A la taula següent s'inclouen els camps d'una oportunitat basada en projectes que són únics per al Project Operations o que tenen canvis importants en el comportament de les oportunitats del Sales.

| **Camp** | **Ubicació** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Type | Pestanya General (ocult) | Aquest camp de conjunt d'opcions té les opcions següents:</br>- Basat en treball (disponible només amb el Project Operations)</br>- Basat en elements (disponible només quan s'instal·len el Project Operations i el Sales)</br>- Basat en el manteniment del servei (disponible quan el Field Service està instal·lat) | Quan utilitzeu el Project Operations, aquest valor de camp es defineix automàticament com a **Basat en el treball**, que classifica l'oportunitat com a basada en projectes. Una oportunitat ha d'estar basada en projectes per habilitar totes les extensions i funcionalitats específiques del projecte al procés de venda descendent per a aquest acord. |
| Contacte | Pestanya General | Referència al contacte principal del client per a aquest acord. | |
| Compte | Pestanya General | Referència al registre d'empresa o compte del client. | |
| Administrador de comptes | Pestanya General | Nom de l'administrador del compte per a aquesta oportunitat basada en projectes. | L'administrador del compte s'encarrega d'administrar la relació amb el client per mitjà de la finalització d'aquest projecte. En funció del registre de recurs reservable vinculat a l'administrador de comptes, es determina el valor per defecte de la unitat contractant. |
| Unitat de contractació | Pestanya General | La unitat de l'organització responsable del lliurament del projecte o projectes associats amb aquest acord. | La unitat de contractació és la divisió de l'empresa que completarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda, i aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant el projecte. |

Per a la resta de camps i seccions de la pestanya **Resum** de l'oportunitat, vegeu [Crear o editar oportunitats (Sales i Centre de vendes)](/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
