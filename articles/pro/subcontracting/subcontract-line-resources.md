---
title: Recursos de línia de subcontracte
description: En aquest tema s'explica com s'especifiquen els recursos dedicats que proporciona el proveïdor per a una línia de subcontracte específica per a temps.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323359"
---
# <a name="subcontract-line-resources"></a>Recursos de línia de subcontracte

[!include [banner](../../includes/dataverse-preview.md)]

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Al Dynamics 365 Project Operations, un proveïdor pot especificar recursos que s'utilitzaran per proporcionar la capacitat de recursos que s'adquireix amb la línia de subcontracte per a temps.

## <a name="create-subcontract-line-resources"></a>Crear recursos de línia de subcontracte

Per crear recursos de línia de subcontracte, seguiu aquests passos.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu el subcontracte amb el qual voleu treballar.
2. Obriu la línia de subcontracte per a temps en què voleu especificar els recursos del proveïdor.
3. A la pestanya **Recursos de la línia de subcontracte**, a la subquadrícula, seleccioneu **+ Nou recurs de línia de subcontracte**.
4. A la pàgina **Nova fita de línia de subcontracte**, introduïu la informació necessària i, a continuació, seleccioneu **Desa i tanca**.

A la taula següent s'expliquen els camps del recurs de línia de subcontracte.

| Camp |  Descripció |
| ----- | ------------ |
| Recurs que es pot reservar | Seleccioneu un recurs que es pot reservar de tipus "Treballador de contracte" que vulgueu utilitzar com a recurs a la línia de subcontracte. Si encara no heu creat un recurs que es pot reservar per al treballador de contracte, deixeu aquest camp buit. Es crea un recurs que es pot reservar en desar el registre.  |
| Contacte | Si el camp **Recurs que es pot reservar** està buit, podeu crear el recurs de línia de subcontracte a partir d'un contacte existent. Utilitzeu la cerca per veure la llista de contactes actius al sistema. Seleccioneu un contacte per al proveïdor d'aquest subcontracte. El contacte que heu seleccionat es valida quan deseu el registre. Si el contacte que heu seleccionat no és un contacte vàlid, el registre no es desa. Si no hi ha cap recurs que es pot reservar per al contacte seleccionat, el sistema crea un recurs que es pot reservar per al contacte seleccionat abans de crear el recurs de línia de subcontracte. |
| Usuari | Si el camp **Recurs que es pot reservar** està buit, podeu crear un recurs de línia de subcontracte seleccionant un usuari actiu. Utilitzeu la cerca per veure la llista d'usuaris actius al sistema. Si no hi ha cap recurs que es pot reservar per a l'usuari seleccionat, el sistema crea un recurs que es pot reservar per a l'usuari seleccionat abans de crear el recurs de línia de subcontracte. |
| Data d’inici | La data en què s'iniciarà l'assignació del treballador de subcontracte. Si aquest recurs es reserva per un període abans d'aquest interval de dates, es mostrarà un advertiment. |
| Data d’acabament | La data en què finalitza l'assignació del treballador de subcontracte. Si aquest recurs es reserva per un període després d'aquest interval de dates, es mostrarà un advertiment. |
| Esforç | Nombre total d'hores d'esforç que el treballador de subcontracte passarà en aquesta línia de subcontracte. Si aquest recurs es reserva per més de l'esforç assignat a aquest subcontracte, es mostrarà un advertiment. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
