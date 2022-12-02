---
title: Administració del treball pendent de facturació
description: Aquest article proporciona informació sobre com veure i treballar el treball pendent de facturació al Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929354"
---
# <a name="manage-billing-backlog"></a>Administració del treball pendent de facturació

**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització

El Dynamics 365 Project Operations té visualitzacions dedicades per ajudar-vos a administrar el registre de facturació. Per administrar el registre de facturació, seleccioneu els enllaços a l'àrea **Vendes**, a **Facturació**. 

Les següents visualitzacions estan disponibles:

- Bestretes i avançaments
- Bestretes i avançaments disponibles
- Fites de preu fix
- Treball pendent de facturació de temps i material

## <a name="retainers-and-advances"></a>Bestretes i avançaments

A la visualització **Bestretes i avançaments** es visualitzen les bestretes i els avançaments de tots els contractes de projecte. Quan una bestreta o avançament s'ha facturat, l'import de l'avançament estarà disponible per a l'ús.

## <a name="available-retainers-and-advances"></a>Bestretes i avançaments disponibles

A la visualització **Bestretes i avançaments disponibles** es visualitzen totes les bestretes i els avançaments disponibles de tots els contractes de projecte. Quan una bestreta o avançament s'ha facturat, l'import de l'avançament estarà disponible per a l'ús i s'afegeix a la llista. Després que s'utilitzi completament la quantitat de la bestreta o l'avançament, se suprimeix de la llista.

## <a name="fixed-price-milestones"></a>Fites de preu fix

La visualització **Fites de preu fix** mostra totes les fites de preu fix a totes les línies de contracte del projecte. Des d'aquesta visualització, les fites simples o múltiples es poden marcar com a **Preparat per la facturació** o **No preparat per a la facturació**. Marcar una fita com a **A punt per facturar** fa que estigui disponible per incloure-la en un esborrany de factura.

Quan les línies de contracte de diversos clients tenen un mètode de facturació de preu fix, es crea una fita per a cada client de la línia de contracte. Es pot crear una fita i dividir-la en registres de fita específics per al client. Aquesta divisió és interna i d'acord amb la divisió de facturació per percentatge definida per a cada client de la línia de contracte. A la visualització **Fites en el preu fix** veureu els registres de fita específics per al client. Cadascun d'aquests registres de fita es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització. Quan una o més de les fraccions de la fita relacionada estan marcades com a **Preparat per a facturació**, l'estat de la capçalera s'actualitza a **En curs** des de **No iniciat**. Quan es facturen totes les fraccions de la fita, la capçalera d'estat de la fita s'actualitza a **Completat**.

Una fita en un esborrany de factura es mostra en aquesta visualització amb un estat de facturació de **Factura del client creada**. Quan es confirma l'esborrany de factura, l'estat de facturació del registre s'actualitzarà a **Factura de client comptabilitzada**. 

> [!NOTE] 
> No actualitzeu aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funciona correctament quan aquests valors d'estat s'actualitzen amb codi personalitzat.

## <a name="time-and-material-billing-backlog"></a>Treball pendent de facturació de temps i material

La visualització **Registre de facturació de temps i material** enumera tots els valors reals de vendes no facturades en tots els contractes del projecte al sistema que no s'han facturat. Es poden marcar individualment o col·lectivament valors reals de vendes no facturades com a **A punt per facturar** o **No preparada per a facturar** des d'aquesta visualització. Marcar un valor real de venda no facturada com a **A punt per facturar** fa que estigui disponible per afegir-lo a un esborrany de factura.

Els valors reals de vendes sense facturar que tenen un **Estat del límit que no s'ha de superar** que és **Error** no es poden marcar com a **A punt per facturar**. Si els valors reals s'han de marcar com a **Preparat per a facturació**, restabliu l'estat d'altres valors reals a la línia de contracte que s'hagin confirmat i torneu a avaluar l'estat **No es pot superar**.

Si les línies de contracte de diversos clients tenen un mètode de facturació de temps i material, quan s'aproven el temps i les despeses, es crea un valor real de venda no facturada per a cada client a la línia de contracte d'acord amb la divisió de facturació pel percentatge definit per a cadascun dels clients. A la visualització **Registre de facturació de temps i material**, veureu aquests valors reals de vendes no facturades específics d'un client. Cadascun d'aquests registres de valors reals de vendes sense facturar es pot marcar com a **A punt per facturar** independentment des d'aquesta visualització.

Les vendes real no facturades que es mostren en un esborrany de factura es mostren en aquesta visualització amb l'estat **Factura de client creada**. Quan es confirma l'esborrany de la factura, l'estat de facturació d'aquest registre s'actualitza a **Factura del client comptabilitzada**. 

> [!NOTE] 
> No actualitzeu aquest valor d'estat mitjançant codi personalitzat. El Project Operations no funciona correctament quan aquests valors d'estat s'actualitzen amb codi personalitzat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
