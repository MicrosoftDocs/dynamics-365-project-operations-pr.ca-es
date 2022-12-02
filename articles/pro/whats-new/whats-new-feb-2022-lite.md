---
title: Novetats del febrer del 2022 - Implementació bàsica del Project Operations
description: Aquest article proporciona informació sobre les actualitzacions de qualitat que estan disponibles en el llançament de febrer de 2022 de la implementació bàsica del Project Operations.
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

Aquest article s'aplica als components i les versions següents del Microsoft Dynamics 365 Project Operations:

- Project Operations en un entorn del Dataverse, versió 4.28.0.120

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

A partir d'aquesta versió, podeu afegir fins a 300 membres de l'equip a un únic projecte. Anteriorment, el límit pel que fa al nombre de membres de l'equip era de 150. Per obtenir més informació, vegeu [Límits de projecte](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Actualitzacions de qualitat

| Àrea de característiques | Número de referència | Actualització de qualitat |
| --- | --- | --- |
| Facturació i preus | 2497369 | La correcció de materials ha de seguir el valor de data dels paràmetres de **Correcció**. |
| Facturació i preus | 2498697 | S'ha millorat la configuració de seguretat de **Recuperació d'entrada de temps**. |
| Facturació i preus | 2517455 | L'acció **Transaccions de línia de factura actualitzades** no es pot permetre que s'activi diverses vegades simultànies per a la mateixa factura. |
| Facturació i preus | 2517465 | L'acció **Desactiva els detalls de la línia de factura** està bloquejada perquè no està admesa. |
| Facturació i preus | 2556660 | S'han corregit les comprovacions d'efectivitat de la data que es fan a la llista de preus que s'adjunta a un registre de paràmetres de projecte. |
|   Administració d'oportunitats | 2369202 | S'ha corregit la lògica empresarial que verifica que es poden adjuntar llistes de preus que tenen dates d'efecte superposades al mateix contracte de projecte. |
|   Administració d'oportunitats | 2385965 | S'ha corregit el comportament de la pestanya **Clients** de la pàgina **Contracte del projecte** quan seleccioneu **Desa i tanca**. |
