---
title: 'Novetats de febrer de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles en el llançament de febrer de 2021 del Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 41d7d7133652069ca3899db7f12e67e9ba531bcd3e36d67c3686a6b637b077d3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986794"
---
# <a name="whats-new-february-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de febrer de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

- Project Operations a l'entorn del Dataverse 4.7.0.95
- Administració de projectes i comptabilitat a l'entorn del Dynamics 365 Finance versió 10.0.16 

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| **Facturació i preus** | 2053736 | Ara, els detalls de la línia de factura estan accessibles anant a **Factura** > **Informació relacionada**. |
| **Facturació i preus** | 2122613 | Les accions **Activa** i **Desactiva** s'han eliminat de les entitats de l'associació **Llista de preus**. |
| **Facturació i preus** | 2128606 | S'ha resolt el problema amb **ullReferenceException** al complement **GetEstimatesForProject**. |
| **Implementació i configuració** | 2139346 | S'ha resolt el problema amb la importació de la solució **Dynamics365ProjectOperationsDualWrite** no administrada. |
| **Implementació i configuració** | 2140569 | La solució del projecte no pot estar instal·lada als entorns d'equip del Dataverse. |
| **Implementació i configuració** | 2086991 | Localització de la personalització restringida dels recursos web. |
| **Administració d'oportunitats** | 2136794 | Visualitzeu el missatge d'error correcte quan els processos **Confirmació de la factura** o **Marca la factura com a pagada** fallen. |
| **Administració d'oportunitats** | 2139330 | Si canvieu l'administrador del projecte en un projecte, no cal tornar a restablir l'empresa propietària al valor per defecte. |
| **Administració d'oportunitats** | 2146376 | L'import de l'impost corregit en un valor real no facturable es crea a partir de la confirmació de la factura. |
| **Planificació i seguiment de projectes** | 2099879 | La implementació de l'entorn del Dataverse ha de crear una categoria de transacció per defecte amb un identificador estàtic i no generar-ne aleatòriament un per entorn. |
| **Planificació i seguiment de projectes** | 2128577 | S'han corregit els privilegis d'usuari del Project Service per actualitzar la categoria de transaccions en una assignació de recursos. |
| **Planificació i seguiment de projectes** | 2164035 | S'han corregit problemes amb la funció **Copia el projecte**. |
| **Entrada de temps** | 2129161 | S'apliquen restriccions més ajustades per garantir que els usuaris no poden canviar ni actualitzar una entrada de temps enviada o aprovada. |
| **Entrada de temps** | 2103572 | La aprovació de temps per a entrades de tempos que no són de projecte no pot estar cercant funció d'aprovador de projecte. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance 

Per obtenir més informació sobre l'administració i la comptabilitat de projectes al Dynamics 365 Finance, vegeu [Novetats del gener de 2021 - Project Operations per a escenaris basats en recursos/sense existències](whats-new-jan-2021-resource-based.md) .


## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reglamentàries de les aplicacions del Finance and Operations, vegeu [Actualitzacions reglamentàries](/dynamics365/finance/localizations/regulatory-updates). Una altra manera de saber les actualitzacions reglamentàries és iniciar sessió als Lifecycle Services (LCS) i visualitzar les actualitzacions reglamentàries planificades mitjançant l'eina de cerca d'edicions. La cerca de problemes us permet cercar per país, tipus de funció i llançament.


[!INCLUDE[footer-include](../includes/footer-banner.md)]