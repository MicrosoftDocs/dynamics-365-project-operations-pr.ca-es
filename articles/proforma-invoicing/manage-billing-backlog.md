---
title: Administració del treball pendent de facturació
description: Aquest tema proporciona informació sobre com veure i treballar el treball pendent de facturació al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287721"
---
# <a name="manage-the-billing-backlog"></a>Administració del treball pendent de facturació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations té dues visualitzacions dedicades per ajudar-vos a utilitzar i administrar el registre de facturació. Són **Fites de preu fix** i **Treball pendent de facturació de temps i material** Per seleccionar una visualització, a l'àrea **Vendes** del Project Operacions, a la pàgina de navegació esquerra, seleccioneu **Facturació**. Els enllaços de treball pendent de facturació s'emmagatzemen allà.

## <a name="fixed-price-milestones"></a>Fites de preu fix

Aquesta visualització vista enumera totes les fites de preu fix en totes les línies de contracte del projecte del sistema. Es poden marcar individualment o col·lectivament les fites com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Quan es marca una fita com a **A punt per facturar**, la fita passa a estar disponible per a un esborrany de factura.

Quan les línies de contracte de diversos clients tenen un mètode de facturació de preu fix, es crea una fita per a cada client en la línia de contracte. L'usuari crea una fita i aquesta fita es divideix en registres de fita específics del client internament, d'acord amb el percentatge de facturació definit per a cada client en la línia de contracte. A la visualització **Fites de preu fix**, veureu registres de fita específics per als clients. Cadascun d'aquests registres de fita es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització. Quan un o més dels desglossaments de fita relacionats es marquen com a **A punt per facturar**, la capçalera passa a l'estat **En progrés** de **No iniciat**. Quan tots els desglossaments de fites s'han facturat, l'estat de la fita de la capçalera es converteix en **Completat**.

Una fita en un esborrany de factura es mostra en aquesta visualització amb un estat de facturació de **Factura del client creada**. Quan es confirma l'esborrany de la factura, l'estat de facturació d'aquest registre s'actualitza a **Factura comptabilitzada**. No es recomana actualitzar aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funcionarà correctament si aquests valors d'estat s'actualitzen amb codi personalitzat.

## <a name="time-and-material-billing-backlog"></a>Treball pendent de facturació de temps i material

Aquesta visualització enumera tots els valors reals de vendes no facturades que no han estat facturats en tots els contractes de projecte del sistema. Es poden marcar individualment o col·lectivament valors reals de vendes no facturades com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Marcar un valor real de venda no facturada com a **A punt per facturar** fa que estigui disponible per afegir-lo a un esborrany de factura.

Els valors reals de vendes no facturades que tenen un estat **No es pot superar** que és **Error** no es poden marcar com a **A punt per facturar**. Si aquests valors reals s'han de marcar així, reinicieu l'estat d'altres valors reals de la línia de contracte que s'han publicat i avalueu l'estat **No es pot superar**.

En el cas de les línies de contracte de diversos clients que tenen un mètode de facturació de temps i material, quan s'aproven el temps i les despeses, es crea un valor real de venda no facturada per a cada client en la línia de contracte d'acord amb el percentatge de facturació definit per a cada client en la línia de contracte. A la visualització **Treball pendent de facturació de temps i material** veureu aquests valors reals de vendes individuals no facturats. Cadascun d'aquests registres de valors reals de vendes sense facturar es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització.

Un valor real de vendes sense facturar en un esborrany de factura es mostra en aquesta visualització amb l'**Estat de facturació** **Factura del client creada**. Quan es confirma l'esborrany de la factura, l'estat de facturació d'aquest registre s'actualitza a **Factura del client comptabilitzada**. No es recomana actualitzar aquest valor d'estat quan té aquest estat mitjançant codi personalitzat. El Project Operations no funcionarà correctament quan aquests valors d'estat s'actualitzin amb codi personalitzat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]