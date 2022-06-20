---
title: Aplicació de la configuració de la demostració i les dades de configuració (bàsic)
description: En aquest article s'ofereix informació sobre com aplicar la configuració de la demostració i les dades de configuració per a les operacions del projecte.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 68e504dd031596b295b1383a8e81621744cae8d2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922302"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Aplicació de la configuració de la demostració i les dades de configuració per al Project Operations (bàsic) 

_**Implementació bàsica: acord a facturació proforma_



## <a name="prerequisites"></a>Requisits previs

Abans de començar la configuració, heu de tenir un entorn del Common Data Service (CDS) proveït per al Dynamics 365 Project Operations.


## <a name="instructions"></a>Instruccions

1. Baixeu el [paquet de dades mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Aneu a la carpeta *ProjOpsSampleSetupData - CE only CMT* i executeu el fitxer executable, *DataMigrationUtility*.
3. A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.

    ![Migració de la configuració.](./media/1ConfigurationMigration.png)

4. A la pàgina 2 de l'auxiliar CMT, seleccioneu **Microsoft 365** com a **Tipus d'implementació**.
5. Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.
6. Seleccioneu la regió del vostre inquilí, introduïu les credencials i, a continuació, seleccioneu **Inicia la sessió**.

   ![Inici de sessió de configuració.](./media/2ConfigurationSignin.png)

7. A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i, a continuació, feu clic a **Inicia la sessió**.
8. A la pàgina 4, seleccioneu el fitxer zip, *SampleSetupAndConfigData* de la carpeta desempaquetada, *ProjOpsSampleSetupData - CE only CMT*.

   ![Fitxer zip.](./media/3ZipFile.png)

   ![Seleccioneu un fitxer.](./media/4SelectAFile.png)

9. Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.

   ![Importa dades.](./media/5ImportData.png)

10. La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa. Després de completar-se, sortiu de l'auxiliar de CMT. 
11. Consulteu a la vostra organització les dades de les següents 18 entitats:

    -   Moneda
    -   Compte
    -   Unitat organitzativa
    -   Contacte
    -   Unitat
    -   Grup d’unitats
    -   Llista de preus
    -   Llista de preus del paràmetre de projecte 
    -   Freqüència de facturació
    -   Categoria de recursos que es poden reservar
    -   Categoria de transacció
    -   Categoria de despesa
    -   Preu per funció
    -   Preu de categoria de transacció
    -   Característica
    -   Recurs que es pot reservar
    -   Associació de categoria de recursos que es poden reservar
    -   Característica dels recursos que es poden reservar

    ![Importació completada.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
