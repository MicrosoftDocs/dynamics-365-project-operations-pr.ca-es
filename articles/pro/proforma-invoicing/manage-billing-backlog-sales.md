---
title: Administració del treball pendent de facturació (bàsic)
description: En aquest tema es proporciona informació sobre les diverses visualitzacions que hi ha en administrat el registre de facturació.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 77c4df8c4370017b9199eec3a21cd07dd0343fd9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274086"
---
# <a name="manage-the-billing-backlog---lite"></a>Administració del treball pendent de facturació (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

El Dynamics 365 Project Operations té visualitzacions dedicades per ajudar-vos a administrar el registre de facturació. Per administrar el registre de facturació, seleccioneu els enllaços a l'àrea **Vendes**, a **Facturació**. 

Les següents visualitzacions estan disponibles:

- Bestretes i avançaments
- Bestretes i avançaments disponibles
- Fites de preu fix
- Treball pendent de facturació de producte
- Treball pendent de facturació de temps i material

## <a name="retainers-and-advances"></a>Bestretes i avançaments

La visualització **Bestretes i avançaments** enumera totes les bestretes i avançaments en tots els contractes del projecte del sistema. Quan una bestreta o avançament s'ha facturat, l'import de l'avançament estarà disponible per a l'ús.

## <a name="available-retainers-and-advances"></a>Bestretes i avançaments disponibles

La visualització **Bestretes i avançaments disponibles** enumera totes les bestretes i avançaments disponibles en tots els contractes del projecte del sistema. Quan una bestreta o avançament s'ha facturat, l'import de l'avançament estarà disponible per a l'ús i s'afegeix a la llista. Quan l'import de la bestreta o avançament s'utilitza per complet, se suprimeix de la llista.

## <a name="fixed-price-milestones"></a>Fites de preu fix

La visualització **Fites de preu fix** enumera vista totes les fites de preu fix en totes les línies de contracte del projecte del sistema. Es poden marcar individualment o col·lectivament les fites com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Marcar una fita com a **A punt per facturar** fa que estigui disponible per incloure-la en un esborrany de factura.

Quan les línies de contracte de diversos clients tenen un mètode de facturació de preu fix, es crea una fita per a cada client de la línia de contracte. Es pot crear una fita i dividir-la en registres de fita específics per al client. Aquesta divisió és interna i d'acord amb la divisió de facturació per percentatge definida per a cada client de la línia de contracte. A la visualització **Fites en el preu fix** veureu els registres de fita específics per al client. Cadascun d'aquests registres de fita es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització. Quan una o diverses divisions de la fita relacionada es marquen com a **A punt per facturar**, l'estat de la capçalera s'actualitza de **En curs** a **No iniciada**. Quan es facturen totes les divisions de fites, l'estat de la fita de la capçalera s'actualitza a **Completada**.

Una fita en un esborrany de factura es mostra en aquesta visualització amb un estat de facturació de **Factura del client creada**. Quan es confirma l'esborrany de factura, l'estat de facturació del registre s'actualitzarà a **Factura de client comptabilitzada**. No actualitzeu aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funciona correctament quan aquests valors d'estat s'actualitzen amb codi personalitzat.

## <a name="product-billing-backlog"></a>Treball pendent de facturació de producte

La visualització **Registre de facturació de productes** mostra totes les línies de contracte basades en productes en tots els contractes de projecte del sistema. Es poden marcar individualment o col·lectivament les línies de contracte basades en productes com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Marcar una línia de contracte basada en productes com a **A punt per facturar** fa que estigui disponible per incloure-la en un esborrany de factura.

Una línia de contracte basada en productes que es troba en un esborrany de factura es mostra en aquesta visualització amb un estat de facturació **Factura del client creada**. Quan es confirma l'esborrany de la factura, l'estat de facturació d'aquest registre s'actualitza a **Factura del client comptabilitzada**. No actualitzeu aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funciona correctament quan aquests valors d'estat s'actualitzen amb codi personalitzat.

## <a name="time-and-material-billing-backlog"></a>Treball pendent de facturació de temps i material

La visualització **Registre de facturació de temps i material** enumera tots els valors reals de vendes no facturades en tots els contractes del projecte al sistema que no s'han facturat. Es poden marcar individualment o col·lectivament valors reals de vendes no facturades com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Marcar un valor real de venda no facturada com a **A punt per facturar** fa que estigui disponible per afegir-lo a un esborrany de factura.

Els valors reals de vendes sense facturar que tenen un **Estat del límit que no s'ha de superar** que és **Error** no es poden marcar com a **A punt per facturar**. Si els valors reals s'han de marcar com a **A punt per facturar**, restabliu l'estat en altres valors reals de la línia de contracte que s'han confirmat. i torneu a avaluar l'**estat del límit que no s'ha de superar**.

Si les línies de contracte de diversos clients tenen un mètode de facturació de temps i material, quan s'aproven el temps i les despeses, es crea un valor real de venda no facturada per a cada client a la línia de contracte d'acord amb la divisió de facturació pel percentatge definit per a cadascun dels clients. A la visualització **Registre de facturació de temps i material**, veureu aquests valors reals de vendes no facturades específics d'un client. Cadascun d'aquests registres de valors reals de vendes sense facturar es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització.

Un valor de vendes sense facturar que es troba en un esborrany de factura es mostra en aquesta visualització amb un estat de facturació **Factura del client creada**. Quan es confirma l'esborrany de la factura, l'estat de facturació d'aquest registre s'actualitza a **Factura del client comptabilitzada**. No actualitzeu aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funciona correctament quan aquests valors d'estat s'actualitzen amb codi personalitzat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]