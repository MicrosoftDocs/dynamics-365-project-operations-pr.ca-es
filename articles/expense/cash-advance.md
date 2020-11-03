---
title: Avançament d'efectiu
description: Aquest tema proporciona informació sobre els avançaments d'efectiu.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072095"
---
# <a name="cash-advance"></a>Avançament d'efectiu

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Un avançament d'efectiu permet als empleats demanar prestat diners de la seva empresa abans d'incórrer en les despeses. Quan s'aprova i es paga un avançament d'efectiu sol·licitat, l'empleat pot utilitzar els diners per a les despeses de l'empresa en què pot incórrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear i enviar una sol·licitud d'avançament d'efectiu

1. A **Les meves despeses** , seleccioneu **Avançaments d'efectiu** > **Nou** per crear un avançament d'efectiu nou. 
2. A la pàgina **Nova sol·licitud d'avançament d'efectiu** , introduïu la finalitat de la despesa i seleccioneu la ubicació on s'incorrerà la despesa.
3. Introduïu l'import sol·licitat i la moneda i, a continuació, seleccioneu **Desa**. 
4. Quan estigueu a punt per enviar la sol·licitud d'avançament d'efectiu, a la pàgina **Sol·licitud d'avançament d'efectiu** , seleccioneu **Flux de treball** > **Envia**.

## <a name="modify-a-cash-advance-request"></a>Modificar una sol·licitud d'avançament d'efectiu

Si no s'ha enviat per a la seva aprovació, podeu modificar una sol·licitud d'avançament en efectiu.

1. A **Les meves despeses: avançaments d'efectiu** localitzeu i seleccioneu l'avançament d'efectiu que voleu editar.
2. Seleccioneu **Edita** i feu els canvis necessaris a la sol·licitud d'avançament d'efectiu. 
3. Seleccioneu **Desa i tanca**.


## <a name="view-cash-advance-requests"></a>Visualitzar les sol·licituds d'avançament d'efectiu
Podeu revisar la llista de tots els avançaments d'efectiu que estiguin en esborrany, enviats, en revisió o pagats a **Les meves despeses: avançaments d'efectiu**. 

## <a name="approve-cash-advance-requests"></a>Aprovar sol·licituds d'avançament d'efectiu

Els administradors o els usuaris configurats com a aprovadors al flux de treball podran aprovar els avançaments d'efectiu que se'ls presentin per revisar-los. 

1. Per aprovar un avançament d'efectiu, a **Processa els avançaments d'efectiu** , seleccioneu **Avançaments d'efectiu per a la meva revisió**.
2. Seleccioneu l'avançament d'efectiu que heu de revisar i seleccioneu **Aprova**.  

## <a name="pay-cash-advances"></a>Pagar avançaments d'efectiu 
El procediment següent el sol completar un comptable o un usuari amb permisos comptables.

1. Per comptabilitzar els avançaments d'efectiu aprovats, seleccioneu **Avançaments d'efectiu aprovats** i, a continuació, seleccioneu **Paga i transfereix**.  
2. Proporcioneu els detalls del diari per als avançaments d'efectiu i, a continuació, seleccioneu **D'acord**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Enviar un informe de despeses d'un avançament d'efectiu pagat 

Quan creeu i envieu un informe de despeses per a l'avançament d'efectiu que ja heu rebut, les despeses s'ajustaran automàticament a l'avançament. Si l'avançament d'efectiu és superior a l'import gastat, heu de retornar el balanç a l'empresa mitjançant la categoria de despeses **Retorn d'efectiu**. Si l'avançament d'efectiu pagat per l'empresa és inferior a la quantitat que heu gastat, l'empresa ha de reemborsar el balanç. 

### <a name="example"></a>Exemple
Teniu pensat viatjar per a una conferència de Seattle a la ciutat de Nova York. Creeu una sol licitud d'avançament d'efectiu de 3000,00 USD ja que heu calculat que el cost de l'entrada a la conferència, els vols, l'hotel, els àpats i el taxi serà aproximadament aquesta quantitat. No rebreu cap pagament excepte si el vostre administrador aprova aquesta sol·licitud. Quan l'administrador l'aprovi, l'avançament d'efectiu es paga com a 3000,00 USD al vostre compte bancari. A continuació, assistiu a la conferència. Després de completar el vostre viatge, esbrineu que la despesa total només era de 2790,00 USD. Seleccioneu **Efectiu** al camp **Mètode de pagament** i envieu la vostra despesa de 2790,00 USD. L'import de despesa enviat s'ajusta automàticament a l'avançament d'efectiu de 3000,00 USD que se us ha prestat. Ara deveu un balanç de 210,00 USD (3000,00-2790,00) a l'empresa, que podeu tornar a l'empresa mitjançant la categoria de despeses **Retorn d'efectiu**. 
