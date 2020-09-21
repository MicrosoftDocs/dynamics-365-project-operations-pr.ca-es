---
title: Previsions i pressupostos del projecte
description: El Microsoft Dynamics 365 Finance proporciona previsions de projecte i pressupostos de projecte per administrar i controlar els vostres projectes.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749520"
---
# <a name="project-forecasts-and-budgets"></a>Previsions i pressupostos del projecte

[!include [banner](../includes/banner.md)]

Hi ha dues maneres d'administrar i controlar els vostres projectes: previsions de projecte i pressupostos de projecte. 

Utilitzeu les previsions del projecte si l'organització té una perspectiva operativa i si se centra en els ingressos i els costos derivats de transaccions específiques. Utilitzeu els pressupostos de projecte si l'organització està més centrada en els imports financers. 

Tant les previsions del projecte com els pressupostos del projecte utilitzen models de predicció per mantenir els imports de transaccions previstos. 

Cada mètode té els seus avantatges. Heu de tenir en compte els següents aspectes abans de seleccionar un mètode per a l'organització.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Previsió de projecte**                  | **Pressupost de projecte**                              |
| **Assignació de període**     | No podeu assignar explícitament transaccions al llarg d'un període fiscal. En lloc d'això, la previsió i el control de la previsió es basen en la vida del projecte. Com que les previsions es basen en una data concreta, heu d'inferir el període de la data. | No podeu assignar transaccions al llarg de tot un projecte o període fiscal. Si assigneu més d'un període, podeu transferir els imports sense utilitzar al següent període fiscal. |
| **Visualització de transaccions**  | Podeu visualitzar les transaccions en els formularis de previsió, on veureu les previsions per a tota l'empresa i per a tots els projectes, independentment de la jerarquia. Per centrar-vos en un projecte concret, heu de filtrar les dades.                                       | Podeu visualitzar les transaccions pressupostades per a una única jerarquia de projectes. Per tant, podeu visualitzar els detalls de les transaccions d'un projecte principal o dels seus subprojectes.                 |
| **Variables de la transacció** | Quan introduïu transaccions de previsió, podeu utilitzar tots els atributs que existeixen per a una transacció real. Això permet més detalls a la previsió. Per exemple, podeu introduir detalls per a les quantitats, els treballadors, els elements o les propietats de la línia.         | Quan introduïu els detalls del pressupost, només podeu utilitzar imports, categories i activitats.                    |
| **Seguretat**              | La previsió es basa en les transaccions que introduïu en els formularis de la previsió i no involucra cap mecanisme de control del procés. Qualsevol treballador que tingui permisos per a un formulari de previsió pot revisar-ne la informació sense l'aprovació.                                        | La pressupostació utilitza el sistema de flux de treball, que permet l'administració de canvis i us permet mantenir l'historial de les revisions.         |
| **Tipus d'entrada**           | Les entrades de transacció de previsió es basen en el nombre d'unitats i en el preus unitaris dels costos i les vendes.  | Els detalls del pressupost es basen en imports, que es divideixen entre costos i ingressos.                                          |
| **Models de previsió**       | Com que cada previsió s'ha d'associar amb un model, podeu crear diversos models de previsió i també configurar submodels.           | La pressupostació del projecte limita els models de previsió que s'utilitzen per a la pressupostació. Un nombre menor de models de previsió pot ajudar a augmentar la coherència en el nombre de prediccions.                           |
| **Sobrecostos**         | Només podeu permetre o no permetre l'entrada de transaccions que provocaran un sobrecost.   | El pressupost de projecte proporciona opcions de control addicionals per als usuaris. Podeu permetre els advertiments i sobrecostos.                    |
| **Control**               | El control de previsió es realitza mitjançant la reducció de la previsió. Els imports reals es resten dels saldos de les transaccions previstes sense cap pista d'auditoria. Això pot fer que sigui més difícil rastrejar on s'ha produït les transaccions reals.                   | Al control pressupostari del projecte, els imports reals es resten dels imports en el pressupost restant. Això permet una ruta d'auditoria més clara.                                   |

## <a name="project-forecasts"></a>Previsions de projecte
Quan utilitzeu la previsió del projecte, podeu introduir transaccions de previsió en formularis de previsió per a cada tipus de transacció. Tots els atributs que estan disponibles per a una transacció real es poden utilitzar per a una transacció de previsió; exemple, la rendibilitat de la línia, els atributs de línia, els treballadors o les descripcions. També podeu preveure quant de temps després d'incórrer en un cost facturareu al client. 

Les transaccions de previsió de projectes es basen en unitats i imports. 

Heu d'associar cada previsió d'un projecte amb un model de previsió. Quan introduïu una transacció de previsió, es suggereix automàticament un model de previsió. El model de previsió actua com a contenidor per a les transaccions previstes. 

Podeu designar els models de previsió com a submodels d'un model. Això us permet fer previsions per regió, període de temps o departament. Podeu copiar les transaccions previstes en un model per crear un model nou i també podeu transferir les transaccions al llibre major general. Com que hi ha una relació d'u a u entre una previsió i un model, cada model de previsió constitueix un pressupost independent per a un projecte. 

Els models de previsió poden utilitzar la reducció de la previsió com a mecanisme de control per als projectes. A la reducció de la previsió, les transaccions reals redueixen els saldos previstos a les transaccions. No obstant, com que la reducció de la previsió s'aplica al projecte més alt de la jerarquia, proporciona una visualització limitada dels canvis a la previsió. Per exemple, si un treballador està associat a un subprojecte, les transaccions reals del treballador es publicaran al projecte principal. Això pot fer difícil fer un seguiment dels canvis, perquè no podeu determinar fàcilment quina transacció de quin subprojecte ha provocat una reducció de l'import de la previsió. Per tant, és una bona idea crear una còpia d'un model de previsió per a la reducció de la previsió a l'ús. A continuació, podeu utilitzar informes per visualitzar el que s'havia previst inicialment. 

Podeu revisar, copiar, suprimir o transferir previsions de projecte a un pressupost d'un llibre major general. No obstant, no hi ha cap control del procés. Qualsevol treballador que tingui permís per a un formulari de previsió pot fer revisions sense revisió.

-   **Revisió**: podeu revisar una transacció de previsió en els mateixos formularis en què es van fer les entrades originals.
-   **Còpia o supressió**: quan copieu transaccions de previsió, copieu les línies d'operació d'un model de previsió a un altre model de previsió. Quan suprimiu una previsió, suprimiu les transaccions de previsió d'un model de previsió. Per limitar les transaccions de previsió que s'han copiat o suprimit, seleccioneu tipus de transaccions i dates específiques. Això us permet copiar o suprimir només les parts específiques d'una previsió.
-   **Transferència**: quan transferiu una previsió de projecte a un pressupost del llibre major general, transferiu les transaccions de previsió d'un model de previsió a un pressupost del llibre major general. Podeu sobreescriure qualsevol transacció prèviament transferida al pressupost del llibre major general a la qual transferiu la previsió del projecte.

## <a name="project-budgets"></a>Pressupostos de projecte
El pressupost de projecte és un mètode més senzill que la previsió, tot i que s'integra amb models de previsió. Utilitza un únic formulari d'entrada per als detalls i revisions del pressupost original i permet fer prediccions que es basen només en l'import, la categoria o l'activitat. 

Al pressupost del projecte, tots els pressupostos i revisions originals s'han d'enviar a un flux de treball del projecte per a la seva aprovació. Els fluxos de treball us permeten controlar el procés i crear un registre d'historial de canvis. 

El pressupost del projecte s'assembla a la pressupostació del llibre major general, però és més ràpid i més fàcil de configurar. Moltes de les opcions d'un pressupost de llibre major general, com ara les seqüències de nombres o la moneda, no s'hauran de configurar separadament per als projectes.

Els pressupostos del projecte s'associen automàticament amb dos models de predicció, un per al pressupost original i un per al pressupost restant. Per tant, els informes basats en models de previsió poden utilitzar dades pressupostàries. Quan es confirma un pressupost de projecte, el sistema crea transaccions de previsió basades en els models associats, que s'utilitzen per als informes i el control.

## <a name="forecast-models"></a>Models de previsió
Els models de previsió tenen una jerarquia d'una sola capa. Això vol dir que una previsió de projecte ha d'estar associada a un model de previsió.

Si utilitzeu la previsió del projecte, podeu identificar els models com a submodels. Això us permet creat previsions per departament, període de temps o regió. Per exemple, podeu crear un model de previsió per a un any i, a continuació, crear submodels per a les previsions regionals del nord-est, el sud-est, el nord-oest i el sud-oest que envien els caps regionals. En seleccionar les diferents opcions dels informes disponibles, podeu visualitzar la informació per previsió total o per submodel.



