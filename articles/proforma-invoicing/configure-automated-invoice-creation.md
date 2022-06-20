---
title: Configurar la creació automàtica de factures
description: En aquest article s'ofereix informació sobre com configurar el sistema per generar factures automàticament.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 273e00e7841c8a34e249e54a7d868034bc34a1f7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920600"
---
# <a name="configure-automatic-invoice-creation"></a>Configurar la creació automàtica de factures

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Seguiu aquests passos per configurar una execució de factura automàtica al Dynamics 365 Project Operations.

1. Aneu a **Configuració** > **Treballs per lots**.
2. Creeu un treball per lots i anomeneu-lo **Creació de factures del Project Operations**. El nom del treball per lots ha d'incloure les paraules "Creació de factures".
3. Al camp **Tipus de treball**, seleccioneu **Cap**. Per defecte, les opcions **Freqüència diària** i **Actiu** estan definides com a **Sí**.
4. Seleccioneu **Executa el flux de treball**. Al quadre de diàleg **Registre de cerca**, veureu tres fluxos de treball:

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Seleccioneu **ProcessRunCaller** i després trieu **Afegeix**.
6. Al quadre de diàleg següent, seleccioneu **D'acord**. Un flux de treball **Repòs** va seguit d'un flux de treball **Procés**.

  > [!NOTE]
  > També podeu seleccionar **ProcessRunner** al pas 5. Després, quan seleccioneu **D'acord**, un flux de treball **Procés** va seguit d'un flux de treball **Repòs**.

Els fluxos de treball **ProcessRunCaller** i **ProcessRunner** creen factures. **ProcessRunCaller** crida a **ProcessRunner**. **ProcessRunner** és el flux de treball que en realitat crea les factures. Passa per totes les línies de contracte per a les quals s'han de crear factures i crea factures d'aquestes línies. Per determinar les línies de contracte per a les quals s'han de crear factures, el treball consulta les dates d'execució de la factura per a les línies de contracte. Si les línies de contracte que pertanyen a un contracte tenen la mateixa data d'execució de la factura, les transaccions es combinen en una factura que té dues línies de factura. Si no hi ha cap transacció per a la qual crear factures, el treball omet la creació de la factura.

Després d'haver acabat d'executar-se **ProcessRunner**, crida a **ProcessRunCaller**, proporciona l'hora d'acabament i es tanca. **ProcessRunCaller** llavors inicia un temporitzador que s'executa durant 24 hores a partir de l'hora d'acabament especificada. Al final del temporitzador, **ProcessRunCaller** es tanca.

El treball de processament per lots per crear factures és una feina recurrent. Si aquest procés per lots s'executa moltes vegades, es creen diverses instàncies del treball que causen errors. Per tant, hauríeu d'iniciar el procés de processament per lots només una vegada i reiniciar-lo només si s'atura l'execució.

> [!NOTE]
> La facturació per lots només s'executa per a les línies de contracte del projecte que es configuren mitjançant planificacions de factura. Una línia de contracte amb un mètode de facturació de preu fix ha de tenir les fites configurades. Una línia de contracte de projecte amb un mètode de facturació de temps i material necessitarà una configuració de planificació de facturació basada en la data. El mateix s'aplica a una línia de contracte basada en projectes.     


[!INCLUDE[footer-include](../includes/footer-banner.md)]