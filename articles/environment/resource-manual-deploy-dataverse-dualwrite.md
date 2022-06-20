---
title: Implementació manual de l'aplicació Dataverse del Project Operations amb compatibilitat amb l'escriptura doble
description: En aquest article s'explica com implementar manualment l'aplicació Project Operations Dataverse perquè admeti la doble escriptura.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: be80ea3956fbf0264c2eeb7a5e30dd50b77e3c78
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911998"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Implementació manual de l'aplicació Dataverse del Project Operations amb compatibilitat amb l'escriptura doble

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

En aquest article s'explica com implementar manualment Microsoft Dynamics 365 Project Operations Microsoft Dataverse de manera que admeti la doble escriptura. El Project Operations detecta la configuració de l'entorn i afegeix compatibilitat addicional per a l'escriptura doble si es compleixen els requisits previs.

Durant el desplegament a través Microsoft Dynamics de Lifecycle Services (LCS), si heu seguit les instruccions d'aquest article, podeu ometre el desplegament de la Microsoft Power Platform integració (anteriorment coneguda com a Common Data Service entorn).

El procés d'implementació del Project Operations al Dataverse per tal que admeti l'escriptura doble té quatre passos principals:

1. [Crear un entorn nou al Dataverse que admeti l'escriptura doble](#create).
2. [Afegir requisits previs d'escriptura doble a l'entorn](#prerequisites).
3. [Afegir l'aplicació del Dataverse del Project Operations](#dataverse).
4. [Enllaçar els entorns](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Crear un entorn nou al Dataverse que admeti l'escriptura doble

Per completar aquest procediment, heu d'iniciar la sessió com a administrador.

1. Obriu el [Centre d'administració del Power Platform](https://admin.powerplatform.com) i inicieu la sessió com a administrador.
2. Creeu un entorn nou i anomeneu-lo.
3. Seleccioneu el tipus d'entorn. Si us heu registrat per obtenir l'oferta de prova, seleccioneu **Prova (basada en subscripció)**.
4. Confirmeu la regió d'implementació.
5. Habiliteu l'opció **Crea una base de dades per a aquest entorn**. 
6. Confirmeu l'idioma i confirmeu que la moneda coincideix amb la moneda de les aplicacions Finances i Operacions.
7. Habiliteu l'opció **Aplicacions del Dynamics 365** i confirmeu que el camp **Implementa automàticament aquestes aplicacions** estigui definit com a **Cap**.
8. Afegiu un grup de seguretat, si és obligatori.
9. Seleccioneu **Desa** per crear l'entorn.
10. Espereu fins que la implementació es completi i l'entorn arribi a l'estat **Preparat**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Afegir requisits previs d'escriptura doble a l'entorn

La compatibilitat amb l'escriptura doble inclou camps addicionals que s'afegeixen a entitats clau, com ara l'entitat **Empresa**. Si afegiu compatibilitat amb l'escriptura doble a un entorn existent, pot ser que calgui actualitzar les dades per habilitar la compatibilitat. Per obtenir informació sobre com inicialitzar les dades, vegeu [Inicialitzar les dades de l'empresa](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Per obtenir més informació sobre l'escriptura doble, vegeu [Requisits del sistema d'escriptura doble](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Completeu aquest procediment per afegir els requisits previs d'escriptura doble a l'entorn.

1. Obriu l'entorn que acabeu de crear i, a continuació, aneu a **Recursos** \> **Aplicacions del Dynamics 365**.
2. Seleccioneu **Solució bàsica d'escriptura doble** a la llista d'aplicacions i instal·leu-la.
3. Espereu fins que es completi la instal·lació. A continuació, seleccioneu **Solució d'orquestració d'aplicacions d'escriptura doble** a la llista d'aplicacions i instal·leu-la.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>Afegir l'aplicació del Dataverse del Project Operations

Aquest procediment només es pot completar si heu completat els procediments anteriors abans d'instal·lar el Project Operations. Durant la instal·lació, el sistema analitzarà la configuració de l'entorn i afegeix compatibilitat amb l'escriptura doble si cal.

1. Obriu l'entorn que heu creat abans i, a continuació, aneu a **Recursos** \> **Aplicacions del Dynamics 365**.
2. Seleccioneu **Microsoft Dynamics 365 Project Operations** a la llista d'aplicacions i instal·leu-lo.

## <a name="link-your-environments"></a><a name="link"></a>Enllaçar els entorns

Un cop desplegat l'entorn Dataverse, podeu configurar l'enllaç a les aplicacions Finances i Operacions. Seguiu els passos que es mostren a [Utilitzar l'auxiliar d'escriptura doble per enllaçar els entorns](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
