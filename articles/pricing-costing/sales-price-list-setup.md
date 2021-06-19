---
title: Configuració d'una llista de preus de vendes
description: En aquest tema es proporciona informació sobre les llistes de preus de vendes per als preus del projecte.
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004879"
---
# <a name="set-up-a-sales-price-list"></a>Configuració d'una llista de preus de vendes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Per a les ofertes i els contractes del projecte, una llista de preus de projecte té un patró de substitució de preu diferent que una llista de preus de producte. En una línia d'oferta basada en un catàleg de productes, podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta, perquè cada línia d'oferta apunta a exactament un element del catàleg. Tanmateix, en una línia d'oferta basada en projectes, no podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta. Podeu utilitzar la llista de preus del projecte per treballar amb els dos patrons de substitució diferents.

> [!NOTE]
> Es recomana que tingueu una llista de preus separada per als recursos del projecte i per als elements del catàleg, a causa de les diferències de comportament entre les dues en substituir els preus.

Cadascuna de les entitats següents pot tenir una o diverses llistes de preus associades per a preus del projecte:

- Client (compte) 
- Oportunitat 
- Oferta 
- Contracte de projecte

L'associació d'aquestes entitats amb una llista de preus s'indica a les llistes de preus del projecte. Podeu associar una o diverses llistes de preus amb les entitats de vendes Client, Oportunitat, Oferta i Contracte del projecte.

Una llista de preus de projecte per defecte no s'introdueix automàticament en un registre de client. No obstant, podeu adjuntar manualment una llista de preus de projecte al registre de client. De totes maneres, heu d'adjuntar manualment una llista de preus de projecte només quan tingueu un acord de preus personalitzat amb el client. 

Quan una llista de preus de projecte s'adjunta a una entitat de vendes, es valida la següent informació:

- La llista de preus té un context de **Vendes**. 
- La moneda de la llista de preus coincideix amb la moneda del client. 

En un contracte de projecte, s'utilitza el següent ordre de precedència per definir automàticament les llistes de preus relacionades amb el projecte:

1. Oferta
2. Oportunitat
3. Client 
4. Configuració global 

Quan una llista de preus de projecte s'introdueix per defecte, el sistema valida que la moneda coincideix amb la moneda del client i que les llistes de preus per defecte que s'han introduït tenen un context de **Vendes**.

Podeu associar diverses llistes de preus amb les entitats Client, Oportunitat, Oferta i Contracte del projecte. Aquesta capacitat admet els preus per defecte específics d'una data per a un contracte de projecte de llarg termini, on podeu necessitar més d'una llista de preus per explicar les actualitzacions dels preus que es produeixen a causa de la inflació. No obstant, si les llistes de preus que s'associen amb l'entitat Client, Oportunitat, Oferta o Contracte del projecte tenen una data d'efectivitat que se solapa, els preus per defecte podrien ser incorrectes. Per tant, heu d'assegurar-vos que les llistes de preus de projecte que tenen una data d'efectivitat que se solapa no estan associades amb aquestes entitats.


[!INCLUDE[footer-include](../includes/footer-banner.md)]