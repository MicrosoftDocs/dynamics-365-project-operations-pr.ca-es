---
title: Administració de diversos clients en contractes de projectes
description: Aquest article proporciona informació sobre l'administració de diversos clients en contractes de projectes.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 001c3c822a5d1cef6bd85164ef5e63e81719dafb
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824518"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administració de diversos clients en contractes de projectes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Els contractes de projecte al Dynamics 365 Project Operations admeten l'escenari en què un acord contractual implica diversos clients que estan finançant un acord. La pestanya **Resum** de la pàgina **Contracte de projecte** inclou el camp **Client**. Aquest camp identifica el client principal de l'acord. Altres clients de l'acord es poden configurar a la pestanya **Clients** de la pàgina **Contracte de projecte**.

Tots els clients del contracte indicats al contracte de projecte per defecte són clients de línia de contracte en qualsevol nova línia de contracte basada en projectes creada per al contracte del projecte. Les línies de contracte basades en projectes existents no hereten els clients de contracte nous quan es creen registres nous.

Les línies de contracte basades en productes s'associen automàticament al client principal.

Els clients del contracte i els clients de la línia de contracte es poden afegir, actualitzar o suprimir en qualsevol moment abans de guanyar el contracte.

## <a name="primary-customer"></a>Client principal

El client que apareix a la pestanya **Resum** del contracte del projecte com a client potencial és el client principal del contracte. Quan intenteu suprimir el client principal de la llista de clients del contracte, rebreu un missatge d'error indicant que un registre de client principal d'un contracte no es pot suprimir.

El client principal no es pot actualitzar de la llista de clients del contracte. En lloc d'això, canvieu el client potencial a la pestanya **Resum** del contracte. Quan aquest camp s'actualitza a la pàgina **Resum del contracte**, el client nou s'afegeix com a client de contracte nou amb la marca **Principal** definida. El client principal anterior continuarà sent client del contracte.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualitzar o suprimir un registre de client de contracte

Es pot crear, actualitzar o suprimir un client de contracte de la pestanya **Clients** de la pàgina **Contracte de projecte**. Els camps de la taula següent estan en el registre de client de contracte d'un contracte de projecte i s'han de tenir en compte quan treballeu amb el contracte.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| **Compte** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Enumera tots els comptes actius. Aquest camp està blocat quan es crea el registre. Per actualitzar el compte, suprimiu el registre i torneu-lo a crear. Si heu registrat cap valor real o si el registre de client del contracte és un client principal, no podeu suprimir el registre. | Els clients del contracte es copien com a clients de la línia de contracte quan es crea una línia de contracte. |
| **Percentatge dividit de facturació** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Representa el percentatge de cada transacció de vendes no facturades que s'atribueix a aquest client de contracte. | Es copia a les noves línies de contracte i per projectar els clients de línia de contracte en noves línies de contracte de projecte. |
| **Nom de contacte de facturació** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Aquest camp de text s'ha d'utilitzar per identificar la persona de contacte de la factura d'aquest client. Aquest camp per defecte prové del registre de compte relacionat. | Es copia al camp **Factura al nom del contracte** de la factura generada per a aquest client. |
| **Nom de facturació** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte | Aquest camp de text s'ha d'utilitzar per identificar la persona de contacte de la factura d'aquest client. Aquest camp per defecte prové del registre de compte relacionat. | Es copia al camp **Factura al nom del contracte** de la factura generada per a aquest client. |
| **Condicions de pagament** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Els valors per defecte provenen del registre de compte relacionat. | Es copia al camp **Factura al nom del contracte** de la factura generada per a aquest client. |
| **És arrodoniment** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Indica si aquest client és un tipus d'arrodoniment per defecte per a aquest contracte. Només hi pot haver un client d'arrodoniment en un contracte de projecte. | Quan les divisions de cost i vendes no facturades de la quantitat generen a una diferència d'arrodoniment, aquesta diferència s'aplica al valor real que s'assigna a aquest client. |
| **Límit que no s’ha de superar** | La quadrícula es pot editar a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte | Indica si hi ha un límit o màxim negociat a l'import global que es facturarà al client per aquesta interacció. | El **Límit que no s'ha de superar** configurat a nivell de client del contracte s'avaluarà a **Valors reals de vendes no facturades** que fan referència a aquest client del contracte. |

## <a name="edit-billing-split-percentages"></a>Edició dels percentatges de divisió de la facturació

Els percentatges de divisió de facturació es poden editar amb l'experiència d'edició de la quadrícula en línia. Quan els percentatges de divisió de facturació no sumin el 100 per cent, rebreu un error. Després d'editar els percentatges de divisió de facturació, actualitzeu la pàgina per descartar l'error.

També podeu seleccionar **Distribueix uniformement** a la subquadrícula **Clients de contracte** per assignar divisions de facturació uniformement a tots els clients del contracte. Si hi ha cap factor d'arrodoniment, s'afegirà al client d'arrodoniment. Un dels clients del contracte sempre està etiquetat com el client d'**arrodoniment**, la qual cosa significa que el registre del client del contracte té l'indicador d'arrodoniment definit en **Sí**. Normalment, aquest és el client principal del contracte, però també es pot canviar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
