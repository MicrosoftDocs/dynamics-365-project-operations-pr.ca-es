---
title: Com assigno un recurs que es pot reservar a una tasca en l'aplicació web
description: Informació general de les maneres en què podeu assignar recursos que es poden reservar.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 0aaf7f69fa8ae081a74fbc4f18014686f625661c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578834"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Com assigno un recurs reservable a una a una tasca en l'aplicació web (v2.x de l'aplicació Project Service)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Hi ha dues maneres d'assignar un recurs a una tasca al Project Service. Podeu reservar un recurs com a membre de l'equip i després assignar-lo a una tasca. O bé, podeu crear un membre de l'equip genèric mitjançant l'assignació de rols en tasques, generar un equip i després, complir els requisits de seguretat amb un recurs amb nom.

Recordeu que si voleu assignar un recurs reservable a una tasca, el membre de l'equip de recursos reservables ha de tenir suficients reserves disponibles. L'estat de la reserva ha de ser tipus de confirmació Reserva fixa i Estat confirmat. Si no hi ha prou reserves per al recurs, el Project Service elimina l'assignació i mostra el missatge d'error següent:

*No es pot assignar el recurs a la tasca: els recursos següents no tenen prou hores reservades per al projecte*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Reservar un recurs com a membre de l'equip i després assignar-lo a una tasca

Amb aquest mètode, afegiu un recurs a l'equip del projecte i després assigneu tasques al recurs en la planificació del projecte. Aquesta és la manera de fer-ho:
1.  A la quadrícula de membres de l'equip, afegiu un nou membre de l'equip amb **Crea**.
2.  A la pantalla Creació ràpida d'un membre de l'equip, seleccioneu el nom del recurs que es pot reservar i establiu una funció.
3.  Seleccioneu les dates **Des de** i **Fins a**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de l'addició d'un membre a l'equip.](media/FAQ-Resources-to-Tasks2-1.png "Captura de pantalla de l'addició d'un membre a l'equip")
 
4.  Seleccioneu un dels següents mètodes d'assignació per reservar el recurs:
    - **Capacitat total**: reserva la capacitat total del recurs per a les dates especificades des de i fins a.
    - **Capacitat percentual**: reserva el recurs per a un percentatge de capacitat del recurs per a les dates especificades des de i fins a.
    - **Per hores distribuïdes uniformement**: reserva el recurs durant un nombre específic d'hores i les distribueix de manera uniforme per dia durant les dates especificades des de i fins a.
    - **Per hores amb la càrrega frontal**: reserva el recurs durant un nombre específic d'hores, carrega les hores per dia durant les dates especificades des de i fins a.

    No seleccioneu **Cap** perquè afegeix el recurs a l'equip, però no crea cap reserva que absorbeixi la capacitat del recurs.
5.  Seleccioneu **Desa**.

    Recordeu que les hores de la reserva han de ser suficients per cobrir les hores d'esforç i els intervals de dates de les tasques a les que assigneu aquest recurs. Si no estan alineades, no podreu assignar el recurs a la tasca.

6.  En l'estructura del desglossament del treball (WBS) per a la tasca, feu clic al menú desplegable de la cel·la de recursos. Aleshores: 

    1. Seleccioneu **Afegeix**.
    2. Seleccioneu el menú desplegable de **Recursos** i el membre de l'equip que heu afegit anteriorment.
    3. Seleccioneu **D'acord**. El membre de l'equip ara està assignat a la tasca.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de l'addició de recursos amb el WBS.](media/FAQ-Resources-to-Tasks2-2.png "Captura de pantalla de l'addició de recursos amb el WBS")
 
A la quadrícula de membres de l'equip, veureu el total d'hores assignades del recurs a l'apartat Hores assignades. Serà menor o igual que les hores reservades per al recurs. 

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de les hores assignades per a un recurs.](media/FAQ-Resources-to-Tasks2-3.png "Captura de pantalla de les hores assignades per a un recurs")
 
Si la tasca que està intentant assignar al recurs comença després de la data de finalització de les reserves de recursos, el recurs no apareixerà en el menú desplegable.

Recordeu que podeu assignar un recurs a més hores que les hores reservades si té alguna capacitat restant sense assignar. En aquest cas, el recurs només s'assignarà parcialment fins arribar a les seves reserves. Podeu veure aquestes hores de tasques restants sense assignar si afegiu la columna Hores sense personal a l'estructura del desglossament del treball.

Si els recursos s'assignen a les hores reservades (les hores reservades són iguals a les hores assignades), apareixerà el següent missatge d'error quan intenteu assignar-los més tasques:

*No es pot assignar el recurs a la tasca: els recursos següents no tenen prou hores reservades per al projecte.*

A més, el membre predeterminat de l'equip de l'administrador del projecte que s'agrega a l'equip quan es crea el projecte s'agrega sense reserves i no es pot assignar a cap tasca. No es mostraran al menú desplegable de recursos per a tasques.

Si voleu assignar aquest recurs, heu d'eliminar-les de l'equip i després tornar a afegir-les amb un mètode d'assignació diferent a Cap. La raó per la qual s'agreguen a l'equip quan es crea el projecte és perquè un projecte tingui almenys un aprovador de projectes per defecte.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Crear un membre de l'equip genèric a través de l'assignació de rols en les tasques

Aquest mètode assegura que els recursos tinguin suficients reserves per a les tasques. En primer lloc, heu de crear un contenidor o un recurs genèric que descrigui les característiques del recurs amb nom en el qual voleu treballar en les tasques mitjançant un equip després d'assignar rols a les tasques. Aquesta és la manera de fer-ho:

1. A l'estructura del desglossament del treball, seleccioneu una tasca.
2. Seleccioneu la icona desplegable **Rol assignat** a la cel·la del recurs.
3. Seleccioneu la llista desplegable **Funció** i la funció per al recurs genèric.
4. Seleccioneu **D'acord**.

    > [!div class="mx-imgBorder"] 
    > ![Captura de pantalla de l'ús del WBS per afegir un recurs.](media/FAQ-Resources-to-Tasks2-4.png "Captura de pantalla de l'ús del WBS per afegir un recurs")
 
Un cop hagueu completat l'assignació de funcions a les tasques al WBS, seleccioneu **Genera un equip de projecte**. El Project Service crea la quantitat mínima de membres genèrics de l'equip en funció dels rols, les unitats d'organització de recursos i el calendari del projecte amb les tasques assignades.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de la generació d'un equip de projecte.](media/FAQ-Resources-to-Tasks2-5.png "Captura de pantalla de la generació d'un equip de projecte")
 
A la quadrícula Membre de l'equip, veureu els recursos del tipus Recurs genèric amb el nom de la funció i la posició. Si calen dos recursos perquè una funció completi la feina, la funció Generar equip crea dos membres de l'equip i fa servir el nom de la posició per distingir-los.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de l'addició de dos recursos genèrics.](media/FAQ-Resources-to-Tasks2-6.png "Captura de pantalla de l'addició de dos recursos genèrics")
 
Podeu obrir el requisit del recurs de suport per al membre genèric de l'equip mitjançant l'enllaç que apareix a Requisit de recursos.

> [!div class="mx-imgBorder"] 
> ![Captura de pantalla de l'obertura d'un requisit de recurs de suport.](media/FAQ-Resources-to-Tasks2-7.png "Captura de pantalla de l'obertura d'un requisit de recurs de suport")

Seleccioneu **Reserva** per al recurs genèric i després podeu utilitzar el tauler de programació per buscar i reservar un recurs real. També podeu enviar el requisit de compliment per un administrador de recursos si seleccioneu **Envia sol·licitud**.

Quan el recurs genèric es compleix amb un recurs amb nom, el genèric s'elimina de l'equip i les assignacions de tasques s'assignen al recurs amb nom que va complir els requisits de recursos del recurs genèric.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
