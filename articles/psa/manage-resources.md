---
title: Administrar els recursos
description: En aquest tema es proporciona informació sobre com administrar els recursos.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b067f900fa49bba04536b49600dbe80a2167f707
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997814"
---
# <a name="manage-resources"></a>Administrar els recursos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

El Dynamics 365 Project Service Automation inclou un escriptori digital d'administració de recursos que proporciona una visió general visual de la demanda i l'aprofitament dels recursos a tota l'organització. Podeu utilitzar els gràfics d'aquest escriptori digital per visualitzar la informació següent:

- **Demanda de recursos**: el gràfic **Sol·licitud de recursos activa** mostra recursos que s'ha enviat. Els recursos s'agreguen per funció o projecte.
- **Demanda de recursos no enviats**: el gràfic **Demanda de recursos no assignats** mostra tots els requisits de recursos que no s'han enviat. Ajuda els administradors de recursos a veure la demanda que no és ferma i podria ser enviada a través d'una sol·licitud de recursos.
- **Ús facturable durant la setmana passada**: el gràfic **Utilització per funció** mostra el percentatge de l'ús facturable real de l'organització per funció en comparació amb l'objectiu d'ús facturable per funció.

    > [!NOTE]
    > Per fer que el gràfic **Ús per funció** estigui disponible, creeu una feina que executi el flux de treball UpdateRoleUtilization. Aquesta feina periòdica s'executa cada set dies per calcular l'ús facturable dels set dies anteriors. Els resultats s'agreguen per funció.

## <a name="manage-project-team-members"></a>Administrar membres de l'equip del projecte

Els administradors de projecte poden utilitzar l'escriptori digital d'administrador de recursos per administrar els recursos dels projectes. Per exemple, poden afegir un membre de l'equip directament a un projecte i reservar un membre de l'equip per complir els requisits dels recursos que s'han capturat per un recurs genèric.

### <a name="add-a-team-member-directly-to-a-project"></a>Afegir un membre de l'equip directament a un projecte

Per afegir un membre de l'equip directament a un projecte , seleccioneu **Crea** a la pàgina **Projectes** de la pestanya **Equip**. Apareixerà el quadre de diàleg **Creació ràpida: membre de l'equip del projecte**. En aquest quadre de diàleg, podeu dur a terme aquestes tasques:

- **Reservar un recurs amb nom**: al camp **Recursos que es poden reservar**, seleccioneu el nom del recurs. A continuació, seleccioneu la funció, definiu el període i seleccioneu un mètode d'assignació. El recurs amb nom que heu seleccionat s'afegeix al projecte mitjançant el mètode d'assignació i el calendari de recursos seleccionat.
- **Afegir un recurs genèric**: deixeu el camp **Recurs que es pot reservar** en blanc i, a continuació, seleccioneu la funció, definiu el període i seleccioneu el mètode d'assignació preferit. Un recurs genèric s'afegeix a l'equip com a marcador de posició per mantenir el patró de demanda que s'utilitza per reservar els recursos amb nom a l'equip. El requisit es realitza d'acord amb el calendari del projecte.
- **Afegir un recurs amb nom a l'equip sense haver de consumir la capacitat dels recursos**: al camp **Recurs que es pot reservar**, seleccioneu un recurs. A continuació, seleccioneu el període, i seleccioneu **Cap** com a mètode d'assignació. El recurs s'afegeix a l'equip, però la capacitat del recurs no es consumeix a través d'una reserva.

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a>Reserveu un membre de l'equip per complir els requisits de recursos per a un recurs genèric

Al PSA, podeu reservar un recurs genèric en un equip del projecte i especificar la funció, la capacitat requerida i la manera com es distribueix aquesta capacitat. Al requeriment de recursos, podeu especificar els atributs associats amb el recurs genèric. Aquests atributs inclouen les aptituds necessàries, la unitat organitzativa preferida i els recursos preferents.

Seguiu els passos que s'indiquen a continuació per especificar les aptituds necessàries en un recurs genèric per a un desenvolupador.

1. A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu **Crea** per reservar un recurs genèric.

    ![Recurs genèric reservat a l'equip](media/Resource-Management-image9.png)

2. A la visualització **Tots els membres de l'equip**, a la columna **Requisits de recursos**, seleccioneu l'enllaç per afegir les competències necessàries per al recurs genèric.

    ![Enllaç de requisit](media/Resource-Management-image10.png)

3. A la pàgina **Requisit de recursos** que es mostra, a la quadrícula **Aptituds**, seleccioneu els punts suspensius (**...**) i, a continuació, seleccioneu **Afegeix una característica de requisit nova** per afegir les aptituds necessàries per al desenvolupador.

    ![Ordre Afegeix una característica de requisit nova](media/Resource-Management-image11.png)

4. Al quadre de diàleg **Creació ràpida: característica de requisit** que apareix, al camp **Característica**, seleccioneu l'aptitud necessària. A continuació, al camp **Valor de qualificació**, seleccioneu el nivell de competència per a aquesta aptitud. Finalment, al camp **Requisit de recursos**, definiu el requisit dels recursos d'origen d'unitats organitzatives o fins i tot de recursos amb nom. Quan hagueu acabat, trieu **Desa**.

    ![Quadre de diàleg Creació ràpida: característica de requisit](media/Resource-Management-image12.png)

5. A la pàgina **Requisits de recursos**, seleccioneu **Reserva** per complir el requisit de recursos.

    ![Botó Reserva a la pàgina Requisits de recursos](media/Resource-Management-image13.png)

    També podeu seleccionar el recurs genèric a la quadrícula **Tots els membres de l'equip** i, a continuació, seleccionar **Reserva**.

    ![Botó Reserva per sobre de la quadrícula Tots els membres de l'equip](media/Resource-Management-image14.png)

    > [!NOTE]
    > En aquest exemple, hi ha 40 hores necessàries però no hores reservades reals, perquè els recursos genèrics no tenen reserves. A més, no hi ha cap hora assignada, perquè el recurs genèric s'ha afegit directament a l'equip. No s'ha afegit mitjançant l'assignació de tasques.

    A la pàgina **Auxiliar de planificació**, podeu filtrar els recursos disponibles mitjançant els requisits que s'especifiquen al requisit del recurs. Els recursos s'ordenen segons els paràmetres d'ordenació que s'especifiquen al Tauler de planificació.

    ![Pàgina Auxiliar de planificació](media/Resource-Management-image15.png)

    A continuació teniu alguns filtres que s'utilitzen sovint:

    - **Característiques amb una valoració**: filtreu per competències, certificacions i altres qualitats de recursos, a més d'avaluacions de competència.
    - **Funcions**: filtreu per les funcions per defecte que estan assignades a recursos que es poden reservar.
    - **Unitats organitzatives**: filtreu recursos que es poden reservar per les unitats organitzatives que tenen assignades.

6. Si no esteu satisfet amb els resultats de la cerca inicial de requisits, podeu canviar els criteris de filtratge. Expandiu la subfinestra **Filtra la visualització** a l'esquerra i, a continuació, seleccioneu **Cerca** per cercar recursos addicionals.

    ![Subfinestra Filtra la visualització](media/Resource-Management-image16.png)

7. Per canviar la manera com s'ordenen els resultats, seleccioneu **Ordena**.

    ![Ordre Ordena](media/Resource-Management-image17.png)

8. Seleccioneu recursos segons la demanda que s'especifica a l'exigència, tal com s'indicava a la part superior de la quadrícula. Podeu desactivar la selecció de cel·les a la quadrícula i deixar oberta la capacitat d'un recurs. Només es pot seleccionar un recurs cada vegada com a reservat.

9. Seleccioneu **Reserva** per reservar el recurs seleccionat i deixeu obert el Tauler de planificació, de manera que pugueu seleccionar recursos addicionals. Alternativament, seleccioneu **Reserva i surt** per reservar el recurs seleccionat i tanqueu el Tauler de planificació.

    ![Recurs per reservar](media/Resource-Management-image19.png)

    Rebreu una notificació sobre les hores reservades. Els indicadors de demanda mostren la quantitat de requisits de reserva satisfets i quants en queden. També podeu veure la quantitat de la capacitat del recurs seleccionat consumida. Seleccioneu **Expandeix** per veure més detalls sobre les reserves de recursos.

9. Torneu a la visualització **Tots els membres de l'equip**. A la quadrícula, heu de tenir en compte que el recurs genèric s'ha substituït pel recurs amb nom i que les 40 hores es mostren com a reservades per a aquest recurs.

    ![Quadrícula Tots els membres de l'equip actualitzada](media/Resource-Management-image20.png)

    > [!NOTE]
    > No es mostren les hores assignades, perquè estaven reservades directament a l'equip. No s'han reservat mitjançant l'assignació de tasques.

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a>Assignar recursos genèrics a tasques i generar requisits de recursos

Al PSA, podeu crear tasques i, a continuació, assignar-hi recursos genèrics. D'aquesta manera, la demanda de recursos es pot representar amb marcadors de posició mentre s'estima la planificació i els números financers. A continuació, podeu generar requisits de recursos per als recursos genèrics i complir-los.

1. A la pàgina **Projectes**, a la pestanya **Planificació**, seleccioneu **Afegeix** per crear una tasca.

    ![Tasca nova creada](media/Resource-Management-image21.png)

2. Al camp **Recursos**, seleccioneu el símbol **Selector de recursos**. El Selector de recursos apareix i mostra els membres de l'equip existents per al projecte.

    ![Selector de recursos](media/Resource-Management-image22.png)

3. Introduïu el nom del recurs genèric nou i, a continuació, seleccioneu **Crea**.

    ![Nom d'un recurs genèric nou introduït](media/Resource-Management-image23.png)

4. Al quadre de diàleg **Creació ràpida: membre de l'equip del projecte** que apareix, al camp **Funció**, seleccioneu la funció per al recurs genèric. Al camp **Unitat de recursos**, seleccioneu la unitat organitzativa del recurs genèric. A continuació, seleccioneu **Desa**.

    ![Quadre de diàleg Creació ràpida: membre de l'equip del projecte](media/Resource-Management-image24.png)

    El membre de l'equip genèric ara està assignat a la tasca.

    ![Membre de l'equip genèric assignat a la tasca](media/Resource-Management-image25.png)

    A la pestanya **Equip**, veureu el nou membre de l'equip genèric. Observeu que només té hores assignades. Aquestes hores són la suma de totes les tasques assignades al membre de l'equip genèric. El membre genèric de l'equip encara no té hores obligatòries o un requisit de recurs.

    ![Membre de l'equip genèric a la pestanya Equip](media/Resource-Management-image26.png)

5. Ara podeu assignar el membre de l'equip genèric a altres tasques mitjançant el Selector de recursos.

    ![Membre de l'equip genèric al Selector de recursos](media/Resource-Management-image27.png)

    Quan hàgiu acabat d'assignar el recurs genèric a les tasques, podeu generar un requisit de recurs per al recurs genèric.

5. A la pestanya **Equip**, seleccioneu el recurs genèric i, a continuació , seleccioneu **Genera un requisit**.

    ![Ordre Genera un requisit](media/Resource-Management-image28.png)

    Quan es genera el requisit, el membre de l'equip genèric tindrà hores obligatòries i un enllaç per al requeriment del recurs.

    ![Enllaç al requisit de recursos](media/Resource-Management-image29.png)

    Després de reservar un recurs amb nom, el recurs genèric se suprimeix de l'equip i se substitueix pel recurs amb nom.

    ![Recurs genèric substituït pel recurs amb nom](media/Resource-Management-image30.png)

    A la pestanya **Planificació**, les assignacions de recursos genèrics s'eliminen i se substitueixen pel recurs amb nom.

    ![Assignacions de recursos genèrics substituïdes pel recurs amb nom a la pestanya Planificació](media/Resource-Management-image31.png)

    > [!NOTE]
    > Aquest comportament només es produeix quan un recurs amb nom està completament reservat per al requisit de recursos genèrics. Quan un recurs amb nom reemplaça parcialment el requisit de recurs genèric o diversos recursos amb nom reemplacen els requisits de recurs genèric, el recurs genèric es manté assignat a la tasca.

    A la il·lustració següent, s'ha planificat una tasca de 80 hores per a una duració de cinc dies (16 hores al dia més de cinc dies) i s'assigna al recurs genèric amb el nom **Funcional**.

    ![Tasca de vuitanta hores en cinc dies assignada al recurs genèric Funcional](media/Resource-Management-image32.png)

    En generar el requisit, és de 80 hores al llarg de cinc dies.

    ![Requisit generat per a 80 hores en cinc dies](media/Resource-Management-image33.png)

    Com que els recursos disponibles treballen només vuit hores al dia, calen dos recursos per complir el requisit.

    ![Segon recurs](media/Resource-Management-image35.png)

    A la pestanya **Equip**, ara podeu veure que el recurs genèric no té hores necessàries, però les hores assignades encara es mostren juntament amb els dos recursos amb nom que formen el compliment.

    ![Dos recursos amb nom a la pestanya Equip](media/Resource-Management-image36.png)

    A la pestanya **Planificació**, el recurs genèric es manté assignat a la tasca.

    ![Recursos genèrics a la pestanya Planificació](media/Resource-Management-image37.png)

El PSA no assigna tots dos recursos a la tasca, perquè aquest comportament produiria una planificació menys predictible. En aquest senzill exemple, és fàcil dividir les hores de manera equitativa entre dos recursos. No obstant, en escenaris més complexos que impliquen diverses tasques i diversos recursos, el PSA hauria de fer suposicions sobre com hauria d'assignar les reserves que es reben per a diversos recursos en diverses tasques.

Per tant, en aquests escenaris, l'administrador del projecte s'encarrega d'analitzar les diverses reserves i d'assignar-les segons calgui. Per assignar les reserves, l'administrador del projecte assigna les tasques des dels recursos genèrics als recursos amb nom i, a continuació, utilitza la visualització **Conciliació** per assegurar-se que l'assignació funciona amb les reserves.

### <a name="edit-a-resource-requirement"></a>Editar un requisit de recursos

Després d'haver creat un requisit de recurs, pot ser que un administrador de projectes o un administrador de recursos vulguin editar els detalls per perfeccionar els criteris de cerca quan s'utilitza e Tauler de planificació. Per editar el requisit de recursos, seguiu aquests passos.

1. A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu l'enllaç a qualsevol requisit en un recurs genèric.
2. A la pàgina **Requisits de recursos** que es mostra, podeu actualitzar diversos atributs. A continuació trobareu alguns exemples:

    - Nom
    - Data d'inici
    - Data final
    - Duració
    - Tipus de recurs

A la pàgina **Requisits de recursos**, l'administrador del projecte o administrador de recursos també pot definir la següent informació:

- Aptituds
- Funcions
- Preferències de recursos
- Unitat organitzativa preferida

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a>Actualitzar les reserves de recursos un cop s'hagin reservat en un projecte

Després d'afegir un recurs genèric o amb nom a un equip de projecte, podeu canviar les reserves del recurs.

1. A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu un membre de l'equip i seleccioneu **Mantén les reserves**.

    ![Tauler de planificació obert per al membre de l'equip seleccionat](media/Resource-Management-image40.png)

    El Tauler de planificació apareix i mostra les reserves de membres de l'equip del projecte. Expandiu el registre del membre de l'equip per visualitzar les hores que s'han reservat a aquest projecte i altres projectes que estan consumint la capacitat del membre de l'equip.

2. Seleccioneu i arrossegueu la reserva per ampliar-la o reduir-la. Apareix un quadre de diàleg **Crea la reserva de recursos** que us permet ajustar la reserva.

    ![Quadre de diàleg Crea la reserva de recursos](media/Resource-Management-image41.png)

3. Feu clic amb el botó dret a la reserva. A continuació, podeu utilitzar el menú de drecera per completar les accions següents:

    - Canviar l'estat de la reserva.
    - Editar la reserva.
    - Substituir un recurs a l'equip del projecte.

### <a name="change-the-booking-status"></a>Canviar l'estat de la reserva

Podeu canviar qualsevol estat de reserva per defecte o personalitzat.

![Ordre Canviar l'estat](media/Resource-Management-image42.png)

El PSA inclou els estats següents:

- **Cancel·lat**: l'estat cancel·la la reserva d'un recurs i allibera la capacitat del recurs.
- **Reserva fixa**: l'estat consumeix la capacitat d'un recurs. Una reserva normalment té aquest estat quan obriu **Mantén les reserves** a la quadrícula **Tots els membres de l'equip** a la pàgina **Projectes**.
- **Reserva flexible**: l'estat afegeix un recurs a un equip però no consumeix la capacitat del recurs. Indica que el recurs s'ha reservat per a un treball potencial però té capacitat si és necessari en altres feines. A la visualització de la disponibilitat de recursos globals, les reserves flexibles tenen un estat diferent de les reserves fixes.
- **Proposat**: l'estat representa una proposta de l'administrador de recursos o l'administrador de projectes per a un recurs. Les propostes no consumeixen la capacitat d'un recurs i el recurs no s'afegeix a l'equip del projecte. Per reservar el recurs de l'equip, l'administrador del projecte ha d'acceptar la proposta.

### <a name="submit-resource-requests"></a>Enviar sol·licituds de recurs

Les sol·licituds de recursos s'utilitzen per dur a terme la demanda (requisit de recurs) que ha de complir un administrador de recursos. Per a un recurs genèric que ja està a l'equip, podeu enviar una sol·licitud de recurs directament. Una sol·licitud de recurs es pot complir de dues maneres:

- L'administrador de recursos compleix directament la sol·licitud. En aquest cas, el recurs genèric se substitueix per una reserva fixa que té un recurs amb nom.
- L'administrador de recursos proposa un recurs a l'administrador de projectes i el director del projecte aprova o rebutja el recurs proposat.

#### <a name="direct-fulfillment-of-resource-requests"></a>Compliment directe de sol·licituds de recursos

Quan es genera un requisit de recurs, un administrador de projecte pot enviar una sol·licitud de recurs per a un recurs genèric seleccionant el recurs i, a continuació, seleccionant **Envia la sol·licitud**.

![Botó Envia la sol·licitud](media/Resource-Management-image45.png)

Els comentaris sobre el recurs es poden proporcionar a l'administrador de recursos que està complint la sol·licitud. Després d'enviar la sol·licitud, el camp **Estat** per al membre de l'equip canvia a **Enviat**.

![Introduir comentaris opcionals](media/Resource-Management-image46.png)

Quan l'administrador de recursos compleix la sol·licitud, el membre de l'equip genèric se substitueix pel recurs amb nom a la quadrícula **Tots els membres de l'equip**.

![Membre de l'equip genèric substituït pel recurs amb nom a la quadrícula Tots els membres de l'equip](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a>Utilitzar una proposta de recurs per a sol·licituds de recursos

En lloc de fer la reserva directament d'un recurs d'una sol·licitud de recurs, un administrador de recursos pot proposar un recurs a l'administrador del projecte. Pot ser que un administrador de recursos utilitzi aquesta opció quan no hi hagi una coincidència exacta per als requisits. Quan un administrador de recursos proposa un recurs, l'administrador del projecte veu que el camp **Estat** del membre genèric de l'equip canvia a **Necessita revisió**.

![Estat d'un membre de l'equip genèric canviat a Necessita revisió](media/Resource-Management-image48.png)

Per visualitzar el recurs proposat juntament amb una visualització de l'efecte de la reserva de la proposta, feu doble clic al membre de l'equip que tingui l'estat **Necessita revisió**. A continuació, seleccioneu la pestanya **Recursos proposats**.

![Pestanya Recursos proposats](media/Resource-Management-image49.png)

Seleccioneu **Accepta totes les propostes** per acceptar tots els recursos proposats o **Rebutja totes les propostes** per rebutjar-les. Si accepteu els recursos proposats, es reserven de manera fixa al projecte com a membres de l'equip i reemplacen els recursos genèrics.

> [!NOTE]
> Heu d'acceptar o rebutjar tots els recursos proposats. No es poden acceptar ni rebutjar parcialment.

### <a name="substitute-a-resource-on-the-project-team"></a>Substituir un recurs a l'equip del projecte

De vegades, un administrador de projecte ha de substituir un membre de l'equip reservat en un projecte.

1. A la pàgina **Projectes**, a la pestanya **Equip**, seleccioneu el recurs que cal substituir i seleccioneu **Mantén les reserves**.
2. Expandiu el recurs per visualitzar els projectes als quals està assignat.

    ![Recurs ampliat per mostrar els projectes assignats](media/Resource-Management-image50.png)

3. Feu clic amb el botó dret del ratolí al projecte i seleccioneu **Substitueix el recurs**.
4. Si coneixeu el recurs que voleu substituir per al recurs actual, seleccioneu o escriviu-ne el nom i, a continuació, seleccioneu **Torna a assignar**.

    ![Especificar d'un recurs substitut](media/Resource-Management-image51.png)

    De manera alternativa, seguiu aquests passos per cercar un recurs:

    1. Seleccioneu **Cerca una substitució**.

        ![Cercar un recurs substitut](media/Resource-Management-image52.png)

        L'Auxiliar de planificacions retorna una llista de substituts disponibles. A l'Auxiliar de planificació, podeu continuar filtrant els recursos disponibles per trobar un substitut adient.

        ![Llista dels substituts disponibles](media/Resource-Management-image53.png)

    2. Per substituir el recurs, seleccioneu el recurs que voleu i, a continuació, seleccioneu **Substitueix**.

        ![Recurs substitut seleccionat](media/Resource-Management-image54.png)

    Les reserves i assignacions es substitueixen pel recurs nou.

    ![Reserves i assignacions substituïdes pel recurs nou](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a>Conciliar les reserves dels membres de l'equip i les assignacions

Per als membres de l'equip, les reserves i assignacions estan lleugerament vinculades. En altres paraules, els recursos poden tenir assignacions però no reserves, o poden tenir reserves però no assignacions. Idealment, les reserves i assignacions s'han d'alinear perquè els recursos tinguin capacitat confirmada de dur a terme l'assignació de tasques. No obstant, les reserves poden basar-se en la disponibilitat i els temps de treball podrien canviar a mesura que el projecte continua. Per tant, la lleugera vinculació de les reserves i les assignacions proporciona flexibilitat.

El PSA té una pestanya **Conciliació** que permet als administradors projectar les reserves dels membres de l'equip i els seus treballs per a equips de projectes.

![Pestanya Conciliació](media/Resource-Management-image56.png)

La pestanya **Conciliació** mostra les reserves i les assignacions al nivell de l'assignació de tasques individuals per a cada membre de l'equip. Mostra hores a les cel·les que representen períodes de temps de mesos a dies.

La pestanya també mostra un total de la xarxa global per al projecte, juntament amb una columna total.

Per a cada recurs, la pestanya calcula la diferència entre les reserves dels membres de l'equip i un valor consolidat de les assignacions de tasques del membre de l'equip. Idealment, aquesta diferència hauria de ser 0 (zero). En altres paraules, no hi hauria d'haver diferències entre les reserves i les assignacions. Les diferències es marquen amb color i un ombrejat per cridar l'atenció sobre dues condicions:

- **Manca de reserves**: una manca de reserves es produeix quan un recurs té més assignacions que reserves. Com que aquesta capacitat no s'ha reservat, un administrador de projecte pot voler corregir aquesta situació ampliant les reserves del recurs fins a cobrir el dèficit.
- **Excés de reserves**: un excés de reserves es produeix quan un recurs s'ha reservat al projecte però no s'ha assignat a tasques. Aquesta situació podria ser acceptable en els casos en què s'ha reservat el recurs al projecte abans d'haver produït una assignació de tasques. No obstant, en altres casos, el recurs no està planificat per assignar-se a tasques. En aquests casos, l'administrador del projecte hauria de considerar la cancel·lació de les reserves del recurs, de manera que la capacitat pugui utilitzar-se per a un altre projecte.

En alguns casos, quan visualitzeu temps en un nivell superior al nivell de dia (per exemple, al nivell de mes), pot ser que vegeu una diferència neta de zero per a un recurs (en altres paraules, reserves = assignacions). No obstant, si visualitzeu temps al nivell de la setmana, podeu veure que hi ha assignacions de zero hores i reserves de 40 hores a la primera setmana, però assignacions de 40 hores i reserves de zero hores a la segona setmana. En general, les reserves i assignacions es concilien, però difereixen d'una setmana a la següent.

Quan visualitzeu el temps en nivells superiors, les cel·les de la pestanya **Conciliació** tenen un indicador per informar-vos que hi ha diferències en nivells inferiors. En fer doble clic en una cel·la, podeu apropar el zoom per visualitzar la diferència. A continuació, podeu fer clic amb el botó dret per allunyar-vos. En seleccionar un recurs i utilitzar el control **Diferència següent** a la barra d'eines de la quadrícula, podeu anar a la diferència següent entre les reserves i les assignacions d'aquest recurs. A continuació, podeu utilitzar el control **Diferència anterior** per tornar enrere. També podeu desactivar l'indicador de diferències i el comportament de la navegació a **Configuració**.

![Indicador de diferències](media/Resource-Management-image57.png)

Si teniu assignacions de tasca per a un recurs però no hi ha cap reserva, a la pàgina **Projectes**, a la pestanya **Conciliació**, seleccioneu la manca de reserves i, a continuació, seleccioneu **Amplia la reserva**. El quadre de diàleg **Amplia la reserva** apareix i mostra la reserva necessària per fer front a la manca del recurs. També mostra les reserves existents del recurs en tots els projectes o altres entitats planificables. Si seleccioneu **D'acord** per crear la reserva del recurs, independentment de la disponibilitat del recurs, pot ser que hi hagi un excés de reserves.

![Quadre de diàleg Amplia la reserva](media/Resource-Management-image58.png)

L'administrador de projectes o administrador de recursos poden utilitzar el Tauler de planificació per administrar les situacions en què el recurs té un excés de reserves més enllà de la seva capacitat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]