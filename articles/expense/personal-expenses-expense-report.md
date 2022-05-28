---
title: Treballar amb despeses personals en un informe de despeses
description: Aquest tema proporciona informació sobre com treballar amb les despeses personals ocasionades pels empleats mentre viatgen amb finalitats empresarials.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: d35bf6960bb60e2ad4184e1b5f188695a3525be0
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586516"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a>Treballar amb despeses personals en un informe de despeses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Durant els desplaçaments empresarials, un empleat pot pagar les despeses personals amb la seva targeta de crèdit empresarial. Si un procés no s'ha definit per gestionar les despeses personals, pot ser que el procés d'aprovació d'informes de despeses s'interrompi quan un empleat enviï l'informe de despeses detallat.

Hi ha dos mètodes que podeu utilitzar per treballar amb les despeses personals d'un empleat:

  - **Pagat per l'empleat**: la vostra organització no paga les despeses personals que apareixen a la factura de la targeta de crèdit corporativa. En lloc d'això, l'empleat paga el proveïdor de targetes de crèdit directament per les despeses. 
  - **Pagat per l'empresa:** la vostra organització paga la factura completa de la targeta de crèdit empresarial i, a continuació, carrega la quantitat de les despeses personals en el compte del treballador.

Podeu seleccionar el mètode que utilitza la vostra organització a la pàgina **Paràmetres de l'administració de despeses**.


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a>Habilitar la funció de despesa dividida quan el camp d'import personal té un valor definit

La característica **Habilita la funció de despesa dividida quan el camp d'import personal té un valor definit** només s'aplica als informes de despesa aprovats amb un flux de treball de nivell de línia. Els informes s'aproven anant a **Processa els informes de despesa** > **Informes de despesa que tinc assignats** > **Obre l'informe de despesa**. 

Per habilitar aquesta característica, aneu a **Àrees de treball** > **Administració de característiques**, seleccioneu **Habilita la funció de despesa dividida quan el camp d'import personal té un valor definit** i, a continuació, seleccioneu **Habilita ara**. 

Quan la característica està habilitada, les línies de despesa que utilitzen aquesta funcionalitat generen dues línies en enviar l'informe. Es generen dues línies per tal que l'aprovador pugui aprovar cada línia per separat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
