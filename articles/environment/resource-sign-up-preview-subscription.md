---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1b8c8982ede83191ce346e76718322d47abf0dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000424"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

En aquest tema s'explica com subscriure's a l'oferta de versió preliminar/associats i implementar l'entorn del Project Operations per a escenaris de recursos/sense existències.

## <a name="prerequisites"></a>Requisits previs

- Rebreu un correu electrònic que us convidarà a participar a la versió preliminar. Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.
- La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn. Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar. L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.

## <a name="subscribe"></a>Subscripció

Quan s'aprovi la [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu tres ofertes de Microsoft per correu electrònic. Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:

- Prova de versió preliminar del Dynamics 365 Project Operations (CRM)
- Office 365 Project Operations: prova de versió preliminar
- Dynamics 365 Finance: prova de versió preliminar

> [!IMPORTANT]
> Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Prova de versió preliminar del Dynamics 365 Project Operations (CRM) 

Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.

1. Redimiu el primer codi d'oferta, prova de versió preliminar del **Dynamics 365 Project Operations (CRM)** enganxant-lo a l'URL del navegador.

![Bescanviar l'oferta](./media/16RedeemFirstOfferNew.png)

2. Confirmeu la comanda.

![Confirmeu la comanda](./media/17ConfirmOrderNew.png)

Veureu que l'oferta de confirmació s'ha bescanviat correctament.

![Confirmació](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations: prova de versió preliminar

Repetiu els mateixos passos que amb el primer codi d'oferta. Assegureu-vos d'afegir el segon codi d'oferta amb el mateix compte d'usuari utilitzat amb el primer codi d'oferta.

### <a name="dynamics-365-finance-preview-trial"></a>Prova de versió preliminar del Dynamics 365 Finance

Repetiu els mateixos passos amb l'última oferta del correu electrònic de benvinguda.

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.

1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.

![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

![Assignar llicències](./media/15AssignLicenses.png)

3. Verifiqueu que heu seleccionat la llicència de la versió preliminar del **Dynamics 365 Project Operations (CRM)** i la versió preliminar de l'**Office 365** i seleccioneu **Desa els canvis**.

> [!NOTE]
> L'oferta de prova del Finance no s'ha d'assignar a un usuari.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un projecte nou al LCS

Creeu un projecte nou del LCS tal com es descriu al tema [Iniciar un projecte nou al LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Addició d'una subscripció a l'Azure a un projecte del LCS

Per completar aquesta tasca, seguiu els passos del tema [Afegir una subscripció de l'Azure al projecte del LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar l'entorn de demostració del Finance amb el Project Operations per a escenaris de recursos/sense existències

Seguiu les instruccions del tema [Proveir un nou entorn](resource-provision-new-environment.md) per completar la implementació. Utilitzeu el tipus d'implementació [entorn de demostració](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per a la versió preliminar. 

## <a name="install-cds-setup-and-configuration-data"></a>Configuració de la instal·lació del CDS i dades de configuració

Instal·leu les dades instal·lació i les dades de configuració del CDS com es descriu al tema [Configurar i aplicar les dades de configuració al Common Data Service](resource-apply-pro-setup-config-data.md).
Completeu aquest pas només després que s'hagi implementat l'entorn de demostració del Finance i que les dades de demostració del FO estiguin a punt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]