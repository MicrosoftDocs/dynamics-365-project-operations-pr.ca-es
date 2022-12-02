---
title: Sincronitzar l'estat del projecte per evitar l'entrada en projectes tancats
description: En aquest article s'explica com sincronitzar l'estat del projecte per evitar les entrades en projectes inactius o tancats.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348100"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronitzar l'estat del projecte per evitar l'entrada en projectes tancats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="scenario"></a>Escenari

Contoso està actiu amb el Microsoft Dynamics 365 Project Operations per als escenaris de recursos/no mantinguts en existències. Com a part de les activitats empresarials normals, és possible que els projectes s'hagin completat o retingut. Podeu desactivar el projecte per assegurar-vos que no es generen despeses ni factures.

## <a name="solution"></a>Solució

### <a name="prerequisites"></a>Requisits previs

-   Cal que hi hagi instal·lat el Microsoft Dynamics 365 Finance 10.0.29 o posterior.
-   Les assignacions de doble escriptura 1.0.0.3 per al Projects V2 (msdyn\_projects) s'han d'instal·lar o configurar manualment com s'explica a continuació.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Crear una versió actualitzada de l'assignació de doble escriptura de la integració del Project Operations Projects V2

Per actualitzar l'assignació de doble escriptura del Project Operations Projects V2:

1. Aneu a l'àrea de treball **Administració de dades** i seleccioneu **Escriptura doble**.
2. Seleccioneu la peça **Escriptura doble**.
3. a la columna **Assignació de taula**, localitzeu i seleccioneu **Project V2 (msdyn\_projects)** i, a continuació, seleccioneu Atura.
4. Seleccioneu el nom de l'assignació per obrir-la i, a continuació, seleccioneu **[Cap]**.
5. Al quadre de diàleg Selecció de columnes, seleccioneu **statecode \[Project Status\]** i, a continuació, seleccioneu D'acord. Podeu escriure **state** al valor de filtre per reduir la llista.
6.  Seleccioneu **Afegeix o edita la transformació** a la columna del **tipus d'assignació** per editar la transformació.
7.  A **Tipus de transformació**, seleccioneu **ValueMap**.
8.  Seleccioneu **Afegeix una assignació de valors** i, a continuació, afegiu les **claus** i els **valors** següents:

   Tecla       | Valor 
   ----------|-------
   InProcess | 0     
   Completat | 1     

![Captura de pantalla que mostra l'assignació de doble escriptura](media/projectstage-dw-mapping.png)

9. Seleccioneu **Desa**.
10. A la part superior de la pàgina **Escriptura doble > Projects V2 (msdyn_projects)**, seleccioneu **Desa com a**.
11. A **Afegeix una taula** al camp **Editor**, seleccioneu **CDS Default Publisher**.
12. Definiu el camp **Versió** en 1.0.0.3.
13. Escriviu una **descripció** i, a continuació, seleccioneu **Desa**.
14. A la part superior de la pàgina **Escriptura doble > Projects V2 (msdyn_projects)**, seleccioneu **Executa** per iniciar l'assignació i, a continuació, seleccioneu **Sí** si heu de confirmar perquè s'executi. 

### <a name="close-a-newly-completed-project"></a>Tancar un projecte acabat de completar

El Dynamics 365 Finance utilitza el camp de **fase del projecte** per diferenciar entre projectes **en procés** o **finalitzats**. Els projectes **finalitzats** no poden incórrer en despeses ni facturar-se als clients.

1. Obriu un projecte per desactivar-lo.
2. Seleccioneu **Desactiva** a la franja.

> [!NOTE]
> Podeu desactivar o tancar un projecte perquè ambdues accions es comporten igual en el context de Finance.

3. A Finance, obriu la pàgina **Llista de tots els projectes**.
4. Confirmeu que el projecte desactivat no es mostra a la llista.
5. Al filtre **mostra els projectes** de sobre de la llista, canvieu el valor de **Actiu** a **Tot**.
6. Ara veureu el projecte desactivat.

Si intenteu registrar el temps o la despesa en aquest projecte a Finance, no hauríeu de veure el projecte per seleccionar-lo. Si introduïu manualment el número de projecte en una despesa, veureu un missatge com ara: "La fase del projecte acabada no permet el registre en el projecte". La facturació i altres funcions de facturació haurien d'estar inhabilitades perquè estaran en el context d'un projecte tancat.

