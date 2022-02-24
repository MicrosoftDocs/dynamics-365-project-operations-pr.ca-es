---
title: Administració de les estimacions d'ingressos
description: En aquest tema es proporciona informació sobre com treballar amb estimacions d'ingressos per a projectes.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 98df0301eaa8e9f8e9cd51fc5714254ae3bbc83d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531363"
---
# <a name="manage-revenue-estimates"></a>Administració de les estimacions d'ingressos

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Podeu crear, calcular, comptabilitzar, revertir o suprimir estimacions d'ingressos. Podeu fer-ho manualment o mitjançant un procés periòdic. En aquest tema es proporciona informació sobre com treballar amb estimacions d'ingressos per a projectes.

### <a name="manage-revenue-estimates-manually"></a>Administració manual d'estimacions d'ingressos

Al projecte d'estimació d'ingressos de preu fix o a la pàgina **Consulta d'estimació** (**Gestió de projectes i comptabilitat** > **Informes i consultes** > **Consultes d'estimacions i informes**), seleccioneu **Estimacions**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Administració d'estimacions d'ingressos mitjançant un procés periòdic

Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions** i seleccioneu el procés corresponent.

## <a name="create-a-revenue-estimate"></a>Crear una estimació d'ingressos

Per crear una estimació d'ingressos, completeu els passos següents. 

1. Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions**.
2. Seleccioneu **Crea**. A la pàgina **Creació d'estimació**, seleccioneu els paràmetres següents:

   - **Codi de període**: aquest codi determina amb quina freqüència es publiquen les estimacions.
   - **Data d'estimació**: data de processament de l'estimació.
   - **Contínua**: activeu aquesta casella de selecció per crear estimacions només si les estimacions s'han publicat en el període anterior, o si l'estimació és la primera estimació que s'ha creat. Si no se selecciona, es creen estimacions encara que les estimacions no s'hagin publicat en el període anterior.
   - **Mètode de cost per completar**: definiu com calcular el treball restant del projecte. Per obtenir més informació, vegeu [Mètodes de cost per completar](cost-complete-methods.md).
   - **Mètode de compleció**: seleccioneu un mètode de compleció de les opcions següents:
     - **Automàtic**: el percentatge de compleció es calcula automàticament i es basa en les línies de cost incloses en el càlcul. La plantilla de cost defineix les línies de cost que s'inclouen.
     - **Manual**: el percentatge de compleció és igual al percentatge de compleció de l'última estimació. Un cop creada l'estimació, podeu canviar el **Càlcul manual** a la pàgina **Estimacions**.
     - **A partir de la plantilla de cost**: una combinació dels mètodes automàtic i manual. Aquesta opció s'estableix automàticament o manualment, depenent del valor per defecte de la plantilla de costos.
   - **Model de predicció**: seleccioneu un model de predicció per a l'estimació.
   - **Imprimir llista d'estimació**: creeu i mostreu una llista d'estimació. La llista conté l'estat de la funció actual. Podeu imprimir els advertiments sobre l'estimació de l'informe. Les condicions següents fan que apareguin advertiments a la llista d'estimació:
     - Un percentatge completat de més del 100 per cent.
     - Un percentatge completat de menys del zero per cent.
     - Una quantitat negativa a la columna **Per completar**.
     - Una estimació sense l'import del contracte corresponent.
     - Una estimació sense una estimació de costos adjunta.
   - **Mostra Infolog**: seleccioneu aquesta opció per rebre un missatge que contingui informació sobre els projectes d'estimació que s'han processat quan s'ha executat la feina.


## <a name="post-wip-or-accruals"></a>Publicar WIP o meritacions

Després de l'avaluació, les estimacions es mantenen, disminueixen o augmenten. A continuació, podeu publicar la WIP quan treballeu amb el principi d'avaluació de **Contracte completat** o publicar les meritacions quan treballeu amb el principi d'avaluació de **Percentatge completat**.
  
L'estat del període d'estimació canvia de **Creat** a **Publicat**.

## <a name="reverse-wip-or-accruals"></a>Revertir WIP o meritacions

Utilitzeu l'opció de revertir per abonar WIP o meritacions ja publicades i, a continuació, creeu estimacions per al període.

> [!NOTE]
> Per revertir un període que es troba entre altres períodes, revertiu els períodes d'estimació necessaris i, a continuació, torneu-los a publicar. Com que tots els períodes posteriors depenen de les estimacions del període anterior, no se salta cap període.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Suprimir el projecte d'estimació i acabar el projecte

L'últim pas en el procés d'estimació és suprimir el projecte d'estimació i acabar el projecte de preu fix quan el percentatge d'acabament arriba al 100 per cent.

El següent es produeix quan s'executa la supressió:

- Per a un projecte de preu fix amb un contracte completat, els valors de WIP s'esborren dels balanços i es publiquen als comptes de pèrdues i guanys.
- Per a un projecte de preu fix que tingui un percentatge completat, les meritacions s'eliminen dels comptes de pèrdues i guanys.

L'estimació canvia l'estat per **Eliminat**.

> [!NOTE]
> En casos especials, el percentatge pot prolongar-se més enllà del 100 per cent. Quan això passi, reduïu el percentatge completat mitjançant el **Mètode de cost per completar a zero** per arribar al 100 per cent.

## <a name="reverse-elimination"></a>Revertir supressió

1. Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Estimacions** > **Revertir supressió**. 
2. A la subfinestra Acció, a la pestanya **Procés**, al grup **Manteniment**, seleccioneu **Estimació**. 
3. Seleccioneu **Revertir supressió**.

Utilitzeu aquesta pàgina per revertir totes les supressions amb una data d'estimació especificada i amb un estat d'estimació de **Suprimit**. L'estat de la transacció canvia després de seleccionar els camps apropiats.

Això també canvia automàticament l'estat del projecte per **En procés** si la fase del projecte està definida com a acabada. L'estat de l'estimació del període de projecte canvia a **Publicat**.
