---
title: Substitucions de preus de data de vigència
description: En aquest article s'explica com es defineixen les substitucions de preus per als preus específics de la llista de preus.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445997"
---
# <a name="date-effective-price-overrides"></a>Substitucions de preus de data de vigència 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les *substitucions de preus de data de vigència* proporcionen una manera de substituir o canviar preus específics de la llista de preus. Per exemple, teniu una llista de preus estàndard efectiva des de l'1 de gener de 2022 fins al 31 de desembre de 2022. Aquesta llista de preus té preus per a moltes funcions. El preu que està configurat per a la funció de **Tècnic de xarxa** és de 100 dòlars EUA (USD) per hora. Quan un tècnic de xarxa registra el temps entre l'1 de gener del 2022 i el 31 de desembre de 2022, el temps es compta com a 100 USD. L'1 d'octubre de 2022, heu d'ajustar el preu *només* per a la funció **Tècnic de xarxa**, de 100 USD per hora a 110 USD per hora. La característica **Substitueix els preus de data de vigència** us permet configurar aquest canvi com una substitució de la fila d'aquest preu de funció específic. Per tant, no cal que copieu la llista de preus completa i canvieu el preu només d'aquesta fila.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Substitucions de preus de data de vigència per als preus laborals

El procés de configurar substitucions de preus de data de vigència per a la mà d'obra d'un projecte consta de dos passos bàsics.

1. Habiliteu la característica **Substitucions de preus de data de vigència**.
1. Configureu una substitució de preus de data de vigència.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Habilitar la característica Substitucions de preus de data de vigència

> [!NOTE]
> Després d'habilitar la característica **Substitucions de preus de data de vigència** no es pot inhabilitar.

Per habilitar la característica **Substitucions de preus de data de vigència**, seguiu aquests passos.

1. Aneu a **Configuració** \> **Paràmetres**.
1. Obriu el registre **Paràmetres**.
1. A la subfinestra Acció, a la pestanya **Control de característiques**, seleccioneu **Habilita les substitucions de preus de data de vigència**.
1. Al quadre de diàleg de confirmació, seleccioneu **D'acord**.
1. Al cap d'uns moments, actualitzeu el navegador. Ara, les capacitats de substitució de preus de data de vigència haurien d'estar disponibles. Sabreu que aquestes capacitats s'han habilitat si el botó **Habilita les substitucions de data de vigència** ja no apareix a la subfinestra Acció.

### <a name="set-up-a-date-effective-price-override"></a>Configurar una substitució de preus de data de vigència

Les substitucions de preus de data de vigència només es poden configurar a les llistes de preus de **Cost**, **Vendes** o **Compra**.

> [!NOTE]
>El comportament de **Substitucions de preus de data de vigència** actualment té les limitacions següents:
>
> - Només els preus per funció i els marges comercials de preus per funció admeten la característica **Substitucions de preus de data de vigència** al Project Operations.
> - Quan copieu una llista de preus mitjançant l'acció **Copia** a la pàgina **Detalls de la llista de preus** i quan creeu una llista de preus del projecte des d'una llista de preus estàndard o personalitzada durant la creació del contracte, les substitucions de preus de data de vigència **no** es copien de la llista de preus d'origen.

Per configurar una substitució de preus de data de vigència per a un preu per funció o un marge comercial de preu per funció, seguiu aquests passos:

1. Obriu la pàgina de la llista de preus per a la qual voleu configurar la substitució de preus de data de vigència.
1. Seleccioneu la pestanya **Preus per funcions**. Aquesta pestanya mostra tots els registres de **Preu per funció** de la llista de preus.
1. Seleccioneu el registre de **Preu per funció** per al qual voleu configurar una substitució de preus de data de vigència i, a continuació, feu doble toc (o doble clic) a **Preu per funció** per obrir la pàgina **Detalls del preu per funció**.
1. Seleccioneu la pestanya **Substitucions de data de vigència**. La quadrícula d'aquesta pestanya mostra totes les substitucions de preus de data de vigència per al registre de **Preu per funció** seleccionat.
1. A la barra d'eines que hi ha a sobre de la quadrícula, seleccioneu **Nova substitució de preu per funció**. S'obre el control lliscant **Nova substitució de preu per funció**.
1. Especifiqueu la data de vigència, la unitat i el preu nou per a la substitució de preu. A continuació, seleccioneu **Desa** i tanqueu el formulari.

> [!NOTE]
> - Una substitució de preus de data de vigència per a un preu per funció o un marge comercial de preu per funció és aplicable a la mateixa combinació de valors de dimensió de preus que existeix a la fila **Preu per funció** o **Marge comercial de preu per funció** principal.
> - La data seleccionada al camp **Efectiu des del** hauria d'estar dins de les dates de vigència de la llista de preus principal. La substitució de preus tindrà efecte en la data seleccionada al camp **Efectiu des del** i s'aplicarà fins a la data d'acabament de la llista de preus principal. Si configureu una altra substitució de preus de data de vigència per al mateix preu per funció, la primera substitució de preus tindrà efecte en la data seleccionada al camp **Efectiu des del** i s'aplicarà fins a l'inici de la segona substitució.

## <a name="examples"></a>Exemples

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemple 1: Determinar la data de vigència per a un preu per funció que té substitucions de preus per funció

A l'exemple següent es mostra com es determina la data de vigència d'un preu per funció específic per al qual es configuren substitucions de preus per funcions.

**Llista de preus A: de l'1 de gener al 30 de juny**

*Preu per funció*

| Preu per funció | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|
| Tècnic de xarxa | Hora | 100 | Aquest preu s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre l'1 de gener i el 14 de març. |

*Substitució de preu per funció*

| Efectiu des del | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|
| Març de 15 | Hora | 110 | Aquest preu s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre el 15 de març i el 30 de març. |
| Abril de 1 | Hora | 120 | Aquest preu s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre l'1 d'abril i el 30 de juny. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemple 2: Determinar la data de vigència per a un marge comercial de preu per funció que té substitucions de marges comercials de preus per funció

A l'exemple següent es mostra com es determina la data de vigència d'un marge comercial de preu per funció específica per a la qual es configuren substitucions de marges comercials de preus per funció.

**Llista de preus A: de l'1 de gener al 30 de juny**

*Preu per funció*

| Preu per funció | Hores de feina | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|---|
| Tècnic de xarxa | Normal | Hora | 100 | Aquest preu s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre l'1 de gener i el 14 de març. |

*Marge comercial de preu de funció*

| Unitat d'organització | Hores de feina | % de marge comercial |
|---|---|---|
| Contoso EUA | Hores extra | 10% |

*Substitució de marge comercial de preus per funció*

| Efectiu des del | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|
| Març de 15 | 20% | Aquest percentatge de marge comercial s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre el 15 de març i el 30 de març. |
| Abril de 1 | 25 % | Aquest marge comercial s'utilitzarà en qualsevol transacció on la data de la transacció sigui entre l'1 d'abril i el 30 de juny. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
