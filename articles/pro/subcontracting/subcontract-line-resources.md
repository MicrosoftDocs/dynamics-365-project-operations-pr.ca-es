---
title: Recursos de línia de subcontracte
description: En aquest article s'explica com especificar els recursos dedicats que proporciona el proveïdor per a una línia de subcontractació específica durant el temps.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 84fbbd6e1a82db2b2d998b5f41579396df884ec3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924142"
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
