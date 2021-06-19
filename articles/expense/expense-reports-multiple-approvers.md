---
title: Informes de despeses i diversos aprovadors
description: En aquest tema es proporciona informació sobre els informes de despeses que requereixen l'aprovació de més d'una persona.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2502b2975ad3aebad720970e693ea68eac0a302c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002044"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="2c1de-103">Informes de despeses i diversos aprovadors</span><span class="sxs-lookup"><span data-stu-id="2c1de-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="2c1de-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_</span><span class="sxs-lookup"><span data-stu-id="2c1de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2c1de-105">En funció de les normes d'aprovació de despeses de l'organització, pot ser que més d'una persona hagi d'aprovar un informe de despeses enviat.</span><span class="sxs-lookup"><span data-stu-id="2c1de-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="2c1de-106">En configurar el procés de flux de treball per a l'aprovació de l'informe de despeses, podeu afegir elements de flux de treball que incloguin tasques o passos per a un o diversos aprovadors de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2c1de-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="2c1de-107">Per exemple, és possible que necessiteu que tots els informes de despeses els aprovin dues persones independents, el cap del treballador que ha enviat l'informe i el coordinador de compte a pagar.</span><span class="sxs-lookup"><span data-stu-id="2c1de-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="2c1de-108">Si decidiu que voleu que calguin diversos aprovadors d'informes de despeses, podeu afegir els elements del flux de treball d'una de les maneres següents:</span><span class="sxs-lookup"><span data-stu-id="2c1de-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="2c1de-109">Afegiu un element d'aprovació que tingui un pas.</span><span class="sxs-lookup"><span data-stu-id="2c1de-109">Add one approval element that has one step.</span></span> <span data-ttu-id="2c1de-110">Per exemple, pot ser que el pas requereixi que s'assigni un informe de despeses a un grup d'usuaris i que l'aprovin un 50 per cent dels membres del grup d'usuaris.</span><span class="sxs-lookup"><span data-stu-id="2c1de-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="2c1de-111">Afegiu un element d'aprovació que tingui diversos passos.</span><span class="sxs-lookup"><span data-stu-id="2c1de-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="2c1de-112">Per exemple, pot ser que l'element d'aprovació tingui els passos següents:</span><span class="sxs-lookup"><span data-stu-id="2c1de-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="2c1de-113">El cap de l'empleat que ha enviat l'informe de despeses l'aprova.</span><span class="sxs-lookup"><span data-stu-id="2c1de-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="2c1de-114">L'empleat de compte a pagar verifica els rebuts i els elements de l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2c1de-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="2c1de-115">El propietari del pressupost aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2c1de-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="2c1de-116">Afegiu diversos elements d'aprovació, cadascun dels quals tingui un pas.</span><span class="sxs-lookup"><span data-stu-id="2c1de-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="2c1de-117">Per exemple, pot ser que afegiu un element d'aprovació independent per a cadascun dels passos següents:</span><span class="sxs-lookup"><span data-stu-id="2c1de-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="2c1de-118">El cap de l'empleat aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2c1de-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="2c1de-119">El propietari del pressupost aprova l'informe de despeses.</span><span class="sxs-lookup"><span data-stu-id="2c1de-119">The budget owner approves the expense report.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]