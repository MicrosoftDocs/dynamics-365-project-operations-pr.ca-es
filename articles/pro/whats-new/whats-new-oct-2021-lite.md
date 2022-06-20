---
title: "Novetats d'octubre de 2021: implementació bàsica del Project Operations"
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'octubre de 2021 de la implementació lite d'operacions del projecte.
author: sigitac
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7199853bea7e8e99a2a1ce19d6ce88736edb38f8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921934"
---
# <a name="whats-new-october-2021---project-operations-lite-deployment"></a>Novetats d'octubre de 2021: implementació bàsica del Project Operations

_S'aplica a: implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents Dynamics 365 Project Operations:

  - Project Operations en entorn del Microsoft Dataverse versió 4.25.0.91


## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

[Administració de subcontractes](../subcontracting/managing-subcontracts-overview.md): aquesta característica proporciona la capacitat de crear un subcontracte amb el proveïdor, detallar totes les compres com a elements de línia al subcontracte, ajustar els preus i associar contactes.


## <a name="quality-updates"></a>Actualitzacions de qualitat

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2209402 | S'han corregit les validacions que impedien que es poguessin facturar els imports de bestreta quan es confirmava un contracte de projecte. |
|   Administració d'oportunitats | 2227414 | Els camps **Producte**, **Escriptura** i **IsProductOverriden** es copien als detalls de la línia d'oferta i als detalls de la línia de contracte. |
| Facturació i preus | 2338357 | La moneda al registre d'ús de materials ha de ser per defecte la moneda del projecte quan el projecte se selecciona. |
| Temps i despeses | 2414777 | Ha de ser possible cancel·lar una aprovació quan la despesa o entrada de temps té més d'una aprovació de projecte associada. |
