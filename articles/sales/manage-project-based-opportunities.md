---
title: Administració d'oportunitats basades en projectes
description: Aquest tema proporciona informació sobre com treballar amb oportunitats relacionades amb els projectes.
author: rumant
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d640bda1f325c283e591eb8d1a100d4e6b09d76ae847833e9664c3631eabd154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991879"
---
# <a name="manage-project-based-opportunities"></a>Administració d'oportunitats basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les empreses basades en projectes solen tenir les seves operacions de lliurament distribuïdes entre països i zones geogràfiques. El cost de l'execució i lliurament del projecte pot variar en funció de la zona geogràfica o divisió que gestiona el lliurament. Al seu torn, això pot afectar els marges de l'acord. El lliurament de serveis basats en projectes sol implicar grans quantitats de temps de recursos humans, despeses considerables per a viatges, costos materials i altres despeses.

Les oportunitats basades en projectes al Dynamics 365 Project Operations estan dissenyades amb extensions del Dynamics 365 Sales. El tema proporciona detalls sobre els diferents camps i la lògica empresarial inclosa en la funcionalitat addicional que necessiten les empreses basades en projectes per administrar les oportunitats basades en projectes.

## <a name="view-all-project-based-opportunities"></a>Visualitzar totes les oportunitats basades en projectes

Es pot veure una llista de totes les oportunitats basades en projectes des de la pàgina de llista **Oportunitat**. 

1. Aneu a **Vendes** > **Oportunitats**.
2. Utilitzeu el **Commutador de visualització** per seleccionar altres visualitzacions filtrades de les oportunitats. Podeu crear les vostres pròpies visualització amb criteris de filtratge personalitzats per configurar aquestes visualitzacions i opcions de navegació.

Les oportunitats del projecte es poden crear o suprimir des d'aquesta pàgina de llista o la pàgina de detalls.

## <a name="business-process-flow-for-project-based-deals"></a>Flux del procés de negoci per a acords basats en projectes

Els fluxos del procés de negoci següents s'admeten per als acords basats en projectes al Project Operations:

- Procés de negoci de client potencial a oportunitat
- Procés de vendes d'oportunitat

### <a name="lead-to-opportunity-business-process"></a>Procés de negoci de client potencial a oportunitat 
El procés de negoci de client potencial a oportunitat admet les fases següents:

| Fase | Entitat assignada | Funcionalitat |
| --- | --- | --- |
| Qualifica | Client potencial | Qualifiqueu el client potencial per crear un compte, un contacte i una oportunitat. |
| Desenvolupament | Oportunitat | Desenvolupeu l'oportunitat per afegir més informació sobre el treball implicat, les parts interessades clau i la competència. |
| Proposa | Oportunitat | Desenvolupeu la proposta i obteniu l'aprovació de l'equip de revisió intern. |
| Tanca  | Oportunitat | Guanyeu l'oportunitat per tancar l'acord. |

### <a name="opportunity-sales-process"></a>Procés de vendes d'oportunitat
El procés de vendes d'oportunitats al Project Operations és una extensió del flux de negoci del procés de vendes d'oportunitat a l'aplicació Sales. Aquest procés de negoci està dissenyat de fàbrica per admetre les següents fases en una oportunitat basada en projectes.

| Fase | Entitat assignada | Funcionalitat |
| --- | --- | --- |
| Qualifica | Oportunitat | Qualifiqueu el client potencial per crear un compte, un contacte i una oportunitat. |
| Proposa | Oferta | Desenvolupeu la proposta mitjançant ofertes de projecte i obteniu l'aprovació de l'equip de revisió intern. |
| Contracte | Contracte de projecte | Guanyeu l'oferta per crear el contracte i començar l'execució i el lliurament del projecte. |
| Tanca  | Contracte de projecte | Acabeu el treball amb èxit i tanqueu el contracte del projecte. |

> [!NOTE]
> Si el vostre acord basat en projectes va començar amb un client potencial, el procés de negoci de client potencial a oportunitat té prioritat.
>
> Si el vostre acord basat en projectes va començar amb una oportunitat, el procés de venda d'oportunitat té prioritat.

Podeu editar el flux del procés de negoci del producte o crear els vostres propis fluxos del procés de negoci per fer un seguiment del vostre procés de vendes segons sigui necessari. Per obtenir més informació sobre el flux del procés de negoci, vegeu [Informació general dels fluxos del procés de negoci](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).


[!INCLUDE[footer-include](../includes/footer-banner.md)]