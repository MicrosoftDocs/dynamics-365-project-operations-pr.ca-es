---
title: Actualització de consideracions per a les aprovacions modernes
description: L'article cobreix els punts que els administradors han de tenir en compte quan habiliten la funcionalitat Aprovacions modernes.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>Actualització de consideracions per a les aprovacions modernes 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Com a part de la fase 1 de la versió d'abril de 2022, la funcionalitat Aprovacions modernes s'habilitarà per defecte. Aquesta funcionalitat millora la fiabilitat de la lògica d'aprovació i garanteix que podeu determinar la raó si falla la lògica d'aprovació.

Com a part d'aquest canvi, s'actualitzen els canvis d'estat per a les aprovacions de projecte. L'estat passa ara directament d'**Enviada** a **Aprovada**. L'estat **Pendent** ja no és per a les aprovacions. Per determinar si hi ha una aprovació està pendent, comproveu que l'aprovació formi part d'un conjunt d'aprovació i reviseu l'estat del conjunt d'aprovació adjunt.

## <a name="before-you-upgrade"></a>Abans d'actualitzar

Abans d'actualitzar a Aprovacions moderns, assegureu-vos que no teniu cap aprovació pendent. Aprovacions modernes no utilitza l'estat **Pendent**. Per tant, totes les aprovacions que encara estan marcades com a **Pendents** després de l'actualització no es processaran.

## <a name="after-you-upgrade"></a>Després de l'actualització

Després d'actualitzar a Modern Approvals, un administrador ha de validar que s'hagi habilitat el flux de núvol que processa les aprovacions.

1. Inicieu la sessió a [flow.microsoft.com](https://flow.microsoft.com)
2. A la part superior dreta de la pàgina, canvieu l'entorn a l'entorn que heu actualitzat.
3. Seleccioneu **Solucions** per enumerar les solucions que hi ha instal·lades a l'entorn.
4. A la llista de solucions, seleccioneu **Project Operations** o **Project Service**.
5. Canvieu el filtre de **Tots** a **Fluxos de núvol**.
6. Verifiqueu que l'opció **Project Service: planifica de manera recurrent els conjunts d'aprovacions del projecte** estigui definida com a **Activat**. Si no ho està, seleccioneu el flux i, a continuació, seleccioneu **Activa**.
7. Verifiqueu que el processament es produeixi cada cinc minuts revisant la llista **Feines del sistema** de l'àrea **Configuració**.

## <a name="short-term-rollback"></a>Reversió a curt termini

Si no podeu recuperar els canvis o si us trobeu amb un problema greu amb aquesta característica, podeu tornar temporalment al flux d'aprovació original amb els passos següents:
1. Inicieu la sessió a l'entorn i comproveu que no hi hagi aprovacions pendents.
2. Aneu a **Configuració** > **Paràmetres del projecte**.
3. Seleccioneu **Control de característica** i, a continuació, seleccioneu **Aprovacions modernes** per desactivar la característica.

## <a name="removing-the-feature-flag"></a>Suprimir l'indicador de característica

A l'actualització d'octubre de 2022, fase 2, la possibilitat de desactivar aquesta característica s'eliminarà.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
