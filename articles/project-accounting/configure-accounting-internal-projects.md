---
title: Configuració de la comptabilitat per a projectes interns
description: Aquest tema proporciona informació sobre com configurar les pràctiques de comptabilitat per a projectes interns al Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072146"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="a33f0-103">Configuració de la comptabilitat per a projectes interns</span><span class="sxs-lookup"><span data-stu-id="a33f0-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="a33f0-104">_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_</span><span class="sxs-lookup"><span data-stu-id="a33f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a33f0-105">Els projectes interns permeten a les empreses fer un seguiment del cost relacionat amb activitats que no es facturen a un client.</span><span class="sxs-lookup"><span data-stu-id="a33f0-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="a33f0-106">Alguns exemples de projectes interns són:</span><span class="sxs-lookup"><span data-stu-id="a33f0-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="a33f0-107">Desenvolupar un producte, com una aplicació mòbil, i fer un seguiment del cost associat al desenvolupament.</span><span class="sxs-lookup"><span data-stu-id="a33f0-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="a33f0-108">Administrar el temps i les despeses prèvies a la venda.</span><span class="sxs-lookup"><span data-stu-id="a33f0-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="a33f0-109">Aquest projecte intern previ a la venda es pot convertir més tard en un projecte facturable si es guanya l'oferta.</span><span class="sxs-lookup"><span data-stu-id="a33f0-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="a33f0-110">Qualsevol projecte no associat amb un contracte a Dynamics 365 Project Operations es tracta com a intern.</span><span class="sxs-lookup"><span data-stu-id="a33f0-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="a33f0-111">Els perfils de cost i ingrés del projecte no s'utilitzen per determinar les regles de comptabilitat per al projecte.</span><span class="sxs-lookup"><span data-stu-id="a33f0-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="a33f0-112">El cost intern del projecte sempre es comptabilitza amb els principis de beneficis i pèrdues.</span><span class="sxs-lookup"><span data-stu-id="a33f0-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="a33f0-113">Els comptes del registre major per a les comptabilitzacions es defineixen a la pàgina **Configuració de comptabilització del registre major**.</span><span class="sxs-lookup"><span data-stu-id="a33f0-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="a33f0-114">Les transaccions de temps es comptabilitzen carregant-les al compte **Cost** i pagant-les al compte **Assignació de nòmines**.</span><span class="sxs-lookup"><span data-stu-id="a33f0-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="a33f0-115">Les transaccions de despeses es comptabilitzen carregant-les al compte **Cost** i pagant-les al compte **Compte de desplaçament per a despeses**.</span><span class="sxs-lookup"><span data-stu-id="a33f0-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="a33f0-116">Després de comptabilitzar les transaccions al projecte, si el projecte està associat amb un contracte de projecte, el sistema reverteix totes les transaccions acumulades i crea noves transaccions facturables.</span><span class="sxs-lookup"><span data-stu-id="a33f0-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="a33f0-117">Les transaccions facturables segueixen les regles de comptabilitat definides en el perfil de cost i ingressos del projecte respectiu.</span><span class="sxs-lookup"><span data-stu-id="a33f0-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>


