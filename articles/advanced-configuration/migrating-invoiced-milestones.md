---
title: Migrar les fites de facturació completament facturades a la retallada
description: En aquest article s'explica com migrar les fites de facturació a preu fix que s'han facturat al client per a contractes de projecte oberts abans de la data de publicació.
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
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar les fites de facturació completament facturades a la retallada

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="scenario"></a>Escenari

Contoso es publicarà amb Microsoft Dynamics 365 Project Operations per a escenaris de recursos o no emmagatzemats. Com a part de les activitats de retallada, l'equip d'implementació ha de migrar els contractes de projecte oberts des de l'antic sistema. Alguns dels contractes del projecte inclouen línies contractuals que utilitzen el mètode de facturació de preu fix i que ja s'han facturat parcialment al client final. L'equip d'implementació ha de migrar aquestes fites de facturació com a comptabilitzades a **les factures del** client, ja que s'han d'incloure al valor total del contracte a efectes de reconeixement d'ingressos. No obstant això, els saldos de clients en Comptes a cobrar i llibre major general no s'han de veure afectats.

## <a name="solution"></a>Solució

### <a name="prerequisites"></a>Requisits previs

- Dynamics 365 Finance 10.0.24 o posterior s'ha d'instal·lar.
- L'entorn on es completaran els passos de migració ha d'estar en mode de manteniment. No s'han de realitzar altres activitats mentre es migren les fites.
- Els passos de migració s'han de seguir exactament com es descriu aquí i només es poden utilitzar per a l'activitat de tall. Microsoft no admet cap altre ús d'aquesta capacitat.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Creeu una versió de retallada de les fites de la línia de contracte d'integració d'operacions del projecte de doble escriptura 

1. Assegureu-vos que l'assignació de destinació per a l'entitat **Fites del contracte d'integració d'Operacions** del Projecte estigui actualitzada. 

    1. A Finances, aneu a **Entitats de dades de gestió** \> **de dades** i seleccioneu l'entitat Fites del contracte d'integració **d'operacions** de projecte. 
    2. Seleccioneu **Modifica les assignacions de destinació**. 
    3. A la fase d'escenificació del **mapa a la pàgina de destinació**, seleccioneu **Genera l'assignació** i, a continuació, confirmeu que voleu generar l'assignació.

2. Atureu i actualitzeu les fites de la **línia de contracte d'integració d'operacions** de projecte (**msdyn\_ contractlinescheduleofvalues**) mapa de doble escriptura. 

    1. Aneu a **Gestió** \> **de dades De doble escriptura**, seleccioneu el mapa i obriu-ne els detalls. 
    2. Seleccioneu **Atura** i espereu fins que el sistema aturi el mapa. 
    3. Seleccioneu **Actualitza les taules**.

3. Afegiu una assignació per a l'estat de la transacció.

    1. Seleccioneu **Afegeix una assignació**.
    2. A la línia nova, a la **columna Aplicacions** de finances i operacions, seleccioneu el **camp TRANSSTATUS \[TRANSSTATUS\]**.
    3. A la **Microsoft Dataverse** columna, seleccioneu **l'estat\_ de la factura msdyn\[invoicestatus\]**.
    4. A la **columna Tipus** de mapa, seleccioneu la fletxa dreta (**\>**).
    5. Al quadre de diàleg que apareix, al camp Sincronitza la **direcció**, seleccioneu **Dataverse a Aplicacions financeres i operacions**.
    6. Seleccioneu **Afegeix una transformació**.
    7. Al camp Tipus de **transformació, seleccioneu** Mapa de valor **.**
    8. Seleccioneu **Afegeix una assignació** de valor.
    9. Al camp esquerre, introduïu **4**. Al camp de la dreta, introduïu **192350001**. 
    10. Seleccioneu **Desa** i, a continuació, tanqueu el quadre de diàleg.

4. Seleccioneu **Desa com** per desar la versió del mapa de doble escriptura. 
5. A la **subfinestra Afegeix taula**, al **camp Editor**, seleccioneu **Editor per** defecte.
6. **Al camp Versió**, introduïu la versió.
7. **Al camp Descripció**, introduïu una nota sobre aquesta versió de tall del mapa. 
8. Seleccioneu **Desa**.
9. Inicieu el mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar les fites facturades a l'entorn Dataverse

1. A l'entorn del Project Operations Dataverse, creeu fites que tinguin l'estat de factura a **Punt per a la** facturació. Arribats a aquest punt, no migreu cap fita que no s'hagi facturat.

    > [!NOTE]
    > Abans de migrar les fites de facturació, assegureu-vos que les dimensions financeres relacionades amb la línia de contracte del projecte s'estableixin com s'esperava. Les dimensions financeres no es poden editar un cop finalitzada la migració.

2. Després de migrar totes les fites, atureu els següents mapes de doble escriptura:

    - Fites de la línia de contracte d'integració d'operacions de projecte (msdyn\_ contractlinescheduleofvalues)
    - Valors reals d'integració del Project Operations (msdyn\_actuals)
    - Proposta de factura de projecte V2 (factures)

    Per aturar els mapes, seguiu aquests passos:

    1. A Finances, aneu a **Gestió** \> **de dades De doble escriptura**, seleccioneu un mapa i obriu-ne els detalls.
    2. Seleccioneu **Atura** i espereu fins que el sistema aturi el mapa.

3. A l'entorn del Project Operations Dataverse, creeu i confirmeu factures proforma per a les fites de facturació. 

    1. Al mapa del lloc, aneu als contractes del projecte, seleccioneu els contractes i, a continuació, seleccioneu **Crea factures**.
    2. Un cop creades les factures, obriu-les des del **menú Factures** del mapa del lloc i, a continuació, seleccioneu **Confirma**.

    Aquest pas crea els registres necessaris a l'entorn Dataverse. Tanmateix, no afecta les finances i els comptes a cobrar, ja que es van aturar els mapes de doble escriptura enumerats anteriorment.

4. Un cop confirmades totes les factures proforma, torneu tots els mapes de doble escriptura al seu estat inicial.

    1. Actualitzeu la versió de les fites **de la** línia de contracte d'integració de Project Operations (**msdyn\_ contractlinescheduleofvalues**) de doble escriptura al mapa de doble escriptura a l'original. 
    2. Seleccioneu el mapa de doble escriptura a la llista de mapes, seleccioneu **Versió del mapa de la taula** i, a continuació, seleccioneu la versió original del mapa de la taula.
    3. Seleccioneu **Desa**.
    4. Reinicieu els mapes de doble escriptura següents:

        - Fites de la línia de contracte d'integració d'operacions de projecte (msdyn\_ contractlinescheduleofvalues)
        - Valors reals d'integració del Project Operations (msdyn\_actuals)
        - Proposta de factura de projecte V2 (factures)

Les fites ara es migren i el sistema està preparat per als propers passos de l'activitat de tall.
