---
title: Configurar els subcontractistes com a recursos que es poden reservar
description: En aquest tema s'explica com es configuren i es fa el manteniment dels recursos subcontractius creats a partir dels usuaris i els contactes del sistema per tal que es puguin associar amb els subcontractes al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994174"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar els subcontractistes com a recursos que es poden reservar

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Seguiu aquests passos per configurar els subcontractistes com a recursos que es poden reservar al Microsoft Dynamics 365 Project Operations.

1. Aneu a **Projecte** \> **Recursos** i seleccioneu **Crea**.
2. A la pàgina **Recurs que es pot reservar nou**, al camp **Tipus de recurs**, seleccioneu una de les opcions següents:

    - **Usuari**: seleccioneu aquest tipus de recurs si el subcontractista ha d'accedir al Project Operations per introduir temps o despeses. Si seleccioneu **Usuari**, el subcontractista necessita una llicència vàlida per accedir al sistema.
    - **Contacte** o **Compte**: seleccioneu un d'aquests tipus de recursos si el subcontractista no necessita accés al Project Operations, però ha d'estar disponible per a les assignacions de tasques o reserves en projectes. Cap d'aquests tipus de recursos proporciona accés al sistema. Seleccioneu **Compte** per representar l'empresa del proveïdor com a recurs que es pot reservar. Seleccioneu **Contacte** per representar els empleats individuals del proveïdor.

3. Segons el tipus de recurs que hàgiu seleccionat, se us demanarà que seleccioneu el registre d'usuari, compte o contacte corresponent.
4. Al camp **Tipus de treballador**, seleccioneu el "Treballador de contracte" per configurar el subcontractista com a recurs que es pot reservar.

    > [!NOTE]
    > Si deixeu en blanc el camp **Tipus de treballador**, el recurs que es pot reservar es considerarà com un empleat.

5. Si heu seleccionat **Treballador de contracte** com a tipus de treballador, seleccioneu el proveïdor per al qual treballa el recurs.
6. Seleccioneu el fus horari del recurs i, a continuació, seleccioneu **Desa**. Per assignar una plantilla d'hora de feina al recurs que es pot reservar, podeu seleccionar **Defineix el calendari** a la pàgina de la llista de **Recurs que es pot reservar**.

Per associar-se a una línia de subcontracte, el recurs que es pot reservar ha de complir aquestes condicions:

- El recurs que es pot reservar ha de ser un treballador de contracte.
- Un recurs que es pot reservar del tipus de recurs **Contacte** ha d'estar associat al compte del proveïdor com a contacte. Un recurs que es pot reservar del tipus de recurs **Usuari** no ha d'estar associat al compte del proveïdor com a contacte.
- El valor del camp **Proveïdor** del recurs que es pot reservar ha de coincidir amb el valor del camp **Proveïdor** per al subcontracte.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Actualitzar el tipus d'assignació de treballadors i proveïdors per als recursos que es poden reservar

El camp **Tipus de treballador** d'un recurs que es pot reservar determina si el recurs que es pot reservar és un treballador de contracte o un empleat. El camp **Proveïdor** defineix el compte del proveïdor amb el qual està associat el recurs que es pot reservar. En associar un recurs que es pot reservar amb un proveïdor com a contacte, heu d'indicar que el contacte és un empleat de l'empresa del proveïdor.

Si els camps **Tipus de treballador** i **Proveïdor** d'un recurs que es pot reservar es canvien, els canvis afecten qualsevol validació futura dels registres nous que el recurs que es pot reservar crea, com ara les entrades de temps. Tanmateix, els canvis no invaliden els registres existents.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
