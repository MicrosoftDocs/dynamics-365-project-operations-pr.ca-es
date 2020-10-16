---
title: Línies d'oportunitat basades en productes
description: Aquest tema proporciona informació sobre els elements de línia d'oportunitat basats en productes al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896224"
---
# <a name="product-based-opportunity-lines"></a>Línies d'oportunitat basades en productes

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les línies d'oportunitat basades en productes són elements de línia de l'oportunitat. Aquestes línies es lliuren al client com a elements de línia diferents de la factura eventual sense cap altre servei de valor afegit. No es fa el seguiment de la despesa i el consum associats a les tasques de cap projecte relacionat.

Les línies basades en productes poden ser elements del catàleg o productes fora del catàleg. La major part de la funcionalitat de les línies basades en productes d'una oportunitat segueix la funcionalitat proporcionada per l'aplicació Dynamics 365 Sales. Per obtenir més informació sobre les línies d'oportunitat basades en productes, vegeu [Afegir productes a una oportunitat](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).

Un concepte de línies d'oportunitat basades en productes que és específic per a les oportunitats basades en projectes és el **Pressupost del client**. Utilitzeu aquest camp per fer el seguiment de l'import que el client està disposat a pagar per l'element de línia.

Si el mètode d'ingrés del resum de l'oportunitat està definit com a **Calculat pel sistema**, els valors del pressupost del client a les línies de producte i de projecte es resumiran per calcular els ingressos previstos.
