---
title: 'Novetats de juliol de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles a la versió de juliol de 2021 del Project Operations per a escenaris basats en recursos/no mantinguts en existències.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c004a6adc265f8f02fc557700d9b88a174c221c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931686"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de juliol de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

*S'aplica a: Project Operations per a escenaris basats en recursos/sense cotització*

Aquest article s'aplica als components i versions següents del Dynamics 365 Project Operations:

   - Project Operations en un entorn del Microsoft Dataverse, versió 4.12.0.148 o 4.12.0.152.
   - Administració de projectes i comptabilitat en l'entorn del Dynamics 365 Finance, versió 10.0.20.

## <a name="features-included-in-this-release"></a>Característiques incloses en aquesta versió

En aquesta versió s'inclouen les característiques següents:

- Capacitat per als administradors de poder visualitzar registres de PSS i de conjunt d'operacions des del menú de configuració. Els registres s'emmagatzemen durant 90 dies.

## <a name="project-operations-dual-write-maps-updates"></a>Actualitzacions de les assignacions de doble ecriptura del Project Operations

En aquesta versió no hi ha actualitzacions per a les assignacions d'escriptura doble del Project Operations.

Per a una llista actual i versions de les assignacions d'escriptura doble del Project Operations, consulteu [Versions de les assignacions d'escriptura doble del Project Operations](../environment/resource-dual-write-maps.md).

Executeu sempre la versió més recent de l'assignació a l'entorn i habiliteu totes les assignacions de taules relacionades a mida que actualitzeu la versió de la solució del Finance i del Dataverse del Project Operations. És possible que algunes característiques i capacitats no funcionin correctament si la versió més recent del mapa no s'activa. Podeu veure la versió activa de l'assignació a la pàgina **Escriptura doble**, a la columna **Versió**. Per activar una versió nova de l'assignació, seleccioneu les **Versions de l’assignació de taules**, seleccioneu la versió més recent i deseu la versió seleccionada. Si heu personalitzat una assignació de taules llesta per al seu ús, torneu a aplicar els canvis. Per a més informació, vegeu [Administració del cicle de vida de les aplicacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si teniu qualsevol problema relacionat amb l'inici de l'assignació, seguiu les instruccions de la secció [Problema Falten columnes de la taula a les assignacions](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) de la guia de solució de problemes de l'escriptura doble.

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques**              | **Número de referència** | **Actualització de qualitat**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facturació i preus           | 2224046              | El camp **Classe de la transacció** es pot editar a la pestanya **Detalls de la línia d’oferta**, però està blocat si treballeu des de la pàgina **Detalls de la línia d’oferta**.                                                                     |
| Facturació i preus           | 2224400              | Es produeix un error en l'acció **Tanca l'oferta com a guanyada** quan una oferta no té fites de data.                                                                                                                                    |
| Facturació i preus           | 2234089              | Quan introduïu manualment una descripció del producte, s'esborra després d'introduir la quantitat per a una estimació de material.                                                                                                                         |
| Facturació i preus           | 2234100              | La quadrícula **Configuració de facturació de la tasca** no inclou la columna **Material** i és un valor a la pestanya **Facturació de la tasca** del projecte.                                                                                                       |
| Facturació i preus           | 2277409              | L'identificador del producte no està disponible al detall de la línia de contracte per a una línia de tipus de material.                                                                                                                                        |
| Facturació i preus           | 2281728              | La creació d'una línia de contracte torna a avaluar de manera innecessària els valors reals, la qual cosa fa que augmenti significativament el volum de dades i afecti el rendiment.                                                                                |
| Facturació i preus           | 2298668              | Les línies del llibre diari associades a una despesa recuperada i suprimida no s'eliminen.                                                                                                                                     |
| Facturació i preus           | 2300192              | Quan diversos usuaris editen una factura, és possible crear un detall de la línia de factura nou en una factura confirmada.                                                                                   |
| Facturació i preus           | 2301569              | Les factures no es poden corregir si s'ha aplicat una retenció per valor de 0 \$.                                                                                                                                        |
| Facturació i preus           | 2307965              | Es produeix un error si es crea un preu de categoria on falten valors.                                                                                                                           |
| Facturació i preus           | 2326870              | Es produeix un error a **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** si **producttypecode** és nul.                                                                            |
| Facturació i preus           | 2332732              | Es produeix un error si es crea una fita de línia de contracte sense una línia de comanda.                                                                                                                |
| Planificació i seguiment de projectes | 2181094              | L'API de planificació de projectes admet ara registres de PSS i del conjunt d'operacions que s'emmagatzemen durant 90 dies.                                                                                                                  |
| Planificació i seguiment de projectes | 2254201              | L'etiqueta **Mode de planificació** s'actualitza amb detalls que descriuen la lògica per defecte.                                                                                                                                      |
| Planificació i seguiment de projectes | 2300252              | La memòria cau de resposta **openProject** s'actualitza i inclou el propietari del testimoni a la clau de la memòria cau, l'**adreça URL base** i l'**adreça URL del segment**, de manera que l'**adreça URL de la sol·licitud** es pot tornar a crear si canvia l'**adreça URL base**. |
| Planificació i seguiment de projectes | 2301312              | S'ha suprimit **msdyn_membershipstatus** de la visualització **Membre de l'equip del projecte**.                                                                                                                                        |
| Planificació i seguiment de projectes | 2302759              | Els productes es recuperen innecessàriament a les pestanyes **Assignacions de recursos**, **Estimacions** i **Estimacions de despeses**.                                                                                                        |
| Planificació i seguiment de projectes | 2308050              | Es produeix l'error "No s'ha pogut obtenir el testimoni per parlar amb el servei remot" amb **CopyProject**.                                                                                                                           |
| Planificació i seguiment de projectes | 2322650              | La visualització **Llista de tasques del projecte** s'ha actualitzat per mostrar la data de la tasca per defecte.                                                                                                            |
| Planificació i seguiment de projectes | 2327266              | **CopyProject** genera l'error "No s'ha trobat la clau al diccionari" quan es copien estimacions.                                                                                                      |
| Planificació i seguiment de projectes | 2328123              | **CopyProject** genera l'error "No s'ha pogut obtenir el testimoni per parlar amb el servei remot".                                                                                                                          |
| Planificació i seguiment de projectes | 2336258              | **CopyProject** copia incorrectament els noms de funció dels recursos.                                                                                                                                                 |
| Facturació i preus           | 2224476              | El camp **Recurs que es pot reservar** no canvia per defecte correctament a l'usuari que ha iniciat la sessió a la pàgina **Ús del material**.                                                                                                            |
| Administració de recursos           | 2277249              | Es produeix un error quan s'actualitza un requisit de recursos que no està basat en un projecte.                                                                                                            |
| Administració de recursos           | 2323869              | L'ús del recurs no reconeix correctament els recursos filtrats.                                                                                                                                             |
| Temps i despesa              | 2176538              | S'apliquen operadors de filtre incorrectes al control **Entrada de temps**.                                                                                                                                                   |
| Temps i despesa              | 2177462              | Si suprimiu una entrada de temps a la quadrícula, no s'actualitza l'estat dels botons **Envia**, **Recupera**, **Suprimeix** i **Edita l'entrada** segons s'espera.                                                                                        |
| Temps i despesa              | 2299985              | **TimeEntriesImportFromResourceAssignment** no conserva les hores d'inici i finalització els contorns de l'assignació.                                                                                                  |
| Temps i despesa              | 2318426              | Després d'enviar una entrada d'hora, els camps bloquejats encara es poden editar.                                                                                                                                   |
| Temps i despesa              | 2323749              | Es produeix un error quan es crea una despesa des de la pestanya **Relacionat** d'un recurs que es pot reservar.                                                                                                      |
| Temps i despesa              | 2327678              | Quan creeu una entrada de temps des de la pestanya **Relacionat** d'un recurs que es pot reservar, el recurs principal no es passa al control d'entrada de temps.                                                                            |
| General                       | 2296857              | Seguiment del progrés de les feines que s'executen durant molt de temps.                                                                                                                                                                        |
| General                       | 2253682              | La solució d'escriptura doble del Project Operations no s'ha d'instal·lar quan s'instal·la la versió bàsica de l'escriptura doble en un entorn sense la solució d'orquestració d'escriptura doble.                                                |
| General                       | 2316420              | Es produeix un error en proveir la versió bàsica del Project Service si canvia la unitat de negoci de l'usuari de l'aplicació.                                                                                                                     |
| General                       | 2376405              | S'ha solucionat un problema d'actualització de l'editor (l'actualització de la qualitat està disponible a la versió 4.12.0.152)                                                                                                                     |
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Administració de projectes i comptabilitat al Dynamics 365 Finance

| Àrea de característiques                      | Número de referència | Actualització de qualitat                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Administració i comptabilitat de projectes | 4620267          | No es poden personalitzar formularis per afegir un camp **Finalitat** a les pàgines següents **Transacció publicada al projecte**, **Creació de la proposta de factura** o **Proposta de factura**.                                                                                                                                                                                         |
| Administració i comptabilitat de projectes | 4613449          | Quan seleccioneu un identificador de contracte de projecte al Finance, l'entorn integrat del Project Operations obre la pàgina per crear un registre nou, en comptes de la pàgina de contractes del projecte que ja s'han creat.                                                                                                                                           |
| Administració i comptabilitat de projectes | 4614445          | A la implementació de l'escenari integrat amb el Project Operations, no podeu editar el camp **Grup d'impostos sobre les vendes d'articles** a la proposta de factura que s'importa des de la còpia intermèdia. El grup d'impostos sobre les vendes d'articles s'ha de poder editar per a una proposta de factura oberta de tots els tipus de transaccions, que inclouen el compte, les hores, les despeses, les tarifes i els articles. |
| Administració i comptabilitat de projectes |                  | No es pot publicar una proposta de factura que sigui el resultat d'una correcció de transacció de temps negativa.                                                                                                                                                                                                                                              |
| Administració i comptabilitat de projectes |                  | Les línies de proposta de factura estan duplicades a causa de diversos processos periòdics **Importa des de la còpia intermèdia** que s'executen alhora.                                                                                                                                                                                                                |

