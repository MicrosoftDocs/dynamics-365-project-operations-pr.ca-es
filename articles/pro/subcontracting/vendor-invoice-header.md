---
title: Detalls de la capçalera de les factures del proveïdor
description: En aquest article s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor a Microsoft Dynamics 365 Project Operations.
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

En aquest article s'explica la funcionalitat que es proporciona a la capçalera de la factura del proveïdor a Microsoft Dynamics 365 Project Operations.

A mesura que els gestors de projectes planifiquen i executen projectes, poden contractar subcontractistes i comprar productes i serveis a proveïdors. Durant l'execució d'un projecte, els costos s'incorren en serveis, materials i categories de despeses que s'adquireixen en subcontractes amb proveïdors. Els venedors facturen aquests costos als projectes creant factures de proveïdors.

La taula següent proporciona informació sobre els camps de les capçaleres de factures de proveïdor del Project Operations.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la factura del venedor. | A totes les llistes desplegables de factures de proveïdor, el nom de la factura de proveïdor es mostra a la primera columna per ajudar-vos a identificar la factura de proveïdor. Per defecte, quan es crea una factura de proveïdor a partir d'un subcontractista, el **camp Nom** de la factura del venedor s'estableix en un valor que consisteix en el nom del subcontractista més la data actual. |
| Descripció | Una breu descripció dels serveis i productes que s'estan facturant a la factura del venedor. | cap |
| Proveïdor | El nom de l'empresa que factura els productes i serveis. Aquesta empresa ha de ser un registre de compte que tingui un tipus de relació de **proveïdor** o **proveïdor**. | <p>Segons el proveïdor seleccionat, els valors per defecte s'introdueixen automàticament als camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul> |
| Subcontracte | Una referència a la subcontractació de la factura del venedor. | <p>A partir de la subcontractació seleccionada, els valors per defecte s'introdueixen automàticament en els camps següents:</p><ul><li>Moneda</li><li>Llistes de preus</li><li>Condicions de pagament</li><li>Adreça de pagament</li></ul><p>El subcontractista seleccionat a la capçalera de la factura del proveïdor s'introdueix per defecte a les línies de factura del proveïdor i no es pot canviar allà.</p> |
| Data de la factura | La data dels reals de cost que es crearan quan es confirmi la factura del proveïdor. | La data de factura també s'utilitza per seleccionar la llista de preus de compra correcta, ja sigui de les llistes de preus que s'adjunten al proveïdor relacionat o dels paràmetres del projecte. |
| Raó per a l’estat | L'estat de la factura del venedor. | <p>L'estat determina on es troba la factura del proveïdor en el procés de negoci i si es pot editar. Aquests són alguns dels valors disponibles:</p><ul><li>**Esborrany** : es pot editar la factura del proveïdor.</li><li>**Confirmat** - La factura del proveïdor s'ha verificat i confirmat. Les factures de proveïdor en aquest estat no es poden editar ni suprimir.</li><li>**En procés** - S'està revisant la factura del proveïdor. Les factures de proveïdor en aquest estat es poden editar, però no es poden suprimir.</li><li>**Cancel·lat** - La factura del venedor s'ha cancel·lat. Les factures de proveïdor en aquest estat no es poden editar ni suprimir.</li></ul> |
| Moneda | La moneda en què el venedor factura els productes i serveis de la factura del venedor. | En una factura de venedor que fa referència a un subcontractista, la moneda del subcontractat s'introdueix per defecte com a moneda de la factura del venedor. En una factura de proveïdor que no fa referència a un subcontractista, el valor per defecte s'introdueix des del registre del compte de proveïdor i es pot canviar. Després de desar una factura de proveïdor, la moneda ja no es pot editar. |
| Unitat de contractació | La divisió de l'empresa que s'encarrega de rebre els serveis i/o productes del venedor. | cap |
| Condicions de pagament | Les condicions de pagament de les factures de proveïdors que s'expedeixen. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Les condicions de pagament d'un subcontractat es copien a totes les factures dels proveïdors que estiguin relacionades amb la subcontractació. Les condicions de pagament es poden actualitzar si la factura del proveïdor té l'estat **esborrany**. |
| Adreça de pagament | Adreça del proveïdor a la qual s'han d'enviar els pagaments. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Es copia l'adreça de pagament d'un subcontractista com a adreça de pagament a totes les factures de proveïdors que es creen per a aquesta subcontractació. L'adreça de pagament es pot actualitzar si la factura del venedor té l'estat **Esborrany**. |
| Subtotal | Si la factura del venedor no té línies, introduïu el subtotal de factura abans d'impostos. Si la factura del proveïdor té línies, aquest camp només es llegeix. En aquest cas, l'import que es mostra és l'import subtotal de totes les línies de la factura del proveïdor. | cap |
| Impost total | Si la factura del venedor no té línies, introduïu els impostos totals del subcontractat. Si la factura del proveïdor té línies, aquest camp només es llegeix. En aquest cas, l'import que es mostra és la suma de les quantitats impositives de totes les línies de la factura del venedor. | cap |
| Import total | Aquest camp calculat mostra l'import total de la factura de proveïdor després d'incloure els impostos. | cap |

> [!NOTE]
> Els camps següents d'una factura de proveïdor no es poden canviar després de desar la factura del proveïdor: Proveïdor, Subcontractat **,** Moneda **,** Unitat **de contractació i** Condicions **de pagament.** **·** Si es requereix algun canvi en aquests camps d'una factura de proveïdor, heu de suprimir la factura de proveïdor i crear una factura de proveïdor nova.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
