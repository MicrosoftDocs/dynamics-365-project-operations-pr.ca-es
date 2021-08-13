---
title: Afegir membres de l'equip des de la quadrícula Membre de l'equip
description: En aquest tema es proporciona informació sobre com administrar els recursos de membre de l'equip.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c4ff7792a9a99cbbe791a10dbc5157ffd51de285c02f23471532a09e7a55b031
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008394"
---
# <a name="add-team-members-from-the-team-member-grid"></a>Afegir membres de l'equip des de la quadrícula Membre de l'equip

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations inclou un escriptori digital d'Administració de recursos que proporciona una visió general visual de la demanda i l'aprofitament dels recursos a tota l'organització. Podeu utilitzar els gràfics d'aquest escriptori digital per visualitzar la informació següent:

- **Demanda de recursos**: el gràfic **Sol·licitud de recursos activa** mostra recursos que s'ha enviat. Els recursos s'agreguen per funció o projecte.
- **Demanda de recursos no enviats**: el gràfic **Demanda de recursos no assignats** mostra tots els requisits de recursos que no s'han enviat. Aquest gràfic ajuda els administradors de recursos a veure la demanda que no és ferma i podria ser enviada a través d'una sol·licitud de recursos.
- **Ús facturable durant la setmana passada**: el gràfic **Utilització per funció** mostra el percentatge de l'ús facturable real de l'organització per funció en comparació amb l'objectiu d'ús facturable per funció.

    > [!NOTE]
    > Per fer que el gràfic **Ús per funció** estigui disponible, creeu una feina que executi el flux de treball **UpdateRoleUtilization**. Aquesta feina periòdica s'executa cada set dies per calcular l'ús facturable dels set dies anteriors. Els resultats s'agreguen per funció.

## <a name="manage-project-team-members"></a>Administrar membres de l'equip del projecte

Els administradors de projecte poden utilitzar l'escriptori digital d'administrador de recursos per administrar els recursos dels projectes. Per exemple, poden afegir un membre de l'equip directament a un projecte i reservar un membre de l'equip per complir els requisits dels recursos que s'han capturat per un recurs genèric.

### <a name="add-a-team-member-directly-to-a-project"></a>Afegir un membre de l'equip directament a un projecte

Per afegir un membre de l'equip directament a un projecte , seleccioneu **Crea** al formulari **Projectes** de la pestanya **Equip**. Apareixerà el quadre de diàleg **Creació ràpida: membre de l'equip del projecte**. En aquest quadre de diàleg, podeu dur a terme aquestes tasques:

- **Reservar un recurs amb nom**: al camp **Recursos que es poden reservar**, seleccioneu el nom del recurs. A continuació, seleccioneu la funció, definiu el període i seleccioneu un mètode d'assignació. El recurs amb nom que heu seleccionat s'afegeix al projecte mitjançant el mètode d'assignació i el calendari de recursos seleccionat.
- **Afegir un recurs genèric**: deixeu el camp **Recurs que es pot reservar** en blanc i, a continuació, seleccioneu la funció, definiu el període i seleccioneu el mètode d'assignació preferit. Un recurs genèric s'afegeix a l'equip com a contenidor. El contenidor conté el patró de demanda que s'utilitza per reservar els recursos amb nom a l'equip. El requisit es realitza d'acord amb el calendari del projecte.
- **Afegir un recurs amb nom a l'equip sense haver de consumir la capacitat dels recursos**: al camp **Recurs que es pot reservar**, seleccioneu un recurs. Seleccioneu el període i, a continuació, seleccioneu **Cap** com a mètode d'assignació. El recurs s'afegeix a l'equip, però la capacitat del recurs no es consumeix a través d'una reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reserveu un membre de l'equip per complir els requisits de recursos per a un recurs genèric

Al Project Operations, podeu reservar un recurs genèric en un equip del projecte. També podeu especificar la funció, la capacitat requerida i la manera com es distribueix aquesta capacitat. Per al requisit de recursos, podeu especificar els atributs associats amb el recurs genèric. Aquests atributs inclouen les aptituds necessàries, la unitat organitzativa preferida i els recursos preferents.

Completeu els passos que s'indiquen a continuació per especificar les aptituds necessàries en un recurs genèric per a un desenvolupador.

1. Al formulari **Projectes**, a la pestanya **Equip**, seleccioneu **Crea** per reservar un recurs genèric.
2. A la visualització **Tots els membres de l'equip**, a la columna **Requisits de recursos**, seleccioneu l'enllaç per afegir les competències necessàries per al recurs genèric.
3. Al formulari **Requisit de recursos**, a la quadrícula **Aptituds**, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Afegeix una característica de requisit nova** per afegir les aptituds necessàries per al desenvolupador.
4. Al formulari de diàleg **Creació ràpida: característica de requisit**, al camp **Característica**, seleccioneu l'aptitud necessària.
5. Al camp **Valor de qualificació**, seleccioneu el nivell de competència per a aquesta aptitud. 
6. Al camp **Requisit de recursos**, definiu el requisit dels recursos d'origen d'unitats organitzatives o fins i tot de recursos amb nom. Quan hagueu acabat, trieu **Desa**.
7. Al formulari **Requisits de recursos**, seleccioneu **Reserva** per complir el requisit de recursos. També podeu seleccionar el recurs genèric a la quadrícula **Tots els membres de l'equip** i, a continuació, seleccionar **Reserva**.

    > [!NOTE]
    > En aquest exemple, hi ha 40 hores necessàries però no hores reservades reals, perquè els recursos genèrics no tenen reserves. A més, no hi ha cap hora assignada, perquè el recurs genèric s'ha afegit directament a l'equip en comptes d'afegir-se mitjançant l'assignació de tasques.

    Al formulari **Auxiliar de planificació**, podeu filtrar els recursos disponibles mitjançant els requisits que s'especifiquen al requisit del recurs. Els recursos s'ordenen segons els paràmetres d'ordenació que s'especifiquen al Tauler de planificació.

   Alguns dels filtres més habituals són:

    - **Característiques amb una valoració**: filtreu per competències, certificacions i altres qualitats de recursos, a més d'avaluacions de competència.
    - **Funcions**: filtreu per les funcions per defecte que estan assignades a recursos que es poden reservar.
    - **Unitats organitzatives**: filtreu recursos que es poden reservar per les unitats organitzatives que tenen assignades.

8. Si no esteu satisfet amb els resultats de la cerca inicial de requisits, podeu canviar els criteris de filtratge. Expandiu la subfinestra **Filtra la visualització** a l'esquerra i, a continuació, seleccioneu **Cerca** per cercar recursos addicionals. Per canviar la manera com s'ordenen els resultats, seleccioneu **Ordena**.
9. Seleccioneu recursos segons la demanda que s'especifica a l'exigència, tal com s'indicava a la part superior de la quadrícula. Podeu desactivar la selecció de cel·les a la quadrícula i deixar oberta la capacitat d'un recurs. Només es pot seleccionar un recurs cada vegada com a reservat.
10. Seleccioneu **Reserva** per reservar el recurs seleccionat i deixeu obert el Tauler de planificació, de manera que pugueu seleccionar recursos addicionals. Alternativament, seleccioneu **Reserva i surt** per reservar el recurs seleccionat i tanqueu el Tauler de planificació.
11. Torneu a la visualització **Tots els membres de l'equip**. A la quadrícula, heu de tenir en compte que el recurs genèric s'ha substituït pel recurs amb nom i que les 40 hores es mostren com a reservades per a aquest recurs.

    > [!NOTE]
    > No es mostren les hores assignades, perquè estaven reservades directament a l'equip. No s'han reservat mitjançant l'assignació de tasques.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Assignar recursos genèrics a tasques i generar requisits de recursos

Al Project Operations, podeu crear tasques i, a continuació, assignar-hi recursos genèrics. La demanda de recursos llavors es pot representar amb marcadors de posició mentre s'estima la planificació i els números financers. A continuació, podeu generar requisits de recursos per als recursos genèrics i complir-los.

1. Al formulari **Projectes**, a la pestanya **Planificació**, seleccioneu **Afegeix** per crear una tasca.
2. Al camp **Recursos**, seleccioneu el símbol **Selector de recursos**. El Selector de recursos apareix i mostra els membres de l'equip existents per al projecte.
3. Introduïu el nom del recurs genèric nou i, a continuació, seleccioneu **Crea**.
4. Al quadre de diàleg **Creació ràpida: membre de l'equip del projecte** que apareix, al camp **Funció**, seleccioneu la funció per al recurs genèric. 
5. Al camp **Unitat de recursos**, seleccioneu la unitat organitzativa del recurs genèric. A continuació, seleccioneu **Desa**. El membre de l'equip genèric ara està assignat a la tasca.

   A la pestanya **Equip**, veureu el nou membre de l'equip genèric. Observeu que només té hores assignades. Aquestes hores són la suma de totes les tasques assignades al membre de l'equip genèric. El membre genèric de l'equip encara no té les hores obligatòries o un requisit de recurs.

6. Ara podeu assignar el membre de l'equip genèric a altres tasques mitjançant el Selector de recursos.

   Quan hàgiu acabat d'assignar el recurs genèric a les tasques, podeu generar un requisit de recurs per al recurs genèric.

7. A la pestanya **Equip**, seleccioneu el recurs genèric i, a continuació , seleccioneu **Genera un requisit**. Quan es genera el requisit, el membre de l'equip genèric tindrà hores obligatòries i un enllaç per al requeriment del recurs.

  Després de reservar un recurs amb nom, el recurs genèric se suprimeix de l'equip i se substitueix pel recurs amb nom. A la pestanya **Planificació**, les assignacions de recursos genèrics s'eliminen i se substitueixen pel recurs amb nom.

  > [!NOTE]
  > Aquest comportament només es produeix quan un recurs amb nom està completament reservat per al requisit de recursos genèrics. Quan un recurs amb nom reemplaça parcialment el requisit de recurs genèric o diversos recursos amb nom reemplacen els requisits de recurs genèric, el recurs genèric es manté assignat a la tasca.

El Project Operations no assigna tots dos recursos a la tasca, perquè aquest comportament produiria una planificació menys predictible. En aquest senzill exemple, és fàcil dividir les hores de manera equitativa entre dos recursos. No obstant, en escenaris més complexos que impliquen diverses tasques i diversos recursos, el PSA hauria de fer suposicions sobre com hauria d'assignar les reserves que es reben per a diversos recursos en diverses tasques.

Per tant, en aquests escenaris, l'administrador del projecte s'encarrega d'analitzar les diverses reserves i d'assignar-les segons calgui. Per assignar les reserves, l'administrador del projecte assigna les tasques des dels recursos genèrics als recursos amb nom i, a continuació, utilitza la visualització **Conciliació** per assegurar-se que l'assignació funciona amb les reserves.

### <a name="edit-a-resource-requirement"></a>Editar un requisit de recursos

Després d'haver creat un requisit de recurs, pot ser que un administrador de projectes o un administrador de recursos vulguin editar els detalls per perfeccionar els criteris de cerca quan s'utilitza el Tauler de planificació. Per editar el requisit de recursos, seguiu aquests passos.

1. Al formulari **Projectes**, a la pestanya **Equip**, seleccioneu l'enllaç a qualsevol requisit en un recurs genèric.
2. Al formulari **Requisit de recursos** que apareix, introduïu la informació de camp necessària

   Al formulari **Requisit de recursos**, l'administrador del projecte o administrador de recursos també pot definir aptituds, funcions, preferències de recursos i la unitat organitzativa preferida.

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualitzar les reserves de recursos un cop s'hagin reservat en un projecte

Després d'afegir un recurs genèric o amb nom a un equip de projecte, podeu canviar les reserves del recurs.

1. Al formulari **Projectes**, a la pestanya **Equip**, seleccioneu un membre de l'equip i seleccioneu **Mantén les reserves**.
 
   El Tauler de planificació apareix i mostra les reserves de membres de l'equip del projecte. Expandiu el registre del membre de l'equip per visualitzar les hores que s'han reservat a aquest projecte i altres projectes que estan consumint la capacitat del membre de l'equip.

2. Seleccioneu i arrossegueu la reserva per ampliar-la o reduir-la. Apareix un quadre de diàleg **Crea la reserva de recursos** que us permet ajustar la reserva.
3. Feu clic amb el botó dret a la reserva. A continuació, podeu utilitzar el menú de drecera per completar les accions següents:

    - Canviar l'estat de la reserva
    - Editar la reserva
    - Substituir un recurs a l'equip del projecte

### <a name="change-the-booking-status"></a>Canviar l'estat de la reserva

Podeu canviar qualsevol estat de reserva per defecte o personalitzat.

El Project Operations inclou els estats següents:

- **Cancel·lat**: cancel·la la reserva d'un recurs i allibera la capacitat del recurs.
- **Reserva fixa**: consumeix la capacitat d'un recurs. Una reserva normalment té aquest estat quan obriu **Mantén les reserves** a la quadrícula **Tots els membres de l'equip** al formulari **Projectes**.
- **Reserva flexible**: afegeix un recurs a un equip però no consumeix la capacitat del recurs. Aquest estat indica que el recurs s'ha reservat per a un treball potencial però té capacitat si és necessari en altres feines. A la visualització de la disponibilitat de recursos globals, les reserves flexibles tenen un estat diferent de les reserves fixes.
- **Proposat**: representa una proposta de l'administrador de recursos o l'administrador de projectes per a un recurs. Les propostes no consumeixen la capacitat d'un recurs i el recurs no s'afegeix a l'equip del projecte. Per reservar el recurs de l'equip, l'administrador del projecte ha d'acceptar la proposta.

### <a name="submit-resource-requests"></a>Enviament de sol·licituds de recursos

Les sol·licituds de recursos s'utilitzen per dur a terme la demanda o requisit de recurs que ha de complir un administrador de recursos. Per a un recurs genèric que ja està a l'equip, podeu enviar una sol·licitud de recurs directament. Una sol·licitud de recurs es pot complir de dues maneres:

- L'administrador de recursos compleix directament la sol·licitud. En aquest cas, el recurs genèric se substitueix per una reserva fixa que té un recurs amb nom.
- L'administrador de recursos proposa un recurs a l'administrador de projectes i el director del projecte aprova o rebutja el recurs proposat.

#### <a name="direct-fulfillment-of-resource-requests"></a>Compliment directe de sol·licituds de recursos

Quan es genera un requisit de recurs, un administrador de projecte pot enviar una sol·licitud de recurs per a un recurs genèric seleccionant el recurs i, a continuació, seleccionant **Envia la sol·licitud**. Els comentaris sobre el recurs es poden proporcionar a l'administrador de recursos que està complint la sol·licitud. Després d'enviar la sol·licitud, el camp **Estat** per al membre de l'equip canvia a **Enviat**. Quan l'administrador de recursos compleix la sol·licitud, el membre de l'equip genèric se substitueix pel recurs amb nom a la quadrícula **Tots els membres de l'equip**.

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilitzar una proposta de recurs per a sol·licituds de recursos

En lloc de fer la reserva directament d'un recurs d'una sol·licitud de recurs, un administrador de recursos pot proposar un recurs a l'administrador del projecte. Pot ser que un administrador de recursos utilitzi aquesta opció quan no hi hagi una coincidència exacta per als requisits. Quan un administrador de recursos proposa un recurs, l'administrador del projecte veu que el camp **Estat** del membre genèric de l'equip canvia a **Necessita revisió**.

Podeu visualitzar el recurs proposat juntament amb una visualització de l'efecte de la reserva de la proposta. 

1. Feu doble clic al membre de l'equip que tingui l'estat **Necessita revisió**. 
2. Seleccioneu la pestanya **Recursos proposats**.
3. Seleccioneu **Accepta totes les propostes** per acceptar tots els recursos proposats o **Rebutja totes les propostes** per rebutjar-les. Si accepteu els recursos proposats, es reserven de manera fixa al projecte com a membres de l'equip i reemplacen els recursos genèrics.

> [!NOTE]
> Heu d'acceptar o rebutjar tots els recursos proposats. No es poden acceptar ni rebutjar parcialment.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir un recurs a l'equip del projecte

De vegades, un administrador de projecte ha de substituir un membre de l'equip reservat en un projecte.

1. Al formulari **Projectes**, a la pestanya **Equip**, seleccioneu el recurs que cal substituir i seleccioneu **Mantén les reserves**.
2. Expandiu el recurs per visualitzar els projectes als quals està assignat.
3. Feu clic amb el botó dret del ratolí al projecte i seleccioneu **Substitueix el recurs**.
4. Si coneixeu el recurs que voleu substituir per al recurs actual, seleccioneu o escriviu-ne el nom i, a continuació, seleccioneu **Torna a assignar**.

O bé. Si heu de cercar un recurs, seguiu aquests passos.

1. Seleccioneu **Cerca una substitució**.

   L'Auxiliar de planificacions retorna una llista de substituts disponibles. A l'Auxiliar de planificació, podeu continuar filtrant els recursos disponibles per trobar un substitut adient.

2. Per substituir el recurs, seleccioneu el recurs que voleu i, a continuació, seleccioneu **Substitueix**.   

   Les reserves i assignacions es substitueixen pel recurs nou.

## <a name="reconcile-team-member-bookings-and-assignments"></a>Conciliar les reserves dels membres de l'equip i les assignacions

Per als membres de l'equip, les reserves i assignacions estan lleugerament vinculades. En altres paraules, els recursos poden tenir assignacions però no reserves, o poden tenir reserves però no assignacions. Idealment, les reserves i assignacions s'han d'alinear perquè els recursos tinguin capacitat confirmada de dur a terme l'assignació de tasques. No obstant, les reserves poden basar-se en la disponibilitat i els temps de treball podrien canviar a mesura que el projecte continua. Per tant, la lleugera vinculació de les reserves i les assignacions proporciona flexibilitat.

El Project Operations té una pestanya **Conciliació** que permet als administradors projectar les reserves dels membres de l'equip i els seus treballs per a equips de projectes.

La pestanya **Conciliació** mostra les reserves i les assignacions al nivell de l'assignació de tasques individuals per a cada membre de l'equip. Mostra hores a les cel·les que representen períodes de temps de mesos a dies.

La pestanya també mostra un total de la xarxa global per al projecte, juntament amb una columna total.

Per a cada recurs, la pestanya calcula la diferència entre les reserves dels membres de l'equip i un valor consolidat de les assignacions de tasques del membre de l'equip. Idealment, aquesta diferència hauria de ser 0 (zero). En altres paraules, no hi hauria d'haver diferències entre les reserves i les assignacions. Les diferències es marquen amb color i un ombrejat per cridar l'atenció sobre dues condicions:

- **Manca de reserves**: es produeix quan un recurs té més assignacions que reserves. Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot voler corregir aquesta situació ampliant les reserves del recurs fins a cobrir el dèficit.
- **Excés de reserves**: es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques. Aquesta situació podria ser acceptable en els casos en què s'ha reservat el recurs al projecte abans d'haver produït una assignació de tasques. No obstant, en altres casos, el recurs no està planificat per assignar-se a tasques. En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.

En alguns casos, quan visualitzeu temps en un nivell superior al nivell de dia (per exemple, al nivell de mes), pot ser que vegeu una diferència neta de zero per a un recurs. És a dir, reserves = assignacions. No obstant, si visualitzeu temps al nivell de la setmana, podeu veure que hi ha assignacions de zero hores i reserves de 40 hores a la primera setmana, però assignacions de 40 hores i reserves de zero hores a la segona setmana. En general, les reserves i assignacions es concilien, però difereixen d'una setmana a la següent.

Quan visualitzeu el temps en nivells superiors, les cel·les de la pestanya **Conciliació** tenen un indicador per informar-vos que hi ha diferències en nivells inferiors. Feu doble clic en una cel·la per apropar-vos per visualitzar la diferència. A continuació, podeu fer clic amb el botó dret per allunyar-vos. En seleccionar un recurs i **Diferència següent** a la barra d'eines de la quadrícula, podeu anar a la diferència següent entre les reserves i les assignacions d'aquest recurs. Seleccioneu **Diferència anterior** per tornar. També podeu desactivar l'indicador de diferències i el comportament de la navegació a **Configuració**.

Si teniu assignacions de tasca per a un recurs però no hi ha cap reserva, al formulari **Projectes**, a la pestanya **Conciliació**, seleccioneu la manca de reserves i, a continuació, seleccioneu **Amplia la reserva**. El quadre de diàleg **Amplia la reserva** apareix i mostra la reserva necessària per fer front a la manca del recurs. El quadre de diàleg també mostra les reserves existents del recurs en tots els projectes o altres entitats planificables. Si seleccioneu **D'acord** per crear la reserva del recurs, independentment de la disponibilitat del recurs, pot ser que hi hagi un excés de reserves.

L'administrador de projectes o administrador de recursos poden utilitzar el Tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]