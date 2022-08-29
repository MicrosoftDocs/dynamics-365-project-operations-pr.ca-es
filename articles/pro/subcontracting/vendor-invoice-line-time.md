---
title: Línies de factura del proveïdor per al temps
description: En aquest article s'explica com registrar les línies de factures dels proveïdors pels costos de temps que posen els subcontractistes.
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

Una factura de proveïdor a Microsoft Dynamics 365 Project Operations pot tenir línies de factures de proveïdor durant un temps. Els gestors de projectes poden utilitzar línies de factures de proveïdors durant temps per registrar els costos del temps del subcontractista en els projectes.

Les línies de factures dels proveïdors durant el temps poden fer referència o no a una línia de subcontractació durant el temps. Si una línia de factura de proveïdor per temps fa referència a un subcontractista, els gestors de projectes podran igualar i verificar el temps que està sent facturat per la línia de factura del venedor contra el temps que és registrat pels subcontractistes i aprovat pels gestors del projecte en el projecte.

La taula següent proporciona informació sobre els camps de les línies de factures de proveïdors durant el temps.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | El nom de la línia de factura del venedor, per ajudar a la identificació. | Aquest nom es mostrarà com a primera columna de totes les cerques basades en línies de factures de proveïdor. |
| Descripció | Una breu descripció dels serveis que està facturant el venedor a la línia de factura del proveïdor. | cap |
| Subcontracte | La subcontractació en què es van encarregar originalment els serveis. | Quan se selecciona un subcontractista per a la factura del venedor, totes les línies de la factura del venedor heretaran aquesta selecció. Una factura de proveïdor no pot tenir línies de factures de proveïdors que facin referència a diferents subcontractes. |
| Línia de subcontractació | La línia de subcontractació en la qual es van encarregar els serveis. La llista de línies de subcontractació que es poden seleccionar es limita a les línies de la subcontractació seleccionada. | Quan se selecciona una línia de subcontractació en una línia de factures de proveïdor durant el temps, els valors predeterminats per als **camps Projecte**, **Funció** i **recurs** reservable s'introdueixen des dels camps corresponents de la línia de subcontractació. Si la línia de subcontractació seleccionada té valors als **camps Projecte**, **Funció** i **Reserves**, els valors dels camps corresponents de la línia de factures del proveïdor no poden diferir d'aquests valors. |
| Data de la transacció | La data en què es registrarà al projecte el cost real de la línia de factura del proveïdor. | cap |
| Classe de la transacció | El valor per defecte és **Temps**. | El valor **Time** indica que la línia de factura del venedor s'està utilitzant per registrar l'import de la factura del temps del subcontractista. |
| Project | El nom del projecte en què es van utilitzar els serveis que s'estan facturant. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | El nom de la tasca del projecte en què es van utilitzar els serveis que s'estan facturant. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, el gestor del projecte pot fer coincidir la línia de factura del proveïdor amb el temps que registren els recursos del subcontractista en qualsevol tasca del projecte. Si la línia de factures del proveïdor no fa referència a una línia de subcontractació i aquest camp es deixa en blanc, el cost real creat per la línia de factures del proveïdor no estarà vinculat a cap real de vendes no codificat. En aquest cas, si es configura la facturació basada en tasques, és possible que els costos no es puguin facturar al client final. |
| Funció | El paper dels recursos subcontractats el temps dels quals s'està facturant. | En aquest camp s'especifica el paper que realitzen els recursos subcontractats el temps dels quals es factura a la factura del proveïdor. |
| Recurs que es pot reservar | El nom del subcontractista el temps del qual s'està facturant. La selecció d'un recurs que es pot reservar és opcional. | Si aquest camp es deixa en blanc, el gestor de projectes pot fer coincidir la línia de factura del proveïdor amb el temps que registra qualsevol recurs que pertanyi al proveïdor a la línia de factures del proveïdor. |
| Quantitat | Introduïu el nombre d'hores de temps que el venedor facturarà a la línia de factura. |cap |
| Grup d'unitats | El valor per defecte és **Grup d'unitats** de temps i no es pot canviar. | cap |
| Unit | El valor per defecte és la unitat base d'hores del grup d'unitats de temps. Podeu canviar aquest valor per comprar en qualsevol unitat del grup d'unitats de temps, com ara el dia o la setmana. | La combinació de valors Rol i Unitat s'utilitzarà **com a valor per defecte o calculat per al camp Preu** unitari de la **línia de factura del proveïdor.** **·** |
| Preu unitari | El preu unitari per defecte utilitza la combinació de valors Rol **i** **Unitat** de la llista de preus del projecte que s'aplica a la data de transacció de la línia de factura de proveïdor. | Si el preu de la llista de preus del projecte aplicable està configurat en una unitat diferent de la unitat de la línia de factura de proveïdor, el sistema utilitza la conversió unitària per calcular el preu per unitat. |
| Subtotal | Aquest camp només de lectura es calcula com a *Quantitat*&times;*Preu* unitari, si s'introdueixen valors tant al camp Quantitat **com** al **camp Preu** unitari. Si un o tots dos camps estan en blanc, podeu introduir un valor en aquest camp. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | L'import total de la línia de factures del proveïdor, inclosos els impostos. Aquest camp es calcula com a *impost sobre les vendes subtotals* + *·*. | cap |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
