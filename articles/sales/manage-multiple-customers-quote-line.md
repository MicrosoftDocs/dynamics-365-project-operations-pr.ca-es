---
title: Administració de diversos clients a les línies d'ofertes basades en projectes
description: En aquest tema es proporciona informació sobre com administrar diversos clients en línies d'oferta basades en projectes.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffb89a954b8af9d726c64cceeafca638c3393130
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965730"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Administració de diversos clients a les línies d'ofertes basades en projectes

Les línies d'oferta basades en projectes admeten escenaris en què cada línia d'oferta té una llista de clients que paguen. Aquesta llista de clients de la línia d'oferta basada en projectes pot ser la mateixa que la llista de clients a l'oferta. També podeu canviar la llista de clients per tal que sigui diferent. Per crear el contracte del projecte eventual quan es guanya una oferta de projecte, la llista de clients de la línia d'oferta basada en projectes es copia a la línia de contracte corresponent basada en projectes. Els clients de l'oferta basada en projectes es copien al contracte del projecte.

Quan factureu el contracte del projecte eventual, la llista de clients de la línia de contracte basada en projectes té prioritat sobre la llista del contracte del projecte. La llista de clients del contracte de projecte només s'utilitza per als valors predeterminats de les noves línies de contracte del projecte.

Tots els clients de l'oferta de la pestanya **Clients** de l'oferta del projecte són per defecte clients de la línia d'oferta a les línies d'oferta basades en projectes noves creades per a l'oferta del projecte. Totes les línies de l'oferta basades en projectes no hereten els registres de client d'oferta nova que s'hagin creat després.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Crear, actualitzar o suprimir un registre de client d'una línia d'oferta

Podeu crear, actualitzar o suprimir un client de línia d'oferta a la pestanya **Clients de la línia d'oferta** de la pàgina **Línia d'oferta basada en projectes**. En afegir un client nou a la línia d'oferta basada en projectes, el client també s'afegeix a l'oferta global com a client de l'oferta, amb un percentatge de divisió de facturació per defecte de l'oferta global del 0%. El percentatge de divisió de facturació de l'oferta global es copia a les línies d'oferta noves i al contracte eventual del projecte. No obstant, quan factureu el contracte, s'utilitza el percentatge de divisió de la facturació al nivell de la línia d'oferta, no el percentatge de divisió de la facturació del nivell de contracte global. 

La taula següent mostra els camps del registre del client d'oferta d'una línia d'oferta basada en projectes.

| Camp | Location | Descripció i instruccions | Impacte descendent |
| --- | --- | --- | --- |
| **Compte** | Quadrícula editable a la pestanya **Clients de la línia d'oferta**, al formulari principal i al formulari de creació ràpida per a un client de línia d'oferta. | Enumera tots els comptes actius. Aquest camp està blocat quan es crea el registre. Si heu d'actualitzar el camp, suprimiu i torneu a crear el registre. Si heu enregistrat valors reals, no podeu suprimir el registre. | En triar un compte de la llista mestra de comptes per afegir, el client de la línia d'oferta també s'afegeix com a client d'oferta. En guanyar una oferta, els clients de la línia d'oferta també es copiaran al clients de la línia de contracte del projecte. |
| **Percentatge dividit de facturació** | Quadrícula editable a la pestanya **Clients de la línia d'oferta**, al formulari principal i al formulari de creació ràpida per a un client de línia d'oferta. | Representa el percentatge de cada transacció de vendes sense facturar que s'atribuirà a aquest client de la línia d'oferta. | Es copia als clients de la línia de contracte del projecte. |
| **Límit que no s’ha de superar** | Quadrícula editable a la pestanya **Clients de la línia d'oferta**, al formulari principal i al formulari de creació ràpida per a un client de línia d'oferta. | Indica si hi ha un límit o un màxim negociat a l'import global que es facturarà a aquest client per a aquesta línia d'oferta. | Es copia als clients de la línia de contracte del projecte quan es guanya una oferta. |
| **Empresa propietària** | Quadrícula editable a la pestanya **Clients de la línia d'oferta**, al formulari principal i al formulari de creació ràpida per a un client de línia d'oferta. | L'entitat jurídica en la qual està configurat aquest client dins del mòdul **Administració de projectes i comptabilitat**. Aquest camp és només de lectura i es defineix a l'empresa propietària de l'oferta. La llista de clients que s'afegeixen al camp **Compte** ja està filtrada a la llista de l'empresa propietària al mòdul **Administració de projectes i comptabilitat** del Project Operations. | L'empresa propietària és equivalent al concepte d'entitat jurídica. Totes les despeses i ingressos acumulats d'aquest projecte es comptabilitzen al registre general de l'empresa propietària. |
| **És arrodoniment** | Quadrícula editable a la pestanya **Clients de la línia d'oferta**, al formulari principal i al formulari de creació ràpida per a un client de línia d'oferta. | Indica si aquest client és un client d'arrodoniment per defecte de la línia d'oferta basada en projectes. | Es copia als clients del contracte del projecte quan es guanya una oferta. |

## <a name="edit-billing-split-percentages"></a>Edició dels percentatges de divisió de la facturació

Podeu editar els percentatges de divisió de facturació en línia. Quan els percentatges de divisió de la facturació no sumen un total de 100%, es produeix un error. Després d'editar els percentatges de divisió de la facturació, actualitzeu la pàgina de la línia d'oferta per suprimir l'error.

Utilitzeu l'acció de distribució uniforme a la subquadrícula de clients de la línia d'oferta per assignar les divisions de facturació a tots els clients de la línia d'oferta. Si hi ha un factor d'arrodoniment, s'afegirà al client d'arrodoniment. Un dels clients de la línia d'oferta sempre està etiquetat com a client d'arrodoniment, la qual cosa vol dir que el registre de client de la línia d'oferta té la marca definida com a **Sí**. 
