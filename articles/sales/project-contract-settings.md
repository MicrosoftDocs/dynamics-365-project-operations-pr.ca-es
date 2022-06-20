---
title: Configuració de contractes de projecte
description: En aquest article s'ofereix informació sobre els camps que afecten les línies de contracte i la informació sobre el contracte que es resumeix en tots els elements de la línia.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1c3317eb36a98e14074fb504cfac5ff6e25fa3a0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921566"
---
# <a name="header-details-for-project-based-contracts"></a>Detalls de la capçalera per als contractes basats en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest article s'ofereix informació sobre els camps que s'apliquen a tot el contracte del projecte, inclosa la configuració que afecta totes les línies de contracte. També s'inclou informació sobre el contracte que es resumeix en tots els elements de la línia per impulsar els KPI del contracte de projecte.

A la taula següent es detallen els camps d'un contracte de projecte que són exclusius del Dynamics 365 Project Operations o que tenen alguns canvis importants en el comportament de les comandes de vendes al Dynamics 365 Sales.

| Camp | Location | Descripció | Impacte descendent |
| --- | --- | --- | --- |
| Type | Pestanya **Resum** (oculta) | Aquest és un camp de conjunt d'opcions amb les opcions següents:</br>- **Basat en treball** (disponible només quan s'instal·la el Project Operations)</br>- **Basat en elements** (disponible només quan s'instal·len el Project Operations i el Sales)</br>- **Basat en el manteniment del servei** (disponible quan el Dynamics 365 Field Service està instal·lat) | Al Project Operations, el valor d'aquest camp per defecte és **Basat en el treball** i classifica el contracte com a contracte basat en projectes. Un contracte ha d'estar basat en projectes per habilitar totes les extensions i funcionalitats específiques del projecte. |
| Empresa propietària | Pestanya **Resum** | Entitat jurídica que assumeix els costos i els ingressos que s'acumulen dels projectes associats amb aquest contracte del projecte. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. | L'empresa propietària equival al concepte d'entitat jurídica en el mòdul **Administració de projectes i comptabilitat** del Project Operations. Totes les despeses i ingressos acumulats d'aquest projecte es comptabilitzaran al registre general de l'empresa propietària. |
| Client | Pestanya **Resum** | Referència al registre d'empresa o compte del client. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. | La moneda del contracte del projecte es genera per defecte a partir de la moneda del client. La moneda es pot canviar després desar el contracte. |
| Administrador de comptes | Pestanya **Resum** | Nom de l'administrador de comptes per a aquest acord. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. | L'administrador del compte s'encarrega d'administrar la relació amb el client per mitjà de la finalització del projecte. En funció del registre de recurs reservable vinculat a l'administrador de comptes, es determina el valor per defecte al contracte del projecte. |
| Unitat de contractació | Pestanya **Resum** | La unitat de l'organització responsable del lliurament dels projectes associats amb aquest contracte. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. | La unitat de contractació és la divisió de l'empresa que executarà els projectes, Cada unitat de contractació té una moneda, i aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant el projecte. |
| Llista de preus del producte | Pestanya **Resum** | Aquesta la llista de preus s'utilitza per obtenir els preus per defecte a les línies de contracte basades en productes. A la llista d'opcions desplegables es mostra una llista de llistes de preus en què la moneda de la llista de preus coincideix amb la moneda del contracte. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. Al contracte del projecte, aquest camp té el valor per defecte del registre del compte però es pot canviar. | No hi ha cap rellevància descendent per a aquest camp. |
| Moneda | Pestanya **Resum** | Moneda utilitzada per notificar el valor d'aquest acord i moneda en què es facturarà el client. Quan es crea un contracte a partir d'una oferta, aquest camp es copia des del camp corresponent al registre d'oferta. Al contracte del projecte, aquest camp té el valor per defecte del registre del compte però es pot canviar. | Després de desar un contracte, aquest camp ja no es pot editar. Aquest camp s'utilitza per obtenir les llistes de preus de productes i projectes per defecte del contracte. La moneda del contracte s'utilitza per fer coincidir la moneda de la llista de preus. |
| Límit que no s’ha de superar | Pestanya **Resum** | Aquest camp indica el límit negociat sobre el valor final que el client ha acordat per a aquest acord. | El màxim s'avalua durant l'execució i s'aplica a tots els elements de la línia i als projectes associats amb aquest acord. |
| Data de lliurament sol·licitada | Pestanya **Resum** | Quan es crea un contracte a partir d'una oferta de projecte, aquest camp es copia des del camp corresponent a l'oferta de projecte. | Aquesta data s'utilitza com a data d'acabament per a la generació de planificacions de factura. |

Els KPI següents estan disponibles a la pestanya **Rendiment del contracte** d'un contracte de projecte.

| Camp | Location | Descripció |
| --- | --- | --- |
| Valor del contracte | Contracte general | Valor total del contracte del projecte. |
| Import facturat | Contracte general | Suma dels imports en totes les factures d'aquest contracte. |
| Cost acumulat | Contracte general | Suma de tots els valors reals registrats en tots els projectes que s'assignen al contracte. |
| Marge brut | Contracte general | Import facturat - cost incorregut fins a la data/import facturat |
| Marge esperat | Contracte general | (Valor del contracte - costos previstos)/valor del contracte Costos estimats = suma de tots els costos previstos en tots els projectes assignats al contracte.|
| Valor del contracte | Línies basades en projectes | Valor de la línia de contracte. |
| Import facturat | Línies basades en projectes | Per a una línia de contracte de preu fix: suma dels imports en tots els valors reals de fita de venda facturats en relació amb aquesta línia de contracte en diverses factures creades per a aquest contracte. Per a una línia de contracte de temps i material: suma dels imports en tots els valors reals imputables de venda facturats en relació amb aquesta línia de contracte en diverses factures creades per a aquest contracte. |
| Cost acumulat | Línies basades en projectes | Suma de tots els valors reals registrats en tots els projectes que s'assignen a la línia de contracte. |
| Marge brut | Línies basades en projectes | (Import facturat - cost incorregut fins a la data)/import facturat |
| Marge esperat | Línies basades en projectes | (Import de la línia de contracte en la moneda base - costos previstos per a la línia de contracte en la moneda base)/import de la línia de contracte en la moneda base |
| Cost acumulat | Detall d'una línia basada en projectes | Temps: suma de l'import dels valors reals de cost de temps registrat per a aquesta funció al projecte assignada a la línia de contracte. Despeses: suma de l'import de tots els valors reals de cost de despeses registrat per a aquesta categoria al projecte assignada a la línia de contracte. |
| Quantitat registrada | Detall d'una línia basada en projectes | Temps: tota la quantitat de temps als valors reals de cost de temps per a una funció al projecte assignada a aquesta línia de contracte. Despeses: totes les quantitats per a aquesta categoria de despeses registrades als valors reals de cost de despeses al projecte s'assignen a aquesta línia de contracte. |
| Import facturat | Detall d'una línia basada en projectes | Per a una línia de contracte de preu fix, aquest camp es deixa en blanc a nivell de detall i només es mostra a nivell de línia de contracte. Per a una línia de contracte de temps i material, els càlculs es completen al nivell de detalls. Els detalls mostren la suma de l'import en totes les línies d'ingressos facturats d'aquesta línia de contracte que són imputables. |
| Quantitat facturada | Detall d'una línia basada en projectes | Per a una línia de contracte de preu fix, aquest camp es deixa en blanc a nivell de detall i només es mostra a nivell de línia de contracte. Per a una línia de contracte de temps i material, els càlculs es completen al nivell de detalls per a temps i despeses. Temps: suma de les hores en totes les línies d'ingressos facturats per a aquesta funció d'aquesta línia de contracte que són imputables. Despeses: totes les quantitats per a aquesta categoria de despeses registrades als valors reals de cost de despeses al projecte s'assignen a aquesta línia de contracte. |
| Valor del contracte | Línies basades en el producte | Valor de la línia de contracte d'aquesta línia de contracte basada en productes. |
| Import facturat | Línies basades en el producte | Suma dels imports a totes les línies de factura de la línia de contracte basada en productes en diverses factures creades per a aquest contracte. |
| Cost acumulat | Línies basades en el producte | Suma de tots els valors reals registrats per a la línia de contracte basada en productes. |
| Marge brut | Línies basades en projectes | Import facturat - cost incorregut fins a la data/import facturat |
| Marge esperat | Línies basades en el producte | (Valor de la línia de contracte - costos estimats per a la línia de contracte)/valor de la línia de contracte |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
