---
title: Administració de diversos clients a les línies de contracte basades en projectes (bàsic)
description: Aquest tema proporciona informació sobre l'administració de diversos clients en línies de contracte basades en projectes.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a7e29b1a92a5fefcf4812931383d03e5f81a27001f0e6525bb4eeb8dc93b18b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001779"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines---lite"></a>Administració de diversos clients a les línies de contracte basades en projectes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les línies de contracte basades en projectes poden incloure una llista de clients que s'encarreguen del pagament. Aquesta llista de clients de la línia de contracte basada en projectes pot ser la mateixa que la llista de clients del contracte, però això no és necessari. Quan es guanya una oferta de projecte i es crea un contracte de projecte, la llista de clients de la línia d'oferta es copia a la línia de contracte corresponent. Els clients de l'oferta es copien al contracte.

Quan es factura el contracte del projecte, la llista de clients de la línia de contracte basada en projectes té prioritat sobre la llista de clients del contracte. La llista de clients del contracte del projecte només s'utilitza per generar per defecte noves línies de contracte.

Tots els clients contractats a la pestanya **Clients** del contracte de projecte per defecte són a clients de línia de contracte en qualsevol nova línia de contracte creada per al contracte del projecte. Les línies de contracte existents no heretaran els registres de client de contracte nous creats posteriorment.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Crear, actualitzar o suprimir un registre de client de línia de contracte

Podeu crear, actualitzar o suprimir un client de línia de contracte des de la pestanya Clients de la línia de contracte a la pàgina Línia de contracte basada en projectes. Quan s'afegeix un client nou a la línia de contracte basada en projectes, també s'afegeix al contracte global com a client de contracte amb un percentatge de divisió de facturació per defecte del zero per cent. El percentatge de divisió de facturació del contracte global es copia a les noves línies de contracte i al contracte de projecte eventual. No obstant això, quan es factura des del contracte, és el percentatge de divisió de facturació al nivell de línia de contracte que s'utilitza i no el percentatge de divisió de facturació al nivell global del contracte.

A continuació, es mostren els camps al registre de client de línia de **contracte** d'una línia de contracte basada en projectes que heu de tenir en compte quan hi treballeu:

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| **Compte** | Quadrícula editable a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Tots els comptes actius. Aquest camp està blocat quan es crea el registre. Per actualitzar el camp, suprimiu el registre i creeu un registre nou. Si heu enregistrat cap valor real, no podeu suprimir el registre. Tanmateix, podeu marcar el percentatge de divisió de facturació com a zero per a aquest compte. Quan el registre es marca com a zero, es veuen afectats els valors reals de costos i ingressos futurs que s'atribueixin o es divideixin a aquest client. | Quan trieu un compte de la llista mestra de comptes per afegir-los i desar-los, el client de la línia de contracte també s'afegeix com a client del contracte. Els clients de la línia de contracte s'utilitzen quan es generen factures. |
| **Percentatge dividit de facturació** | Quadrícula editable a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Aquest camp representa el percentatge de cada transacció de vendes no facturades que s'atribuirà a aquest client de línia de contracte. | Els clients de la línia de contracte i els percentatges de divisió de facturació s'utilitzen quan es creen els valors reals després de l'aprovació i quan es genera la factura. |
| **Límit que no s’ha de superar** | Quadrícula editable a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client del contracte. | Indica si hi ha un límit o màxim negociat a l'import global que es facturarà a aquest client per a la línia de contracte. | El límit que no s'ha de superar del client de la línia de contracte s'utilitza quan es creen els valors reals i es generen les factures. |
| **És arrodoniment** | Quadrícula editable a la pestanya **Clients del contracte** i als formularis **Principal** i **Creació ràpida** per a un client de la línia de contracte. | Aquest camp indica si aquest client és un client d'arrodoniment per defecte per a aquesta línia de contracte basada en projectes. | Quan genereu valor real segons el percentatge de divisió de facturació, és possible que hi hagi algunes diferències d'arrodoniment. S'atribueixen a aquest client les diferències d'arrodoniment en aquest cas. |

## <a name="edit-billing-split-percentages"></a>Edició dels percentatges de divisió de la facturació

Els percentatges de divisió de facturació es poden editar a la quadrícula. Quan els percentatges de divisió de facturació no sumin el 100 per cent, es produirà un error. Després d'editar els percentatges de divisió de facturació, actualitzeu la pàgina per suprimir l'error.

També podeu seleccionar **Distribueix uniformement** a la subquadrícula de client de la línia de contracte. Aquesta acció assigna uniformement les divisions de facturació a tots els clients de la línia de contracte. Si hi ha cap factor d'arrodoniment, s'afegirà al client d'arrodoniment. Un client de línia de contracte sempre s'etiqueta com a client d'**arrodoniment** amb la marca **Arrodoniment** establerta en **Sí**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]