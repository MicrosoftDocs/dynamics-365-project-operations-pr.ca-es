---
title: Migrar les fites de facturació totalment facturades a cutover
description: En aquest article s'explica com migrar les fites de facturació a preu fix que s'han facturat al client per contractes de projecte oberts abans de la data de sortida.
author: sigitac
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d7bb3dbb5acd9be447c405ec17f18d00c500f655
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912228"
---
# <a name="migrate-fully-invoiced-billing-milestones-at-cutover"></a>Migrar les fites de facturació totalment facturades a cutover

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="scenario"></a>Escenari

Contoso està en marxa amb Microsoft Dynamics 365 Project Operations per a escenaris de recursos / no emmagatzemats. Com a part de les activitats de retallada, l'equip d'implementació ha de migrar contractes de projectes oberts des de l'antic sistema. Alguns dels contractes del projecte inclouen línies de contracte que utilitzen el mètode de facturació de preu fix i ja s'han facturat parcialment al client final. L'equip d'implementació ha de migrar aquestes fites de facturació com a **factura del client publicada**, ja que s'han d'incloure al valor total del contracte a efectes de reconeixement d'ingressos. No obstant això, els saldos de clients en comptes a cobrar i llibre major general no s'han de veure afectats.

## <a name="solution"></a>Solució

### <a name="prerequisites"></a>Requisits previs

- Dynamics 365 Finance 10.0.24 o posterior s'ha d'instal·lar.
- L'entorn on es completaran els passos de migració ha d'estar en mode de manteniment. No s'han de realitzar altres activitats mentre es migren les fites.
- Els passos de migració s'han de seguir exactament com es descriu aquí i només es poden utilitzar per a l'activitat de retallada. Microsoft no admet cap altre ús d'aquesta capacitat.

### <a name="create-a-cutover-version-of-the-project-operations-integration-contract-line-milestones-dual-write-map"></a>Crea una versió retallada del mapa de fites de la línia de contracte d'integració d'operacions del projecte 

1. Assegureu-vos que l'assignació de destinació de l'entitat **fites** de la línia de contracte d'integració de projectes estigui actualitzada. 

    1. A Finances, aneu a **Entitats** de dades d'administració de \>**dades** de dades i seleccioneu l'entitat fites **de la línia de contracte d'integració d'operacions** del projecte. 
    2. Seleccioneu **Modifica les assignacions** de destinació. 
    3. A la pàgina Designació per a la **destinació**, seleccioneu **Genera l'assignació** i, a continuació, confirmeu que voleu generar l'assignació.

2. Atura i actualitza el mapa de doble escriptura de la **línia** de contracte d'integració d'operacions de projecte (**msdyn\_ contractlinescheduleofvalues**). 

    1. Aneu a **Administració** \> **de dades De doble escriptura**, seleccioneu el mapa i obriu-ne els detalls. 
    2. Seleccioneu Atura **i espereu** fins que el sistema aturi el mapa. 
    3. Seleccioneu **Actualitza les taules**.

3. Afegeix una assignació per a l'estat de la transacció.

    1. Seleccioneu **Afegeix una assignació**.
    2. A la nova línia, a la columna d'aplicacions **de** Finances i Operacions, seleccioneu el **camp TRANSSTATUS \[TRANSSTATUS\]**.
    3. A la **Microsoft Dataverse** columna, seleccioneu **l'estat de la factura de l'msdyn\_ invoicestatus\[\]**.
    4. A la **columna Tipus** mapa, seleccioneu la fletxa dreta (**\>**).
    5. Al quadre de diàleg que apareix, al camp Direcció de sincronització **, seleccioneu** a Les aplicacions **Dataverse Finances i Operacions.**
    6. Seleccioneu **Afegeix una transformació**.
    7. Al camp Transforma el **tipus**, seleccioneu **Mapa de valor**.
    8. Seleccioneu **Afegeix l'assignació de valors**.
    9. Al camp esquerre, introduïu **4**. Al camp dret, introduïu **192350001**. 
    10. Seleccioneu **Desa** i tanqueu el quadre de diàleg.

4. Seleccioneu **Desa com** a per desar la versió del mapa de doble escriptura. 
5. A la **subfinestra Afegeix taula**, al **camp Editor**, seleccioneu **Editor** per defecte.
6. **Al camp Versió**, introduïu la versió.
7. **Al camp Descripció**, introduïu una nota sobre aquesta versió de tall del mapa. 
8. Seleccioneu **Desa**.
9. Comença el mapa.

### <a name="migrate-invoiced-milestones-to-the-dataverse-environment"></a>Migrar les fites facturades a l'entorn Dataverse

1. A l'entorn Operacions Dataverse del projecte, creeu fites que tinguin un estat de factura de **Preparat per a la facturació**. En aquest punt, no migreu cap fita que no s'hagi facturat.

    > [!NOTE]
    > Abans de migrar les fites de facturació, assegureu-vos que les dimensions financeres relacionades amb la línia de contracte del projecte es defineixin com s'esperava. Les dimensions financeres no es poden editar un cop finalitzada la migració.

2. Després de migrar totes les fites, atureu els següents mapes de doble escriptura:

    - Fites de la línia de contracte d'integració d'operacions de projectes (msdyn\_ contractlinescheduleofvalues)
    - Valors reals d'integració del Project Operations (msdyn\_actuals)
    - Proposta de factura de projecte V2 (factures)

    Per aturar els mapes, seguiu aquests passos:

    1. A Finances, aneu a **Gestió** \> **de dades De doble escriptura**, seleccioneu un mapa i obriu-ne els detalls.
    2. Seleccioneu Atura **i espereu** fins que el sistema aturi el mapa.

3. A l'entorn Operacions Dataverse del projecte, creeu i confirmeu factures proforma per a les fites de facturació. 

    1. Al mapa del lloc, aneu als contractes del projecte, seleccioneu els contractes i, a continuació, seleccioneu **Crea factures**.
    2. Després de crear les factures, obriu-les **al menú Factures** del mapa del lloc i, a continuació, seleccioneu **Confirma**.

    Aquest pas crea els registres necessaris a l'entorn Dataverse. No obstant això, no afecta els financers i els comptes a cobrar, ja que els mapes de doble escriptura anteriorment llistats es van aturar.

4. Després de confirmar totes les factures proforma, retorneu tots els mapes de doble escriptura al seu estat inicial.

    1. Actualitzeu la versió del mapa de línia **de contracte d'integració** d'operacions del projecte (**msdyn\_ contractlinescheduleofvalues**) de tornada a l'original. 
    2. Seleccioneu el mapa de doble escriptura a la llista de mapes, seleccioneu **La versió** del mapa de la taula i, a continuació, seleccioneu la versió original del mapa de la taula.
    3. Seleccioneu **Desa**.
    4. Reinicieu els següents mapes de doble escriptura:

        - Fites de la línia de contracte d'integració d'operacions de projectes (msdyn\_ contractlinescheduleofvalues)
        - Valors reals d'integració del Project Operations (msdyn\_actuals)
        - Proposta de factura de projecte V2 (factures)

Les fites ara estan migrades, i el sistema està preparat per als propers passos en l'activitat de retallada.
