---
title: Configuració i aplicació de les dades de configuració al Common Data Service
description: En aquest tema es proporciona informació sobre com configurar i aplicar les dades de configuració al Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642216"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configuració i aplicació de les dades de configuració al Common Data Service 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Requisits previs

Abans de començar a configurar les dades al Common Data Service (CDS), s'han de complir els següents requisits previs:

1.  Proveir un entorn del CDS i un entorn del Dynamics 365 Finance per al Project Operations.
2.  La informació de les entitats jurídiques del Dynamics 365 Finance es comparteix a l'entorn del CDS. Això significa que l'entitat **Empresa** al CDS té els següents registres d'empresa:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Configuració de la instal·lació i dades de configuració

1. Baixeu, desbloquegeu i descomprimiu el [paquet de dades d'instal·lació i configuració](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Aneu a la carpeta descomprimida i executeu el fitxer executable, *DataMigrationUtility*.
3. A la pàgina 1 de l'auxiliar de configuració de la migració del Common Data Service (CMT), seleccioneu **Importa les dades** i, a continuació, seleccioneu **Continua**.

![Migració de la configuració](./media/1ConfigurationMigration.png)

4. A la pàgina 2 de l'auxiliar CMT, seleccioneu **Microsoft 365** com a **Tipus d'implementació**.
5. Marqueu les caselles **Mostra una llista d'organitzacions disponibles** i **Mostra les opcions avançades**.
6. Seleccioneu la regió del vostre inquilí, introduïu les credencials i seleccioneu **Inicia la sessió**.

![Inici de sessió de configuració](./media/2ConfigurationSignin.png)

7. A la pàgina 3, a la llista d'organitzacions de l'inquilí, seleccioneu l'organització a la qual voleu importar les dades de demostració i feu clic a **Inicia la sessió**.
8. A la pàgina 4, seleccioneu el fitxer zip *MasterAndSetupData* de la carpeta desempaquetada.

![Selecció del fitxer ZIP](./media/3ZipFile.png)

![Permet seleccionar un fitxer.](./media/4SelectAFile.png)

9. Després de seleccionar el fitxer zip, seleccioneu **Importa les dades**.

![Importa les dades](./media/5ImportData.png)

10. La importació s'executarà durant aproximadament dos-deu minuts en funció de la velocitat de la xarxa. Després de completar-se la importació, sortiu de l'auxiliar de CMT. 
11. Consulteu a la vostra organització les dades de les següents 19 entitats:

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

## <a name="update-project-operations-configurations"></a>Actualitzar les configuracions del Project Operations

1. Navegueu a l'entorn del CE. Podeu trobar-la obrint el [centre d'administració del Power Platform](https://admin.powerplatform.microsoft.com/environments), seleccionant l'entorn i, a continuació, seleccionant **Obre l'entorn**. 

![Obrir l'entorn](./media/7OpenEnvironment.png)

2. Aneu a **Projectes** > **Recursos** i, a continuació, seleccioneu **Nou** per crear un recurs reservable per a l'usuari.

![Recursos que es poden reservar](./media/8BookableResources.png)

3. A la pestanya **General**, seleccioneu el vostre usuari d'administració. Verifiqueu que el fus horari coincideixi amb el fus en què us trobeu. 

![Nou recurs que es pot reservar](./media/9NewBookableResource.png)

4. A la pestanya **Planificació**, al camp **Empresa**, trieu l'empresa **USPM** i, a continuació, seleccioneu **Desa**. 

![Pestanya Planificació](./media/10SchedulingTab.png)

5. Seleccioneu la pestanya **Hores de treball**.  

![Hores de feina](./media/11WorkHours.png)

6. Feu doble clic a qualsevol valor del calendari i seleccioneu **Edita** > **Tots els esdeveniments de la sèrie**. 

![Calendari de treball](./media/12WorkCalendar.png)

7. Canvieu les hores de treball a una jornada de treball de vuit (8) hores, marqueu els caps de setmana com a dies inhàbils i assegureu-vos que el fus horari coincideixi amb el vostre. 
8. Seleccioneu **Desa i tanca**.

![Actualitzar el calendari](./media/13UpdateCalendar.png)

9. Aneu a **Configuració** > **Plantilles de calendari** i seleccioneu **Nova**.
 
 ![Plantilles de calendari](./media/14CalendarTemplates.png)
 
 10. Introduïu un nom, seleccioneu el recurs de la plantilla que heu creat i, a continuació, seleccioneu **Desa**. 
 
 ![Desar la plantilla de calendari](./media/15SaveCalendarTemplate.png)
 
 11. Aneu a **Paràmetres** i feu doble clic al registre. 
 
 ![Paràmetres del projecte](./media/16ProjectParameters.png)
 
12. Actualitzeu els camps següents:

 - **Empresa per defecte**: USPM
 - **Unitat organitzativa per defecte**: Contoso Robotics Global
 - **Freqüència de factura**: setè i últim dia
 - **Plantilla d'hores de treball**: canvieu-ho a la plantilla que heu creat.

13. Seleccioneu **Desa**. 

![Paràmetres del projecte actualitzats](./media/17UpdatedProjectParameters.png)
