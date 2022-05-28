---
title: 'Novetats de gener de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències'
description: Aquest tema proporciona informació sobre les actualitzacions de qualitat disponibles en el llançament de gener de 2021 del Project Operations per a escenaris de recursos/sense existències.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 50874d771afe03b08bd95b670f7095bc2d61509d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599534"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novetats de gener de 2021: Project Operations per a escenaris basats en recursos/no mantinguts en existències

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_


Aquest tema s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.6.0.154
  - Gestió de projectes i comptabilitat en entorn Dynamics 365 Finance versió 10.0.16

## <a name="quality-updates"></a>Actualitzacions de qualitat

### <a name="project-operations-on-dataverse"></a>Project Operations a Dataverse

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| **Implementació i configuració** | 2106818 | S'ha corregit el nom del recurs web que estava provocant problemes relacionats amb la personalització d'una pàgina. |
| **Facturació i preus** | 2091908 | S'ha corregit la visibilitat de les opcions **Bloqueja els preus** i **Utilitza els preus actuals** a la pàgina **Factura** quan s'instal·la el Project Operations conjuntament amb el Dynamics 365 Field Service. |
| **Facturació i preus** | 2103058 | S'han actualitzat els **totals del projecte** per gestionar els valors nuls del cost real en una tasca. |
| **Facturació i preus** | 2116100 | S'han millorat els missatges d'error utilitzats amb la funcionalitat **Corregeix les entrades en els valors reals**. |
| **Facturació i preus** | 2116129 | S'ha millorat la visibilitat de les estimacions de despeses a la pestanya **Estimacions** de la pàgina **Projectes**. |
| **Facturació i preus** | 2119112 | S'ha arreglat l'agregació de les vendes reals i el cost real quan es fan servir diferents tipus de canvi. |
| **Facturació i preus** | 2134705 | S'ha corregit l'error "No es pot llegir la propietat **getResourceString** de no definit" quan s'obre la pàgina **Factura** i el Field Service està instal·lat. |
| **Administració d'oportunitats** | 2022195 | La quadrícula de facturació basada en tasques de la pàgina **Projecte** inclou una icona que indica que hi ha un contracte o una línia d'oferta enllaçada a la tasca. |
| **Administració d'oportunitats** | 2029135 | S'ha corregit l'error del procés de negoci que es produeix quan un usuari prova d'obrir una línia de factura en una factura confirmada que té un import facturat per avançat. |
| **Administració d'oportunitats** | 2040713 | S'ha corregit l'error de seqüència d'ordres que es produeix en crear una factura a partir d'un contracte i el Field Service està instal·lat. |
| **Planificació i seguiment de projectes** | 2090202 | S'han marcat les regles de negoci que ja no s'utilitzen com a **Obsoletes**. |
| **Temps i despesa** | 2091249 | S'han ajustat els controls de manera que els usuaris no poden canviar la tasca en una entrada de temps enviada o aprovada. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Gestió de projectes i comptabilitat en Dynamics 365 Finance

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| **Administració i comptabilitat de projectes** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Import del contracte incorrecte a la pàgina **On-account** d'un projecte de preu fix amb diverses fonts de finançament. |
| **Administració i comptabilitat de projectes** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | El contenidor **Invoiceproposal.PSAnfRefProjId** no mostra l'identificador del projecte per al flux de treball, **reviseu les propostes de factures del projecte**. |
| **Administració i comptabilitat de projectes** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Es fa servir la data de descompte en efectiu incorrecta quan es publiquen propostes de factura de projecte. |
| **Administració i comptabilitat de projectes** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Suprimir i llegir les assignacions de recursos a Project Operations duplica les entrades de previsió de projecte a Finances. |
| **Administració i comptabilitat de projectes** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | A Project Operations, no podeu crear estimacions de projecte a Dataverse sense tenir una línia de contracte al projecte. |
| **Administració i comptabilitat de projectes** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | La dimensió financera d'una transacció de despesa del projecte no se sincronitza amb el val relacionat i la distribució comptable de l'informe de despeses quan els costos es publiquen a Balanç. |
| **Administració i comptabilitat de projectes** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filtrar **l'estat de la factura** en transaccions de projecte publicades per a projectes de preu fix no funciona. |
| **Administració i comptabilitat de projectes** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L'eliminació de previsió inversa no funciona a la secció **Periòdic**. |
| **Administració i comptabilitat de projectes** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Es poden suprimir les línies de proposta de factura a Project Operations quan s'integra amb Dataverse. |
| **Administració i comptabilitat de projectes** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Evitar que s'habiliti la característica de línies de contracte múltiples sense la integració de Dataverse. |
| **Administració i comptabilitat de projectes** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Quan la factura a compte és igual a guanys i pèrdues, els ingressos facturats es mostren com a zero a la pàgina Estimacions. |
| **Administració i comptabilitat de projectes** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Les correccions de factura no funcionen en entorns integrats. |
| **Administració i comptabilitat de projectes** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Quan es publica el valor de vendes WIP a la facturació de projectes entre empreses, es tria un compte incorrecte. |
| **Administració i comptabilitat de projectes** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | A Project Operations, les dependències de les tasques de previsió al Dataverse no es poden actualitzar. |
| **Administració i comptabilitat de projectes** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | La supressió repetida dels diaris d'integració del Projecte Operations a l'estat de Finances genera una pèrdua de dades. |
| **Administració i comptabilitat de projectes** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Es produeix l'error següent quan es publica una proposta de factura de projecte "Transacció no fa balanç en la moneda d'informes quan s'afegeix la factura anticipada descomptada". |
| **Administració i comptabilitat de projectes** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | S'inclou un identificador de projecte erroni a les deduccions després d'actualitzar el contracte de projecte per defecte Project Operations. |
| **Administració i comptabilitat de projectes** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | El reconeixement d'estimacions i ingressos no es pot completar quan s'ha habilitat Project Operations. |
| **Administració i comptabilitat de projectes** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | A Project Operations, si suprimiu un projecte d'un contracte, no es restableix el projecte per defecte del contracte. |
| **Administració i comptabilitat de projectes** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | A Project Operations, en una factura entre empreses, es mostren les línies de despesa errònies a la llista **Afegeix línia**. |
| **Viatge i despesa** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Les línies de despesa no es poden publicar perquè falta la configuració d'hores a la línia de contracte. |
| **Viatge i despesa** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Quan la validació del projecte/categoria és obligatòria, les categories de despesa associades al projecte no estan visibles a l'informe de despeses. |
| **Viatge i despesa** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | El balanç d'avançament en efectiu no s'actualitza quan un informe de despeses es publica per línia. |
| **Viatge i despesa** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | La feina **actualitza la informació de pagament** falla després de tornar revocar acords on s'ha acordat una factura amb dues o més transaccions de pagament. |
| **Viatge i despesa** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Hi ha un problema amb el càlcul de la reducció del menjar de l'últim dia per a la categoria de despesa per dia. |
| **Viatge i despesa** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | L'informe **tipus de despesa per empleat** no mostra les despeses detalldes si la primera connexió d'un usuari va ser en la llengua, es-MX. |
| **Viatge i despesa** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | El pagament del proveïdor d'una factura de l'informe de despeses està utilitzant el compte de resum erroni per a la publicació de l'acord. |
| **Viatge i despesa** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Quan un informe de despeses es publica amb **Permetre agrupament de transaccions segons el compte de pagament amb desplaçament** i **Corregir data comptable en publicar** activats, les dates de comptabilitat no s'agrupen a la taula **Distribució comptable**, cosa que influeix en els registres de l'impost sobre les vendes. |
| **Viatge i despesa** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | L'assignació de subcategoria de despeses s'elimina quan la casella de selecció Utilitza a la despesa està desactivada i, a continuació, es torna a seleccionar. |
| **Viatge i despesa** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | No es pot crear cap informe de despeses entre empreses si l'identificador del projecte s'afegeix al nivell de capçalera. |
| **Viatge i despesa** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Hi ha un problema amb els pagaments de despeses quan l'import de la despesa és superior a l'import de la bestreta en efectiu. |
| **Viatge i despesa** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | El camp de **l'identificador del projecte** en un informe de despeses entre empreses és buida si la funció de l'usuari s'assigna a una organització específica. |
| **Viatge i despesa** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | La categoria de despesa es bloca quan s'afegeix una línia de despesa nova. |
| **Viatge i despesa** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Detallar les línies d'informe de despesa que ja estan separades genera un val de llibre major de comptes pagables\general publicat incomplet. A causa de la duplicitat de **TRVEXPTRANS.SOURCEDOCUMENTLINE**, també es trenca l'explorador d'origen de comptabilitat. |
| **Viatge i despesa** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | L'índex afegit a la taula **TRVREQUISITIONLINE** per al qual el client té duplicats genera un error durant l'actualització. |
| **Viatge i despesa** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | A Project Operations, el temps amb tasques entre empreses al Dataverse no es pot crear ni aprovar. |

## <a name="regulatory-updates"></a>Actualitzacions reglamentàries

Per obtenir informació sobre les actualitzacions reguladores de les aplicacions financeres i d'operacions, consulta [Actualitzacions reguladores](/dynamics365/finance/localizations/regulatory-updates). També podeu iniciar sessió al LCS i veure les actualitzacions reglamentàries planificades mitjançant l'eina de cerca de problemes. La cerca de problemes us permet cercar per país, tipus de funció i llançament.


[!INCLUDE[footer-include](../includes/footer-banner.md)]