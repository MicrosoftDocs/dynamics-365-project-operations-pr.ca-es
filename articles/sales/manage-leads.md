---
title: Administració de clients potencials
description: Aquest tema proporciona informació sobre l'administració de clients potencials basats en projectes.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 526f2ab1fd186877f32a2d11bd92ee8c26a19139
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278046"
---
# <a name="manage-leads"></a>Administració de clients potencials

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els clients potencials basats en projectes es poden administrar i qualificar al Project Operations. El procés d'administració de clients potencials inclou la creació de clients potencials basats en el treball i la qualificació dels clients potencials. 

## <a name="project-sales-leads"></a>Clients potencials de vendes del projecte

A la secció **Vendes**, a la subfinestra de navegació esquerra, obriu la pàgina de la llista **Clients potencials** per veure una llista de tots els registres de client potencial del sistema. La llista de clients potencials que es mostren són basats en treball i altres tipus de clients potencials que es poden crear si també teniu les aplicacions Dynamics 365 Sales o Dynamics 365 Field Service.

Podeu crear una visualització filtrada per veure només els clients potencials basats en projectes mitjançant la creació d'un filtre al valor **Tipus**. Per exemple, podeu seleccionar si voleu que només es mostrin clients potencials basats en el treball.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Crear un client potencial nou per a un acord basat en projectes

Quan es qualifica un client potencial basat en un projecte, es crearà una oportunitat i un compte. Una oportunitat basada en projectes és el punt de partida per a les activitats de cerca de vendes en la fase d'oportunitat. Les oportunitats basades en projectes tenen capacitats úniques necessàries per vendre treball del projecte. Aquestes capacitats inclouen:

- Mètode de facturació de temps i material i preu fix
- Llistes de preus eficaces de diverses dates per a recursos humans, despeses i materials incorreguts en projectes

Per tal que un client potencial qualificat creï automàticament una oportunitat, definiu l'atribut **Tipus** a **Basat en el treball** en el moment de crear el client potencial. Si trieu un tipus diferent, el client potencial no crearà una oportunitat basada en projectes en qualificar-lo. Si l'oportunitat basada en projectes no es crea, les capacitats específiques del projecte no estaran disponibles als processos de vendes descendents.

A la taula següent s'inclou informació de camp important per a un client potencial i les implicacions descendents d'aquests camps.
 
| **Camp** | **Ubicació** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Tema | Pestanya General | Aquest camp de text ha de contenir una breu descripció de l'acord. | El tema del client potencial serà per defecte com el tema de l'oportunitat i el nom de l'oferta i el contracte del projecte. |
| Type | Pestanya General | Aquest camp de conjunt d'opcions té les opcions següents:</br>- Basat en treball (disponible només quan s'instal·la el Project Operations)</br>- Basat en elements (disponible només quan s'instal·len el Project Operations i el Sales)</br>- Basat en el manteniment del servei (disponible quan el Field Service està instal·lat) | Quan el valor d'aquest camp està definit com a **Basat en el treball** en el client potencial, el client potencial està qualificat per crear una oportunitat basada en projectes. Es necessita una oportunitat basada en projectes per habilitar totes les extensions i funcionalitats específiques del projecte al procés de venda descendent per a aquest acord. |
| Nom | Pestanya General | Nom del contacte del donant potencial | Quan es qualifica el client potencial, es crearà un compte, un contacte i una oportunitat. El nom del contacte és el valor que es defineix aquí. |
| Cognom | Pestanya General | Cognom del contacte del donant potencial | Quan es qualifica el client potencial, es crearà un compte, un contacte i una oportunitat. El cognom del contacte és el valor que es defineix aquí. |
| Empresa | Pestanya General | Nom de l'empresa del client del donant potencial | Quan es qualifica el client potencial, es crearà un compte, un contacte i una oportunitat. El nom del compte creat és el valor que es defineix aquí. |
| Moneda | Pestanya Detalls | Moneda del client del donant potencial | Quan es qualifica el client potencial, es crearà un compte, un contacte i una oportunitat. La moneda del compte creat és el valor que es defineix aquí. |

## <a name="qualify-a-new-project-based-lead"></a>Qualificar un client potencial nou basat en projectes

Els clients potencials que tenen el valor **Tipus** definit com a **Basat en el treball** s'anomenen clients potencials basats en projectes. Quan es qualifica un client potencial basat en un projecte, es crea el següent:

- Un compte que utilitza el camp **Empresa** del client potencial.
- Un registre de contacte associat al compte segons els valors dels camps **Nom** i **Cognom** del client potencial.
- Una oportunitat basada en projectes que té el camp **Tipus** definit com a **Basat en treball**.

Per obtenir informació més detallada sobre els clients potencials qualificats, vegeu [Qualificar o convertir clients potencials](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Informació sobre la qualificació de clients potencials i les entitats jurídiques 

Quan executeu el Project Operations mitjançant el mode d'implementació, el Project Operations per a escenaris basats en recursos/sense cotització, cada client i oportunitat requerirà que s'hagi definit el camp **Empresa propietària**. L'empresa propietària és una entitat jurídica a la vostra organització propietària del lliurament del projecte. Cada client o compte amb el tipus de relació de client, ha de tenir el valor de camp **Entitat propietària** definit a l'entitat legal que contracta i negocia amb aquest client. Un client només pot ser en una entitat legal.

Quan es qualifica un client potencial, els registres de client i oportunitat creats tindran el camp **Empresa propietària** definit a l'empresa del registre de recurs reservable de l'usuari actual.

Si el registre de recurs reservable de l'usuari actual és buit, el valor del camp **Empresa propietària** del registre d'usuari s'utilitza per defecte als registres de client i oportunitat.

## <a name="business-process-flow-for-project-based-deals"></a>Flux del procés de negoci per a acords basats en projectes

Els fluxos del procés de negoci següents s'admeten per als acords basats en projectes al Project Operations:

- Procés de negoci de client potencial a oportunitat
- Procés de vendes d'oportunitat

El procés de negoci de client potencial a oportunitat admet les fases següents:

| Nom de la fase | Entitat assignada | Funcionalitat |
| --- | --- | --- |
| Qualifica | Client potencial | Qualifiqueu el client potencial per crear un compte, un contacte i una oportunitat. |
| Desenvolupament | Oportunitat | Desenvolupeu l'oportunitat per afegir més informació sobre el treball implicat, les parts interessades clau i la competència. |
| Proposa | Oportunitat | Desenvolupeu la proposta i obteniu l'aprovació de l'equip de revisió intern. |
| Tanca  | Oportunitat | Guanyeu l'oportunitat per tancar l'acord. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]