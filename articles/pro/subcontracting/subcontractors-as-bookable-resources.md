---
title: Configurar els subcontractistes com a recursos que es poden reservar
description: En aquest article s'explica com es configuren i es fa el manteniment dels recursos subcontractius creats a partir dels usuaris i els contactes del sistema per tal que es puguin associar amb els subcontractes al Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 727508c41c190c3703e9cd1420066fa0e551f147
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522689"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurar els subcontractistes com a recursos que es poden reservar

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

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
