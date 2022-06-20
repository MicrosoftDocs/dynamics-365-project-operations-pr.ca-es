---
title: 'Novetats de març de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de març de 2021 de Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fbdcb01117c39f879f80319b01d278c91a56e8f6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932928"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de març de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents Dynamics 365 Project Operations:

- Project Operations en entorn del Dataverse versió 4.8.0.91 
- Gestió de projectes i comptabilitat sobre Dynamics 365 Finance entorn versió 10.0.16 

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse


| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2133873 | S'ha corregit la visualització del símbol de moneda de **Preu de venda per unitat** a la quadrícula **Estimacions de despeses**. |
| Facturació i preus | 2174616 | Quan es guanya una oferta, es fa referència a la llista de preus personalitzada del contracte als detalls de la línia de contracte que es copien de l'oferta. |
| Administració d'oportunitats | 2167475 | Import de l'impost fix a la factura de correcció que s'ha originat d'una entrada real no facturada. |
| Administració d'oportunitats | 2176285 | L'import de l'impost no s'ha de copiar dels detalls del contracte de vendes/línia d'oferta als detalls del contracte de cost/línia d'oferta. |
| Administració d'oportunitats | 2188079 | No s'ha de crear una regla de facturació dividida per als contractes que no estiguin basats en treball. |
| Planificació i seguiment | 2125274 | Atribut **Assignació d'escriptura doble de projecte** per a **Assignació de data d'inici de projecte** actualitzat de **msdyn\_taskearlieststart** a **msdyn\_actualstart**. |
| Planificació i seguiment | 2138853 | La funció de còpia del projecte s'actualitza per garantir que les línies d'estimació de despeses que fan referència a tasques es copien al projecte de destinació. |
| Planificació i seguiment | 2154306 | S'han corregits els problemes amb la supressió de les estimacions de despeses al Project Operations per a escenaris basats en recursos. |
| Planificació i seguiment | 2173259 | Funció de còpia del projecte actualitzada per assegurar-se que no es mostra el missatge d'error **S'està copiant l'estructura de desglossament del treball (WBS)** en certs escenaris. |
| Temps i despesa | 2148910 | S'ha corregit el problema de visualització a la pàgina **Edita l'entrada** a la quadrícula **Entrada de temps**. |
| Temps i despesa | 2159798 | Controls ajustats per garantir que les entrades de despeses aprovades no es poden editar. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Gestió de projectes i comptabilitat sobre Dynamics 365 Finance

Per obtenir més informació, vegeu [Novetats de gener de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions financeres i d'operacions, consulta [Actualitzacions reguladores](/dynamics365/finance/localizations/regulatory-updates). Una altra manera d'obtenir informació sobre les actualitzacions reglamentàries és iniciar sessió als LCS i visualitzar les actualitzacions reglamentàries planificades mitjançant l'eina de cerca de problemes. La cerca de problemes us permet cercar per país, tipus de funció i llançament.


[!INCLUDE[footer-include](../includes/footer-banner.md)]