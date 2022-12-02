---
title: Línies de factura del proveïdor per al temps
description: En aquest article s'explica com es registren les línies de factura de proveïdor per als costos de temps que els subcontractistes afegeixen.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262000"
---
# <a name="vendor-invoice-lines-for-time"></a>Línies de factura del proveïdor per al temps

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura de proveïdor del Microsoft Dynamics 365 Project Operations pot tenir línies de factura de proveïdor per al temps. Els administradors de projecte poden utilitzar les línies de factura de proveïdor per al temps per registrar els costos del temps de subcontractista en els projectes.

Les línies de factura de proveïdor per al temps podrien o no fer referència a una línia de subcontracte per al temps. Si una línia de factura de proveïdor per al temps fa referència a un subcontracte, els administradors de projecte podran fer coincidir i verificar el temps que s'està facturant amb la línia de factura de proveïdor amb el temps que registren els subcontractistes i que aproven els administradors del projecte al projecte.

La taula següent proporciona informació sobre els camps de les línies de factura de proveïdor per al temps.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | Nom de la línia de factura de proveïdor per ajudar a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les consultes basades en les línies de factura de proveïdor. |
| Descripció | Descripció breu dels serveis que factura el proveïdor a la línia de factura de proveïdor. | cap |
| Subcontracte | El subcontracte en què es van demanar els serveis originalment. | Quan se selecciona un subcontracte per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura del proveïdor no pot tenir línies de factura del proveïdor que facin referència a diferents subcontractes. |
| Línia de subcontracte | La línia de subcontracte en què es van demanar els serveis. La llista de línies de subcontracte que es poden seleccionar està limitada a les línies del subcontracte seleccionat. | Quan se selecciona una línia de subcontracte en una línia de factura de proveïdor per al temps, els valors per defecte dels camps **Projecte**, **Funció** i **Recurs que es pot reservar** s'introdueixen des dels camps corresponents de la línia de subcontracte. Si la línia de subcontracte seleccionada té valors als camps **Projecte**, **Funció** i **Es pot reservar**, els valors dels camps corresponents de la línia de factura de proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què el valor real de cost de la línia de factura del proveïdor es registrarà al projecte. | cap |
| Classe de la transacció | El valor per defecte és **Temps**. | El valor **Temps** indica que la línia de factura de proveïdor s'utilitza per registrar la quantitat de temps de subcontractista de la factura. |
| Project | Nom del projecte on s'han utilitzat els serveis que es facturen. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | Nom de la tasca del projecte on s'han utilitzat els serveis que es facturen. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, l'administrador del projecte pot aparellar la línia de factura de proveïdor amb el temps que registren els recursos del subcontractista en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontracte i aquest camp es deixa en blanc, el valor real de cost que crea la línia de factura del proveïdor no s'enllaçarà amb cap valor real de vendes no facturades. En aquest cas, si es configura la facturació basada en tasques, pot ser que els costos no es puguin facturar al client final. |
| Funció | Funció dels recursos de subcontracte el temps del qual s'està facturant. | Aquest camp especifica la funció que fan els recursos de subcontracte el temps del qual es factura a la factura del proveïdor. |
| Recurs que es pot reservar | Nom del subcontractista el temps del qual s'està facturant. La selecció d'un recurs que es pot reservar és opcional. | Si aquest camp es deixa en blanc, l'administrador del projecte pot aparellar la línia de factura de proveïdor amb el temps que registra qualsevol recurs que pertany al proveïdor a la línia de factura de proveïdor. |
| Quantitat | Introduïu el nombre d'hores de temps que factura el proveïdor a la línia de factura. |cap |
| Grup d'unitats | El valor per defecte és **Grup d'unitats de temps** i no es pot canviar. | cap |
| Unit | El valor per defecte és la unitat base d'hores del grup d'unitats de temps. Podeu canviar aquest valor per comprant qualsevol unitat del grup d'unitats de temps, com ara dia o setmana. | La combinació dels valors **Funció** i **Unitat** s'utilitzarà com a valor per defecte o valor calculat per al camp **Preu unitari** de la línia de factura de proveïdor. |
| Preu unitari | El preu unitari per defecte utilitza la combinació dels valors **Funció** i **Unitat** de la llista de preus del projecte aplicable a la data de la transacció de la línia de factura de proveïdor. | Si el preu de la llista de preus aplicable del projecte està configurat en una unitat diferent de la unitat de la línia de factura de proveïdor, el sistema utilitza la conversió d'unitats per calcular el preu unitari. |
| Subtotal | És un camp només de lectura que es calcula com *Quantitat* &times; *Preu unitari* si s'introdueixen valors tant en el camp **Quantitat** com en el camp **Preu unitari**. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | Quantitat total de la línia de factura de proveïdor amb els impostos. Aquest camp es calcula com *Subtotal* + *Impost sobre les vendes*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
