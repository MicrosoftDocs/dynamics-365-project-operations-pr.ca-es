---
title: Integració de la factura del projecte
description: En aquest article s'ofereix informació sobre la integració de doble escriptura de Project Operations per a la facturació del client.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912090"
---
# <a name="project-invoice-integration"></a>Integració de la factura del projecte

En aquest article s'ofereix informació sobre la integració de doble escriptura de Project Operations per a la facturació del client.

Al Project Operations, l'administrador del projecte administra els treballs pendents de facturació del projecte i crea una factura proforma per al client al Microsoft Dataverse. En funció d'aquesta factura proforma, el responsable del compte a cobrar o el comptable del projecte crea una factura orientada al client. La integració de doble escriptura garanteix que els detalls de la factura proforma se sincronitzin amb les aplicacions de finances i operacions. Un cop publicada la factura orientada al client, el sistema actualitza els valors reals del projecte rellevants al Dataverse amb el detall de comptabilitat. El gràfic següent proporciona una visió general conceptual d'alt nivell d'aquesta integració.

   ![Integració de la factura del projecte.](./media/DW5Invoicing.png)

Després que el Gestor de projectes confirmi la factura proforma al Dataverse, la informació de la capçalera de la factura proforma se sincronitza amb les aplicacions Finances i Operacions mitjançant el mapa de la taula de doble escriptura, **proposta de factura del projecte V2 (factures)**. Es tracta d'una integració unireccional des de les aplicacions de Dataverse finances i operacions. No s'admet la creació o supressió de propostes de factures del projecte directament a les aplicacions Finances i Operacions.

La confirmació de la factura al Dataverse també activa la lògica empresarial per crear registres relacionats amb la facturació a l'entitat **Valors reals**. Aquests registres se sincronitzen amb Finances i operacions utilitzant l'assignació de taula de doble escriptura, **reals d'integració d'operacions del projecte (msdyn\_ reals).** Per obtenir més informació, vegeu [Estimacions i valors reals del projecte](resource-dual-write-estimates-actuals.md). 

El procés periòdic **Importa una còpia intermèdia d'un formulari** crea les línies de proposta de factura del projecte. Aquest procés es basa en els detalls dels valors reals de vendes facturats a la taula **Còpia intermèdia dels valors reals**. Per obtenir més informació, vegeu [Administració de propostes de factura del projecte](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
