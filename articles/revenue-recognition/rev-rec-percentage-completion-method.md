---
title: Projectes d'estimació d'ingressos de preu fix
description: En aquest article s'ofereix informació sobre els ingressos de preus fixos en projectes.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3febb22397faa31222015231481d43fb0449d0a2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928374"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projectes d'estimació d'ingressos de preu fix 

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Quan creeu una línia de contracte de projecte amb els atributs següents al Dynamics 365 Project Operations al Microsoft Dataverse, el sistema crea automàticament un projecte d'estimació d'ingressos de preu fix. La informació d'aquest projecte es basa en el següent:

  - Un mètode de facturació de preu fix.
  - Un projecte associat.
  - Com a mínim una fita definida a la pestanya **Planificació de la factura** de la pàgina **Línia de contracte del projecte**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Revisió de projectes d'estimació d'ingressos de preu fix
Per revisar els projectes d'estimació d'ingressos de preu fix, seguiu aquests passos:

1. En l'entorn Dynamics 365 Finance, aneu a **Projectes de Gestió de Projectes i Comptabilitat** > **Projectes** > **d'estimació d'ingressos de preu fix**.
2. Seleccioneu el projecte que voleu visualitzar i feu doble clic a **Identificador del projecte d'estimació** per obrir el registre i revisar els detalls del projecte.
3. Expandiu la pestanya **Projecte**. Veureu un projecte a la quadrícula **Projectes seleccionats**. El sistema l'utilitza com a projecte per defecte perquè és el projecte associat a la línia de contracte del projecte. 
4. Per canviar l'associació, seleccioneu projectes addicionals i afegiu-los a la quadrícula **Projectes seleccionats**. Si se seleccionen diversos projectes en aquesta quadrícula, el percentatge completat del projecte i les estimacions d'ingressos es calculen junts per a tots els projectes seleccionats.

  El cost del projecte, el perfil d'ingressos, la plantilla de costos i el codi del període es poden definir manualment. Si no es defineixen manualment, els valors per defecte durant el càlcul de la primera estimació del projecte fan servir les regles configurades per als perfils de costos i ingressos del projecte.



[!INCLUDE[footer-include](../includes/footer-banner.md)]