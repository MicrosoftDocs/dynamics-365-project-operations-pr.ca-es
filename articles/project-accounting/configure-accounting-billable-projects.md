---
title: Configuració de la comptabilitat per a projectes facturables
description: En aquest tema es proporciona informació sobre les opcions de comptabilitat dels projectes facturables.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1159a31ba4f30f09734bf9c5a9e594b5c77a831e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596452"
---
# <a name="configure-accounting-for-billable-projects"></a>Configuració de la comptabilitat per a projectes facturables

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations admet diverses opcions de comptabilitat per a projectes facturables que inclouen transaccions de temps i de materials i de preu fix.

- **Transaccions per temps i materials** : aquestes transaccions es facturen a mesura que la feina progressi segons el consum d'hores, de despeses, d'articles o de càrrecs del projecte. Aquests costos de transacció es poden assignar als ingressos de cada transacció i el projecte es factura a mesura que el treball progressa. Els ingressos del projecte també es poden acumular en el moment en què es produeix la transacció. Durant la facturació, es reconeixen els ingressos i, si escau, l'acumulació es reverteix.
- **Transaccions de preu fix**: aquestes transaccions es fracturen segons una planificació de facturació basada en el contracte del projecte. Els ingressos per a transaccions de preu fix es poden reconèixer en la facturació o calcular i comptabilitzar-se periòdicament, d'acord amb els mètodes de **Contracte finalitzat** o **Percentatge completat**.

Un projecte es considera facturable quan està associat a una o diverses línies de contracte. Una línia de contracte de projecte defineix per si mateixa quin mètode de facturació i tipus de transaccions es permeten.

Per exemple, Fabrikam Robotics ha guanyat un contracte de projecte amb Adatum Corporation per a l'optimització de l'equipament. Adatum pagarà una quantitat fixa de 10.000 USD per cobrir les despeses del projecte incorregudes. Aquest és un mètode de facturació de preu fix. El temps i els càrrecs del projecte es facturaran per ús. Aquest és un mètode de facturació per temps i material. Tot el treball se seguirà sota un únic projecte anomenat Optimització d'equipament d'Adatum.

Un membre de l'equip del projecte envia vuit hores de feina al projecte Optimització d'equipament d'Adatum. Quan l'administrador del projecte aprova aquest temps, el sistema utilitza el mètode de facturació per temps i materials per crear transaccions reals, una factura i un compte. Aquesta transacció no s'inclourà al càlcul d'estimació d'ingressos per preu fix.

Un altre membre de l'equip del projecte envia una despesa de viatge de 2000,00 USD al projecte Optimització d'equipament d'Adatum. Quan l'administrador del projecte aprova aquest enviament, el sistema utilitza el mètode de facturació per preu fix per crear transaccions reals i un compte per a aquesta despesa del projecte. El client no es facturarà per aquesta transacció. En comptes d'això, es facturarà mitjançant fites de facturació configurades per separat. Aquesta transacció de despesa, juntament amb les estimacions de despesa, s'inclourà al càlcul d'estimació d'ingressos per preu fix.

Els principis de comptabilitat de les transaccions de projecte es defineixen en els perfils de cost i ingrés del projecte. Per a cada transacció de projecte, el sistema determina el perfil de cost i d'ingressos del projecte adient mitjançant les regles de perfil de cost i d'ingressos del projecte que s'han configurat.

## <a name="define-project-cost-and-revenue-profiles"></a>Definir perfils de costos i ingressos del projecte 

Els perfils de cost i ingrés del projecte determinen les regles de comptabilitat de les transaccions de projecte. Aquests perfils es configuren a Administració de projectes i comptabilitat. 

Completeu els passos següents per crear un perfil d'ingressos i costos del projecte nou. 

1. Aneu a **Administració de projectes i comptabilitat** > **Configuració** > **Comptabilització** > **Perfils de costos i ingressos del projecte**. 
2. Seleccioneu **Nou** per crear un perfil d'ingressos i costos del projecte nou.
3. Al camp **Nom**, introduïu el nom i una descripció breu del perfil.
4. Al camp **Mètode de facturació**, seleccioneu **Temps i material** o **Preu fix**.
5. Expandiu el FastTab **Registre major**. Els camps d'aquesta pestanya defineixen els principis de comptabilitat que s'utilitzen en el moment en què es realitzen transaccions de projectes mitjançant el llibre diari d'integració del Project Operations i que es facturen a través de la proposta de factura de projecte.
6. Seleccioneu la informació adequada en els camps següents al FastTab **Registre major**:

    - **Comptabilització de costos: hora**:

       - *Sense registre major*: el cost de les transaccions de temps no s'enviarà al registre major quan el diari d'integració del Project Operations hagi estat comptabilitzat. Tanmateix, el comptable pot comptabilitzar les despeses mitjançant la funció de comptabilització de costos en un moment posterior.
       - **Balanç**: el cost de les transaccions de temps es carregarà al tipus de compte del registre major *En curs: valor de cost* i s'abonarà al *Compte d'assignació de nòmines* a la configuració de comptabilització del registre major. El comptable utilitzarà la funció de comptabilització de costos per desplaçar aquest cost d'un compte de balanç a un compte de beneficis i de pèrdues de manera periòdica.
       - **Beneficis i pèrdues**: quan es comptabilitza el llibre diari d'integració del Project Operations, el cost de transacció de temps es carregarà al tipus de compte del registre major *Cost* i es carregarà al *Compte d'assignació de nòmines* definit a la pestanya **Cost** de la pàgina **Configuració de comptabilització del llibre major** (**Administració de projectes i comptabilitat**\>**Configuració**\>**Comptabilització**\>**Configuració de la comptabilització del registre major**). És la configuració més comuna per a les transaccions de temps i materials.
        - *Sense registre major*: el cost de les transaccions de temps no es comptabilitzarà mai al llibre major.

    - **Comptabilització de costos: despesa**:

         - **Balanç**: en comptabilitzar en el diari d'integració del Project Operations, el cost de les transaccions de despeses es carregarà al tipus de compte comptable *En curs: valor del cost* tal com es defineix a la pestanya **Cost** de la pàgina **Configuració de publicació del registre major** i s'abonarà al compte de desplaçament de la línia de diari. Els comptes de desplaçament per defecte per a despeses es defineixen a **Administració de projectes i comptabilitat** > **Configuració** \> **Comptabilització** \> **Compte de desplaçament defecte per a les despeses**. El comptable utilitzarà la funció de **comptabilització de costos** per desplaçar aquest cost del compte de balanç al compte de beneficis i de pèrdues de manera periòdica.
        - **Beneficis i pèrdues**: en comptabilitzar en el diari d'integració del Project Operations, el cost de les transaccions de despeses es carregarà al tipus de compte comptable *Cost* tal com es defineix a la pestanya **Cost** de la pàgina **Configuració de publicació del registre major** i s'abonarà al compte de desplaçament de la línia de diari. Els comptes de desplaçament per defecte per a despeses es defineixen a **Administració de projectes i comptabilitat** \> **Configuració** \> **Comptabilització** \> **Compte de desplaçament defecte per a les despeses**.
      
    - **Costos posteriors: article**:

         - **Saldo**: quan es comptabilitza el diari d'integració de Project Operations, el cost de la transacció de l'article es cobrarà al tipus de compte de Llibre major *Treball en curs - Valor de cost - article* tal com es defineix a la pestanya **Cost** de la pàgina **Configuració de comptabilització del llibre major** i s'abona al següent:
    
              - Per a l'ús del tipus de document: compte **Cost - article** a la **Configuració de comptabilització del llibre major**.  
              - Per a la compra de tipus de document: **Compte d'integració de proveïment** als **Paràmetres d'administració i comptabilitat de projectes**.
           El comptable utilitzarà la funció de **comptabilització de costos** per desplaçar aquest cost del compte de balanç al compte de beneficis i de pèrdues de manera periòdica.
        - **Pèrdues i guanys**: quan es comptabilitza el diari d'integració de Project Operations, el cost de la transacció de l'article es cobrarà al tipus de compte de Llibre major *Cost* tal com es defineix a la pestanya **Cost** de la pàgina **Configuració de comptabilització del llibre major** i s'abonarà al següent:
         
             - Per a l'ús del tipus de document: compte **Cost - article** a la **Configuració de comptabilització del llibre major**.  
             - Per a la compra de tipus de document: **Compte d'integració de proveïment** als **Paràmetres d'administració i comptabilitat de projectes**.
       
    - **Facturació del compte**:

        - **Balanç**: en comptabilitzar la proposta de factura de projecte, s'abonarà una transacció al compte (fita de facturació) al tipus de compte de registre *En curs facturat: al compte* tal com es defineix a la pestanya **Ingressos** a la pàgina de **Configuració de comptabilització del registre major**, i es carregarà al compte de saldo del client.
         - **Beneficis i pèrdues**: en comptabilitzar la proposta de factura de projecte, s'abonarà una transacció al compte (fita de facturació) al tipus de compte de registre *Ingrés facturat: al compte* tal com es defineix a la pestanya **Ingressos** a la pàgina de **Configuració de comptabilització del registre major**, i es carregarà al compte de saldo del client. Els comptes de balanç dels clients es defineixen a **Comptes a cobrar** \> **Configuració** \> **Perfils de comptabilització del client**.

   Quan definiu els perfils de comptabilització dels mètodes de facturació de temps i materials, teniu l'opció d'acumular els ingressos per tipus de transacció (hora, despesa, article i tarifa). Si l'opció **Acumula els ingressos** està definida com a **Sí**, les transaccions de vendes no facturades al diari d'integració del Project Operations es registraran al llibre general. El valor de vendes es carregarà a **En curs: compte de valor de vendes** i s'abonarà al compte **Ingressos acumulats: valor de vendes** configurat a la pàgina **Configuració de la comptabilització del registre** a la pestanya **Ingressos**. 
  
  > [!NOTE]
  > L'opció **Acumula els ingressos** està disponible només quan el **cost** de tipus de transacció respectiu es comptabilitza al compte de pèrdues i guanys.
    
7. Expandiu el FastTab **Estimació**. Els camps d'aquesta pestanya defineixen la configuració de càlcul per a les estimacions dels ingressos per preu fix. Els camps d'aquesta pestanya només s'apliquen als perfils de cost i ingressos del projecte amb un mètode de facturació **Preu fix**.
8. Seleccioneu la informació adequada en els camps següents al FastTab **Estimació**:

    - **Principi utilitzat per als càlculs de finalització del projecte**:

        - **Contracte finalitzat**: l'assignació de costos i el reconeixement dels ingressos no es produeix fins a la finalització del projecte. Els costos es reflecteixen com a en curs al balanç fins que s'hagi completat el projecte.
        - **Percentatge completat**: els ingressos acumulats es calculen i es comptabilitzen al llibre major cada període segons el percentatge de finalització del projecte. Hi ha diversos mètodes disponibles per calcular el percentatge d'acabament. Aquests mètodes poden ser automàtics basant-se en la configuració o manuals.
        - **Sense en curs**: aquesta configuració s'utilitza per a projectes de preu fix amb un lapse de temps curt i on la factura i els costos es produeixen en el mateix període. En aquest cas, el valor del camp **Facturació al compte** de la FastTab **Registre** es defineix automàticament com a **Beneficis i pèrdues** per garantir que els ingressos es reconeguin en la facturació. El procés d'estimació dels ingressos no s'utilitzarà per a aquest perfil de cost i ingrés del projecte.

    - **Principi de coincidència**: aquest camp determina la manera com el valor de venda calculat (ingressos acumulats) es comptabilitzarà al llibre major.

        - Amb el principi **Valor de les vendes**, el sistema calcularà el valor de vendes, combinant els costos i els ingressos i, a continuació, comptabilitzant-lo com a import únic.
        - Amb el principi **Producció i benefici**, el sistema dividirà el valor de les vendes en costos realitzats i benefici calculat. Es publiquen per separat.

    - **Plantilles de cost**: permeteu que s'agrupin les transaccions de projecte segons el tipus de transacció i el projecte i definiu regles de càlcul de compleció de percentatge per a aquests grups.
    - **Codis de període**: definiu la freqüència amb què es calculen les estimacions d'ingrés per a un perfil de cost i d'ingressos determinat del projecte.
    - **Categories per a l'estimació**: s'utilitza per a la comptabilització del valor de les vendes (ingressos acumulats) a transaccions de projecte. En primer lloc, configureu la categoria de projecte dedicada per a un tipus de transacció **Càrrec** i, a continuació, definiu la marca **Estimació** per a aquesta categoria de projecte. A continuació, en funció del principi de coincidència seleccionat, trieu aquesta categoria del projecte al valor **Vendes** o al camp **Beneficis** del perfil de cost i ingrés del projecte.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Configuracions d'exemple per a perfils de costos i ingressos de projecte

Temps i materials: sense en curs

![Perfil de cost i ingressos: temps i materials: sense en curs.](media/time-material-no-wip.png)

Temps i materials: en curs (ingressos)

![Perfil de cost i ingressos: temps i materials: en curs.](media/time-material-with-wip.png)

Preu fix: sense en curs

![Perfil de cost i ingressos: preu fix: sense en curs.](media/fixed-price-no-wip.png)

Preu fix: contracte finalitzat

![Perfil de cost i ingressos: preu fix: contracte finalitzat.](media/fixed-price-completed-contract.png)

Preu fix: percentatge d'acabament

![Perfil de cost i ingressos: preu fix: percentatge de finalització.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemples d'esdeveniments de comptabilitat per a perfils de costos i ingressos de projecte d'exemple.

| Esdeveniment de comptabilitat                  | Temps i material: sense en curs                       | Temps i material: en curs                                                                                           | Preu fix: sense en curs                                            | Preu fix: contracte finalitzat                                                                            | Preu fix: percentatge d'acabament                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Registre de transaccions de temps    | Dèbit: cost <br>Crèdit: assignació de nòmines          | Dèbit: cost <br>Crèdit: assignació de nòmines <br>Dèbit: valor de vendes en curs <br>Crèdit: valor de vendes d'ingressos acumulats                | Dèbit: cost <br>Crèdit: assignació de nòmines                         | Dèbit: cost <br>Crèdit: assignació de nòmines                                                                    | Dèbit: cost <br>Crèdit: assignació de nòmines                       |
| Registre de transaccions de despesa | Dèbit: cost <br>Crèdit: compte de desplaçament per a despeses | Dèbit: cost <br>Crèdit: compte de desplaçament per a despeses <br>Dèbit: valor de vendes en curs <br>Crèdit: valor de vendes d'ingressos acumulats      | Dèbit: cost <br>Crèdit: compte de desplaçament per a despeses                 | Dèbit: cost<br> Crèdit: compte de desplaçament per a despeses                                                            | Dèbit: cost <br>Crèdit: compte de desplaçament per a despeses               |
| Client a facturar                | Dèbit: balanç del client <br>Crèdit: ingressos facturats | Dèbit: balanç del client <br>Crèdit: ingressos facturats <br>Crèdit: dèbit de valor de vendes en curs: valor de vendes d'ingressos acumulats | Dèbit: balanç del client <br>Crèdit: ingressos facturats: al compte | Dèbit: balanç del client <br>Crèdit: en curs: facturat al compte                                                  | Dèbit: balanç del client <br>Crèdit: en curs: facturat al compte    |
| Comptabilització de la previsió d'ingressos             | No aplicable                                   | No aplicable                                                                                                    | No aplicable                                                  | Dèbit: valor de cost en curs <br>Crèdit: cost                                                                         | Dèbit: en curs: valor de vendes <br>Crèdit: valor de vendes d'ingressos acumulats |
| Elimina                         | No aplicable                                   | No aplicable                                                                                                    | No aplicable                                                  | Crèdit: valor de cost en curs <br>Dèbit: cost <br>Crèdit: ingressos acumulats: valor de vendes <br>Dèbit: en curs: facturat al compte | Dèbit: en curs: facturat al compte <br>Crèdit: valor de vendes en curs     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configuració de regles de perfils de costos i ingressos del projecte

Les regles de perfil de cost i d'ingressos del projecte determinen el perfil cost i ingrés del projecte que s'ha d'utilitzar quan es processen transaccions del projecte facturables. Definiu les regles anant a **Administració de projectes i comptabilitat** \> **Configuració** \> **Comptabilització** \> **Regles de perfils d'ingressos i costos del projecte**.

Les regles es poden definir per contracte de projecte, grup de projectes o per projecte específic. Primer, el sistema sempre tria la regla amb la granularitat més alta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
