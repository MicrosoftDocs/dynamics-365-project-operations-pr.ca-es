---
title: Informació resumida d'una oferta de projecte (vendes)
description: Aquest tema proporciona informació sobre la informació i la configuració que s'apliquen i tenen un impacten en les ofertes del projecte. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d050258ae457bb4392d5fa761442cfc7a444feb0
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966737"
---
# <a name="summary-information-on-a-project-quote-sales"></a>Informació resumida d'una oferta de projecte (vendes)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

En aquest article s'explica la informació que s'aplica a una oferta de projecte. Això inclou la configuració que té un impacte en totes les línies d'oferta i informació sobre l'oferta que es resumeix en tots els elements de línia per impulsar els KPI de l'oferta del projecte.

A la taula següent s'enumeren els camps d'informació resumida d'una oferta de projecte que són únics del Dynamics 365 Project Operations o que tenen canvis importants en el comportament de les ofertes del Dynamics 365 Sales.

| **Camp** | **Ubicació** | **Rellevància, propòsit i orientació** | **Impacte descendent** |
| --- | --- | --- | --- |
| Type | Pestanya Resum (oculta) | Aquest camp de conjunt d'opcions té les opcions següents:</br>- Basat en treball (disponible només quan s'instal·la el Project Operations)</br>- Basat en elements (disponible només quan s'instal·len el Project Operations i el Sales)</br>- Basat en el manteniment del servei (disponible quan el Dynamics 365 Field Service està instal·lat) | Quan utilitzeu l'aplicació Project Operations, el valor d'aquest valor de camp es defineix automàticament com a **Basat en el treball**. Això classifica l'oferta com a oferta basada en projectes. Una oferta ha de ser basada en projectes per habilitar totes les extensions i funcionalitats específiques del projecte. |
| Client potencial | Pestanya de resum | Referència al registre d'empresa o compte del client. Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. | La moneda de l'oferta de projecte es genera per defecte a partir de la moneda del client. Això, no obstant, es pot canviar després desar l'oferta. |
| Administrador de comptes | Pestanya de resum | Nom de l'administrador de comptes per a aquest acord. Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. | L'administrador del compte s'encarrega d'administrar la relació amb el client per mitjà de la finalització d'aquest projecte. En funció del registre de recurs reservable vinculat a l'administrador de comptes, es determina el valor per defecte a l'oferta del projecte. |
| Unitat de contractació | Pestanya de resum | Unitat de l'organització responsable del lliurament del projecte o projectes associats amb aquesta oferta. Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. | Unitat de contractació és la divisió de l'empresa que executarà els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda, i aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant l'execució del projecte. |
| Llista de preus del producte | Pestanya de resum | Aquesta és la llista de preus que s'utilitza per obtenir els preus per defecte a les línies d'oferta basades en productes. A la llista d'opcions d'aquest camp es mostra una llista de llistes de preus en què la moneda de la llista de preus coincideix amb la moneda de l'oferta. Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. Aquest camp de l'oportunitat té el valor per defecte del registre del compte però es pot canviar. | El valor d'aquest camp es copia a la línia de contracte del projecte que es crea des d'aquesta línia d'oferta en guanyar l'oferta. |
| Moneda | Pestanya de resum | Això indica la moneda que s'utilitzarà per informar del valor d'aquest acord. També és la moneda en què es facturarà al client si es guanya l'acord. Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. Aquest camp de l'oportunitat té el valor per defecte del registre del compte però l'usuari el pot canviar. | Després de desar una oferta, aquest camp ja no es pot editar. S'utilitza per obtenir les llistes de preus de productes i projectes per defecte de l'oferta. La moneda de l'oferta s'utilitza per fer coincidir la moneda de la llista de preus. |
| Límit que no s’ha de superar | Pestanya de resum | Això indica el límit negociat sobre el valor final que el client ha acordat per a aquest acord. | Aquest màxim s'avalua durant l'execució i s'aplica a tots els elements de la línia i als projectes associats amb aquest acord. |
| Data de lliurament sol·licitada | Pestanya de resum | Quan es crea una oferta a partir d'una oportunitat, aquest camp es copia des del camp corresponent a l'oportunitat. | Aquesta data s'utilitza com a data d'acabament per a la generació de planificacions de factura. |

A continuació es mostren les pestanyes i els KPI disponibles en una oferta de projecte que són únics per al Project Operations o que tenen canvis importants al comportament de les ofertes del Sales:

| **Camp** | **Ubicació** | **Rellevància, propòsit i orientació** |
| --- | --- | --- |
| Anàlisi de rendibilitat | Pestanya a l'oferta | La pestanya mostra les mètriques següents:</br>- Cost imputable total</br></br>- Cost no imputable total</br>- Total d’ingressos</br>- Total d’ingressos (base)</br>- Marge brut</br>- Marge brut ajustat|
| Comparació amb les expectatives del client | Pestanya a l'oferta | Aquesta pestanya mostra les mètriques següents:</br>- Finalització estimada</br>- Finalització sol·licitada</br>- Pressupost del client</br>- Valor ofert |
| Anàlisi de l’oferta | Pestanya a l'oferta | Aquesta pestanya resumeix els següents KPI principals per a una oferta de projecte</br>- Comparació amb les expectatives del client del pressupost i de la planificació</br>- Marge brut</br>- Marge brut ajustat |
