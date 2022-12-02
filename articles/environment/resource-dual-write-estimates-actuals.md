---
title: Integració d'estimacions i valors reals del projecte
description: Aquest article proporciona informació sobre la integració de doble escriptura del Project Operations per a les estimacions i els valors reals del projecte.
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

Aquest article proporciona informació sobre la integració de doble escriptura del Project Operations per a les estimacions i els valors reals del projecte.

## <a name="project-estimates"></a>Estimacions del projecte

Les estimacions laborals, de despeses i de materials del projecte es creen i es mantenen al Microsoft Dataverse i se sincronitzen amb les aplicacions de finances i operacions amb finalitats de comptabilitat. Les operacions de creació, actualització i supressió no estan admeses a través de les aplicacions de finances i operacions.

Per crear estimacions cal tenir una configuració de comptabilitat vàlida per al projecte. Els projectes associats amb línies de contracte han de tenir un perfil de cost i ingressos del projecte vàlid definit a les regles del perfil de cost i d'ingressos del projecte. Per obtenir més informació, vegeu [Configuració de la comptabilitat per a projectes facturables](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Estimacions laborals

Les estimacions laborals les crea l'administrador de projectes o l'administrador de recursos que també assigna un recurs genèric o amb nom a la tasca de projecte. Els registres d'assignació de recursos es poden revisar a la pestanya **Assignacions de recursos** de la pàgina **Detalls del projecte** al Dataverse. Els registres d'assignació de recursos del Dataverse creen registres de previsió d'hora a les aplicacions de finances i operacions  utilitzant l'**entitat d'integració del Project Operations per a les estimacions d'hores (msdyn\_resourceassignments)**.

   ![Integració de les estimacions laborals.](./Media/DW4LaborEstimates.png)

L'escriptura doble sincronitza els registres d'assignació de recursos a la taula de còpia intermèdia (**ProjCDSEstimateHoursImport**) i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió d'hores (**ProjForecastEmpl**).

El comptable del projecte revisa els registres d'hora de previsió creats a les aplicacions de finances i operacions anant a **Gestió i comptabilitat de projectes** > **Tots els projectes** > **Planifica** > **Previsions d'hora**.

## <a name="expense-estimates"></a>Estimacions de despeses

L'administrador del projecte crea les estimacions de despeses a la pestanya **Estimacions de despeses** de la pàgina **Detalls del projecte** al Dataverse. Els registres de previsió de despeses s'emmagatzemen a l'entitat **Línia d'estimació** al Dataverse. La classe de transacció d'aquests registres d'estimacions és **Despesa** i se sincronitzen amb els registres de previsió de despeses a les aplicacions de finances i operacions que utilitzen l'**entitat d'integració del Project Operations per a les estimacions de despeses (msdyn\_estimatelines)**.

   ![Integració de les estimacions de despeses.](./Media/DW4ExpenseEstimates.png)

L'escriptura doble sincronitza els registres d'estimacions de despeses a la taula de còpia intermèdia **ProjCDSEstimateExpenseImport** i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió de despeses (**ProjForecastCost**). Les línies d'estimació emmagatzemen els registres d'estimacions de vendes i de cost per separat. La lògica empresarial de les aplicacions de finances i operacions emplena un únic registre de previsió de despeses amb aquest detall a la taula de còpia intermèdia.

El comptable del projecte pot revisar els registres de previsió de despeses creats a les aplicacions de finances i operacions anant a **Gestió i comptabilitat de projectes** > **Tots els projectes** > **Planifica** > **Previsions de despeses**.

## <a name="material-estimates"></a>Estimacions de material

L'administrador del projecte crea les estimacions de material a la pestanya **Estimacions de material** de la pàgina **Detalls del projecte** al Dataverse. Els registres de previsió de material s'emmagatzemen a l'entitat **Línia d'estimació** al Dataverse. La classe de transacció d'aquests registres d'estimacions és **Material** i se sincronitzen amb els registres de previsió d'elements a les aplicacions de finances i operacions que utilitzen la **Taula d'integració del projecte per a les estimacions de material (msdyn\_estimatelines)**.

   ![Integració de les estimacions de material.](./Media/DW4MaterialEstimates.png)

L'escriptura doble sincronitza els registres d'estimacions de material a la taula de còpia intermèdia **ProjForecastSalesImpor** i, a continuació, utilitza la lògica empresarial per crear i actualitzar registres de previsió d'elements (**ForecastSales**). Les línies d'estimació emmagatzemen els registres d'estimacions de vendes i de cost per separat. La lògica empresarial de les aplicacions de finances i operacions emplena un únic registre de previsió d'element amb aquest detall a la taula de còpia intermèdia.

El comptable del projecte pot revisar els registres de previsió d'elements creats a les aplicacions de finances i operacions anant a **Gestió i comptabilitat de projectes** > **Tots els projectes** > **Planifica** > **Previsions d'elements**.

## <a name="project-actuals"></a>Valors reals del projecte

Els valors reals del projecte es creen al Dataverse segons el temps, la despesa, el material i l'activitat de facturació. Tots els atributs d'operació d'aquestes transaccions, incloent-hi la quantitat, el preu de cost, el preu de venda i el projecte es capturen en aquesta entitat del Dataverse. Per obtenir més informació, vegeu [Valor reals](../actuals/actuals-overview.md). Els registres de valors reals se sincronitzen amb les aplicacions de finances i operacions amb l'assignació de taules de doble escriptura **Valors reals d'integració del Project Operations (msdyn\_actuals)** de comptabilitat descendent.

   ![Integració de valors reals.](./Media/DW4Actuals.png)

L'assignació de taula dels **valors reals d'integració del Project Operations** sincronitza tots els registres de l'entitat **Valors reals** al Dataverse amb l'atribut **Omet la sincronització (només ús intern)** definida com a **Fals**. Aquest valor d'atribut es defineix automàticament al Dataverse en crear el registre. Els exemples en què aquest atribut està definit com a **Cert** són:

  - Valors reals de cost del projecte per a transaccions entre empreses. Per obtenir més informació, vegeu [Crear transaccions entre empreses](../project-accounting/create-intercompany-transactions.md). Aquests registres s'ometen perquè el sistema torna a crear el cost del projecte real a les aplicacions de finances i operacions quan la factura del proveïdor entre empreses es publica.
  - Registres de vendes no facturats negatius creats quan es confirma la factura proforma. Aquests registres s'ometen perquè el subcompte de projectes de les aplicacions de finances i operacions no inverteix el registre de vendes no facturades a la factura, sinó que canvia l'estat per totalment facturat.

L'assignació de taules de doble escriptura sincronitza els registres reals amb la taula de còpia intermèdia, **ProjCDSActualsImport**. Aquests registres els processa el procés periòdic **Importa de la taula de còpia intermèdia** en crear línies de llibre diari d'integració del Project Operations i línies de proposta de factura del projecte. Per obtenir més informació, vegeu [Llibre diari d'integració al Project Operations](../project-accounting/project-operations-integration-journal.md).

El Dataverse també capta els enllaços entre les transaccions reals del projecte a l'entitat **Connexió de transaccions**. Per obtenir més informació, vegeu [Enllaçar els valors reals amb els registres originals](../actuals/linkingactuals.md). Els enllaços entre transaccions reals també se sincronitzen amb les aplicacions de finances i operacions mitjançant l'assignació de taules de doble escriptura **Entitat d'integració per a relacions de transacció de projecte (msdyn\_transactionconnections)**. Aquests registres els fa servir el procés periòdic **Importa de la taula de còpia intermèdia** en crear línies de llibre diari d'integració del Project Operations i línies de proposta de factura del projecte.

La publicació d'un libre diari d'integració del Project Operations i d'una proposta de factura del projecte activa una actualització en els registres respectius a la taula de còpia intermèdia **ProjCDSActualsImport**. El sistema capta i registra els següents atributs de comptabilitat per a transaccions reals:

- Import de la divisa de comptabilitat
- Tipus de canvi
- Número de val
- Import de l'impost sobre les vendes

L'assignació de taules de **valors reals d'integracó del Project Operations** actualitza els registres de valors reals respectius al Dataverse amb aquesta informació.
