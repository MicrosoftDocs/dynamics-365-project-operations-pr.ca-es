---
title: Addició de camps personalitzats obligatoris a la configuració de preus i a entitats transaccionals
description: En aquest tema es proporciona informació sobre com afegir referències de camps personalitzats obligatoris a entitats i a formularis i visualitzacions.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c324e0e8797d0b6d3a06ffc2a40b787a475c49b5
ms.sourcegitcommit: 16c442258ba24c79076cf5877a0f3c1f51a85f61
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4590889"
---
# <a name="add-required-custom-fields-to-price-setup-and-transactional-entities"></a>Addició de camps personalitzats obligatoris a la configuració de preus i a entitats transaccionals

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest tema s'assumeix que heu completat els procediments en el tema [Crear camps i entitats personalitzats per utilitzar-los com a dimensions de preus](create-custom-fields-entities-pricing-dimensions.md). Si no heu completat aquests procediments, aneu enrere per completar-los torneu a aquest tema. 

En aquest tema, els procediments us mostraran com afegir les referències de camp personalitzades necessàries a les entitats i als elements de la interfície d'usuari (IU), com ara formularis i visualitzacions.

## <a name="add-custom-pricing-dimension-fields"></a>Afegeix camps de dimensió de preus personalitzats 
Quan s'han creat camps i entitats personalitzats, el pas següent és fer que les entitats de configuració de preus i transaccionals reconeguin qualsevol entitat o conjunt d'opcions personalitzades creant camps de referència. En funció de si la llista de dimensions de preus de preus inclou dimensions o dimensions de l'entitat de conjunt d'opcions o ambdues, seguiu només els passos a **Dimensions de preus personalitzades basades en el conjunt d'opcions** o **Dimensions de preus personalitzades basades en l'entitat**, o ambdues, respectivament.

### <a name="option-set-based-custom-pricing-dimensions"></a>Dimensions de preus personalitzades basades en conjunts d'opcions
Quan una dimensió de preus personalitzada està basada en un conjunt d'opcions, afegiu-la com a camp a entitats clau. En el procediment següent, s'utilitzen **Ubicació de treball del recurs** i **Hores de treball del recurs** com a dimensions de preu basades en un conjunt d'opcions. Primer s'han d'afegir com a camps a les entitats de preus, **Preu per funció** i **Marge comercial del preu per funció**.

1. Al Project Operations, seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Preu per funció**.
3. Expandiu l'entitat **Preu per funció** i seleccioneu **Camps**.
4. Seleccioneu **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu **Conjunt d'opcions** com a tipus de camp. 
5. Seleccioneu **Utilitza una conjunt d'opcions existent**, seleccioneu el conjunt d'opcions **Ubicació de treball del recurs** i, a continuació, seleccioneu **Desa**.
6. Repetiu els passos 1-5 per afegir aquest camp a l'entitat **Marge comercial del preu per funció**. 
7. Repetiu els passos 1-5 per al conjunt d'opcions **Hores de treball del recurs**.

> [!IMPORTANT]
> Quan afegiu un camp a més d'una entitat, utilitzeu el mateix nom de camp a totes les entitats. 

> ![Afegir Ubicació de treball del recurs al preu per funció](media/RWL-Field.png)

En les fases de vendes i estimació d'un projecte, les estimacions de l'esforç de treball necessari per completar treball **Local** i **In situ** a **Hores normals** i **Hores extres** s'utilitzen per calcular el valor de l'oferta o el projecte. S'afegiran els camps **Ubicació de treball del recurs** i **Hores de treball del recurs** a les entitats d'estimació, **Detall de la línia d'oferta**, **Detall de la línia de contracte**, **Membre de l'equip del projecte** i **Línia d'estimació**.

1. Al Project Operations, seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Detall de la línia d'oferta**.
3. Expandiu l'entitat **Detall de la línia d'oferta** i seleccioneu **Camps**.
4. Seleccioneu **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu el tipus de camp **Conjunt d'opcions**. 
5. Seleccioneu **Utilitza una conjunt d'opcions existent** i **Ubicació de treball del recurs** i, a continuació, seleccioneu **Desa**.
6. Repetiu els passos 1-5 per afegir aquest camp a les entitats **Detall de la línia de contracte del projecte**, **Membre de l'equip del projecte** i **Línia d'estimació**.
7. Repetiu els passos 1-6 per al conjunt d'opcions **Hores de treball del recurs**. 

> ![Afegir Ubicació de treball del recurs a Línia d'estimació](media/RWL-Default-Value.png)

Per al lliurament i la facturació, el treball completat ha de tenir un preu precís per seleccionar si s'ha realitzat **Local** o **In situ**, i si es va completar durant **Hores normals** o **Hores extres** a Valors reals del projecte. S'han d'afegir els camps **Ubicació de treball del recurs** i **Hores de treball del recurs** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.

1. Seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**.
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Entrada de temps**.
3. Expandiu l'entitat **Detall de la línia d'oferta** i, a continuació, seleccioneu **Camps**.
4. Seleccioneu **Nou** per crear un camp nou anomenat **Ubicació de treball del recurs** i seleccioneu **Conjunt d'opcions** com a tipus de camp. 
5. Seleccioneu **Utilitza una conjunt d'opcions existent**, seleccioneu el conjunt d'opcions **Ubicació de treball del recurs** i, a continuació, seleccioneu **Desa**.
6. Repetiu els passos 1-5 per afegir aquest camp a les entitats **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.
7. Repetiu els passos 1-6 per al conjunt d'opcions **Hores de treball del recurs**. 

> ![Afegir Ubicació de treball del recurs a una entrada de temps](media/RWL-time-entry.png)

Això completa els canvis d'esquema necessaris per a les dimensions personalitzades basades en conjunts d'opcions.

## <a name="entity-based-custom-pricing-dimensions"></a>Dimensions de preus personalitzades basades en entitats

Quan la dimensió de preus personalitzada és una entitat, hi afegireu relacions 1:N entre l'entitat de la dimensió i les entitats clau. Utilitzant de l'exemple de càrrec estàndard anterior, és raonable esperar que cada empleat tingui assignat un càrrec estàndard. Per tant, necessitareu una relació 1:N de Càrrec estàndard a Recurs que es pot reservar o una relació N:1 si s'ha creat des de Recurs que es pot reservar a Càrrec estàndard.

1. Al Project Operations, seleccioneu **Configuració** > **Solucions** i feu doble clic a **Dimensions de preus de \<your organization name>**. 
2. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.
3. Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.
4. Seleccioneu **Nou** per crear una relació 1:N nova anomenada **Càrrec estàndard a Recurs que es pot reservar**. Introduïu la informació requerida i seleccioneu **Desa**.

> ![Afegir Càrrec estàndard com a camp de referència a Recurs que es pot reservar](media/ST-BR.png)

El Càrrec estàndard també s'haurà d'afegir a les entitats de preus, **Preu per funció** i **Marge comercial del preu per funció**. Això també es completa utilitzant relacions 1:N entre les entitats **Càrrec estàndard** i **Preu per funció** i les entitats **Càrrec estàndard** i **Preu per funció**.

1. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.
2. Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.
3. Seleccioneu **Nou** per crear una relació 1:N nova anomenada **Càrrec estàndard a Preu per funció**. Introduïu la informació requerida i seleccioneu **Desa**.
4. Repetiu els passos 1-4 per crear relacions 1:N entre les entitats **Càrrec estàndard** i **Marge comercial del preu per funció**.

En les fases de vendes i estimació per al projecte, per posar un preu a l'oferta/projecte, les estimacions de l'esforç de treball són necessàries per a cada càrrec estàndard. Això significa que les relacions 1:N des de Càrrec estàndard a cadascuna d'aquestes entitats d'estimació són necessàries: 

- **Detall de la línia d'oferta**
- **Detall de la línia de contracte del projecte**
- **Membre de l'equip del projecte**
- **Línia d'estimació**

5. Repetiu els passos 1-5 per crear relacions 1:N des de **Càrrec estàndard** a **Detall de la línia d'oferta**, **Detall de la línia de contracte del projecte**, **Membre de l'equip del projecte** i **Línia d'estimació**.

> ![Afegir Càrrec estàndard com a camp de referència a Línia d'estimació](media/ST-Estimate-Line.png)

  En les fases de lliurament i de facturació, els treballs completats per cada càrrec estàndard han de tenir un preu precís a Valors reals del projecte. Això vol dir que hi ha d'haver relacions 1:N des de **Càrrec estàndard** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.

6. Repetiu els passos 1-6 per crear relacions 1:N des de **Càrrec estàndard** a les entitats **Entrada de temps**, **Valor real**, **Detall de la línia de factura** i **Línia del llibre diari**.

> ![Afegir Càrrec estàndard com a camp de referència a Entrada de temps](media/ST-Mapping.png)

### <a name="set-up-dimension-value-defaulting-using-the-mappings-features-of-the-platform"></a>Configurar el valor de la dimensió per defecte amb les característiques d'assignacions de la plataforma
Per a l'entrada de temps, seria útil tenir el valor per defecte del sistema a l'entrada de temps del recurs disponible que està registrant l'entrada de temps. Seguiu aquests passos per afegir assignacions de camp a la relació 1:N des de **Recurs que es pot reservar** a **Entrada de temps**.

1. A l'Explorador de solucions, a la subfinestra de navegació esquerra, seleccioneu **Entitats > Càrrec estàndard**.
2. Expandiu l'entitat **Càrrec estàndard** i seleccioneu **Relacions 1:N**.
3. Feu doble clic a **Recurs que es pot reservar a Entrada de temps**. A la pàgina **Relació**, seleccioneu **Utilitza assignacions de camps**. 
4. Seleccioneu **Nou** per crear una assignació de camp nova entre el camp **Càrrec estàndard** a l'entitat **Recurs que es pot reservar** al camp de referència **Càrrec estàndard** a l'entitat **Entrada de temps**. 

> ![Configurar les assignacions de camps per permetre l'assignació per defecte de Càrrec estàndard de Recurs disponible a Entrada de temps](media/ST-Mapping2.png)

Això completa els canvis d'esquema necessaris per a les dimensions personalitzades basades en entitats.

##  <a name="add-custom-fields-to-forms-views-and-business-rules"></a>Afegir camps personalitzats a formularis, visualitzacions i regles de negocis.

Després d'haver fet tots els canvis d'esquema necessaris, el pas següent és fer que els camps siguin visibles a la interfície d'usuari afegint els camps als formularis i a les visualitzacions.

1. Obriu el formulari o la visualització. A la subfinestra de navegació dreta, seleccioneu el camp i arrossegueu-lo al llenç del formulari. 
2. Si esteu editant una visualització, utilitzeu la subfinestra de navegació dreta, seleccioneu **Afegeix camps** i, al quadre de diàleg **Llista de camps**, seleccioneu els camps que necessiteu i seleccioneu **D'acord**.

La taula següent proporciona una llista exhaustiva dels formularis i les visualitzacions de fàbrica, llistats per entitat, que s'han d'actualitzar amb els nous camps. Si teniu visualitzacions o formularis addicionals a les personalitzacions d'aquestes entitats, afegiu també els camps nous.

| Entity        | Formularis que necessiten el nou camp   |Visualitzacions que necessiten el nou camp      |
| ------------------------------|---------------------------------|----------------------------------|
|  Preu per funció|• Informació |• Preus de categories de recursos actius<br> • Visualització associada de preus de categories de recursos|
|  Marge comercial de preu de funció|• Informació|• Marge comercial de preu de funcions actives<br>• Visualització associada de marge comercial de preus de la funció|
|  Detall de la línia d'oferta|• Informació del projecte<br>• Creació ràpida de projectes|• Detall de la línia d'oferta activa<br>• Detalls de la línia d'oferta combinada<br>• Visualització associada de detall de la línia d'oferta|
|  Detall de la línia de contracte del projecte|• Informació del projecte<br>• Creació ràpida de projectes|• Detalls de la línia de contracte combinada<br>• Detalls de la línia de contracte activa<br>• Visualització associada de detalls de la línia de contracte|
|  Membre de l'equip del projecte|• Informació<br>• Formulari nou|• Membres de l'equip del projecte actius<br>• Membres de l'equip del projecte<br>• Visualització associada de membres de l'equip del projecte|
|  Entrada de temps|• Informació<br>• Crear entrada de temps|• Les meves entrades de temps per data<br>• Les meves entrades de temps aquesta setmana<br>• Entrades de temps pendents d'aprovació|
|  Línia del llibre diari|• Informació<br>• Creació ràpida:|• Línies del llibre diari actives<br>• Visualització associada de les línies del llibre diari|
|  Detall de la línia de factura|• Informació<br>• Creació ràpida:|• Detalls de la línia de factura activa<br>• Transaccions de factura imputables<br>• Transaccions de factura gratuïtes<br>• Visualització associada de detall de la línia de factura<br>• Transaccions de factura no imputables|
|  Real|• Informació<br>• Valors reals actius|• Visualització associada de valors reals|

Els camps personalitzats també s'han d'afegir a les regles de negocis en funció del que hàgiu definit. Un exemple de fàbrica és per a la regla de negocis **Capacitat d'edició de l'entrada de temps basada en l'estat**. Aquesta regla defineix quins camps s'han de blocar quan l'entrada de temps es troba en un estat no editable com ara **Aprovada**. Afegiu camps a aquesta regla de negocis per tal que els camps estiguin blocats per editar-se quan l'entrada de temps es trobi en un estat que no sigui **Esborrany** o **Retornada**.
