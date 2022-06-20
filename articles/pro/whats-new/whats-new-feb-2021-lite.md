---
title: Novetats del febrer del 2021 - Implementació bàsica del Project Operations
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de febrer de 2021 de la implementació lite d'operacions del projecte.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 329bc31ad4c0958fe60e73b257e6b4c262bb60f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914022"
---
# <a name="whats-new-february-2021---project-operations-lite-deployment"></a>Novetats del febrer del 2021 - Implementació bàsica del Project Operations

Aquest article s'aplica als components i versions següents Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.7.0.95

## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| **Facturació i preus** | 2053736 | Ara, els detalls de la línia de factura estan accessibles anant a **Factura** > **Informació relacionada**. |
| **Facturació i preus** | 2122613 | Les accions **Activa** i **Desactiva** s'han eliminat de les entitats de l'associació **Llista de preus**. |
| **Facturació i preus** | 2128606 | S'ha resolt el problema amb **ullReferenceException** al complement **GetEstimatesForProject**. |
| **Implementació i configuració** | 2140569 | La solució del projecte no pot estar instal·lada als entorns d'equip del Dataverse. |
| **Implementació i configuració** | 2086991 | Localització de la personalització restringida dels recursos web. |
| **Administració d'oportunitats** | 2136794 | Visualitzeu el missatge d'error correcte quan el procés **Confirmació de la factura** o **Marca la factura com a pagada** fallen. |
| **Administració d'oportunitats** | 2146376 | L'import de l'impost corregit en un valor real no facturable es crea a partir de la confirmació de la factura. |
| **Planificació i seguiment de projectes** | 2099879 | La implementació de l'entorn del Dataverse ha de crear una categoria de transacció per defecte amb un identificador estàtic i no generar-ne aleatòriament un per entorn. |
| **Planificació i seguiment de projectes** | 2128577 | S'han corregit els privilegis d'usuari del Project Service per actualitzar la categoria de transaccions en una assignació de recursos. |
| **Planificació i seguiment de projectes** | 2164035 | S'han corregit problemes amb la funció **Copia el projecte**. |
| **Entrada de temps** | 2129161 | S'apliquen restriccions més ajustades per garantir que els usuaris no poden canviar ni actualitzar una entrada de temps enviada o aprovada. |
| **Entrada de temps** | 2103572 | La aprovació de temps per a entrades de tempos que no són de projecte no pot estar cercant funció d'aprovador de projecte. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]