---
title: Administració de l'estat que no s'ha de superar i les validacions
description: En aquest article s'ofereix informació sobre les comprovacions de límits que no excedeixen realitzades a les operacions del projecte.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d10a88305339a84b36d8606631ea9761806098a1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932744"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Administració de l'estat que no s'ha de superar i les validacions 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

## <a name="not-to-exceed-on-approvals"></a>Límits que no s'han de superar a les aprovacions

Quan s'envia una entrada de temps, despesa o ús de materials, es crea un registre d'aprovació. Si l'aprovació és imputable i s'assigna a una línia de contracte de temps i material, el sistema completa una comprovació de validació de límit que no s'ha de superar als nivells següents:

  - Comprovació amb el límit configurat per al client a la línia de contracte del projecte
  - Comprovació amb el límit configurat a la línia de contracte
  - Comprovació amb el límit configurat per al client
  - Comprovació amb el límit configurat al contracte

Les comprovacions de cada nivell impliquen assegurar-se que l'import del valor de venda en aquesta aprovació no infringirà el límit que no s'ha de superar en aquest nivell després de comptabilitzar l'import del registre de facturació ja registrat i l'import facturat fins a la data en aquest nivell.

Si la comprovació és correcta, l'aprovació rep un estat de validació **Correcta**.

Si la comprovació és incorrecta, l'aprovació rep un estat de validació **Error**. El detall de validació de límit que no s'ha de superar informarà l'usuari del nivell en què s'ha produït l'error de validació.

Quan l'entrada de temps, despesa o ús material es considera no imputable, l'estat de validació sense superar es defineix com a **No aplicable** amb el detall de validació igual a **No aplicable**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Límit que no s'ha de superar en valors reals de vendes sense facturar

Quan s'aprova una entrada de temps, despesa o ús de materials, es creen registres de valors reals de cost i de vendes no facturades. Si el valor real de vendes sense facturar creat és imputable i s'assigna a una línia de contracte de temps i material, l'aplicació realitza una comprovació de validació de límit que no s'ha de superar als nivells següents:

  - Comprovació amb el límit configurat per al client de la línia de contracte del projecte
  - Comprovació amb el límit configurat a la línia de contracte
  - Comprovació amb el límit configurat per al client
  - Comprovació amb el límit configurat al contracte

Les comprovacions de cada nivell asseguren que l'import del valor de venda al valor real no infringirà el límit que no s'ha de superar en aquest nivell després de comptabilitzar l'import del registre de facturació ja registrat i l'import facturat fins a la data en aquest nivell.

Si la comprovació és correcta, el valor real de vendes no facturades rep un estat de límit que no s'ha de superar **Confirmat**.

Si la comprovació és incorrecta, el valor real de vendes no facturades rep un estat de límit que no s'ha de superar **Error**. El detall de validació informa l'usuari del nivell en què s'ha produït l'error de validació.

Quan el valor real de vendes no facturades es considera no facturable o complementari, si no hi ha una configuració de límit que no s'ha de superar en cap dels quatre nivells o si el valor real que s'està creant és Cost, Bestreta, Unitat de recursos o Vendes entre organitzacions, els camps **Estat del límit que no s'ha de superar** i **Detall de validació del límit que no s'ha de superar** s'han de definir com a **No aplicable**.

## <a name="reset-the-not-to-exceed-status"></a>Reiniciar l'estat del límit que no s'ha de superar

Podeu fer un restabliment massiu de l'estat del límit que no s'ha de superar. Els administradors de projecte poden ajustar la validació que no es pot excedir per prioritzar la facturació d'un cos de treball, temps, despesa o ús material concret sobre altres que ja s'han confirmat des de l'import disponible que no es pot excedir.

Un cop restablert l'estat del límit que no s'ha de superar als valors reals de vendes no facturades, l'import compromès es redueix. L'Administrador del projecte pot seleccionar un altre cos de feina, hora, despesa o entrada d'ús de materials que anteriorment no ha superat la validació del que no es pot excedir i de reavaluació. Amb la reducció de l'import confirmat, aquests valors reals passen ara la validació, cosa que ajuda l'Administrador del projecte a controlar i influir més en les transaccions facturables durant aquest període.

Per restablir l'estat del límit que no s'ha de superar, seleccioneu un o més valors reals a la visualització **Registre de facturació de temps i material** o **Valors reals** i, a continuació, seleccioneu **Restableix l'estat del límit que no s'ha de superar**.

L'estat del límit que no s'ha de superar es restableix a **No avaluat** en tots els valors reals seleccionats pertinents. Els valors reals per als quals es restableix l'estat del límit que no s'ha de superar són valors reals de vendes no facturades que encara no s'han facturat, no estan en un esborrany de factura i es marquen com a imputables. S'ignoren els altres valors reals seleccionats.

## <a name="reevaluate-not-to-exceed-status"></a>Tornar avaluar l'estat del límit que no s'ha de superar

Podeu fer una reavaluació massiva de l'estat del límit que no s'ha de superar. La reavaluació de l'estat del límit que no s'ha de superar és útil quan:

  - Hi ha hagut una renegociació dels límits que no s'han de superar amb el client i els valors reals s'han de tornar a avaluar.
  - L'administrador del projecte vol afinar la facturació del registre de vendes no facturades prioritzant un cos de treball sobre un altre.

Per reavaluar l'estat del límit que no s'ha de superar, seleccioneu un o més valors reals a la visualització **Registre de facturació de temps i material** o **Valors reals** i, a continuació, seleccioneu **Reavalua l'estat del límit que no s'ha de superar**.

Tots els valors reals seleccionats pertinents amb un límit que no s'ha de superar s'avaluaran en relació amb la configuració del límit que no s'ha de superar. Els valors reals que són rellevants per a la reavaluació de l'estat del límit que no s'ha de superar són valors reals de vendes no facturades que encara no s'han facturat, no estan en un esborrany de factura i es marquen com a imputables. Qualsevol altre valor real seleccionat.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
