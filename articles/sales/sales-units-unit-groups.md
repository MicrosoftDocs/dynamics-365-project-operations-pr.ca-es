---
title: Unitats i grups d'unitats
description: En aquest tema es proporciona informació sobre com crear unitats i grups d'unitat al Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898744"
---
# <a name="units-and-unit-groups"></a>Unitats i grups d'unitats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les unitats són les quantitats o mesures en les quals vendreu els productes o serveis. Per exemple, si veneu materials per a jardineria, els podeu vendre en unitats de paquets, caixes i palets. Un grup d'unitats és un conjunt d'aquestes unitats diferents.

Per completar els passos d'aquest tema, assegureu-vos que se us hagi assignat la funció Administrador del sistema o Administrador del Sales Professional o que tingueu permisos equivalents.

## <a name="create-a-unit-group"></a>Crear un grup d'unitats

1. En el mapa del lloc, seleccioneu **Unitats**.
2. Seleccioneu **Nou** i, al quadre de diàleg **Crea un grup d'unitats**, introduïu el nom de la unitat.
3. Al camp **Unitat principal**, introduïu la unitat de mesura comuna més baixa en què es vendrà el producte. Per exemple, podeu introduir "peça" o "unça".
4. Seleccioneu **D'acord**.

## <a name="add-units-to-a-unit-group"></a>Afegir unitats a un grup d'unitats

1. Obriu un grup d'unitats i, a la pestanya **Relacionat**, seleccioneu **Unitats**. Veureu que la unitat principal ja s'ha afegit.
2. Seleccioneu **Afegeix una unitat nova** i a la pàgina **Creació ràpida: unitat**, al camp **Nom**, introduïu el nom de la unitat.
3. Al camp **Quantitat**, introduïu la quantitat que contindrà la unitat. Per exemple, si una caixa conté dues peces, introduïu "2". 
4. Al camp **Unitat de base**, seleccioneu una unitat de base per establir la unitat de mesura més baixa per a la unitat. Per exemple, podeu seleccionar "peça".
5. Seleccioneu **Desa**:
