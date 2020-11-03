---
title: Creació d'ofertes de projectes a partir d'oportunitats
description: Aquest tema proporciona informació sobre la creació d'una oferta de projecte des d'una oportunitat.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072124"
---
# <a name="create-project-quotes-from-opportunities"></a>Creació d'ofertes de projectes a partir d'oportunitats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Es poden crear ofertes a partir d'oportunitats de projecte de les maneres següents:

- Des de la pestanya **Ofertes** a la pàgina **Oportunitat del projecte**
- Des del flux del procés de vendes d'oportunitat
- Actualitzant la referència d'oportunitat d'una oferta existent

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Des de la pestanya Ofertes de la pàgina Oportunitat del projecte

Per crear una oferta de projecte a partir d'una oportunitat, completeu els passos següents.

1. Obriu la pàgina **Oportunitat del projecte** i seleccioneu la pestanya **Ofertes**. 
2. A la subquadrícula **Ofertes** , seleccioneu **+** per crear una oferta de projecte nova basada en l'oportunitat. Totes les línies d'oportunitat i les llistes de preus de projecte relacionades es copien a la nova oferta de l'oportunitat.

## <a name="from-the-opportunity-sales-process-flow"></a>Des del flux del procés de vendes d'oportunitat

Per crear una oferta des del flux de procés de vendes d'oportunitat, completeu els passos següents.

1. Des del flux del procés de vendes d'oportunitats, obriu l'oportunitat.
2. Seleccioneu la fase **Qualificació**. 
3. Seleccioneu **Següent** i, a continuació, seleccioneu **+ Crea** per crear una oferta nova. La major part de la informació de la pestanya **Resum** d'aquesta oferta nova tindrà els valors per defecte de l'oportunitat. 
4. Introduïu qualsevol informació necessària que falti o actualitzeu els valors per defecte segons calgui a la pestanya **Resum**.
5. Seleccioneu **Desa**. L'oferta nova es crea i s'associa a l'oportunitat. Ara podeu visualitzar la informació de l'oferta a la pestanya **Ofertes** de la pàgina **Oportunitat**. 

   El procés de vendes d'oportunitat passa a la següent fase, **Proposta**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Actualitzant la referència d'oportunitat d'una oferta existent

Una oferta existent es pot enllaçar a una oportunitat. Seguiu aquests passos per actualitzar la informació d'oportunitat d'una oferta existent.

1. Obriu la pàgina **Oportunitat** i seleccioneu la pestanya **Resum**.
2. Al camp **Oportunitat** , seleccioneu l'oportunitat que voleu enllaçar amb l'oferta. Podeu veure l'oferta a la quadrícula **Ofertes** de l'oportunitat. 
3. Mitjançant el procés de venda d'oportunitats, l'oportunitat pot passar a la següent fase, **Proposta**. 

   Quan passeu una oportunitat a aquesta fase, podeu seleccionar aquesta oferta d'una llista d'ofertes associades a aquesta oportunitat. Si seleccioneu aquesta oferta, indiqueu que avanceu.

   Totes les altres ofertes associades a l'oportunitat continuaran estant disponibles i actives fins que se'n guanyi una. Podeu fer retrocedir el procés de vendes a la fase anterior de **Qualificació** i seleccionar una altra oferta amb la qual avançar.
