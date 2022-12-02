---
title: 'Novetats de juny de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juny de 2021 del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd745107fa6d50882ebea302d3d2ae0de21b79ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028163"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juny de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents del Dynamics 365 Project Operations:

- Project Operations en un entorn del Dynamics 365 Dataverse, versió 4.11.0.156 o 4.11.0.164.
- Administració de projectes i comptabilitat en entorns d'aplicacions de finances i operacions versió 10.0.19.

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Capacitat de suprimir [línies de proposta de factura del projecte per a escenaris d'ajustament](../invoicing/correct-project-invoice-proposals.md).
- Les línies de despesa desglossades reflecteixen els noms de subcategoria a l'informe de despeses [Informes de despeses nous (noves característiques)](../expense/expense-reports-reimagined.md#new-features).
- El mètode de pagament està disponible a la subfinestra de despeses noves quan creeu una despesa nova.
- Disponibilitat general de les API de planificació de projectes. Aquesta nova funcionalitat permet als clients dur a terme les operacions de programació per a la creació, actualització i supressió en tasques de projectes, assignacions de recursos, dependències de tasques i registres de membres de l'equip del projecte. Per obtenir més informació, vegeu [Utilitzar les API de planificació de projectes per realitzar operacions amb entitats de planificació](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations. 

Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Project Operations al Dataverse i de les aplicacions de finances i operacions. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu veure la versió activa de l'assignació a la pàgina **Escriptura doble**, a la columna **Versió**. Per activar una versió nova de l'assignació, seleccioneu les **Versions de l’assignació de taules**, seleccioneu la versió més recent i deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema relacionat amb l'inici de l'assignació, seguiu les instruccions de la secció [Problema Falten columnes de la taula a les assignacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de solució de problemes de l'escriptura doble.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2281417 | S'ha corregit el problema relacionat amb l'error de l'acció de creació automàtica de factures mitjançant la planificació de factures. |
| Facturació i preus | 2287835 | S'ha millorat el rendiment de la confirmació de factures. |
| Administració d'oportunitats | 2222555 | La imputabilitat de les estimacions dels materials s'ha de copiar correctament als detalls de la línia d'oferta quan s'utilitza **Importa des de l'estimació del projecte**. |
| Administració d'oportunitats | 2223427 | Les personalitzacions es permeten ara per a l'acció **GenerateRetainersFromRetainerScheduleOptions**. |
| Administració d'oportunitats | 2277528 | S'ha corregit el càlcul de valors de fites de facturació per a les línies de contracte de projectes amb diversos clients. |
| Planificació i seguiment de projectes | 2226110 | S'ha corregit el problema intermitent amb la funció **Genera el requisit** a la quadrícula **Equip del projecte**. |
| Planificació i seguiment de projectes | 2208109 | Els usuaris no poden crear un projecte en una moneda amb tasques relacionades en una altra moneda. |
| Planificació i seguiment de projectes | 2258228 | S'ha actualitzat la llista de camps que es poden modificar amb les entitats **Planificació** que utilitzen l'API de planificació. |
| Planificació i seguiment de projectes | 2293989 | La llengua i la configuració regional correctes s'han de passar a la quadrícula **Tasques del projecte**. |
| Administració de recursos | 2220493 | S'ha corregit l'experiència de l'usuari a la quadrícula **Tasca** quan es marca ràpidament una sol·licitud de recurs com a completada. |
| Administració de recursos | 2330496 | S'ha corregit el problema de càrrega del **Tauler de planificació**. (L'actualització de qualitat està disponible a la versió 4.11.0.164) |
| Temps i despesa | 2194431 | La quadrícula **Entrada de temps** ha de tenir l'inici de la setmana definit igual que a la **Configuració del sistema**. |
| Temps i despesa | 2277311 | Després de suprimir el valor d'una cel·la a la quadrícula **Entrada de temps**, el cursor es queda a la quadrícula. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | Les **Notes de formulari** i la **Configuració del formulari** no es mostren a la **Configuració de l'administració de projectes** a Entitats jurídiques del Finance integrades amb el Project Operations. |
| Administració i comptabilitat de projectes | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | La descripció per defecte per a l'IVA està en blanc quan **Tipus de publicació** = **Impost sobre les vendes** per als vals de la factura del projecte. |
| Administració i comptabilitat de projectes | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Les transaccions dobles es publiquen quan s'utilitza la facturació basada en tasques al Dataverse amb la integració del Project Operations. |
| Administració i comptabilitat de projectes | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | El percentatge completat en el reconeixement d'ingressos no és correcte mentre s'utilitza la integració del Project Operations. |
| Administració i comptabilitat de projectes | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | L'acumulació d'ingressos es duplica en una factura de proveïdor pendent en un escenari integrat del Project Operations. |
| Administració i comptabilitat de projectes | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | No es pot publicar el llibre diari d'integració quan la regla de perfil d'ingressos s'ha definit com a configuració de **Grup**. |
| Administració i comptabilitat de projectes | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | No es pot publicar una factura de compra per a comandes de compra de projectes que tenen línies amb diverses unitats de mesura. |
| Administració i comptabilitat de projectes | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | La mesura financera per defecte d'un projecte no es pot actualitzar amb l'entitat de dades **V2** dels projectes. |
| Administració i comptabilitat de projectes | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | El procés per lots per crear estimacions de projectes triga massa temps a completar-se. |
| Administració i comptabilitat de projectes | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | En suprimir un contracte, se suprimeix també l'adreça associada al client. |
| Viatge i despesa | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | La condició de flux de treball d'aprovació de l'informe de despeses no s'avalua correctament. |
| Viatge i despesa | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | La norma de l'informe de despeses no avalua correctament l'identificador del projecte. |
| Viatge i despesa | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | L'acció **Divideix a personal per a les transaccions de despeses entre empreses** no funciona correctament. |
| Viatge i despesa | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Les justificacions de les línies d'informe de despeses se suprimeixen accidentalment quan se suprimeixen determinats requisits de viatge. Això passa quan el recID de l'informe de despeses i el requisit de viatge són iguals. |
| Viatge i despesa | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Hi ha un problema a l'aplicació mòbil de despeses quan el camp **Identificador del projecte** és obligatori a les normes de l'informe de despeses. |
| Viatge i despesa | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Les despeses entre empreses associades a un projecte no es poden editar. En lloc d'això, es mostrar el missatge d'error següent: "Referència d'objecte no definida com a instància d'un objecte". |
| Viatge i despesa | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Quan l'informe de despeses es publica, es mostren la moneda i l'import incorrectes al subllibre bancari. |
| Viatge i despesa | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | S'han fet millores a la característica *Suprimeix les transaccions de targetes de crèdit*.  |
| Viatge i despesa | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | L'impost de vendes inclòs en un informe de despeses no es calcula de manera coherent quan s'especifica una moneda d'informe diferent en una entitat legal. |
| Viatge i despesa | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | El rendiment es veu afectat quan s'afegeix una nova despesa d'efectiu de viatge. |
| Viatge i despesa | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Les regles de la norma de despeses no s'activen en un informe de despeses. |
| Viatge i despesa | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | En carregar una categoria compartida nova amb el marc d'administració de dades, se suprimeixen totes les subcategories de totes les categories compartides. |
| Viatge i despesa | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Quan creeu una línia de despeses i seleccioneu una categoria, es mostra el missatge d'error següent: "La combinació del DOM del grup d'impostos sobre les vendes i l'STD del grup d'impostos sobre les vendes d'articles no és vàlida". |
| Viatge i despesa | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Hi ha problemes de sincronització a l'aplicació mòbil de despeses. |
