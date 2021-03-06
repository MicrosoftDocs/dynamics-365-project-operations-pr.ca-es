---
title: Proveïment d'un entorn nou
description: En aquest tema s'ofereix informació sobre com proveir un entorn nou del Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949350"
---
# <a name="provision-a-new-environment"></a>Proveïment d'un entorn nou

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest tema es proporciona informació sobre com es proveeix un nou entorn del Dynamics 365 Project Operations per a escenaris basats en recursos/sense existències.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Habilitar el proveïment automatitzat del Project Operations en un projecte del LCS

Seguiu aquests passos per habilitar el flux de proveïment automatitzat del Project Operations per al projecte del LCS.

1. Aneu a [LCS](https://lcs.dynamics.com/v2) i seleccioneu la peça **Administració de característiques de versió preliminar**.
2. A la llista **Característiques de versió preliminar**, seleccioneu **Project Operations** i **Característica de versió preliminar habilitada** per habilitar el Project Operations.

> [!NOTE]
> Aquest pas només es fa una vegada per projecte del LCS.

## <a name="provision-a-project-operations-environment"></a>Proveïment d'un entorn del Project Operations

1. Obriu una nova implementació d'un [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o [entorn de producció](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) del Dynamics 365 Finance. 
2. Seguiu els passos de l'auxiliar **Proveïment de l'entorn**. 

> [!IMPORTANT]
> Assegureu-vos que la versió de l'aplicació seleccionada sigui 10.0.13 o superior.

3. Per proveir el Project Operations, a **Configuració avançada**, seleccioneu **Common Data Service**. 
4. Habiliteu la **Configuració del Common Data Service** seleccionant **Sí** i, a continuació, introduïu informació als camps obligatoris:

  - Nom
  - Regió
  - Language
  - Moneda
 
5. Al camp **Plantilla del Common Data Service**, seleccioneu **Project Operations** 

6. Seleccioneu el tipus d'entorn per a la implementació. Una prova basada en subscripció us permetrà implementar un entorn del CDS durant 30 dies. 

![Configuració de la implementació](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Seleccioneu **Accepto** per reconèixer les condicions del servei i, a continuació, seleccioneu **Fet** per tornar a la configuració de la implementació.

![Consentiment de la implementació](./media/2DeploymentConsent.png)

7. Completeu els camps obligatoris restants a l'auxiliar i confirmeu la implementació. El temps de proveïment de l'entorn varia segons el tipus d'entorn. El proveïment pot tardar fins a sis hores.

  Quan la implementació es completi correctament, l'entorn es mostrarà com a **Implementat**.

8. Per confirmar que l'entorn s'ha implementat correctament, seleccioneu **Inicia la sessió** i inicieu la sessió a l'entorn per confirmar-ho.

![Detalls de l'entorn del ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Aplicar les dades de demostració del Project Operations Finance (pas opcional)

Apliqueu les dades de demostració del Project Operations Finance a l'entorn allotjat al núvol de la versió del servei 10.0.13 com es descriu en [aquest article](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar les actualitzacions a l'entorn del Finance

El Project Operations requereix un entorn del Finance amb la versió de l'aplicació **10.0.13 (10.0.569.20009)** o superior.

Pot ser que hàgiu d'aplicar actualitzacions de qualitat al vostre entorn del Finance per rebre aquesta versió.

1. Al LCS, a la pàgina **Detalls de l'entorn**, a la secció **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització**.

![Visualitzar les actualitzacions](./media/5ViewUpdates.png)

2. A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet.**

![Desar el paquet](./media/6SavePackage.png)

3. Feu clic a **Selecciona-ho tot** i seleccioneu **Desa el paquet**.

![Revisar i desar les actualitzacions](./media/7ReviewAndSaveUpdates.png)

4. Introduïu un nom i una descripció del paquet i, a continuació, seleccioneu **Desa**. En funció de la connexió a Internet, pot ser que aquest procés tardi una estona.

![Carregar el paquet a la biblioteca d'actius](./media/8UploadPackageToAssetsLibrary.png)

5. Un cop desat el paquet, seleccioneu **Fer** i deseu aquest paquet a la biblioteca d'actius del projecte del LCS.

El desament i la validació del paquet poden tardar uns 15 minuts.

6. Per aplicar l'actualització, aneu a la pàgina **Detalls de l'entorn** del LCS i seleccioneu **Mantén** > **Aplica les actualitzacions**.

![Mantenir els entorns](./media/9MaintainEnvironment.png)

7. A la llista actualitzacions, seleccioneu el paquet que heu creat i seleccioneu **Aplica**.

![Aplicar les actualitzacions](./media/10ApplyUpdates.png)

El procés de servei de l'entorn tardarà una estona. Després d'haver acabat, l'entorn tornarà a un estat implementat.

![Entorn implementat](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establir una connexió d'escriptura doble 

1. Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.
2. A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions**.
3. Després d'haver acabat l'enllaç, torneu a seleccionar **Enllaça amb el CDS per a aplicacions**. Se us redirigirà a l'escriptura doble al Finance.

![Enllaça amb el CDS](./media/12LinktoCDS.png)

4. Seleccioneu **Aplica la solució** per accedir a les entitats que s'assignaran a la integració.

![Aplicar les solucions](./media/13ApplySolutions.png)

5. Seleccioneu les dues solucions, **Assignació d'entitats d'escriptura doble del Dynamics 365 Finance and Operations** i **Assignacions d'entitats d'escriptura doble del Dynamics 365 Project Operations** i, a continuació, seleccioneu **Aplica**.

![Confirmar les solucions](./media/14ConfirmSolutions.png)

Després de l'aplicació de les solucions, les entitats d'escriptura doble s'apliquen a l'entorn.

![Aplicar les solucions](./media/15ApplyingSolutions.png)

Després d'aplicar les entitats, totes les assignacions disponibles apareixen a la llista de l'entorn.

![Assignacions d'escriptura doble](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualitzar les entitats de dades després de l'actualització

1. Al Finance, aneu a l'àrea de treball **Administració de dades**.

![Espai de treball d'administració de dades](./media/16DataManagement.png)

2. Seleccioneu la peça **Paràmetres del marc**.

![Paràmetres del marc](./media/17FrameworkParameters.png)

3. A la pàgina **Configuració de l'entitat**, seleccioneu **Actualitza la llista d'entitats**.

![Actualitzar la llista d'entitats](./media/18RefreshEntityList.png)

L'actualització tardarà uns 20 minuts. Rebreu una alerta quan s'hagi completat.

![Confirmació d'actualització](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Executar assignacions d'escriptura doble del Project Operations

1. Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.
2. A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions.** Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.
3. Inicieu les assignacions com es descriu a la taula següent. Assegureu-vos de seguir la seqüència que s'indica a la llista.

| **Assignació d'entitats** | **Actualitzar l'entitat** | **Sincronització inicial** | **Mestre per a la sincronització inicial** | **Requisits previs de l'execució** | **Sincronització inicial dels requisits previs** |
| --- | --- | --- | --- | --- | --- |
| **Funcions de recurs del projecte per a totes les empreses (bookableresourcecategories)** | No | Sí | Common Data Service | No | N/D |
| **Entitats jurídiques (cdm\_companies)** | No | Sí | Aplicacions del Finance and Operations | No | N/D |
| **Valors reals d'integració del Project Operations (msdyn\_actuals)** | No | No | N/D | Sí | No |
| **Línies de contracte del projecte (salesorderdetails)** | No | No | N/D | No | No |
| **Entitat d'integració per a les relacions de transaccions del projecte (msdyn\_transactionconnections)** | No | No | N/D | No | N/D |
| **Fites de línia de contracte d'integració del Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | N/D | No | N/D |
| **Entitat d'integració del Project Operations per a l'estimació de despeses (msdyn\_estimateslines)** | No | No | N/D | No | N/D |
| **Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)** | No | No | N/D | No | N/D |
| **Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn\_expenses)** | Sí | No | N/D | No | N/D |
| **Entitat d'integració del Project Operations per a l'estimació d'hores (msdyn\_resourceassignments)** | Sí | No | N/D | No | N/D |

4. Per actualitzar l'entitat, seleccioneu el nom de l'assignació i, a continuació, **Actualitza les entitats**. 
5. Continueu amb l'execució de l'assignació després d'haver acabat l'actualització.

![Actualitzar l'assignació](./media/20RefreshMapping.png)

Abans d'habilitar la següent assignació, verifiqueu que l'assignació de la taula estigui en estat **En execució**. L'execució d'assignacions amb un major nombre de requisits previs podria tardar una estona.

Per executar una assignació amb requisits previs, habiliteu l'opció **Mostra les assignacions d'entitats relacionades**. Si la taula indica que la **Sincronització inicial de requisits previs** és **No**, verifiqueu que l'indicador **Sincronització inicial** estigui **desactivat** a totes les assignacions de requisits previs abans d'executar-la.

![Executar l'assignació](./media/21RunMap.png)

6. Valideu que totes les assignacions relacionades del projecte estiguin en execució.

![Totes les assignacions en execució](./media/22AllMapsRunning.png)

L'entorn del Project Operations ja està proveït i configurat.
