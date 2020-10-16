---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948762"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest tema s'explica com subscriure's a l'oferta de versió preliminar/associats i implementar l'entorn del Project Operations per a escenaris de recursos/sense existències.

## <a name="prerequisites"></a>Requisits previs

- Rebreu un correu electrònic que us convidarà a participar a la versió preliminar. Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.
- La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn. Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar. L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.

## <a name="subscribe"></a>Subscripció

Quan s'aprovi la [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu dues ofertes de Microsoft per correu electrònic. Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:

- Dynamics 365 Project Operations: prova de versió preliminar
- Prova de versió preliminar del Dynamics 365 for Finance and Operations.

> [!IMPORTANT]
> Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: prova de versió preliminar

1. Bescanvieu la primera oferta, **Prova del Dynamics 365 Project Operations**, amb l'adreça URL proporcionada al correu electrònic de benvinguda.

![Primera oferta](./media/1FirstOffer.png)

2. Verifiqueu que heu iniciat la sessió com a l'usuari que pertany a l'organització que se subscriurà el servei.
3. Continueu amb el bescanvi de l'oferta. 
4. Seleccioneu **Sí, afegeix-ho al meu compte**.

![Bescanviar l'oferta](./media/2RedeemFirstOffer.png)

![Confirmar l'oferta](./media/3ConfirmFirstOffer.png)

![Oferta bescanviada](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Prova de versió preliminar del Dynamics 365 Finance

Repetiu els mateixos passos amb la segona oferta del correu electrònic de benvinguda.

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal de l'Office 365 de l'organització per completar els passos següents.

1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.

![Portal d'administració de l'Office](./media/5OfficeAdminPortal.png)

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

![Assignar llicències](./media/6AssignLicenses.png)

3. Verifiqueu que s'hagi seleccionat la llicència del Project Operations i seleccioneu **Desa els canvis**. 

> [!NOTE]
> L'oferta de prova del Finance no s'ha d'assignar a un usuari.

## <a name="start-a-new-project-in-lcs"></a>Iniciar un projecte nou al LCS

Creeu un projecte nou del LCS tal com es descriu al tema [Iniciar un projecte nou al LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Addició d'una subscripció a l'Azure a un projecte del LCS

Per completar aquesta tasca, seguiu els passos del tema [Afegir una subscripció de l'Azure al projecte del LCS](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementar l'entorn de demostració del Finance amb el Project Operations per a escenaris de recursos/sense existències

Seguiu les instruccions del tema [Proveir un nou entorn](resource-provision-new-environment.md) per completar la implementació. Utilitzeu el tipus d'implementació [entorn de demostració](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) per a la versió preliminar.

## <a name="install-cds-setup-and-configuration-data"></a>Configuració de la instal·lació del CDS i dades de configuració

Instal·leu les dades instal·lació i les dades de configuració del CDS com es descriu al tema [Configurar i aplicar les dades de configuració al Common Data Service](resource-apply-pro-setup-config-data.md).

