---
title: Detalls de la capçalera per als subcontractes
description: En aquest tema s'explica la funcionalitat proporcionada a la capçalera del subcontracte a Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323629"
---
# <a name="header-details-for-subcontracts"></a>Detalls de la capçalera per als subcontractes

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest tema s'explica la funcionalitat proporcionada a la capçalera del subcontracte al Dynamics 365 Project Operations.

Quan un Administrador de projectes planifica i executa projectes, pot recórrer a subcontractistes i comprar productes i serveis a proveïdors. Quan un Administrador de projectes ha de comprar productes o serveis, pot crear un subcontracte al Project Operations.

Per crear un subcontracte, seguiu aquests passos.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i, a la pàgina **Subcontracte**, seleccioneu **Crea**.
2. Introduïu la informació requerida i seleccioneu **Desa**.

    La taula següent proporciona informació sobre els camps de la pàgina de capçalera de Subcontracte.

    | **Camp** | **Descripció** |
    | --- | --- | 
    | Nom | El nom del subcontracte. |
    | Descripció | Descripció breu dels serveis i productes que es compren al subcontracte. |
    | Proveïdor | Nom de l'empresa a la qual es compren els productes i serveis. Aquest registre de compte té un tipus de relació de **Proveïdor** o **Distribuïdor**. |
    | Data de subcontracte | Data de creació del subcontracte. |
    | Raó per a l’estat | Estat del subcontracte. |
    | Moneda | Moneda en què es compren els productes i serveis. El valor d'aquest camp és per defecte el compte del proveïdor, però es pot canviar. Les llistes de preus del projecte que s'utilitzen per als preus dels productes i serveis del subcontracte haurien d'estar en aquesta moneda. Les llistes de preus en altres monedes no es poden associar amb el subcontracte. El cost dels productes i serveis incorreguts en aquest subcontracte es registrarà en el projecte en aquesta moneda. |
    | Unitat de contractació | Divisió de l'empresa que està celebrant un contracte de compra o un subcontracte amb el proveïdor. |
    | Condicions de pagament | Condicions de pagament de les factures del proveïdor que s'emeten en aquest subcontracte. El valor d'aquest camp és per defecte el registre del compte del proveïdor. |
    | Adreça de pagament | Adreça on s'envia el pagament a les factures del proveïdor. El valor d'aquest camp és per defecte el registre del compte del proveïdor. |
    | Nom de facturació | Nom de la persona o divisió de l'empresa del proveïdor que enviarà la factura. El valor d'aquest camp és per defecte el del registre del compte del proveïdor i s'utilitzarà com a nom del contacte principal a les factures del proveïdor creades per a aquest subcontracte. |
    | Adreça de facturació | Adreça utilitzada a les factures d'aquest proveïdor. El valor d'aquest camp és per defecte el registre del compte del proveïdor. Aquesta adreça s'utilitza també com a adreça de factura a les factures del proveïdor creades per a aquest subcontracte. |
    | Subtotal | Si un subcontracte no té línies, introduïu un valor en aquest camp que denoti el subtotal de la comanda abans d'impostos. Si el subcontracte té línies, aquest camp és només de lectura. La quantitat que es visualitza és la quantitat subtotal de totes les línies del subcontracte. |
    | Impostos totals | Si un subcontracte no té línies, introduïu un valor en aquest camp que denoti els impostos del subcontracte. Si el subcontracte té línies, aquest camp és només de lectura. La quantitat que es visualitza és la suma dels impostos de totes les línies del subcontracte. |
    | Import total |  Aquest camp calculat mostra la quantitat total del subcontracte després d'incloure-hi els impostos.  |
    | Data de confirmació | Data en què s'ha confirmat el subcontracte.  |
    | Sol·licitat per | El valor d'aquest camp és per defecte el nom de l'usuari que crea el subcontracte. Aquest valor el pot canviar l'autor del subcontracte per indicar la persona en nom de la qual es crea el subcontracte.  |
    | Administrador de compte del proveïdor | Nom del contacte principal del compte del proveïdor. El valor d'aquest camp és per defecte el registre del compte del proveïdor. Aquest valor de camp el pot canviar l'usuari per seleccionar un contacte diferent com a administrador del compte de proveïdor del subcontracte. Aquest contacte pot configurar i enviar alertes de correu electrònic i negociacions de preus. |


