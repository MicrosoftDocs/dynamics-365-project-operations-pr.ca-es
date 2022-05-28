---
title: Configuració del Project Operations i integració de les dades de configuració
description: Aquest tema proporciona informació sobre la configuració d'assignacions de doble escriptura del Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586884"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configuració del Project Operations i integració de les dades de configuració

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema proporciona informació sobre la integració de doble escriptura del Project Operations per a les entitats de configuració.

## <a name="project-contracts-contract-lines-and-projects"></a>Contractes del projecte, línies de contracte i projectes

Els contractes de projectes, les línies de contracte i els projectes es creen Dataverse i se sincronitzen amb les aplicacions financeres i d'operacions per obtenir una comptabilitat addicional. Els registres d'aquestes entitats només es poden crear i suprimir al Dataverse. No obstant això, els atributs comptables, com ara els impagaments del grup d'impostos sobre les vendes i les dimensions financeres, es poden afegir a aquests registres a les aplicacions Finances i Operacions.

  ![Conceptes d'integració de contractes de projecte.](./media/1ProjectContract.jpg)

Es fa un seguiment dels clients potencials, oportunitats i ofertes de Dataverse l'activitat de vendes i no se sincronitzen amb les aplicacions Financeres i operacions perquè no hi ha cap comptabilitat descendent associada amb aquesta activitat.

La funcionalitat del contracte del projecte a Dataverse crea un registre de contracte de projecte a les aplicacions Finances i Operacions mitjançant el mapa de la taula de capçaleres de **contracte del projecte (salesorders).** En desar un contracte de projecte al Dataverse, també s'inicia la creació d'un registre d'entitat de client de contracte de projecte. Aquest registre se sincronitza amb les aplicacions de finances i operacions mitjançant l'assignació de taula de la **font de finançament del projecte (msdyn\_ projectcontractssplitbillingrules).** Aquesta assignació també sincronitza les addicions, les actualitzacions i les supressions de clients del contracte del projecte. Els percentatges de facturació dividits entre els clients del contracte del projecte només Dataverse es dominen i no se sincronitzen amb les aplicacions Financeres i Operacions.

Després de crear un contracte de projecte el Dataverse, el comptable del projecte pot actualitzar els atributs comptables d'aquest contracte de projecte a les aplicacions Finances i Operacions anant a **Gestió de projectes i comptabilitat** > **Els contractes** > **del projecte Configura** > **Mostra la comptabilitat** predeterminada. El comptable pot revisar els atributs operatius del contracte del projecte, com ara la data de lliurament sol·licitada i l'import del contracte seleccionant l'identificador del contracte del projecte a les aplicacions Finances i Operacions que obre el registre de contracte del projecte relacionat al Dataverse.

L'entitat del projecte està sincronitzada amb les aplicacions de finances i operacions mitjançant el mapa de la **taula Projectes V2 (projectes msdyn\_).** L'administrador del projecte pot:

  - Revisar projectes en aplicacions de Finances i Operacions anant a **Gestió de Projectes i comptabilitat** > **Tots els projectes**. 
  - Actualitzeu els atributs comptables del projecte a les aplicacions Finances i Operacions anant a **Gestió de projectes i comptabilitat** > **Tots els projectes** > **Configura** > **Mostra la comptabilitat** predeterminada.  
  - Reviseu els atributs operatius del projecte, com ara les dates d'inici i de finalització estimades, seleccionant l'identificador del projecte a les aplicacions finances i operacions que obre el registre del projecte relacionat al Dataverse.

Un projecte s'associa amb un contracte de projecte mitjançant l'entitat **Línia de contracte del projecte**.

Les línies Dataverse de contracte del projecte generen una regla de facturació de contracte de projecte a les aplicacions Finances i Operacions mitjançant el **mapa de la taula Línies de contracte del projecte (salesorderdetails).** El mètode de facturació defineix el tipus de regla de facturació del contracte del projecte a les aplicacions Finances i Operacions:

  - Les línies de contracte del projecte amb un mètode de facturació de temps i materials creen una regla de facturació de tipus de temps i material.
  - Les línies de contracte del mètode de facturació de preu fix creen una regla de facturació de fita.

Les línies de contracte del projecte poden ser revisades pel comptable del projecte a les aplicacions Finances i Operacions anant a **Gestió de projectes i comptabilitat** > **Els contractes** > **de projectes Configura** > **Mostra la comptabilitat** predeterminada i revisant els detalls de la pestanya Línies **de** contracte. El comptador també pot establir dimensions financeres predeterminades per a les línies de contracte del mètode de facturació de preus fixos en aquesta pestanya.

## <a name="billing-milestones"></a>Fites de facturació

Les línies de contracte del projecte que fan servir el mètode de facturació de preu fix es facturen mitjançant fites de facturació. Les fites de facturació se sincronitzen amb les transaccions en compte del projecte a les aplicacions finances i operacions mitjançant el mapa de la taula Fites de la **línia de contracte d'integració d'operacions del projecte (msdyn\_ contractlinescheduleofvalues).**

  ![Integració de fites de facturació.](./media/2Milestones.jpg)

El comptable pot revisar les transaccions del compte i ajustar els atributs de comptabilitat d'aquestes transaccions anant a **Administració i comptabilitat del projecte** > **Contractes de projecte** > **Manteniment** > **Transaccions del compte** o **Administració i comptabilitat del projecte** > **Tots els projectes** > **Manteniment** > **Transaccions del compte**.

Quan es crea per primera vegada una fita de facturació a una línia de contracte del projecte, el sistema crea automàticament un projecte de previsió d'ingressos de preu fix per al projecte associat amb aquesta línia de contracte. Els projectes de previsió d'ingressos de preu fix es poden revisar anant a **Administració i comptabilitat del projecte** > **Projectes de previsió d'ingressos fixos**.

### <a name="project-tasks"></a>Tasques del projecte

Les tasques del projecte se sincronitzen amb les aplicacions finances i operacions a través de l'assignació de la **taula Tasques del projecte (msdyn\_ projecttasks)** només amb finalitats de referència. La creació, l'actualització i la supressió d'operacions no són compatibles amb les aplicacions Finances i Operacions.

  ![Integració de tasques del projecte.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de projecte

L'entitat **Funcions de** recursos del projecte se sincronitza amb les aplicacions de finances i operacions mitjançant les **funcions de recursos del projecte per a totes les empreses (bookableresourcecategories)** només per a finalitats de referència. Com que les funcions de recursos a Dataverse no són específiques de l'empresa, el sistema crea automàticament registres de funcions de recursos específics de l'empresa a les aplicacions de finances i operacions automàticament per a totes les persones jurídiques incloses en l'àmbit d'integració de doble escriptura.

![Integració de funcions de recursos.](./media/5Resources.jpg)

Els recursos del projecte a les operacions del projecte es mantenen Dataverse i no se sincronitzen amb les aplicacions De finances i operacions.

### <a name="transaction-categories"></a>Categories de transacció

Les categories de transaccions es mantenen Dataverse i se sincronitzen amb les aplicacions de finances i operacions mitjançant l'assignació de la **taula De les categories de transaccions del projecte (msdyn\_ transactioncategories).** Després de sincronitzar el registre de categoria de transacció, el sistema crea automàticament quatre registres de categoria compartida. Cada registre correspon a un tipus de transacció a les aplicacions finances i operacions i les enllaça al registre de categoria de transacció.

![Integració de categories de transacció.](./media/4TransactionCategories.jpg)

L'ús de categories de transaccions per a estimacions i valors reals requereix que el comptable del projecte o l'administrador del sistema creï les categories de projecte corresponents a cada entitat legal. Per obtenir més informació, vegeu [Configuració de categories de projecte](../project-accounting/configure-project-categories.md).
