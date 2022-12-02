---
title: Migrar fites de retallada facturades totalment en la transició
description: En aquest article s'explica com migrar les fites de facturació de preu fix que s'han facturat al client per a contractes de projecte oberts abans de la data de publicació.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 05cd71f9860b5698e3a26bc72660b0b2044206c8
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028690"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar fites de retallada facturades totalment en la transició

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="scenario"></a>Escenari

Contoso s'activarà amb el Microsoft Dynamics 365 Project Operations per als escenaris de recursos/no mantinguts en existències. Com a part de les activitats de retallada, l'equip d'implementació ha de migrar els contractes de projecte oberts del sistema antic. Alguns dels contractes del projecte inclouen línies de contracte que utilitzen el mètode de facturació de preu fix i que ja han estat facturades parcialment al client final. L'equip d'implementació ha de migrar aquestes fites de facturació com a **Factura de client comptabilitzada**, perquè s'han d'incloure al valor total del contracte per al reconeixement d'ingressos. No obstant això, els saldos del client al compte a cobrar i al llibre general de comptabilitat no s'han de veure afectats.

## <a name="solution"></a>Solució

### <a name="prerequisites"></a>Requisits previs

- Cal que hi hagi instal·lat el Dynamics 365 Finance 10.0.24 o posterior.
- L'entorn on es completaran els passos de migració ha d'estar en mode de manteniment. No s'ha de fer cap altra activitat mentre es migren les fites.
- Els passos de la migració s'han de seguir exactament segons s'indica aquí i només es poden utilitzar per a l'activitat de retallada. Microsoft no admet cap altre ús d'aquesta capacitat.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Crear una versió de retallada de l'assignació de doble escriptura de els fites de línia de contracte d'integració del Project Operations 

1. Assegureu-vos que l'assignació de destinació de l'entitat de **fites de línia de contracte d'integració del Project Operations** estigui actualitzada. 

    1. Al Finance, aneu a **Administració de dades** \> **Entitats de dades** i seleccioneu l'entitat **fites de línia de contracte d'integració del Project Operations**. 
    2. Seleccioneu **Modifica les assignacions de destinació**. 
    3. A la pàgina **Assigna la fase a la destinació**, seleccioneu **Genera l'assignació** i, a continuació, confirmeu que voleu generar l'assignació.

2. Atureu i actualitzeu l'assignació de doble escriptura **Fites de línia de contracte d'integració del Project Operations** (**msdyn\_contractlinesscheduleofvalues**). 

    1. Aneu a **Administració de dades** \> **Doble escriptura**, seleccioneu l'assignació i obriu-ne els detalls. 
    2. Seleccioneu **Atura** i espereu fins que el sistema aturi l'assignació. 
    3. Seleccioneu **Actualitza les taules**.

3. Afegiu una assignació per a l'estat de la transacció.

    1. Seleccioneu **Afegeix una assignació**.
    2. A la línia nova, a la columna **Aplicacions de finances i operacions**, seleccioneu el camp **TRANSSTATUS \[TRANSSTATUS\]**.
    3. A la columna **Microsoft Dataverse**, seleccioneu **msdyn\_invoicestatus \[invoice status\]**.
    4. A la columna **Tipus d'assignació**, seleccioneu la fletxa dreta (**\>**).
    5. Al quadre de diàleg que apareix, al camp **Direcció de sincronització**, seleccioneu **Dataverse a aplicacions de finances i operacions**.
    6. Seleccioneu **Afegeix transformació**.
    7. Al camp **Tipus de transformació**, seleccioneu **ValueMap**.
    8. Seleccioneu **Afegeix una assignació de valors**.
    9. Al camp de l'esquerra, introduïu **4**. Al camp de la dreta, introduïu **192350001**. 
    10. Seleccioneu **Desa** i tanqueu el quadre de diàleg.

4. Seleccioneu **Desa com a** per desar la versió de l'assignació de doble escriptura. 
5. A la subfinestra **Afegeix una taula**, al camp **Editor**, seleccioneu **Editor per defecte**.
6. Al camp **Versió**, introduïu la versió.
7. Al camp **Descripció**, introduïu una nota sobre aquesta versió de retallada de l'assignació. 
8. Seleccioneu **Desa**.
9. Inicieu l'assignació.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar les fites facturades a l'entorn del Dataverse

1. A l'entorn del Project Operations del Dataverse, creeu fites que tinguin un estat de factura **Preparat per a factura**. En aquest moment, no migreu cap fita que no s'hagi facturat.

    > [!NOTE]
    > Abans de migrar les fites de facturació, assegureu-vos que les dimensions financeres relacionades amb la línia de contracte del projecte estiguin definides com estava previst. Les dimensions financeres no es poden editar un cop completada la migració.

2. Després de migrar totes les fites, atureu les assignacions de doble escriptura següents:

    - Fites de línia de contracte d'integració al Project Operations (msdyn\_contractlinescheduleofvalues)
    - Valors reals d'integració del Project Operations (msdyn\_actuals)
    - Proposta de factura de projecte V2 (factures)

    Per aturar les assignacions, seguiu aquests passos:

    1. Al Finance, aneu a **Administració de dades** \> **Doble escriptura**, seleccioneu una assignació i obriu-ne els detalls.
    2. Seleccioneu **Atura** i espereu fins que el sistema aturi l'assignació.

3. A l'entorn del Project Operations del Dataverse, creeu i confirmeu factures proforma per a les fites de facturació. 

    1. Al mapa del lloc, aneu als contractes del projecte, seleccioneu els contractes i, a continuació, seleccioneu **Crea factures**.
    2. Després de crear les factures, obriu-les des del menú **Factures** del mapa del lloc i seleccioneu **Confirma**.

    Aquest pas crea els registres necessaris a l'entorn del Dataverse. No obstant això, no afecta les finances i els comptes a cobrar, perquè les assignacions de doble escriptura enumerades anteriorment s'han aturat.

4. Després de confirmar totes les factures proforma, torneu totes les assignacions de doble escriptura al seu estat inicial.

    1. Torneu a la versió original l'assignació de doble escriptura de **Fites de línia de contracte d'integració del Project Operations** (**msdyn\_contractlinesscheduleofvalues**). 
    2. Seleccioneu l'assignació de doble escriptura a la llista de mapes, seleccioneu **Versió de l'assignació de taula** i, a continuació, seleccioneu la versió original de l'assignació de taula.
    3. Seleccioneu **Desa**.
    4. Reinicieu les assignacions de doble escriptura següents:

        - Fites de línia de contracte d'integració al Project Operations (msdyn\_contractlinescheduleofvalues)
        - Valors reals d'integració del Project Operations (msdyn\_actuals)
        - Proposta de factura de projecte V2 (factures)

Les fites es migren i el sistema està preparat per als passos següents de l'activitat de retallada.
