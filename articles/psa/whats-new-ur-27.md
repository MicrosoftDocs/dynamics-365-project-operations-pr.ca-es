---
title: Novetats o canvis de la versió d'actualització 27 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 27.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8879229b50ef113d6d6cb8622b707f0c12182a57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280296"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Novetats o canvis de la versió d'actualització 27 del Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 27. Aquesta versió té el número de compilació V3.10.45.98 i està disponible de forma general a través d'una actualització automàtica el gener de 2021.

## <a name="update-release-27"></a>Versió d'actualització 27

### <a name="bug-fixes"></a>Correccions d'errors

**General**

S'han corregit els problemes següents:

- Els registres generats pels complements al Project Service Automation no s'han definit com a supressió automàtica.
- L'actualització automàtica falla perquè la solució Project Service Automation conté un element de NavBarArea nul heratat i un element de títol.

**Temps i despesa**

S'han corregit els problemes següents:

- A la quadrícula **Entrada de temps** es mostren dades incorrectes per al comportament de la data **Independent de l'interval de temps**.
- La quadrícula **Entrada de temps** crea un temps incorrecte per al comportament de la data **Independent de l'interval de temps**.
- La cerca de tasques no està limitada al projecte seleccionat de la pàgina **Edita l'entrada de temps**.
- L'aprovació de temps per a les entrades de temps que no són del projecte està blocada perquè el sistema està cercant una funció d'aprovador de projecte.
- Les entrades correctes a Valors reals mostren un missatge d'error incorrecte.
- Quan una tasca conté un valor nul del cost real i els totals del projecte s'actualitzen, es produeix l'error següent: "La clau introduïda no és al diccionari".
- En instàncies específiques, els filtres **Agrupa per** de la pestanya **Estimació del projecte** no mostra les estimacions de despeses.
- L'interval de l'**Horari d'estiu** no és correcte per a les entrades de temps.

**Administració de projectes**

S'han corregit els problemes següents:

- Millores en l'emmagatzematge en la memòria cau, que milloren el rendiment relacionat amb la càrrega de la pàgina **Projecte**.
- Una regla de negocis obsoleta impedeix que es completin les tasques de projecte.
- El complement del Microsoft Project no respecta el calendari del complement, cosa que genera requisits de recursos incorrectes.
- La creació de projectes a partir de plantilles defineix incorrectament les dates d'assignació i impedeix la capacitat de generar requisits de recursos.
- L'usuari no pot accedir a les opcios **Categoria**, **Descripció**, **Estat** mitjançant el teclat.
- Els valors de vendes reals del projecte no inclouen els valors de venda de materials i de tarifes.
- L'agregació de les vendes reals i el cost real es produeix incorrectament amb diferents tipus de canvi.
- La descripció de la **Plantilla d'hores de treball per defecte** és equívoca.
- Sagnar una tasca no suprimeix **Categoria** a la interfície d'usuari fins que no s'actualitza.
- No pot faltar la validació per garantir el desplaçament d'un projecte fora de la seva data d'acabament.

**Sales**

S'han corregit els problemes següents:

- Una excepció de referència nul·la es genera en una línia d'oferta del projecte perquè **Importa des de l'estimació del projecte** està visible quan un projecte no s'ha seleccionat.
- L'error següent, "La referència de l'objecte no s'ha definit en una instància d'un objecte" es produeix en tancar una oferta com a **Guanyada**.
- L'estat d'ajustament no s'ha definit durant la reversió actual mentre es desvincula un projecte d'una línia de contracte.
- Quan el Dynamics 365 Field Service i el Project Service Automation estan instal·lats, les opcions **Blocatge de preus** i **Utilitza els preus actuals** no es visualitzen a la vegada a la pàgina **Factura**.
- Per a la llengua japonesa, hi ha una traducció incoherent amb altres pàgines basades en el calendari.
- **Activa** i **Desactiva** s'han eliminat de les entitats **Associació de llistes de preus** al Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]