---
title: Configuració de categories del projecte
description: Aquest tema proporciona informació sobre la configuració de categories de projectes.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: cea43422469adf12f336f7686814a8199717090c18804d3d0a7509452349566e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997099"
---
# <a name="configure-project-categories"></a>Configuració de categories del projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

El Project Operations ofereix capacitats robustes per categoritzar ingressos i despeses als projectes. Les categories proporcionen la capacitat d'informar i analitzar les transaccions de projectes i impulsar la comptabilització al llibre major.

El diagrama següent il·lustra la correlació entre categories de transaccions, categories compartides i categories de projectes. 

Les categories de transacció són l'agrupament bàsic per a transaccions de projectes. Dins d'aquest agrupament, hi ha un conjunt de categories compartides que es poden compartir entre aplicacions i mòduls. De manera més específica, les categories de projectes són el nivell de categoria més granular. Les categories de projecte són especifiques per a l'entitat legal, el mòdul i l'aplicació.

![Correlació entre categories de transaccions, categories compartides i categories de projectes.](media/project-categories.png)

## <a name="transaction-categories"></a>Categories de transacció

Les categories de transacció representen l'agrupament bàsic per a transaccions de projectes i no són específiques de l'empresa ni del tipus de transacció. Per exemple, Contoso Robotics utilitza les categories Disseny, Viatge, Instal·lació i Transacció de servei per agrupar les transaccions de projecte.

Les categories de transaccions es defineixen al mòdul Project Operations. 
1. Aneu a **Configuració** \> **Categories de transaccions** per obrir el formulari. 
2. Creeu una categoria de transacció nova seleccionant **Nou** o seleccionant **Importa des de l'Excel**.

## <a name="shared-categories"></a>Categories compartides

El Dynamics 365 utilitza el concepte de "categories compartides" per classificar les despeses en diferents aplicacions, com ara el Dynamics 365 Finance, el Dynamics 365 Supply Chain i el Dynamics 365 Project Operations. Per a cada categoria de transacció creada, el Project Operations crea automàticament quatre categories compartides relacionades: hores, despeses, càrrecs i article. Podeu revisar i ajustar les categories compartides anant a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Categories compartides**.

## <a name="project-categories"></a>Categories del projecte

Les categories de projecte representen el nivell de configuració més granular i s'han de configurar per separat i per a cada empresa; ho ha de fer un comptable de projecte.

1. Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Categories del projecte**.
2. Seleccioneu **Crea**.
3. Seleccioneu l'**identificador de categoria** de la categoria compartida que heu creat a la secció anterior. El Project Operations només permet utilitzar les categories compartides que estan associades amb categories de transaccions.
4. Seleccioneu un grup de categories.

## <a name="category-groups"></a>Grups de categories

Els grups de categories s'utilitzen per compartir propietats, principalment perfils de comptabilització, entre categories de projectes relacionats. Hi ha d'haver com a mínim un grup de categoria per a cada tipus de transacció i s'assigna a cada categoria de projecte un grup.

Les especificacions de comptabilització del Project Operations es defineixen per les regles del perfil de cost i ingrés del projecte, categories de projectes i grups de categories. Podeu configurar els grups de categories anant a **Administració de projectes i comptabilitat** \> **Configuració** \> **Categories** \> **Grups de categories**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]