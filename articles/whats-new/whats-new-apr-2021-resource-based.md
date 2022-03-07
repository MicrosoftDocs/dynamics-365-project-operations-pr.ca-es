---
title: "Novetats de l'abril de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències"
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles a la versió d'abril de 2021 del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867981"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de l'abril de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

- Project Operations en entorn del Dataverse versió 4.9.0.221
- Administració de projectes i comptabilitat a l'entorn del Dynamics 365 Finance versió 10.0.17

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Materials no mantinguts en existències per als projectes. Les capacitats principals són:
  - Estimar i calcular preus de materials no mantinguts en existències durant el cicle de venda d'un projecte. Per obtenir més informació, vegeu [Configuració de les tarifes de cost i de vendes per als productes del catàleg (bàsica)](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Fer el seguiment de l'ús de materials no mantinguts en existències durant el lliurament del projecte. Per obtenir més informació, vegeu [Registre de l'ús de materials als projectes i les tasques de projecte](../material/material-usage-log.md).
  - Facturació amb costos de materials no mantinguts en existències. Per obtenir més informació, vegeu [Administració del treball pendent de facturació](../proforma-invoicing/manage-billing-backlog.md).
- Facturació basada en tasques: s'ha afegit la capacitat d'associar tasques de projecte amb línies de contracte del projecte i, d'aquesta manera, sotmetre-les al mateix mètode de facturació, freqüència de facturació i clients que la línia de contracte. Aquesta associació garanteix la facturació, la comptabilitat, l'estimació dels ingressos i el reconeixement de la feina amb precisió d'acord amb aquesta configuració en les tasques de projecte.
- Les noves API del Dynamics 365 Dataverse permeten crear, actualitzar i suprimir operacions amb **Entitats de planificació**. Per obtenir més informació, vegeu [Ús de les API de planificació per realitzar operacions amb entitats de Planificació](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations al Dynamics 365 Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 2124532 | El botó **Factura correcta** es visualitza en una factura proforma quan l'import de retenció o l'import de retenció aplicat està present a la factura original. El botó només es visualitza per als entorns amb la versió 10.0.19 de Finance o posterior. |
| Facturació i preus | 2224568 | S'ha afegit lògica per permetre personalitzacions que impliquen la invocació del complement de confirmació de la factura. |
| Facturació i preus | 2101098 | S'ha millorat la lògica dels camps per defecte a la factura proforma: **Adreça de facturació**, **Nom de facturació** i **Condicions de pagament** ara tenen com a valors per defecte els del registre de client de contracte de projecte corresponent. |
| Facturació i preus | 2021413 | S'han actualitzat els camps **Cost real** i **Vendes** de l'entitat **Tasca** per incloure els valors de vendes de les despeses no facturades i facturades en les tasques. |
| Facturació i preus | 2182110 | Quan es copia un contracte de projecte, l'identificador de línia de contracte es torna a generar al contracte del projecte de destinació per assegurar que és únic. |
| Administració d'oportunitats | 2186741 | S'han afegit validacions per assegurar que el camp **Origen** i el **Tipus de transacció** no es poden actualitzar en els detalls de la línia d'oferta existent. |
| Administració d'oportunitats | 2191353 | Les fites no s'han de crear en una línia de contracte de temps i material. |
| Administració d'oportunitats | 2216956 | Problemes corregits amb **Actualitza els preus**. |
| Planificació i seguiment | 2182979 | La funció de còpia del projecte s'ha millorat per garantir que les línies de previsió de la despesa es copien del projecte original. |
| Planificació i seguiment | 2184144 | La funció de còpia del projecte s'ha millorat per garantir que el nom de posició del recurs es copia del projecte original. |
| Planificació i seguiment | 2184799 | Còpia del projecte: s'ha millorat el control per assegurar que la data d'inici prevista no es pot canviar quan la còpia està en curs. |
| Planificació i seguiment | 2185134 | Còpia del projecte: la data d'inici prevista per al projecte de destinació es defineix com la data d'avui. |
| Planificació i seguiment | 2196373 | Còpia del projecte: assegureu-vos que els registres de l'administrador del projecte i dels membres de l'equip no estan duplicats a l'equip del projecte. |
| Planificació i seguiment | 2211833 | Còpia del projecte: les assignacions de recursos es copien des de la tasca de projecte d'origen al projecte de destinació. |
| Planificació i seguiment | 2186541 | Es solucionen problemes a la quadrícula **Estimacions** en agrupar per recurs. |
| Planificació i seguiment | 2166906 | La categoria de transacció d'una tasca s'ha de copiar a l'entitat **Assignació de recursos**. |
| Administració de recursos | 2125362 | S'han corregit problemes a l'hora de crear un membre de l'equip genèric utilitzant un mètode basat en hores. |
| Temps i despesa | 2113603 | S'ha corregit el problema relacionat amb la personalització en suprimir atributs de la pàgina **Entrada de temps**. Ara, el sistema comprova si l'atribut existeix a la pàgina abans d'accedir-hi mitjançant un script. |
| Temps i despesa | 2204377 | Els fulls d'hores copiats s'han de mostrar automàticament quan seleccioneu **Copia la setmana** durant l'entrada de l'hora. |
| Temps i despesa | 2209059 | El camp **Estat** es pot editar per a les entrades de temps del Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Administració i comptabilitat de projectes | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L'eliminació de previsió inversa no funciona a **Periòdic**.  |
| Administració i comptabilitat de projectes | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | La característica **Ajustament de comptabilitat** crea un problema amb comptes de llibre major que no tenen seleccionat **No permetis l'entrada manual**. |
| Administració i comptabilitat de projectes | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | S'ha afegit lògica empresarial a les factures de correcció de processos, incloent-hi l'import de retenció o l'import de retenció aplicat. |
| Administració i comptabilitat de projectes | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | El valor de vendes WIP que es publiquen a la facturació de projectes entre empreses tria un compte inesperat. |
| Administració i comptabilitat de projectes | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Quan es treballa amb retencions al Project Operations, si canvieu el projecte per defecte d'un contracte després de facturar els prepagaments es produeixen problemes amb les deduccions entrants. |
| Administració i comptabilitat de projectes | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Al Project Operations, si suprimiu un projecte d'un contracte, cal que restabliu el projecte per defecte del contracte, si cal. |
| Administració i comptabilitat de projectes | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Al Project Operations, es mostren línies de despesa errònies a la llista **Afegeix línia** de la factura entre empreses. |
| Administració i comptabilitat de projectes | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Al Project Operations, la pàgina **Contracte de compra** no està visible a les entitats jurídiques de finances integrades amb el Project Operations. |
| Administració i comptabilitat de projectes | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | A causa d'un error d'integració del Dataverse, no podeu convertir una oferta en guanyada al Project Operations. |
| Administració i comptabilitat de projectes | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** pot definir l'adreça de factura de la font de finançament d'un client diferent.  |
| Administració i comptabilitat de projectes | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Al Project Operations, no se seleccionen dimensions quan creeu una factura de comptabilització per a una transacció. |
| Viatge i despesa | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | El saldo de l'avançament en efectiu no s'actualitza per a un informe de despeses si està aprovat i comptabilitzat per línies. |
| Viatge i despesa | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Els impostos dels informes de despeses entre empreses detallats no es calculen correctament. |
| Viatge i despesa | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Els camps addicionals relacionats amb els projectes es visualitzen a la pàgina **Informes de despesa entre empreses** actualitzats. |
| Viatge i despesa | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Es produeix un missatge d'error incorrecte als rebuts de capçalera dels informes de despeses. |
| Viatge i despesa | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Un informe de despesa no es comptabilitza correctament en un escenari entre empreses si l'impost de vendes es comptabilitza a l'entitat legal de destinació. |
| Viatge i despesa | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Les dates d'enviament d'informes no s'imprimeixen als informes de despeses aprovats. |
| Viatge i despesa | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Els camps **Data d'aprovació** i **Data de rebuig** no s'emplenen després d'aprovar una despesa. |
| Viatge i despesa | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | El requisit de viatge creat per a un treballador es pot utilitzar per a un altre informe de despesa del treballador. |
| Viatge i despesa | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Les categories de despesa es bloquegen quan s'afegeix una línia de despesa nova. |
| Viatge i despesa | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | En afegir detalls a les línies d'informe de despeses ja dividides es comptabilitza de manera incompleta el val de Comptes a pagar\Llibre major i es trenca l'Explorador d'origen de comptes perquè **TRVEXPTRANS.SOURCEDOCUMENTLINE** està duplicat. |
| Viatge i despesa | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | La política de requisit de viatge no funciona segons s'espera. |
| Viatge i despesa | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | El nom del compte de proveïdor no es mostra a les transaccions de projecte comptabilitzades per als informes de despeses. |
| Viatge i despesa | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | A Project Operations, no podeu aprovar el temps amb una tasca per a un projecte entre empreses. |
| Viatge i despesa | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | La categoria de devolució d'avançament en efectiu no actualitza els saldos d'avançaments en efectiu quan es comptabilitzen. |
| Viatge i despesa | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | El preu de venda es calcula incorrectament per als informes de despeses que s'han creat en una moneda estrangera amb transaccions de targeta de crèdit importades i s'associen a un projecte. |
| Viatge i despesa | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | S'ha revertit l'entitat de dades **TrvRequisitionLine** i l'índex únic associat. |
| Viatge i despesa | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | S'ha afegit instrumentació a la generació **SOURCEDOCUMENTLINE**. |
| Viatge i despesa | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Es mostra el llibre diari de llibre major auxiliar incorrecte en un escenari entre empreses si l'impost de vendes es comptabilitza a l'entitat legal de destinació. |
| Viatge i despesa | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Al Project Operations, les estimacions de despeses no se suprimeixen de Finance quan se suprimeixen del Dataverse. |
| Viatge i despesa | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Quan una categoria de despesa és una categoria que no és de projecte, les dimensions financeres seleccionades a la pàgina **Despesa** no es copien a l'informe de despeses. |
