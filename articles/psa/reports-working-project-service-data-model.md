---
title: Treballar amb el model de dades del Project Service Automation
description: En aquest article s'ofereix informació sobre com treballar amb el model de dades.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 67932eea78048c09f5f836d1330f412466622c6a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926672"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Treballar amb el model de dades del Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


El Dynamics 365 Project Service Automation amplia altres entitats de l'aplicació i presenta les seves pròpies entitats al model de dades del Common Data Service. En aquest article es descriuen algunes de les entitats que trobareu en escenaris típics d'informes de PSA.

## <a name="reporting-on-opportunities"></a>Informes en oportunitats

El Project Service Automation amplia l'entitat **Oportunitat** del Dynamics 365 Sales afegint camps que habiliten escenaris basats en projectes. Aquests camps s'identifiquen amb un nom d'esquema que està precedit per **msdyn\_**. Un camp nou que és important per als informes sobre les oportunitats del PSA és **Tipus de comanda**. Un valor **Basat en el treball** en aquest camp indica que l'oportunitat és una oportunitat del PSA. Altres camps que s'han afegit a l'entitat inclouen **Organització de contractació**, que captura l'organització que està retenint l'oportunitat i **Administrador de comptes**, que captura el nom de l'administrador de comptes que és responsable de l'oportunitat.

L'entitat **Línia d'oportunitat** també inclou els camps relacionats amb el Project Service. El **Mètode de facturació** indica si s'ha de facturar la línia d'oportunitat a partir del temps i els materials o a partir d'un preu fix, i el **Projecte** captura el nom del projecte que dona suport a l'oportunitat. Altres camps dels quals podeu informar capturen els imports de costos i pressupost del client per a l'element de línia.

## <a name="reporting-on-quotes"></a>Informar de les ofertes

El PSA amplia l'entitat **Oferta de vendes** afegint-hi camps relacionats amb projectes. El **Tipus de comanda** distingeix les ofertes del PSA de les ofertes que no són del PSA. Un valor **Basat en el treball** en aquest camp indica que l'oferta és una oferta del PSA. Altres camps que poden ser rellevants per a informes sobre ofertes del PSA inclouen camps d'import , com ara **Costos imputables**, **Costos no imputables**, **Marge brut**, **Estimacions** i **Pressupost**. Altres camps útils indiquen si l'oferta és profitosa, si es completarà a la planificació i si compleix les expectatives de pressupost del client.

El PSA també amplia l'entitat **Línia d'oferta** del Sales. Un camp que el PSA afegeix és **Mètode de facturació**, que indica com es facturarà la línia d'oferta (temps i materials o preu fix). Altres camps que s'hagin afegit a l'entitat capturen el projecte relacionat que dona suport a la línia d'oferta, la facturació, el cost i el pressupost.

El PSA també afegeix noves entitats relacionades amb l'oferta al model de dades del Dynamics 365. A continuació trobareu alguns exemples:

- **Detall de la línia d'oferta**: aquesta entitat conté els detalls de l'estimació del projecte de la línia d'oferta. Té dos registres per a cada línia d'oferta. Un registre emmagatzema el cost i els detalls de costos de la línia d'oferta i l'altre registre emmagatzema l'import de vendes i els detalls de venda de la línia d'oferta.
- **Planificació de factures de línia d'oferta**: aquesta entitat conté la planificació de facturació de la línia d'oferta. Aquesta planificació es genera a partir de la freqüència de facturació assignada a la línia d'oferta.
- **Fita de línia d'oferta**: aquesta entitat conté les fites de facturació per a les línies d'oferta de preu fix.
- **Desglossament d'anàlisi de la línia d'oferta**: aquesta entitat conté els detalls financers de la línia d'oferta. Aquests detalls poden ser útils per informar de vendes ofertes i costos estimats segons diferents dimensions.

Altres entitats que el PSA afegeix a les ofertes són **Llista de preus de projecte de línia d'oferta**, **Categoria de recurs de la línia d'oferta** i **Categoria de transacció de línia d'oferta**.

![Diagrama que mostra relacions d'oferta, línia d'oferta i projecte.](media/PS-Reporting-image2.png "Diagrama que mostra relacions d'oferta, línia d'oferta i projecte")

## <a name="reporting-on-project-contracts"></a>Informes sobre contractes de projecte

El PSA amplia l'entitat **Comanda** del Sales que s'utilitza quan es registren contractes de projecte. Afegeix un camp nou important, **Tipus de comanda**, que identifica el contracte com a contracte de projecte del PSA en comptes d'una comanda de vendes. Un valor **Basat en el treball** en aquest camp indica que la comanda és un contracte de projecte del PSA. Altres camps nous que s'afegeixen a l'entitat **Comanda** capturen els detalls sobre els costos, l'estat del contracte del PSA i l'organització propietària del contracte.

El PSA també amplia l'entitat **Línia d'oferta de vendes**. Entre els camps que s'afegeixen, hi ha camps que capturen el mètode de facturació (temps i materials o preu fix), els imports del pressupost del client i el projecte subjacent.

El PSA també afegeix entitats noves dissenyades per a contractes de projectes. A continuació trobareu alguns exemples:

- **Detall de la línia de contracte del projecte**: aquesta entitat conté els detalls de nivell de línia que s'han generat a l'import de la línia de contracte. Aquests poden ser tan detallats com els elements de línia que es generen des d'una planificació de projecte al nivell de tasca.
- **Planificació de factures de línia de contracte**: aquesta entitat conté la planificació de facturació generada a partir de la freqüència de la factura que s'assigna a la línia de contracte.
- **Fita del contracte**: aquesta entitat conté les fites de facturació de les línies de contracte que tenen un terme de facturació de preu fix.

Altres entitats que el PSA afegeix als contractes són **Llista de preus de projecte de línia de contracte de projecte**, **Categoria de recurs de la línia de contracte de projecte** i **Categoria de transacció de línia de contracte de projecte**.

![Diagrama que mostra relacions de comanda, línia de comanda i projecte.](media/PS-Reporting-image3.png "Diagrama que mostra relacions de comanda, línia de comanda i projecte")

## <a name="reporting-on-projects"></a>Informes sobre projectes

L'entitat **Projectes** i les entitats relacionades són exclusives del PSA. El **Projecte** és l'entitat de nivell superior que s'utilitza per capturar el treball i el cost del funcionament de les operacions. Aquí teniu una llista de les entitats relacionades:

- **Membre de l'equip del projecte**: aquesta entitat conté detalls dels recursos que es poden reservar que s'assignen al projecte. Aquests recursos poden ser recursos genèrics disponibles per a la seva disposició, o bé poden ser recursos amb nom que ha introduït l'administrador del projecte o que es generen des de la planificació del projecte.
- **Tasca del projecte**: aquesta entitat conté les tasques que conformen el pla del projecte o la planificació.
- **Assignació de recursos**: aquesta entitat conté l'assignació de tasques per als recursos que es poden reservar.
- **Requisit de recursos**: aquesta entitat conté els requisits per a tots els membres de l'equip de recursos genèrics.
- **Estimacions** i **Línia d'estimació**: aquestes entitats tenen una relació de capçalera/línia i contenen estimacions de despeses per al projecte. Les estimacions de les tasques s'emmagatzemen a l'entitat **Estimació de recursos**.

![Diagrama que mostra relacions de requisit de recursos i projecte.](media/PS-Reporting-image4.png "Diagrama que mostra relacions de requisit de recursos i projecte")

## <a name="reporting-on-resources"></a>Informes de recursos

Els recursos del projecte utilitzen les entitats de **Recurs que es pot reservar** de l'Universal Resource Scheduling (URS) que es comparteixen amb altres aplicacions, com ara el Microsoft Dynamics 365 Field Service. A continuació trobareu una llista de les entitats que podríeu haver d'utilitzar en informar dels recursos del projecte:

- **Recurs que es pot reservar**: aquesta entitat representa l'usuari, el contacte, el recurs genèric, el compte, el grup o l'equipament que s'utilitza a l'equip del projecte.
- **Característiques de recursos que es poden reservar**: aquesta entitat inclou les aptituds, certificacions o educació del recurs. Les característiques poden tenir uns valors de qualificació definits pel model de classificació.
- **Categoria de recursos que es poden reservar**: aquesta entitat representa la funció del recurs disponible.
- **Reserves de recursos que es poden reservar**: aquesta entitat representa el temps que s'ha reservat en els projectes del recurs. Cada reserva té una entitat d'encapçalament i entitats de línies, i cada línia té un estat que representa l'estat de la reserva.

![Diagrama que mostra relacions de característiques de recursos reservables.](media/PS-Reporting-image5.png "Diagrama que mostra relacions de característiques de recursos reservables")

## <a name="reporting-on-actual-transactions"></a>Informes sobre transaccions de valors reals

Quan aproveu un calendari de pagaments o una despesa, o bé factureu un contracte al PSA, la transacció empresarial es captura a l'entitat **Valor real**. Aquesta entitat pot servir com a base per a gairebé tots els informes relacionats amb el finançament al PSA. L'entitat **Valor real** captura les transaccions de cost i de vendes de l'esdeveniment empresarial. També captura molts atributs rellevants.

Quan treballeu amb l'entitat **Valor real**, és important que entengueu quina transacció o transaccions s'han registrat a l'entitat i quan es registren les transaccions. Aquest és el flux típic quan treballeu amb entrades de temps (el flux per a les entrades de despeses és similar):

1. Quan l'entrada de temps es desa, no es creen registres a l'entitat **Valor real**.
2. Quan l'entrada de temps s'envia, no es creen registres a l'entitat **Valor real**.
3. Quan s'aprova l'entrada de temps, es crearà un registre a l'entitat **Valor real** i es pot crear també un segon registre. El primer registre emmagatzema el cost de l'entrada de temps. El segon registre emmagatzema l'import de venda no facturat de l'entrada de temps. El segon registre depèn del projecte, ja sigui amb un client, una oferta o una línia de contracte assignada.

    | Data del document | Tipus de transacció | Classe de la transacció | Client         | Contracte   | Recurs     | Funció de recurs | Tipus de facturació | Quantitat | Preu per unitat | Import |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 2/3/18        | Cost             | Time              | Alpine Ski House | Alpine CRM | Cèlia Canal | Administrador de projecte   | Imputable   | 8.0      | 50.00      | 400.00 |
    | 2/3/18        | Vendes no facturades   | Time              | Alpine Ski House | Alpine CRM | Cèlia Canal | Administrador de projecte   | Imputable   | 8.0      | 100.00     | 800.00 |

    Aquests dos registres són registres separats però relacionats. No són dèbits ni crèdits.

4. Si un contracte està associat amb el projecte, quan l'entrada de temps s'ha facturat, es creen dos registres més a l'entitat **Valor real**. En primer lloc, es crea una quantitat negativa per al registre de vendes no facturades. Aquest registre, en essència, inverteix la venda no facturada. En segon lloc, es crea una transacció per a la venda facturada. Una vegada més, aquests registres són registres separats però relacionats, no dèbits i crèdits.

    | Data del document | Tipus de transacció | Classe de la transacció | Client         | Contracte   | Recurs     | Funció de recurs | Tipus de facturació | Quantitat | Preu per unitat | Import   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 2/4/18        | Vendes no facturades   | Time              | Alpine Ski House | Alpine CRM | Cèlia Canal | Administrador de projecte   | Imputable   | - 8.0    | 100.00     | - 800.00 |
    | 2/4/18        | Vendes facturades     | Time              | Alpine Ski House | Alpine CRM | Cèlia Canal | Administrador de projecte   | Imputable   | 8.0      | 100.00     | 800.00   |

L'entitat **Origen de la transacció** registra l'origen del registre **Valor real** i l'entitat **Connexió de la transacció** registra els registres relacionats del registre **Valor real**. A més, el registre **Valor real** conté referències al projecte, contracte de projecte (comanda), recurs disponible i client.

![Diagrama que mostra relacions de connexió de la transacció, origen i valors reals.](media/PS-Reporting-image6.png "Diagrama que mostra relacions de connexió de la transacció, origen i valors reals")


[!INCLUDE[footer-include](../includes/footer-banner.md)]
