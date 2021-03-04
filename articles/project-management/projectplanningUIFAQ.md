---
title: Solucionar problemes de funcionament a la quadrícula de tasques
description: En aquest tema es proporciona informació sobre la detecció d'errors que es necessita quan es treballa a la quadrícula de tasques.
author: ruhercul
manager: tfehr
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 89bbad62c2a0a5693a57cf5c9a812ab644486469
ms.sourcegitcommit: c9edb4fc3042d97cb1245be627841e0a984dbdea
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031525"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemes de funcionament a la quadrícula de tasques 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest tema es descriu com solucionar els problemes amb què us podeu trobar mentre treballeu amb l'administració de costos.

## <a name="enable-cookies"></a>Habilita les galetes:

El Project Operations requereix que s'habilitin galetes de tercers per representar l'estructura del desglossament del treball. Quan les galetes de tercers no estan habilitades, en lloc de veure les tasques, veureu una pàgina en blanc quan seleccioneu la pestanya **Tasques** a la pàgina **Projecte**.

![Pestanya en blanc quan les galetes de tercers no estan habilitades](media/blankschedule.png)


### <a name="workaround"></a>Solució alternativa
Per als navegadors Microsoft Edge o Google Chrome, a continuació s'explica com s'actualitza la configuració del navegador per habilitar les galetes de tercers.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Obriu el navegador Microsoft Edge.
2. A la cantonada superior dreta, seleccioneu la **el·lipsi** (...) i, a continuació, seleccioneu **Configuració**.
3. A **Galetes i permisos del lloc**, seleccioneu **Galetes i dades del lloc**.
4. Desactiveu **Bloqueja les galetes de tercers**.

#### <a name="google-chrome"></a>Google Chrome

1. Obriu el navegador Chrome.
2. A la cantonada superior dreta, seleccioneu els tres punts verticals i, a continuació, seleccioneu **Configuració**.
3. A **Privades i seguretat**, seleccioneu **Galetes i altres dades dels llocs web**.
4. Seleccioneu **Permet totes les galetes**.

> [!IMPORTANT]
> Si bloquegeu les galetes de tercers, totes les galetes i les dades de llocs d'altres llocs es bloquejaran, encara que el lloc estigui autoritzat a la vostra llista d'excepcions.

## <a name="pex-endpoint"></a>Extrem PEX

El Project Operations requereix que un paràmetre de projecte faci referència a l'extrem del PEX. Aquest extrem es necessita per comunicar-se amb el servei utilitzat per representar l'estructura del desglossament del treball. Si el paràmetre no està habilitat, rebreu l'error "El paràmetre de projecte no és vàlid". 

### <a name="workaround"></a>Solució alternativa
 ![Camp extrem del PEX al paràmetre de projecte](media/projectparameter.png)

1. Afegiu el camp **extrem del PEX** a la pàgina **Paràmetres del projecte**.
2. Actualitzeu el camp amb el següent valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=\<id>&type=2`
3. Suprimiu el camp de la pàgina **Paràmetres del projecte**.

## <a name="privileges-for-project-for-the-web"></a>Privilegis per al projecte per al web

El Project Operations es basa en un servei de planificació extern. El servei requereix que un usuari tingui assignades diverses funcions per llegir i escriure a entitats relacionades amb l'estructura del desglossament del treball. Aquestes entitats inclouen tasques de projecte, assignacions de recursos i dependències de tasques. Si un usuari no pot representar l'estructura del desglossament del treball quan va a la pestanya **Tasques**, probablement és perquè projecte per al Project Operations no s'ha habilitat. Un usuari pot rebre un error de funció de seguretat o un error relacionat amb una denegació d'accés.


## <a name="workaround"></a>Solució alternativa

1. Aneu a **Configuració > Seguretat > Usuaris > Usuaris d'aplicació**.  

   ![Lector de l'aplicació](media/applicationuser.jpg)
   
2. Feu doble clic al registre d'usuari de l'aplicació per verificar el següent:

 - L'usuari té accés al projecte. Normalment, aquesta verificació es fa comprovant que l'usuari té la funció de seguretat **Administrador del projecte**.
 - L'usuari de l'aplicació Microsoft Project existeix i està configurat correctament.
 
3. Si aquest usuari no existeix, podeu crear un registre d'usuari nou. Seleccioneu **Usuaris nous**. Canvieu el formulari d'entrada a **Usuari de l'aplicació** i, a continuació, afegiu **l'identificador de l'aplicació**.

   ![Detalls de l'usuari de l'aplicació](media/applicationuserdetails.jpg)

4. Verifiqueu que s'hagi assignat la llicència correcta a l'usuari i que el servei estigui habilitat als detalls dels plans de servei de la llicència.
5. Verifiqueu que l'usuari pot obrir project.microsoft.com.
6. Verifiqueu a través dels paràmetres de projecte que el sistema assenyala a l'extrem del projecte correcte.
7. Verifiqueu que s'hagi creat l'usuari de l'aplicació de projecte.
8. Apliqueu les funcions de seguretat següents a l'usuari:

  - Usuari del Dataverse
  - Sistema del Project Operations
  - Sistema del projecte

## <a name="error-when-updating-the-work-breakdown-structure"></a>Es produeix un error quan s'actualitza l'estructura del desglossament del treball

Quan es fan una o més actualitzacions a l'estructura del desglossament del treball, els canvis finalment fallen i no es desen. S'ha produït un error a la quadrícula de planificació i s'ha especificat que "Els canvis recents que heu fet no s'han pogut desar".

### <a name="workaround"></a>Solució alternativa

1. Verifiqueu que s'hagi assignat la llicència correcta a l'usuari i que el servei estigui habilitat als detalls dels plans de servei de la llicència.
2. Verifiqueu que l'usuari pot obrir project.microsoft.com.
3. Verifiqueu que el sistema assenyala l'extrem del projecte correcte.
4. Verifiqueu que s'ha creat l'usuari de l'aplicació de projecte.
5. Apliqueu les funcions de seguretat següents a l'usuari:
  
  - Usuari del Dataverse o usuari base
  - Sistema del Project Operations
  - Sistema del projecte
  - Sistema d'escriptura doble del Project Operations (aquesta funció és necessària si esteu implementant l'escenari basat en el recurs/sense existències del Project Operations.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]