---
title: Administració de diversos clients a les ofertes de projectes
description: En aquest tema es proporciona informació sobre com treballar en les ofertes amb diversos clients que finançaran el projecte. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966738"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Administració de diversos clients a les ofertes de projectes (Sales)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les ofertes del projecte admeten l'escenari en què la proposta implica diversos clients que finançaran el tracte. La pestanya **Resum** de l'oferta té el camp **Client potencial**, que identifica el client principal del tracte. Altres clients per al tracte es poden configurar a la pestanya **Clients** de l'oferta del projecte.

Tots els clients de l'oferta de la pestanya **Clients** de l'oferta del projecte són per defecte clients de la línia d'oferta a les línies d'oferta basades en projectes **noves** creades per a l'oferta. Totes les línies de l'oferta basades en projectes no hereten els registres de client d'oferta nova que s'hagin creat després.

Les línies de l'oferta basades en productes s'associen automàticament amb el client principal que també és el client del camp **Client potencial** de la pestanya **Resum** de l'oferta.

Es poden afegir, actualitzar o suprimir els clients de l'oferta i els clients de la línia d'oferta en qualsevol moment abans de guanyar l'oferta.

## <a name="concept-of-a-primary-customer"></a>Concepte de client principal

Al client que apareix a la pestanya de resum de l'oferta del projecte com a client potencial és el client principal de l'oferta. Quan intenteu suprimir el client principal de la llista de clients de l'oferta, veureu un error indicant que no es pot suprimir un registre de client principal d'una oferta.

El client principal no s'ha d'actualitzar des de la llista de clients a l'oferta. No obstant, podeu influir en el client principal canviant el client potencial a la pestanya **Resum** de l'oferta. Quan s'actualitza aquest camp al **Resum de l'oferta**, el client potencial que acabeu de seleccionar s'afegeix com a client d'oferta nou amb la marca **Principal** definida. El client potencial antic continuarà sent un client de l'oferta.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Crear, actualitzar o suprimir un registre de client d'oferta

Es pot crear, actualitzar o suprimir un client d'oferta a la pestanya **Clients de l'oferta** de la pàgina **Oferta**. Els camps que es mostren a la taula següent estan al registre del client d'oferta d'una oferta de projecte.

| **Camp** | **Ubicació** | **Rellevància, propòsit i orientació** | **Impacte descendent** |
| --- | --- | --- | --- |
| Compte | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Enumera tots els comptes actius. Aquest camp està blocat quan es crea el registre. Si voleu actualitzar-lo, suprimiu el registre i torneu-lo a crear. Si heu enregistrat valors reals o si el registre del client d'oferta és un client principal, se us permetrà suprimir el registre. | Els clients d'oferta es copien com a clients de línia d'oferta quan es crea una línia d'oferta. Els clients de l'oferta també es copiaran al clients del contracte del projecte quan es guanya una oferta. |
| Percentatge dividit de facturació | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Representa el percentatge de cada transacció de vendes sense facturar que s'atribuirà a aquest client de l'oferta. | Es copia a les noves línies d'oferta i als clients del contracte del projecte. |
| Nom de contacte de facturació | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Es tracta d'un camp de text i s'ha d'utilitzar per identificar la persona de contacte de la factura d'aquest client. Es prenen per defecte del registre de compte relacionat | Es copien als clients de contracte de projecte quan es guanya una oferta i al seu torn al camp de nom de contacte de facturació a la factura que es genera per a aquest client. |
| Nom de facturació | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Aquest camp de text s'ha d'utilitzar per identificar la persona de contacte de la factura d'aquest client. | Es copia als clients de contracte de projecte quan es guanya una oferta i al seu torn al camp **Nom de contacte de facturació** a la factura que es genera per a aquest client. |
| Condicions de pagament | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Es tracta d'una conjunt d'opcions amb valors que per defecte són del registre de compte relacionat. | Es copia als clients de contracte de projecte quan es guanya una oferta i al seu torn al camp **Nom de contacte de facturació** a la factura que es genera per a aquest client. |
| És arrodoniment | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Indica si aquest client és un tipus d'arrodoniment per defecte per a aquest contracte. | Es copia als clients del contracte del projecte quan es guanya una oferta. |
| Límit que no s’ha de superar | Quadrícula editable a la pestanya **Clients de l'oferta** i als formularis **Principal** i **Creació ràpida** per a un client d'oferta. | Indica si hi ha un límit o un màxim negociat a l'import global que es facturarà a aquest client per a aquesta interacció | Es copia als clients del contracte del projecte quan es guanya una oferta. |

## <a name="editing-billing-split-percentages"></a>Edició dels percentatges de divisió de la facturació

Podeu editar els percentatges de divisió de la facturació mitjançant l'experiència d'edició de quadrícula en línia. Quan els percentatges de divisió de la facturació no sumin un total de 100%, es produirà un error. Després d'actualitzar els percentatges de divisió de la facturació, actualitzeu la pàgina per suprimir l'error.

També podeu provar de seleccionar **Distribueix de manera uniforme** a la subquadrícula de clients de l'oferta. Aquesta acció assigna les divisions de la facturació a tots els clients de l'oferta. Si hi ha cap factor d'arrodoniment, s'afegirà al client d'arrodoniment. Un dels clients de l'oferta sempre està etiquetat com a client d'arrodoniment. Això vol dir que el registre de client d'oferta té la marca **Arrodoniment** definida com a **Sí**. Normalment, aquest és el client principal de l'oferta, però es pot canviar.
