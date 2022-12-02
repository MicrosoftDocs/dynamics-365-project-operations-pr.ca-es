---
title: Recursos de línia de subcontracte
description: En aquest article s'explica com s'especifiquen els recursos dedicats que proporciona el proveïdor per a una línia de subcontracte específica per a temps.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 04e3e5ee70c50068304a8a6c8f7e93df48ed7e85
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522360"
---
# <a name="subcontract-line-resources"></a>Recursos de línia de subcontracte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Al Dynamics 365 Project Operations, un proveïdor pot especificar recursos que s'utilitzaran per proporcionar la capacitat de recursos que s'adquireix amb la línia de subcontracte per a temps.

## <a name="create-subcontract-line-resources"></a>Crear recursos de línia de subcontracte

Per crear recursos de línia de subcontracte, seguiu aquests passos.

1. A la subfinestra de navegació, seleccioneu **Subcontractes** i obriu el subcontracte amb el qual voleu treballar.
2. Obriu la línia de subcontracte per a temps en què voleu especificar els recursos del proveïdor.
3. A la pestanya **Recursos de la línia de subcontracte**, a la subquadrícula, seleccioneu **+ Nou recurs de línia de subcontracte**.
4. A la pàgina **Nou recurs de línia de subcontracte**, introduïu la informació necessària i seleccioneu **Desa i tanca**.

A la taula següent s'expliquen els camps del recurs de línia de subcontracte.

| Camp | Descripció | Impacte funcional |
| ----- | ----------- | ----------------- |
| Recurs que es pot reservar | Seleccioneu un recurs que es pot reservar de tipus **Treballador de contracte** que vulgueu utilitzar com a recurs a la línia de subcontracte.| Si no heu creat cap recurs que es pot reservar per al treballador de contracte, deixeu aquest camp buit. Es crearà un recurs que es pot reservar en desar el registre.  |
| Contacte | Podeu crear el recurs de línia de subcontracte a partir d'un contacte existent. Utilitzeu la cerca per veure la llista de contactes actius al sistema. Seleccioneu un contacte per al proveïdor d'aquest subcontracte. Si el contacte que heu seleccionat no és un contacte vàlid per al proveïdor del subcontracte, el registre del recurs de línia de subcontracte no es desarà.| Si no hi ha cap recurs que es pot reservar per al contacte seleccionat, el sistema crea un recurs que es pot reservar per al contacte seleccionat abans de crear el recurs de línia de subcontracte. |
| Usuari | Podeu crear un recurs de línia de subcontracte seleccionant un usuari actiu. Utilitzeu la cerca per veure la llista d'usuaris actius al sistema.| Si no hi ha cap recurs que es pot reservar per a l'usuari seleccionat, el sistema crea un recurs que es pot reservar per a l'usuari seleccionat abans de crear el recurs de línia de subcontracte. |
| Data d’inici | La data en què s'iniciarà l'assignació del treballador de subcontracte.| Si aquest recurs es reserva per un període abans d'aquest interval de dates, es mostrarà un advertiment. |
| Data d’acabament | La data en què finalitza l'assignació del treballador de subcontracte.| Si aquest recurs es reserva per un període després d'aquest interval de dates, es mostrarà un advertiment. |
| Esforç | Nombre total d'hores d'esforç que passarà el treballador contractat en aquesta línia de subcontracte.| Si aquest recurs es reserva per més de l'esforç assignat en aquest subcontracte, es produirà un advertiment. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
