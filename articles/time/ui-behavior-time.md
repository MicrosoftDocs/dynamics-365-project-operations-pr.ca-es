---
title: Comportament de la interfície d'usuari d'entrada de temps
description: En aquest tema es proporciona informació sobre el comportament de la interfície d'usuari de l'entrada de temps.
author: stsporen
ms.date: 03/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: fd62fb1d8e0b2d859cb7da8b99cb725af587ff2f
ms.sourcegitcommit: 639ec8a41fda15dedfd6918702d33ea406999ba6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304289"
---
# <a name="time-entry-ui-behavior"></a>Comportament de la interfície d'usuari d'entrada de temps

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


La quadrícula **Entrada de temps setmanal** és un control personalitzat que té dues seccions principals, **Dimensions** i **Duració**.

## <a name="keyboard-shortcuts"></a>Dreceres de teclat
| Acció        | Drecera                  |
|------------   |------------------------   |
| Nova           | Alt + Maj + n           |
| Copia la fila      | Alt + Maj + c           |
| Edició d'entrada    | Alt + Maj + e           |
| Edita la fila      | Alt + Maj + Ctrl + e    |
| Entrada oberta    | Alt + Maj + o           |
| Enviament        | Alt + Maj + s           |
| Recupera        | Alt + Maj + r           |
| Delete        | Alt + Maj + d           |
| Copia la setmana     | Alt + Maj + w           |

## <a name="dimensions"></a>Dimensions
A la secció **Dimensions** es mostren totes les dimensions en què es pot introduir el temps. Les dimensions següents s'admeten de fàbrica:

  - Project
  - Tasca del projecte
  - Funció
  - Type
  - Estat de l’entrada

La secció **Dimensions** no permet l'edició en línia. Aquesta secció està basada en una visualització que permet afegir camps personalitzats a la quadrícula d'entrada de temps setmanal.

## <a name="duration"></a>Durada
La secció Duració mostra els dies de la setmana com a capçaleres de columna. Aquesta secció permet l'edició en línia. Després de crear una fila d'entrada de temps amb les dimensions adequades, els usuaris poden introduir ràpidament la quantitat de temps que han invertit en aquestes dimensions.

## <a name="create-a-new-time-entry"></a>Crea una entrada de temps nova

1. A la quadrícula d'entrada de temps, seleccioneu **Nou**. 
2. Al quadre de diàleg **Creació ràpida d'entrada de temps**, seleccioneu la data d'entrada de temps.
3. Introduïu les dades per a les dimensions **Projecte**, **Tasca del projecte**, **Funció** i **Duració**. Aquesta informació s'ha d'afegir en minuts, hores o dies escrivint **h**, **m** o **d** juntament amb el nombre. 
4. Introduïu una descripció per a l'entrada i comentaris que es puguin compartir externament en relació a l'entrada de temps. 

Quan deseu l'entrada, els valors introduïts es mostren a la secció **Dimensions**. La informació introduïda al camp **Duració** apareix a la data en la qual s'ha creat l'entrada de temps.

Els camps de cerca es basen en visualitzacions del sistema. Per exemple, després que un usuari entri en un projecte , el camp **Tasca de projecte** està definit a la visualització **Còpia** per defecte. Per crear entrades de temps per a les tasques que no s'assignen a l'usuari, seleccioneu **Canvia la visualització** al quadre de diàleg de cerca i seleccioneu la visualització **Totes les tasques de projecte actives**.

## <a name="edit-a-time-entry"></a>Editar una entrada de temps 
Els detalls d'alguns camps de la pàgina d'entrada de temps, com ara **Descripció** i **Comentaris externs**, no es mostren a la quadrícula d'entrada de temps setmanal. En lloc d'això, un petit indicador triangular apareix a les cel·les **Duració** que tenen aquests detalls addicionals. 

1. Per editar una entrada de temps, seleccioneu la cel·la que voleu actualitzar a l'entrada de temps.
2. Seleccioneu **Edita els detalls** per actualitzar les dades a la subfinestra **Formulari principal d'entrada de temps**. 

## <a name="copy-a-time-entry-row"></a>Copiar una fila d'entrada de temps
Després de crear la primera fila d'entrada de temps, podeu seleccionar **Copia la fila** per copiar la fila sencera en una fila nova. Quan una fila es copia d'aquesta manera, les dimensions i duracions també es copien. També podeu seleccionar **Edita la fila** per actualitzar els valors de les dimensions i les duracions a la secció **Duració**.

## <a name="open-a-time-entry-behavior"></a>Comportament en obrir una entrada de temps
Per admetre l'entrada òptima i ràpida en els camps més importants, la quadrícula d'entrada de temps setmanal mostra un subconjunt de dimensions i temps de duració seleccionats. Per visualitzar tots els detalls d'una sola vegada a l'entrada de temps, a **Edita l'entrada**, seleccioneu **Obre**.

## <a name="submit-a-time-entry"></a>Enviar una entrada de temps
Podeu enviar una única entrada de temps o un grup d'entrades de temps seleccionant un bloc de cel·les o una fila d'entrada de temps sencera i, a continuació, seleccionant **Envia**. Les entrades de temps enviades apareixen com a entrades pendents d'aprovació a la pàgina **Aprovació** dels aprovadors. Després d'haver enviat correctament les entrades de temps, no es poden editar.

## <a name="recall-a-time-entry"></a>Recuperar una entrada de temps
Podeu recuperar entrades de temps que heu enviat. Podeu recuperar una entrada d'una sola vegada, un bloc d'entrades de temps o tota una fila d'entrades de temps. Es poden editar les entrades de temps recuperades.

## <a name="time-entry-status"></a>Estat de l'entrada de temps

- **Esborrany**: les entrades de temps noves s'assignen automàticament a un estat **Esborrany**. Només es poden suprimir les entrades de temps que tenen un estat **Esborrany**.
- **Enviada**: quan s'envia una entrada de temps, l'estat s'actualitzarà a **Enviada**. 
- **Aprovada**: quan s'aprova una entrada de temps enviada, l'estat s'actualitzarà a **Aprovada**. 
- **Retornada**: si es rebutja una entrada de temps, l'estat s'actualitzarà a **Retornada** i l'entrada estarà disponible per a la correcció i el reenviament. 

## <a name="view-rejection-comments"></a>Veure comentaris sobre el rebuig
Quan una entrada de temps és rebutjada per un aprovador, l'aprovador podria afegir comentaris per ajudar el recurs a comprendre la raó del rebuig. Per visualitzar els comentaris de rebuig d'una entrada de temps, seleccioneu **Obre l'entrada**. Els comentaris de rebuig es mostraran a la cronologia. L'usuari pot respondre als comentaris de rebuig abans de tornar a enviar l'entrada.

## <a name="copy-week"></a>Copia la setmana
Després de crear algunes quantes entrades de temps, els usuaris poden crear diverses entrades de temps a la vegada.

1. Al formulari **Entrades de temps**, seleccioneu **Copia la setmana** per crear entrades de temps addicionals massivament. 
2. Al quadre de diàleg **Copia**, a la secció **Del període**, utilitzeu els camps **Data d'inici** i **Data de finalització** per definir l'interval de dates des d'on copiar entrades de temps. 
3. A la secció **Al període**, al camp **Data d'inici**, especifiqueu la data on crear les entrades de temps. 
4. Seleccioneu **Copia**. Per a la data especificada a **Al període**, es crea una còpia de les entrades de temps del corresponent dia de la setmana a **Del període**. Per exemple, l'entrada de temps del dilluns de la setmana passada es copia al dilluns de la setmana especificada a **Al període**.

## <a name="import"></a>Importa
El mateix procés bàsic s'utilitza per importar a partir de reserves, assignacions i intercanvis. Podeu especificar l'interval de dates de les reserves que s'importen i, a continuació, seleccionar explícitament les reserves que haurien de copiar-se com a entrades de temps d'esborrany. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
