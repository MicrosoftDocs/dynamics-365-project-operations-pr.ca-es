---
title: Projectes d'estimació d'ingressos de preu fix
description: En aquest tema es proporciona informació sobre els ingressos de preu fix en projectes.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531366"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projectes d'estimació d'ingressos de preu fix 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan creeu una línia de contracte de projecte amb els atributs següents al Dynamics 365 Project Operations al Microsoft Dataverse, el sistema crea automàticament un projecte d'estimació d'ingressos de preu fix. La informació d'aquest projecte es basa en el següent:

  - Un mètode de facturació de preu fix.
  - Un projecte associat.
  - Com a mínim una fita definida a la pestanya **Planificació de la factura** de la pàgina **Línia de contracte del projecte**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisió de projectes d'estimació d'ingressos de preu fix
Per revisar els projectes d'estimació d'ingressos de preu fix, seguiu aquests passos:

1. A l'entorn del Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilitat** > **Projectes** > **Projectes d'estimació d'ingressos de preu fix**.
2. Seleccioneu el projecte que voleu visualitzar i feu doble clic a **Identificador del projecte d'estimació** per obrir el registre i revisar els detalls del projecte.
3. Expandiu la pestanya **Projecte**. Veureu un projecte a la quadrícula **Projectes seleccionats**. El sistema l'utilitza com a projecte per defecte perquè és el projecte associat a la línia de contracte del projecte. 
4. Per canviar l'associació, seleccioneu projectes addicionals i afegiu-los a la quadrícula **Projectes seleccionats**. Si se seleccionen diversos projectes en aquesta quadrícula, el percentatge completat del projecte i les estimacions d'ingressos es calculen junts per a tots els projectes seleccionats.

  El cost del projecte, el perfil d'ingressos, la plantilla de costos i el codi del període es poden definir manualment. Si no es defineixen manualment, els valors per defecte durant el càlcul de la primera estimació del projecte fan servir les regles configurades per als perfils de costos i ingressos del projecte.
