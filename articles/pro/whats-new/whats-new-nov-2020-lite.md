---
title: 'Novetats de novembre de 2020: implementació bàsica del Project Operations; tracte de facturació proforma'
description: 'Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles en el llançament de novembre de 2020 de la implementació bàsica del Project Operations: tracte de facturació proforma.'
author: sigitac
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3a7d63e746edf73873840aee2f095192364cb286
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584630"
---
# <a name="whats-new-november-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novetats de novembre de 2020: implementació bàsica del Project Operations; tracte de facturació proforma

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

A la taula següent s'enumeren les actualitzacions al Project Operations a la versió de l'entorn del CDS 4.4.0.70.

| Àrea de característiques                 | Número de referència | Actualització de qualitat                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Administració d'oportunitats       | 2036993          | Les línies de contracte de línia d'estimació i assignació de recursos s'actualitzen a les ofertes guanyadores quan el tipus de línia d'oferta és **Totes les tasques**.                                                 |
|   Administració d'oportunitats       | 2071514          | No es pot crear una factura per a una fita de preu fix en un contracte que té la facturació basada en tasques habilitada.                                                                          |
| Facturació i preus          | 2070392          | Les línies de contracte de projecte a la factura augmenten cada vegada que se selecciona **Actualitza les transaccions de la factura**.                                                                       |
| Planificació del projecte             | 2043336          | No es pot suprimir un registre de membre de l'equip del projecte.                                                                                                                                    |
| Planificació del projecte             | 2046013          | Comportament incoherent per a les columnes d'etiquetes d'estimacions durant la càrrega en comparació amb el canvi de tipus de fase de temps.                                                                                   |
| Planificació del projecte             | 2046647          | Les hores d'inici i d'acabament tenen un desplaçament d'una hora quan es generen requisits de recursos a partir dels membres de l'equip del projecte.                                                                      |
| Planificació del projecte             | 2053879          | (Per a la pròxima implementació del CDS) PublishUnassignedAssignments trenca un intent de desar una tasca amb l'error, "El valor enviat a ConditionOperator.In està buit". |
| Planificació del projecte             | 2055501          | Deixar buida la **Data d'inici del projecte** provoca un error a la planificació.                                                                                                      |
| Planificació del projecte             | 2066817          | No es pot crear un recurs genèric amb el selector de persones de la pestanya **Tasques**.                                                                                               |
| Planificació del projecte             | 2067034          | El botó **Visualitza els detalls** no està disponible a la pàgina **Detalls de la tasca**.                                                                                                         |
| Administració de recursos          | 2046667          | Els membres de l'equip genèrics no se suprimeixen fins i tot després de complir tots els recursos.                                                                                                     |
| Entrada de temps i despesa ràpida | 2047499          | El botó **Nou** de la pàgina Entrada de temps obre la pàgina **Nova signatura de correu electrònic**.                                                                                               |
| Entrada de temps i despesa ràpida | 2059859          | S'obre una finestra emergent inesperada en crear una entrada de despesa.                                                                                                                         |
| Un altre                        | 2044181          | [Desinstal·lació del PO]: l'error "El registre no està disponible" es produeix quan intenteu desinstal·lar les solucions **msdyn_ProjectServiceCore_Patch** i msdyn_ProjectServiceCore.        |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]