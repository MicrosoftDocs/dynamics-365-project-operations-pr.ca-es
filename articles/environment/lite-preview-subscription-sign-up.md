---
title: Registre per obtenir una subscripció de versió preliminar
description: "En aquest tema es proporciona informació sobre com subscriure's i implementar la implementació bàsica del Project Operations: acord a facturació proforma."
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948759"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Registrar-se per obtenir una subscripció de versió preliminar per a la implementació bàsica: acord a facturació proforma

En aquest tema s'explica com subscriure's a l'oferta per a associats de versió preliminar i implementar la implementació bàsica del Dynamics 365 Project Operations: acord a facturació proforma.

> [!NOTE]
> Aquest procés canviarà en pròximes versions del Project Operations.

## <a name="prerequisites"></a>Requisits previs

- Rebreu un correu electrònic que us convidarà a participar a la versió preliminar. Podeu sol·licitar una versió preliminar al [lloc web del Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure.
- L'usuari que implementa la versió preliminar necessitarà un número de telèfon i una targeta de crèdit vàlida. Durant el registre, no tindreu càrrecs a la targeta durant sis mesos. Després de sis mesos, heu de cancel·lar la subscripció. 
- Reviseu tots els termes i condicions.

## <a name="subscribe"></a>Subscripció

Quan rebeu una aprovació de [sol·licitud de versió preliminar](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), rebreu dues ofertes de Microsoft per correu electrònic. Aquestes ofertes us permeten implementar la versió preliminar del Project Operations:

- Prova de versió preliminar del Dynamics 365 Customer Service: codi d'ús individual
- Dynamics 365 Project Operations: prova de versió preliminar

### <a name="dynamics-365-customer-service-paid-offer"></a>Oferta de pagament del Dynamics 365 Customer Service

1. Mitjançant una finestra del navegador InPrivate/d'incògnit, bescanvia el primer codi d'oferta per al Dynamics 365 Customer Service. Per registrar-vos al Customer Service, necessitareu:

- Un número de telèfon
- Una targeta de crèdit. Durant el registre, no tindreu càrrecs a la targeta durant sis mesos. Després de sis mesos, heu de cancel·lar la subscripció.
- Reviseu tots els termes i condicions.

2. Proporcioneu la vostra informació de contacte.

![Informació de contacte](./media/1ContactInformation.png)

3. Proporcioneu les dades del nou inquilí.

![Crear l'ID d'usuari](./media/2CreateUserID.png)

4. Verifiqueu la vostra identitat, deseu l'ID d'usuari nou i, a continuació, seleccioneu **Configura**.

![Desar la informació](./media/3SaveInfo.png)

5. Completeu el registre amb la targeta de crèdit i reviseu totes les condicions d'ús. 

![Completar la targeta de crèdit](./media/4CompleteCreditCard.png)

![Pagament amb targeta de crèdit](./media/5CreditCardCheckout.png)

![Desar la comanda](./media/6SaveOrder.png)

![Confirmació de la targeta de crèdit](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>Cancel·lar l'oferta empresarial del Dynamics 365 Customer Service

L'oferta empresarial del Dynamics 365 Customer Service es proporciona de manera gratuïta durant sis mesos. L'oferta es renovarà pel preu complet al final del període de sis mesos. Per cancel·lar-la abans de la data d'inici de la renovació, heu de completar les instruccions següents. 

> [!NOTE]
> Després de completar aquests passos, ja no podreu utilitzar l'entorn de versió preliminar pública del Project Operations.

1. Aneu al [Portal d'administració](https://admin.microsoft.com/) i, a **Facturació**, seleccioneu **Els meus productes**.

![Portal d'administració, pàgina Els meus productes](./media/8AdminPortal.png)

2. Seleccioneu l'**oferta empresarial del Dynamics 365 Customer Service**.

![Cancel·lar la subscripció](./media/9CancelSubscription.png)

3. Seleccioneu **Configuració** > **Accions** > **Cancel·la la subscripció**.
4. Al formulari **Cancel·lació de subscripcions**, introduïu informació als camps obligatoris.
5. Seleccioneu **Cancel·la** > **Subscripció.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations: prova de versió preliminar

1. Bescanvieu la segona oferta, la prova del Dynamics 365 Project Operations amb l'adreça URL proporcionada al correu electrònic de benvinguda.

![Bescanviar l'oferta 2](./media/10RedeemOffer2.png)

2. Verifiqueu que heu iniciat la sessió com a l'usuari que pertany a la mateixa organització que s'ha subscrit mitjançant el primer codi d'oferta i, a continuació, continueu amb el bescanvi de l'oferta. 
3. Seleccioneu **Sí, afegeix-ho al meu compte**.

![Afegir al compte](./media/11AddToAccount.png)

![Pantalla Prova-ho ara](./media/12TryNow.png)

![Detalls de la comanda](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal de l'Office 365 de l'organització per completar els passos següents.

1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.

![Pàgina principal del centre d'administració](./media/14AdminPortal.png)

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

![Assignar llicències](./media/15AssignLicenses.png)

3. Verifiqueu que s'hagi seleccionat la llicència **Customer Service Enterprise** i **Project Operations** i seleccioneu **Desa els canvis**.

## <a name="create-a-new-cds-environment"></a>Crear un entorn nou del CDS

Proveïu d'un nou entorn d'implementació del CDS del Project Operations seguint les instruccions del tema [Model d'implementació del CDS](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>Instal·lar una configuració del CDS i configurar les dades de demostració

Instal·leu la configuració del CDS i configureu les dades de demostració seguint les instruccions del tema [Aplicar la configuració de la demostració i les dades de configuració](lite-apply-demo-setup-config-data.md).
