---
title: Informes de despeses i diversos aprovadors
description: En aquest tema es proporciona informació sobre els informes de despeses que requereixen l'aprovació de més d'una persona.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2acae2d518a02539f01d5498450236999fe609d1e8f26b5f90e18b986b83cab1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988414"
---
# <a name="expense-reports-and-multiple-approvers"></a>Informes de despeses i diversos aprovadors

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En funció de les normes d'aprovació de despeses de l'organització, pot ser que més d'una persona hagi d'aprovar un informe de despeses enviat. En configurar el procés de flux de treball per a l'aprovació de l'informe de despeses, podeu afegir elements de flux de treball que incloguin tasques o passos per a un o diversos aprovadors de l'informe de despeses. Per exemple, és possible que necessiteu que tots els informes de despeses els aprovin dues persones independents, el cap del treballador que ha enviat l'informe i el coordinador de compte a pagar.

Si decidiu que voleu que calguin diversos aprovadors d'informes de despeses, podeu afegir els elements del flux de treball d'una de les maneres següents:

- Afegiu un element d'aprovació que tingui un pas. Per exemple, pot ser que el pas requereixi que s'assigni un informe de despeses a un grup d'usuaris i que l'aprovin un 50 per cent dels membres del grup d'usuaris.
- Afegiu un element d'aprovació que tingui diversos passos. Per exemple, pot ser que l'element d'aprovació tingui els passos següents:

    1. El cap de l'empleat que ha enviat l'informe de despeses l'aprova.
    2. L'empleat de compte a pagar verifica els rebuts i els elements de l'informe de despeses.
    3. El propietari del pressupost aprova l'informe de despeses.

- Afegiu diversos elements d'aprovació, cadascun dels quals tingui un pas. Per exemple, pot ser que afegiu un element d'aprovació independent per a cadascun dels passos següents:

    1. El cap de l'empleat aprova l'informe de despeses.
    2. El propietari del pressupost aprova l'informe de despeses.


[!INCLUDE[footer-include](../includes/footer-banner.md)]