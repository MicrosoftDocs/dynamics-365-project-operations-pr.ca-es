---
title: Transferència de pressupostos de projecte al final de l'exercici fiscal
description: Aquest article proporciona una informació sobre com transferir les quantitats restants del pressupost a anys futurs i crear detalls del registre pressupostari.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 74b2831a19688636f5c4863036adf7043c80d49829737b56c131abb6998d6cb3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007359"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transferència de pressupostos de projecte al final de l'exercici fiscal

[!include [banner](../includes/banner.md)]

Quan es treballa en un projecte pluriennal, pot ser que tingueu pressupost restant al final de l'exercici fiscal. Podeu transferir els imports restants del pressupost a un any futur i crear els detalls del registre pressupostaria per als imports en els comptes del registre general associats. Abans de transferir les quantitats restants, reviseu i analitzeu els imports restants del pressupost.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Revisar i analitzar els imports pressupostaris restants

Completeu els següents passos per a revisar els imports pressupostaris a finals d'any per als projectes però no transferir els imports.

1. Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Pressupostos** > **Transfereix pressupostos**. 
2. A la pàgina **Procés de transferència del pressupost del projecte**, a la pestanya **Opcions de final d'any**, verifiqueu que **Transfereix els imports pressupostaris del projecte restants** no estigui habilitat.
3. A la pestanya **Paràmetres**, en el camp **Any pressupostari del projecte**, seleccioneu l'exercici fiscal per al qual voleu veure l'import pressupostari restant. 
4. Al camp **Exercici fiscal d'obertura**, seleccioneu l'exercici fiscal per al qual voleu veure l'import pressupostari restant. 
5. En el camp **Del model de previsió**, seleccioneu **Pressupost restant**. 
6. Per incloure projectes que compleixin els criteris seleccionats i no tinguin pressupost restant, seleccioneu **Mostra zero restant**.  
7. A la pestanya **Selecció de pressupostos**, seleccioneu **Recupera tots els pressupostos** per carregar tots els pressupostos que coincideixin amb els criteris seleccionats i seleccioneu **Processa**. 
8. Per dissenyar una consulta de base de dades que carregui un conjunt específic de pressupostos a la subfinestra, seleccioneu **Recupera els pressupostos seleccionats**.

Per a més informació sobre una línia específica de la subfinestra, seleccioneu la línia i seleccioneu **Visualitza els detalls del pressupost** o **Visualitza els comptes**.

## <a name="carry-forward-remaining-budget-amounts"></a>Transferir imports pressupostaris restants 

Quan processeu els imports restants del pressupost, es poden crear transaccions en el llibre major general per a les quantitats que esteu transferint. Per a crear transaccions de llibre major general, completeu els passos de la secció [Transferir imports del pressupost i crear transaccions al llibre major general](#carry-forward). 

> [!NOTE]
> Els imports pressupostaris transferits es transfereixen al model de previsió que s'ha seleccionat a la pàgina **Models de previsió** com a model de previsió per a la transferència.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Transferir imports pressupostaris i crear transaccions al llibre major general

1.  Seleccioneu **Administració de projectes i comptabilitat** > **Periòdic** > **Pressupostos** > **Transfereix pressupostos**. 
2. A la pàgina **Procés de transferència del pressupost del projecte**, seleccioneu **Fi d'any** i habiliteu **Transfereix els imports pressupostaris del projecte restants** i **Crea entrades de registre pressupostari al llibre de registre general**. 
3. A la pestanya **Paràmetres**, al grup de camps **Paràmetres del projecte**, seleccioneu el següent:

   - **Any de pressupost del projecte**: seleccioneu el començament de l'exercici fiscal per al qual voleu veure els imports restants del pressupost. 
   - **Beneficis i pèrdues**: creeu transaccions de beneficis i pèrdues en el llibre major general. 
   -  **Treball en curs**: creeu transaccions de treball en curs (WIP) al llibre major general.
   -  **Nòmina**: creeu transaccions d'assignació de nòmina en el llibre major general. 

5. En el grup de camps **Llibre major general**, proporcioneu la següent informació: 

   - Al camp **Exercici fiscal d'obertura**, seleccioneu l'exercici fiscal al qual voleu transferir els imports pressupostaris restants per als projectes. El valor per defecte és un any després del valor en el camp **Any del pressupost del projecte**.
   -  En el camp **Període de transferència**, seleccioneu el període per al qual voleu crear els detalls del registre de pressupost al llibre major general. És normalment el primer període de l'exercici fiscal inicial.

6. En el grup de camps **Copia de/a**, proporcioneu la següent informació:

   - En el camp **Del model de previsió**, seleccioneu el model de previsió del pressupost del projecte associat amb els imports restants del pressupost que voleu transferir per als projectes. 
   - En el camp **Model de pressupost al llibre major**, seleccioneu el model de pressupost del llibre major associat amb els imports del pressupost que voleu transferir al llibre major general. 
   -  Seleccioneu **Transfereix la moneda de vendes** per utilitzar la moneda de venda del projecte per a les operacions generals del llibre major que es creen quan es transfereixen els imports del pressupost per als projectes. Quan l'opció no està seleccionada, les transaccions utilitzen la moneda de comptabilitat. 
   -  Seleccioneu **Mostra zero restant** per incloure els projectes que no tenen quantitats de pressupost restants, però que compleixen els altres criteris que seleccioneu en els projectes que es mostren a la subfinestra inferior.

7. A la pestanya **Selecció de pressupostos**, seleccioneu **Recupera tots els pressupostos** per carregar tots els pressupostos que coincideixin amb els criteris seleccionats. Si preferiu dissenyar una consulta de base de dades que carregui un conjunt específic de pressupostos de projecte a la subfinestra, seleccioneu **Recupera els pressupostos seleccionats**.
8. Per a cada projecte que voleu processar, seleccioneu l'opció al començament de la línia per al projecte.

    > [!TIP]
    > Per seleccionar tots o la majoria dels projectes, selecciona la marca de selecció a la cantonada superior esquerra. Per excloure qualsevol projecte, esborreu la marca de selecció d'aquest projecte.

9. Per transferir els imports pressupostaris restants per als projectes seleccionats a l'exercici fiscal seleccionat i crear detalls del registre pressupostari en el llibre major general, seleccioneu **Processa**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Transferir imports pressupostaris sense crear transaccions al llibre major general

1. Aneu a **Administració de projectes i comptabilitat** > **Periòdic** > **Pressupostos** > **Transfereix pressupostos**.
2. A la pàgina **Procés de transferència del pressupost del projecte**, al camp **Opcions de final d'any**, seleccioneu **Transfereix els imports pressupostaris del projecte restants**.
3. Al grup **Paràmetres**, en el camp **Any pressupostari del projecte**, seleccioneu l'exercici fiscal per al qual voleu veure els imports pressupostaris restants.
4. En el grup **Copia de/a**, proporcioneu la següent informació:

   - En el camp **Del model de previsió**, seleccioneu el model de previsió del pressupost del projecte associat amb els imports restants del pressupost que voleu transferir per als projectes. 
   - Seleccioneu **Mostra zero restant** per incloure els projectes que no tenen imports de pressupost restants, però que compleixen els altres criteris que heu seleccionat.
   - Al grup **Selecció de pressupostos**, seleccioneu **Recupera tots els pressupostos** per carregar tots els pressupostos que coincideixin amb els criteris seleccionats. Per dissenyar una consulta de base de dades que carregui un conjunt específic de pressupostos de projecte a la subfinestra, seleccioneu **Recupera els pressupostos seleccionats**.

5. Per a cada projecte que voleu processar, seleccioneu l'opció al començament de la línia per al projecte. 
6. Seleccioneu **Processa** per transferir els imports pressupostaris restants per als projectes seleccionats a l'exercici fiscal seleccionat.



[!INCLUDE[footer-include](../includes/footer-banner.md)]