---
title: Actualitzeu el Project Operations a l'entorn de finances
description: Aquest tema proporciona informació sobre com actualitzar el Project Operations al vostre entorn del Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3665bccfa25c759c0f2351c691d24901867c178f7c339f4a524856842666aec5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986749"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Actualitzeu el Project Operations a l'entorn de finances

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Aquest tema proporciona informació sobre com actualitzar el Dynamics 365 Project Operations al vostre entorn del Dynamics 365 Finance. Hi ha tres procediments que són necessaris per actualitzar el Project Operations a l'actualització 5 (UR5):

- [Importa el paquet al vostre projecte de visualització prèvia](#import)
- [Aplica l'actualització](#apply)
- [Configuració del vostre entorn del Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importa el paquet al vostre projecte LCS

1. Inicieu sessió als [Lifecycle Services (LCS)](https://lcs.dynamics.com/) com a propietari del projecte o administrador de l'entorn.
2. A la llista de projectes, seleccioneu el vostre projecte LCS.
3. A la pàgina **Projecte**, al grup **Entorns**, obriu l'entorn que voleu actualitzar.
4. Comproveu que l'entorn s'estigui executant. Si no s'ha iniciat, inicieu l'entorn.
5. A la secció **Nova versió**, a **Actualitzacions disponibles**, seleccioneu **Visualitza l'actualització** per a 10.0.15.

![Visualitza el botó d'actualització.](media/view-update.png)

6. A la pàgina **Actualitzacions binàries**, seleccioneu **Desa el paquet**.
7. A la pàgina **Revisa i desa actualitzacions**, seleccioneu **Desa el paquet**.
8. Al panell **Desa el paquet a la biblioteca d'actius** que s'obre, introduïu el nom del paquet i seleccioneu **Desa el paquet**.
9. Quan l'LCS hagi desat el paquet, el botó **Fet** està habilitat. Seleccioneu **Fet**. L'LCS verificarà el paquet. La verificació pot trigar uns minuts o fins a una hora.


## <a name="apply-the-package-update"></a><a name="apply"></a>Aplica l'actualització del paquet

1. A l'LCS, a la pàgina **Detalls de l'entorn**, seleccioneu **Conserva** > **Aplica actualitzacions**.
2. A la llista, seleccioneu el paquet que heu desat abans i, a continuació, seleccioneu **Aplica**.
3. Seleccioneu **Sí** per confirmar que voleu implementar el paquet.

![Quadre de diàleg Confirmació de la implementació del paquet.](media/confirm-package-deployment.png)

4. Seleccioneu **Sí** per confirmar que voleu actualitzar l'aplicació.

![Quadre de diàleg Confirmació de l'actualització de l'aplicació.](media/confirm-application-update.png)

S'iniciarà la implementació i l'actualització de l'aplicació. 

A la pàgina **Detalls de l'entorn**, a la part superior dreta, l'estat de l'entorn s'actualitzarà a **Manteniment**. Aproximadament en dues hores, l'actualització es completarà. La informació de la versió de l'aplicació s'actualitzarà a **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** i l'estat de l'entorn s'actualitzarà a **Implementat**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Actualització del vostre entorn del Dataverse

1. Inicieu la sessió al [Centre d'administració del Power Platform](https://admin.powerplatform.com/).
2. A la llista, cerqueu i obriu l'entorn que heu utilitzat per instal·lar el Project Operations.
3. A la pàgina **Entorns**, seleccioneu **Recurs** > **Aplicacions del Dynamics 365**.
4. A la llista, localitzeu el **Microsoft Dynamics 365 Project Operations** i, a la columna **Estat**, seleccioneu **Actualització disponible**.
5. Activeu la casella de selecció **Accepto les condicions del servei** i, a continuació, seleccioneu **Actualitza**. S'instal·larà la versió més recent de la solució.

Un cop completada la instal·lació, tindreu instal·lada la versió 4.5.0.134.

## <a name="configure-new-features"></a>Configura característiques noves

### <a name="enable-dual-write-mapping"></a>Habilita les assignacions d'escriptura doble

Un cop completada l'actualització als entorns de Finances i del Dataverse, podeu habilitar les assignacions d'escriptura doble necessàries. Completeu els següents passos per habilitar les assignacions d’escriptura doble.

- [Actualitza la configuració de seguretat de l'entorn del Customer Engagement](#security)
- [Actualitza les entitats de dades](#refresh)
- [Actualitza i executa les assignacions d'escriptura doble](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Actualitza la configuració de seguretat de l'entorn del Dataverse

Les actualitzacions següents per als privilegis de seguretat per a les entitats són necessàries com a part de l'actualització a UR5.

1. Al vostre entorn del Dataverse, aneu a **Configuració** i, al grup **Sistema**, seleccioneu **Seguretat**.

![Configuració de l'entorn del Dataverse.](media/Picture21.png)

2. Seleccioneu **Funcions de seguretat**.
3. A la llista de funcions, seleccioneu **usuari de l'aplicació de doble escriptura** i seleccioneu la pestanya **Entitats personalitzades**. 
4. Verifiqueu que la funció té permisos de **Lectura** i **Annexa a**:

      - **Tipus de canvi de moneda**
      - **Taula de comptes** 
      - **Calendari fiscal** 
      - **Llibre major**

5. Quan la funció de seguretat s'actualitzi, aneu **Configuració** > **Seguretat** > **Equips**. Verifiqueu que la funció d'**usuari de l'aplicació de doble escriptura** s'hagi aplicat a l'equip. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Actualitza les entitats de dades des de l'actualització

1. A l'entorn de finances, obriu l'espai de treball **Administració de dades** i, a continuació, obriu la pàgina **Paràmetres del marc**.
2. A la pestanya **Configuració d'entitat**, seleccioneu **Actualitza la llista d'entitats**.
3. Seleccioneu **Tanca** per confirmar l'actualització de l'entitat.

 > [!NOTE]
 > Aquest procés trigarà 20 aproximadament. Quan l'actualització finalitzi, se us notificarà.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Actualitza les assignacions d'escriptura doble

1. A l'àrea de treball **Administració de dades**, seleccioneu **Escriptura doble**.
2. Seleccioneu **Aplicar solucions**, seleccioneu les dues solucions a la llista i, a continuació, seleccioneu **Aplica**.
3. A la pàgina **Escriptura doble**, seleccioneu les assignacions de taula següents i, a continuació, seleccioneu **Atura**.

    - **Valors reals d'integració del Project Operations (msdyn_actuals)**
    - **Categories de despeses del projecte d'integració del Project Operations (msdyn_expensecategories)**
    - **Entitat d'exportació de despeses del projecte d'integració del Project Operations (msdyn_expenses)**

4. A la pàgina **Vversió de l'assignació de la taula**, apliqueu una versió nova del mapa a cadascuna de les tres entitats.
5. A la pàgina **Escriptura doble**, seleccioneu executa per reiniciar les assignacions.
6. A la llista de mapes, seleccioneu l'assignació **Llibre major (msdyn_ledgers)** amb tots els requisits previs i activeu la casella de selecció **Sincronització inicial**. 
7. Al camp **Mestre per a la sincronització inicial**, seleccioneu les **aplicacions Finance and Operations** i, a continuació, seleccioneu **Executa**.
 
 ![Sincronització de l'assignació de llibres majors.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]