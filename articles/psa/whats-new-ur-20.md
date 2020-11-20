---
title: Novetats o canvis de la versió d'actualització 20 del Project Service Automation, V3
description: En aquest tema es mostren les característiques i correccions disponibles al Project Service Automation V3, versió d'actualització 20
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126741"
---
# <a name="project-service-automation-update-release-20-v3"></a>Project Service Automation, versió d'actualització 20, V3

Estem encantats d'anunciar-vos l'última actualització per a l'aplicació Project Service Automation per al Dynamics 365. Aquesta versió inclou algunes millores importants per a la qualitat, el rendiment i la usabilitat. Aquest llançament és compatible amb el Dynamics 365 9.x. Per actualitzar a aquesta versió, visiteu el Centre d'administració del Dynamics 365 en línia i aneu a la pàgina de solucions per instal·lar l'actualització. Per obtenir més informació, vegeu [Instal·lar, actualitzar o eliminar una solució preferida](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

En aquest tema es mostren les característiques i correccions que són noves o s'han canviat per al Project Service Automation V3, versió d'actualització 20. Aquesta versió té el número de compilació V 3.10.31.37 i està disponible de manera general a través d'una actualització automàtica el juny de 2020.

## <a name="update-release-20"></a>Versió d'actualització 20

### <a name="bug-fixes"></a>Correccions d'errors

**Administració de projectes**

S'han corregit els problemes següents:

- La importació dels membres de l'equip del projecte amb un mètode d'assignació que requereix hores resulta en un missatge d'error confús quan les hores especificades són zero.
- Els usuaris reben un error incorrecte quan s'ha introduït el nombre màxim de caràcters en el camp **Descripció** d'una tasca de projecte.
- La pàgina **Baixada del complement del Microsoft Dynamics 365 Project Service Automation** redirigeix a la pàgina de baixada en anglès quan la configuració de llengua de l'usuari està definida en japonès.
- Quan es produeix un error del servidor, l'etiqueta de sincronització de la pestanya **Planificació** del formulari **Projectes** de vegades no desapareix.
- S'envien actualitzacions de tasques redundants al servidor quan es modifica una tasca.

**Sales**

S'han corregit els problemes següents:

- Al formulari **Contracte**, fer doble clic a **Crea una factura** crea dues factures per a un únic registre de valors reals.
- A l'Internet Explorer 11, els usuaris no poden crear entrades de despeses.
- La revocació del cost i dels valors reals de vendes no facturades no s'enllaça.
- El botó **Actualitza els valors reals** del formulari **Projecte** no actualitza **Hores reals de la tasca**.
- El complement **PreValidateProjectTeamMemberCreate** pot crear recursos reservables genèrics duplicats si l'atribut **msdyn_isgenericresourceprojectscoped** està definit com a **fals**.
- **Torna a calcular** esborra els costos facturables de detalls de la línia d'oferta basada en productes i detalls de la línia de contracte.
- En escenaris concrets, el complement **PostEstimateLineUpdate** mostra un error d'excepció de referència nul·la.
- Duració de la fase de temps del **Gràfic d'anàlisi de rendibilitat** no coincideix amb la duració dels costos del detall de la línia d'oferta de preu fix de l'oferta.
- Els valors d'unitat i grup d'unitats no canvien per defecte correctament per a les categories de despesa als formularis **Detalls de la línia de contracte** i **Detalls de la línia d'oferta**.
- Les llistes **Preu de cost per unitat organitzativa** permeten solapaments en la data de l'efectivitat.
- Els usuaris no poden canviar la **Unitat organitzativa** quan el tipus de comanda no està basat en el treball, ja que produirà un error d'excepció de referència nul·la.
- Quan intenteu navegar del formulari **Detalls de la línia d'oferta** a la pestanya **Oferta**, el formulari s'actualitza i es mostrarà la pestanya **Resum**.
