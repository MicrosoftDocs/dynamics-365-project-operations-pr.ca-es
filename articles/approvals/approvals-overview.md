---
title: Informació general de les aprovacions
description: En aquest tema es proporciona informació sobre treballar amb aprovacions al Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: d77c62455c346d6d427d71af4b01d62b5132a2377c2c1a0a64f56fb313219c46
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991699"
---
# <a name="approvals-overview"></a>Informació general de les aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les entrades de temps, despeses i ús de materials es desplacen a través d'un flux de treball d'aprovació. Un cop aprovades les entrades, les transaccions es registren en els valors reals o el temps es reserva a la planificació.

## <a name="approvals-workflow"></a>Flux de treball d'aprovacions
Quan creeu i envieu una entrada de temps, despesa o ús de materials, es crea un registre d'aprovació. L'aprovador o l'administrador del projecte revisa i aprova l'entrada. Si l'entrada està relacionada amb un projecte, els valors reals es crearan quan s'aprovi. Això permet fer un seguiment del cost i de la facturació.

## <a name="approve-an-entry"></a>Aprovar una entrada
La pàgina **Aprovacions** us permet canviar entre diferents visualitzacions per tal de visualitzar els diferents tipus d'aprovacions.
  
1. Aneu a la pàgina **Aprovacions** i seleccioneu **Despeses**, **Temps**, **Ús de materials** o **Recuperacions**.
2. Reviseu cada aprovació i seleccioneu les que voleu aprovar.
3. Seleccioneu **Aprova** per aprovar les entrades seleccionades.
El sistema processa aquestes entrades i crea valors reals.

## <a name="reject-an-entry"></a>Rebutjar una entrada
Com a aprovador de projectes, potser haureu de retornar una entrada a un usuari per corregir-la.
  
1. Aneu a la pàgina **Aprovacions** i seleccioneu l'entrada per rebutjar. 
2. Seleccioneu **Rebutja**.
3. Opcionalment, afegiu un comentari al quadre de diàleg **Comentaris de rebuig** per informar l'usuari sobre la raó per la qual es rebutja l'entrada.
4. Seleccioneu **D'acord**. L'entrada es retornarà a l'usuari.
  
## <a name="cancel-approval"></a>Cancel·la l'aprovació
En alguns casos, pot ser que hàgiu de cancel·lar una entrada prèviament aprovada. La cancel·lació d'una entrada prèviament aprovada tindrà un impacte financer. 

## <a name="approving-recall-requests"></a>Aprovació de sol·licituds de recuperació
En alguns casos, un consultor pot haver de recuperar una entrada prèviament aprovada. La cancel·lació d'una entrada prèviament aprovada tindrà un impacte financer. Cal l'aprovador del projecte per aprovar la recuperació per invertir la transacció a Valors reals.

## <a name="specify-project-approvers"></a>Especificar els aprovadors del projecte
Cada projecte té un nombre de membres de l'equip del projecte. Podeu especificar quins membres de l'equip són també aprovadors del projecte.

1. Aneu a la pàgina **Projectes** i obriu el projecte de la llista.
2. A la pestanya **Equip**, seleccioneu el membre de l'equip que serà un aprovador del projecte i, a continuació, seleccioneu **Edita**.
3. Definiu el camp **Aprovador del projecte** a **Sí**.
4. Seleccioneu **Desa**.
5. Repetiu els passos 2 i 4 per afegir aprovadors del projecte addicionals.

## <a name="configure-the-users-manager"></a>Configurar l'administrador de l'usuari

1. Aneu a **Configuració** > **Seguretat** > **Usuaris**.
2. Seleccioneu l'usuari a qui esteu assignant un administrador i a l'àrea **Informació de l'organització**, seleccioneu l'administrador de la llista. 
3. Seleccioneu **Desa**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
