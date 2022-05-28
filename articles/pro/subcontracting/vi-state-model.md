---
title: Transicions d'estat en una factura de proveïdor
description: En aquest tema s'expliquen les transicions d'estat d'una factura de proveïdor a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584676"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transicions d'estat en una factura de proveïdor

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest tema s'expliquen les transicions d'estat d'una factura de proveïdor a Microsoft Dynamics 365 Project Operations. S'utilitzen els estats següents: Esborrany, En revisió **,** Confirmat **,** En espera **i** Cancel·lat **.** **·**

Les següents il·lustracions mostren les transicions d'estat.

![Model de transició d'estat de subcontractació.](../media/VI_State_Model.jpg)

A la taula següent s'explica què representa cada estat al cicle de vida d'una factura de proveïdor a Les operacions del projecte.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Aquest estat és l'estat inicial d'una factura de proveïdor. Les línies i els preus estan subjectes a modificacions. Es pot editar i suprimir una factura de proveïdor d'aquest estat. | En procés |
| En revisió | Aquest estat representa l'estat de processament d'una factura de proveïdor. Com a mínim una línia de factura de proveïdor té l'estat de verificació de **En curs**. | Confirmat, En espera |
| Confirmat | Aquest estat representa la fase d'una factura de proveïdor on l'aplicació ha creat reals de cost per a cada línia de factura del proveïdor. Tots els reals de costos enllaçats que coincideixen amb les línies de factura del proveïdor s'han invertit i s'han substituït amb els reals de cost d'aquestes línies de factura del proveïdor. Una factura de proveïdor d'aquest estat no es pot editar ni suprimir. Podeu utilitzar el botó Cancel·**la** per cancel·lar una factura de proveïdor confirmada. L'acció Cancel·la reverteix l'impacte de l'acció Confirma. | Cancel·lada |
| Retingut | <p>Aquest estat representa una fase d'una factura de proveïdor en què la factura del proveïdor no es pot moure a causa d'un problema amb la factura o l'estat del proveïdor. Una factura de proveïdor d'aquest estat no es pot confirmar, cancel·lar, editar ni suprimir.</p><p>Podeu utilitzar l'acció Torna a obrir per desplaçar la factura del proveïdor a l'estat **Esborrany** o **En revisió**. Si almenys una línia de la factura del proveïdor té un estat de verificació de **En curs** o **Completat**, la factura del proveïdor es tornarà a obrir a l'estat **de revisió**. Si totes les línies de la factura del proveïdor tenen un estat de verificació de No iniciat **, la factura del** proveïdor es tornarà a obrir a l'estat **Esborrany**.</p> | Esborrany, en revisió |
| Cancel·lada | Aquest estat representa l'etapa d'una subcontracta on ja no es requereix el lliurament real de materials i /o treballs per recursos subcontractats. Una subcontracta en aquest estat no es pot utilitzar per estimar i el personal dels requisits del projecte per als recursos i materials, i tampoc es pot fer referència a temps, despesa i ús de material en un projecte. Una subcontracta d'aquest estat no es pot editar ni suprimir. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
