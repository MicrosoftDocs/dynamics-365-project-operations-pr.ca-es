---
title: Solucionar problemes de funcionament a la quadrícula de tasques
description: Aquest article proporciona la informació necessària per resoldre problemes quan es treballa a la quadrícula de tasques.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911032"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Solucionar problemes de funcionament a la quadrícula de tasques 


_**S'aplica a:** Project Operations per a escenaris basats en recursos/no mantinguts en existències, implementació bàsica: tracte de facturació proforma, Project for the web_

La quadrícula de tasques que utilitza el Dynamics 365 Project Operations és un iframe allotjat dins del Microsoft Dataverse. Com a resultat d'aquest ús, s'han de complir requisits específics per garantir el funcionament correcte de l'autenticació i l'autorització. En aquest article es descriuen els problemes comuns que poden afectar la capacitat de renderitzar la quadrícula o gestionar tasques a l'estructura del desglossament del treball (WBS).

Alguns problemes comuns són:

- La pestanya **Tasca** de la quadrícula Tasca és buida.
- Quan s'obre el projecte, el projecte no es carrega i la interfície d'usuari (IU) es col·loca al control giratori.
- Administració de privilegis per al **Project for the Web**.
- Els canvis no es desen quan creeu, actualitzeu o suprimiu una tasca.

## <a name="issue-the-task-tab-is-empty"></a>Problema: la pestanya Tasca és buida

### <a name="mitigation-1-enable-cookies"></a>Mitigació 1: habilitar les galetes

El Project Operations requereix que s'habilitin les galetes de tercers per representar l'estructura del desglossament del treball. Quan les galetes de tercers no estan habilitades, en lloc de veure les tasques, veureu una pàgina en blanc quan seleccioneu la pestanya **Tasques** a la pàgina **Projecte**.

Per als navegadors Microsoft Edge o Google Chrome, a continuació s'explica com s'actualitza la configuració del navegador per habilitar les galetes de tercers.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Obriu el navegador Microsoft Edge.
2. A la cantonada superior dreta, seleccioneu la **el·lipsi** (...) i, a continuació, seleccioneu **Configuració**.
3. A **Galetes i permisos del lloc**, seleccioneu **Galetes i dades del lloc**.
4. Desactiveu **Bloqueja les galetes de tercers**.
5. Actualitzeu el navegador. 

#### <a name="google-chrome"></a>Google Chrome

1. Obriu el navegador Chrome.
2. A la cantonada superior dreta, seleccioneu els tres punts verticals i, a continuació, seleccioneu **Configuració**.
3. A **Privades i seguretat**, seleccioneu **Galetes i altres dades dels llocs web**.
4. Seleccioneu **Permet totes les galetes**.
5. Actualitzeu el navegador. 

> [!NOTE]
> Si bloquegeu les galetes de tercers, totes les galetes i les dades de llocs d'altres llocs es bloquejaran, encara que el lloc estigui autoritzat a la vostra llista d'excepcions.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Mitigació 2: la validació de l'extrem PEX s'ha configurat correctament

El Project Operations requereix que un paràmetre de projecte faci referència a l'extrem del PEX. Aquest extrem es necessita per comunicar-se amb el servei que s'utilitza per representar l'estructura del desglossament del treball. Si el paràmetre no està habilitat, rebreu l'error "El paràmetre de projecte no és vàlid". Per actualitzar l'extrem PEX, seguiu els passos següents.

1. Afegiu el camp **extrem del PEX** a la pàgina **Paràmetres del projecte**.
2. Identifiqueu el tipus de producte que utilitzeu. Aquest valor s'utilitza quan es defineix l'extrem PEX. Després de recuperar-se, el tipus de producte ja està definit a l'extrem PEX. Conserveu aquest valor.
3. Actualitzeu el camp amb el següent valor: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. La taula següent proporciona el paràmetre de tipus que s'ha d'utilitzar segons el tipus de producte.

      | **Tipus de producte**                     | **Tipus paràmetre** |
      |--------------------------------------|--------------------|
      | Project for the Web a l'organització per defecte   | tipus=0             |
      | Project for the Web a l'organització anomenada CDS | tipus=1             |
      | Project Operations                   | tipus=2             |

4. Suprimiu el camp de la pàgina **Paràmetres del projecte**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Mitigació 3: inicia sessió a project.microsoft.com
Microsoft Edge Al navegador, obriu una pestanya nova, aneu a project.microsoft.com i inicieu la sessió mitjançant la funció d'usuari que utilitzeu per accedir a les operacions del projecte.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Problema: el projecte no es carrega i la interfície d'usuari es troba atrapada en el control giratori

Per a l'autenticació, cal habilitar les finestres emergents per carregar la quadrícula Tasca. Si les finestres emergents no estan habilitades, la pantalla es quedarà bloquejada en la càrrega del control giratori. Al gràfic següent es mostra l'adreça URL amb una etiqueta emergent bloquejada a la barra d'adreces, la qual cosa fa que el control giratori es bloquegi en intentar carregar la pàgina. 

   ![Control giratori encallat i bloqueig de finestres emergents.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Mitigació 1: habilitar les finestres emergents

Quan el projecte es troba bloquejat al control giratori, és possible que les finestres emergents no estiguin habilitades.

#### <a name="microsoft-edge"></a>Microsoft Edge

Hi ha dues maneres d'habilitar les finestres emergents al navegador Edge.

1. Al navegador Edge, seleccioneu la notificació a la part superior dreta del navegador.
2. Seleccioneu **Permet sempre els missatges emergents de** l'entorn del Dataverse específic.
 
     ![Finestra de finestres emergents bloquejades.](media/enablepopups.png)

Com a alternativa, també podeu completar els passos següents.

1. Obriu el navegador Microsoft Edge.
2. A la part superior dreta, seleccioneu els **punts suspensius** (...), i, a continuació, seleccioneu **Configuració** > **Permisos de lloc** > **Finestres emergents i redireccions**.
3. Desactiveu **Finestres emergents i redireccions** per bloquejar les finestres emergents o activeu-ho per permetre les finestres emergents al dispositiu.
4. Quan habiliteu les finestres emergents, actualitzeu el navegador. 

#### <a name="google-chrome"></a>Google Chrome
1. Obriu el navegador Chrome.
2. Aneu a una pàgina en què les finestres emergents estiguin bloquejades.
3. A la barra d'adreces, seleccioneu **Finestres emergents bloquejades**.
4. Seleccioneu l'enllaç per a la finestra emergent que voleu veure.
5. Quan habiliteu les finestres emergents, actualitzeu el navegador. 

> [!NOTE]
> Per veure sempre les finestres emergents del lloc, seleccioneu **Permet sempre les finestres emergents i les redireccions del [lloc]** i, a continuació, seleccioneu **Fet**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Problema 3: administració de privilegis per al Project for the Web

El Project Operations es basa en un servei de planificació extern. El servei requereix que un usuari tingui diverses funcions assignades que li permetin llegir i escriure a entitats relacionades amb el sistema WBS. Aquestes entitats inclouen tasques de projecte, assignacions de recursos i dependències de tasques. Si un usuari no pot representar el sistema WBS quan va a la pestanya **Tasques**, probablement és perquè **Project** for **Project Operations** no s'ha habilitat. Un usuari pot rebre un error de funció de seguretat o un error relacionat amb una denegació d'accés.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Mitigació 1: validar les funcions de seguretat d'usuari d'aplicació i usuari final

1. Aneu a **Configuració** > **Seguretat** > **Usuaris** > **Usuaris d'aplicació**.  

   ![Lector de l'aplicació.](media/applicationuser.jpg)
   
2. Feu doble clic al registre d'usuari d'aplicació per verificar:

     - L'usuari té accés al projecte. Podeu fer-ho comprovant que l'usuari té la funció de seguretat **Administrador de projecte**.
     - L'usuari de l'aplicació Microsoft Project existeix i està configurat correctament.
 
3. Si aquest usuari no existeix, creeu un registre d'usuari nou. 
4. Seleccioneu **Usuaris nous**, canvieu el formulari d'entrada per **Usuari d'aplicació** i, a continuació, afegiu **Identificador de l'aplicació**.

   ![Detalls de l'usuari de l'aplicació.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Problema 4: els canvis no es desen quan creeu, actualitzeu o suprimiu una tasca

Quan feu una o més actualitzacions al sistema WBS, els canvis fallen i no es desen. Es produeix un error a la quadrícula de planificació amb un missatge que indica que "Els canvis recents que heu fet no s'han pogut desar".

### <a name="mitigation-1-validate-the-license-assignment"></a>Mitigació 1: validar l'assignació de llicència

1. Verifiqueu que s'hagi assignat la llicència correcta a l'usuari i que el servei estigui habilitat als detalls dels plans de servei de la llicència.  
2. Verifiqueu que l'usuari pot obrir **project.microsoft.com**.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Mitigació 2: configuració de la validació de l'usuari d'aplicació Projecte
1. Verifiqueu que s'ha creat l'usuari d'aplicació Projecte.
2. Apliqueu les funcions de seguretat següents a l'usuari:
  
  - Usuari del Dataverse o usuari base
  - Sistema del Project Operations
  - Sistema del projecte
  - Sistema d'escriptura doble del Project Operations. Aquesta funció és necessària per a l'escenari d'implementació basada en recursos/no mantinguda en existències del Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
