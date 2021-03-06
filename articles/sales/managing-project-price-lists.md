---
title: Llistes de preus del projecte
description: Aquest tema proporciona informació sobre l'entitat Llista de preus del projecte.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: d09a0dd8234641ca106c37a38d1d721dfb07236c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898654"
---
# <a name="project-price-lists"></a>Llistes de preus del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations amplia l'entitat Llista de preus del Dynamics 365 Sales. 

## <a name="key-entities"></a>Entitats clau

Una llista de preus inclou informació proporcionada per quatre entitats diferents:

- **Llista de preus:** aquesta entitat emmagatzema informació sobre el context, la moneda, l'efectivitat de la data i la unitat de temps per al temps de fixació de preus. El context mostra si la llista de preus expressa les tarifes de cost o les tarifes de vendes. 
- **Moneda**: aquesta entitat emmagatzema la moneda del preu a la llista de preus. 
- **Data**: aquesta entitat s'utilitza quan el sistema prova d'introduir un preu per defecte d'una transacció. Se selecciona la llista de preus que té l'efectivitat de la data que inclou la data de la transacció. Si es troba més d'una llista de preus que és efectiva per a la data de la transacció i s'adjunta a la unitat de cotització, contracte o organització, llavors no s'adopta cap preu per defecte. 
- **Hora**: aquesta entitat emmagatzema la unitat de temps en què s'expressen els preus per a les tarifes diàries o per hora. 

L'entitat Llista de preus té tres taules relacionades que emmagatzemen els preus:

  - **Preu per funció**: aquesta taula emmagatzema una tarifa per a una combinació de valors de funció i unitat organitzativa i s'utilitza per configurar els preus basats en funcions dels recursos humans.
  - **Preu de la categoria de la transacció**: aquesta taula emmagatzema els preus per categoria de transacció i s'utilitza per configurar els preus de les categories de despesa.
  - **Elements de la llista de preus**: aquesta taula emmagatzema les tarifes dels productes del catàleg.
 
La llista de preus és una targeta de tarifes. Una targeta de tarifes és una combinació de l'entitat Llista de preus i les files relacionades a les taules Preu per funció, el Preu de la categoria de la transacció i Elements de la llista de preus.

## <a name="resource-roles"></a>Funcions de recursos

El terme *funció de recurs* fa referència a un conjunt d'aptituds, competències i certificacions que ha de tenir una persona per dur a terme un conjunt específic de tasques en un projecte.

El temps dels recursos humans s'ofereix en funció del paper que compleix un recurs d'un projecte específic. Per al temps de recursos humans, el cost i la facturació es basen en la funció del recurs. Es pot definir un preu per temps en qualsevol unitat del grup **Unitats de temps**.

El grup d'unitats **Temps** es crea en instal·lar el Project Operations. Té una unitat **Hora** per defecte. No podeu suprimir, canviar el nom o editar els atributs del grup d'unitats **Temps** o la unitat **Hora**. No obstant, podeu afegir altres unitats al grup d'unitats **Temps**. Si proveu de suprimir el grup d'unitats **Temps** o la unitat **Hora**, pot ser que provoqueu fallades en la lògica empresarial.
 
## <a name="transaction-categories-and-expense-categories"></a>Categories de transacció i de despeses

Els viatges i altres despeses que comporten els consultors dels projectes es facturen al client. Els preus de les categories de despesa es completen mitjançant llistes de preus. Tarifes aeroportuàries, hotel i lloguer de cotxes són exemples de categories de despeses. Cada línia de llista de preus per a les despeses especifica el preu d'una categoria de despesa concreta. Els tres mètodes següents s'utilitzen per definir el preu de les categories de despeses:

- **Al cost**: el cost de la despesa es factura al client, i no s'aplica cap marge comercial.
- **Percentatge de marge comercial**: el percentatge del cost real es factura al client. 
- **Preu per unitat**: un preu de facturació es defineix per a cada unitat de la categoria de despesa. L'import que es factura al client es calcula en funció del nombre d'unitats de despesa que informa el consultor. El quilometratge utilitza el mètode de preus de preu per unitat. Per exemple, la categoria de despesa de quilometratge es pot configurar a 30 dòlars americans (USD) per dia o 2 USD per milla. Quan un consultor informa del quilometratge en un projecte, l'import a facturar es calcula a partir del nombre de milles que va informar el consultor.
 
## <a name="project-sales-pricing-and-overrides"></a>Preus de vendes de projectes i substitucions

Per a les ofertes i els contractes del projecte, una llista de preus de projecte té un patró de substitució de preu diferent que una llista de preus de producte. En una línia d'oferta basada en un catàleg de productes, podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta, perquè cada línia d'oferta apunta a exactament un element del catàleg. Tanmateix, en una línia d'oferta basada en projectes, no podeu substituir el preu a les funcions i a les categories directament a la línia d'oferta. Utilitzeu la llista de preus del projecte per admetre els dos patrons de substitució diferents.

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

### <a name="deal-specific-price-overrides"></a>Substitucions de preu específiques per a una oferta

Podeu crear substitucions específiques per a un acord per a les tarifes seleccionades a les llistes de preus del projecte que s'introdueixen per defecte en una oferta o en un contracte de projecte.

Per defecte, un contracte de projecte sempre obté una còpia de la llista de preus de vendes mestra en comptes d'un enllaç directe. Aquest comportament ajuda a garantir que els acords de preus que es facin amb un client per a una declaració de treball (SOW) no canvien si la llista de preus mestra es canvia.

No obstant, en una oferta, podeu utilitzar una llista de preus mestra. Si ho preferiu, podeu copiar una llista de preus mestra i editar-la per crear una llista de preus personalitzada que només s'apliqui a aquesta oferta. Per crear una llista de preus específica d'una oferta, a la pàgina **Oferta**, seleccioneu **Crea un preu personalitzat**. Podeu accedir a la llista de preus de projecte específica d'un acord només des de l'oferta. 

Quan creeu una llista de preus de projecte personalitzada, només es copien els components del projecte de la llista de preus. En altres paraules, una nova llista de preus creada com a còpia de la llista de preus del projecte existent que s'adjunta a l'oferta, i aquesta llista de tarifes nova només té preus relacionats amb els preus per funció i la categoria de transacció.
  
## <a name="tracking-costs"></a>Seguiment de costos

El Project Operations segueix els costos per a l'ús del temps de recursos humans en projectes. També fa el seguiment dels costos d'altres despeses que es generen durant el projecte, com ara les despeses de viatge.

Com les tarifes de facturació, les tarifes de cost de recursos humans també es configuren mitjançant llistes de preus. A continuació, es mostren les diferències principals en el comportament de la llista de preus de costos i la llista de preus de vendes:

- La tarifa de cost d'un recurs no es pot substituir per a un projecte, un contracte o una oferta específics. No obstant això, les tarifes de facturació es pot substituir segons l'acord si es fan canvis que són específics de la naturalesa de l'acord. 

- Per resoldre una llista de preus de cost, s'utilitza l'ordre següent:

    1. La llista de preus de cost adjunta a la unitat de l'organització.
    2. La llista de preus de cost adjunta als paràmetres del Project Operations. Com que les llistes de preus de cost en moltes monedes diferents poden adjuntar-se a paràmetres, es completa una coincidència de moneda de la unitat organitzativa del contractant del projecte, el contracte o l'oferta i la moneda de la llista de preus de cost.
    3. Per a les despeses, els mètodes de preus a partir del cost i de marge comercial sobre el cost no s'apliquen a les llistes de preus de cost. Fins i tot si aquests mètodes de preus s'utilitzen a les línies de llista de preus de cost per configurar els costos de categoria de la transacció, el sistema els ignora i no s'introdueix cap preu de cost per defecte.
