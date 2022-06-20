---
title: Administració de subcontractacions al Project Operations
description: Aquest article proporciona una visió general del procés de gestió de subcontractacions d'extrem a extrem normalment en organitzacions basades en projectes.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8f5e025b5f741935494349fb1bdfd3a19bacb5e1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911492"
---
# <a name="subcontract-management-in-project-operations"></a>Administració de subcontractacions al Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article proporciona una visió general del procés de gestió de subcontractacions d'extrem a extrem en organitzacions basades en projectes. La subcontractació per a serveis normalment segueix el flux del procés de negoci que es mostra al diagrama següent.

![Flux del procés de subcontractació](../media/SubcontractingProcessFlow.png)

A la llista següent es mostra una descripció pas a pas del procés de subcontractació.

1. L'administrador del projecte crea un subcontracte amb un proveïdor. Per defecte, les llistes de preus adjuntes al registre del proveïdor s'utilitzen per a la subcontractació. El compte del proveïdor té un tipus de relació de **Proveïdor** o **Distribuïdor**.
2. L'administrador del projecte pot desglossar totes les compres com a elements de línia del subcontracte. Les línies del subcontracte poden ser per temps, despeses o productes. La classe de transacció de la línia del subcontracte determina per a què serveix la línia.
3. L'administrador del compte del proveïdor i l'administrador del projecte poden iterar el subcontracte. Els preus es poden ajustar a les llistes de preus de compra que hi ha adjuntes al subcontracte.
4. En aquest punt o més endavant en el procés, si la línia del subcontracte és per al temps, l'administrador del compte del proveïdor associa els contactes del proveïdor amb cada línia de subcontracte. Aquesta associació proporciona informació a l'administrador del projecte sobre qui està treballant en el subcontracte. Quan un contacte del proveïdor s'associa amb una línia del subcontracte, el sistema crea automàticament un recurs que es pot reservar a partir del contacte, si encara no existeix cap recurs que es pot reservar.
5. El mètode de facturació de cada línia del subcontracte pot ser **Preu fix** o **Temps i material**. Per a les línies del subcontracte de preu fix, es configura una planificació de la factura basada en fites.
6.  Quan el subcontracte està configurat i ha finalitzat la negociació, es confirma. Els subcontractes confirmats no es poden editar, però si es produeixen canvis, un subcontracte es pot "tornar a obrir per a editar-lo", cosa que canvia l'estat de **Confirmat** a **Esborrany** i permet tornar a obrir la negociació. 
7.  En crear un membre de l'equip genèric en un projecte, el membre de l'equip es pot associar a una línia de subcontracte. Això indica la necessitat de dotar el membre de l'equip genèric amb capacitat subcontractada.
8.  Els membres de l'equip nomenats es poden crear directament en un projecte o crear-los reservant-los utilitzant les experiències de planificació de recursos. Si un membre de l'equip del projecte nomenat és un treballador del contracte, és possible associar-lo a una línia de subcontracte. Amb això s'agruparà la capacitat disponible en una línia de subcontracte.
9.  Els recursos de subcontractista poden registrar el temps, les despeses i l'ús de materials dels projectes i les tasques de projecte i, a continuació, enviar-los per a la seva aprovació. Per als empleats funciona de manera similar. Quan es registra el temps, un treballador de contracte pot seleccionar un subcontracte i una línia de subcontracte específiques.
10. Després de l'aprovació, el temps aprovat pels subcontractes registrarà els valors reals de cost del projecte basant-se en el preu de compra del treballador del contracte o en la funció que han dut a terme en el projecte.
11. Les factures del proveïdor i els elements de la línia de factura del proveïdor es poden registrar al sistema per a la feina feta pels recursos del proveïdor o els productes lliurats pel proveïdor. Les línies de factura del proveïdor han de ser específiques d'un projecte i d'una classe de temps, despesa, producte/material, fita o tarifa. Opcionalment, les línies de factura del proveïdor poden fer referència a una línia de subcontracte.
12. El sistema associarà automàticament tots els valors reals de cost que coincideixin amb la línia de subcontracte i el projecte a la factura del proveïdor. Això facilitarà un procés de verificació i coincidència en 3 passos.
13. A continuació, l'administrador de projectes pot revisar els valors reals del projecte coincidents automàticament, suprimir o afegir altres valors reals de cost del projecte i completar el procés de verificació.
14. Completar el procés de verificació a totes les línies marcarà la factura del proveïdor com a **Preparada per al pagament**. En aquesta fase, la factura i les línies del proveïdor es poden transferir a un sistema de Comptabilitat o de Pagaments per processar el pagament al proveïdor. Els costos de projecte prèviament registrats s'invertiran i els costos reals de la línia de factura del proveïdor es registraran al projecte.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Línies de subcontracte basades en quantitat i línies de subcontracte basades en treball

Una línia de subcontracte pot estar basada en quantitat o en treball. 

Quan una línia de subcontracte està **basada en quantitat**, la quantitat que es compra a la línia de subcontracte per a temps, despeses o material es pot utilitzar en qualsevol projecte.

Quan una línia de subcontracte està **basada en el treball**, la línia de subcontracte s'assigna a un cos de treball representat per un node del pla del projecte. El valor de la línia de subcontracte és la suma de tots els components necessaris per dur a terme aquest cos del treball. Es modelen com a detalls de la línia de subcontracte i poden ser un conjunt de temps, despeses o material. Per a una línia de subcontracte basada en treball, la línia de subcontracte també es dedica a un únic projecte. Aquest tipus de subcontractacions no són compatibles amb les operacions del projecte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

