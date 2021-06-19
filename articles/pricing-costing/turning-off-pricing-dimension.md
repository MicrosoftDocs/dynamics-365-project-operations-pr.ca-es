---
title: Desactivació d'una dimensió de preus
description: En aquest tema, podreu obtenir informació sobre com desactivar dimensions de preus.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004519"
---
# <a name="turning-off-a-pricing-dimension"></a>Desactivació d'una dimensió de preus

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Pot ser que hàgiu de revisar i actualitzar l'estratègia de preus cada pocs anys. Pot ser que les actualitzacions que feu exigeixin que desactiveu una dimensió de preus existent i que en creeu una de nova. Per exemple, pot ser que hàgiu tingut un preu per **Funció**, però ara hàgiu decidit definir preus per **Experiència laboral**. Potser necessitareu desactivar **Funció** com a dimensió de preus i que creeu **Experiència de treball** com a nova dimensió de preus. 

Desactivar una dimensió de preus, independentment de si és personalitzada o per defecte, pot fer-se definint els camps **Aplicable al cost** i **Aplicable a les vendes** de la dimensió de preus com a **No**.

No obstant, en fer-ho, pot ser que rebeu el missatge d'error **La dimensió de preus no es pot actualitzar ni suprimir si hi ha registres de preu associats.**

![Error de procés empresarial probable quan desactiveu una dimensió de preus](media/Business-Process-Error.png)

Aquest missatge d'error indica que hi ha registres de preus que abans s'havien configurat per a la dimensió que s'està desactivant. Tots els registres **Preu per funció** i **Marge comercial de preu per funció** que facin referència a una dimensió s'han de suprimir abans que l'aplicabilitat de la dimensió pugui definir-se com a **No**. Aquesta regla s'aplica a les dues dimensions de preus per defecte i a les dimensions de preus personalitzades que hàgiu creat. La raó d'aquesta validació és que cada registre **Preu per funció** ha de tenir una combinació única de dimensions. Per exemple, en una llista de preus anomenada **Tarifes de costos dels EUA 2018**, teniu les files **Preu per funció** següents. 

| Càrrec estàndard         | Unitat organitzativa    |Unitat   |Preu  |Moneda  |
| -----------------------|-------------|-------|-------|----------|
| Enginyer de sistemes|Contoso US|Hora| 100|USD|
| Enginyer de sistemes sènior|Contoso US|Hora| 150| USD|


Quan desactiveu **Càrrec estàndard** com a dimensió de preus, i el motor de preus cerqui un preu, només utilitzarà el valor **Unitat organitzativa** del context d'entrada. Si la **Unitat organitzativa** del context d'entrada és "Contoso US", el resultat serà no determinista perquè ambdues files coincidiran. Per evitar aquest escenari, quan creeu registres **Preu per funció**, el sistema valida que la combinació de dimensions és única. Si la dimensió s'ha desactivat després de crear els registres **Preu per funció**, aquesta restricció es pot violar. Per tant, és necessari que abans de desactivar una dimensió, suprimiu totes les files **Preu per funció** i **Marge comercial de preu per funció** que tenen aquest valor de dimensió amb valors.


[!INCLUDE[footer-include](../includes/footer-banner.md)]