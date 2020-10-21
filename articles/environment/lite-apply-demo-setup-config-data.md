---
title: Aplicació de la configuració de la demostració i les dades de configuració
description: En aquest tema es proporciona informació sobre com aplicar la configuració de la demostració i les dades de configuració per al Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948757"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Aplicar la configuració de demostració i les dades de configuració per a la implementació bàsica del Project Operations: acord a la facturació proforma

_**Implementació bàsica: acord a facturació proforma_

1. Baixeu el [paquet de dades mestres](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Aneu a la carpeta *ProjOpsDemoDataSetupAndMaster - Integrated CMT* i executeu el fitxer executable, *DataMigrationUtility*.
3. A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.

![Migració de la configuració](./media/1ConfigurationMigration.png)

4. A la pàgina 2 de l'auxiliar CMT, seleccioneu **Office 365** com a **Tipus d'implementació**.
5. Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.
6. Seleccioneu la regió del vostre inquilí, introduïu les credencials i, a continuació, seleccioneu **Inicia la sessió**.

![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i, a continuació, feu clic a **Inicia la sessió**.
8. A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Fitxer zip](./media/3ZipFile.png)

![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.

![Importa dades](./media/5ImportData.png)

10. La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa. Després de completar-se, sortiu de l'auxiliar de CMT. 
11. Consulteu a la vostra organització les dades de les següents 20 entitats:

- Moneda
- Unitat organitzativa
- Contacte
- Grup d'impostos
- Grup de clients
- Unit
- Grup d’unitats
- Llista de preus
- Llista de preus del paràmetre de projecte
- Freqüència de facturació
- Detall de la freqüència de facturació
- Categoria de recursos que es poden reservar
- Categoria de transacció
- Categoria de despesa
- Preu per funció
- Preu de categoria de transacció
- Característica
- Recurs que es pot reservar
- Associació de categoria de recursos que es poden reservar
- Característica dels recursos que es poden reservar

![Importació completada](./media/6CompleteImport.png)
