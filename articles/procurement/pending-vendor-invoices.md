---
title: Comrpa de materials sense existències mitjançant una factura pendent del proveïdor
description: En aquest tema s'explica com es registren les factures pendents del proveïdor.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880622"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="9e48c-103">Comrpa de materials sense existències mitjançant una factura pendent del proveïdor</span><span class="sxs-lookup"><span data-stu-id="9e48c-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="9e48c-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="9e48c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9e48c-105">Com que una empresa processa materials sense existències per a un projecte, els costos es poden registrar immediatament en el projecte.</span><span class="sxs-lookup"><span data-stu-id="9e48c-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="9e48c-106">Per exemple, s'està realitzant un projecte de renovació d'equipament a Contoso Robotics US i necessiten llicències de programari.</span><span class="sxs-lookup"><span data-stu-id="9e48c-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="9e48c-107">Aquestes llicències provenen d'un proveïdor de tercers.</span><span class="sxs-lookup"><span data-stu-id="9e48c-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="9e48c-108">Mitjançant el Dynamics 365 Finance, l'encarregat del compte a pagar registra un document de factura pendent del proveïdor i atribueix els costos de llicència directament al projecte de renovació d'equipament.</span><span class="sxs-lookup"><span data-stu-id="9e48c-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="9e48c-109">Abans d'utilitzar la funcionalitat descrita en aquest tema, reviseu i apliqueu les configuracions necessàries.</span><span class="sxs-lookup"><span data-stu-id="9e48c-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="9e48c-110">Per obtenir més informació, vegeu [Habilitar materials sense existències i factures pendents del proveïdor](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="9e48c-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="9e48c-111">Publicar una factura pendent del proveïdor relacionada amb el projecte</span><span class="sxs-lookup"><span data-stu-id="9e48c-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="9e48c-112">Les factures pendents del proveïdor es poden registrar a la pàgina **Factures pendents del proveïdor** (**Compte a pagar** > **Factures** > **Factures pendents del proveïdor**).</span><span class="sxs-lookup"><span data-stu-id="9e48c-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="9e48c-113">Seguiu els passos següents per publicar una factura pendent del proveïdor relacionada amb el projecte:</span><span class="sxs-lookup"><span data-stu-id="9e48c-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="9e48c-114">Aneu a **Compte a pagar** > **Factures** i seleccioneu **Crea**.</span><span class="sxs-lookup"><span data-stu-id="9e48c-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="9e48c-115">Al camp **Compte de factura**, seleccioneu un proveïdor i, al camp **Número**, introduïu l'identificador de factura del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="9e48c-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="9e48c-116">Afegiu una línia a la factura del proveïdor i, al camp **Número d'element**, seleccioneu l'article sense existències adquirit del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="9e48c-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9e48c-117">Les línies de factura del proveïdor basades en una categoria de proveïment no es poden registrar en el projecte.</span><span class="sxs-lookup"><span data-stu-id="9e48c-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="9e48c-118">Afegiu la quantitat comprada.</span><span class="sxs-lookup"><span data-stu-id="9e48c-118">Add the quantity purchased.</span></span> <span data-ttu-id="9e48c-119">El sistema emplenarà el preu per unitat segons la configuració del preu de l'article sense existències.</span><span class="sxs-lookup"><span data-stu-id="9e48c-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="9e48c-120">Verifiqueu l'import total i altres detalls necessaris a la línia.</span><span class="sxs-lookup"><span data-stu-id="9e48c-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="9e48c-121">Als detalls de línia, a la pestanya **Projecte**, seleccioneu l'identificador del projecte al qual es registrarà aquest element.</span><span class="sxs-lookup"><span data-stu-id="9e48c-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="9e48c-122">O bé seleccioneu el número d'activitat i actualitzeu la categoria del projecte i la propietat de la línia.</span><span class="sxs-lookup"><span data-stu-id="9e48c-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="9e48c-123">Publiqueu la factura pendent del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="9e48c-123">Post pending vendor invoice.</span></span> <span data-ttu-id="9e48c-124">Quan la factura es publica,el sistema registra:</span><span class="sxs-lookup"><span data-stu-id="9e48c-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="9e48c-125">Import del balanç del proveïdor.</span><span class="sxs-lookup"><span data-stu-id="9e48c-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="9e48c-126">Import de l’impost sobre les vendes.</span><span class="sxs-lookup"><span data-stu-id="9e48c-126">The sales tax amount.</span></span>
    - <span data-ttu-id="9e48c-127">El cost en relació amb el projecte es registra al compte d'integració del proveïment.</span><span class="sxs-lookup"><span data-stu-id="9e48c-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="9e48c-128">La transacció real del projecte al Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9e48c-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="9e48c-129">Aquesta transacció es processa addicionalment per mitjà del [Llibre diari d'integració del Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="9e48c-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="9e48c-130">El fet de publicar aquest llibre diari desplaça l'import del compte d'integració de proveïment al compte de cost del projecte.</span><span class="sxs-lookup"><span data-stu-id="9e48c-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
