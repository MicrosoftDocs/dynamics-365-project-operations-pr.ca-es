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
ms.openlocfilehash: 670b5d15ecf1ef7dcc034064e625814cbe6d54b0
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595427"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="9b18f-103">Informació general de la facturació entre empreses</span><span class="sxs-lookup"><span data-stu-id="9b18f-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="9b18f-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="9b18f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9b18f-105">La vostra organització pot tenir diverses divisions, filials i altres entitats jurídiques que es transfereixen productes i serveis entre si per als projectes.</span><span class="sxs-lookup"><span data-stu-id="9b18f-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="9b18f-106">L'entitat jurídica que proporciona el servei o producte s'anomena *entitat jurídica prestadora*.</span><span class="sxs-lookup"><span data-stu-id="9b18f-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="9b18f-107">L'entitat jurídica que rep el servei o producte s'anomena *entitat jurídica prestatària*.</span><span class="sxs-lookup"><span data-stu-id="9b18f-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="9b18f-108">A la il·lustració següent es mostra un escenari típic on dos entitats jurídiques, Contoso Robotics USA (l'entitat jurídica prestatària) i Contoso Robotics UK (l'entitat jurídica prestadora) comparteixen recursos per dur a terme un projecte per al client, Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="9b18f-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="9b18f-109">Per a aquest escenari, Contoso Robotics USA és contractada per dur a terme el treball a Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="9b18f-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Facturació entre empreses](./media/IntercompanyScenario.png) 

<span data-ttu-id="9b18f-111">El Dynamics 365 Project Operations utilitza el flux següent per processar les transaccions entre empreses:</span><span class="sxs-lookup"><span data-stu-id="9b18f-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="9b18f-112">Els recursos del registre d'entitat jurídica prestadora registren transaccions de temps o de despesa entre empreses per reservar temps i despeses als projectes en l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="9b18f-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="9b18f-113">Els costos de temps i de despesa es registren a l'empresa prestadora per mitjà de la llista de preus de cost unitari de l'empresa prestatària.</span><span class="sxs-lookup"><span data-stu-id="9b18f-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="9b18f-114">Les transaccions de venda sense factura entre empreses es registren a l'empresa prestadora per mitjà de la llista de preus de cost unitari de l'empresa prestatària.</span><span class="sxs-lookup"><span data-stu-id="9b18f-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="9b18f-115">Els ingressos sense facturar es registren a l'empresa prestatària mitjançant la llista de preus de venda del contracte de projecte.</span><span class="sxs-lookup"><span data-stu-id="9b18f-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="9b18f-116">Es pot facturar al client quan s'ha registrat un ingrés no facturat.</span><span class="sxs-lookup"><span data-stu-id="9b18f-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="9b18f-117">El client no ha d'esperar que s'hagi completat el processament de la factura entre empreses.</span><span class="sxs-lookup"><span data-stu-id="9b18f-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="9b18f-118">Les factures de clients entre empreses es creen de manera periòdica a l'empresa prestadora.</span><span class="sxs-lookup"><span data-stu-id="9b18f-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="9b18f-119">Les factures es creen manualment o mitjançant un procés automatitzat periòdic.</span><span class="sxs-lookup"><span data-stu-id="9b18f-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="9b18f-120">Es pot crear una única factura per a cada entitat jurídica prestatària o crear factures independents per projecte.</span><span class="sxs-lookup"><span data-stu-id="9b18f-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="9b18f-121">Quan la factura de client entre empreses es comptabilitza a l'entitat jurídica prestadora, la factura corresponent del proveïdor pendent es crea a l'entitat jurídica prestatària.</span><span class="sxs-lookup"><span data-stu-id="9b18f-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="9b18f-122">Els costos de la factura de proveïdor pendent s'enregistraran al subdiari del projecte quan es comptabilitzi la factura.</span><span class="sxs-lookup"><span data-stu-id="9b18f-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="9b18f-123">El diagrama següent il·lustra la facturació entre empreses segons la seva relació amb actes comptables i comptabilitzacions esperades al llibre major.</span><span class="sxs-lookup"><span data-stu-id="9b18f-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Flux entre empreses](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="9b18f-125">Recursos addicionals</span><span class="sxs-lookup"><span data-stu-id="9b18f-125">Additional resources</span></span>

- [<span data-ttu-id="9b18f-126">Configuració de la facturació entre empreses</span><span class="sxs-lookup"><span data-stu-id="9b18f-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="9b18f-127">Registre de transaccions entre empreses</span><span class="sxs-lookup"><span data-stu-id="9b18f-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="9b18f-128">Creació de factures entre empreses de clients i proveïdors</span><span class="sxs-lookup"><span data-stu-id="9b18f-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)
