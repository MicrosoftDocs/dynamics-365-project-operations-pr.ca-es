---
title: Error de discrepància de moneda
description: En aquest article es proporciona informació sobre com solucionar un error de discrepància de moneda que es produeix quan deseu tipus de registres específics.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914712"
---
# <a name="currency-mismatch-error"></a>Error de discrepància de moneda 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan deseu un projecte, contracte, oferta o recurs que es pot reservar, pot ser que rebeu l'error **La moneda de l'empresa propietària no coincideix amb la moneda de la unitat de contractació. Per continuar, trieu una empresa propietària o una unitat de contractació diferent**. Això es deu a que hi ha una discrepància de moneda entre la moneda de la unitat de contractació del registre i la moneda de l'empresa propietària.


## <a name="resolution"></a>Resolució

Per resoldre aquest problema, feu el següent:
- Verifiqueu la moneda de la unitat de contractació d'aquest registre. Per veure la moneda, obriu el registre d'unitat organitzativa i verifiqueu el valor de la pestanya **General** del camp **Moneda**.
- Verifiqueu la moneda de l'empresa propietària. Podeu veure la moneda anant a **Relacionats** > **Llibres de comptabilitat** del registre de l'empresa. Feu doble clic al registre del llibre de comptabilitat que està associat amb l'empresa i verifiqueu el valor de la pestanya **General** del camp **Moneda de comptabilitat**.

Si la moneda definida a la unitat de contractació i al registre de llibre de comptabilitat no coincideixen, ajusteu la configuració o seleccioneu valors diferents quan deseu el registre. El sistema requereix que aquests registres coincideixin per garantir la facturació correcta entre empreses. Per obtenir més informació sobre les configuracions entre empreses, vegeu [Crear transaccions entre empreses](../../project-accounting/create-intercompany-transactions.md).

Si el registre de l'empresa no té cap registre de llibre de comptabilitat associat, això indica que no s'ha definit una configuració en configurar l'entorn. L'administrador del sistema ha de corregir la configuració. L'administrador del sistema ha d'anar a **Configuracions de doble escriptura** i aturar i reiniciar l'**Assignació de doble escriptura dels llibres de comptabilitat** amb la sincronització inicial d'aquesta assignació i els requisits previs. Per obtenir més informació, vegeu [Versions d'assignació amb doble escriptura al Project Operations](../../environment/resource-dual-write-maps.md).
