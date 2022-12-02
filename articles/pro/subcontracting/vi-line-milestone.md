---
title: Línies de factura del proveïdor per a fites
description: En aquest article s'explica com crear línies de factura del proveïdor per a les fites d'un subcontracte.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/11/2022
ms.locfileid: "9260983"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Línies de factura del proveïdor per a fites

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura del proveïdor del Microsoft Dynamics 365 Project Operations pot tenir línies de factura del proveïdor per a les fites que es defineixen en una línia de subcontracte. Els administradors de projecte poden utilitzar les línies de factura del proveïdor per a les fites per registrar els costos dels serveis que s'obtenen com a costos basats en fites en què s'incorre amb els serveis o productes proveïts per al projecte.

Les línies de factura del proveïdor per a les fites sempre han de fer referència a una línia de subcontracte que tingui un mètode de facturació de preu fix. Si una línia de factura de proveïdor per a fites fa referència a una línia de subcontracte, els administradors de projecte podran fer coincidir i verificar els costos subjacents de temps, despeses o materials que facin referència a aquesta línia de subcontracte amb la fita que està facturant el proveïdor.

La taula següent proporciona informació sobre els camps de les línies de factura de proveïdor per a fites.

| Camp | Descripció | Impacte funcional |
| --- | --- | --- |
| Nom | Nom de la línia de factura de proveïdor per ajudar a identificar-la. | Aquest nom es mostrarà com la primera columna de totes les consultes basades en les línies de factura de proveïdor. |
| Descripció | Descripció breu dels serveis que factura el proveïdor a la línia de factura de proveïdor. | cap |
| Subcontracte | El subcontracte en què es van demanar els serveis originalment. | Quan se selecciona un subcontracte per a la factura del proveïdor, totes les línies de la factura del proveïdor heretaran aquesta selecció. Una factura del proveïdor no pot tenir línies de factura del proveïdor que facin referència a diferents subcontractes. |
| Línia de subcontracte | La línia de subcontracte en què es van demanar els serveis. La llista de línies de subcontracte que es poden seleccionar està limitada a les línies del subcontracte seleccionat. | Quan se selecciona una línia de subcontracte en una línia de factura del proveïdor per a les fites, els camps **Funció** i **Categoria de transacció** i els camps relacionats amb els productes són irrellevants i no estan disponibles. Els camps **Quantitat**, **Unitat** i **Grup d'unitats** tampoc són rellevants per a les línies de factura del proveïdor basades en fites. |
| Data de la transacció | La data en què el valor real de cost de la línia de factura del proveïdor es registrarà al projecte. | cap |
| Classe de la transacció | Seleccioneu **Fita** per registrar una factura del proveïdor per a una fita completada que s'ha definit en una línia de subcontracte. | cap |
| Fita | Seleccioneu la fita definida a la línia de subcontracte relacionada que està marcada com a **Preparada per facturar**. | Les fites de línia de subcontracte que tenen l'estat **Preparada per facturar** es poden seleccionar a la línia de factura del proveïdor. |
| Project | Nom del projecte on s'han utilitzat els serveis que es facturen. | Aquest camp és obligatori i no es pot deixar en blanc. |
| Tasca | Nom de la tasca del projecte on s'han utilitzat els serveis que es facturen. Aquest camp només està disponible si se selecciona un projecte. La selecció d'una tasca de projecte és opcional. | Si aquest camp es deixa en blanc, l'administrador del projecte pot aparellar la línia de factura de proveïdor amb la classe de transaccions de la línia de subcontracte relacionada que està registrada en qualsevol tasca del projecte. Si la línia de factura del proveïdor no fa referència a una línia de subcontracte i aquest camp es deixa en blanc, el valor real de cost que crea la línia de factura del proveïdor no s'enllaçarà amb cap valor real de vendes no facturades. En aquest cas, si es configura la facturació basada en tasques, pot ser que els costos no es puguin facturar al client final. |
| Import de la fita | Introduïu el valor de la fita definida a la línia de subcontracte que està preparada per facturar. | cap |
| Impost sobre les vendes | Especifiqueu l'import de l'impost sobre les vendes. | cap |
| Import total | Quantitat total de la línia de factura de proveïdor amb els impostos. Aquest camp es calcula com *Import de la fita* + *Impost de vendes*. | cap |

> [!NOTE]
> Quan es crea una línia de factura del proveïdor que fa referència a una fita de la línia de subcontracte, l'estat de la fita de subcontracte s'actualitza a **Factura del proveïdor creada**. Després, quan es confirma la factura del proveïdor, l'estat de la fita de la línia de subcontracte s'actualitza a **Factura del proveïdor confirmada**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
