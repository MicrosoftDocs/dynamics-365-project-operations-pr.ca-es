---
title: Error de no coincideix amb la moneda
description: Aquest tema proporciona informació de resolució de problemes sobre un error de no coincideix amb la moneda que es produeix quan deseu tipus de registres específics.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589736"
---
# <a name="currency-mismatch-error"></a>Error de no coincideix amb la moneda 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan deseu un projecte, un contracte, una oferta o un recurs que es pot reservar, és possible que rebeu l'error, **que la moneda de l'empresa propietària no coincideixi amb la moneda de la unitat de contractació. Trieu diferents empreses propietàries o unitat de contractació per continuar**. Això es deu al fet que hi ha un desajust de moneda entre la moneda de la unitat de contractació del registre i la moneda de l'empresa propietària.


## <a name="resolution"></a>Resolució

Per treballar al voltant d'aquest tema, feu el següent:
- Verifiqueu la moneda de la unitat de contractació d'aquest registre. Podeu veure la moneda obrint el registre d'unitat organitzativa i verificant el valor de la **pestanya General** al **camp Moneda**.
- Verificar la moneda de l'empresa propietària. Podeu veure la moneda anant a **Llibres de comptabilitat relacionats** > **al** registre de l'empresa. Feu doble clic al registre del llibre major associat amb l'empresa i verifiqueu el valor a la **pestanya General** del **camp Moneda comptable**.

Si la moneda establerta a la unitat de contractació i al registre del llibre major no coincideixen, ajusteu la configuració o seleccioneu valors diferents quan deseu el registre. El sistema requereix que aquests registres coincideixin per garantir un correcte flux de facturació interempresariari. Per obtenir més informació sobre les configuracions interempresases, vegeu [Crear transaccions interempresaents](../../project-accounting/create-intercompany-transactions.md).

Si el registre de l'empresa no té cap registre de llibre major associat, això indica que falta una configuració en configurar l'entorn. L'administrador del sistema ha de corregir la configuració. L'administrador del sistema ha d'anar a **configuracions** de doble escriptura i aturar i reiniciar **el mapa** de doble escriptura dels Llibres d'error amb la sincronització inicial d'aquest mapa i els seus requisits previs. Per obtenir més informació, vegeu [Versions d'assignació amb doble escriptura al Project Operations](../../environment/resource-dual-write-maps.md).
