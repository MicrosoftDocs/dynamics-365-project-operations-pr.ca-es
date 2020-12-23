---
title: Configurar una planificació de bestreta
description: Aquest tema proporciona informació sobre com configurar una planificació de bestreta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1c264b544660cf7a0b116f09b6bd7c94fcf0457e
ms.sourcegitcommit: 250270409412ba4cad95fbd4c345a80d3d2b3e53
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/21/2020
ms.locfileid: "4596360"
---
# <a name="set-up-a-retainer-schedule"></a>Configurar una planificació de bestreta

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Les planificacions de bestreta es configuren a la pàgina **Contracte del projecte** del Dynamics 365 Project Operations.

1. A la pàgina **Contracte del projecte**, a la pestanya **Avançaments i bestretes**, seleccioneu **Configura la planificació de bestretes**.
2. A la pàgina de diàleg que s'obre, es mostren els camps indicats a la taula següent. La taula proporciona una idea de com els valors introduïts tenen impacte o influeixen en la planificació de bestretes que es crearà.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| Client de contracte de projecte | Client del contracte al qual es facturarà aquesta bestreta o avançament. | Si teniu diversos clients en el contracte i necessiteu facturar a cadascun un import específic de bestreta o avançament, creeu manualment una factura per a cada client. |
| Inici de planificació d’una bestreta | Introduïu la data d'inici de la planificació de bestretes. | Aquesta data no pot ser la data de creació de la primera bestreta o avançament. La data en què es crea la primera bestreta o avançament també es veu afectada per la freqüència de la factura. |
| Fi de planificació d’una bestreta | Introduïu la data de finalització de la planificació de bestretes. | Aquesta data no pot ser la data de creació de l'última bestreta o avançament. La data en què es crea l'última bestreta o avançament també es veu afectada per la freqüència de la factura. |
| Nombre de bestretes que s’han de crear | Quan introduïu el nombre de bestretes que voleu crear, el sistema utilitza la data d'inici i la freqüència per crear el número d'aquest camp. | Quan aquest camp s'actualitza manualment, el sistema ignora el valor del camp **Final de la planificació de bestretes** i, en canvi, crea el nombre específic de bestretes o avançaments. |
| Freqüència de facturació | Amb quina freqüència l'aplicació crearà bestretes i avançaments. | Aquest valor influeix directament en el nombre de bestretes i avançaments i en les dates de creació. |
| Import total | L'import total és l'import que es divideix en els pagaments individuals de bestreta o avançament que es crearan. | No hi ha cap impacte descendent d'aquest camp. |
