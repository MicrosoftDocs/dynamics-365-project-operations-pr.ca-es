---
title: Línies d'oportunitat basades en projectes
description: En aquest tema s'ofereix informació sobre el treball amb línies d'oportunitat basades en projectes.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181935"
---
# <a name="project-based-opportunity-lines"></a>Línies d'oportunitat basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Les línies d'oportunitat basades en projectes només estan disponibles a les oportunitats basades en projectes. Els registres d'oportunitat basada en projectes tenen el valor del camp **Tipus** definit com a **Basat en el treball**.

Les línies d'oportunitat basades en projectes són els elements de línia que s'enviaran al client mitjançant un projecte. No obstant, un projecte no es pot vincular a una línia d'oportunitat basada en projectes. Els projectes es poden vincular als elements de línia a partir de la fase **Oferta**, ja que normalment l'oportunitat es produeix en una de les primeres fases d'un acord. La determinació de quants projectes s'utilitzaran per lliurar el treball per al client és una decisió que es pren posteriorment en la fase de vendes. Utilitzeu la fase d'oportunitat per identificar els components discrets de lliurament per al client. Les decisions pel que fa al nombre real de projectes que s'utilitzen per lliurar aquests components es pot posposar fins que es conegui més informació sobre el treball.

A continuació es mostren els camps d'una línia d'oportunitat basada en projectes:

| **Camp** | **Ubicació** | **Descripció** | **Impacte descendent** |
| --- | --- | --- | --- |
| Tipus de producte | Pestanya General (ocult) | Aquest és un camp de conjunt d'opcions. Si teniu instal·lat el Dynamics 365 Operations, una de les opcions disponibles és **Servei basat en projectes**.  | El valor d'aquest camp es defineix com a **Servei basat en projectes** quan creeu la línia d'oportunitat basada en projectes des de la quadrícula de línies basades en projectes de l'oportunitat. <br> Si canvieu o anul·leu aquest valor, la funcionalitat del projecte no s'habilitarà als elements de línia basats en el projecte. |
| Oportunitat | Pestanya General | Aquest camp és només de lectura i fa referència al registre d'oportunitat principal al qual pertany aquest element de línia. | No hi ha cap impacte descendent d'aquest camp. |
| Nom | Pestanya General | Es tracta d'un camp de text editable que es pot utilitzar per donar una identitat breu a aquest element de línia | Aquest valor s'aprofita a la línia d'oferta quan creeu una oferta a partir d'aquesta oportunitat |
| Pressupost del client | Pestanya General | Aquest camp de moneda editable es pot utilitzar per fer el seguiment de l'import que el client està disposat a gastar en aquest element de línia. | Aquest valor s'aprofita al camp corresponent a la línia d'oferta quan creeu una oferta a partir d'aquesta oportunitat |
| Mètode de facturació | Pestanya General | Aquest camp editable té els següents valors:</br>- Temps i material</br>- Preu fix | Aquest valor s'aprofita al camp corresponent a la línia d'oferta quan creeu una oferta a partir d'aquesta oportunitat. Després de crear la línia d'oferta, el camp està bloquejat i no es pot canviar. Assigneu aquest valor de camp de la manera més exacta possible. Si heu de canviar el valor d'aquest camp a la línia d'oferta, suprimiu i torneu a crear la línia d'oferta. |
