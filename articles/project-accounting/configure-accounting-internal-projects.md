---
title: Configuració de la comptabilitat per a projectes interns
description: Aquest tema proporciona informació sobre com configurar les pràctiques de comptabilitat per a projectes interns al Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012844"
---
# <a name="configure-accounting-for-internal-projects"></a>Configuració de la comptabilitat per a projectes interns

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Els projectes interns permeten a les empreses fer un seguiment del cost relacionat amb activitats que no es facturen a un client. Alguns exemples de projectes interns són:

- Desenvolupar un producte, com una aplicació mòbil, i fer un seguiment del cost associat al desenvolupament.
- Administrar el temps i les despeses prèvies a la venda. Aquest projecte intern previ a la venda es pot convertir més tard en un projecte facturable si es guanya l'oferta.

Qualsevol projecte no associat amb un contracte al Dynamics 365 Project Operations es tracta com a intern. Els perfils de cost i ingrés del projecte no s'utilitzen per determinar les regles de comptabilitat per al projecte. El cost intern del projecte sempre es comptabilitza amb els principis de beneficis i pèrdues. Els comptes del registre major per a les comptabilitzacions es defineixen a la pàgina **Configuració de comptabilització del registre major**.

- Les transaccions de temps es comptabilitzen carregant-les al compte **Cost** i pagant-les al compte **Assignació de nòmines**.
- Les transaccions de despeses es comptabilitzen carregant-les al compte **Cost** i pagant-les al compte **Compte de desplaçament per a despeses**.
- Les transaccions dels articles es publiquen carregant-les al compte **Cost** i pagant-les al compte **Cost: article**.

Després de comptabilitzar les transaccions al projecte, si el projecte està associat amb un contracte de projecte, el sistema reverteix totes les transaccions acumulades i crea noves transaccions facturables. Les transaccions facturables segueixen les regles de comptabilitat definides en el perfil de cost i ingressos del projecte respectiu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
