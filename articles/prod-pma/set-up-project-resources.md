---
title: Configuració dels recursos del projecte
description: Aquest tema proporciona informació sobre la configuració o la sol·licitud de recursos del projecte.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072384"
---
# <a name="set-up-project-resources"></a>Configuració dels recursos del projecte

[!include [banner](../includes/banner.md)]

Heu de configurar un calendari i associar-lo a un empleat o a un treballador. El calendari s'utilitza per planificar el projecte i el temps de treball dels recursos que es reserven per al projecte. Durant la configuració del calendari, els administradors del projecte poden fer un anivellament de recursos com a part de l'optimització de recursos. Segons la planificació de calendari, es poden posar restriccions als recursos. Podeu configurar un calendari a la pàgina **Calendaris**.

Quan configureu un treballador com a recurs de projecte, podeu seleccionar els treballadors que treballen a l'empresa per a la qual configureu els recursos. Si ho preferiu, podeu seleccionar treballadors d'altres empreses a l'organització. Aquests treballadors s'anomenen recursos entre empreses.

En els procediments següents s'explica com es configura un treballador com a recurs de projecte a l'empresa i com es configura un recurs de projecte entre empreses.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurar un treballador com a recurs de projecte

1. A la pàgina **Treballadors**, a la llista **Treballadors**, seleccioneu el treballador que voleu afegir com a recurs del projecte i obriu el registre del treballador.
2. A la subfinestra d'acció, seleccioneu **Projecte** &gt; **Configuració** &gt; **Configuració del projecte**.
3. Seleccioneu un calendari i, a continuació, tanqueu la pàgina.

També podeu especificar projectes per defecte per a un recurs com a tipus d'assignació prèvia. Les assignacions prèvies es poden utilitzar quan l'administrador de recursos o l'administrador del projecte sap en quins projectes treballarà el recurs amb antelació. Les assignacions prèvies també poden basar-se en la sol·licitud d'un patrocinador o client del projecte. Per assignar prèviament un projecte abans, a la pàgina **Assigna els projectes**, a la pestanya **Projectes**, a la llista **Projectes restants**, seleccioneu el projecte adient.

## <a name="set-up-an-intercompany-resource"></a>Configurar un recurs entre empreses

Quan configureu un treballador com a recurs entre empreses, heu d'emplenar la configuració tant de l'empresa prestadora com de l'empresa prestatària.

### <a name="in-the-lending-company"></a>A l'empresa prestadora

1. Al Finance, comproveu que l'empresa prestadora està seleccionada i, a continuació, completeu el procediment a la secció anterior, "Configurar un treballador com a recurs del projecte".
2. A la pàgina **Comptabilitat entre empreses**, seleccioneu **Nova**.
3. Al camp **ID de l'entitat jurídica**, seleccioneu l'empresa prestadora. Empleneu els camps restants segons calgui i seleccioneu **Desa**.
4. A la pàgina **Transferència de preus**, seleccioneu **Nova**.
5. Al camp **Entitat jurídica prestatària**, seleccioneu l'empresa adequada.
6. Per prestar a l'empresa prestatària només el recurs que heu creat a l'inici d'aquesta secció, al camp **Recurs**, seleccioneu el nom del recurs que heu creat. Per fer que tots els recursos de l'empresa prestadora estiguin disponibles per a l'empresa prestatària, deixeu el camp **Recurs** en blanc.
7. A la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**, a la pestanya **Entre empreses**, definiu l'opció **Habilita la planificació de recursos i els fulls d'hores entre empreses** a **Sí**.

### <a name="in-the-borrowing-company"></a>A l'empresa prestatària

- A la pàgina **Llista de recursos**, al filtre de cerca, introduïu el nom del recurs que heu creat per a l'empresa prestadora, per comprovar que el nom s'inclou a la llista de recursos de l'empresa prestatària.

## <a name="request-project-resources"></a>Sol·licitud de recursos del projecte
La funcionalitat per a la planificació de recursos de projectes només permet distribuir els recursos de personal a compromisos o projectes. Per habilitar aquesta funcionalitat, completeu les tasques següents o verifiqueu que s'hagin completat:

- Configureu les seqüències de números.
- Configureu l'administració de projectes i els fluxos de treball de comptabilitat.
- Habiliteu els fluxos de treball de sol·licitud de recursos.

Quan s'hagin completat les tasques anteriors, podreu completar les tasques següents segons calgui:

- Crear una sol·licitud de recurs des d'un recurs de personal reservat de manera flexible.
- Supervisar les sol·licituds de recursos.
- Complir les sol·licituds de recursos.
- Sol·licitar un recurs de personal d'una WBS.
- Reservar recursos en un projecte sense necessitat de tenir una sol·licitud de recurs de personal.
