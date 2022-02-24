---
title: Crear un equip de projecte
description: Aquest tema proporciona informació sobre com crear i administrar els equips de projectes.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270846"
---
# <a name="create-a-project-team"></a>Creació d'un equip de projecte

[!include [banner](../includes/banner.md)]

Per utilitzar les funcions que s'han configurat prèviament en un projecte, un administrador de projectes ha d'associar les funcions amb el projecte. Es poden assignar diverses funcions per a un projecte. Per evitar confusions, aquestes funcions s'etiqueten automàticament a la reserva. Per exemple, si l'administrador de projectes requereix tres enginyers de programari, es generen automàticament tres funcions Enginyer de programari que tenen les etiquetes **Enginyer de programari 1**, **Enginyer de programari 2** i **Enginyer de programari 3**. Si abans s'havien definit característiques de funció per a la funció, s'apliquen com a filtre durant les cerques d'un recurs. Les característiques addicionals es poden afegir com a necessàries per refinar la cerca.

La configuració de la visualització també es pot personalitzar per oferir una millor visualització de la disponibilitat dels recursos. Hi ha opcions per mostrar la disponibilitat horària, diària, setmanal, mensual, trimestral i anual. També hi ha una opció per mostrar la capacitat disponible i restant dels recursos. Aquesta opció és útil per a l'administració de temps, quan estimeu el temps disponible per a activitats o la disponibilitat dels recursos.

L'administrador del projecte pot seleccionar una funció a la pàgina i, a continuació, si hi ha un recurs disponible que s'ajusta al requisit, seleccionar la reserva d'un recurs per emplenar la funció. Heu de tenir en compte que els recursos no s'hauran de reservar en aquest moment a la fase de planificació. Quan creeu una WBS, podeu substituir les funcions per recursos de personal per al projecte. Si les funcions se substitueixen amb els recursos de personal a la WBS, la configuració del recurs actualitza automàticament la llista i la planificació de l'equip del projecte.

[![Llista de l'equip del projecte que inclou les funcions i els recursos reals](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

L'administrador de projectes té diverses opcions per reservar un recurs per a un projecte, com ara **Capacitat restant**, **Capacitat completa**, **Percentatge de capacitat** i **Especifica les hores**. Aquestes opcions de reserva es poden cancel·lar en qualsevol moment si canvien les assignacions de recursos. S'admeten dos tipus de reserves:

- **Reserva fixa**: la reserva de recursos s'ha aprovat i confirmat per treballar en la implicació durant la duració especificada.
- **Reserva flexible**: la reserva de recursos s'ha definit provisionalment per treballar en la implicació durant la duració especificada.

El següent procés explica com crear un equip de projecte.

## <a name="create-a-project-team"></a>Creació d'un equip de projecte

1. A la pàgina de llista **Tots els projectes**, seleccioneu un projecte i, a continuació, seleccioneu **Edita**.
2. A la pestanya **Equip del projecte i planificació**, al camp **Data de finalització de la planificació**, introduïu la data d'inici de la planificació més un mes. Per exemple, si la data d'inici de la planificació és el 24 de juny de 2017 (24/06/2017), introduïu **24/07/2017**.
3. Seleccioneu **Afegeix**.
4. A la subfinestra **Afegeix funcions al projecte**, al camp **Funció**, seleccioneu **Administrador de projectes sènior**.
5. Seleccioneu **Competències necessàries**.
6. A la pàgina **Trieu les característiques**, les característiques que prèviament heu definit per a la funció Administrador de projectes sènior se seleccionen per defecte. Seleccioneu **D'acord**.
7. A la pàgina **Afegiu funcions al projecte**, al camp **Nombre de recursos**, introduïu **1**.
8. Al camp **Recurs**, la cerca mostra tots els recursos que tenen les competències necessàries. Seleccioneu **Daniel Goldschmidt** i, a continuació, seleccioneu **Crea**.
9. A la pàgina **Projecte**, seleccioneu **Afegeix**.
10. A la subfinestra **Afegeix funcions al projecte**, al camp **Funció**, seleccioneu **Membre de l'equip**. En el camp **Nombre de recursos**, introduïu **5**.
11. Seleccioneu **Crea**.
12. A la pàgina **Projectes**, seleccioneu **Completa el recurs**.

## <a name="monitor-project-teams"></a>Supervisar els equips del projecte
1. A la pàgina **Tots els projectes**, seleccioneu l'enllaç **Identificador del projecte** per al projecte **Fase 2 d'actualització d'XYZ**.
2. Al FastTab **Equip del projecte i planificació**, comproveu que els recursos del projecte que es mostren siguin correctes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]