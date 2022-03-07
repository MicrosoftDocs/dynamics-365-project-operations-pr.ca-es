---
title: Configuració de la creació de factures automàtica
description: Aquest tema proporciona informació sobre com configurar la creació automàtica de factures proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997504"
---
# <a name="set-up-automatic-invoice-creation"></a>Configuració de la creació de factures automàtica 
 
_**S'aplica a:** Implementació bàsica: tracte de facturació proforma, Project Operations per a escenaris basats en recursos/sense cotització_

Podeu configurar la creació de factures automàtica al Dynamics 365 Project Operations. El sistema crea un esborrany de factura proforma basada en la planificació de factures per a cada contracte de projecte i línia de contracte. Les planificacions de factures es configuren al nivell de línia de contracte. Cada línia d'un contracte pot tenir una planificació de factures diferent, o la mateixa planificació de factures es pot incloure en cada línia del contracte.

Quan es crea una factura, el sistema sempre crea com a mínim una factura per contracte de projecte. En alguns casos, es poden crear diverses factures. Per exemple, si el contracte té diversos clients, es crearà el mateix nombre de factures que nombre de clients que tenen transaccions facturables per facturar en aquest contracte de projecte.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Com s'inclouen les transaccions en una factura 

De vegades, cada línia de contracte basada en projectes especifica una planificació de factures independent. Per exemple, els serveis d'implementació del contracte d'Adatum tenen les següents línies de contracte:

- Treball prototip que és un preu fix amb dues fites creades manualment.
- Treball d'implementació que inclou temps i que es facturarà quinzenalment els dilluns.
- Despeses incorregudes que s'han de facturar mensualment el primer dilluns de cada mes.

Les planificacions de factures definides en cadascun d'aquests dos elements de línia tenen un aspecte similar a la taula següent:

| Línia de contracte | Data de creació de la factura | Data límit de la transacció | Data de la fita | Import de la fita |
| --- | --- | --- | --- | --- |
| Treball prototip | Dilluns 5 d'octubre | - | Dilluns 5 d'octubre | 5000 USD |
| - | Dimarts 3 de novembre | - | Dimarts 3 de novembre | 12,000 USD |
| Treball d'implementació | Dilluns 5 d'octubre | Diumenge 4 d'octubre | - | - |
| - | Dilluns 19 d'octubre | Diumenge 18 d'octubre | - | - |
| - | Dilluns 2 de novembre | Dilluns 1 de novembre | - | - |
| - | Dilluns 16 de novembre | Diumenge 15 de novembre | - | - |
| Despeses incorregudes | Dilluns 5 d'octubre | Diumenge 4 d'octubre | - | - |
| - | Dilluns 2 de novembre | Dilluns 1 de novembre | - | - |

En aquest exemple, quan la facturació automàtica s'executa el dia:

- **4 d'octubre o qualsevol data anterior**: no es genera cap factura per aquest contracte perquè la taula **Planificació de factures** per a cadascuna d'aquestes línies de contracte no té el diumenge 4 d'octubre com a data d'execució de la factura.
- **Dilluns 5 d'octubre**: es genera una factura per a:

    - Treball prototip que inclou la fita, si es marca com a **A punt per facturar**.
    - Treball d'implementació que inclou totes les transaccions de temps creades abans de la data límit de transaccions del diumenge 4 d'octubre, que estigui marcat com a **A punt per facturar**.
    - Despeses incorregudes que inclouen totes les transaccions de despeses creades abans de la data límit de transaccions del diumenge 4 d'octubre, que estiguin marcades com a **A punt per facturar**.
  
- **6 d'octubre o qualsevol data abans del 19 d'octubre**: no es genera cap factura per a aquest contracte ja que la taula **Planificació de factures** per a cadascuna d'aquestes línies de contracte no té el 6 d'octubre ni cap data abans del 19 d'octubre com a data d'execució de la factura.
- **Dilluns 19 d'octubre**: es genera una factura per al treball d'implementació que inclou totes les transaccions de temps creades abans de la data límit de transaccions del diumenge 18 d'octubre, que estigui marcat com a **A punt per facturar**.
- **Dilluns 2 de novembre**: es genera una factura per a:

    - Treball d'implementació que inclou totes les transaccions de temps creades abans de la data límit de transaccions del diumenge 1 de novembre, que estigui marcat com a **A punt per facturar**.
    - Despeses incorregudes que inclouen totes les transaccions de despeses creades abans de la data límit de transaccions del diumenge 1 de novembre, que estiguin marcades com a **A punt per facturar**.

- **Dimarts 3 de novembre**: es genera una factura per al treball prototip que inclou la fita per 12.000 USD, si es marca com a **A punt per facturar**.

## <a name="configure-automatic-invoicing"></a>Configurar la facturació automàtica

Completeu els passos següents per configurar una execució de factura automàtica.

1. Al **Projecte Operacions**, aneu a **Configuració** > **Configuració de la facturació recurrent**.
2. Creeu un treball per lots i anomeneu-lo **Creació de factures del Project Operations**. El nom del treball per lots ha d'incloure les paraules "Creació de factures".
3. Al camp **Tipus de treball**, seleccioneu **Cap**. Per defecte, els camps **Freqüència diària** i **Actiu** estan definides com a **Sí**.
4. Seleccioneu **Executa el flux de treball**. Al quadre de diàleg **Registre de cerca**, veureu tres fluxos de treball:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Seleccioneu **ProcessRunCaller** i després trieu **Afegeix**.
6. Al quadre de diàleg següent, seleccioneu **D'acord**. Un flux de treball **Repòs** va seguit d'un flux de treball **Procés**. 

> [!NOTE]
> També podeu seleccionar **ProcessRunner** al pas 5. Després, quan seleccioneu **D'acord**, un flux de treball **Procés** va seguit d'un flux de treball **Repòs**.

Els fluxos de treball **ProcessRunCaller** i **ProcessRunner** creen factures. **ProcessRunCaller** crida a **ProcessRunner**. **ProcessRunner** és el flux de treball que en realitat crea les factures. El flux de treball passa per totes les línies de contracte per a les quals s'han de crear factures i crea factures d'aquestes línies. Per determinar les línies de contracte per a les quals s'han de crear factures, el treball consulta les dates d'execució de la factura per a les línies de contracte. Si les línies de contracte que pertanyen a un contracte tenen la mateixa data d'execució de la factura, les transaccions es combinen en una factura que té dues línies de factura. Si no hi ha cap transacció per a la qual crear factures, el treball omet la creació de la factura.

Després d'haver acabat d'executar-se **ProcessRunner**, crida a **ProcessRunCaller**, proporciona l'hora d'acabament i es tanca. **ProcessRunCaller** llavors inicia un temporitzador que s'executa durant 24 hores a partir de l'hora d'acabament especificada. Al final del temporitzador, **ProcessRunCaller** es tanca.

El treball de processament per lots per crear factures és una feina recurrent. Si aquest procés per lots s'executa moltes vegades, es creen diverses instàncies del treball que causen errors. Per tant, hauríeu d'iniciar el procés de processament per lots només una vegada i reiniciar-lo només si s'atura l'execució.

> [!NOTE]
> La facturació per lots al Project Operations només s'executa per a les línies de contracte del projecte que es configuren mitjançant planificacions de factura. Una línia de contracte amb un mètode de facturació de preu fix ha de tenir les fites configurades. Una línia de contracte de projecte amb un mètode de facturació de temps i material necessitarà una configuració de planificació de facturació basada en la data.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
