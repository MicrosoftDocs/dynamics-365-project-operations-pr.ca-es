---
title: Crear un projecte nou
description: Aquest tema proporciona informació sobre com crear un projecte nou.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006229"
---
# <a name="create-a-new-project"></a>Crear un projecte nou

[!include [banner](../includes/banner.md)]

Completeu els passos següents per crear un projecte nou.

1. A la pàgina **Administració de projectes**, seleccioneu **Projecte nou** i introduïu els valors següents:

    - **Tipus de projecte:** temps i material
    - **Nom del projecte:** Fase 2 d'actualització d'XYZ
    - **Grup de projectes:** TM\_WIP
    - **Identificador de contracte de projecte**: 00000002

2. Seleccioneu **Crea el projecte**.

## <a name="assign-a-resource-to-a-project"></a>Assignació d'un recurs a un projecte

1. A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el registre del treballador per al qual heu configurat les competències anteriorment i obriu el registre del treballador.
2. A la subfinestra d'acció, a la pestanya **projecte**, al grup **Configuració**, seleccioneu **Assigna projectes**.
3. A la pàgina **Assignacions de projecte de validació de recursos**, a la pestanya **Projectes**, al camp **Afegeix el projecte als projectes seleccionats**, filtreu el projecte **Fase 2 d'actualització d'XYZ**.
4. A la subfinestra **Projectes restants**, seleccioneu un projecte i, a continuació, seleccioneu el botó de fletxa per afegir-lo a la subfinestra **Projectes seleccionats**.

També podeu assignar categories per a un recurs a mesura que les necessiteu. El tipus de categoria és **Cost** o **Ingrés**. El tipus de categoria ve determinat per la vostra organització. Si no s'assigna cap categoria a un recurs, el Finance cerca la categoria per defecte a preus per hora per als costos i els ingressos.

## <a name="set-up-project-resource-and-role-characteristics"></a>Configurar els recursos del projecte i les característiques de la funció

Un administrador de projectes pot utilitzar la funcionalitat de recursos de projecte per crear les funcions necessàries per al projecte. Es poden utilitzar funcions si els recursos confirmats es desconeixen quan es reserven els recursos. Les funcions es poden reservar temporalment com a recursos planificats per tal de poder continuar la fase de planificació del projecte.

[![Exemple d'una funció](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Escenari:** Contoso ha rebut un contracte per completar un projecte de temps i materials que té una carta de projecte aprovada. L'administrador de projectes júnior encara està completant l'àmbit del projecte. L'administrador de recursos està identificant actualment els recursos específics que es reservaran per treballar en el nou projecte. A causa del caràcter crític del projecte, el patrocinador del projecte ha sol·licitat l'administrador de projectes sènior com una de les funcions. L'administrador de recursos ha d'adquirir el recurs nou i definir la funció en el sistema en cas que l'administrador de projectes júnior requereixi la informació del recurs durant la planificació del projecte.

Els passos següents mostren com l'administrador de recursos pot configurar la funció Administrador de projectes sènior i associar-hi les característiques del recurs. Més endavant, la funció es pot utilitzar per cercar recursos disponibles que coincideixin amb les competències de recursos necessàries.

1. A la pàgina **Configura les funcions**, seleccioneu **Nou** i introduïu els valors següents:

    - **Identificador de funció:** administrador de projectes sènior
    - **Descripció:** administrador de projectes sènior

2. Seleccioneu **Crea**.
3. Seleccioneu la funció **Administrador de projectes sènior** i, a continuació, seleccioneu **Configura les característiques**.
4. Al camp **Tipus de característiques**, seleccioneu **Habilitat**.
5. Al camp **Característiques disponibles**, introduïu l'habilitat que voleu cercar.
6. Al camp **Tipus de característiques**, seleccioneu **Certificat**.
7. Al camp **Característiques disponibles**, introduïu el tipus de certificat que voleu cercar.

## <a name="assign-a-project-resource-to-a-project"></a>Assignació d'un recurs de projecte a un projecte

1. A la pàgina **Tots els projectes**, seleccioneu el projecte **Fase 2 d'actualització d'XYZ**.
2. A la pestanya **Equip del projecte i planificació**, seleccioneu **Afegeix**.
3. Al camp **Funció**, seleccioneu **Membre de l'equip**.
4. Seleccioneu **Reserva des del calendari**.
5. A la pàgina **Disponibilitat de recursos**, seleccioneu **Visualitza la configuració**.
6. A la pàgina **Ajusta la configuració de visualització**, introduïu els valors següents:

    - **Format per a la visualització d'interval de dates:** dia
    - **Mostra les descripcions de disponibilitat:** Sí
    - **Mostra la capacitat restant:** Sí

7. Seleccioneu un recurs de la llista de recursos.
8. Seleccioneu **Reserva fixa** i **Capacitat completa**.

## <a name="assign-a-resource-to-a-default-role"></a>Assignar un recurs a una funció per defecte

Per ajudar els administradors de projecte o de recursos, podeu desglossar els recursos que es poden reservar per a un projecte. Podeu associar una funció per defecte amb un recurs existent o un recurs adquirit recentment. Per exemple, quan Daniel va ser contractat, tenia l'experiència i les habilitats necessàries per cobrir la funció d'analista de negocis. L'administrador de recursos ha assignat aquesta funció com a funció per defecte del Daniel. Per tant, l'administrador de recursos ha afegit en Daniel a un grup d'analistes de negoci que estan disponibles per treballar en projectes.

Durant la reserva de recursos, els administradors de projectes poden filtrar els recursos de la funció que estan disponibles per treballar en projectes. Poden utilitzar aquesta informació com un criteri quan realitzen una anàlisi de decisió de diversos criteris durant el compliment dels recursos. També poden afegir altres característiques de recursos al filtre per cercar recursos que tinguin habilitats, formació i experiència específics per a un projecte concret.

**Escenari:** s'ha iniciat un projecte aprovat i la funció Administrador de projectes sènior s'ha reservat com a recurs planificat durant la fase de planificació del projecte. L'administrador de recursos ha adquirit un recurs per cobrir la funció Administrador de projectes sènior.

1. A la pàgina **Llista de recursos**, seleccioneu **Daniel Goldschmidt**.
2. A la pàgina **Funció del recurs**, seleccioneu **Nova** i introduïu els valors següents:

    - **Efectivitat:** introduïu la data actual.
    - **Venciment:** introduïu **Mai**.
    - **Funció:** introduïu **Administrador de projectes sènior**.

3. Seleccioneu **Desa** i, a continuació, tanqueu la pàgina.
4. A la pestanya **Competències**, afegiu l'habilitat **ProjectMgmt** i el certificat **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]