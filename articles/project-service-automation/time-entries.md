---
title: Crear entrades de temps
description: En aquest tema es proporciona informació sobre com crear entrades de temps.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749537"
---
# <a name="create-time-entries"></a>Crear entrades de temps

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En versions anteriors del Dynamics 365 Project Service Automation, les entrades de temps s'introduïen de manera setmanal. A la versió 3 del Project Service Automation, les entrades de temps s'introdueixen diàriament. No obstant això, després de crear algunes entrades de temps, podeu crear-ne més massivament o copiar-les.

## <a name="create-a-time-entry"></a>Crear una entrada de temps

Seguiu els passos que es descriuen a continuació per crear una entrada de temps.

1. A la pàgina **Entrades de temps**, seleccioneu **Nova**.
2. Al quadre de diàleg **Creació ràpida: entrada de temps**, introduïu la duració de l'entrada de temps en minuts, hores o dies. La duració s'ha d'escriure en el format següent: "*x* minuts", "*x* hores" o "*x* dies". Les hores i els dies també es poden escriure amb decimals, per exemple, "*x,x* hores" o "*x,x* dies".
3. Seleccioneu el tipus d'entrada de temps i el projecte per al qual introduïu l'entrada de temps.
4. Al camp **Tasca del projecte**, cerqueu la tasca per a l'entrada de temps.

    > [!NOTE]
    > Si esteu creant una entrada de temps per a una tasca que no està assignada a un usuari , al camp **Tasca del projecte**, seleccioneu el botó **Cerca**, seleccioneu **Canvia la visualització** i, a continuació, seleccioneu **Totes les tasques actives del projecte** per llistar totes les tasques.

5. Introduïu una descripció, si cal una descripció i, a continuació, seleccioneu **Desa i tanca**.

Després d'haver creat i desat l'entrada de temps, podeu editar-la a la quadrícula d'entrada de temps. La quadrícula d'entrada de temps admet dos formats:

- Podeu introduir entrades de temps en el format **hh:mm**. Aquest format es converteix en hores i fraccions.
- Podeu introduir hores i fraccions directament.

Heu de tenir en compte que les fraccions d'una hora no són minuts. Per tant, 1,5 hores representen 1 hora i 30 minuts. La mateixa regla s'aplica a les fraccions d'un dia. Un dia és de 24 hores, i 0,5 dies representen 12 hores.

## <a name="bulk-create-time-entries"></a>Crear entrades de temps massivament

Després de crear algunes d'entrades de temps, podeu copiar-les per crear entrades de temps addicionals massivament.

1. A la pàgina **Entrades de temps**, seleccioneu **Copia la setmana**.
2. Al grup de camps **Del període**, utilitzeu els camps **Data d'inici** i **Data de finalització** per definir l'interval de dates des d'on copiar entrades de temps.
3. Al grup de camps **Al període**, al camp **Data d'inici**, especifiqueu la data on crear les entrades de temps.
4. Seleccioneu **Copia** per crear una còpia de les entrades de temps que corresponen al dia de la setmana que s'especifica al grup de camps **Al període**. Per exemple, l'entrada de temps del dilluns de la setmana passada es copia al dilluns de la setmana especificada al grup de camps **Al període**.

## <a name="import-data-for-time-entries"></a>Importar dades d'entrades de temps

Podeu importar dades a partir de les reserves de projectes i assignacions. Quan importeu dades, podeu especificar l'interval de dates de les reserves que s'han d'importar i, a continuació, seleccionar explícitament les reserves que haurien de crear-se com a entrades de temps **Esborrany**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Agrupar, ordenar, cercar i filtrar capacitats

Podeu agrupar i filtrar entrades de temps per les dimensions que s'especifiquen a les columnes. Al camp **Agrupa per**, seleccioneu la dimensió que s'utilitzarà per filtrar les entrades de temps. També podeu ordenar els registres d'entrada de temps en ordre ascendent o descendent mitjançant la fletxa d'ordenació a les capçaleres de columna. A més, podeu mostrar o amagar les entrades seleccionant el botó **Filtra** a les capçaleres de columna i, a continuació, al quadre **Cerca**, introduint el text que s'hauria d'utilitzar per cercar entrades de temps pel nom del projecte, tasca de projecte, entrada de temps o recurs.
