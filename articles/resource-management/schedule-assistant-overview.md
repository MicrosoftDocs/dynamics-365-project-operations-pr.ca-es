---
title: Informació general sobre l'ajudant de planificació
description: En aquest tema es proporciona informació sobre com treballar amb l'ajudant de planificació per reservar recursos.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279216"
---
# <a name="schedule-assistant-overview"></a>Informació general sobre l'ajudant de planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

L'auxiliar de planificació s'utilitza per reservar recursos en funció dels requisits definits per l'administrador del projecte. L'auxiliar de planificació es basa en els paràmetres proporcionats al requisit de recurs per cercar el recurs. L'auxiliar de planificació recomana recursos que coincideixen amb els requisits pertinents, com ara franges temporals o coneixements necessaris.

Un cop identificats els recursos adients, l'administrador de recursos o del projecte poden reservar el recurs al treball.

## <a name="prerequisites"></a>Requisits previs

L'auxiliar de planificació forma part de la solució Universal Resource Scheduling. Aquesta solució s'inclou i s'instal·la amb el Dynamics 365 Project Operations, el Dynamics 365 Field Service i el Dynamics 365 Customer Service.

## <a name="matching-requirements-and-resources"></a>Assignació de requisits i recursos

Un requisit de recurs generat es basa en detalls com:

-   Característiques
-   Funcions
-   Unitats de negoci
-   Preferències de recursos
-   Contorns d'esforç
-   Fus horari

L'auxiliar de planificació utilitza aquests detalls per filtrar els recursos.

## <a name="launch-the-schedule-assistant"></a>Iniciar l'auxiliar de planificació

Hi ha dues maneres d'iniciar l'auxiliar de planificació. Si utilitzeu el mode híbrid, a la quadrícula de membres de l'equip podeu seleccionar qualsevol membre de l'equip amb un requisit de recurs no complert i, a continuació, seleccionar **Reserva**. Si utilitzeu el mode central, l'administrador de recursos cerca i selecciona el recurs.

## <a name="schedule-assistant-filters"></a>Filtres de l'Auxiliar de planificació

Després d'executar l'auxiliar de planificació, els detalls del requisit del recurs es mostren com a valors filtrats a la subfinestra esquerra. L'administrador de recursos o l'administrador de projectes poden afinar els resultats ajustant els filtres per complir les necessitats de planificació.

A la subfinestra de filtratge es mostren les opcions relacionades amb el treball, incloent-hi:

-   Inici i acabament del treball
-   Característiques
-   Funcions
-   Unitats organitzatives
-   Empresa de dotació de recursos
-   Tipus de recursos
-   Recursos preferits


[!INCLUDE[footer-include](../includes/footer-banner.md)]