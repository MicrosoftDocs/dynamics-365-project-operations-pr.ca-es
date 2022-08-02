---
title: Configuració del Project Operations i integració de les dades de configuració
description: Aquest article proporciona informació sobre la configuració i configuració de mapes de doble escriptura d'Operacions de projecte.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029140"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configuració del Project Operations i integració de les dades de configuració

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article proporciona informació sobre la integració de doble escriptura del Project Operations per a les entitats de configuració i configuració.

## <a name="project-contracts-contract-lines-and-projects"></a>Contractes del projecte, línies de contracte i projectes

Els contractes de projectes, línies de contracte i projectes es creen i sincronitzen amb Dataverse aplicacions de finançament i operacions per a una comptabilitat addicional. Els registres d'aquestes entitats només es poden crear i suprimir al Dataverse. Tanmateix, a aquests registres es poden afegir atributs comptables, com ara els impagaments del grup fiscal sobre les vendes i les dimensions financeres, a les aplicacions de finances i operacions.

  ![Conceptes d'integració de contractes de projecte.](./media/1ProjectContract.jpg)

Es fa un seguiment dels clients potencials, les oportunitats i els pressupostos de Dataverse l'activitat de vendes i no se sincronitzen amb les aplicacions de finances i operacions perquè no hi ha cap comptabilitat descendent associada a aquesta activitat.

La funcionalitat del contracte de projecte crea un registre de contracte de Dataverse projecte a les aplicacions de finances i operacions mitjançant el **mapa de capçaleres de contracte de projecte (salesorders).** En desar un contracte de projecte al Dataverse, també s'inicia la creació d'un registre d'entitat de client de contracte de projecte. Aquest registre se sincronitza amb les aplicacions de finançament i operacions utilitzant el mapa de la **font de finançament del projecte (msdyn\_ projectcontractssplitbillingrules).** Aquesta assignació també sincronitza les addicions, les actualitzacions i les supressions de clients del contracte del projecte. Els percentatges de facturació dividits entre els clients del contracte de projecte només Dataverse es dominen i no se sincronitzen amb les aplicacions de finances i operacions.

Després de crear un contracte de projecte a Dataverse, el comptable del projecte pot actualitzar els atributs comptables d'aquest contracte de projecte a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Contractes** > **de projectes Configurar** > **Mostra la comptabilitat** per defecte. El comptable pot revisar els atributs del contracte del projecte operatiu, com ara la data de lliurament sol·licitada i l'import del contracte seleccionant l'identificador del contracte del projecte a les aplicacions de finances i operacions que obre el registre de contracte de projecte relacionat a Dataverse.

L'entitat del projecte està sincronitzada amb les aplicacions de finançament i operacions mitjançant el mapa de la **taula Projects V2 (msdyn\_ projects).** L'administrador del projecte pot:

  - Revisa projectes en apps de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Tots els projectes**. 
  - Actualitzeu els atributs comptables del projecte a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Tots els projectes** > **Configurats** > **Mostra la comptabilitat** per defecte.  
  - Reviseu els atributs del projecte operatiu, com ara les dates estimades d'inici i de finalització, seleccionant l'identificador del projecte a les aplicacions de finances i operacions que obre el registre del projecte relacionat a Dataverse.

Un projecte s'associa amb un contracte de projecte mitjançant l'entitat **Línia de contracte del projecte**.

Les línies Dataverse de contracte del projecte creen una regla de facturació del contracte de projecte a les aplicacions de finances i operacions mitjançant el **mapa de la taula de línies de contracte del projecte (salesorderdetails).** El mètode de facturació defineix el tipus de regla de facturació del contracte de projecte a les aplicacions de finances i operacions:

  - Les línies de contracte del projecte amb un mètode de facturació de temps i materials creen una regla de facturació de tipus de temps i material.
  - Les línies de contracte del mètode de facturació de preu fix creen una regla de facturació de fita.

El comptable del projecte pot revisar les línies de contracte del projecte a les aplicacions de finances i operacions anant a **Gestió de projectes i comptabilitat** > **Contractes** > **de projectes Configuració** > **Mostra la comptabilitat** per defecte i revisant els detalls a la pestanya Línies **de** contracte. El comptable també pot establir dimensions financeres per defecte per a les línies de contracte del mètode de facturació de preu fix en aquesta pestanya.

## <a name="billing-milestones"></a>Fites de facturació

Les línies de contracte del projecte que fan servir el mètode de facturació de preu fix es facturen mitjançant fites de facturació. Les fites de facturació se sincronitzen per projectar transaccions a compte en aplicacions de finances i operacions mitjançant el **mapa de la línia de contracte d'integració del Project Operations (msdyn\_ contractlinescheduleofvalues).**

  ![Integració de fites de facturació.](./media/2Milestones.jpg)

El comptable pot revisar les transaccions del compte i ajustar els atributs de comptabilitat d'aquestes transaccions anant a **Administració i comptabilitat del projecte** > **Contractes de projecte** > **Manteniment** > **Transaccions del compte** o **Administració i comptabilitat del projecte** > **Tots els projectes** > **Manteniment** > **Transaccions del compte**.

Quan es crea per primera vegada una fita de facturació a una línia de contracte del projecte, el sistema crea automàticament un projecte de previsió d'ingressos de preu fix per al projecte associat amb aquesta línia de contracte. Els projectes de previsió d'ingressos de preu fix es poden revisar anant a **Administració i comptabilitat del projecte** > **Projectes de previsió d'ingressos fixos**.

### <a name="project-tasks"></a>Tasques del projecte

Les tasques del projecte se sincronitzen amb les aplicacions de finances i operacions a través del mapa de la **taula tasques del projecte (msdyn\_ projecttasks)** només amb finalitats de referència. La creació, l'actualització i la supressió d'operacions no s'admeten mitjançant les aplicacions de finances i operacions.

  ![Integració de tasques del projecte.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de projecte

L'entitat **Funcions de recursos del projecte se sincronitza amb les aplicacions de finances** i operacions mitjançant les **funcions de recursos del projecte per a totes les empreses (bookableresourcecategories)** mapa de taula només amb finalitats de referència. Com que les funcions de recursos no són específiques de Dataverse l'empresa, el sistema crea automàticament registres de funcions de recursos específics de l'empresa respectius a les aplicacions de finances i operacions automàticament per a totes les entitats jurídiques incloses en l'àmbit d'integració de doble escriptura.

![Integració de funcions de recursos.](./media/5Resources.jpg)

Els recursos del projecte al Project Operations es Dataverse mantenen i no se sincronitzen amb les aplicacions de finances i operacions.

### <a name="transaction-categories"></a>Categories de transacció

Les categories de transaccions es Dataverse mantenen i se sincronitzen amb les aplicacions de finances i operacions mitjançant el mapa de la **taula Categories de transaccions de projecte (msdyn\_ transactioncategories).** Després de sincronitzar el registre de categoria de transacció, el sistema crea automàticament quatre registres de categoria compartida. Cada registre correspon a un tipus de transacció en aplicacions de finances i operacions i els enllaça amb el registre de categoria de transacció.

![Integració de categories de transacció.](./media/4TransactionCategories.jpg)

L'ús de categories de transaccions per a estimacions i valors reals requereix que el comptable del projecte o l'administrador del sistema creï les categories de projecte corresponents a cada entitat legal. Per obtenir més informació, vegeu [Configuració de categories de projecte](../project-accounting/configure-project-categories.md).
