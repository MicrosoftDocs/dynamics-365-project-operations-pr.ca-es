---
title: Proveïment d'un entorn nou
description: En aquest article s'ofereix informació sobre com proveir un entorn nou del Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 78f40ebe79c038799fbc59902442ad6c23fb94d4
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028485"
---
# <a name="provision-a-new-environment"></a>Proveïment d'un entorn nou

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_



En aquest article es proporciona informació sobre com proveir un nou entorn de Dynamics 365 Project Operations per a escenaris basats en recursos/sense existències.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Habilitar el proveïment automatitzat del Project Operations en un projecte del LCS

Seguiu aquests passos per habilitar el flux de proveïment automatitzat del Project Operations per al projecte del LCS.

1. Aneu a [LCS](https://lcs.dynamics.com/v2) i seleccioneu la peça **Administració de característiques de versió preliminar**.
2. A la llista **Característiques de versió preliminar**, seleccioneu **Característica del Project Operations** i **Característica de versió preliminar habilitada** per habilitar el Project Operations.

   > [!NOTE]
   > Aquest pas només es fa una vegada per projecte del LCS.

## <a name="provision-a-project-operations-environment"></a>Proveïment d'un entorn del Project Operations

1. Obriu una nova implementació d'un [entorn de demostració](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) o un [entorn d'espai aïllat/de producció](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) del Dynamics 365 Finance. 
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

     ![Configuració de la implementació.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Seleccioneu **Accepto** per reconèixer les condicions del servei i, a continuació, seleccioneu **Fet** per tornar a la configuració de la implementació.
    >
    >![Consentiment de la implementació.](./media/2DeploymentConsent.png)

7. Opcional: aplicar dades de demostració a l'entorn. Aneu a **Configuració avançada**, seleccioneu **Personalitza la configuració de la base de dades SQL** i definiu **Especifica un conjunt de dades per a la base de dades d'aplicacions** a **Demostració**.
8. Completeu els camps obligatoris restants a l'auxiliar i confirmeu la implementació. El temps de proveïment de l'entorn varia segons el tipus d'entorn. El proveïment pot tardar fins a sis hores.

   Quan la implementació es completi correctament, l'entorn es mostrarà com a **Implementat**.

9. Per confirmar que l'entorn s'ha implementat correctament, seleccioneu **Inicia la sessió** i inicieu la sessió a l'entorn per confirmar-ho.

    ![Detalls de l'entorn.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplicar les actualitzacions a l'entorn del Finance

El Project Operations requereix un entorn del Finance amb la versió de l'aplicació **10.0.13 (10.0.569.20009)** o superior.

Pot ser que hàgiu d'aplicar actualitzacions de qualitat al vostre entorn del Finance per rebre aquesta versió.

1. Al LCS, a la pàgina **Detalls de l'entorn**, a la secció **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització**.

    ![Visualitzar les actualitzacions.](./media/5ViewUpdates.png)

2. A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet.**

    ![Desar el paquet.](./media/6SavePackage.png)

3. Feu clic a **Selecciona-ho tot** i seleccioneu **Desa el paquet**.

    ![Revisar i desar les actualitzacions.](./media/7ReviewAndSaveUpdates.png)

4. Introduïu un nom i una descripció del paquet i, a continuació, seleccioneu **Desa**. En funció de la connexió a Internet, pot ser que aquest procés tardi una estona.

    ![Carregar el paquet a la biblioteca d'actius.](./media/8UploadPackageToAssetsLibrary.png)

5. Un cop desat el paquet, seleccioneu **Fer** i deseu aquest paquet a la biblioteca d'actius del projecte del LCS.

   El desament i la validació del paquet poden tardar uns 15 minuts.

6. Per aplicar l'actualització, aneu a la pàgina **Detalls de l'entorn** del LCS i seleccioneu **Mantén** > **Aplica les actualitzacions**.

    ![Mantenir els entorns.](./media/9MaintainEnvironment.png)

7. A la llista actualitzacions, seleccioneu el paquet que heu creat i seleccioneu **Aplica**.

    ![Aplicar les actualitzacions.](./media/10ApplyUpdates.png)

   El procés de servei de l'entorn tardarà una estona. Després d'haver acabat, l'entorn tornarà a un estat implementat.

    ![Entorn implementat.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Establir una connexió d'escriptura doble 

1. Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.
2. A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions**.
3. Després d'haver acabat l'enllaç, torneu a seleccionar **Enllaça amb el CDS per a aplicacions**. Se us redirigirà a l'escriptura doble al Finance.

    ![Enllaça amb el CDS.](./media/12LinktoCDS.png)

4. Seleccioneu **Aplica la solució** per accedir a les entitats que s'assignaran a la integració.

    ![Aplicar les solucions.](./media/13ApplySolutions.png)

5. Seleccioneu les dues solucions, el **mapa d'entitats d'escriptura doble del Dynamics 365 Finance** i els **mapes d'entitat d'escriptura doble del Dynamics 365 Project Operations** i, a continuació, seleccioneu **Aplica**.

    ![Confirmar les solucions.](./media/14ConfirmSolutions.png)

    Després de l'aplicació de les solucions, les entitats d'escriptura doble s'apliquen a l'entorn.

    ![Aplicar les solucions.](./media/15ApplyingSolutions.png)

    Després d'aplicar les entitats, totes les assignacions disponibles apareixen a la llista de l'entorn.

    ![Assignacions d'escriptura doble.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualitzar les entitats de dades després de l'actualització

1. Al Finance, aneu a l'àrea de treball **Administració de dades**.

    ![Espai de treball d'administració de dades.](./media/16DataManagement.png)

2. Seleccioneu la peça **Paràmetres del marc**.

    ![Paràmetres del marc.](./media/17FrameworkParameters.png)

3. A la pàgina **Configuració de l'entitat**, seleccioneu **Actualitza la llista d'entitats**.

    ![Actualitzar la llista d'entitats.](./media/18RefreshEntityList.png)

L'actualització tardarà uns 20 minuts. Rebreu una alerta quan s'hagi completat.

  ![Confirmació d'actualització.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Actualitzar la configuració de seguretat del Project Operations al Dataverse

1. Aneu al Project Operations del vostre entorn del Dataverse. 
2. Aneu a **Configuració** > **Seguretat** > **Funcions de seguretat**. 
3. A la pàgina **Funcions de seguretat**, a la llista de funcions, seleccioneu **usuari de l'aplicació de doble escriptura** i seleccioneu la pestanya **Entitats personalitzades**.  
4. Verifiqueu que la funció té permisos de **Lectura** i **Annexa a** per a les entitats següents:
      
      - **Tipus de canvi de moneda**
      - **Taula de comptes**
      - **Calendari fiscal**
      - **Llibre major**
      - **Empresa**
      - **Despesa**

5. Quan la funció de seguretat s'actualitzi, aneu a **Configuració** > **Seguretat** > **Equips** i seleccioneu l'equip per defecte a la visualització d'equips **Propietari de l'empresa local**.
6. Seleccioneu **Administra les funcions** i verifiqueu que s'aplica el privilegi de seguretat **usuari de l'aplicació de doble escriptura** a aquest equip.

## <a name="run-project-operations-dual-write-maps"></a>Executar assignacions d'escriptura doble del Project Operations

1. Al projecte del LCS, aneu a la pàgina **Detalls de l'entorn**.
2. A **Informació de l'entorn del Common Data Service**, seleccioneu **Enllaça amb el CDS per a aplicacions.** Després de seleccionar l'enllaç, se us redirigirà a la llista d'entitats de les assignacions.
3. Inicieu les assignacions. Per obtenir més informació, vegeu [Versions d'assignació amb doble escriptura al Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Valideu que totes les assignacions relacionades del projecte estiguin en execució.

    ![Totes les assignacions en execució.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Aplicació de les dades de configuració al CDS per al Project Operations (opcional)

Si heu aplicat dades de demostració a l'entorn del Finance, vegeu [Configurar i aplicar dades de configuració al Common Data Service per al Project Operations](resource-apply-pro-setup-config-data.md) per aplicar dades de demostració a l'entorn del CDS.


L'entorn del Project Operations ja està proveït i configurat. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
