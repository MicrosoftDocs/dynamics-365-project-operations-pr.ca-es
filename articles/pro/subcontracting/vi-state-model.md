---
title: Transicions d'estat en una factura del proveïdor
description: En aquest article s'expliquen les transicions d'estat en una factura de proveïdor a Microsoft Dynamics 365 Project Operations.
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

En aquest article s'expliquen les transicions d'estat en una factura de proveïdor a Microsoft Dynamics 365 Project Operations. S'utilitzen els estats següents: **Esborrany**, **En revisió**, **Confirmat**, **En espera** i **Cancel·lat**.

Les il·lustracions següents mostren les transicions d'estat.

![Model de transició estatal subcontractada.](../media/VI_State_Model.jpg)

La taula següent explica què representa cada estat en el cicle de vida d'una factura de proveïdor a Project Operations.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Aquest estat és l'estat inicial d'una factura de proveïdor. Les línies i els preus estan subjectes a modificacions. Una factura de proveïdor en aquest estat es pot editar i suprimir. | En procés |
| En revisió | Aquest estat representa l'estat de tramitació d'una factura de proveïdor. Almenys una línia de factures de proveïdor té un estat de verificació de **En curs**. | Confirmat, En espera |
| Confirmat | Aquest estat representa l'etapa d'una factura de proveïdor on l'aplicació ha creat reals de costos per a cada línia de factura del proveïdor. Tots els reals de costos vinculats que coincidien amb les línies de factures del proveïdor s'han invertit i substituït pels reals de costos d'aquestes línies de factures de proveïdors. Una factura de proveïdor en aquest estat no es pot editar ni suprimir. Podeu utilitzar el botó Cancel·la **per** cancel·lar una factura de proveïdor confirmada. L'acció Cancel·la reverteix l'impacte de l'acció Confirma. | Cancel·lada |
| Retingut | <p>Aquest estat representa una etapa d'una factura de proveïdor en què la factura de proveïdor no es pot moure a causa d'un problema amb la factura o l'estat del proveïdor. Una factura de proveïdor en aquest estat no es pot confirmar, cancel·lar, editar ni suprimir.</p><p>Podeu utilitzar l'acció Torna a obrir per moure la factura de proveïdor a l'estat **Esborrany** o **En revisió**. Si almenys una línia de la factura del proveïdor té un estat de verificació d'En curs o Completa, la factura del proveïdor es tornarà a obrir a l'estat **En revisió**.**·** **·** Si totes les línies de la factura del proveïdor tenen un estat de verificació de **No iniciat**, la factura del venedor es tornarà a obrir a l'estat **Esborrany**.</p> | Esborrany, En revisió |
| Cancel·lada | Aquest estat representa l'etapa d'una subcontractació on ja no es requereix el lliurament real de materials i/o treballs per recursos subcontractats. Una subcontracta en aquest estat no es pot utilitzar per estimar i els requisits del projecte de personal per a recursos i materials, i tampoc no es pot fer referència sobre el temps, la despesa i l'ús de material en un projecte. Un subcontractat en aquest estat no es pot editar ni suprimir. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
