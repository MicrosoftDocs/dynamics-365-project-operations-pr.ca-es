---
title: Informació general del procés de facturació
description: Aquest tema proporciona una vista general del procés de facturació al Project Operations per a escenaris basats en recursos/no en existències.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275795"
---
# <a name="invoicing-process-overview"></a>Informació general del procés de facturació

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

El Project Operations per a escenaris basats en recursos/no existències ofereixen capacitats completes adaptades a les necessitats de l'administrador de projectes i de l'encarregat dels comptes a cobrar/comptable del projecte. Per al procés de facturació, l'administrador del projecte gestiona el la feina pendent de facturació del projecte i l'encarregat dels comptes a cobrar/comptable del projecte crea un document de facturació compatible i exacte amb el client.

![Diagrama d'un flux de facturació](./media/invoicing-flow.png)

La línia de contracte del projecte defineix el mètode de facturació de les transaccions de projecte associades. Quan l'administrador del projecte aprova transaccions de temps i despeses, el sistema registra les transaccions de l'entitat **Valors reals del projecte** i envia la informació al mòdul **Administració i comptabilitat del projecte** del Dynamics 365 Finance. A continuació, el comptable del projecte revisa i publica els registres mitjançant el [llibre diari d'integració del Project Operations](../project-accounting/project-operations-integration-journal.md). Aquest, a més a més, inclou detalls importants de comptabilitat per als valors reals del projecte, com ara la facturació, el grup d'impostos sobre les vendes, el grup d'impostos sobre les vendes dels articles de facturació i les mesures financeres.

L'administrador del projecte pot revisar les transaccions de vendes no facturades mitjançant el mètode de facturació de temps i materials al [Registre de feines pendents de temps i materials](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) i la facturació de preu fix a [Fites de preu fix](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Aquestes visualitzacions us permeten filtrar i seleccionar transaccions que s'han d'incloure al següent cicle de facturació i, a continuació, marcar-les com a **Preparades per a facturar-se**.

Podeu [crear manualment una factura de proforma](../proforma-invoicing/create-manual-proforma-invoice.md) o utilitzar un [procés periòdic](../proforma-invoicing/configure-automated-invoice-creation.md). L'administrador del projecte pot [ajustar una factura de proforma en forma de esborrany](../proforma-invoicing/manage-proforma-invoice.md) segons calgui i, a continuació, confirmar-la.

La factura de proforma confirmada s'envia al mòdul **Administració i comptabilitat del projecte** de Finances. El comptable del projecte formata i actualitza la proposta de factura del projecte i, a continuació, publica i imprimeix el document. Les factures de projecte publicades es registren al llibre major general, així com als subllibres de client i de projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]