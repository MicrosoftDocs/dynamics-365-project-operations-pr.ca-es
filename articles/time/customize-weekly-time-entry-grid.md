---
title: Ampliació d'entrades de temps
description: En aquest tema es proporciona informació sobre com els desenvolupadors poden ampliar el control d'entrada de temps.
author: stsporen
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c36a47b09e6012925a047f81318e89167d5c506facaae8d72b0bb6e8e267a7d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993319"
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
Cada entrada de temps està associada a un registre d'origen de temps. Aquest registre determina la manera i quines aplicacions han de processar l'entrada de temps.

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

1. Afegiu el camp personalitzat al quadre de diàleg de creació ràpida.
2. Configureu la quadrícula per mostrar el camp personalitzat.
3. Afegiu el camp personalitzat al flux de la tasca d'edició de la fila o el flux de la tasca d'edició de la cel·la.

Assegureu-vos que el camp nou tingui les validacions necessàries al flux de la tasca d'edició de la fila o de la cel·la. Com a part d'aquest pas, bloqueu el camp, segons l'estat de l'entrada de temps.

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Afegir el camp personalitzat al quadre de diàleg de creació ràpida
Afegiu el camp personalitzat al quadre de diàleg **Creació ràpida d'entrada de temps**. Llavors, quan s'afegeixen entrades de temps, podeu introduir un valor seleccionant **Nova**.

### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar la quadrícula per mostrar el camp personalitzat
Hi ha dues maneres d'afegir un camp personalitzat a la quadrícula d'entrada de temps setmanal:

  - Personalitzar una visualització i afegir un camp personalitzat
  - Crea una entrada de temps personalitzada per defecte nova 


#### <a name="customize-a-view-and-add-a-custom-field"></a>Personalitzar una visualització i afegir un camp personalitzat

Personalitzeu la visualització **Les meves entrades de temps setmanal** i afegir-hi el camp personalitzat. Podeu triar la posició i la mida del camp personalitzat a la quadrícula editant aquestes propietats a la visualització.

#### <a name="create-a-new-default-custom-time-entry"></a>Crea una entrada de temps personalitzada per defecte nova

Aquesta visualització hauria de contenir els camps **Descripció** i **Comentaris externs**, a més de les columnes que voleu tenir a la quadrícula. 

1. Trieu la posició, la mida i l'ordre per defecte de la quadrícula editant aquestes propietats a la visualització. 
2. Configureu el control personalitzat per a aquesta visualització per tal que sigui un control **Quadrícula d'entrada de temps**. 
3. Afegiu aquest control a la visualització i seleccioneu-lo per a la web, telèfons i tauletes. 
4. Configureu els paràmetres per a la quadrícula d'entrada de temps setmanal. 
5. Definiu el camp **Data d'Inici** a **msdyn_date**, definiu el camp **Duració** a **msdyn_duration** i definiu el camp **Estat** a **msdyn_entrystatus**. 
6. Per a la visualització per defecte, el camp **Llista d'estat de només lectura** s'estableix a **192350002,19235003,192350004**. El camp **Flux de tasca d'edició de fila** s'estableix a **msdyn_timeentryrowedit**. El camp **Flux de tasca d'edició de cel·la** s'estableix a **msdyn_timeentryedit**. 
7. Podeu personalitzar aquests camps per afegir o suprimir l'estat de només de lectura o per utilitzar una altra experiència basada en tasques (TBX) per a la fila o l'edició de la cel·la. Aquests camps estan ara enllaçats a un valor estàtic.


> [!NOTE] 
> Ambdues opcions retiraran alguns filtres de fàbrica de les entitats **Projecte** i **Tasca de projecte**, de manera que es veuran totes les visualitzacions de cerca per a les entitats. De fàbrica, només es veuen les visualitzacions de cerca rellevants.

Determineu el flux de la tasca adient per al camp personalitzat. Si heu afegit el camp a la quadrícula, hauria d'anar al flux de la tasca d'edició de files que s'utilitza per als camps que s'apliquen a tota la fila d'entrades de temps. Si el camp personalitzat té un valor únic cada dia, com ara un camp personalitzat per a l'**Hora d'acabament**, hauria d'anar al flux de la tasca d'edició de cel·les.

Per afegir el camp personalitzat a un flux de la tasca, arrossegueu un element **Camp** a la posició adient de la pàgina i, a continuació, definiu les propietats del camp. Definiu la propietat **Origen** a **Entrada de temps** i definiu la propietat **Camp de dades** al camp personalitzat. La propietat **Camp** especifica el nom de visualització a la pàgina de TBX. Seleccioneu **Aplica** per desar els canvis al camp i, a continuació, seleccioneu **Actualitza** per desar els canvis a la pàgina.

Per utilitzar una nova pàgina personalitzada de TBX en el seu lloc, creeu un procés nou. Definiu la categoria a **Flux del procés de negoci**, definiu l'entitat a **Entrada d'hora** i definiu el tipus de procés de negoci a **Executa el procés com a flux de la tasca**. A **Propietats**, la propietat **Nom de la pàgina** s'ha de definir al nom de visualització de la pàgina. Afegiu tots els camps corresponents a la pàgina de TBX. Deseu i activeu el procés. Actualitzeu la propietat del control personalitzat del flux de la tasca rellevant al valor **Nom** del procés.

### <a name="add-new-option-set-values"></a>Afegir nous valors de conjunts d'opcions
Per afegir valors de conjunt d'opcions a un camp de fàbrica, obriu la pàgina d'edició del camp i, a continuació, a **Tipus**, seleccioneu **Edita** al costat del conjunt d'opcions. Afegiu una opció nova que tingui una etiqueta i un color personalitzats. Si voleu afegir un nou estat de l'entrada de temps, el camp de fàbrica es diu **Estat de l'entrada**, no **Estat**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar un nou estat d'entrada de temps com a només de lectura
Per designar un nou estat d'entrada de temps com a només de lectura, afegiu el nou valor d'entrada de temps a la propietat **Llista d'estat de només de lectura**. La part editable de la quadrícula d'entrada de temps es bloquejarà per a les files que tenen l'estat nou.
A continuació, afegiu regles de negoci per blocar tots els camps de les pàgines de TBX **Edició de les files d'entrades de temps** i **Edició d'entrades de temps**. Podeu accedir a les regles de negoci d'aquestes pàgines obrint l'editor del flux del procés de negoci de la pàgina i,a continuació, seleccionant **Regles de negoci**. Podeu afegir l'estat nou a la condició en les regles de negocis existents o bé afegir una regla de negocis nova per a l'estat nou.

### <a name="add-custom-validation-rules"></a>Afegir regles de validació personalitzades
Hi ha dos tipus de regles de validació que podeu afegir per a l'experiència de quadrícula d'entrada de temps setmanal:

- Regles de negoci del client que funcionen en quadres de diàleg de creació ràpida i a les pàgines de TBX.
- Validacions del connector del costat del servidor que s'apliquen a totes les actualitzacions d'entrada de temps.

#### <a name="business-rules"></a>Regles de negocis
Utilitzeu regles de negoci per bloquejar i desbloquejar camps, introduir valors per defecte als camps i definir validacions que requereixin informació del registre d'entrada de temps actual. Podeu accedir a les regles de negoci d'una pàgina de TBX obrint l'editor del flux del procés de negoci de la pàgina i, a continuació, seleccionant **Regles de negoci**. A continuació, podeu editar les regles de negocis existents o afegir una regla de negocis nova. Per a validacions encara més personalitzades, podeu fer que una regla de negocis executi JavaScript.

#### <a name="plug-in-validations"></a>Validacions de complement
Utilitzeu validacions de complements per a totes les validacions que requereixin un context més ampli que el disponible en un registre de temps únic o per a totes les validacions que voleu executar en actualitzacions en línia a la quadrícula. Per completar la validació, creeu un complement personalitzat a l'entitat **Entrada de temps**.

### <a name="copying-time-entries"></a>Còpia d'entrades de temps
Utilitzeu la visualització **Còpia de columnes d'entrada de temps** per definir la llista de camps que es copiaran durant l'entrada de temps. **Data** i **Duració** són camps obligatoris i no s'han d'eliminar de la visualització.


[!INCLUDE[footer-include](../includes/footer-banner.md)]