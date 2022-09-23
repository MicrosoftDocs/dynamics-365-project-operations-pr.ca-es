---
title: Línies del subcontracte per als productes
description: En aquest article s'explica com registrar les línies de subcontractació de productes i utilitzar els diferents camps per registrar les compres de productes als venedors.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1ca042eaf95a5e252f00248e83efb959ab3ce801
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522830"
---
# <a name="subcontract-lines-for-products"></a>Línies del subcontracte per als productes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Un subcontracte al Dynamics 365 Project Operations pot tenir una línia de subcontracte per als productes. Aquestes línies permeten a un Administrador de projectes comprar productes dels proveïdors que poden utilitzar a les tasques del projecte.

Completeu els passos següents per crear una línia de subcontracte per a productes al Project Operations.

1. A la pàgina de navegació, seleccioneu **Subcontractes** i després obriu el subcontracte amb el qual voleu treballar. 
2. A la pestanya **Línies de subcontracte**, seleccioneu **+ Nou** per crear una línia de subcontracte nova.
3. A la pàgina **Creació ràpida**, al camp **Classe de transacció**, seleccioneu **Material** i introduïu o seleccioneu la informació dels camps obligatoris. 
4. Seleccioneu **Desa**.

A la taula següent es proporciona informació sobre els camps de la pàgina **Detalls de la línia de subcontracte** i la pàgina **Creació ràpida** perquè són rellevants per comprar productes.

| Camp | Descripció | Impacte funcional|
| ----- | ----------- | ----------- |
| Nom | Nom de la línia de subcontracte per ajudar a identificar-la. |Es mostrarà com la primera columna de totes les consultes basada en les línies de subcontracte.
| Descripció | Descripció breu dels productes que s'encarreguen a la línia de subcontracte. | Cap |
| Tipus de línia | Aquest camp té un valor per defecte **Basat en quantitat**. |Cap |
| Mètode de facturació | Es tracta d'un conjunt d'opcions que representa els dos models de contractació principals que admet el Project Operations: **Preu fix** i **Temps i material**. | Segons el mètode de facturació seleccionat, una planificació de factura basada en fites està disponible per a les línies de subcontracte amb el mètode de facturació de preus fixos. |
| Classe de la transacció |Aquest camp té un valor per defecte de **Temps**. Per crear línies de subcontracte per comprar productes, definiu el camp **Classe de transacció** com a **Material**.  | Això indica que la línia de subcontracte s'utilitza per registrar la compra de productes que s'utilitzaran en els projectes. |
| Seleccioneu el producte | Seleccioneu si el producte que es compra es manté al catàleg de productes o si és un producte fora de catàleg. |Cap |
| Producte | Seleccioneu un producte actiu del catàleg, Aquest camp només està disponible si **Seleccioneu el producte** s'ha definit com a **Existent**. |La combinació de **Producte** i **Unitat** s'utilitzarà com a valor per defecte o es calcularà per al preu unitari de la línia de subcontracte.
| Producte fora de catàleg | Introduïu el nom del producte fora de catàleg. Aquest camp només està disponible si **Seleccioneu el producte** s'ha definit com a **Fora de catàleg**.  |El preu de compra no s'emplenarà automàticament per als productes fora de catàleg.|
| Data de lliurament sol·licitada | Introduïu la data de lliurament necessària per als productes.| Aquesta data també s'utilitza per seleccionar una llista de preus a les llistes de preus del projecte adjuntades al subcontracte. El cost del producte a la línia de subcontracte es pren per defecte d'aquesta llista de preus. |
| Data de lliurament contractada | Introduïu la data en què s'ha acordat per contracte que es lliurin els productes.  |Cap|
| Quantitat demanada | Introduïu la quantitat del producte que es compra al proveïdor.| S'utilitzarà per mostrar advertiments quan un administrador de projecte prengui un excés d'aquesta quantitat.|
| Grup d’unitats | Aquest valor es pren per defecte només per als productes del catàleg. |Quan se selecciona alhora **Producte** i **Data de lliurament sol·licitada**, el sistema selecciona la llista de preus aplicable segons la data de lliurament. Es consulten els elements de la llista de preus relacionada per al producte coincident. Els valors d'unitat i grup d'unitats per defecte de la configuració del registre d'element de la llista de preus. |
| Unitat | Aquest valor és per defecte la unitat configurada al registre d'element de la llista de preus. Podeu canviar-lo per una altra unitat segons convingui.| La combinació de producte i unitat s'utilitza com a valor per defecte del preu unitari a la línia de subcontracte per als productes del catàleg existents. |
| Preu per unitat | El preu unitari pren el valor per defecte de la combinació de producte i unitat dels elements de la llista de preus relacionats amb la llista de preus del projecte que sigui aplicable a la data de lliurament sol·licitada de la línia de subcontracte.  |Cap |
| Subtotal | Aquest camp només de lectura es calcula com a preu de Quantitat x Unitat si ambdós camps tenen valors introduïts. Si el camp **Quantitat**, el camp **Preu unitari** o tots dos estan buits, podeu introduir un valor manualment.  |Cap |
| Impost sobre les vendes | Especifiqueu el valor de l'impost sobre les vendes. |Cap |
| Import total | Aquest camp calculat mostra la quantitat total de la línia de subcontracte després d'impostos. El valor d'aquest camp es calcula com a Subtotal + impostos. |Cap |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
