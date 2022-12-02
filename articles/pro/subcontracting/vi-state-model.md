---
title: Transicions d'estat en una factura del proveïdor
description: En aquest article s'expliquen les transicions d'estat en una factura de proveïdor del Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261004"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transicions d'estat en una factura del proveïdor

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest article s'expliquen les transicions d'estat en una factura de proveïdor del Microsoft Dynamics 365 Project Operations. S'utilitzen els estats següents: **Esborrany**, **En revisió**, **Confirmat**, **Retingut** i **Cancel·lat**.

Les il·lustracions següents mostren les transicions d'estat.

![Model de transicions d'estat del subcontracte.](../media/VI_State_Model.jpg)

La taula següent explica què representa cada estat en el cicle de vida d'una factura de proveïdor al Project Operations.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Aquest estat és l'estat inicial d'una factura del proveïdor. Les línies i els preus estan subjectes a modificacions. Una factura del proveïdor en aquest estat es pot editar i suprimir. | En curs |
| En revisió | Aquest estat representa l'estat de processament d'una factura del proveïdor. Com a mínim una línia de factura del proveïdor té l'estat de verificació **En curs**. | Confirmada, Retinguda |
| Confirmat | Aquest estat representa la fase d'una factura del proveïdor en que l'aplicació ha creat valors reals de cost per a cada línia de factura del proveïdor. Els valors reals de cost enllaçats que s'han aparellat amb les línies de factura del proveïdor s'han revertit i se substitueixen pels valors reals de cost d'aquestes línies de factura del proveïdor. Una factura del proveïdor en aquest estat no es pot editar ni suprimir. Podeu utilitzar el botó **Cancel· la** per cancel·lar una factura del proveïdor confirmada. L'acció Cancel·la inverteix l'impacte de l'acció Confirma. | Cancel·lada |
| Retingut | <p>Aquest estat representa una fase d'una factura del proveïdor en què la factura del proveïdor no es pot desplaçar a causa d'un problema amb la factura o l'estat del proveïdor. Una factura del proveïdor en aquest estat no es pot confirmar, cancel·lar, editar ni suprimir.</p><p>Podeu utilitzar l'acció Torna a obrir per desplaçar la factura del proveïdor a l'estat **Esborrany** o **En revisió**. Si almenys una línia de la factura del proveïdor té un estat de verificació **En curs** o **Completa**, la factura del proveïdor es tornarà a obrir en l'estat **En revisió**. Si totes les línies de la factura del proveïdor tenen un estat de verificació de **No iniciada**, la factura del proveïdor es tornarà a obrir en estat d'**Esborrany**.</p> | Esborrany, En revisió |
| Cancel·lada | Aquest estat representa la fase d'un subcontracte en què ja no es necessita el lliurament real de materials i/o treball per part de recursos subcontractats. Un subcontracte en aquest estat no es pot utilitzar per calcular i dotar els requisits del projecte amb recursos i materials ni s'hi pot fer referència en el temps, la despesa i l'ús de materials d'un projecte. Un subcontracte en aquest estat no es pot editar ni suprimir. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
