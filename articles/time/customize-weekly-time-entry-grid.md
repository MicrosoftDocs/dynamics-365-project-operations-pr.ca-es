---
title: Ampliació d'entrades de temps
description: En aquest article es proporciona informació sobre com els desenvolupadors poden ampliar el control d'entrada de temps.
author: stsporen
ms.date: 01/27/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 7ed501af3fb2059ab3c3ab6f6c957fe518595d55
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914758"
---
# <a name="extending-time-entries"></a>Ampliació d'entrades de temps

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou un control personalitzat d'entrada de temps ampliable. Aquest control inclou les funcions següents:

- Introducció de temps horitzontalment durant una setmana
- Totals per dia, fila o setmana
- Còpia de files o setmanes
- Entrada de temps mitjançant HH:mm o HH.hh (es converteix automàticament en HH.hh)
- Importació a partir d'assignacions, reserves o cites

L'ampliació de les entrades de temps és possible en dos àmbits:
- [Afegir entrades de temps personalitzades per a l'ús propi](#add)
- [Personalització del control d'entrada de temps setmanal](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a>Afegir entrades de temps personalitzades per a l'ús propi

Les entrades de temps són una entitat principal utilitzada en diversos escenaris. A la fase 1 d'abril de 2020, es va introduir la solució central de TESA. TESA proporciona una entitat **Configuració** i una nova funció de seguretat **Usuari d'entrada de temps**. També s'hi han inclòs els nous camps, **msdyn_start** i **msdyn_end**, que tenen una relació directa amb **msdyn_duration**. L'entitat nova, la funció de seguretat i els camps permeten una aproximació més unificada al temps en diversos productes.


### <a name="time-source-entity"></a>Entitat d'origen de temps
| Camp | Descripció | 
|-------|------------|
| Nom  | El nom de l'entrada d'origen de temps que s'utilitza com a valor de la selecció quan es creen les entrades de temps. |
| Origen del temps per defecte [origen del temps: isdefault] | Per defecte, només es pot marcar un origen de temps per al valor per defecte. Això permet que les entrades canviïn per defecte a un origen de temps si no s'especifica. |
|Tipus d'origen del temps [origen del temps: sourcetype] | El tipus d'origen és una opció (tipus d'origen d'entrada de temps) que permet l'associació de l'origen del temps a una aplicació. Microsoft es reserva els valors superiors a 190.000.000.|


### <a name="time-entries-and-the-time-source-entity"></a>Entrades de temps i entitat d'origen de temps
Cada entrada de temps està associada a un registre d'origen de temps. Aquest registre determina quines aplicacions han de processar l'entrada de temps i com ho han de fer.

Les entrades de temps són sempre un bloc contigu de temps amb l'inici, la finalització i la duració enllaçats.

La lògica actualitzarà automàticament el registre d'entrada de temps en les situacions següents:

- Si es proporcionen dos dels tres camps següents, el tercer es calcula automàticament. 

    - **msdyn_start**
    - **msdyn_end**
    - **msdyn_duration**

- Els camps **msdyn_start** i **msdyn_end** tenen en compte la zona horària.
- Les entrades de temps creades amb només **msdyn_date** i **msdyn_duration** especificats s'iniciaran a mitjanit. Els camps **msdyn_start** i **msdyn_end** s'actualitzaran en conseqüència.

#### <a name="time-entry-types"></a>Tipus d'entrada de temps

Els registres d'entrada de temps tenen un tipus associat que defineix el comportament del flux d'enviament de l'aplicació associada.

|Etiqueta | Valor|
|-----|-----|
|En una pausa   |192,355,000|
|Viatge | 192,355,001|
|Hores extra   | 192,354,320|
|Treballa   | 192,350,000|
|Absència    | 192,350,001|
|Vacances   | 192,350,002|


## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a>Personalització del control d'entrada de temps setmanal
Els desenvolupadors poden afegir camps i cerques addicionals a altres entitats i implementar regles de negoci personalitzades per admetre els seus escenaris empresarials.

### <a name="add-custom-fields-with-lookups-to-other-entities"></a>Afegir camps personalitzats amb cerques a altres entitats
Hi ha tres passos principals per afegir un camp personalitzat a la quadrícula d'entrada de temps setmanal.

1. Afegiu el camp personalitzat al quadre de diàleg **Creació ràpida**.
2. Configureu la quadrícula per mostrar el camp personalitzat.
3. Afegiu el camp personalitzat a la pàgina **Edició de la fila** o **Edició de l'entrada de temps**, segons correspongui.

Assegureu-vos que el camp nou tingui les validacions necessàries a la pàgina **Edició de fila** o **Edició d'entrada de temps**. Com a part d'aquesta tasca, bloqueu el camp, segons l'estat de l'entrada de temps.

Quan afegiu un camp personalitzat a la quadrícula **Entrada de temps** i després creeu entrades de temps directament a la quadrícula, el camp personalitzat d'aquestes entrades es defineix automàticament per tal que coincideixi amb la fila. 

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Afegir el camp personalitzat al quadre de diàleg Creació ràpida
Afegiu el camp personalitzat al quadre de diàleg **Creació ràpida: crear una entrada de temps**. Els usuaris poden introduir un valor quan afegeixen entrades de temps seleccionant **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar la quadrícula per mostrar el camp personalitzat
Hi ha dues maneres d'afegir un camp personalitzat a la quadrícula **Entrada de temps setmanal**.

- Personalitzeu la visualització **Les meves entrades de temps setmanal** i afegiu-hi el camp personalitzat. Podeu especificar la posició i la mida del camp personalitzat a la quadrícula editant aquestes propietats a la visualització.
- Creeu una nova visualització d'entrada de temps personalitzat i definiu-la com a visualització per defecte. Aquesta visualització hauria de contenir els camps **Descripció** i **Comentaris externs**, a més de les columnes que voleu que inclogui la quadrícula. Podeu especificar la posició, la mida i l'ordre per defecte de la quadrícula editant les propietats a la visualització. A continuació, configureu el control personalitzat per a aquesta visualització per tal que sigui un control **Quadrícula d'entrada de temps**. Afegiu el control a la visualització i seleccioneu-lo per a **Web**, **Telèfon** i **Tauleta**. A continuació, configureu els paràmetres per a la quadrícula **Entrada de temps setmanal**. Definiu el camp **Data d'Inici** a **msdyn\_date**, definiu el camp **Durada** a **msdyn\_duration** i definiu el camp **Estat** com a **msdyn\_entrystatus**. El camp **Llista d'estatsnomés de lectura** està definit com a **192350002 (aprovat)**, **192350003 (enviat)** o **192350004 (sol·licitud de recuperació)**.

### <a name="add-the-custom-field-to-the-appropriate-edit-page"></a>Afegir el camp personalitzat a la pàgina d'edició adient
Les pàgines utilitzades per editar una entrada de temps o una fila d'entrades de temps es poden trobar a **Formularis**. El botó **Edita l'entrada** de la quadrícula obre la pàgina **Edita l'entrada** i el botó **Edita la fila** obre la pàgina **Edita la fila**. Podeu editar aquestes pàgines per tal que incloguin camps personalitzats.

Ambdues opcions eliminen alguns filtres estàndard de les entitats **Projecte** i **Tasca de projecte**, de manera que es veuen totes les visualitzacions de cerca per a les entitats. De fàbrica, només es veuen les visualitzacions de cerca rellevants.

Heu de determinar la pàgina adient per al camp personalitzat. El més probable és que, si heu afegit el camp a la quadrícula, hàgiu d'anar a la pàgina **Edició de la fila** que s'utilitza per als camps que s'apliquen a tota la fila d'entrades de temps. Si el camp personalitzat té un valor únic a la fila cada dia (per exemple, si és un camp personalitzat per a l'hora d'acabament), hauria d'anar a la pàgina **Edició d'entrada de temps**.

Per afegir el camp personalitzat a una pàgina, arrossegueu un element **Camp** a la posició adient de la pàgina i, a continuació, definiu-ne les propietats.

### <a name="add-new-option-set-values"></a>Afegir nous valors de conjunts d'opcions
Per afegir valors del conjunt d'opcions a un camp estàndard, seguiu aquests passos.

1. Obriu la pàgina d'edició del camp i, a continuació, a **Tipus**, seleccioneu **Edita** al costat del conjunt d'opcions.
2. Afegiu una opció nova que tingui una etiqueta i un color personalitzats. Si voleu afegir un nou estat de l'entrada de temps, el camp de fàbrica es diu **Estat de l'entrada**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar un nou estat d'entrada de temps com a només de lectura
Per designar un nou estat d'entrada de temps com a només de lectura, afegiu el nou valor d'entrada de temps a la propietat **Llista d'estat de només de lectura**. Assegureu-vos d'afegir el número, no l'etiqueta. La part editable de la quadrícula d'entrada de temps ara es bloquejarà per a les files que tenen l'estat nou. Per definir la propietat **Llista d'estats només de lectura** de manera diferent per a les diferents visualitzacions d'**Entrada de temps**, afegiu la quadrícula d'**Entrada de temps** a la secció **Controls personalitzats** d'una visualització i configureu els paràmetres segons calgui.

A continuació, afegiu regles de negocis per blocar tots els camps de les pàgines **Edició de fila** i **Edició d'entrada de temps**. Per accedir a les regles de negocis d'aquestes pàgines, obriu l'editor de formularis de cada pàgina i,a continuació, seleccioneu **Regles de negocis**. Podeu afegir l'estat nou a la condició en les regles de negocis existents o bé afegir una regla de negocis nova per a l'estat nou.

### <a name="add-custom-validation-rules"></a>Afegir regles de validació personalitzades
Podeu afegir dos tipus de regles de validació per a l'experiència de quadrícula **Entrada de temps setmanal**:

- Regles de negocis del client que funcionen a les pàgines
- Validacions de complements del servidor que s'apliquen a totes les actualitzacions d'entrades de temps

#### <a name="client-side-business-rules"></a>Regles de negocis del client
Utilitzeu regles de negoci per bloquejar i desbloquejar camps, introduir valors per defecte als camps i definir validacions que requereixin informació del registre d'entrada de temps actual. Per accedir a les regles de negocis d'una pàgina, obriu l'editor de formularis i,a continuació, seleccioneu **Regles de negocis**. A continuació, podeu editar les regles de negocis existents o afegir una regla de negocis nova.

#### <a name="server-side-plug-in-validations"></a>Validacions de complements del servidor
Heu d'utilitzar validacions de complements per a totes les validacions que requereixin un context més ampli que el disponible en un registre d'entrada de temps únic. També els heu d'utilitzar per a les validacions que voleu executar en actualitzacions en línia a la quadrícula. Per completar les validacions, creeu un complement personalitzat a l'entitat **Entrada de temps**.

### <a name="limits"></a>Límits
Actualment, la quadrícula **Entrada de temps** té un límit de mida de 500 files. Si hi ha més de 500 files, les files en excés no es mostraran. No hi ha manera d'augmentar aquest límit de mida.

### <a name="copying-time-entries"></a>Còpia d'entrades de temps
Utilitzeu la visualització **Còpia de columnes d'entrada de temps** per definir la llista de camps que es copiaran durant l'entrada de temps. **Data** i **Duració** són camps obligatoris i no s'han d'eliminar de la visualització.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
