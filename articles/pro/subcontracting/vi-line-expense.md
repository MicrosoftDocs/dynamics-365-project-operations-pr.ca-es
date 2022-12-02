---
title: Línies de factura del proveïdor per a categories de despeses
description: En aquest article s'explica com es registren les línies de factura del proveïdor per a les categories de despeses.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261663"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Línies de factura del proveïdor per a categories de despeses

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor del Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdor per a categories de despesa. Els administradors de projecte poden utilitzar les línies de factura del proveïdor per a categories de despesa per registrar els costos dels serveis que es proveeixen com a categories de despesa.

Les línies de factura de proveïdor de categories de despesa podrien o no fer referència a una línia de subcontracte per a categories de despesa. Si una línia de factura de proveïdor per a categories de despesa fa referència a un subcontracte, els administradors de projecte podran fer coincidir i verificar les despeses que s'estan facturant amb la línia de factura de proveïdor amb les despeses que es registren en aquestes categories de despesa i que aproven els administradors del projecte al projecte.

La taula següent proporciona informació sobre els camps de les línies de factura de proveïdor per a categories de despesa.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | Nom de la línia de factura de proveïdor per ajudar a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les consultes basades en les línies de factura de proveïdor. |
| Descripció | Descripció breu dels serveis que factura el proveïdor a la línia de factura de proveïdor. | cap |
| Subcontracte | El subcontracte en què es van demanar els serveis originalment. | Quan se selecciona un subcontracte per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura del proveïdor no pot tenir línies de factura del proveïdor que facin referència a diferents subcontractes. |
| Línia de subcontracte | La línia de subcontracte en què es van demanar els serveis. La llista de línies de subcontracte que es poden seleccionar està limitada a les línies del subcontracte seleccionat. | Quan se selecciona una línia de subcontracte en una línia de factura de proveïdor per a categories de despesa, els valors per defecte dels camps **Projecte**, **Tasca** i **Categoria de transacció** s'introdueixen des dels camps corresponents de la línia de subcontracte. Si la línia de subcontracte seleccionada té valors als camps **Projecte**, **Tasca del projecte** i **Categoria de transacció**, els valors dels camps corresponents de la línia de factura de proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què el valor real de cost de la línia de factura del proveïdor es registrarà al projecte. |cap |
| Classe de la transacció | Seleccioneu **Despesa** per registrar una factura de proveïdor per a una categoria de despesa. | El valor de **Despesa** indica que la línia de factura del proveïdor s'utilitza per registrar l'import de la factura dels serveis que s'han proveït com a categories de despesa. |
| Project | Nom del projecte on s'han utilitzat els serveis que es facturen. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | Nom de la tasca del projecte on s'han utilitzat els serveis que es facturen. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, l'administrador del projecte pot aparellar la línia de factura de proveïdor amb les despeses que es registren en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontracte i aquest camp es deixa en blanc, el valor real de cost que crea la línia de factura del proveïdor no s'enllaçarà amb cap valor real de vendes no facturades. En aquest cas, si es configura la facturació basada en tasques, pot ser que els costos no es puguin facturar al client final. |
| Categoria de la transacció | Categoria de transacció que s'està facturant. S'ha de crear una categoria de despesa corresponent per a la categoria de transacció seleccionada. | La combinació dels valors **Categoria de transacció** i **Unitat** s'utilitzarà com a valor per defecte o valor calculat per al camp **Preu unitari** de la línia de factura de proveïdor. |
| Quantitat | Introduïu la quantitat que factura el proveïdor a la línia de factura. |cap|
| Grup d'unitats | S'introdueix un valor per defecte a partir del grup d'unitats de la categoria de transacció seleccionada. | cap |
| Unit | El valor per defecte és la unitat base del grup d'unitats seleccionat. Podeu canviar aquest valor per comprar qualsevol unitat del grup d'unitats. | La combinació dels valors **Categoria de transacció** i **Unitat** s'utilitzarà com a valor per defecte o valor calculat per al camp **Preu unitari** de la línia de factura de proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació dels valors **Categoria de transacció** i **Unitat** de la llista de preus del projecte aplicable a la data de la transacció de la línia de factura de proveïdor. | Si el preu de la llista de preus aplicable del projecte està configurat en una unitat diferent de la unitat de la línia de factura de proveïdor, el sistema utilitza la conversió d'unitats per calcular el preu unitari. |
| Subtotal | És un camp només de lectura que es calcula com *Quantitat* &times; *Preu unitari* si s'introdueixen valors tant en el camp **Quantitat** com en el camp **Preu unitari**. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp.| cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | Quantitat total de la línia de factura de proveïdor amb els impostos. Aquest camp es calcula com *Subtotal* + *Impost sobre les vendes*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
