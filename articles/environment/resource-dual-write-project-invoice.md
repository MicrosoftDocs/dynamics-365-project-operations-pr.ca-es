---
title: Integració de la factura del projecte
description: Aquest tema proporciona informació sobre la integració de doble escriptura del Project Operations per a factures de clients.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955707"
---
# <a name="project-invoice-integration"></a>Integració de la factura del projecte

Aquest tema proporciona informació sobre la integració de doble escriptura del Project Operations per a factures de clients.

Al Project Operations, l'administrador del projecte administra els treballs pendents de facturació del projecte i crea una factura proforma per al client al Microsoft Dataverse. En funció d'aquesta factura proforma, el responsable del compte a cobrar o el comptable del projecte crea una factura orientada al client. La integració amb doble escriptura garanteix que els detalls de la factura proforma se sincronitzin amb les aplicacions del Finance and Operations. Un cop publicada la factura orientada al client, el sistema actualitza els valors reals del projecte rellevants al Dataverse amb el detall de comptabilitat. El gràfic següent proporciona una visió general conceptual d'alt nivell d'aquesta integració.

   ![Integració de la factura del projecte](./media/DW5Invoicing.png)

Quan l'administrador del projecte confirma la factura proforma al Dataverse, la informació de la capçalera de la factura proforma se sincronitza amb les aplicacions del Finance and Operations amb l'assignació de taules de doble escriptura **Proposta de factura del projecte V2 (factures)**. Es tracta d'una integració única del Dataverse a les aplicacions del Finance and Operations. La creació o supressió de propostes de factura del projecte directament a les aplicacions del Finance and Operations no estan admeses.

La confirmació de la factura al Dataverse també activa la lògica empresarial per crear registres relacionats amb la facturació a l'entitat **Valors reals**. Aquests registres se sincronitzen amb el Finance and Operations mitjançant l'assignació de taules de doble escriptura **Valors reals d'integració del Project Operations (msdyn\_actuals).** Per obtenir més informació, vegeu [Estimacions i valors reals del projecte](resource-dual-write-estimates-actuals.md). 

El procés periòdic **Importa una còpia intermèdia d'un formulari** crea les línies de proposta de factura del projecte. Aquest procés es basa en els detalls dels valors reals de vendes facturats a la taula **Còpia intermèdia dels valors reals**. Per obtenir més informació, vegeu [Administració de propostes de factura del projecte](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
