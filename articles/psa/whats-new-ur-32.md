---
title: Novetats o canvis de la versió d'actualització 32 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 32.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129654"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Novetats o canvis de la versió d'actualització 32 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Ens complau anunciar l'última actualització de l'aplicació Microsoft Dynamics 365 Project Service Automation. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. És compatible amb el Dynamics 365 9.x. Per actualitzar aquesta versió, visiteu la pàgina de solucions en línia del Centre d'administració del Dynamics 365 i instal·leu l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 32. Aquesta versió té el número de compilació V3.10.53.108 i està disponible de manera general a través d'una actualització d'autoservei el juny de 2021.

## <a name="update-release-32"></a>Versió d'actualització 32

### <a name="bug-fixes"></a>Correccions d'errors

#### <a name="general"></a>General

- Quan es produeix un error en una actualització principal, només s'han de bloquejar els punts d'entrada principals de l'aplicació per assegurar-vos que les entitats compartides encara siguin accessibles.

#### <a name="time-and-expense"></a>Temps i despesa

S'han corregit els problemes següents:

- **TimeEntriesImportFromResourceAssignment** no conserva les hores d'inici i d'acabament de les porcions de contorn d'assignació de recursos.
- Quan seleccioneu **Obre l'entrada** a la quadrícula **Entrada de temps**, és possible que no pugueu seleccionar altres formularis.
- Mentre importeu assignacions a entrades de temps, la consulta de codi de client podria generar una adreça URL llarga que generi un error a la consulta.
- A la quadrícula **Entrada de temps**, després de suprimir un valor d'una cel·la, el focus no es queda a la quadrícula.
- El botó **Rebutja** s'ha eliminat de la visualització **Aprovacions de processament** per a les aprovacions moderns.
- L'estabilitat i el rendiment de l'aprovació massiva d'entrades de temps es veuen afectades per bloquejos i un error en gestionar correctament les personalitzacions relacionades amb l'entitat **Entrada de temps**.

#### <a name="project-planning"></a>Planificació del projecte

- Una excepció de referència nul·la es genera quan actualitzeu un projecte que té un valor nul al camp **Unitat contractant**.
- **Actualitza els totals del projecte** calcula incorrectament el cost restant i les vendes restants en un projecte.
- Els càlculs de preus redundants afecten el rendiment relacionat amb les actualitzacions dels contorns d'assignació de recursos.

#### <a name="resource-management"></a>Administració de recursos

S'ha corregit el problema següent:

- Quan la capacitat de calendari d'un recurs que es pot reservar és més d'1, el Project Service Automation reconeix incorrectament la capacitat com a 0 (zero). Per tant, es produeix un bucle infinit a la visualització de planificació.

#### <a name="sales"></a>Vendes

S'han corregit els problemes següents:

- Quan es crea una línia del llibre diari que té un tipus de transacció personalitzat, es produeix l'excepció de referència nul·la següent: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- No afegiu funcions i categories desactivades abans de copiar una oferta a funcions i categories imputables d'una oferta nova copiada.
- La data i la data de compte del document no estan alineades amb la data d'inici que es proporciona en un detall de la línia de factura que es crea directament en un esborrany de factura.
- Es generen excepcions de referència nul·la en escenaris relacionats amb la inactivació de funcions i categories abans de copiar una oferta.
- L'acció **Actualitza els preus** a la pàgina **Projectes** no actualitza les estimacions de despeses ni les estimacions de materials.
