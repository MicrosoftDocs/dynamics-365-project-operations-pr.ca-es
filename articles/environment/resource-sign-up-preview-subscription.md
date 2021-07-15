---
title: Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències
description: En aquest tema es proporciona informació sobre com registrar-se i implementar el Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334815"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Registrar-se a les subscripcions de versió preliminar del Project Operations per a escenaris de recursos/sense existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

En aquest tema s'explica com subscriure's a l'oferta de prova i implementar l'entorn del Project Operations per als escenaris basats en recursos/no mantinguts en existències.

## <a name="prerequisites"></a>Requisits previs
- L'usuari que implementa la versió preliminar ha de tenir drets d'administrador global a l'inquilí de l'Azure. Podeu crear un inquilí en bescanviar la primera oferta. 
- La implementació d'un entorn del Finance requereix una subscripció vàlida de l'Azure que es facturarà per entorn. Podeu utilitzar la subscripció existent de l'organització o utilitzar una [versió de prova de l'Azure](https://azure.microsoft.com/en-us/free/) per començar. L'entorn del CDS es proporcionarà gratuïtament durant un període de 30 dies limitat.

> [!IMPORTANT]
> Només cal que una persona de l'organització, l'administrador d'inquilins, realitzi aquesta tasca. Si no sou el subscriptor en aquesta versió, espereu fins que l'organització s'hagi registrat i hàgiu rebut les vostres credencials d'usuari.
> 
> Les proves són d'un sol ús a l'inquilí. Una versió de prova només es pot executar una vegada. Us recomanem que creeu un inquilí nou per a la versió de prova.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE): prova de versió preliminar 

Abans de començar, assegureu-vos que hàgiu iniciat la sessió en un navegador amb el compte laboral de l'usuari a l'inquilí on voleu la versió preliminar del Project Operations.

1. Bescanvieu el primer codi de l'oferta, **Dynamics 365 Project Operations**, aquí [Prova del Project Operations](https://aka.ms/try-po).
2. Confirmeu la comanda.

  Veureu que l'oferta de confirmació s'ha bescanviat correctament.

### <a name="dynamics-365-finance-preview-trial"></a>Prova de versió preliminar del Dynamics 365 Finance

Aneu a [Prova de versió preliminar del Dynamics 365 for Finance](https://aka.ms/trypoche) i repetiu els passos de la secció anterior amb l'oferta Registrar-se per obtenir un entorn allotjat al núvol.  

## <a name="assign-licenses"></a>Assignar llicències

> [!IMPORTANT]
> Necessitareu accés d'administrador al portal del Microsoft 365 de l'organització per completar els passos següents.

1. Aneu al [centre d'administració del Microsoft 365](https://portal.office.com/) per assignar les llicències als usuaris.

2. A la pàgina **Usuaris actius**, seleccioneu els usuaris als quals voleu assignar una llicència.

3. Verifiqueu que la llicència del **Dynamics 365 Project Operations** estigui seleccionat i seleccioneu **Desa els canvis**.

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
Completeu aquest pas només quan s'implementi l'entorn de demostració del Finance i les dades de demostració estiguin a punt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
