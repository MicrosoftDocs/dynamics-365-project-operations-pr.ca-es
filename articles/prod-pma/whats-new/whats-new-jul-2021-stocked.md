---
title: Novetats i canvis de juliol de 2021 del Project Operations per a escenaris basats en producció o mantinguts en existències
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juliol de 2021 del Project Operations per a escenaris basats en producció o mantinguts en existències.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028828"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Novetats i canvis de juliol de 2021 del Project Operations per a escenaris basats en producció o mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Aquest article s'aplica als components i versions següents del Dynamics 365 Project Operations:

- Administració de projectes i comptabilitat en l'entorn del Dynamics 365 Finance, versió 10.0.20
 
### <a name="quality-updates"></a>Actualitzacions de qualitat
                                                                                                                                                                                  
| Àrea de característiques                      | Número de referència| Actualització de qualitat                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administració i comptabilitat de projectes | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Els registres de compromís de cost d'un requisit de compra es desactiven tan bon punt s'allibera la comanda de compra del problema de requisit de compra.                                                                           |
| Administració i comptabilitat de projectes | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | La validació del pressupost té lloc dues vegades segons un requisit de compra. Aquesta duplicació significa que el requisit no es pot tancar i no es crea la comanda de compra corresponent.                                                                                                                        |
| Administració i comptabilitat de projectes | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | La regla de facturació **Percentatge de facturació** no s'ha pogut completar a causa d'un problema d'arrodoniment.                                                                              |
| Administració i comptabilitat de projectes | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Quan ajusteu la transacció i el percentatge té decimals, el cost i el preu de venda no s'ajusten correctament.                                      |
| Administració i comptabilitat de projectes | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | L'explorador d'orígens de comptabilitat mostra les hores d'una sola línia de full d'hores per a diverses línies de full d'hores amb activitats diferents.                                      |
| Administració i comptabilitat de projectes | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Les visualitzacions desades i la personalització de detalls de les línia del full d'hores provoca que el sistema sempre obri els detalls del primer full d'hores de la llista quan intenteu obrir-ne un.  |
| Administració i comptabilitat de projectes | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | El node arrel del projecte desapareix i els registres d'estructura del desglossament del treball se suprimeixen després de la importació.                                                                                             |
| Administració i comptabilitat de projectes | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Quan es reben i s'emeten parcialment articles des del requisit d'articles, el sistema actualitza el balanç de consum del pressupost incorrecte. |
| Administració i comptabilitat de projectes | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Les comandes de compra de retenció del projecte no mostren correctament els totals a la subfinestra **Totals** ni a la quadrícula **Factura pendent**.                                                                  |
| Administració i comptabilitat de projectes | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | En tancar inventari, els ajustaments de cost dels articles del projecte es publiquen al compte de balanç en comptes del compte de beneficis i pèrdues.                                                            |
| Administració i comptabilitat de projectes | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un val de transacció publicada al projecte i un val d'estimació utilitzen USD com a moneda de comptabilitat, però l'import mostra quin en seria l'equivalent en CAD.              |
| Administració i comptabilitat de projectes | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Els costos confirmats amb un requisit d'article i una comanda de compra no són correctes en el procés de facturació de la comanda de compra amb una part del producte com a rebut i una altra com a factura.       |
| Administració i comptabilitat de projectes | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | L'ajustament del projecte no actualitza correctament l'import de les vendes amb els costos indirectes.                                                                                    |
| Administració i comptabilitat de projectes | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | A la taula **Full d'hores** falta una relació definida amb la visualització **Treballador o Recurs**.                                                                                   |
| Administració i comptabilitat de projectes | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | No es pot emplenar el camp **Número d'activitat** quan el seleccioneu al menú desplegable per a un full d'hores entre empreses.                                                                 |
| Administració i comptabilitat de projectes | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | No podeu afegir un camp personalitzat **Finalitat** o **Descripció de l'activitat** a les pàgines següents: **Transacció publicada al projecte**, **Creació de la proposta de factura** o **Proposta de factura**.  |
| Administració i comptabilitat de projectes | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Es proporciona el control de data de lliurament incorrecte quan creeu requisits d'article mitjançant l'administració de dades (**ProjSalesItemRequirementEntity**).                                              |
| Administració i comptabilitat de projectes | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Quan seleccioneu un identificador de contracte de projecte al Finance, l'entorn integrat del Project Operations obre la pàgina per crear un registre nou en comptes d'obrir el contracte de projecte existent.                                                                                                                 |
| Administració i comptabilitat de projectes | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  L'etiqueta "@SYS4083080" ("No es pot trobar cap registre de treballador únic que correspon als valors introduïts") no està traduït al danès.                                |
| Administració i comptabilitat de projectes | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | El camp **Grup d'impostos sobre les vendes d'articles** no es pot editar en una proposta de factura.                                                                               |
| Administració i comptabilitat de projectes | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | El cost confirmat està inflat amb imports fiscals no deduïbles.                                                                                                    |
| Administració i comptabilitat de projectes | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Publicar un full d'hores entre empreses amb diversos projectes i diferents mesures financeres genera valors inesperats al llibre major.                             |
| Administració i comptabilitat de projectes | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Les línies de proposta de factura estan duplicades a causa de diverses instàncies del procés periòdic **Importa des de la còpia intermèdia** que s'executen alhora.                                      |
| Administració i comptabilitat de projectes | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Hi ha un error en publicar la proposta de factura de nota de crèdit, de manera que les transaccions del val no s'equilibren.    |
| Administració i comptabilitat de projectes | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Els costos confirmats del projecte no són correctes després d'alliberar factures pendents retingudes.                                                                             |
| Administració i comptabilitat de projectes | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | No podeu crear una nota de crèdit per a una comanda de vendes del projecte quan l'impost es troba en una moneda diferent de la moneda de l'empresa.                                      |
| Administració i comptabilitat de projectes | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | En suprimir un contracte, se suprimeix també l'adreça associada al client.                                                                                     |
| Administració i comptabilitat de projectes | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | No es pot publicar una proposta de factura que sigui el resultat d'una correcció de transacció de temps negativa.                                                                    |
| Viatge i despesa                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Els impostos es calculen de manera diferent als informes de despeses.                                                                                                                  |
| Viatge i despesa                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | L'actualització de la versió **DB72_Expense.updateTrvExpTransProjTransId()** no permet que **trvExpTrans.ReferenceDataAreaId** creï la nova seqüència de números.                    |
| Viatge i despesa                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | L'import registrat no es mostra amb el camp obligatori.                                                                                                             |
| Viatge i despesa                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Millores en el rendiment d'adjuntar una despesa a l'informe de despeses mitjançant la interfície d'usuari de despeses noves.                                                            |
| Viatge i despesa                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Podeu suprimir els informes de despeses publicats.                                                                                           |
| Viatge i despesa                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | El missatge de norma de despeses es visualitza diverses vegades.                                                                                                       |
| Viatge i despesa                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | El camp **Mètode de pagament** s'inclou a la subfinestra **Despesa nova**.                                                                                                      |
| Viatge i despesa                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | L'eina **Restableix l'estat del document de despeses** ha de restablir l'estat de l'informe de despeses a **Esborrany** si no s'ha trobat el flux de treball. 

### <a name="regulatory-updates"></a>Actualitzacions reglamentàries
Per obtenir informació sobre les actualitzacions reglamentàries de les aplicacions de finances i operacions, vegeu [Actualitzacions reglamentàries](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió al Lifecycle Services (LCS) i visualitzar les actualitzacions normatives planificades mitjançant l'eina de cerca de problemes. La cerca de problemes us permet cercar per país, tipus de funció i llançament.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
