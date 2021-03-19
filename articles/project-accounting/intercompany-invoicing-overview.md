---
title: Informació general de la facturació entre empreses
description: En aquest tema es proporciona informació i exemples sobre la facturació entre empreses per a projectes.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287316"
---
# <a name="intercompany-invoicing-overview"></a>Informació general de la facturació entre empreses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

La vostra organització pot tenir diverses divisions, filials i altres entitats jurídiques que es transfereixen productes i serveis entre si per als projectes. L'entitat jurídica que proporciona el servei o producte s'anomena *entitat jurídica prestadora*. L'entitat jurídica que rep el servei o producte s'anomena *entitat jurídica prestatària*.

A la il·lustració següent es mostra un escenari típic on dos entitats jurídiques, Contoso Robotics USA (l'entitat jurídica prestatària) i Contoso Robotics UK (l'entitat jurídica prestadora) comparteixen recursos per dur a terme un projecte per al client, Adventure Works. Per a aquest escenari, Contoso Robotics USA és contractada per dur a terme el treball a Adventure Works.

![Facturació entre empreses](./media/IntercompanyScenario.png) 

El Dynamics 365 Project Operations utilitza el flux següent per processar les transaccions entre empreses:

1. Els recursos del registre d'entitat jurídica prestadora registren transaccions de temps o de despesa entre empreses per reservar temps i despeses als projectes en l'entitat jurídica prestatària.
2. Els costos de temps i de despesa es registren a l'empresa prestadora per mitjà de la llista de preus de cost unitari de l'empresa prestatària.
3. Les transaccions de venda sense factura entre empreses es registren a l'empresa prestadora per mitjà de la llista de preus de cost unitari de l'empresa prestatària.
4. Els ingressos sense facturar es registren a l'empresa prestatària mitjançant la llista de preus de venda del contracte de projecte. Es pot facturar al client quan s'ha registrat un ingrés no facturat. El client no ha d'esperar que s'hagi completat el processament de la factura entre empreses.
5. Les factures de clients entre empreses es creen de manera periòdica a l'empresa prestadora. Les factures es creen manualment o mitjançant un procés automatitzat periòdic. Es pot crear una única factura per a cada entitat jurídica prestatària o crear factures independents per projecte.
6. Quan la factura de client entre empreses es comptabilitza a l'entitat jurídica prestadora, la factura corresponent del proveïdor pendent es crea a l'entitat jurídica prestatària. Els costos de la factura de proveïdor pendent s'enregistraran al subdiari del projecte quan es comptabilitzi la factura.

El diagrama següent il·lustra la facturació entre empreses segons la seva relació amb actes comptables i comptabilitzacions esperades al llibre major.

![Flux entre empreses](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Recursos addicionals

- [Configuració de la facturació entre empreses](configure-intercompany-invoicing.md)
- [Registre de transaccions entre empreses](create-intercompany-transactions.md)
- [Creació de factures entre empreses de clients i proveïdors](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]