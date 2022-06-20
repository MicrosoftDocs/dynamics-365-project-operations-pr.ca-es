---
title: Còpia d'oportunitats basades en projectes
description: En aquest article s'ofereix informació sobre la còpia d'oportunitats basades en projectes a les operacions del projecte.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926120"
---
# <a name="copy-project-based-opportunities"></a>Còpia d'oportunitats basades en projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_


Les oportunitats del projecte es poden copiar fàcilment per crear noves oportunitats de projecte. 

1. Aneu a la pàgina de llista **Oportunitats del projecte** i seleccioneu una oportunitat de la llista. O bé, obriu la pàgina de detalls d'una oportunitat específica. 
2. Des de qualsevol pàgina, seleccioneu **Copia**. S'obrirà una pàgina de diàleg que conté la informació de camp següent. Segons els valors seleccionats en aquest diàleg, el procés de còpia pot canviar.

    | **Camp** | **Descripció** | **Impacte descendent** |
    | --- | --- | --- |
    | Tema | Introduïu el tema rellevant de l'oportunitat de destinació. Quan s'obri el diàleg, el sistema l'establirà al tema de l'oportunitat d'origen amb **còpia** al final. | No hi ha cap impacte descendent d'aquest camp. |
    | Compte | Fa referència a l'empresa del client o registre de compte. Quan s'obri el diàleg, el sistema l'establirà al compte en l'oportunitat d'origen. | Aquest camp és el client principal de l'oportunitat. |
    | Unitat de contractació | La unitat de l'organització responsable del lliurament dels projectes associats amb aquest acord. Quan s'obre el quadre de diàleg, el sistema el definirà a la unitat contractant de l'oportunitat d'origen. | La unitat de contractació és la divisió de l'empresa que executa els projectes després d'haver tancat l'acord. Cada unitat de contractació té una moneda, i aquesta moneda s'utilitza per informar dels costos estimats i reals incorreguts durant el projecte. |
    | Moneda | Moneda en la qual es realitza la transacció de l'acord. Quan s'obre la pàgina de diàleg, el sistema el definirà a la moneda de l'oportunitat d'origen. | La moneda s'utilitza per obtenir una llista de preus per defecte i crear estimacions financeres a l'oferta. Finalment, la moneda s'utilitza per facturar al client quan es guanya l'acord. |
    | Copia els preus | Valor Sí/No que indica si els preus de l'oportunitat s'han de copiar de l'oportunitat d'origen. | Si se selecciona **Sí**, les llistes de preus es copien de l'oportunitat d'origen a la de destinació. Si se selecciona **No**, les llistes de preus per defecte es basen en les darreres llistes de preus configurades. |

3. Seleccioneu **D'acord**. El sistema crea una còpia de l'oportunitat del projecte en funció dels paràmetres seleccionats i s'obre la nova oportunitat del projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]