---
title: Novetats o canvis de la versió d'actualització 37 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a Microsoft Dynamics 365 Project Service Automation Update Release 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922486"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Novetats o canvis de la versió d'actualització 37 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per a la versió 37, V3. Aquesta versió té el número de sèrie V3.10.58.120 i normalment està disponible mitjançant una actualització automàtica de novembre de 2021.

## <a name="update-release-37"></a>Versió d'actualització 37

### <a name="bug-fixes"></a>Correccions d'errors

S'han corregit els problemes següents.

**Temps i despesa**
- Els usuaris no poden suprimir una entrada de temps esborrant la cel·la.
- La visualització **La meva aprovació fallida** només conté les aprovacions del projecte amb l'estat **Enviat**.

**Administració de projectes**
- Els usuaris reben un error d'excepció de referència nul·la quan obren un projecte al complement d'escriptori de Microsoft si el nom del càrrec del membre de l'equip del projecte és buit.
- No hi ha cap botó **Desa** a la pàgina **Tasca del projecte** i els usuaris no poden desar els canvis als registres de tasques.
- Els usuaris no poden suprimir un projecte que té una tasca associada a una oferta amb l'estat **Guanyada**.

**Vendes**
- El camp **Moneda** de la pàgina **Projecte** s'actualitza perquè coincideixi amb la moneda de la plantilla aplicada.
- El cost es calcula incorrectament en tasques que tenen diverses monedes.
