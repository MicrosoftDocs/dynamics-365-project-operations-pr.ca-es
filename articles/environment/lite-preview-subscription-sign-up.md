---
title: Registre per obtenir una subscripció de versió preliminar (bàsic)
description: "En aquest tema es proporciona informació sobre com subscriure's i implementar la implementació bàsica del Project Operations: acord a facturació proforma."
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175879"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registre per obtenir una subscripció de versió preliminar (bàsic) 

En aquest tema s'explica com subscriure's a l'oferta per a associats de versió preliminar i implementar la implementació bàsica del Dynamics 365 Project Operations: acord a facturació proforma.

> [!NOTE]
> Aquest procés canviarà en pròximes versions del Project Operations.

## <a name="prerequisites"></a>Requisits previs

- Rebreu un correu electrònic que us convidarà a participar a la versió preliminar. Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.
- Reviseu tots els termes i condicions.

## <a name="subscribe"></a>Subscripció

Quan rebeu una aprovació de [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu dues ofertes de Microsoft per correu electrònic. Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:

- Dynamics 365 Project Operations (CRM): prova de versió preliminar
- Office 365 Project Operations: prova de versió preliminar

> [!IMPORTANT]
> Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM): prova de versió preliminar 

Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.

1. Bescanvieu el primer codi d'oferta, **Dynamics 365 Project Operations (CRM): prova de versió preliminar** enganxant-lo a l'URL del navegador.

![Bescanviar l'oferta](./media/16RedeemFirstOfferNew.png)

2. Confirmeu la comanda.
![Confirmeu la comanda](./media/17ConfirmOrderNew.png)

Veureu que l'oferta de confirmació s'ha bescanviat correctament.

![Confirmació](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations: prova de versió preliminar

Repetiu els mateixos passos que amb el primer codi d'oferta. Assegureu-vos d'afegir el segon codi d'oferta amb el mateix compte d'usuari utilitzat amb el primer codi d'oferta.

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.


1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.

![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

![Assignar llicències](./media/15AssignLicenses.png)

3. Verifiqueu que s'hagin seleccionat les llicències **Versió preliminar del Dynamics 365 Project Operations (CRM)** i **Office 365 Project Operations: versió preliminar**. 
4. Seleccioneu **Desa els canvis**.

## <a name="create-a-new-cds-environment"></a>Crear un entorn nou del CDS

1. Proveïu d'un nou entorn d'implementació del CDS del Project Operations seguint les instruccions del tema [Model d'implementació del CDS](lite-deployment.md). Quan seleccioneu el tipus d'entorn, assegureu-vos d'utilitzar **Prova (basada en subscripció)**.
![Entorn nou](./media/19CreateEnvironment.png)

2. Seleccioneu l'opció **Habilita les aplicacions del Dynamics 365** i deixeu **Implementa aquestes aplicacions automàticament** en blanc.  
3. Seleccioneu **Desa** per crear l'entorn.

![Afegeix base de dades](./media/20CreateEnvironment1.png)

4. Després de crear l'entorn, instal·leu la solució **Microsoft Dynamics 365 Project Operations**. 

![Instal·lar la solució](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal·lar una configuració del CDS i configurar les dades de demostració

Instal·leu la configuració del CDS i configureu les dades de demostració seguint les instruccions del tema [Aplicar la configuració de la demostració i les dades de configuració](lite-apply-demo-setup-config-data.md).
