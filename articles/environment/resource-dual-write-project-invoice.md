---
title: Integració de la factura del projecte
description: Aquest article proporciona informació sobre la integració de doble escriptura del Project Operations per a factures de clients.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029012"
---
# <a name="project-invoice-integration"></a>Integració de la factura del projecte

Aquest article proporciona informació sobre la integració de doble escriptura del Project Operations per a factures de clients.

Al Project Operations, l'administrador del projecte administra els treballs pendents de facturació del projecte i crea una factura proforma per al client al Microsoft Dataverse. En funció d'aquesta factura proforma, el responsable del compte a cobrar o el comptable del projecte crea una factura orientada al client. La integració amb doble escriptura garanteix que els detalls de la factura proforma se sincronitzin amb les aplicacions de finances i operacions. Un cop publicada la factura orientada al client, el sistema actualitza els valors reals del projecte rellevants al Dataverse amb el detall de comptabilitat. El gràfic següent proporciona una visió general conceptual d'alt nivell d'aquesta integració.

   ![Integració de la factura del projecte.](./media/DW5Invoicing.png)

Quan l'administrador del projecte confirma la factura proforma al Dataverse, la informació de la capçalera de la factura proforma se sincronitza amb les aplicacions de finances i operacions amb l'assignació de taules de doble escriptura **Proposta de factura del projecte V2 (factures)**. Es tracta d'una integració única del Dataverse a les aplicacions de finances i operacions. La creació o supressió de propostes de factura del projecte directament a les aplicacions de finances i operacions no estan admeses.

La confirmació de la factura al Dataverse també activa la lògica empresarial per crear registres relacionats amb la facturació a l'entitat **Valors reals**. Aquests registres se sincronitzen amb les finances i operacions mitjançant l'assignació de taules de doble escriptura, **Valors reals d'integració del Project Operations (msdyn\_actuals).** Per obtenir més informació, vegeu [Estimacions i valors reals del projecte](resource-dual-write-estimates-actuals.md). 

El procés periòdic **Importa una còpia intermèdia d'un formulari** crea les línies de proposta de factura del projecte. Aquest procés es basa en els detalls dels valors reals de vendes facturats a la taula **Còpia intermèdia dels valors reals**. Per obtenir més informació, vegeu [Administració de propostes de factura del projecte](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
