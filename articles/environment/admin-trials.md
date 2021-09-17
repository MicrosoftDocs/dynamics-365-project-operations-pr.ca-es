---
title: Registre per a les proves del Project Operations
description: En aquest tema es proporciona informació sobre com implementar una prova del Dynamics 365 Project Operations.
author: ruhercul
ms.date: 08/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e9c0d81591061f0ff01200dd5fd634a4a9ff31e4
ms.sourcegitcommit: 0e5de344f2040075ba431918a4499a80510458d9
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/25/2021
ms.locfileid: "7418445"
---
# <a name="sign-up-for-project-operations-trials"></a>Registre per a les proves del Project Operations 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense existències, implementació bàsica: tracte de facturació proforma i Project Operations per a escenaris amb existències/basats en producció_ 

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

En aquest tema s'explica com subscriure's a l'oferta per a associats de la versió preliminar i implementar un entorn del Dynamics 365 Project Operations.

Amb la nova versió de prova de Project Operations, podeu implementar automàticament qualsevol dels tres escenaris d'implementació admesos completant un qüestionari que recomana el millor mètode d'implementació. Aquest tema proporciona informació sobre com:

- Bescanviar l'oferta de prova.
- Iniciar el proveïment.
- Configurar l'escriptura doble.
- Més informació sobre el Project Operations. 

A la taula següent es donen els detalls de la nova oferta de prova.

| **Element de l'oferta**               | **Detalles**                                  |
|------------------------------|----------------------------------------------|
| Tipus d'oferta                   | Aquest tipus d'oferta és Client potencial administrador per tal que es requereixi un administrador d'inquilins per al bescanvi. |
| Ús d'ofertes                    | Una vegada per inquilí                          |
| Durada de l'oferta               | 30 dies naturals                             |
| Bescanvis per inquilí       | 1                                            |
| Nombre d'usuaris              | 25                                           |
| Extensió                    | 1 extensió, 30 dies naturals               |
| Nombre d'entorns de prova | 3                                            |


## <a name="admin-trial-details"></a>Detalls de la versió de prova d'administració
A la taula següent es donen els detalls de la versió de prova i la manera com s'apliquen a cada tipus d'implementació.

| **Element**                      | **Bàsica**                                     | **Materials que no estan en existències** | **Materials en existències** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Dades de configuració proporcionades           | Sí                                          | Sí                       | Sí (USSI)            |
| Dades transaccionals            | No                                           | No                        | No                    |
| Temps de proveïment en minuts  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Requisits previs
Els requisits següents són necessaris per implementar una prova del Dynamics 365 Project Operations.

- Registrar-se per a la [Versió preliminar de prova del Dynamics 365 Project Operations](https://www.aka.ms/try-po).
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.

> [!IMPORTANT]
> Només ha de dur a terme aquesta tasca una persona de l'organització, l'administrador d'inquilins. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations: versió preliminar de prova 

Abans de començar, inicieu la sessió en un navegador amb el compte de treball de l'usuari a l'inquilí on voleu obtenir la versió preliminar del Project Operations.

1. Bescanvieu el primer codi d'oferta, **Dynamics 365 Project Operations: versió preliminar de prova** enganxant-lo a l'URL del navegador.

    ![Bescanviar l'oferta](./media/16RedeemFirstOfferNew.png)

2. Confirmeu la comanda.

    ![Confirmeu la comanda](./media/17ConfirmOrderNew.png)

  Veureu que l'oferta de confirmació s'ha bescanviat correctament.

   ![Confirmació](./media/18OrderConfirmationNew.png)

  Se us redirigirà al [centre d'administració del Power Platform](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Qüestionari i proveïment

1.  Aneu al [centre d'administració del Power Platform](https://admin.powerplatform.com/projectoperationstrial) i empleneu el qüestionari.  
2.  Reviseu el tipus d'implementació recomanat i seleccioneu **Comença la instal·lació** per iniciar el proveïment.
3.  Reviseu les condicions i, a continuació, seleccioneu **Inicia**.

   Un cop començat el proveïment, se us redirigirà a la llista d'entorns del centre d'administració del Power Platform. Mentre s'està proveint, l'estat del vostre entorn és **PrepararingInstance**.
 
  Un cop completat el proveïment, l'estat del vostre entorn és **Preparat**.
 
4.  Quan el proveïment s'hagi completat, seleccioneu l'adreça URL respectiva del Microsoft Dataverse i les adreces URL de les aplicacions de Finance and Operations per validar la implementació.

## <a name="demo-data-installation"></a>Instal·lació de dades de demostració

Utilitzeu els enllaços següents per accedir als paquets de dades de demostració tant per a materials que no estan en existències com per a escenaris d'implementació bàsica. 
- [Dades de demostració de materials que no estan en existències](resource-apply-pro-setup-config-data.md)
- [Dades de demostració bàsiques](lite-apply-demo-setup-config-data.md)

## <a name="configuring-dual-write"></a>Configuració de l'escriptura doble
Per a les implementacions de materials que no estan en existències, configureu les assignacions d'escriptura doble. Per obtenir més informació, vegeu [Versions d'assignació amb doble escriptura al Project Operations](resource-dual-write-maps.md).

## <a name="assign-licenses"></a>Assignar llicències

Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.

1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als vostres usuaris.

   ![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

   ![Assignar llicències](./media/15AssignLicenses.png)

3. Verifiqueu que la llicència de la versió preliminar del **Dynamics 365 Project Operations** estigui seleccionada i, a continuació, seleccioneu **Desa els canvis**.

## <a name="additional-resources"></a>Recursos addicionals

Els recursos següents proporcionen instruccions útils a l'hora de començar a utilitzar el Project Operations:

- [Sèrie de vídeos: descripció general del Project Operations, anàlisi de característiques i full de ruta](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Determinació del tipus d'implementació](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Preguntes freqüents

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Què he de fer si necessito ALM o ELM per al meu entorn d'aplicacions de Finance and Operations?

- Per als associats que requereixen capacitats completes de gestió del cicle de vida de l'entorn, consulteu la [Sol·licitud de llicència d'espai aïllat per a associats](https://experience.dynamics.com/requestlicense) per revisar l'oferta nova per a associats. 
- Per als associats que cerquen més informació sobre els Drets d'ús intern, vegeu [Avantatges al núvol i en programari dels Drets d'ús intern (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Puc ampliar la versió de prova passats els 30 dies?
Per ampliar la versió de prova, seguiu els passos següents.

1. Al **centre d'administració del Microsoft 365**, aneu a **Facturació** > **Els vostres productes**.
2. Seleccioneu **Dynamics 365 Project Operations (CE): versió preliminar de prova**.
3. A **Data de caducitat**, seleccioneu **Amplia la data**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Puc actualitzar des de la implementació bàsica a la implementació d'escenari basat en recursos/sense existències?
Actualment no s'admet l'actualització d'un entorn des d'una implementació bàsica a una implementació sense existències.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Puc accedir a Lifecycle Services (LCS) per als meus entorns de Finance?  
No. Per a aquestes proves, la implementació es gestiona a través del Centre d'administració del Power Platform. L'accés a l'entorn de Finance està restringit.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Puc instal·lar la meva versió de prova en un entorn existent?
Si teniu un entorn existent, se us permetrà instal·lar la implementació bàsica en un entorn de vendes existent del Dataverse des del Centre d'administració del Power Platform.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
