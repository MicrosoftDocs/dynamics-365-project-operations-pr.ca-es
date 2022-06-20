---
title: Rebre articles en una comanda de compra d'un requisit d'article
description: En aquest article s'explica com rebre articles en una comanda de compra a partir d'un requisit d'article.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bbe15fac325ad00bdd2f2fc6ddf3ae15df45271
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929524"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Rebre articles en una comanda de compra d'un requisit d'article

[!include [banner](../../includes/banner.md)]

En aquest article s'explica com rebre articles en una comanda de compra a partir d'un requisit d'article.

Mitjançant l'ús d'un requisit d'article en comptes d'una transacció d'articles, podeu planificar l'entrega just abans d'utilitzar l'article, crear una comanda de compra, incloure l'article a l'estructura de l'acord de comerç i incloure el requisit d'article a la planificació de la producció. 

Aquesta tasca utilitza el conjunt de dades d'USSI.

1. A la subfinestra de navegació, aneu a **Mòduls > Administració de projectes i comptabilitat > Projectes > Tots els projectes**.
2. A la llista, seleccioneu l'enllaç de la fila desitjada.
3. A la subfinestra d'acció, seleccioneu **Planificació**.
4. Seleccioneu **Requisits d'article**.
5. Seleccioneu **Crea**.
6. A la fila nova, introduïu o seleccioneu un valor al camp **Número d'article**.
7. Al camp **Quantitat**, introduïu un número.
8. Seleccioneu **Desa**.
9. A la subfinestra d'acció, seleccioneu **Administra**.
10. Seleccioneu **Funcions**.
11. Seleccioneu **Crea una comanda de compra**.
12. Marqueu la casella de selecció **Inclou-ho tot**.
13. Al camp **Compte del proveïdor**, introduïu o seleccioneu un valor.
14. Seleccioneu **D'acord**.
15. A la subfinestra de navegació, aneu a **Mòduls > Compte a pagar > Comandes de compra > Totes les comandes de compra**.
16. A la llista, seleccioneu l'enllaç de la fila desitjada.
17. A la subfinestra d'acció, seleccioneu **Compra**.
18. Seleccioneu **Confirma**.
19. A la subfinestra d'acció, seleccioneu **Rep**.
20. Seleccioneu **Rebut del producte**.
21. Al camp **Rebut de producte**, escriviu un valor.
22. Seleccioneu **D'acord**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]