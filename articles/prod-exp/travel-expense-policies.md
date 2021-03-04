---
title: Configuració de les normes de despesa
description: Podeu configurar les normes de despeses que els vostres treballadors han de seguir en introduir i enviar informes de despeses i peticions de viatge al Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960685"
---
# <a name="set-up-expense-policies"></a>Configuració de les normes de despesa

Podeu definir normes que els treballadors han de seguir en introduir i enviar informes de despeses i requisicions de viatge.         
Implementar normes de despesa us pot ajudar a administrar les despeses de manera eficaç.         

Per exemple, podeu definir una norma per a les despeses d'hotels a Nova York que indiqui que la despesa per nit no pot superar els 250 USD.       
Si un treballador envia un informe de despeses o una petició de viatge en què el preu de l'habitació excedeixi aquesta quantitat, el sistema notificarà al        
treballador que l'import de la norma per a la despesa s'ha excedit. Podeu configurar el missatge que rebrà el treballador en el moment de        
definir la norma.      
        
Podeu definir tres tipus de normes:         
        
- Advertiment: permet al treballador presentar un informe de despeses o una requisició de viatge però la despesa es marcarà per a tots els aprovadors i        
  per a informes posteriors.        

- Error: requereix que el treballador revisi la despesa per tal de complir la norma abans d'enviar l'informe de despeses o la requisició de viatges.       
 
 - Justificació: requereix que el treballador o un cap introdueixin una justificació per superar la quantitat de la norma abans d'enviar l'informe de despeses o la requisició de viatges.        

## <a name="policy-tips"></a>Consells per a les normes
A continuació, trobareu alguns suggeriments que us poden ajudar a crear normes noves per a l'administració de despeses. 
* Les normes tenen una data efectiva i no tenen efecte si es crea la norma amb una data després de la data en què s'ha produït la despesa. Per exemple, si avui creeu una nova norma per aplicar una despesa màxima per àpat de 50 USD, qualsevol despesa existent introduïda fins ahir no es comprovarà amb aquesta norma.
* Quan es crea una norma per a una categoria de despesa que es pot desglossar, cal afegir una condició per al tipus de línia de despeses. Algunes normes, com ara exigir un rebut, poden no tenir sentit per a les línies i només s'han d'aplicar a la línia de capçalera o a una línia no desglossada. 
* Les normes d'administració de despeses s'avaluen amb l'entitat d'origen per defecte. Per als escenaris entre empreses, podeu definir la norma que s'avalua a l'entitat de destinació (entitat prestatària) en el seu lloc. Per executar les normes a l'entitat de destinació, activeu la funció "Avalua la norma de despesa a l'entitat jurídica prestatària" a l'àrea de treball **Administració de característiques**.

## <a name="when-to-evaluate-policies"></a>Quan avaluar les normes

Als paràmetres d'administració de despeses, hi ha una opció per avaluar les normes d'avaluació de despeses quan es desa una línia o quan s'envia un informe de despeses. Si trieu avaluar-les quan es desa una línia, això assegura que els usuaris tindran una visibilitat prèvia del que han de fer per completar el seu informe de despeses d'una vegada. Si no és així, podeu endarrerir l'avaluació de la norma i estalviar temps si feu que l'avaluació sigui al final, durant l'enviament al flux de treball.


[!INCLUDE[footer-include](../includes/footer-banner.md)]