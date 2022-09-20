---
title: El preu efectiu de la data substitueix
description: En aquest article s'explica com configurar les substitucions de preus per a preus específics a la llista de preus.
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
# <a name="date-effective-price-overrides"></a>El preu efectiu de la data substitueix 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

*Les substitucions de preus efectives* amb data proporcionen una manera d'anul·lar o canviar preus específics de la llista de preus. Per exemple, teniu una llista de preus estàndard que és efectiva des de l'1 de gener de 2022 fins al 31 de desembre de 2022. Aquesta llista de preus té preus per a molts rols. El preu configurat per a la **funció de tècnic de** xarxa és de 100 dòlars EUA (USD) per hora. Quan un tècnic de xarxa registra el temps entre l'1 de gener de 2022 i el 31 de desembre de 2022, l'hora té un preu de 100 USD. L'1 d'octubre de 2022, heu d'ajustar el preu *només* per a la **funció de tècnic** de xarxa, de 100 USD per hora a 110 USD per hora. La **funció Data d'anul·lació del** preu efectiu et permet configurar aquest canvi com una substitució de la fila per al preu de funció específic. Per tant, no cal que copieu tota la llista de preus i canvieu el preu d'aquesta fila.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>El preu efectiu de la data anul·la els preus laborals

El procés d'establiment del preu efectiu de la data anul·la el temps de treball en un projecte consta de dos passos bàsics.

1. Activa la **funció Data de substitució** efectiva del preu.
1. Configureu una substitució del preu efectiva de la data.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activeu la funció Data en què el preu efectiu substitueix

> [!NOTE]
> Un cop activada la **funció Data en què el preu** efectiu substitueix, no es pot desactivar.

Per activar la **funció Data d'aprovació del preu**, segueix aquests passos.

1. Aneu a **Paràmetres** de configuració \>**·**.
1. Obriu el **registre Paràmetres**.
1. A la subfinestra d'accions, a la **pestanya Control de** característiques, seleccioneu **Habilita la data en què s'anul·la** el preu efectiu.
1. Al quadre de diàleg de confirmació, seleccioneu **D'acord**.
1. Al cap d'uns instants, actualitzeu el navegador. Les capacitats d'anul·lació de preus efectives de data ara haurien d'estar disponibles. Sabreu que aquestes capacitats s'han habilitat si **Habilita la data en què el preu efectiu substitueix** ja no apareix a la subfinestra d'acció.

### <a name="set-up-a-date-effective-price-override"></a>Configurar una data d'aprovació del preu efectiva

Les substitucions de preus efectives es poden configurar a les **llistes de preus de cost**, **vendes** o **compra**.

> [!NOTE]
>Actualment, el comportament de la **data en què s'anul·la** el preu efectiu té les limitacions següents:
>
> - Només els preus de les funcions i els marcatges de preus de funció admeten la funció Data d'anul·lació efectiva del **preu** del Project Operations.
> - Quan copieu una llista de preus mitjançant l'acció Copia **de la pàgina Detalls** de la **llista de preus i quan creeu una llista de preus del projecte a partir d'una llista de preus estàndard o personalitzada durant la** creació del contracte, les substitucions de preus efectives de data no **es copien** de la llista de preus d'origen.

Per configurar una substitució de preu efectiva per a un preu de funció o un marcatge del preu de funció, seguiu aquests passos.

1. Obriu la pàgina de la llista de preus per a la qual voleu configurar la data d'aplicació del preu.
1. Seleccioneu la **pestanya Preus de funció** . Aquesta pestanya mostra tots els **registres de preus** de rol de la llista de preus.
1. Seleccioneu el registre de preu de funció **per al qual voleu configurar un preu de substitució nou i efectiu i, a continuació, toqueu dues vegades (o feu doble clic)** Preu **de funció per obrir la pàgina Detalls** del preu de la **funció.**
1. Seleccioneu la **pestanya Data d'anul·lacions efectives**. La quadrícula d'aquesta pestanya mostra totes les substitucions de preus efectives per al registre de preus **de funció seleccionat**.
1. A la barra d'eines que hi ha a sobre de la quadrícula, seleccioneu **Substitueix el preu de** la funció nova. S'obre **el control lliscant de substitució** del preu de la funció nova.
1. Especifiqueu la data efectiva, la unitat i el preu nou per substituir el preu. A continuació, seleccioneu **Desa** i tanqueu el formulari.

> [!NOTE]
> - Una substitució de preu efectiva de data per a un preu de funció o un marcatge de preus de funció és aplicable a la mateixa combinació de valors de dimensió de preus que hi ha al preu de la funció principal **o al quadre** de preus de **funció**.
> - La data que se seleccioni al camp Efectiu des de **la** data d'entrada en vigor de la llista de preus principal. La substitució del preu entrarà en vigor a la data que se seleccioni al **camp Efectiu des de** i s'aplicarà fins a la data de finalització de la llista de preus principal. Si configures una altra substitució del preu de data efectiva per al mateix preu de funció, la primera substitució del preu entrarà en vigor a la data que se seleccioni al **camp Efectiu des de** i s'aplicarà fins a l'inici de la segona substitució.

## <a name="examples"></a>Exemples

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemple 1: determinació de l'efectivitat de la data per a un preu de funció que substitueix el preu de funció

L'exemple següent mostra com es determina l'efectivitat de la data per a un preu de funció específic per al qual es configuren les substitucions de preus de funció.

**Tarifa de preus A: de l'1 de gener al 30 de juny**

*Preu del rol*

| Preu del rol | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|
| Tècnic/a de xarxa | Hora | 100 | Aquest preu s'utilitzarà en totes aquelles operacions en què la data de l'operació estigui compresa entre l'1 de gener i el 14 de març. |

*S'anul·la el preu de funció*

| Efectiu des de | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|
| Març de 15 | Hora | 110 | Aquest preu s'utilitzarà en totes aquelles operacions en què la data de l'operació estigui compresa entre el 15 i el 30 de març. |
| Abril de 1 | Hora | 120 | Aquest preu s'utilitzarà en totes aquelles operacions en què la data de l'operació estigui compresa entre l'1 d'abril i el 30 de juny. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemple 2: determinació de l'efectivitat de la data per a un marcatge de preus de funció que té un marcatge de preus de funció substitueix

L'exemple següent mostra com es determina l'efectivitat de la data per a un marcatge de preus de funció específic per al qual es configuren les substitucions de preus de funció.

**Tarifa de preus A: de l'1 de gener al 30 de juny**

*Preu del rol*

| Preu del rol | Hores de feina | Unit | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|---|---|
| Tècnic/a de xarxa | Regular | Hora | 100 | Aquest preu s'utilitzarà en totes aquelles operacions en què la data de l'operació estigui compresa entre l'1 de gener i el 14 de març. |

*Marcatge del preu de la funció*

| Unitat organitzativa | Hores de feina | Marca % |
|---|---|---|
| Contoso EUA | Hores extra | 10% |

*El marcatge de preus de funció substitueix*

| Efectiu des de | Preu | Efecte sobre els preus de les transaccions entrants |
|---|---|---|
| Març de 15 | 20% | Aquest percentatge d'augment s'utilitzarà en qualsevol transacció en què la data de transacció estigui compresa entre el 15 i el 30 de març. |
| Abril de 1 | 25 % | Aquest marcatge s'utilitzarà en totes aquelles operacions en què la data de l'operació estigui compresa entre l'1 d'abril i el 30 de juny. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
