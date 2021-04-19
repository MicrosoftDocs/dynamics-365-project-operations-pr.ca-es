---
title: Administració de les llistes de preus de projectes als contractes de projectes
description: Aquest tema proporciona informació sobre l'administració de llistes de preus de projecte en contractes de projecte.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ffc48782394995781535ae56142dc76afeb9a040
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858551"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Administració de les llistes de preus de projectes als contractes de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els contractes de projecte al Dynamics 365 Project Operations estan dissenyats per admetre llistes de preus de vendes amb diverses dates d'efectivitat en un contracte. Al Project Operations, hi ha una entitat associada nova anomenada **Llistes de preus del projecte**. Aquesta entitat té una relació d'un a diversos amb un contracte de projecte.

Les llistes de preus del projecte s'utilitzen per calcular el preu de les transaccions de temps, materials i despeses en un projecte. Quan un contracte té una o més llistes de preus del projecte, aquestes llistes de preus s'utilitzen per al preu per a les estimacions de temps, materials i despesa i els valors reals en projectes associats al contracte a través de la línia de contracte.

Quan no hi ha cap llista de preus de projecte en un contracte del projecte, veureu un missatge d'advertiment que indica que no hi ha cap llista de preus del projecte i no es calcularà el preu de les vostres estimacions, la feina real del projecte, el material i les despeses registrades. No hi haurà preu per als valors de vendes.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associar o dessociar una llista de preus del projecte en un contracte de projecte

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-material-and-expenses"></a>Crear o associar una llista de preus específica per estimar el treball, el material i les despeses basats en projectes

1. Al contracte del projecte, seleccioneu la pestanya **Llistes de preus del projecte**.
2. A la subquadrícula, seleccioneu **+ Afegeix una llista de preus de projecte nova**.
3. Al control lliscant **Creació ràpida**, seleccioneu una llista de preus. 

  A la llista desplegable es mostren totes les llistes de preus que tenen el context definit com a **Vendes**, en què la moneda de la llista de preus coincideix amb la moneda del contracte.
  
4. Introduïu una descripció per a l'associació de la llista de preus del projecte, seleccioneu **Desa** i, a continuació, tanqueu el control lliscant **Creació ràpida**.

   Es crea una associació de llista de preus del projecte.
   
5. Repetiu els passos 1-4 per associar més d'una llista de preus del projecte al contracte del projecte. Només creeu diverses llistes de preus del projecte si teniu una data d'efectivitat diferent en cadascuna de les llistes de preus del projecte associat.

> [!NOTE]
> El Project Operations no admet la superposició de la data d'efectivitat de les llistes de preus del projecte. Si hi ha diverses llistes de preus del projecte per a una transacció amb una data determinada, el preu d'aquesta transacció per defecte serà zero.

### <a name="remove-a-project-price-list-association"></a>Suprimir una associació de llista de preus del projecte

- Seleccioneu la llista de preus del projecte i, a continuació, seleccioneu **Suprimeix la llista de preus del projecte de contracte** a la subquadrícula. 

  La llista de preus se suprimeix de les llistes de preus del projecte del contracte. La llista de preus en si no se suprimirà. Només se suprimirà l'associació del contracte.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurar el valor per defecte automàtic de les llistes de preus del projecte en un contracte

Una llista de preus del projecte es pot configurar com la llista de preus del projecte per defecte. Aquesta configuració garanteix que tots els contractes de l'organització sempre comencin amb una llista de preus de projecte estàndard per a aquest període de preus.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurar el valor per defecte de l'organització per a les llistes de preus del projecte

1. Aneu a **Configuració** > **General** i, a continuació, seleccioneu **Paràmetres**.
2. A la pàgina de llista **Paràmetres actius**, seleccioneu i feu doble clic al registre per obrir-lo. Mentre feu doble clic, assegureu-vos que no feu clic en cap valor de camp que sigui un enllaç. 
3. A la pàgina **Paràmetres actius**, seleccioneu la pestanya **Llista de preus**. Una subquadrícula mostra una llista de llistes de preus per defecte. Aquesta és una llista de les llistes de preus de cost i vendes estàndard. Tenir una llista de preus de **vendes** associada aquí per a cada moneda que veneu assegura que la llista de preus de venda sigui la llista per defecte de qualsevol contracte que creeu per als clients que treballin en aquesta moneda.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurar una llista de preus de projecte específica del client

També podeu configurar llistes de preus de projecte específiques del client quan heu negociat un acord de preus mestre amb els vostres clients.

1. Aneu a **Vendes** > **Clients**.
2. A la llista de comptes actius, seleccioneu el client per al qual teniu una llista de preus especial.
3. Seleccioneu el registre de client per obrir-lo i, a continuació, seleccioneu la pestanya **Llistes de preus del projecte**. Una subquadrícula mostra una llista de llistes de preus del projecte específiques d'aquest client. 
4. Creeu aquí una nova associació de llistes de preus per tenir una llista de preus de projecte específica per a aquest client.

## <a name="custom-pricing-on-a-project-contract"></a>Preus personalitzats en un contracte de projecte

Després de tenir llistes de preus de projecte per defecte de l'organització i específiques de clients, els contractes del projecte es crearan automàticament amb aquestes associacions de llistes de preus del projecte. No obstant això, les llistes de preus del projecte d'un contracte de projecte sempre es copien amb la data i el nom del contracte afegits. Els administradors de comptes i projectes poden començar a fer modificacions als preus d'aquestes còpies. Aquests preus canviats només seran aplicables a aquest contracte de projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
