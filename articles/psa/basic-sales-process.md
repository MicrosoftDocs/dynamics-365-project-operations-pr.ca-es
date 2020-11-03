---
title: Processos de venda
description: En aquest tema es proporciona informació sobre els processos de venda bàsics.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f09b30fe6d842faaf896cb97f44b060ec4049213
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072326"
---
# <a name="sales-processes"></a>Processos de venda

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Els processos de venda que s'utilitzen en una organització basada en projectes es diferencien dels processos de venda que s'utilitzen en una organització basada en productes. Aquesta diferència es produeix perquè els cicles de venda d'organitzacions basades en projectes són més llargs i requereixen tècniques d'estimació personalitzades per analitzar i crear ofertes per a cada operació. El Dynamics 365 Project Service Automation utilitza algunes de les mateixes funcionalitats que s'utilitzen en el procés de venda per al Dynamics 365 Sales. A continuació trobareu alguns exemples:

- Una entitat Client potencial s'utilitza per fer el seguiment del procés de vendes.
- Es fa un seguiment dels clients potencials qualificats com a oportunitats. El procés de vendes també pot començar amb l'oportunitat.
- S'accedeix a tots els artefactes relacionats d'una oportunitat. Aquests artefactes inclouen l'equip de vendes, les parts interessades, la probabilitat, la puntuació, les fases de vendes i els processos de negoci.
- Es creen diverses ofertes per a una oportunitat.
- Una oferta es marca com a **Tancada com a guanyada** per crear una comanda de venda. Al PSA, la comanda de vendes es personalitza i s'anomena contracte de projecte.

A la il·lustració següent es mostra un procés de venda típic d'una organització basada en projectes.

> ![Procés de venda d'una organització basada en projectes](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimació d'una venda
El valor d'una venda es pot estimar a partir de projectes que abans s'hagin lliurat i de la complexitat dels projectes. Per a projectes que comportin ampliacions a projectes previs, o projectes en els quals l'experiència del venedor és gran i s'utilitzen plantilles de treball, podeu utilitzar un procés d'estimació més senzill. Normalment, els projectes més complexos tenen un procés de compra més llarg. Per tant, hi ha més fases en el procés d'estimació de vendes. A principis del procés, l'equip de vendes utilitza l'entrada dels administradors del compte i els experts de la matèria (SME) per començar a crear una estimació d'alt nivell per a cada component diferent del treball que s'ofereix. Aquests components de treball es representen amb línies d'oferta. 

Podeu crear una estimació d'alt nivell de l'oferta. Amb el temps, aquesta estimació d'alt nivell es reemplaçarà per una estimació més detallada basada en un pla de projecte que creeu amb les plantilles de projecte estandarditzades. Aquestes plantilles us ajuden a construir una planificació i determinen els valors monetaris de l'oferta i els seus components (línies d'oferta). 

Podeu crear diverses ofertes per a un projecte i agrupar-les en un únic tipus d'entitat d'oportunitat. Eventualment, una d'aquestes ofertes es marca com a **Tancada com a guanyada** i es crea un contracte de projecte o una declaració de treball (SOW). Un contracte de projecte té el valor contractat per a cada component (línia de contracte) que el client accepta per al seu lliurament. Normalment es crea un SOW com a document del Microsoft Word. Totes les factures que s'envien al client en el transcurs de l'enviament del projecte fan referència al contracte del projecte o SOW.

També podeu crear ofertes alternatives en un tipus d'entitat d'oportunitat o configurar el sistema per tal que es creï un contracte de projecte quan es guanya una oferta. En aquest cas, podeu adjuntar un document del Word que representi el SOW al registre de contracte del projecte.

![Tancar una oferta per crear un contracte de projecte](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configurar el procés de vendes
Podeu utilitzar els fluxos del procés de negoci (BPF) al Microsoft Dynamics 365 per configurar el procés de vendes. Els BPF donen al vostre personal de vendes una interfície visual guiada que poden utilitzar per fer avançar ofertes a través de les fases típiques de la vostra empresa.

Per exemple, pot ser que l'empresa tingui les sis fases següents en el procés de vendes:

1. Qualifica
2. Estimat
3. Revisió interna
4. Contracte
5. Lliura
6. Tanca

Aquestes sis fases estan representades per cometes (\>) que seleccioneu per expandir en cada tipus d'entitat d'oportunitat que creeu.

![Configuració del procés de negoci al Dynamics 365](media/basic-guide-3.png)
 
La vostra organització podria utilitzar entitats diferents per representar la mateixa oferta a mesura que evoluciona. A principis del procés de vendes, un acord està representat per l'entitat Oportunitat. A mesura que passa el temps i hi ha més detalls que sorgeixen, podríeu utilitzar estimacions d'alt nivell per crear una o diverses ofertes. Si una d'aquestes ofertes la revisen parts interessades internes i del client, l'entitat Oferta representa el tracte. Quan el client accepta l'oferta, un contracte o SOW del projecte representa el tracte. Per admetre aquest comportament, els BPF s'estructuren de manera que cada fase del procés es vincula a una altra taula de base de dades.

La fase **Qualificació** en el procés de venda pot basar-se en una entitat Oportunitat. Les fases **Estimació** i **Revisió interna** poden basar-se en una entitat Oferta. Les fases **Contracte** , **Lliurament** i **Tancament** poden basar-se en una entitat Contracte del projecte.

A mesura que l'oportunitat avanci a través de les fases, se us demanarà que creeu el registre de l'entitat adient per ajudar i guiar-vos pel procés. Les fases poden ser condicionals. Per exemple, si necessiteu una revisió interna d'una oferta només si l'oferta utilitza una llista de preus personalitzada, podeu configurar aquesta condició en la fase adequada del procés de negoci. Llavors, la fase **Revisió interna** només es mostra per a les ofertes que utilitzen una llista de preus personalitzada. Per a tots els altres negocis i ofertes, l'etapa **Estimació** va seguida de la fase **Contracte**.

> [!NOTE]
> El PSA té pàgines específiques per a les entitats Oportunitat, Oferta, Comanda i Factura. Heu de crear oportunitats, ofertes, comandes i factures del Project Service mitjançant les pàgines d'informació del projecte per a aquestes entitats. Si utilitzeu una altra pàgina per crear un registre, no podreu obrir el registre des de la pàgina **Informació del projecte**. Si voleu obrir un registre des de la pàgina **Informació del projecte** , heu de suprimir el registre i tornar-lo a crear amb la pàgina **Informació del projecte**. A la pàgina **Informació del projecte** , la lògica empresarial per a cadascun d'aquests tipus d'entitats garanteix que el camp **Tipus** del registre es defineixi correctament i que tots els conceptes obligatoris s'inicialitzen correctament.

> ![Informació del projecte per a una nova comanda](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Diferències entre el Project Service Automation i el Sales
Tot i que el procés de vendes del PSA utilitza les capacitats bàsiques del procés de venda al Sales, té algunes diferències clau a causa de les variacions de pràctiques empresarials d'organitzacions basades en projectes. A continuació trobareu alguns exemples:

- **Ofertes del projecte** : al Project Service Automation, l'oferta es tanca després d'haver creat un contracte de projecte a partir d'una oferta. Al Sales, podeu mantenir una oferta oberta després d'haver-la guanyat. La raó d'aquesta diferència és que una coincidència entre una oferta i un contracte de projecte és millor per a organitzacions basades en projectes. 
- **Activació i revisions** : al PSA, l'activació i les revisions no estan admeses per a les ofertes del projecte. Al Sales, es pot bloquejar una oferta per evitar modificacions addicionals.
- **Tancar una oferta com a perduda o guanyada** : al PSA, quan un pressupost de projecte es tanca com a guanyat o perdut, l'oportunitat queda oberta. Totes les altres ofertes a l'oportunitat es tanquen com a perdudes. Al Sales, quan una oferta es tanca com a guanyada o perduda, es demanarà a l'usuari que faci una acció sobre l'oportunitat. En funció de l'entrada de l'usuari, pot ser que l'oportunitat subjacent es tanqui o que quedi oberta.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Seguiment de revisions a ofertes i plans de projecte del cicle de venda
Al PSA, no podeu fer el seguiment de les revisions fetes en una oferta. En lloc d'això, heu de marcar l'oferta existent **Tancada com a perduda** i, a continuació, crear una oferta nova. Podeu copiar una oferta o clonar una oferta basada en projectes mitjançant el PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Seguiment de comentaris i aprovacions d'ofertes i contractes de projectes
Podeu administrar la revisió i l'aprovació de les ofertes i els contractes de projecte mitjançant el mur de registres i els missatges. La vostra organització pot crear fluxos de treball i complements personalitzats per assignar, redirigir, agreujar i administrar les notificacions dels elements de treball de revisió i aprovació.
