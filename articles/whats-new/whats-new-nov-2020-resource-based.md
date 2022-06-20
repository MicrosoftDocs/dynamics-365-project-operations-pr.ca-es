---
title: 'Novetats de novembre de 2020: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de novembre de 2020 de Project Operations per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b98c968a040c14f4d11c350885e2cbb984596c48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923406"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de novembre de 2020: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest article s'aplica als components i versions següents Dynamics 365 Project Operations:

- Project Operations en entorn del CDS versió 4.4.0.70
- Gestió de projectes i comptabilitat en entorn Dynamics 365 Finance versió 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Actualitzacions al Project Operations per a escenaris basats en recursos/sense existències

### <a name="project-operations-on-cds"></a>Project Operations al CDS

| Àrea de característiques                 | Número de referència | Actualització de qualitat                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   Administració d'oportunitats       | 2036993          | Les línies de contracte de línia d'estimació i assignació de recursos s'actualitzen a les ofertes guanyadores quan el tipus de línia d'oferta és **Totes les tasques**.                                                 |
| Facturació i preus          | 2070392          | Les línies de contracte de projecte a la factura augmenten cada vegada que se selecciona **Actualitza les transaccions de la factura**.                                                                         |
| Planificació del projecte             | 2043336          | No es pot suprimir un registre de membre de l'equip del projecte.                                                                                                                                  |
| Planificació del projecte             | 2046013          | Comportament incoherent per a les columnes d'etiquetes d'estimacions durant la càrrega en comparació amb el canvi de tipus de fase de temps.                                                                                   |
| Planificació del projecte             | 2046647          | Les hores d'inici i d'acabament tenen un desplaçament d'una hora quan es generen requisits de recursos a partir dels membres de l'equip del projecte.                                                                      |
| Planificació del projecte             | 2053879          | (Per a la pròxima implementació del CDS) PublishUnassignedAssignments trenca un intent de desar una tasca amb l'error, "El valor enviat a ConditionOperator.In està buit".                       |
| Planificació del projecte             | 2055501          | Deixar buida la **Data d'inici del projecte** provoca un error a la planificació.                                                                                                      |
| Planificació del projecte             | 2066817          | No es pot crear un recurs genèric amb el selector de persones de la pestanya **Tasques**.                                                                                                   |
| Planificació del projecte             | 2067034          | El botó **Visualitza els detalls** no està disponible a la pàgina **Detalls de la tasca**.                                                                                                       |
| Administració de recursos          | 2046667          | Els membres de l'equip genèrics no se suprimeixen fins i tot després de complir tots els recursos.                                                                                                    |
| Entrada de temps i despesa ràpida | 2047499          | El botó **Nou** de la pàgina Entrada de temps obre la pàgina **Nova signatura de correu electrònic**.                                                                                               |
| Entrada de temps i despesa ràpida | 2059859          | S'obre una finestra emergent inesperada en crear una entrada de despesa.                                                                                                                         |
| Un altre                        | 2044181          | [Desinstal·lació de la comanda de compra]: l'error "El registre no està disponible" es produeix quan intenteu desinstal·lar les solucions msdyn_ProjectServiceCore_Patch i msdyn_ProjectServiceCore.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestió de projectes i comptabilitat en Dynamics 365 Finance

| Àrea de característiques        | Número de referència | Actualització de qualitat                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reconeixement d'ingressos | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | El percentatge d'estimació del projecte complet és incorrecte quan el contracte utilitza una moneda estrangera i el percentatge de progrés del treball per al mètode complet.                     |
| Reconeixement d'ingressos | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | No es poden comptabilitzar estimacions amb el mètode de compleció **Cost real**.                                                                                                    |
| Reconeixement d'ingressos | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Es produeix un error de supressió a causa d'un error de desequilibri de comprovants quan la moneda de l'empresa i la moneda de la transacció són diferents.                                              |
| Administració de despeses  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Per als usuaris que no són administradors, els valors de cerca de columnes de línia de despeses, com ara **ID del projecte** i **Categoria de despesa** no es mostren correctament al marc del connector de dades. |
| Administració de despeses  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | El valor per defecte de la propietat de línia no es mostra a les categories de despeses.                                                                                                         |
| Administració de despeses  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | La integració de despeses ha d'incloure la propietat de línia de l'informe de despeses.                                                                                             |
| Facturació           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | No es poden comptabilitzar propostes de factura de projecte a causa d'un missatge d'error que indica que la combinació d'FD no s'ha validat.                                                    |
| Facturació           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | No es poden visualitzar les transaccions des de la pàgina de detalls de la **factura**.                                                                                                              |
| Facturació           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Es poden suprimir les línies de propostes de factura.                                                                                                                                  |
| Comptabilitat del projecte  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Els elements del menú **Previsió** no són visibles a la pàgina de llista **Projectes**.                                                                                                   |
| Comptabilitat del projecte  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | No es pot obrir **Extracte del projecte**   > **Transaccions i previsió**.                                                                                                       |
| Comptabilitat del projecte  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Ajusta la comptabilitat** no està habilitat per a les transaccions de projectes facturats.                                                                                                  |
| Comptabilitat del projecte  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Els detalls de comptabilitat no s'inclouen a la taula **ProjCDSActualsImport** quan es comptabilitza el diari **Integració**.                                                  |
| Comptabilitat del projecte  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | L'entrada de previsió del projecte es duplica quan suprimiu i, a continuació, torneu a afegir una assignació de recursos.                                                                            |
| Comptabilitat del projecte  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | La selecció d'un enllaç d'ID del projecte no obre l'URL de l'enllaç profund del CDS.                                                                                                         |
| Comptabilitat del projecte  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | No es pot actualitzar la data d'inici d'una tasca al CDS.                                                                                                                           |
| Comptabilitat del projecte  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Si habiliteu la característica, no són possibles diverses línies de contracte sense la integració del CDS.                                                                                   |

### <a name="regulatory-updates"></a>Actualitzacions reglamentàries
Per obtenir informació sobre les actualitzacions reguladores de les aplicacions financeres i d'operacions, consulta [Actualitzacions reguladores](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió al LCS i veure les actualitzacions reglamentàries planificades mitjançant l'eina de cerca de problemes. La cerca de problemes us permet cercar per país, tipus de funció i llançament.


[!INCLUDE[footer-include](../includes/footer-banner.md)]