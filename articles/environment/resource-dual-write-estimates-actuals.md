---
title: Integració d'estimacions i valors reals del projecte
description: Aquest article proporciona informació sobre la integració de doble escriptura de Project Operations per a estimacions i reals de projectes.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029068"
---
# <a name="project-estimates-and-actuals-integration"></a>Integració d'estimacions i valors reals del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article proporciona informació sobre la integració de doble escriptura de Project Operations per a estimacions i reals de projectes.

## <a name="project-estimates"></a>Estimacions del projecte

Les estimacions de mà d'obra, despeses i material del projecte es creen i es mantenen en Microsoft Dataverse aplicacions de finances i operacions amb finalitats comptables. Les operacions de creació, actualització i supressió no s'admeten a través de les aplicacions de finances i operacions.

Per crear estimacions cal tenir una configuració de comptabilitat vàlida per al projecte. Els projectes associats amb línies de contracte han de tenir un perfil de cost i ingressos del projecte vàlid definit a les regles del perfil de cost i d'ingressos del projecte. Per obtenir més informació, vegeu [Configuració de la comptabilitat per a projectes facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimacions laborals

Les estimacions laborals les crea l'administrador de projectes o l'administrador de recursos que també assigna un recurs genèric o amb nom a la tasca de projecte. Els registres d'assignació de recursos es poden revisar a la pestanya **Assignacions de recursos** de la pàgina **Detalls del projecte** al Dataverse. Registres d'assignació de recursos per Dataverse crear registres de previsió d'hores a les aplicacions de finances i operacions mitjançant **l'entitat d'integració project operations per a estimacions d'hores (msdyn\_ resourceassignments)**.

   ![Integració de les estimacions laborals.](./Media/DW4LaborEstimates.png)

L'escriptura doble sincronitza els registres d'assignació de recursos a la taula de còpia intermèdia (**ProjCDSEstimateHoursImport**) i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió d'hores (**ProjForecastEmpl**).

El comptable del projecte revisa els registres d'hores de previsió creats a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Tots els projectes** > **Planifiquen** > **les previsions** d'hora.

## <a name="expense-estimates"></a>Estimacions de despeses

L'administrador del projecte crea les estimacions de despeses a la pestanya **Estimacions de despeses** de la pàgina **Detalls del projecte** al Dataverse. Els registres de previsió de despeses s'emmagatzemen a l'entitat **Línia d'estimació** al Dataverse. Aquests registres d'estimació tenen classe de transacció, **despesa** i se sincronitzen amb els registres de previsió de despeses de les aplicacions de finances i operacions que utilitzen **l'entitat d'integració project operations per a estimacions de despeses (línies d'estimació de msdyn\_)**.

   ![Integració de les estimacions de despeses.](./Media/DW4ExpenseEstimates.png)

L'escriptura doble sincronitza els registres d'estimacions de despeses a la taula de còpia intermèdia **ProjCDSEstimateExpenseImport** i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió de despeses (**ProjForecastCost**). Les línies d'estimació emmagatzemen els registres d'estimacions de vendes i de cost per separat. La lògica empresarial de les aplicacions de finances i operacions emplena un únic registre de previsió de despeses utilitzant aquest detall a la taula de posada en escena.

El comptable del projecte pot revisar els registres de previsió de despeses a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Totes les previsions** > **de despeses del pla** > **de projectes**.

## <a name="material-estimates"></a>Estimacions de material

L'administrador del projecte crea les estimacions de material a la pestanya **Estimacions de material** de la pàgina **Detalls del projecte** al Dataverse. Els registres de previsió de material s'emmagatzemen a l'entitat **Línia d'estimació** al Dataverse. Aquests registres d'estimació tenen la classe de transacció, **Material** i se sincronitzen amb els registres de previsió d'elements de les aplicacions de finances i operacions mitjançant **la taula d'integració de projectes per a estimacions de materials (msdyn\_ estimatelines)**.

   ![Integració de les estimacions de material.](./Media/DW4MaterialEstimates.png)

L'escriptura doble sincronitza els registres d'estimacions de material a la taula de còpia intermèdia **ProjForecastSalesImpor** i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió d'elements (**ForecastSales**). Les línies d'estimació emmagatzemen els registres d'estimacions de vendes i de cost per separat. La lògica empresarial de les aplicacions de finances i operacions emplena un únic registre de previsió d'elements utilitzant aquest detall a la taula de posada en escena.

El comptable del projecte pot revisar els registres de previsió d'elements a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Totes les previsions** > **d'elements del pla** > **de projectes**.

## <a name="project-actuals"></a>Valors reals del projecte

Els valors reals del projecte es creen al Dataverse segons el temps, la despesa, el material i l'activitat de facturació. Tots els atributs d'operació d'aquestes transaccions, incloent-hi la quantitat, el preu de cost, el preu de venda i el projecte es capturen en aquesta entitat del Dataverse. Per obtenir més informació, vegeu [Valor reals](../actuals/actuals-overview.md). Els registres reals se sincronitzen amb les aplicacions de finances i operacions mitjançant el mapa **de taula de doble escriptura Project Operations integration reals (msdyn\_ reals)** per a la comptabilitat aigües avall.

   ![Integració de valors reals.](./Media/DW4Actuals.png)

L'assignació de taula dels **valors reals d'integració del Project Operations** sincronitza tots els registres de l'entitat **Valors reals** al Dataverse amb l'atribut **Omet la sincronització (només ús intern)** definida com a **Fals**. Aquest valor d'atribut es defineix automàticament al Dataverse en crear el registre. Els exemples en què aquest atribut està definit com a **Cert** són:

  - Valors reals de cost del projecte per a transaccions entre empreses. Per obtenir més informació, vegeu [Crear transaccions entre empreses](../project-accounting/create-intercompany-transactions.md). Aquests registres s'ometen perquè el sistema recrea el cost del projecte real a les aplicacions de finances i operacions quan es publica la factura del proveïdor entre empreses.
  - Registres de vendes no facturats negatius creats quan es confirma la factura proforma. Aquests registres s'ometen perquè el subledger del projecte a les aplicacions de finances i operacions no reverteix el registre de vendes no reduït a la facturació, sinó que canvia l'estat a facturat completament.

L'assignació de taules de doble escriptura sincronitza els registres reals amb la taula de còpia intermèdia, **ProjCDSActualsImport**. Aquests registres els processa el procés periòdic **Importa de la taula de còpia intermèdia** en crear línies de llibre diari d'integració del Project Operations i línies de proposta de factura del projecte. Per obtenir més informació, vegeu [Llibre diari d'integració al Project Operations](../project-accounting/project-operations-integration-journal.md).

El Dataverse també capta els enllaços entre les transaccions reals del projecte a l'entitat **Connexió de transaccions**. Per obtenir més informació, vegeu [Enllaçar els valors reals amb els registres originals](../actuals/linkingactuals.md). Els enllaços entre transaccions reals també se sincronitzen amb aplicacions de finances i operacions mitjançant el mapa de taula de doble escriptura, **Entitat d'integració per a relacions de transaccions del projecte (msdyn\_ transactionconnections)**. Aquests registres els fa servir el procés periòdic **Importa de la taula de còpia intermèdia** en crear línies de llibre diari d'integració del Project Operations i línies de proposta de factura del projecte.

La publicació d'un libre diari d'integració del Project Operations i d'una proposta de factura del projecte activa una actualització en els registres respectius a la taula de còpia intermèdia **ProjCDSActualsImport**. El sistema capta i registra els següents atributs de comptabilitat per a transaccions reals:

- Import de la divisa de comptabilitat
- Tipus de canvi
- Número de val
- Import de l'impost sobre les vendes

L'assignació de taules de **valors reals d'integracó del Project Operations** actualitza els registres de valors reals respectius al Dataverse amb aquesta informació.
