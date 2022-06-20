---
title: Novetats del febrer del 2022 - Implementació bàsica del Project Operations
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles a la versió de febrer de 2022 de la implementació del lloc de treball del projecte Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1203faa2dd53a8fb82cff0857a1725426ebff19a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922808"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Novetats del febrer del 2022 - Implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents de Microsoft Dynamics 365 Project Operations:

- 4.28.0.120 d'operacions del projecte en una Dataverse versió d'entorn

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

A partir d'aquest llançament, podeu afegir fins a 300 membres de l'equip a un sol projecte. Anteriorment, el límit en el nombre de membres de l'equip era de 150. Per obtenir més informació, vegeu [Límits del projecte](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2497369 | La correcció de material ha de seguir el valor de data en els **paràmetres de correcció**. |
| Facturació i preus | 2498697 | S'ha millorat la configuració de seguretat per a **la recuperació de l'entrada de temps**. |
| Facturació i preus | 2517455 | No s'ha **de permetre que l'acció Transaccions** de línia de factura actualitzada s'activi diverses vegades simultànies per a la mateixa factura. |
| Facturació i preus | 2517465 | L'acció **Desactiva els detalls de** la línia de factura està bloquejada perquè no és compatible. |
| Facturació i preus | 2556660 | S'han corregit les comprovacions d'eficàcia de la data que es fan a la llista de preus que s'adjunta a un registre de paràmetres del projecte. |
|   Administració d'oportunitats | 2369202 | S'ha corregit la lògica empresarial que verifica que les llistes de preus que tenen dates d'eficàcia superposades es poden adjuntar al mateix contracte de projecte. |
|   Administració d'oportunitats | 2385965 | S'ha corregit el comportament de la **pestanya Clients** de la **pàgina Contracte del projecte** quan seleccioneu **Desa i tanca**. |
