---
title: Administració de diversos clients en contractes de projectes
description: Aquest article proporciona informació sobre com administrar diversos clients en un contracte de projecte.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928328"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Administració de diversos clients en contractes de projectes

Aquest article proporciona informació sobre com administrar diversos clients en un contracte de projecte. Podeu utilitzar un contracte de projecte quan es necessiti un acord contractual per a diversos clients per al finançament d'un tracte. A la pàgina **Contracte de projecte**, la pestanya **Resum** inclou informació sobre el client principal d'un tracte. Altres clients que participen en el tracte es poden afegir a la pestanya **Clients**.

Tots els clients de contracte de la pestanya **Clients** del contracte de projecte són per defecte els clients de línia de contracte en qualsevol línia de contracte nova basada en projecte que es creï per al contracte de projecte. Les línies de contracte basades en projecte existents no hereten els registres de clients de contracte nous que es creen posteriorment.

Podeu afegir, actualitzar o suprimir clients de contracte i de línia de contracte en qualsevol moment abans de guanyar el contracte. Un client del contracte de projecte s'ha d'establir com a client a l'empresa propietària o a l'entitat jurídica a la pàgina **Clients**. Les entitats jurídiques es configuren al mòdul **Gestió de projectes i comptabilitat** del Dynamics 365 Project Operations i estan disponibles com a empreses als mòduls **Vendes de projecte** i **Lliuraments** de Project Operations.

## <a name="primary-customers"></a>Clients principals

El client potencial de la pestanya **Resum** del contracte de projecte és el client principal del contracte. No podeu actualitzar el client principal des de la llista de clients del contracte. Si intenteu suprimir el client principal d'una llista de clients del contracte, es produirà un error que indicarà que un registre de client principal d'un contracte no es pot suprimir. En lloc d'això, canvieu el client al camp **Client potencial** de la pestanya **Resum** del contracte de projecte. Quan aquest camp s'actualitza, el client nou seleccionat s'afegeix com a client de contracte nou amb la marca **Principal** definida com a **Sí**. El client principal anterior encara és un client del contracte, però ja no és el client principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Crear, actualitzar o suprimir un registre de client de contracte

Podeu crear, actualitzar o suprimir un client de contracte de la pestanya **Clients de contracte** de la pàgina **Contracte**. Els camps següents s'inclouen al registre de client de contracte d'un contracte de projecte.

| **Camp** | **Ubicació** | **Descripció** | 
| --- | --- | --- | 
| Compte | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Enumera tots els comptes actius. Aquest camp està blocat quan es crea el registre. Per actualitzar el registre, heu de suprimir-lo i tornar-lo a crear. Si heu registrat cap valor real o si el registre de client del contracte és un client principal, no podeu suprimir el registre. Quan es crea una línia de contracte, els clients del contracte es copien com a clients de la línia de contracte. |
| Percentatge dividit de facturació | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Representa el percentatge de cada transacció de vendes no facturada que s'atribueix al client de contracte. Quan es creen noves línies de contracte de projecte, el percentatge de divisió de facturació es copia a les noves línies de contracte creades i als clients de la línia de contracte del projecte. |
| Nom de contacte de facturació | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Aquest camp de text s'ha d'utilitzar per identificar la persona de contacte de la factura per al client. El valor per defecte prové del registre del compte relacionat. El nom del contacte es copia a **Factura al nom del contracte** de la factura generada per al client. |
| Nom de facturació | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Utilitzeu aquest camp per identificar la persona de contacte de la factura per al client. El valor per defecte prové del registre del compte relacionat. El nom es copia al camp **Factura al nom del contracte** de la factura generada per al client. |
| Condicions de pagament | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | El valor per defecte prové del registre del compte relacionat. Els termes es copien a **Factura al nom del contracte** de la factura generada per al client. |
| Empresa propietària | Quadrícula editable a la pestanya **Clients de contracte de projecte** i a les pàgines de creació principal i ràpida d'un client de contracte de projecte. | L'entitat jurídica en la qual es configura el client al mòdul **Gestió de projectes i comptabilitat**. Aquest camp és només de lectura i està definit com a l'empresa propietària del contracte de projecte.</br>La llista de clients que s'afegeixen al camp **Compte** ja està filtrada a la llista de l'empresa propietària al mòdul **Administració de projectes i comptabilitat** del Project Operations. L'empresa propietària és igual a l'entitat jurídica en el mòdul **Gestió de projectes i comptabilitat** de Project Operations. Tots els costos i ingressos meritats pel projecte es comptabilitzen en el llibre major de l'empresa propietària. |
| És arrodoniment | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Indica si el client és un client d'arrodoniment per defecte per al tracte. Només hi pot haver un client d'arrodoniment en un contracte de projecte. Quan els costos i les vendes no facturades es divideixen per quantitat i generen una diferència d'arrodoniment, aquesta diferència s'aplica al valor real que s'assigna al client. |
| Límit que no s’ha de superar | Quadrícula editable a la pestanya **Clients de contracte** i a les pàgines de creació principal i ràpida d'un client de contracte. | Indica si hi ha un límit o màxim negociat a l'import global que es facturarà al client per la interacció. El límit que no s'ha de superar configurat a nivell del client de contracte s'avalua en funció dels valors reals de vendes no facturades que fan referència a aquest client de contracte. |

## <a name="edit-billing-split-percentages"></a>Edició dels percentatges de divisió de la facturació

Podeu editar els percentatges de divisió de facturació a la quadrícula. Quan els percentatges de divisió de facturació no sumen el 100 per cent, es produeix un error. Després d'editar un percentatge de divisió de facturació, actualitzeu la pàgina **Contracte de projecte** per eliminar l'error.

També podeu seleccionar **Distribueix uniformement** a la subquadrícula de clients de contracte de projecte. Les divisions de facturació s'assignen equitativament a tots els clients del contracte de projecte. Si hi ha cap factor d'arrodoniment, s'afegirà al client d'arrodoniment. Un dels clients del contracte sempre té l'indicador **Arrodoniment** definit com a **Sí**. Aquest client és el client d'arrodoniment. Normalment, el client d'arrodoniment és també el client principal del contracte, però no és necessari.


[!INCLUDE[footer-include](../includes/footer-banner.md)]