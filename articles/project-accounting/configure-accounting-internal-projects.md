---
title: Configuració de la comptabilitat per a projectes interns
description: En aquest article s'ofereix informació sobre com configurar pràctiques comptables per a projectes interns en operacions de projectes.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919450"
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
