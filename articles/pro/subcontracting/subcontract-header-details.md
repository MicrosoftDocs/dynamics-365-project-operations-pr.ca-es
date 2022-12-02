---
title: Detalls de la capçalera per als subcontractes
description: En aquest article s'explica la funcionalitat proporcionada a la capçalera del subcontracte a Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 00b7c08235654d4bed0bcb4053d2044a3d092b54
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522548"
---
# <a name="header-details-for-subcontracts"></a>Detalls de la capçalera per als subcontractes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest article s'explica la funcionalitat proporcionada a la capçalera del subcontracte al Dynamics 365 Project Operations.

Quan un Administrador de projectes planifica i executa projectes, pot recórrer a subcontractistes i comprar productes i serveis a proveïdors. Quan un Administrador de projectes ha de comprar productes o serveis, pot crear un subcontracte al Project Operations.

Per crear un subcontracte, seguiu aquests passos.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i, a la pàgina **Subcontracte**, seleccioneu **Crea**.
2. Introduïu la informació requerida i seleccioneu **Desa**.

    La taula següent proporciona informació sobre els camps de la pàgina **Capçalera de subcontracte**.

    | Camp | Descripció |Impacte funcional |
    |---|------|---| 
    | Nom | El nom del subcontracte. | A totes les llistes desplegables del subcontracte, el nom del subcontracte es mostra a la primera columna per ajudar-vos a identificar el subcontracte. | 
    | Descripció | Descripció breu dels serveis i productes que es compren al subcontracte. | Cap |
    | Proveïdor | Nom de l'empresa a la qual es compren els productes i serveis. Aquest registre de compte té un tipus de relació de **Proveïdor** o **Distribuïdor**. | En funció del proveïdor seleccionat, els valors per defecte s'introdueixen automàticament per als camps següents:<br/> **• Moneda** </br> **• Llistes de preus** </br> **• Condicions de pagament**</br> **• Adreça de pagament**</br> **• Adreça de facturació**</br> **• Nom de facturació** </br>**• Administrador de compte del proveïdor**|
    | Data de subcontracte | La data en què es crea el subcontracte. | La data del subcontracte s'utilitza per seleccionar la llista de preus de compra correcta de les llistes de preus adjuntades al proveïdor relacionat o dels paràmetres del projecte. |
    | Raó per a l’estat | Estat del subcontracte. | L'estat determina on es troba el subcontracte en el procés empresarial i si es pot editar. <br/>Els valors inclouen:<br>• **Esborrany**: el subcontracte es pot editar. Només podeu editar les subcontractes amb l'estat **Esborrany**.<br/>• **Confirmat**: la negociació amb el proveïdor està completa i el subcontracte s'aprova per al seu lliurament. <br/>• **Tancat**: el lliurament del subcontracte s'ha completat.<br/>• **Cancel·lat**: el subcontracte s'ha cancel·lat i no s'ha previst cap lliurament.  | 
    | Moneda | Moneda en què es compren els productes i serveis. El valor per defecte s'introdueix automàticament des del compte del proveïdor, però es pot canviar. | La moneda del subcontracte s'utilitza per seleccionar la llista de preus de compra de les llistes de preus adjuntades al proveïdor relacionat o dels paràmetres del projecte. Les llistes de preus en una altra moneda no es poden associar amb el subcontracte. El cost del temps, les despeses i els materials que els recursos del proveïdor lliuren d'aquest subcontracte es registren en aquesta moneda al projecte. Després de desar el registre del subcontracte, la moneda del subcontracte no es pot canviar.|
    | Unitat de contractació | Divisió de l'empresa que està celebrant un contracte de compra o un subcontracte amb el proveïdor. | Cap |
    | Condicions de pagament | Condicions de pagament de les factures de proveïdor que s'emeten en aquest subcontracte. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Les condicions de pagament del subcontracte es copien a totes les factures del proveïdor relacionades amb aquest subcontracte. Les condicions de pagament es poden actualitzar si el subcontracte té l'estat **Esborrany**. | 
    | Adreça de pagament | Adreça del proveïdor a la qual s'han d'enviar els pagaments. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | L'adreça de pagament del subcontracte es copia com l'adreça de pagament a totes les factures del proveïdor creades per a aquest subcontracte. L'adreça de pagament es pot actualitzar si el subcontracte té l'estat **Esborrany**.|
    | Nom de facturació | Nom de la persona o divisió de l'empresa del proveïdor que enviarà la factura. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | El valor de **Nom de facturació** del subcontracte es copia a totes les factures del proveïdor relacionades amb aquest subcontracte. Aquest camp es pot actualitzar si el subcontracte té l'estat **Esborrany**.|
    | Adreça de facturació | Adreça utilitzada en les factures del proveïdor. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. | Aquesta adreça és l'adreça "factura de" a les factures del proveïdor creades per a aquest subcontracte. |
    | Subtotal | Si un subcontracte no té línies, introduïu el subtotal de la comanda abans dels impostos. Si el subcontracte té línies, aquest camp és només de lectura. L'import que es mostra és l'import subtotal de totes les línies del subcontracte. | Cap |
    | Impostos totals | Si un subcontracte no té línies, introduïu els impostos totals d'aquest subcontracte. Si el subcontracte té línies, aquest camp és només de lectura. L'import que es mostra és la suma dels impostos de totes les línies del subcontracte. | Cap |
    | Import total | Aquest camp calculat mostra la quantitat total del subcontracte després d'incloure-hi els impostos. | Cap |
    | Data de confirmació | Data en què s'ha confirmat el subcontracte. | Cap |
    | Sol·licitat per | Per defecte, aquest camp està definit com el nom de l'usuari que crea el subcontracte. Tanmateix, l'autor del subcontracte pot canviar el valor per indicar la persona en nom de la qual estan creant el subcontracte. | Cap |
    | Administrador de compte del proveïdor | Nom del contacte principal del compte del proveïdor. El valor per defecte s'introdueix automàticament des del registre del compte de proveïdor. Podeu seleccionar un contacte diferent com a administrador del compte del subcontracte. | Podeu configurar alertes de correu electrònic per notificar el contacte quan es fan canvis al subcontracte com a resultat de negociacions de preus. |
