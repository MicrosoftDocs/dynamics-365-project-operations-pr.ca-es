---
title: Informació general de les aprovacions
description: En aquest tema es proporciona informació sobre treballar amb aprovacions al Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961154"
---
# <a name="approvals-overview"></a>Informació general de les aprovacions

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els enviaments de temps i de despeses passen per un flux de treball d'aprovació. Un cop aprovades les entrades, les transaccions es registren en els valors reals o el temps es reserva a la planificació.

## <a name="approvals-workflow"></a>Flux de treball d'aprovacions
Quan creeu i envieu una entrada de temps o de despesa, es crea una entrada d'aprovació. L'aprovador de projectes o l'administrador revisa i aprova l'entrada. Si l'entrada està relacionada amb un projecte, quan s'hagi aprovat, es crearan els valors reals. Això permet fer un seguiment del cost i de la facturació. 

## <a name="approve-an-entry"></a>Aprovar una entrada
El formulari **Aprovacions** us permet canviar entre diferents visualitzacions per tal que pugueu visualitzar els diferents tipus d'aprovacions.
  
1. Aneu al formulari **Aprovacions** i seleccioneu **Despeses**, **Temps** o **Recuperacions**.
2. Reviseu cada aprovació i seleccioneu les que voleu aprovar.
3. Seleccioneu **Aprova** per aprovar les entrades seleccionades.
El sistema processarà aquestes entrades i crearà valors reals o una reserva.

## <a name="reject-an-entry"></a>Rebutjar una entrada
Com a aprovador de projectes, potser haureu de retornar una entrada a un usuari per corregir-la.
  
1. Aneu al formulari **Aprovacions** i seleccioneu l'entrada per rebutjar. 
2. Seleccioneu **Rebutja**.
3. Opcional: afegiu un comentari al diàleg **Comentaris de rebuig** per informar l'usuari per què es rebutja l'entrada.
4. Seleccioneu **D'acord**. L'entrada es retornarà a l'usuari.
  
## <a name="recall-entries"></a>Recuperar entrades
En algun moment, pot ser que hàgiu de recuperar una entrada enviada. Si l'entrada no ha estat aprovada, es retornarà immediatament. Això no obstant, una entrada aprovada pot tenir un impacte material. L'aprovador de projectes es necessita per aprovar la recuperar per tal de revertir la transacció en valors reals.

## <a name="specify-project-approvers"></a>Especificar els aprovadors del projecte
Cada projecte té un nombre de membres de l'equip del projecte. Podeu especificar quins membres de l'equip són també aprovadors del projecte.

1. Aneu al formulari **Projectes** i obriu el projecte des de la llista.
2. A la pestanya **Equip**, seleccioneu el membre de l'equip que serà un aprovador del projecte i, a continuació, seleccioneu **Edita**.
3. Definiu el camp **Aprovador del projecte** a **Sí**.
4. Seleccioneu **Desa**.
5. Repetiu els passos 2 i 4 per afegir aprovadors del projecte addicionals.

## <a name="configure-the-users-manager"></a>Configurar l'administrador de l'usuari

1. Aneu a **Configuració** > **Seguretat** > **Usuaris**.
2. Seleccioneu l'usuari a qui esteu assignant un administrador i a l'àrea **Informació de l'organització**, seleccioneu l'administrador de la llista. 
3. Seleccioneu **Desa**.


