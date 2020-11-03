---
title: Definir normes de despesa
description: Podeu definir normes de despesa que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072282"
---
# <a name="define-expense-policies"></a>Definir normes de despesa

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Podeu definir normes que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.         
Implementar normes de despesa us pot ajudar a administrar les despeses de manera eficaç.         

Per exemple, podeu definir una norma per a les despeses d'hotels a Nova York que indiqui que la despesa per nit no pot superar els 250 USD.       
Si un treballador envia un informe de despeses o una requisició de viatges en què el preu de l'habitació excedeixi aquesta quantitat, el sistema notificarà al         
treballador que l'import de la norma per a la despesa s'ha excedit. Podeu configurar el missatge que rebrà el treballador en el moment de        
definir la norma.      
        
Podeu definir tres tipus de normes:         
        
- **Advertiment** : permet al treballador presentar un informe de despeses o una requisició de viatge però la despesa es marcarà per a tots els aprovadors i         
  per a informes posteriors.        

- **Error** : requereix que el treballador revisi la despesa per tal de complir la norma abans d'enviar l'informe de despeses o la requisició de viatges.        
 
 - **Justificació** : requereix que el treballador o un cap introdueixin una justificació per superar la quantitat de la norma abans d'enviar l'informe de despeses o la requisició de viatges.        

## <a name="policy-tips"></a>Consells per a les normes
A continuació, trobareu alguns suggeriments que us poden ajudar a crear normes noves per a l'administració de despeses: 

- Les normes tenen una data efectiva, la qual cosa significa que una norma no té efecte si es crea amb una data després de la data en què s'ha produït la despesa. Per exemple, es crea avui una norma nova per fer complir una despesa màxima d'àpats de 50 USD. Les despeses existents que no s'hagin introduït des d'ahir no es comprovaran amb aquesta norma.
- Quan es crea una norma per a una categoria de despesa que es pot desglossar, cal afegir una condició per al tipus de línia de despeses. Algunes de les normes, com ara requerir un rebut, pot ser que no tinguin sentit per a les línies desglossades. En aquesta situació, la norma només s'aplica a la línia de capçalera o en una línia no desglossada. 
- Les normes d'administració de despeses s'avaluen amb l'entitat d'origen per defecte. Per als escenaris entre empreses, podeu definir la norma que s'avalua a l'entitat de destinació (entitat prestatària) en el seu lloc. Per executar les normes a l'entitat de destinació, activeu la funció **Avalua la norma de despesa a l'entitat jurídica prestatària** a l'àrea de treball **Administració de característiques**.

## <a name="when-to-evaluate-policies"></a>Quan avaluar les normes

A paràmetres d'administració de despeses, podeu seleccionar avaluar les normes d'avaluació de despeses quan es desa una línia o quan s'envia un informe de despeses. Si trieu avaluar-les quan es desa una línia, els usuaris tindran una visibilitat prèvia del que han de fer per completar el seu informe de despeses d'una vegada. Si no és així, podeu endarrerir l'avaluació de la norma i estalviar temps validant-la al final durant l'enviament al flux de treball.
