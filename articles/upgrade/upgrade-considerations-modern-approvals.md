---
title: Millorar les consideracions per a les aprovacions modernes
description: L'article cobreix els punts que els administradors haurien de tenir en compte quan habiliten la funcionalitat d'aprovacions modernes.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931732"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Millorar les consideracions per a les aprovacions modernes 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Com a part de la versió wave 1 d'abril de 2022, la funcionalitat d'aprovacions modernes s'habilitarà per defecte. Aquesta funcionalitat millora la fiabilitat de la lògica d'aprovació i assegura que podeu determinar la raó si la lògica d'aprovació falla.

Com a part d'aquest canvi, s'actualitzen els canvis d'estat per a les aprovacions del projecte. L'estat ara passa directament de **Presentat** a **Aprovat**. **L'pendent** ja no és un estat per a les aprovacions. Per determinar si hi ha una aprovació pendent, verifiqueu que l'aprovació forma part d'un conjunt d'aprovació i reviseu l'estat del conjunt d'aprovació adjunt.

## <a name="before-you-upgrade"></a>Abans d'actualitzar

Abans d'actualitzar a Aprovacions modernes, assegureu-vos que no teniu aprovacions pendents. Aprovacions modernes no utilitza l'estat **pendent**. Per tant, les aprovacions que encara estiguin marcades com a **pendents** després de l'actualització no es processaran.

## <a name="after-you-upgrade"></a>Després d'actualitzar

Després d'actualitzar a Aprovacions modernes, un administrador ha de validar que el flux en el núvol que processa les aprovacions s'ha habilitat.

1. Inicia la sessió a [flow.microsoft.com](https://flow.microsoft.com)
2. A la part superior dreta de la pàgina, canvieu l'entorn a l'entorn que heu actualitzat.
3. Seleccioneu **Solucions** per llistar les solucions instal·lades a l'entorn.
4. A la llista de solucions, seleccioneu **Operacions** del projecte o **Servei del projecte**.
5. Canvia el filtre de **Tots** a fluxos **al** núvol.
6. Verifiqueu que l'opció **Servei de projectes : planifica recurrentment els conjunts d'aprovació del** projecte està establerta a **On**. Si no és així, seleccioneu el flux i, a continuació, seleccioneu **Activa**.
7. Verifiqueu que el processament s'està produint cada cinc minuts revisant la **llista De feines** **del sistema a l'àrea** Configuració.

## <a name="short-term-rollback"></a>Retrocés a curt termini

Si no podeu reprendre els canvis o si trobeu un problema greu amb aquesta funció, podeu tornar temporalment al flux d'aprovació original realitzant els passos següents:
1. Inicieu la sessió al vostre entorn i verifiqueu que no hi ha aprovacions pendents.
2. Aneu a **Paràmetres** > **del projecte de** configuració.
3. Seleccioneu **Control de** funcions i seleccioneu **Aprovacions modernes** per desactivar la funció.

## <a name="removing-the-feature-flag"></a>S'està suprimint l'indicador de característiques

A l'actualització d'octubre de 2022 Wave 2, se suprimirà la possibilitat de desactivar aquesta funció.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
