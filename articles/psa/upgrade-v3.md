---
title: Consideracions d'actualització - Versió 2.x o 1.x del Microsoft Dynamics 365 Project Service Automation a la versió 3
description: En aquest tema es proporciona informació sobre les consideracions que heu de fer en actualitzar des de la versió 2.x o 1.x a la versió 3 del Project Service Automation.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 19d6d312c7cedd2d7b9b5649452b85dd24fae761
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072292"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Consideracions d'actualització - Versió 2.x o 1.x del PSA a la versió 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation i Field Service
Tant el Dynamics 365 Project Service Automation com el Dynamics 365 Field Service utilitzen la solució Universal Resource Scheduling (URS) per a la planificació de recursos. Si teniu tant el Project Service Automation com el Field Service a la vostra instància, heu de planificar l'actualització de les dues solucions a l'última versió (versió 3.x per al Project Service Automation, versió 8.x per al Field Service). L'actualització del Project Service Automation o el Field Service instal·larà la versió més recent del URS, la qual cosa vol dir que el comportament incoherent és possible si les solucions del Project Service Automation i del Field Service en la mateixa instància no es poden actualitzar a la versió més recent.

## <a name="resource-assignments"></a>Assignacions de recursos
A la versió 2 i la versió 1 del Project Service Automation, les assignacions de tasques es desaven com a tasques secundàries (també anomenades tasques de línia) a l'entitat **Tasca** i indirectament relacionades amb l'entitat **Assignació de recursos**. La tasca de línia estava visible a la finestra emergent de l'assignació a l'estructura del desglossament del treball (WBS).

![Tasques de línia al WBS a la versió 2 i a la versió 1 del Project Service Automation](media/upgrade-line-task-01.png)

A la versió 3 del Project Service Automation, l'esquema subjacent d'assignar recursos que es poden reservar a tasques ha canviat. La tasca de línia és obsoleta i hi ha una relació directa 1:1 entre la tasca a l'entitat **Tasca** i el membre de l 'equip a l'entitat **Assignació de recursos**. Les tasques assignades a un membre d'equip del projecte ara s'emmagatzemen directament a l'entitat Assignació de recursos.  

Aquests canvis afecten l'actualització de tots els projectes existents que tenen assignacions de recursos per a recursos que es poden reservar amb nom i recursos genèrics en un equip del projecte. En aquest tema es proporcionen les consideracions que haureu de tenir en compte per als projectes en què actualitzeu a la versió 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tasques assignades a recursos amb nom
Amb l'entitat de la tasca subjacent, les tasques de la versió 2 i la versió 1 permetien que els membres de l'equip representessin una funció que no fos la seva funció definida per defecte. Per exemple, la Jana Jorba, que per defecte està assignada a la funció d'administradora de programa, podria assignar-se a una tasca amb la funció de desenvolupadora. A la versió 3, la funció d'un membre de l'equip amb nom és sempre el valor per defecte, per la qual cosa qualsevol tasca a la qual s'assigni la Jana Jorba utilitza la seva funció per defecte d'administradora de programes.

Si heu assignat un recurs a una tasca fora de la seva funció per defecte a la versió 2 i a la versió 1, en actualitzar, el recurs amb nom s'assignarà la funció per defecte per a totes les assignacions de tasques, independentment de l'assignació de funcions a la versió 2. Això donarà com a resultat diferències en les estimacions calculades des de la versió 2 o la versió 1 a la versió 3 perquè les estimacions es calculen en funció de la funció del recurs i no de l'assignació de tasques de línia. Per exemple, a la versió 2, s'assignen dues tasques a la Cèlia Canal. La funció a la tasca de línia per a la tasca 1 és desenvolupador i per a la tasca 2, administrador de programes. La Cèlia Canal té la funció per defecte d'administradora de programes.

![Diverses funcions assignades a un recurs](media/upgrade-multiple-roles-02.png)

Com que les funcions de desenvolupador i administrador de programes són diferents, les estimacions de cost i vendes són les següents:

![Estimacions de costos per a funcions de recursos](media/upggrade-cost-estimates-03.png)

![Estimacions de vendes per a funcions de recursos](media/upgrade-sales-estimates-04.png)

Quan actualitzeu a la versió 3, les tasques de línia se substitueixen per assignacions de recursos a la tasca del membre de l'equip de recursos que es pot reservar. L'assignació utilitzarà la funció per defecte del recurs que es pot reservar. En el gràfic, la Cèlia Canal, que té una funció d'administradora de programes, és el recurs.

![Assignacions de recursos](media/resource-assignment-v2-05.png)

Com que les estimacions es basen en la funció per defecte del recurs, les estimacions de vendes i de costos poden canviar. Heu de tenir en compte que al gràfic següent ja no veureu la funció **Desenvolupador** ja que la funció ara s'agafa de la funció per defecte del recurs que es pot reservar.

![Estimacions de costos per a funcions per defecte](media/resource-assignment-cost-estimate-06.png)
![Estimació de vendes per a funcions per defecte](media/resource-assignment-sales-estimate-07.png)

Quan s'hagi completat l'actualització, podeu editar la funció del membre d'un equip perquè sigui diferent de l'assignada per defecte. No obstant, si canvieu la funció dels membres de l'equip, es canviarà en totes les tasques assignades perquè els membres de l'equip ja no es podran assignar funcions múltiples a la versió 3.

![Actualitzar una funció de recurs](media/resource-role-assignment-08.png)

Això també és vàlid per a les tasques de línia assignades a recursos amb nom quan canvieu la unitat de l'organització del recurs de la per defecte a una altra unitat d'organització. Quan l'actualització a la versió 3 s'hagi completat, l'assignació utilitzarà la unitat organitzativa per defecte del recurs en comptes de l'establerta a la tasca de línia.

### <a name="tasks-assigned-to-generic-resources"></a>Tasques assignades a recursos genèrics
A la versió 2 i a la versió 1, podeu definir la funció i la unitat organitzativa en una tasca i, a continuació, utilitzar la característica **Genera un equip** per generar recursos genèrics basats en els atributs definits a la tasca. A la versió 3, creeu els membres de l'equip genèric amb la funció i unitat organitzativa i, a continuació, assigneu els membres de l'equip a tasques.

A la versió 2 i la versió 1, els projectes amb recursos genèrics poden estar en dos estats o una combinació de tots dos al nivell de la tasca. Per exemple, podeu tenir els escenaris següents:

- Tasques amb funcions i unitats organitzatives definides, però no s'ha generat cap assignació de recursos afiliats.
- Tasques amb assignacions de recursos dels membres de l'equip genèric que s'han assignat creant recursos genèrics mitjançant la característica **Genera un equip**.

Abans de començar l'actualització, us recomanem que torneu a generar l'equip de cada projecte que tingui les tasques assignades als recursos genèrics o per al qual encara no s'ha executat el procés de generació de l'equip.

Per a les tasques assignades a membres de l'equip genèric que es van generar amb **Genera un equip** , l'actualització deixarà el recurs genèric a l'equip i deixarà l'assignació al membre de l'equip genèric. Us recomanem que genereu el requisit de recurs per al membre de l'equip genèric després de l'actualització, però abans de reservar o enviar una sol·licitud de recurs. Això conservarà qualsevol assignació d'unitat organitzativa als membres de l'equip genèric que són diferents a la unitat organitzativa de contractació del projecte.

Per exemple, en el projecte Projecte Z, la unitat organitzativa de contractació és Contoso US. En el pla del projecte, a les tasques de prova dins de la fase d'implementació s'ha assignat el rol de consultor tècnic i la unitat organitzativa assignada és Contoso India.

![Assignació d'organització de la fase d'implementació](media/org-unit-assignment-09.png)

Després de la fase d'implementació, la tasca de prova d'integració s'assigna a la funció d'assessor tècnic, però l'organització es defineix com a Contoso US.  

![Assignació d'organització de tasca de prova d'integració](media/org-unit-generate-team-10.png)

Quan genereu un equip per al projecte, es crearan dos membres de l'equip genèrics a causa de les diferents unitats organitzatives a les tasques. L'assessor tècnic 1 s'assignarà a les tasques de Contoso India i l'assessor tècnic 2 tindrà les tasques de Contoso US.  

![Membres de l'equip genèrics generats](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> A la versió 2 i la versió 1 del Project Service Automation, el membre de l'equip no té la unitat organitzativa, que es manté a la línia de tasques.

![Tasques de línia de la versió 2 i la versió 1 del Project Service Automation](media/line-tasks-12.png)

Podeu veure la unitat d'organització a la visualització d'estimacions. 

![Estimacions d'unitat organitzativa](media/org-unit-estimates-view-13.png)
 
Quan l'actualització s'hagi completat, la unitat de l'organització a la tasca de línia que correspon al membre de l'equip genèric se suma al membre de l'equip genèric i la tasca de línia se suprimeix. Per això, us recomanem que abans d'actualitzar, genereu o torneu a generar l'equip en cada projecte que conté recursos genèrics.

Per a les tasques assignades a una funció amb una unitat organitzativa que difereix de la unitat organitzativa del projecte de contractació, i que no s'ha generat un equip, l'actualització crearà un membre genèric de l'equip per a la funció, però utilitzarà la unitat de contractació del projecte per al membre de l'equip de la unitat organitzativa. Tornant a l'exemple amb el Projecte Z, això vol dir que a la unitat organitzativa de contractació Contoso US i a les tasques de prova del pla del projecte dins de la fase d'implementació s'ha assignat el rol consultor tècnic amb la unitat organitzativa assignada a Contoso India. La tasca de prova d'integració que es completa després de la fase d'implementació s'ha assignat a la funció d'assessor tècnic. La unitat organitzativa és Contoso US i no s'ha generat un equip. L'actualització crearà un membre genèric de l'equip, un consultor tècnic que té les hores assignades de les tres tasques i una unitat organitzativa de Contoso US, la unitat organitzativa de contractació del projecte.   
 
Canviar el valor per defecte de les diferents unitats organitzatives de recursos en els membres de l'equip no generats és la raó per la que recomanem que genereu o torneu a generar l'equip en cada projecte que conté recursos genèrics abans de l'actualització, de manera que les assignacions d'unitats organitzatives no es perdin.

