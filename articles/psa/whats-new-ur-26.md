---
title: Novetats o canvis de la versió d'actualització 26 del Project Service Automation, V3
description: En aquest article s'enumeren les característiques i les correccions que estan disponibles a la versió 26, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 11f722c1f31c0e8aa08192cc955aabbe97018225
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928788"
---
# <a name="project-service-automation-update-release-26-v3"></a>Project Service Automation, versió d'actualització 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](/power-platform/admin/install-remove-preferred-solution).

En aquest article s'enumeren les característiques i les correccions que són noves o canviades per a la versió 26, V3. Aquesta versió té un número de compilació de V3.10.44.59 i està disponible de manera general a través d'una actualització d'autoservei al desembre de 2020.

## <a name="update-release-26"></a>Versió d'actualització 26

### <a name="bug-fixes"></a>Correccions d'errors

**Temps i despesa**

S'han corregit els problemes següents:

- Els usuaris poden canviar la tasca en un registre de temps que s'ha aprovat o enviat.
- Error "referència d'objecte no definida" en desar una entrada de temps.
- La importació d'entrades de temps a partir de les assignacions de recursos crea anotacions de temps amb valors de data i hora incorrectes.
- Quan Project Service Automation i l'aplicació Field Service estan instal·lats, el botó **Nou** es visualitza dues vegades a la barra d'ordres per a les entrades de temps a l'aplicació Field Service.
- Les actualitzacions a les cel·les **Permet unitat** i **Grup d'unitats** ara es fan a la quadrícula **Estimacions de despesa**.
- El formulari **Actualitza l'edició de l'entrada de temps** inclou **Cronologia**.
- L'aprovació de temps per a les entrades de temps que no són del projecte bloqueja el sistema en cercar una funció d'aprovador de projecte.

**Administració de recursos**

S'han corregit els problemes següents:

- S'ha afegit la validació al complement **PostProjectCreate** per comprovar si es compleix un requisit principal abans de crear-ne un.
- El formulari de creació ràpida **Membre de l'equip de projecte** llança una excepció de referència nul·la si els camps se suprimeixen del formulari.
- Els requisits generació de 12 hores a partir d'1 any fallaran.
- S'ha millorat el missatge d'error d'excepció de referència nul·la durant la creació de requisits de recursos.

**Administració de projectes**

S'han corregit els problemes següents:

- S'ha millorat la validació per tractar l'excepció de referència nul·la generada en el complement **PreProjectUpdate**.
- Els projectes publicats pel complement de l'escriptori de Microsoft Project suprimeixen assignacions no assignades.
- S'ha afegit una validació nova quan la referència del projecte d'una tasca no és vàlida a causa d'una excepció de referència nul·la a **PreValidateProjectTaskUpdate**.
- La quadrícula Membres de l'equip no mostra les assignacions diferents del registre dels membres de l'equip.
- S'han afegit nous missatges de validació i d'error a causa de l'excepció de referència nul·la en el complement **PreProjectTaskDelete**.

**Sales**

S'han corregit els problemes següents:

- Quan seleccioneu una línia basada en projectes a l'oferta o el contracte, el botó **Suggeriment** només hauria de ser visible en seleccionar una línia basada en productes associada amb un producte existent.
- Dividiu el privilegi **Create_Product** del privilegi **Create_ProjectContract**.
- La supressió d'una línia de factura provoca un error de referència nul·la a **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
