---
title: Avançament d'efectiu
description: Aquest tema proporciona informació sobre els avançaments d'efectiu.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c610fdda8f337e0c16fe5010770aca678201c328
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002134"
---
# <a name="cash-advance"></a>Avançament d'efectiu

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Un avançament d'efectiu permet als empleats demanar prestat diners de la seva empresa abans d'incórrer en les despeses. Quan s'aprova i es paga un avançament d'efectiu sol·licitat, l'empleat pot utilitzar els diners per a les despeses de l'empresa en què pot incórrer. 

## <a name="create-and-submit-a-cash-advance-request"></a>Crear i enviar una sol·licitud d'avançament d'efectiu
Per crear un nou avançament en efectiu i enviar una sol·licitud d'avançament en efectiu, feu el següent: 

1. A **Les meves despeses**, seleccioneu **Bestretes en efectiu** > **Noves**. 
2. A la pàgina **Nova sol·licitud d'avançament d'efectiu**, introduïu la finalitat de la despesa i seleccioneu la ubicació on s'incorrerà la despesa.
3. Introduïu l'import sol·licitat i la moneda i, a continuació, seleccioneu **Desa**. 
4. Quan estigueu a punt per enviar la sol·licitud d'avançament d'efectiu, a la pàgina **Sol·licitud d'avançament d'efectiu**, seleccioneu **Flux de treball** > **Envia**.

## <a name="modify-a-cash-advance-request"></a>Modificar una sol·licitud d'avançament d'efectiu

Si no s'ha enviat per a la seva aprovació, podeu modificar una sol·licitud d'avançament en efectiu.

1. A **Les meves despeses: bestretes en efectiu** localitzeu i seleccioneu la bestreta en efectiu que voleu editar.
2. Seleccioneu **Edita** i feu els canvis necessaris a la sol·licitud d'avançament d'efectiu. 
3. Seleccioneu **Desa i tanca**.


## <a name="view-cash-advance-requests"></a>Visualitzar les sol·licituds d'avançament d'efectiu
Podeu revisar la llista de tots els avançaments d'efectiu que estiguin en esborrany, enviats, en revisió o pagats a **Les meves despeses: avançaments d'efectiu**. 

## <a name="approve-cash-advance-requests"></a>Aprovar sol·licituds d'avançament d'efectiu

Els administradors o els usuaris configurats com a aprovadors al flux de treball podran aprovar els avançaments d'efectiu que se'ls presentin per revisar-los. 

1. Per aprovar un avançament d'efectiu, a **Processa els avançaments d'efectiu**, seleccioneu **Avançaments d'efectiu per a la meva revisió**.
2. Seleccioneu l'avançament d'efectiu que heu de revisar i seleccioneu **Aprova**.  

## <a name="pay-cash-advances"></a>Pagar avançaments d'efectiu 
El procediment següent el sol completar un comptable o un usuari amb permisos comptables.

1. Per comptabilitzar els avançaments d'efectiu aprovats, seleccioneu **Avançaments d'efectiu aprovats** i, a continuació, seleccioneu **Paga i transfereix**.  
2. Proporcioneu els detalls del diari per als avançaments d'efectiu i, a continuació, seleccioneu **D'acord**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Enviar un informe de despeses d'un avançament d'efectiu pagat 

Quan creeu i envieu un informe de despeses per a la bestreta en efectiu que ja heu rebut, les despeses s'ajustaran automàticament amb aquesta bestreta. Si l'avançament d'efectiu és superior a l'import gastat, heu de retornar el balanç a l'empresa mitjançant la categoria de despeses **Retorn d'efectiu**. Si la bestreta en efectiu pagada per l'empresa és inferior a l'import que heu despès, l'empresa us ha de tornar el balanç. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Selecció de bestretes en efectiu que s'apliquen a les despeses
Abans d'enviar un informe de despeses, podeu seleccionar l'avançament en efectiu que s'ajusta a les transaccions de despeses de l'informe. Per utilitzar aquesta funcionalitat, cal habilitar les dues característiques següents des de l'àrea de treball **Administració de característiques**:

  - Informes de despeses reimaginats
  - Possibilitat d'assignar bestretes d'efectiu a línies de despesa
 
 Quan aquestes característiques estan habilitades:
 
  - Podeu afegir una o més bestretes d'efectiu per cada línia de despesa.
  - El saldo disponible d'una bestreta d'efectiu és visible en temps real quan es desa un informe de despeses. Això us permet processar les transaccions de despeses i la transacció de devolució d'efectiu al mateix temps.
  - Podeu seleccionar diversos avançaments d'efectiu per a una transacció de despesa.
  - Les dades de conciliació d'avançament d'efectiu estan disponibles mitjançant una consulta. 
 
Si no utilitzeu aquestes funcions, la funcionalitat es mantindrà igual, i els avançaments d'efectiu existents es reduiran automàticament després de l'enviament d'una despesa.

### <a name="example"></a>Exemple 
Teniu previst viatjar des de Seattle a la ciutat de Nova York per a una conferència. Es crea una sol·licitud de bestreta en efectiu per a 3000.00 USD en funció del cost previst del tiquet de la conferència, els vols, l'hotel, els àpats i el taxi. No se us pagarà tret que el vostre cap aprovi aquesta sol·licitud. Quan l'administrador l'aprovi, l'avançament d'efectiu es paga com a 3000,00 USD al vostre compte bancari. A continuació, assistiu a la conferència. Després de completar el vostre viatge, esbrineu que la despesa total només era de 2790,00 USD. Seleccioneu **Efectiu** al camp **Mètode de pagament** i envieu la despesa per a 2790.00 USD. L'import de despesa enviat s'ajusta automàticament a l'avançament d'efectiu de 3000,00 USD que se us ha prestat. Ara deveu un balanç de 210.00 USD (3000.00 - 2790.00), que podeu tornar a l'empresa per mitjà de la categoria de despeses **Retorn en efectiu**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
