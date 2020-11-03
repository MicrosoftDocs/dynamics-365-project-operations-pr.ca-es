---
title: Diversos aprovadors en un informe de despeses
description: Aquest tema proporciona informació sobre els informes de despeses que requereixen l'aprovació de diverses persones.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072368"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="2f0b1-103">Diversos aprovadors en un informe de despeses</span><span class="sxs-lookup"><span data-stu-id="2f0b1-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f0b1-104">Segons les normes d'aprovació de despeses de la vostra organització, més d'una persona podria haver d'aprovar un informe de despeses que presenta un empleat.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="2f0b1-105">En configurar el procés de flux de treball per a l'aprovació de l'informe de despeses, podeu afegir elements de flux de treball que incloguin tasques o passos per a un o diversos aprovadors de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="2f0b1-106">Per exemple, és possible que necessiteu que tots els informes de despeses els aprovin primer el cap del treballador que ha enviat l'informe i després el coordinador de compte a pagar.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="2f0b1-107">Si decidiu que voleu que calguin diversos aprovadors d'informes de despeses, podeu afegir els elements del flux de treball d'una de les maneres següents:</span><span class="sxs-lookup"><span data-stu-id="2f0b1-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="2f0b1-108">Afegiu un element d'aprovació que tingui un pas.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-108">Add one approval element that has one step.</span></span> <span data-ttu-id="2f0b1-109">Per exemple, pot ser que el pas requereixi que s'assigni un informe de despeses a un grup d'usuaris i que l'aprovin un 50 per cent dels membres del grup d'usuaris.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="2f0b1-110">Afegiu un element d'aprovació que tingui diversos passos.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="2f0b1-111">Per exemple, pot ser que l'element d'aprovació tingui els passos següents:</span><span class="sxs-lookup"><span data-stu-id="2f0b1-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="2f0b1-112">El cap de l'empleat que ha enviat l'informe de despeses l'aprova.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="2f0b1-113">L'empleat de compte a pagar verifica els rebuts i els elements de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="2f0b1-114">El propietari del pressupost aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="2f0b1-115">Afegiu diversos elements d'aprovació, cadascun dels quals tingui un pas.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="2f0b1-116">Per exemple, pot ser que afegiu un element d'aprovació independent per a cadascun dels passos següents:</span><span class="sxs-lookup"><span data-stu-id="2f0b1-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="2f0b1-117">El cap de l'empleat aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="2f0b1-118">El propietari del pressupost aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2f0b1-118">The budget owner approves the expense report.</span></span>
