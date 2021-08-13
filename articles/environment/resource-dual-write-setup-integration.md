---
title: Configuració del Project Operations i integració de les dades de configuració
description: Aquest tema proporciona informació sobre la configuració d'assignacions de doble escriptura del Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986524"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Configuració del Project Operations i integració de les dades de configuració

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema proporciona informació sobre la integració de doble escriptura del Project Operations per a les entitats de configuració.

## <a name="project-contracts-contract-lines-and-projects"></a>Contractes del projecte, línies de contracte i projectes

Els contractes de projecte, les línies de contracte i els projectes es creen al Dataverse i se sincronitzen amb les aplicacions del Finance and Operations per a una comptabilitat addicional. Els registres d'aquestes entitats només es poden crear i suprimir al Dataverse. Tanmateix, els atributs de comptabilitat, com ara els valors per defecte del grup d'impostos de vendes i les propietats financeres, es poden afegir a aquests registres a les aplicacions del Finance and Operations.

  ![Conceptes d'integració de contractes de projecte.](./media/1ProjectContract.jpg)

Es fa un seguiment de l'activitat dels clients potencials, de les oportunitats i de les ofertes de vendes al Dataverse i no se sincronitzen amb les aplicacions del Finance and Operations perquè no hi ha cap comptabilitat descendent dels registres associats amb aquesta activitat.

La funcionalitat dels contractes de projecte al Dataverse crea un registre de contractes de projecte a les aplicacions del Finance and Operations utilitzant l'assignació de taula de **Capçaleres de contracte del projecte (salesorders)**. En desar un contracte de projecte al Dataverse, també s'inicia la creació d'un registre d'entitat de client de contracte de projecte. Aquest registre se sincronitza amb les aplicacions del Finance and Operations mitjançant l'assignació de taules **Origen de fons del projecte (msdyn\_projectcontractssplitbillingrules)**. Aquesta assignació també sincronitza les addicions, les actualitzacions i les supressions de clients del contracte del projecte. Els percentatges de facturació fraccionats entre els clients del contracte de projecte només es patronitzen al Dataverse i no se sincronitzen a les aplicacions del Finance and Operations.

Després de crear un contracte de projecte al Dataverse, el comptable del projecte pot actualitzar els atributs de comptabilitat d'aquest contracte de projecte a les aplicacions del Finance and Operations anant a **Administració i comptabilitat del projecte** > **Contractes de projecte** > **Configuració** > **Mostra la comptabilitat per defecte**. El comptador pot revisar els atributs del contracte del projecte operatius, com ara la data de lliurament sol·licitada i l'import del contracte seleccionant l'ID de contracte del projecte a les aplicacions del Finance and Operations, cosa que obre el registre de contracte de projecte relacionat al Dataverse.

L'entitat de projecte se sincronitza amb les aplicacions del Finance and Operations utilitzant l'assignació de taules **Projectes V2 (msdyn\_projects)**. L'administrador del projecte pot:

  - Reviseu els projectes de les aplicacions del Finance and Operations anant a **Administració i comptabilitat de projectes** > **Tots els projectes**. 
  - Actualitzeu els atributs de comptabilitat del projecte a les aplicacions del Finance and Operations anant a **Administració i comptabilitat de projectes** > **Tots els projectes** > **Configuració** > **Mostra la comptabilitat per defecte**.  
  - Reviseu els atributs del projecte operatius, com ara les dates d'inici i d'acabament previstes, seleccionant l'ID de projecte a les aplicacions del Finance and Operations, cosa que obre el registre de projecte relacionat al Dataverse.

Un projecte s'associa amb un contracte de projecte mitjançant l'entitat **Línia de contracte del projecte**.

Les línies de contracte del projecte al Dataverse creen una norma de facturació de contractes de projecte a les aplicacions del Finance and Operations utilitzant l'assignació de taula de **Línies de contracte del projecte (salesorderdetails)**. El mètode de facturació defineix el tipus de regla de facturació del contracte de projecte a les aplicacions del Finance and Operations:

  - Les línies de contracte del projecte amb un mètode de facturació de temps i materials creen una regla de facturació de tipus de temps i material.
  - Les línies de contracte del mètode de facturació de preu fix creen una regla de facturació de fita.

El comptable del projecte pot revisar les línies de contracte del projecte a les aplicacions del Finance and Operations anant a **Administració i comptabilitat del projecte** > **Contractes del projecte** > **Configuració** > **Mostra la comptabilitat per defecte** i revisant els detalls de la pestanya **Línies de contracte**. En aquesta pestanya, el comptable també pot definir mesures financeres per defecte per a les línies de contracte del mètode de facturació de preu fix.

## <a name="billing-milestones"></a>Fites de facturació

Les línies de contracte del projecte que fan servir el mètode de facturació de preu fix es facturen mitjançant fites de facturació. Les fites de facturació se sincronitzen amb les transaccions de compte del projecte a les aplicacions del Finance and Operations utilitzant l'assignació de taules **fites de les línies de contracte d'integració del Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integració de fites de facturació.](./media/2Milestones.jpg)

El comptable pot revisar les transaccions del compte i ajustar els atributs de comptabilitat d'aquestes transaccions anant a **Administració i comptabilitat del projecte** > **Contractes de projecte** > **Manteniment** > **Transaccions del compte** o **Administració i comptabilitat del projecte** > **Tots els projectes** > **Manteniment** > **Transaccions del compte**.

Quan es crea per primera vegada una fita de facturació a una línia de contracte del projecte, el sistema crea automàticament un projecte de previsió d'ingressos de preu fix per al projecte associat amb aquesta línia de contracte. Els projectes de previsió d'ingressos de preu fix es poden revisar anant a **Administració i comptabilitat del projecte** > **Projectes de previsió d'ingressos fixos**.

### <a name="project-tasks"></a>Tasques del projecte

Les tasques de projecte se sincronitzen amb les aplicacions del Finance and Operations mitjançant l'assignació de taules **Tasques del projecte (msdyn\_projecttasks)** només per a finalitats de referència. Les operacions de creació, actualització i supressió no estan admeses a través de les aplicacions del Finance and Operations.

  ![Integració de tasques del projecte.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Recursos de projecte

L'entitat **Funcions del recurs de projecte** se sincronitza amb les aplicacions del Finance and Operations utilitzant l'assignació de taules **Funcions de recurs de projecte per a totes les empreses (bookableresourcecategories)** per motius de referència només. Com que les funcions de recurs al Dataverse no són específiques de l'empresa, el sistema crea automàticament registres de funcions de recursos específiques de l'empresa respectives a les aplicacions del Finance and Operations automàticament per a totes les entitats jurídiques, incloses en l'àmbit d'integració de doble escriptura.

![Integració de funcions de recursos.](./media/5Resources.jpg)

Els recursos del projecte del Project Operations es mantenen al Dataverse i no se sincronitzen amb les aplicacions del Finance and Operations.

### <a name="transaction-categories"></a>Categories de transacció

Les categories de transaccions es mantenen al Dataverse i se sincronitzen amb les aplicacions del Finance and Operations utilitzant l'assignació de taules **Categories de transaccions del projecte (msdyn\_transactioncategories)**. Després de sincronitzar el registre de categoria de transacció, el sistema crea automàticament quatre registres de categoria compartida. Cada registre correspon a un tipus de transacció de les aplicacions del Finance and Operations i els enllaça amb el registre de categoria de transaccions.

![Integració de categories de transacció.](./media/4TransactionCategories.jpg)

L'ús de categories de transaccions per a estimacions i valors reals requereix que el comptable del projecte o l'administrador del sistema creï les categories de projecte corresponents a cada entitat legal. Per obtenir més informació, vegeu [Configuració de categories de projecte](../project-accounting/configure-project-categories.md).
