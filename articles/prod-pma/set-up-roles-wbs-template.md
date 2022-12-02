---
title: Configurar funcions a les plantilles d'estructura del desglossament del treball
description: Aquest article proporciona informació sobre la configuració de la informació de les funcions a les plantilles d'estructura del desglossament del treball.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8721c5e5798c2b80c6f3eb65cef118d1ade5e680
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920784"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurar funcions a les plantilles d'estructura del desglossament del treball

[!include [banner](../includes/banner.md)]

Els administradors de projectes poden configurar les plantilles d'estructura del desglossament del treball (WBS) que poden aplicar-se quan creen una WBS per a nous projectes. Els administradors de projectes poden afegir funcions quan creen una plantilla. Utilitzeu el procediment següent per assignar una funció a una plantilla de WBS.

1. Seleccioneu **Administració de projectes i comptabilitat** > **Configuració** > **Projectes**  > **Plantilles d'estructura del desglossament del treball**.
2. Seleccioneu **Detalls** per a una plantilla de WBS seleccionada.
3. Seleccioneu una tasca a la llista i, a continuació, al camp **Funció**, seleccioneu una funció per assignar a la tasca.

## <a name="work-with-a-wbs"></a>Treballar amb una WBS

Podeu crear una WBS nova o bé copiar una WBS d'una plantilla de WBS existent. Un administrador de projectes pot administrar fàcilment els recursos assignant funcions a tasques noves a la WBS. Les funcions es poden reemplaçar bé després que s'hagi adquirit un recurs o després que s'identifiqui un recurs confirmat per treballar en la tasca. Aquesta flexibilitat permet que els administradors de projectes duguin a terme les tasques següents:

- Identificar el nombre de recursos necessaris per als paquets de treball de WBS.
- Estimar els costos dels projectes.
- Determinar un pressupost preliminar.
- Estimar la duració de l'activitat, segons les funcions i els recursos.
- Desenvolupar plans d'administració de projectes, segons la informació disponible del projecte.

S'ha afegit més opcions a la WBS per utilitzar millor la funcionalitat de recursos.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opció</th>
<th>Descripció</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Assignacions de recursos</td>
<td>Visualitzeu els recursos, les dates, el nombre d'hores i el tipus de reserva de les tasques a la WBS.</td>
</tr>
<tr class="even">
<td>Genera automàticament un equip</td>
<td>Afegiu automàticament recursos planificats mitjançant funcions que estan associades a una tasca. L'assignació suggereix automàticament els recursos planificades mitjançant una anàlisi de decisions de diversos criteris que es basa en funcions. Després que les funcions i l'esforç (hores) s'hagin definit per a les tasques en una WBS i després que s'hagi publicat l'estructura, seleccioneu <strong>Genera automàticament un equip</strong>. El nombre necessari de recursos planificats s'afegeix a la WBS i a la pestanya <strong>Planificació d'equips i projectes</strong>.</td>
</tr>
<tr class="odd">
<td>Recurs (llista desplegable)</td>
<td>A la pàgina <strong>Inicia l'assignació de recursos</strong>, podeu seleccionar recursos per reservar de manera fixa o flexible, segons la duració especificada. Podeu ajustar la configuració de visualització per veure i definir la duració de les activitats dels recursos. Podeu seleccionar i assignar recursos al nivell de paquet de treball mitjançant les opcions següents:
<ul>
<li><strong>Accepta</strong>: confirma els canvis al recurs que s'assigna a una tasca.</li>
<li><strong>Cancel·la</strong>: cancel·la els canvis al recurs que s'assigna a una tasca.</li>
<li><strong>Assigna automàticament</strong>: un recurs disponible de personal que té una funció coincident se selecciona automàticament i s'assigna a la tasca seleccionada.</li>
</ul></td>
</tr>
</tbody>
</table>

1. A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.
2. Seleccioneu **Planificació** > **Activitats** > **Estructura del desglossament del treball**.
3. Seleccioneu **Nou** per afegir les següents opcions de nivell u per a la WBS:

    - Inici
    - Planificació
    - S'està executant
    - Supervisió i control
    - Tanca 

4. Definiu les dates i l'esforç (hores), com es mostra a la il·lustració següent.

    [![Definir les dates i l'esforç.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Seleccioneu la línia de tasca **Inici** i, a continuació, al camp **Funció**, seleccioneu **Administrador de projectes sènior**.
6. Seleccioneu **Publica**.
7. A la mateixa línia, al camp **Recurs**, seleccioneu **Daniel Goldschmidt** i, a continuació, seleccioneu **Accepta**.
8. Seleccioneu la línia de tasques **Planificació** i, a continuació, al camp **Funció**, seleccioneu **Analista de negoci**.
9. Seleccioneu **Publica** i, a continuació, seleccioneu **Genera automàticament l'equip**.
10. Al quadre de missatge que apareix, seleccioneu **Sí**.
11. Al camp **Recurs**, comproveu que el valor és **Analista de negoci 1**.
12. Per al recurs **Analista de negoci 1**, obriu la cerca i seleccioneu **Inicia les assignacions de recursos**. A continuació, seleccioneu un treballador per a la tasca.
13. Seleccioneu **Assignació flexible** &gt; **Capacitat completa**.

    > [!NOTE] 
    > No rebeu cap advertiment que el recurs especificat és ara 2, perquè el nombre de recursos continua sent 1.

14. A la pàgina **Estructura del desglossament del treball**, valideu l'assignació de recursos a la WBS i, a continuació, seleccioneu **Desa**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]