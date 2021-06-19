---
title: Treballar amb despeses personals en un informe de despeses
description: Aquest tema proporciona informació sobre com treballar amb les despeses personals ocasionades pels empleats mentre viatgen amb finalitats empresarials.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025672"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="ca159-103">Treballar amb despeses personals en un informe de despeses</span><span class="sxs-lookup"><span data-stu-id="ca159-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="ca159-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="ca159-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca159-105">Durant els desplaçaments empresarials, un empleat pot pagar les despeses personals amb la seva targeta de crèdit empresarial.</span><span class="sxs-lookup"><span data-stu-id="ca159-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="ca159-106">Si un procés no s'ha definit per gestionar les despeses personals, pot ser que el procés d'aprovació d'informes de despeses s'interrompi quan un empleat enviï l'informe de despeses detallat.</span><span class="sxs-lookup"><span data-stu-id="ca159-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="ca159-107">Hi ha dos mètodes que podeu utilitzar per treballar amb les despeses personals d'un empleat:</span><span class="sxs-lookup"><span data-stu-id="ca159-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="ca159-108">**Pagat per l'empleat**: la vostra organització no paga les despeses personals que apareixen a la factura de la targeta de crèdit corporativa.</span><span class="sxs-lookup"><span data-stu-id="ca159-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="ca159-109">En lloc d'això, l'empleat paga el proveïdor de targetes de crèdit directament per les despeses.</span><span class="sxs-lookup"><span data-stu-id="ca159-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="ca159-110">**Pagat per l'empresa:** la vostra organització paga la factura completa de la targeta de crèdit empresarial i, a continuació, carrega la quantitat de les despeses personals en el compte del treballador.</span><span class="sxs-lookup"><span data-stu-id="ca159-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="ca159-111">Podeu seleccionar el mètode que utilitza la vostra organització a la pàgina **Paràmetres de l'administració de despeses**.</span><span class="sxs-lookup"><span data-stu-id="ca159-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="ca159-112">Habilitar la funció de despesa dividida quan el camp d'import personal té un valor definit</span><span class="sxs-lookup"><span data-stu-id="ca159-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="ca159-113">La característica **Habilita la funció de despesa dividida quan el camp d'import personal té un valor definit** només s'aplica als informes de despesa aprovats amb un flux de treball de nivell de línia.</span><span class="sxs-lookup"><span data-stu-id="ca159-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="ca159-114">Els informes s'aproven anant a **Processa els informes de despesa** > **Informes de despesa que tinc assignats** > **Obre l'informe de despesa**.</span><span class="sxs-lookup"><span data-stu-id="ca159-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="ca159-115">Per habilitar aquesta característica, aneu a **Àrees de treball** > **Administració de característiques**, seleccioneu **Habilita la funció de despesa dividida quan el camp d'import personal té un valor definit** i, a continuació, seleccioneu **Habilita ara**.</span><span class="sxs-lookup"><span data-stu-id="ca159-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="ca159-116">Quan la característica està habilitada, les línies de despesa que utilitzen aquesta funcionalitat generen dues línies en enviar l'informe.</span><span class="sxs-lookup"><span data-stu-id="ca159-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="ca159-117">Es generen dues línies per tal que l'aprovador pugui aprovar cada línia per separat.</span><span class="sxs-lookup"><span data-stu-id="ca159-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
