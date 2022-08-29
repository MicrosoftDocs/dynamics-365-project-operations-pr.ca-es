---
title: Sincronització de l'estat del projecte per evitar l'entrada contra projectes tancats
description: En aquest article s'explica com sincronitzar l'estat del projecte per evitar l'entrada contra projectes inactius o tancats.
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
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Sincronització de l'estat del projecte per evitar l'entrada contra projectes tancats

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

## <a name="scenario"></a>Escenari

Contoso està en contacte amb Microsoft Dynamics 365 Project Operations per a escenaris de recursos o no emmagatzemats. Com a part de les activitats empresarials normals, els projectes es poden completar o posar en suspens. Podeu inactivar el projecte per assegurar-vos que no es generen despeses ni factures.

## <a name="solution"></a>Solució

### <a name="prerequisites"></a>Requisits previs

-   Microsoft Dynamics 365 Finançament 10.0.29 o posterior s'ha d'instal·lar.
-   El mapa Dual Write 1.0.0.3 per als projectes V2 (projectes msdyn\_) s'ha d'instal·lar o configurar manualment tal com es descriu a continuació.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Creeu una versió actualitzada del mapa de doble escriptura de Project Operations Integration Projects V2

Per actualitzar el mapa de doble escriptura de Project Operations Projects V2:

1. Aneu a l'àrea **de treball Administració** de dades i seleccioneu **Escriptura dual**.
2. Seleccioneu el **mosaic de doble escriptura**.
3. Des de la columna del mapa **de la taula T**, localitzeu i seleccioneu **Projecte V2 (projectes msdyn\_)** i, a continuació, seleccioneu Atura.
4. Seleccioneu el nom del mapa per obrir el mapa i, a continuació, seleccioneu **[Cap]**.
5. Des del quadre de diàleg Selecciona la columna, seleccioneu **Estat del projecte de codi \[d'estat\]** i, a continuació, seleccioneu D'acord. Podeu escriure **estat** al valor del filtre per restringir la llista.
6.  Seleccioneu **Afegeix o edita una transformació** a la columna tipus **de** mapa per editar la transformació.
7.  Des **de Tipus de** transformació, seleccioneu **ValueMap**.
8.  Seleccioneu **Afegeix una assignació de** valors i, a continuació, afegiu les claus **i** valors **següents**:

   Tecla       | Valor 
   ----------|-------
   En Procés | 0     
   Completat | 1     

![Captura de pantalla que mostra l'assignació de doble escriptura](media/projectstage-dw-mapping.png)

9. Seleccioneu **Desa**.
10. A la part superior de la **pàgina Projectes > V2 (msdyn_projects)** de doble escriptura, seleccioneu **Desa com a**.
11. Des d'Afegeix **una taula** al **camp Editor**, seleccioneu **Editor** per defecte de CDS.
12. Definiu el **camp Versió** com a 1.0.0.3.
13. Escriviu una **descripció** i, a continuació, seleccioneu **Desa**.
14. Des de la part superior de la **pàgina > projectes V2 (msdyn_projects)** de doble escriptura, seleccioneu **Executa** per iniciar el mapa i, a continuació, seleccioneu **Sí** si se us demana que confirmeu abans d'executar-lo. 

### <a name="close-a-newly-completed-project"></a>Tancar un projecte acabat de finalitzar

Dynamics 365 Finance utilitza l'àmbit de l'etapa **del** projecte per diferenciar entre projectes **en procés** o **acabats**. **Els projectes acabats** no poden incórrer en despeses ni facturar-se als clients.

1. Obriu un projecte per desactivar-lo.
2. A la cinta, seleccioneu **Desactiva**.

> [!NOTE]
> Podeu desactivar o tancar un projecte, ja que tots dos es comportaran igual en el context de Finances.

3. A Finances, obriu la **pàgina Llista** de tots els projectes.
4. Confirmeu que el projecte desactivat no apareix a la llista.
5. Al filtre mostra projectes **que hi ha a sobre de la llista, canvieu el valor d'Actiu** **a** Tots **.**
6. Ara veureu el projecte desactivat.

Si intenteu registrar temps o despeses contra aquest projecte a Finances, no hauríeu de veure el projecte per a la selecció. Si introduïu manualment el número de projecte en una despesa, veureu un missatge com ara "La fase de projecte finalitzada no permet gravar al projecte". La facturació i altres funcions de facturació s'han de desactivar, ja que es faran en el context d'un projecte tancat.

