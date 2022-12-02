---
title: Transicions d'estat en un subcontracte
description: En aquest article s'expliquen les transicions d'estat d'un subcontracte al Microsoft Dynamics 365 Project Operations quan es crea, s'executa i es tanca el subcontracte.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522928"
---
# <a name="state-transitions-on-a-subcontract"></a>Transicions d'estat en un subcontracte 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest article s'expliquen les transicions d'estat en un subcontracte del Microsoft Dynamics 365 Project Operations. Cada estat es representa com a esborrany, confirmat, tancat o cancel·lat. La imatge següent representa les transicions d'estat.

![Model d'estat del subcontracte](../media/SubconStates.png)  

La taula següent proporciona una descripció del que representa cada estat al cicle de vida d'un subcontracte al Project Operations.

| Estat o província | Descripció | Transicions permeses |
| --- | --- | --- |
| Esborrany | Això representa l'estat inicial d'un subcontracte. Hi ha negociacions amb el proveïdor en curs. Les línies i els preus estan subjectes a modificacions. Un subcontracte en aquest estat es pot utilitzar per calcular i seleccionar els requisits del projecte per als recursos i els materials. També s'hi pot fer referència en el temps, les despeses i l'ús de materials d'un projecte. Un subcontracte en aquest estat es pot editar i suprimir. | Confirmat |
| Confirmat | Això representa la fase d'un subcontracte quan finalitzen les negociacions amb el proveïdor sobre els preus i els elements de la línia que s'adquireixen. Tanmateix, la prestació real de materials i/o treball per recursos subcontractats continua en curs. Un subcontracte en aquest estat es pot utilitzar per calcular i seleccionar els requisits del projecte per als recursos i els materials. També s'hi pot fer referència en el temps, les despeses i l'ús de materials d'un projecte. Un subcontracte en aquest estat no es pot editar ni suprimir. El botó **Cancel·la** us permet cancel·lar un subcontracte confirmat. El botó **Torna a obrir** us permet tornar a obrir el subcontracte per tornar-lo a posar en estat d'**Esborrany**. Utilitzeu el botó **Tanca** per tancar un subcontracte confirmat. | Tancada <br> Cancel·lada <br> Esborrany |
| Tancada | Això representa la fase d'un subcontracte quan s'acaba el lliurament real de materials i/o treball per part de recursos subcontractats. Un subcontracte en aquest estat ja no es pot utilitzar per calcular i seleccionar els requisits del projecte per als recursos i els materials. Tampoc s'hi pot fer referència en el temps, les despeses i l'ús de materials d'un projecte. Un subcontracte en aquest estat no es pot editar ni suprimir. | cap |
| Cancel·lada | Això representa la fase d'un subcontracte quan ja no es necessita el lliurament real de materials i/o treball per part de recursos subcontractats. Un subcontracte en aquest estat no es pot utilitzar per calcular i dotar els requisits del projecte amb recursos i materials ni s'hi pot fer referència en el temps, la despesa i l'ús de materials d'un projecte. Un subcontracte en aquest estat no es pot editar ni suprimir. | cap |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
