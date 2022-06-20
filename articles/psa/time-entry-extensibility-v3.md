---
title: Personalització de l'entrada de temps setmanal
description: En aquest article s'ofereix informació sobre com implementar regles de negoci personalitzades que admeten les pràctiques d'una organització.
author: stsporen
ms.custom:
- dyn365-projectservice
ms.date: 07/09/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: bdc8df4050d895504fa126e2ee55fcd3b4de123f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918944"
---
# <a name="customize-weekly-time-entry"></a>Personalització de l'entrada de temps setmanal 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

A la versió 3.3 del Microsoft Dynamics 365 Project Service Automation, Microsoft ha presentat una moderna quadrícula que permet que els recursos de projecte introdueixin ràpidament les hores de fins a tota una setmana. La nova quadrícula d'entrada de temps setmanal pot mostrar els totals per a les entrades per data, per fila o per setmana. Els recursos poden fer còpies d'entrades de temps dins de la setmana i també copiar de manera massiva des de setmanes anteriors. Els personalitzadors del sistema poden personalitzar la visualització afegint-hi camps, afegint cerques a altres entitats i implementant regles de negoci personalitzades per segueixin les pràctiques de l'organització.

A l'entrada de temps i la nova quadrícula de temps setmanal s'hi accedeix a través del mapa del lloc. L'experiència d'entrada de temps personalitzada no extensible que formava part de versions del PSA anteriors ha estat substituïda per la quadrícula d'entrada de temps setmanal extensible i també per una experiència alternativa a la quadrícula i el calendari només de lectura. A causa d'aquest canvi, els usuaris poden introduir l'hora en quantitats setmanals.

## <a name="page-layout"></a>Disposició de pàgina
La nova quadrícula d'entrada de temps setmanal és un control personalitzat que té una barra d'eines i dues seccions principals, **Dimensions** i **Duració**. La barra d'eines inclou un botó que només s'aplica a aquest control personalitzat per a la quadrícula d'entrada de temps. Per contra, els botons de la subfinestra Acció de la part superior de la pàgina s'apliquen als tres tipus de controls que estan admesos a l'entrada de temps: el control d'entrada de temps setmanal, el control només de lectura i el control de calendari.

### <a name="dimensions"></a>Dimensions
A la secció **Dimensions** es mostren, com a capçaleres de columna, totes les dimensions en què es pot introduir el temps. Les dimensions següents s'admeten de fàbrica:

- Projecte
- Tasca del projecte
- Funció
- Tipus
- Estat de l'entrada

La secció **Dimensions** no permet l'edició en línia. Aquesta secció està basada en una visualització que permet afegir camps personalitzats a la quadrícula d'entrada de temps setmanal. Per obtenir informació sobre com afegir camps personalitzats, vegeu la secció "Extensibilitat" més endavant en aquest article.

### <a name="duration"></a>Duració
La secció Duració mostra els dies de la setmana com a capçaleres de columna. Aquesta secció permet l'edició en línia. Després de crear una fila d'entrada de temps que té les dimensions adequades, els usuaris poden introduir ràpidament, en línia, la quantitat de temps que han invertit en aquestes dimensions.

## <a name="create-a-new-time-entry"></a>Crea una entrada de temps nova
Per crear una entrada de temps nova a la quadrícula d'entrada de temps, seleccioneu **Crea**. Apareixerà el quadre de diàleg **Creació ràpida d'entrada de temps**. En aquest quadre de diàleg, els usuaris poden seleccionar la data d'entrada de temps i, a continuació, introduir les dades per a les dimensions **Projecte**, **Tasca de projecte**, **Funció** i **Duració** en minuts, hores o dies escrivint **h**, **m** o **d**, juntament amb el número. Els usuaris també poden introduir una descripció i els comentaris que es poden compartir externament per a l'entrada de temps. Quan els usuaris desin els canvis, els valors que s'han introduït a les dimensions es mostren a la secció **Dimensions**. La informació de duració que s'hagi introduït al camp **Duració** apareix a la data en la qual s'ha creat l'entrada de temps.

Els camps de cerca es basen en visualitzacions del sistema. Per exemple, després que un usuari entri en un projecte , el camp **Tasca de projecte** està definit a la visualització **Còpia** per defecte. Per crear entrades de temps per a les tasques que no s'assignen a l'usuari, seleccioneu **Canvia la visualització** al quadre de diàleg de cerca i seleccioneu la visualització **Totes les tasques de projecte actives**.

## <a name="edit-a-time-entry"></a>Editar una entrada de temps
Els detalls d'alguns camps de la pàgina d'entrada de temps, com ara **Descripció** i **Comentaris externs**, no es mostren a la quadrícula d'entrada de temps setmanal. En lloc d'això, un petit indicador triangular apareix a les cel·les de duració que tenen aquests detalls addicionals. Seleccioneu la cel·la i, a continuació, seleccioneu **Edita els detalls** per visualitzar les dades de la subfinestra **Edició ràpida**. Per editar o actualitzar els detalls d'una entrada de temps específica que no és part de la quadrícula d'entrada de temps setmanal, els usuaris han d'obrir la subfinestra **Edició ràpida**.

## <a name="copy-a-time-entry-row"></a>Copiar una fila d'entrada de temps
Després de crear la primera fila d'entrada de temps, els usuaris poden seleccionar **Copia la fila** per copiar la fila sencera en una fila nova. Quan una fila es copia d'aquesta manera, les dimensions i duracions també es copien. Els usuaris també poden seleccionar **Edita la fila** per actualitzar els valors de les dimensions i les duracions en línia a la secció **Duració**.

## <a name="open-a-time-entry"></a>Obrir una entrada de temps
Per admetre l'entrada òptima i ràpida en els camps més importants, la quadrícula d'entrada de temps setmanal mostra un subconjunt de dimensions i temps de duració seleccionats. Per visualitzar tots els detalls d'una sola vegada a l'entrada de temps, a **Edita l'entrada**, seleccioneu **Obre**.

## <a name="submit-a-time-entry"></a>Enviar una entrada de temps
Els usuaris poden enviar una única entrada de temps o un grup d'entrades de temps seleccionant un bloc de cel·les o una fila d'entrada de temps sencera i, a continuació, seleccionant **Envia**. Les entrades de temps enviades apareixen com a entrades pendents d'aprovació a la pàgina **Aprovació** dels aprovadors. Després d'haver enviat correctament les entrades de temps, no es poden editar.

## <a name="recall-a-time-entry"></a>Recuperar una entrada de temps
Podeu recuperar entrades de temps que heu enviat. Podeu recuperar una entrada d'una sola vegada, un bloc d'entrades de temps o tota una fila d'entrades de temps. Les entrades de temps recuperades estan disponibles per als recursos per editar-les.

## <a name="time-entry-status"></a>Estat de l'entrada de temps
Les entrades de temps noves s'assignen automàticament a un estat **Esborrany**. Quan s'envia una entrada de temps, l'estat s'actualitzarà a **Enviada**. Quan s'aprova una entrada de temps enviada, l'estat s'actualitzarà a **Aprovada**. Si es rebutja una entrada de temps, l'estat s'actualitzarà a **Retornada** i l'entrada estarà disponible per a la correcció i el reenviament. Només es poden suprimir les entrades de temps que tenen un estat **Esborrany**.

## <a name="view-rejection-comments"></a>Veure comentaris sobre el rebuig
Quan una entrada de temps és rebutjada per un aprovador, l'aprovador podria afegir comentaris de rebuig per ajudar el recurs a comprendre la raó del rebuig. Per visualitzar els comentaris de rebuig d'una entrada de temps, seleccioneu **Obre l'entrada**. Els comentaris de rebuig es mostraran a la cronologia. A la cronologia, el recurs pot respondre als comentaris de rebuig abans de retornar l'entrada.

## <a name="copy-week"></a>Copia la setmana
Després de crear algunes d'entrades de temps, els usuaris poden seleccionar **Copia la setmana** crear entrades de temps addicionals massivament. Apareix el quadre de diàleg **Copia**. A la secció **Del període**, utilitzeu els camps **Data d'inici** i **Data de finalització** per definir l'interval de dates des d'on copiar entrades de temps. A la secció **Al període**, al camp **Data d'inici**, especifiqueu la data on crear les entrades de temps. A continuació, seleccioneu **Copia**. Per a la data especificada al període d'inici, es crea una còpia de les entrades de temps del corresponent dia de la setmana al període de destinació. Per exemple, l'entrada de temps del dilluns de la setmana passada es copia al dilluns de la setmana especificada al període de destinació.

## <a name="import"></a>Importar
El mateix procés bàsic s'utilitza per importar a partir de reserves, assignacions i intercanvis. Els usuaris poden especificar l'interval de dates des d'on s'importen les reserves s'importen. Han de seleccionar explícitament les reserves que s' han de copiar en entrades de temps en esborrany. A la versió anterior, les entrades de temps suggerides apareixien a la quadrícula i al calendari, i es perdien quan s'actualitzava la sessió.

## <a name="extensibility"></a>Capacitat d'ampliació
### <a name="add-custom-fields-that-have-lookups-to-other-entities"></a>Afegir camps personalitzats que tenen cerques a altres entitats
Hi ha tres passos principals per afegir un camp personalitzat a la quadrícula d'entrada de temps setmanal.

1.  Afegiu el camp personalitzat al quadre de diàleg de creació ràpida.
2.  Configureu la quadrícula per mostrar el camp personalitzat.
3.  Afegiu el camp personalitzat al flux de la tasca d'edició de la fila o el flux de la tasca d'edició de la cel·la, segons convingui.

També heu d'assegurar-vos que el camp nou tingui les validacions necessàries al flux de la tasca d'edició de la fila o de la cel·la. Com a part d'aquest pas, heu de blocar el camp, segons l'estat de l'entrada de temps.

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a>Afegir el camp personalitzat al quadre de diàleg de creació ràpida
Heu d'afegir el camp personalitzat al quadre de diàleg Creació ràpida d'entrada de temps. per tal que els usuaris puguin introduir un valor en afegir entrades de temps mitjançant el botó **Crea**.

#### <a name="configure-the-grid-to-show-the-custom-field"></a>Configurar la quadrícula per mostrar el camp personalitzat
Hi ha dues maneres d'afegir un camp personalitzat a la quadrícula d'entrada de temps setmanal. La primera opció és personalitzar la visualització **Les meves entrades de temps setmanal** i afegir-hi el camp personalitzat. Podeu triar la posició i la mida del camp personalitzat a la quadrícula editant aquestes propietats a la visualització.

La segona opció és crear una nova visualització d'entrada de temps personalitzat i definir-la com a visualització per defecte. Aquesta visualització hauria de contenir els camps **Descripció** i **Comentaris externs**, a més de les columnes que voleu tenir a la quadrícula. Podeu triar la posició, la mida i l'ordre per defecte de la quadrícula editant aquestes propietats a la visualització. A continuació, configureu el control personalitzat per a aquesta visualització per tal que sigui un control **Quadrícula d'entrada de temps**. Afegiu aquest control a la visualització i seleccioneu-lo per a la web, telèfons i tauletes. A continuació, configureu els paràmetres per a la quadrícula d'entrada de temps setmanal. Definiu el camp **Data d'Inici** a **msdyn_date**, definiu el camp **Duració** a **msdyn_duration** i definiu el camp **Estat** a **msdyn_entrystatus**. Per a la visualització per defecte , el camp **Llista d'estat de només lectura** es defineix com a **192350002,192350003,192350004**, el camp **Flux de la tasca d'edició de files** es defineix com a **msdyn_timeentryrowedit**, i el camp **Flux de la tasca d'edició de cel·les** es defineix com a **msdyn_timeentryedit**. Podeu personalitzar aquests camps per afegir o suprimir l'estat de només de lectura o per utilitzar una altra experiència basada en tasques (TBX) per a la fila o l'edició de la cel·la. Aquests camps han d'estar lligats a un valor estàtic.

#### <a name="add-the-custom-field-to-the-appropriate-edit-task-flow"></a>Afegir el camp personalitzat al flux de la tasca d'edició adient
Les pàgines de TBX que s'utilitzen per a l'edició es poden trobar a **Processos**. Les pàgines per defecte són **Project Service - Edició de files d'entrades de temps** i **Project Service - Edició d'entrada de temps**. Podeu editar aquestes pàgines per defecte o crear-ne de noves personalitzades per a les pàgines de TBX.

> [!NOTE] 
> Ambdues opcions retiraran alguns filtres de fàbrica de les entitats **Projecte** i **Tasca de projecte**, de manera que es veuran totes les visualitzacions de cerca per a les entitats. De fàbrica, només es veuen les visualitzacions de cerca rellevants.

Heu de determinar el flux de la tasca adient per al camp personalitzat. El més probable és que, si heu afegit el camp a la quadrícula, hauria d'anar al flux de la tasca d'edició de files que s'utilitza per als camps que s'apliquen a tota la fila d'entrades de temps. Si el camp personalitzat té un valor únic cada dia, com ara un camp personalitzat per a l'**Hora d'acabament**, hauria d'anar al flux de la tasca d'edició de cel·les.

Per afegir el camp personalitzat a un flux de la tasca, arrossegueu un element **Camp** a la posició adient de la pàgina i, a continuació, definiu les seves propietats. Definiu la propietat **Origen** a **Entrada de temps** i definiu la propietat **Camp de dades** al camp personalitzat. La propietat **Camp** especifica el nom de visualització a la pàgina de TBX. Seleccioneu **Aplica** per desar els canvis al camp. A continuació, seleccioneu **Actualitza** per desar els canvis a la pàgina.

Per utilitzar una nova pàgina personalitzada de TBX en el seu lloc, creeu un procés nou. Definiu la categoria a **Flux del procés de negoci**, definiu l'entitat a **Entrada d'hora** i definiu el tipus de procés de negoci a **Executa el procés com a flux de la tasca**. A **Propietats**, la propietat **Nom de la pàgina** s'ha de definir al nom de visualització de la pàgina. Afegiu tots els camps corresponents a la pàgina de TBX. Deseu i activeu el procés i, a continuació, actualitzeu la propietat del control personalitzat del flux de la tasca rellevant al valor **Nom** del procés.

### <a name="add-new-option-set-values"></a>Afegir nous valors de conjunts d'opcions
Per afegir valors de conjunt d'opcions a un camp de fàbrica, obriu la pàgina d'edició del camp i, a continuació, a **Tipus**, seleccioneu **Edita** al costat del conjunt d'opcions. A continuació, afegiu una opció nova que tingui una etiqueta i un color personalitzats. Si voleu afegir un nou estat de l'entrada de temps, el camp de fàbrica es diu **Estat de l'entrada**, no **Estat**.

### <a name="designate-a-new-time-entry-status-as-read-only"></a>Designar un nou estat d'entrada de temps com a només de lectura
Per designar un nou estat d'entrada de temps com a només de lectura, afegiu el nou valor d'entrada de temps (el número, no l'etiqueta) a la propietat **Llista d'estat de només de lectura**. La part editable de la quadrícula d'entrada de temps es bloquejarà per a les files que tenen l'estat nou.
A continuació, afegiu regles de negoci per blocar tots els camps de les pàgines de TBX **Edició de les files d'entrades de temps** i **Edició d'entrades de temps**. Podeu accedir a les regles de negoci d'aquestes pàgines obrint l'editor del flux del procés de negoci de la pàgina i,a continuació, seleccionant **Regles de negoci**. Podeu afegir l'estat nou a la condició en les regles de negocis existents o bé afegir una regla de negocis nova per a l'estat nou.

### <a name="add-custom-validation-rules"></a>Afegir regles de validació personalitzades
Hi ha dos tipus de regles de validació que podeu afegir per a l'experiència de la quadrícula d'entrada de temps setmanal: •   Regles de negocis del client que funcionen en quadres de diàleg de creació ràpida i pàgines de TBX •   Validacions de connector del costat del servidor que s'apliquen a totes les actualitzacions d'entrades de temps

#### <a name="business-rules"></a>Regles de negocis
Utilitzeu regles de negoci per bloquejar i desbloquejar camps, introduir valors per defecte als camps i definir validacions que requereixin informació del registre d'entrada de temps actual. Podeu accedir a les regles de negoci d'una pàgina de TBX obrint l'editor del flux del procés de negoci de la pàgina i, a continuació, seleccionant **Regles de negoci**. A continuació, podeu editar les regles de negocis existents o afegir una regla de negocis nova. Per a validacions encara més personalitzades, podeu fer que una regla de negocis executi JavaScript.

#### <a name="plug-in-validations"></a>Validacions de complement
Heu d'utilitzar validacions de complements per a totes les validacions que requereixin un context més ampli que el disponible en un registre de temps únic o per a totes les validacions que voleu executar en actualitzacions en línia a la quadrícula. Per completar la validació, creeu un complement personalitzat a l'entitat **Entrada de temps**.

> [!IMPORTANT] 
> Actualment, un problema conegut a les pàgines de TBX impedeix que els usuaris puguin corregir la informació i tornar a seleccionar Fet quan una actualització falla una validació de complements. Com a solució alternativa, configureu les validacions de regles de negocis per evitar aquesta situació en la mesura del possible.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
