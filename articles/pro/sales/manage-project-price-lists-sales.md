---
title: Administració de les llistes de preus de projectes a les ofertes de projectes
description: En aquest tema es proporciona informació sobre treballar amb llistes de preus del projecte en ofertes. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072135"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Administració de les llistes de preus de projectes a les ofertes de projectes (Sales)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les ofertes del projecte estan dissenyades per admetre llistes de preus de vendes efectives de diverses dates. Amb el Dynamics 365 Project Operations, s'afegirà una entitat associada nova anomenada **Llistes de preus del projecte**. Aquesta entitat té una relació d'1 a diversos a una oferta de projecte.

Les llistes de preus del projecte s'utilitzen per assignar preus a les transaccions de temps i de despeses en un projecte. Quan una oferta té una o diverses llistes de preus de projecte, aquestes llistes de preus s'utilitzen per assignar preus a les estimacions i valors reals de temps i despeses als projectes associats a l'oferta a través de la línia d'oferta.

Quan no hi hagi cap llista de preus del projecte en una oferta de projecte, rebreu un missatge d'advertiment. El missatge indica que, com que no hi ha cap llista de preus del projecte, el treball i les despeses del projecte estimades i reals no tindran un preu. En lloc d'això, tindran un preu zero (0) per als valors de venda.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associar o anul·lar l'associació d'una llista de preus de projecte en una oferta de projecte

Per crear o seleccionar una llista de preus concreta per estimar el treball i les despeses basades en projectes, seguiu aquests passos:

1. A l'oferta, seleccioneu la pestanya **Preu del projecte** i, a la subquadrícula, seleccioneu **+ Afegeix una llista de preus del projecte nova**.
2. A la pàgina de creació ràpida, seleccioneu una llista de preus. A la llista desplegable es mostren totes les llistes de preus que tenen el context definit com a **Vendes** i la moneda coincideix amb la moneda de l'oferta.
4. Introduïu una descripció per a l'associació d'una llista de preus del projecte i seleccioneu **Desa i tanca**.

Es crea una associació de llista de preus del projecte.

Podeu repetir aquest procés si heu d'associar més d'una llista de preus de projecte a l'oferta del projecte. Creeu només diverses llistes de preus de projecte si teniu diverses dates efectives a cadascuna de les llistes de preus del projecte associades.

> [!NOTE]
> El Project Operations no admet la superposició de la data d'efectivitat de les llistes de preus del projecte. Si hi ha diverses llistes de preus de projectes per a una transacció amb la data indicada, el preu de la transacció per defecte serà zero (0).
Per suprimir una associació de la llista de preus del projecte, seleccioneu la llista de preus del projecte i, a continuació, seleccioneu **Suprimeix la llista de preus del projecte de l'oferta**. La llista de preus se suprimeix de les llistes de preus del projecte de l'oferta, però la llista de preus no se suprimeix. Només se suprimeix l'associació a l'oferta.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurar llistes de preus per defecte del projecte en una oferta

Les llistes de preus del projecte es poden configurar per defecte en una oferta de projecte. Aquesta configuració garanteix que totes les ofertes de l'organització sempre comencin per una llista de preus estàndard per a aquest període de preu.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurar un valor per defecte organitzatiu per a les llistes de preus del projecte

1. Aneu a **Configuració** > **General** > **Paràmetres**.
2. A la pàgina de llista **Paràmetres actius** , localitzeu el registre i feu-hi doble clic per obrir-lo. 
3. A la pàgina **Paràmetres** , seleccioneu la pestanya **Llista de preus**. Podeu veure la llista de llistes de preus per defecte que es mostra. Es tracta d'una llista estàndard de llistes de preus de costos i vendes. Si teniu una llista de preus de vendes associada aquí per a cada moneda amb què veneu, s'assegurarà que aquesta llista de preus de vendes s'utilitzi per defecte en qualsevol oferta que es creï per als clients que realitzin transaccions en aquesta moneda.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurar llistes de preus de projecte específiques de clients

Les llistes de preus de projecte específiques de clients també es poden configurar quan heu negociat un acord de preus mestre amb els clients.

Per configurar una llista de preus de projecte específica del client, seguiu els passos següents.

1. A l'àrea **Vendes** , seleccioneu **Clients**.
2. A la llista de comptes actius, seleccioneu i obriu el registre de client per al qual teniu la llista de preus especial.
3. A la pestanya **Llistes de preus del projecte** , podeu crear una nova associació de llista de preus per tal que la llista de preus del projecte sigui específica d'aquest client.

## <a name="create-custom-pricing-on-a-project-quote"></a>Crear un preu personalitzat en una oferta de projecte

Quan tingueu llistes de preus de projecte per defecte específiques de l'organització i específiques del client, les ofertes del projecte es crearan automàticament amb aquestes associacions de preus de projecte. No obstant, en determinats casos, pot ser que hàgiu de crear preus personalitzats per a una oferta de projecte concreta. 

1. A **Oferta del projecte** , a la pestanya **Llista de preus del projecte** , comproveu a la subquadrícula que no s'ha seleccionat cap registre de llista de preus concret.
2. Seleccioneu **Crea preus personalitzats**. Això crearà còpies de totes les llistes de preus estàndard associades actualment a l'oferta i associarà aquestes còpies a l'oferta. Les associacions existents a preus estàndard se suprimiran. A continuació, el comercial pot començar a fer edicions en els preus en aquestes còpies. Aquests preus canviats seran aplicables només a aquest oferta de projecte.
