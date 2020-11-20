---
title: Configuració d'una planificació de bestretes (bàsic)
description: Aquest tema proporciona informació sobre com configurar una planificació de bestreta al Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e0312b89d9969f140146b6aaaa9bdcfde702c0b
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181260"
---
# <a name="set-up-a-retainer-schedule---lite"></a>Configuració d'una planificació de bestretes (bàsic)

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Les planificacions de bestreta estan configurades a la pàgina **Contracte del projecte** al Dynamics 365 Project Operations.

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
