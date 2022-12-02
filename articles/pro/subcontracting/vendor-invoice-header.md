---
title: Detalls de la capçalera de les factures del proveïdor
description: En aquest article s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor del Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261641"
---
# <a name="header-details-for-vendor-invoices"></a>Detalls de la capçalera de les factures del proveïdor

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest article s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor del Microsoft Dynamics 365 Project Operations.

Quan els administradors de projectes planifiquen i executen projectes, poden recórrer a subcontractistes i comprar productes i serveis a proveïdors. Durant l'execució d'un projecte, s'incorren costos de serveis, materials i categories de despeses que s'obtenen de subcontractes amb proveïdors. Els proveïdors facturen aquests costos als projectes creant factures de proveïdor.

La taula següent proporciona informació sobre els camps de les capçaleres de factura de proveïdor al Project Operations.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la factura de proveïdor. | A totes les llistes desplegables de factura de proveïdor, el nom de la factura de proveïdor es mostra a la primera columna per ajudar-vos a identificar la factura de proveïdor. Per defecte, quan es crea una factura de proveïdor a partir d'un subcontracte, el camp **Nom** de la factura de proveïdor es defineix en un valor que consisteix en el nom del subcontracte i la data actual. |
| Descripció | Descripció breu dels serveis i productes que es facturen a la factura de proveïdor. | cap |
| Proveïdor | Nom de l'empresa que factura els productes i serveis. Aquesta empresa ha de ser un registre de compte que tingui un tipus de relació de **Proveïdor** o **Distribuïdor**. | <p>En funció del proveïdor seleccionat, els valors per defecte s'introdueixen automàticament per als camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul> |
| Subcontracte | Referència al subcontracte de la factura de proveïdor. | <p>En funció del subcontracte seleccionat, els valors per defecte s'introdueixen automàticament per als camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul><p>El subcontracte seleccionat a la capçalera de la factura de proveïdor s'introdueix per defecte a les línies de factura de proveïdor i no es pot canviar allà.</p> |
| Data de la factura | La data dels valors reals de cost que es crearan quan es confirmi la factura de proveïdor. | La data de factura també s'utilitza per seleccionar la llista de preus de compra correcta de les llistes de preus adjuntades al proveïdor relacionat o dels paràmetres del projecte. |
| Raó per a l’estat | Estat de la factura de proveïdor | <p>L'estat determina on es troba la factura de proveïdor en el procés empresarial i si es pot editar. Alguns dels valors disponibles són:</p><ul><li>**Esborrany**: la factura de proveïdor es pot editar.</li><li>**Confirmat**: la factura de proveïdor s'ha verificat i confirmat. Les factures de proveïdor en aquest estat no es poden editar ni suprimir.</li><li>**En procés** : la factura de proveïdor s'està revisant. Les factures de proveïdor en aquest estat es poden editar, però no suprimir.</li><li>**Cancel·lat** : la factura de proveïdor s'ha cancel·lat. Les factures de proveïdor en aquest estat no es poden editar ni suprimir.</li></ul> |
| Moneda | Moneda en què factura el proveïdor per als productes i serveis de la factura de proveïdor. | En una factura de proveïdor que fa referència a un subcontracte, la moneda del subcontracte s'introdueix per defecte com a moneda de la factura de proveïdor. En una factura de proveïdor que no fa referència a un subcontracte, el valor per defecte s'introdueix des del registre de compte del proveïdor i es pot canviar. Quan una factura de proveïdor es desa, la moneda ja no es pot editar. |
| Unitat de contractació | Divisió de l'empresa responsable de rebre els serveis i/o productes del proveïdor. | cap |
| Condicions de pagament | Condicions de pagament de les factures de proveïdor que s'emeten. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Les condicions de pagament d'un subcontracte es copien a totes les factures del proveïdor relacionades amb el subcontracte. Les condicions de pagament es poden actualitzar si la factura de proveïdor té l'estat **Esborrany**. |
| Adreça de pagament | Adreça del proveïdor a la qual s'han d'enviar els pagaments. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | L'adreça de pagament d'un subcontracte es copia com l'adreça de pagament a totes les factures del proveïdor creades per al subcontracte. L'adreça de pagament es pot actualitzar si la factura de proveïdor té l'estat **Esborrany**. |
| Subtotal | Si la factura de proveïdor no té línies, introduïu el subtotal de la factura abans dels impostos. Si la factura de proveïdor té línies, aquest camp és només de lectura. En aquest cas, l'import que es mostra és l'import subtotal de totes les línies de la factura de proveïdor. | cap |
| Impostos totals | Si la factura de proveïdor no té línies, introduïu el total d'impostos del subcontracte. Si la factura de proveïdor té línies, aquest camp és només de lectura. En aquest cas, l'import que es mostra és la suma dels imports d'impostos de totes les línies de la factura de proveïdor. | cap |
| Import total | Aquest camp calculat mostra la quantitat total de la factura de proveïdor després d'incloure-hi els impostos. | cap |

> [!NOTE]
> Els camps següents d'una factura de proveïdor no es poden canviar després de desar la factura de proveïdor: **Proveïdor**, **Subcontracte**, **Moneda**, **Unitat de contractació** i **Condicions de pagament**. Si cal fer algun canvi en aquests camps en una factura de proveïdor, haureu de suprimir la factura de proveïdor i crear una factura de proveïdor nova.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
