---
title: Línies del subcontracte per als productes
description: En aquest tema s'explica com registrar les línies de subcontracte per als productes i utilitzar els diferents camps per registrar les compres de productes dels proveïdors.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323674"
---
# <a name="subcontract-lines-for-products"></a>Línies del subcontracte per als productes

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Un subcontracte al Dynamics 365 Project Operations pot tenir una línia de subcontracte per als productes. Aquestes línies permeten a un Administrador de projectes comprar productes dels proveïdors que poden utilitzar a les tasques del projecte.

Completeu els passos següents per crear una línia de subcontracte per a productes al Project Operations.

1. A la pàgina de navegació, seleccioneu **Subcontractes** i després obriu el subcontracte amb el qual voleu treballar. 
2. A la pestanya **Línies de subcontracte**, seleccioneu **+ Nou** per crear una línia de subcontracte nova.
3. A la pàgina **Creació ràpida**, al camp **Classe de transacció**, seleccioneu **Material** i introduïu o seleccioneu la informació dels camps obligatoris. 
4. Seleccioneu **Desa**.

A la taula següent es proporciona informació sobre els camps de la pàgina **Detalls de la línia de subcontracte** i la pàgina **Creació ràpida** perquè són rellevants per comprar productes.

| Camp | Descripció |
| ----- | ----------- |
| Nom | Nom de la línia de subcontracte. |
| Descripció | Descripció breu dels productes que s'encarreguen a la línia de subcontracte. |
| Tipus de línia | Aquest valor de camp és per defecte **Basat en quantitat**. |
| Mètode de facturació |  Mètode de facturació de la línia de subcontracte. Hi ha disponible una planificació de factura basada en fites per als mètodes de facturació de preu fix. |
| Classe de la transacció | Aquest valor de camp és per defecte **Temps**. Per crear línies de subcontracte per comprar productes, al camp **Classe de transacció**, seleccioneu **Material**. Aquesta selecció indica que la línia de subcontracte s'utilitza per registrar una compra de productes que s'utilitzaran en els projectes. |
| Seleccioneu el producte | Seleccioneu si el producte que es compra es manté al catàleg de productes o si és un producte fora de catàleg. |
| Producte | Seleccioneu un producte actiu del catàleg, Aquest camp només està disponible si **Seleccioneu el producte** s'ha definit com a **Existent**. |
| Producte fora de catàleg | Introduïu el nom del producte fora de catàleg. Aquest camp només està disponible si **Seleccioneu el producte** s'ha definit com a **Fora de catàleg**.  |
| Data de lliurament sol·licitada | Seleccioneu la data de lliurament necessària per als productes. Aquesta data també s'utilitza per seleccionar una llista de preus a les llistes de preus del projecte adjuntades al subcontracte. El cost del producte a la línia de subcontracte es pren per defecte d'aquesta llista de preus. |
| Data de lliurament contractada | Seleccioneu la data en què s'ha acordat per contracte que es lliurin els productes.  |
| Quantitat demanada | Introduïu la quantitat del producte que es compra al proveïdor. Si un administrador de projectes pren d'aquesta quantitat, es produirà un advertiment. |
| Grup d’unitats | Aquest valor es pren per defecte només per als productes del catàleg. Quan se selecciona alhora **Producte** i **Data de lliurament sol·licitada**, el sistema selecciona la llista de preus aplicable segons la data de lliurament. Es consulten els elements de la llista de preus relacionada per al producte coincident. Els valors d'unitat i grup d'unitats per defecte de la configuració del registre d'element de la llista de preus. |
| Unitat | Aquest valor pren per defecte la configuració de la unitat del registre d'element de la llista de preus. Podeu canviar-lo per una altra unitat segons convingui. La combinació de producte i unitat s'utilitza com a valor per defecte del preu unitari a la línia de subcontracte per als productes del catàleg existents. |
| Preu per unitat | El preu unitari pren el valor per defecte de la combinació de producte i unitat dels elements de la llista de preus relacionats amb la llista de preus del projecte que sigui aplicable a la data de lliurament sol·licitada de la línia de subcontracte.  |
| Subtotal | Aquest camp només de lectura es calcula com a preu de Quantitat x Unitat si ambdós camps tenen valors introduïts. Si el camp **Quantitat**, el camp **Preu unitari** o tots dos estan buits, podeu introduir un valor manualment.  |
| Impost sobre les vendes | Especifiqueu el valor de l'impost sobre les vendes. |
| Import total | Aquest camp calculat mostra la quantitat total de la línia de subcontracte després d'impostos. El valor d'aquest camp es calcula com a subtotal + impostos. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
