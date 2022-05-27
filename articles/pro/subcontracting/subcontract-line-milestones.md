---
title: Fites de línia de subcontracte
description: En aquest tema s'explica com crear i mantenir una planificació de facturació basada en fites per a un subcontracte amb un proveïdor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d1c30f48e0d43aa55e2c1650637f7f102fb200de
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579110"
---
# <a name="subcontract-line-milestones"></a>Fites de línia de subcontracte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Al Dynamics 365 Project Operations, una línia de subcontracte amb un mètode de facturació de preu fix pot especificar una planificació de facturació basada en fites amb el proveïdor.

Les fites de la facturació del proveïdor es poden generar automàticament mitjançant una freqüència establerta o podeu crear-les manualment.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Crear automàticament una planificació de facturació basada en fites per a una línia de subcontracte

Completeu els passos següents per generar automàticament una planificació de facturació basada en fites per a un conjunt fix de fites distribuïdes de manera uniforme.

1. Aneu a **Configuració** > **Freqüències de facturació** i configureu la freqüència de facturació per a les línies de subcontracte.
2. Obriu la pàgina **Subcontractes**, obriu el subcontracte amb el qual voleu treballar i, a continuació, obriu la línia de subcontracte de preu fix per a la qual creareu una planificació per fites.
3. A la pestanya **Fites de línia de subcontracte**, seleccioneu **Genera fites periòdiques**.
4. Al quadre de diàleg, introduïu o seleccioneu un interval de dates, el nombre de fites i la freqüència de facturació. Podeu seleccionar una data d'inici o seleccionar el nombre de fites i la freqüència de facturació o la data d'inici, o bé podeu seleccionar la data final i la freqüència de facturació. No podeu seleccionar la data final i el nombre de fites.
Mitjançant aquesta informació, el sistema genera fites i registres que es mostren a la quadrícula **Fites**.

   - **Nom de la fita**: el nom de la fita s'estableix en la data de fita basant-se en la freqüència de facturació.
   - **Data de la fita**: data basada en la freqüència de facturació.
   - **Import de la fita**: es calcula dividint l'import del subtotal de la línia de subcontracte pel nombre de fites.

Si la línia de subcontracte té un valor en el camp **Import d'impostos estimat**, aquest valor s'afegeix a cada fita de manera uniforme quan es generen fites periòdiques.

La suma dels imports de les fites de la línia de subcontracte ha de ser igual al valor de la línia de subcontracte. Si no són iguals, es produeix un error. Podeu corregir l'error i comprovar que el total de la fita sigui igual al valor de la línia de subcontracte creant, editant o suprimint imports de fita i d'impostos. Quan s'hagin fet els canvis, deseu i actualitzeu la pàgina per assegurar-vos que no hi hagi més errors.

## <a name="manually-create-subcontract-line-milestones"></a>Crear manualment fites de línia de subcontracte

Les fites de preu fix d'una línia de subcontracte es poden generar manualment quan no estan dividides periòdicament. Per crear manualment una línia de subcontracte, seguiu els passos següents:

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu el subcontracte amb el qual voleu treballar.
2. Obriu la línia de subcontracte de preu fix per a la qual voleu crear una fita.
3. A la pestanya **Fites de la línia de subcontracte**, a la subquadrícula, seleccioneu **+ Nova fita de línia de subcontracte**.
4. A la pàgina **Nova fita de línia de subcontracte**, introduïu la informació necessària a partir de la taula següent.

    | Camp | Descripció |Impacte funcional|
    | --- | --- |----------------------|
    | Nom de la fita | Nom de la fita. |Es mostrarà com la primera columna de totes les consultes basada en les fites de línia de subcontracte. La línia de factura del proveïdor creada a partir d'aquesta fita també utilitzarà el nom de la fita de la línia de subcontracte com a nom per defecte de la línia de factura del proveïdor.|
    | Descripció | Descripció de la fita. |La línia de factura del proveïdor creada a partir d'aquesta fita també utilitzarà la descripció de la fita de la línia de subcontracte com a descripció per defecte de la línia de factura del proveïdor.|
    | Data de la fita | Data en què el procés de creació automàtica de factures hauria de consultar l'estat d'aquesta fita per tenir-lo en compte per a la facturació.| Aquest valor s'utilitzarà com a data per defecte de la línia de factura del proveïdor en facturar aquesta línia de subcontracte. |
    | Import | Import o valor de la fita que es facturarà al client. |Aquest valor s'utilitza com a import per defecte a la línia de factura del proveïdor en facturar aquesta línia de subcontracte. |
    | Impostos | Import d'impostos aplicat a la fita.| Aquest valor s'utilitza com a import d'impostos per defecte a la línia de factura del proveïdor en facturar aquesta línia de subcontracte. |
    | Import després d'impostos | Aquest camp només de lectura es calcula com Quantitat + Impost.|Aquest valor s'utilitza per defecte a la línia de factura del proveïdor en facturar aquesta línia de subcontracte. |
    | Estat de la factura | Quan es crea la fita, aquest estat sempre es defineix com a **No preparat per a la facturació**.|  Quan l'estat és **Preparat per a la facturació**, la creació de la factura del proveïdor inclou aquesta fita a la factura del proveïdor. |

5. Seleccioneu **Desa i tanca**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
