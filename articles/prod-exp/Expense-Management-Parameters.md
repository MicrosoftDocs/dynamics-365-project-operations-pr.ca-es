---
title: Paràmetres d'administració de despeses
description: Els paràmetres següents controlen el comportament a l'administració de despeses.
author: KimANelson
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2ef48f844656ff5197ae1731fb3f9bdf91a1a906b16f35bb2124469743a9e954
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991339"
---
# <a name="expense-management-parameters"></a>Paràmetres d'administració de despeses


Els paràmetres controlen el comportament general a l'administració de despeses.

### <a name="general"></a>General

| **Camp**                                                | **Descripció**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Tarifa estàndard de quilometratge**                             | Introduïu la tarifa de reemborsament per a les despeses de quilometratge. La tarifa es multiplicarà pel quilometratge introduït en la despesa per a calcular la quantitat reemborsada per la despesa de viatge.                       |
|**Despeses personals pagades per**                             | Seleccioneu qui és el responsable de pagar els imports de les transaccions de targetes de crèdit que es classifiquen com a personals.                                                                                                     |
|**Mostra l'informe de despeses complet a l'origen**               | Seleccioneu aquesta opció per mostrar totes les despeses d'un informe de despeses quan es visualitzen les dades del document original per a un comprovant específic que es va generar quan es va publicar l'informe de despeses.              |
|**L'autorització prèvia del viatge és obligatòria**                 | Seleccioneu aquesta opció per exigir que es presenti una petició de viatge i s'aprovi abans que un empleat pugui enviar un informe de despeses.                                                                    |
|**Permet l'edició de distribucions abans de publicar-les**            | Seleccioneu si les distribucions d'un informe de despeses es poden editar abans que es comptabilitzi.                                                                                                                 |
|**Avalua les polítiques de gestió de despeses**                     | Seleccioneu quan s'avaluen les despeses per determinar si s'ha infringit una norma de despesa. Les despeses es poden comprovar per cercar-hi infraccions quan s'introdueix i es desa l'entrada de la despesa, o quan la despesa es sotmet a la seva aprovació. Les regles de norma per als rebuts que es requereixin es comprovaran quan es desi la línia de despesa.                   |
|**Permet les línies de despesa entre empreses**                         | Seleccioneu si permeteu la introducció de despeses per a altres entitats jurídiques en un informe de despeses.                                                                                                          |
|**Permet editar el tipus de canvi de les despeses de la targeta de crèdit** | Seleccioneu aquesta opció per permetre a l'usuari editar el tipus de canvi de les despeses de targeta de crèdit importades.                                                                        |
|**Camps de jerarquia de diversos nivells que es mostraran**                  | Seleccioneu quins camps d'aprovador es mostraran quan el tipus d'assignació del flux de treball d'informes de despeses s'estableixi com a jerarquia i la selecció de la jerarquia s'estableixi per utilitzar la jerarquia d'aprovació de despeses de diversos nivells. Quan s'utilitza la jerarquia d'aprovació de diversos nivells per a un flux de treball, els camps seleccionats es mostraran a l'informe de despeses i seran editables. |
|**Introduïu el número de la targeta de crèdit de l'empleat (actualització de juliol de 2017)**     | Seleccioneu si es pot introduir i desar un número de 15 caràcters o de 16 caràcters al camp **Identificador de la targeta** a la pàgina **Targetes de crèdit** d'un empleat.                                                                          |

### <a name="financial"></a>Finances

| **Camp**                                                            | **Descripció**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nom del diari general**                                         | Seleccioneu el nom del registre general al qual es publiquen els informes de despeses aprovats.            |
|**Habilita la recuperació d'impostos de les despeses**                                  | Seleccioneu aquesta opció per habilitar la recuperació d'impostos de les despeses per a les despeses que compleixin els requisits. Aquesta opció no es pot habilitar si l'impost de vendes dels EUA i l'ús de les normes d'impostos estan habilitades.      |
|**Comptabilitza els avançaments d'efectiu immediatament**                                     | Seleccioneu aquesta opció per comptabilitzar un avançament d'efectiu aprovat quan s'hagi completat el procés de pagament i de transferència. Si aquesta opció no està seleccionada, el procés de pagament i de transferència generarà un diari general sense comptabilitzar. |
|**Corregeix la data de comptabilitat durant la comptabilització**                             | Seleccioneu aquesta opció per actualitzar la data de comptabilitat quan es comptabilitzin les despeses, si el període actual està retingut o tancat. La data de comptabilitat es definirà en el següent període de temps obert.   |
|**Permet l'agrupament de transaccions segons el compte de desplaçament especificat a la forma de pagament**      | Seleccioneu aquesta opció per resumir les transaccions de despeses d'un informe de despeses segons el compte de desplaçament que s'especifica al mètode de pagament de les despeses.   
|**Impostos inclosos**                                                   | Seleccioneu aquesta opció per incloure l'impost de vendes a l'import de la despesa per defecte.             |
|**Allibera les impugnacions en tancar les peticions de viatge**            | Seleccioneu aquesta opció per alliberar els fons impugnats quan es tanca una petició de viatge aprovada.                                                                                   |
|**Permet l'enviament de peticions de viatges en excés del pressupost per al registre del pressupost i pressupost de projecte** | Seleccioneu aquesta opció per permetre als empleats enviar peticions de viatge per a l'aprovació que excedeixin el pressupost permès que es defineix en el registre de pressupost o el pressupost permès per a un projecte.            |
|**Permet l'enviament d'informes de despeses en excés del pressupost per al registre del pressupost i pressupost de projecte**    | Seleccioneu aquesta opció per permetre als empleats enviar informes de despeses per a l'aprovació que excedeixin el pressupost permès que es defineix en el registre de pressupost o el pressupost permès per a un projecte.                |
|**Permet l'aprovació d'informes de despeses en excés del pressupost només per al registre del pressupost**                | Seleccioneu aquesta opció per permetre que els aprovadors aprovin els informes de despeses que superin el pressupost permès que s'estableixi al registre de pressupostos.                                                                       |

### <a name="per-diem"></a>Per dia

| **Camp**                             | **Descripció**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Hores mínimes per a la dieta**           | Introduïu el nombre mínim d'hores per defecte que un empleat ha de treballar en un dia per poder rebre una dieta per a les despeses relacionades amb els viatges.  Aquest valor només s'utilitza com a valor per defecte per al camp Hores mínimes per a nivells de tarifes de dietes.                                                                                      |
|**Percentatge d'àpat**                          | Introduïu el percentatge per defecte de les dietes per als àpats que s'utilitza durant el primer i l'últim dia de la despesa relacionada amb el viatge quan el camp **Calcula la reducció de l'àpat per** es defineix com a **Tipus d'àpat per dia** o **Nombre d'àpats per dia**. La jornada laboral del primer i l'últim dia pot ser més curta que una jornada de treball estàndard. Per tant, pot ser que l'import de les dietes d'aquests dies sigui diferent de l'import estàndard. Si el percentatge es defineix com a 0, les deduccions per al primer i últim dia seran 0,00. |
|**Percentatge d'hotel**                        | Introduïu el percentatge per defecte de la dieta dels hotels que s'utilitza durant el primer i l'últim dia de la despesa relacionada amb el viatge. La jornada laboral del primer i l'últim dia pot ser més curta que una jornada de treball estàndard. Per tant, pot ser que l'import de les dietes d'aquests dies sigui diferent de l'import estàndard. Si el percentatge es defineix com a 0, les deduccions per al primer i últim dia seran 0,00.                                              |
|**Percentatge d'altres**                        | Introduïu el percentatge per defecte de la dieta de les despeses diverses que s'utilitza durant el primer i l'últim dia de la despesa relacionada amb el viatge. La jornada laboral del primer i l'últim dia pot ser més curta que una jornada de treball estàndard. Per tant, pot ser que l'import de les dietes d'aquests dies sigui diferent de l'import estàndard. Si el percentatge es defineix com a 0, les deduccions per al primer i últim dia seran 0,00.                                                                                                     |
|**Percentatge de reducció per a l'esmorzar** | Introduïu l'import que es redueix la dieta per esmorzar. Per exemple, si un empleat rep un esmorzar de cortesia, pot ser que us interessi reduir la quantitat de la dieta en un 10 per cent.                               |
|**Percentatge de reducció per al dinar**    | Introduïu l'import que es redueix la dieta per dinar. Per exemple, si un empleat rep un dinar de cortesia, pot ser que us interessi reduir la quantitat de la dieta en un 15 per cent.                                       |
|**Percentatge de reducció per al sopar**   | Introduïu l'import que es redueix la dieta per sopar. Per exemple, si un empleat rep un sopar de cortesia, pot ser que us interessi reduir la quantitat de la dieta en un 25 per cent.                                     |
|**Calcula la reducció d'àpats per**         | Seleccioneu com hauria de calcular el sistema la reducció d'àpats de les dietes, seleccionant si la reducció es basa en el tipus d'àpat per viatge o per dia o si es basa en el nombre d'àpats permesos per dia.|
|**Arrodoniment de dietes**                  | Seleccioneu el tipus d'arrodoniment que s'utilitza per a les despeses de dietes. Si seleccioneu l'arrodoniment normal, qualsevol despesa de dieta que tingui un import de 0,50 s'arrodoneix a 1,00 i qualsevol despesa de dieta que tingui un import inferior a 0,50 s'arrodoneix a 0,00.                                                                                              |
|**Basa el càlcul de dietes en**         | Seleccioneu si l'import d'una dieta es basa en un dia natural o en un període de 24 hores.       |

### <a name="fax-cover-pages"></a>Pàgines de portada de fax

| **Camp**                      | **Descripció**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instruccions**                   | Introduïu les instruccions que els empleats han de seguir quan creen una pàgina de portada d'un fax que s'utilitza per enviar els rebuts que estan relacionats amb un informe de despeses. Feu clic al botó **Traduccions** per introduir el text específic de la llengua que es mostrarà segons la llengua de l'usuari. |
|**Identificador d'usuari (informació del codi de barres)** | Seleccioneu aquesta opció per emmagatzemar l'identificador únic d'un empleat al codi de barres que s'utilitza a la pàgina de portada del fax.                 |
|**Codi de barres**                      | Seleccioneu el codi de barres que s'utilitza a la pàgina de portada del fax. Els codis de barres 39 i 128 estan admesos a l'administració de despeses.               |

### <a name="anti-corruption"></a>Anticorrupció

|                 <strong>Camp</strong>                 |                                                                                                                                                                                            <strong>Descripció</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Mostra la certificació anticorrupció</strong>  | Seleccioneu aquesta opció per mostrar el text anticorrupció quan es crea un informe de despeses. Llavors, es poden habilitar categories de despeses específiques que requeriran que la certificació anticorrupció es seleccioni a l'informe de la despesa. Per exemple, una categoria de regal que estigui relacionada amb una despesa de funcionari del govern podria exigir que l'empleat confirmi que la despesa compleix la norma de l'empresa relacionada amb funcionaris del govern. |
| <strong>Missatge anticorrupció per a la persona que fa l'enviament</strong> |                                                                                             Introduïu el text que es mostrarà a l'empleat en crear un nou informe de despeses. Feu clic al botó <strong>Traduccions</strong> per introduir el text específic de la llengua que es mostrarà segons la llengua de l'usuari.                                                                                             |
| <strong>Missatge anticorrupció per a l'aprovador</strong>  |                                                                                             Introduïu el text que es mostrarà a l'aprovador en crear un nou informe de despeses. Feu clic al botó <strong>Traduccions</strong> per introduir el text específic de la llengua que es mostrarà segons la llengua de l'usuari.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]