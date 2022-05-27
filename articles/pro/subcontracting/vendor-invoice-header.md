---
title: Detalls de la capçalera per a les factures del proveïdor
description: En aquest tema s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor a Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17be106d5486358ff0bbf011af3da26a4c85a274
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575568"
---
# <a name="header-details-for-vendor-invoices"></a>Detalls de la capçalera per a les factures del proveïdor

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest tema s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor a Microsoft Dynamics 365 Project Operations.

A mesura que els gestors de projectes planifiquen i executen projectes, poden contractar subcontractistes i comprar productes i serveis de proveïdors. Durant l'execució d'un projecte, els costos s'incorren en serveis, materials i categories de despeses que s'adquireixen en subcontractes amb proveïdors. Els proveïdors facturen aquests costos als projectes creant factures de proveïdor.

La taula següent proporciona informació sobre els camps de les capçaleres de factura del proveïdor a Les operacions del projecte.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la factura del proveïdor. | A totes les llistes desplegables de factures del proveïdor, el nom de la factura del proveïdor es mostra a la primera columna per ajudar-vos a identificar la factura del proveïdor. Per defecte, quan es crea una factura de proveïdor a partir d'una subcontracta, el **camp Nom** de la factura del proveïdor s'estableix en un valor que consisteix en el nom de la subcontracta més la data actual. |
| Descripció | Breu descripció dels serveis i productes que s'estan facturant a la factura del proveïdor. | cap |
| Proveïdor | El nom de l'empresa que factura els productes i serveis. Aquesta empresa ha de ser un registre de compte que tingui un tipus de relació de **Proveïdor** o **Proveïdor**. | <p>En funció del proveïdor seleccionat, els valors per defecte s'introdueixen automàticament als camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul> |
| Subcontracte | Una referència a la subcontractació de la factura del proveïdor. | <p>En funció de la subcontracta seleccionada, els valors per defecte s'introdueixen automàticament als camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul><p>La subcontractació seleccionada a la capçalera de la factura del proveïdor s'introdueix per defecte a les línies de factura del proveïdor i no es pot canviar allà.</p> |
| Data de la factura | La data dels reals de cost que es crearan quan es confirmi la factura del proveïdor. | La data de la factura també s'utilitza per seleccionar la llista correcta de preus de compra, ja sigui des de les llistes de preus que s'adjunten al proveïdor relacionat o des dels paràmetres del projecte. |
| Raó per a l’estat | L'estat de la factura del proveïdor. | <p>L'estat determina on es troba la factura del proveïdor al procés de negoci i si es pot editar. Aquests són alguns dels valors disponibles:</p><ul><li>**Esborrany** : la factura del proveïdor es pot editar.</li><li>**Confirmat** : la factura del proveïdor ha estat verificada i confirmada. Les factures del proveïdor d'aquest estat no es poden editar ni suprimir.</li><li>**En procés** : s'està revisant la factura del proveïdor. Les factures del proveïdor d'aquest estat es poden editar, però no es poden suprimir.</li><li>**S'ha cancel·lat** : s'ha cancel·lat la factura del proveïdor. Les factures del proveïdor d'aquest estat no es poden editar ni suprimir.</li></ul> |
| Moneda | La moneda en què el proveïdor factura els productes i serveis de la factura del proveïdor. | En una factura de proveïdor que fa referència a una subcontracta, la moneda de la subcontractació s'introdueix per defecte com a moneda de la factura del proveïdor. En una factura de proveïdor que no fa referència a una subcontracta, el valor per defecte s'introdueix des del registre del compte de proveïdor i es pot canviar. Després de desar una factura de proveïdor, la moneda ja no es pot editar. |
| Unitat de contractació | La divisió de l'empresa que s'encarrega de rebre els serveis i/o productes del venedor. | cap |
| Condicions de pagament | Les condicions de pagament de les factures del proveïdor que s'emeten. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Les condicions de pagament d'una subcontracta es copien a totes les factures del proveïdor relacionades amb la subcontractació. Les condicions de pagament es poden actualitzar si la factura del proveïdor té l'estat d'Esborrany **·**. |
| Adreça de pagament | Adreça del proveïdor a la qual s'han d'enviar els pagaments. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | L'adreça de pagament d'una subcontracta es copia com a adreça de pagament a totes les factures del proveïdor que es creen per a aquesta subcontractació. L'adreça de pagament es pot actualitzar si la factura del proveïdor té l'estat d'Esborrany **·**. |
| Subtotal | Si la factura del proveïdor no té línies, introduïu el subtotal de la factura abans d'impostos. Si la factura del proveïdor té línies, aquest camp només és de lectura. En aquest cas, l'import que es mostra és l'import subtotal de totes les línies de la factura del proveïdor. | cap |
| Total d'impostos | Si la factura del proveïdor no té línies, introduïu els impostos totals sobre la subcontracta. Si la factura del proveïdor té línies, aquest camp només és de lectura. En aquest cas, l'import que es mostra és la suma d'imports fiscals de totes les línies de la factura del proveïdor. | cap |
| Import total | Aquest camp calculat mostra l'import total de la factura del proveïdor després d'incloure els impostos. | cap |

> [!NOTE]
> Els camps següents d'una factura de proveïdor no es poden canviar després de desar la factura del proveïdor: Proveïdor, Subcontractació **,** Moneda **,** Unitat **de contractació i** Condicions **de pagament.** **·** Si es requereixen canvis en aquests camps d'una factura de proveïdor, heu de suprimir la factura del proveïdor i crear una factura de proveïdor nova.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
