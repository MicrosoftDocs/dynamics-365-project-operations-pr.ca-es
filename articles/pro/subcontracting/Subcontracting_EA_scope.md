---
title: Versió d'accés anticipat de subcontractació a octubre de 2021
description: Aquest tema proporciona una descripció general de les capacitats de subcontractació del Project Operations que formen part de la versió d'accés anticipat d'octubre de 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383683"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Versió d'accés anticipat de subcontractació a octubre de 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest tema proporciona una descripció general de les capacitats de subcontractació del Dynamics 365 Project Operations que formen part de la versió d'accés anticipat d'octubre de 2021. Aquest conjunt de característiques no està a punt per a entorns de producció o en directe. Per tant, aquestes característiques es mantindran en la versió d'accés anticipat fins que es s'alliberi el conjunt de característiques complet. Us recomanem que no utilitzeu la característica de subcontractació establerta per a escenaris de producció en directe fins que s'elimini el bàner de la versió preliminar. 

La llista següent mostra el que està disponible actualment a la versió d'accés anticipat de l'octubre de 2021:

1. L'administrador del projecte crea un subcontracte amb un proveïdor. Per defecte, les llistes de preus adjuntes al registre del proveïdor s'utilitzen per a la subcontractació. El compte del proveïdor té un tipus de relació de **Proveïdor** o **Distribuïdor**.

2. L'administrador del projecte pot desglossar totes les compres com a elements de línia del subcontracte. Les línies del subcontracte poden ser per temps, despeses o productes. La classe de transacció de la línia del subcontracte determina per a què serveix la línia.

3. L'administrador del compte del proveïdor i l'administrador del projecte poden iterar el subcontracte. Els preus es poden ajustar a les llistes de preus de compra que hi ha adjuntes al subcontracte.

4. En aquest punt o més endavant en el procés, si la línia del subcontracte és per al temps, l'administrador del compte del proveïdor associa els contactes del proveïdor amb cada línia de subcontracte. Aquesta associació proporciona informació a l'administrador del projecte sobre qui està treballant en el subcontracte. Quan un contacte del proveïdor s'associa amb una línia del subcontracte, el sistema crea automàticament un recurs que es pot reservar a partir del contacte, si encara no existeix cap recurs que es pot reservar.

5. El mètode de facturació de cada línia del subcontracte pot ser **Preu fix** o **Temps i material**. Per a les línies del subcontracte de preu fix, es configura una planificació de la factura basada en fites.

Actualment, la resta de passos del flux del procés de negoci per a la subcontractació que es resumeix a la Informació general no estan disponibles. Quan s'afegeixin funcionalitats noves, aquest tema s'actualitzarà. 

La il·lustració següent representa la versió d'accés anticipat de subcontractació en contrast amb el procés de negoci d'extrem a extrem.

![Flux del procés de subcontractació](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Versió d'accés anticipat de les línies de subcontracte basades en quantitat i basades en treball
A la versió d'accés anticipat d'octubre de 2021, només s'admeten les línies de subcontracte basades en quantitat. Això significa que una línia subcontracte es pot utilitzar per adquirir temps, despeses o materials d'un proveïdor, però no per a tota una feina. Això també vol dir que la quantitat que s'adquireix (unitats de temps, despeses o quantitat de materials) en una línia de subcontracte es pot utilitzar en qualsevol projecte del sistema.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
