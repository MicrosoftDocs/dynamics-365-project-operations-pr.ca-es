---
title: Modes de planificació
description: Aquest tema proporciona informació sobre els modes de planificació.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: cb507528c4815f5149c813bba0a354f7d840a4a5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588402"
---
# <a name="scheduling-modes"></a>Modes de planificació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


El Dynamics 365 Project Operations permet a les organitzacions definir com administren els canvis en variables clau de les tasques dins de l'estructura del desglossament del treball. Segons les necessitats específiques de l'organització, els administradors de projectes poden fer canvis en el mode de planificació en crear un projecte.

Hi ha tres modes de planificació disponibles al Project Operations:

  - Duració fixa (és el mode per defecte)
  - Esforç fix (*Treball*)
  - Unitats fixes

Els valors afectats per la definició d'un mode de planificació específic estan determinats per la fórmula següent:

  Esforç = Duració x Unitats

Quan definiu el mode de planificació d'un projecte, esteu configurant un d'aquests valors, que després no es pot canviar. Mantenir aquest valor com una constant dona prioritat sobre aquest valor, que notifica al sistema que no el canviï quan canviïn els altres dos valors. A la taula següent es proporciona informació sobre els impactes de la selecció d'un mode específic.

| **En aquesta tasca**             | **Si reviseu unitats**   | **Si reviseu la duració** | **Si reviseu l'esforç**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| Tasca d'unitats fixes     | La duració es torna a calcular. | L'esforç es torna a calcular.    | La duració es torna a calcular. |
| Tasca d'esforç fix    | La duració es torna a calcular. | Les unitats es tornen a calcular.    | La duració es torna a calcular. |
| Tasca de duració fixa  | L'esforç es torna a calcular.   | L'esforç es torna a calcular.    | Les unitats es tornen a calcular.   |

Per obtenir més informació sobre les implicacions d'un mode determinat, vegeu [Canviar el tipus de tasca per obtenir una planificació més precisa](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72). En el tema, el terme **Feina** s'utilitza en lloc d'**Esforç**.

## <a name="change-the-organizations-scheduling-mode"></a>Canviar el mode de planificació de l'organització

Completeu els passos següents per definir el mode de planificació d'una organització.

1. Aneu a **Configuració** \> **General** \> **Paràmetres** i, a continuació, seleccioneu el paràmetre de projecte. 
2. A la pàgina **Paràmetres del projecte**, seleccioneu el mode de planificació per defecte de l'organització i, a continuació, permeteu que l'administrador de projectes substitueixi la configuració en crear un projecte nou.

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>Canviar la configuració del mode de planificació d'un projecte

Si una organització permet a l'administrador del projecte substituir el mode de planificació per defecte, l'administrador del projecte pot fer que canviï quan creï un projecte nou. Tanmateix, quan el projecte s'ha desat, el mode de planificació no es pot canviar.

## <a name="copied-projects"></a>Projecte copiats

Com que un projecte es crea quan s'adopta l'acció de projecte de còpia, l'administrador del projecte no pot definir el mode de planificació. El projecte de destinació sempre serà per defecte el mode definit en el nivell de l'organització.

## <a name="copied-tasks"></a>Tasques copiades

Quan es copia una tasca d'un projecte a un altre, la tasca hereta el mode de planificació del projecte de destinació.
