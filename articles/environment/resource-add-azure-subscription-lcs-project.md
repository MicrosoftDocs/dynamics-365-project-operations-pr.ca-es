---
title: Addició d'una subscripció a l'Azure a un projecte del LCS
description: En aquest tema es proporciona informació sobre com connectar la subscripció de l'Azure a un projecte del LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175789"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Addició d'una subscripció a l'Azure a un projecte del LCS

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els entorns allotjats al núvol s'han de implementar mitjançant una subscripció existent de l'Azure. En aquest tema s'indica com connectar la subscripció de l'Azure existent a un projecte del LCS. 

## <a name="grant-admin-consent"></a>Concedir el consentiment de l'administrador

1. Al projecte del LCS, a la secció **Entorns**, seleccioneu **Configuració del Microsoft Azure**.

![Configuració del Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. A la pàgina **Configuració del projecte**, a la pestanya **Connectors de l'Azure**, seleccioneu **Autoritza**. Això permet que els entorns s'implementin en aquest projecte.

![Connectors de l'Azure](./media/2AzureConnectors.png)

3. Torneu a seleccionar **Autoritza** per proporcionar el consentiment de l'administrador.

![Concedir el consentiment de l'administrador](./media/3GrantAdminConsent.png)

4. Accepteu la sol·licitud de permisos.

![Acceptar la sol·licitud de permisos](./media/4AcceptPermissionRequest.png)

L'autorització ja s'ha completat. 

![Autorització correcta](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Proporcionar l'accés dels serveis d'implementació del Dynamics a la subscripció de l'Azure

1. Aneu a [Facturació del Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) i seleccioneu la vostra subscripció. Els serveis d'implementació del Dynamics necessiten accedir a aquesta subscripció per poder implementar entorns.

![Detalls de la subscripció de l'Azure](./media/6AzureSubscription.png)

2. Seleccioneu **Control d'accés (IAM)** a la subfinestra de navegació i, a continuació, seleccioneu **Afegeix una assignació de funcions**.
3. Al control lliscant del costat dret, seleccioneu **Funció de col·laborador** i, a la llista proporcionada, cerqueu i seleccioneu **Serveis d'implementació del Dynamics**. 
4. Seleccioneu **Desa**.

![Accés de la subscripció](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Afegir un connector de subscripció a un projecte del LCS

1. Al projecte del LCS, a la pàgina **Configuració del Microsoft Azure**, seleccioneu **Afegeix** per afegir un connector nou.
2. Introduïu l'identificador de subscripció de l'Azure. Podeu trobar l'identificador de subscripció de l'Azure al [portal de l'Azure](https://ms.portal.azure.com/), a **Configuració** a la part inferior esquerra de la pantalla.
3. Al camp **Configura per utilitzar l'Azure Resource Manager**, seleccioneu **Sí**.
4. Assegureu-vos que el domini de l'inquilí de l'AAD de subscripció de l'Azure coincideixi amb la subscripció de l'Azure propietària del domini que esteu utilitzant i seleccioneu **Següent**.
5. A la pantalla **Configuració del Microsoft Azure**, seleccioneu **Següent** per confirmar. Si rebeu un error en aquesta pantalla, torneu a la secció [Proporcionar accés dels serveis d'implementació del Dynamics a la subscripció de l'Azure](#provide) en aquest tema i assegureu-vos que heu completat tots els passos.
6. Baixeu el certificat d'administració de l'Azure a una carpeta local de l'ordinador i, a continuació, carregueu-la al Portal d'administració de l'Azure a **Configuració** > **Certificats d'administració**. Aquest certificat permetrà que el LCS es comuniqui amb l'Azure en el vostre nom. Podeu ometre aquest pas si l'usuari té accés a la subscripció.
7. Seleccioneu **Següent**.
8. Seleccioneu la regió de l'Azure per implementar i seleccioneu un centre de dades a prop del lloc on teniu pensat utilitzar aquest sistema.
9.  Seleccioneu **Connecta**.

Heu connectat correctament la subscripció de l'Azure. Ara podeu implementar els entorns allotjats al núvol del Dynamics 365 Finance.


