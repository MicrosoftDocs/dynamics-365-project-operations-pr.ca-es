---
title: Informació general del procés de vendes
description: Aquest tema proporciona informació sobre els processos bàsics de vendes.
author: rumant
manager: Annbe
ms.date: 10/29/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8300887e7c5fbd78343d16d191775a67e43138e2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5277371"
---
# <a name="sales-process-overview"></a>Informació general del procés de vendes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els processos de venda que s'utilitzen en una organització basada en projectes es diferencien dels processos de venda que s'utilitzen en una organització basada en productes. Això es produeix perquè els cicles de venda d'organitzacions basades en projectes són més llargs i requereixen tècniques d'estimació personalitzades per analitzar i crear ofertes per a cada operació. El Dynamics 365 Project Operations utilitza algunes de les funcionalitats següents que s'utilitzen en un procés de venda:

- Un registre Client potencial s'utilitza per fer el seguiment del procés de vendes.
- Es fa un seguiment dels clients potencials qualificats com a oportunitats.
- Tots els artefactes relacionats d'una oportunitat són accessibles. Aquests artefactes inclouen l'equip de vendes, les parts interessades, la probabilitat, la puntuació, les fases de vendes i els processos de negoci.
- Es creen diverses ofertes per a una oportunitat.
- Una oferta rep l'estat **Tancada com a guanyada** per crear una comanda de venda. Al Project Operations, la comanda de vendes es personalitza i s'anomena contracte de projecte.

## <a name="estimate-a-sale"></a>Estimació d'una venda
El valor d'una venda es pot estimar a partir de projectes que abans s'hagin lliurat i de la complexitat dels projectes. Per a projectes que comportin ampliacions a projectes previs, o projectes en els quals l'experiència del venedor és gran i s'utilitzen plantilles de treball, podeu utilitzar un procés d'estimació més senzill. Normalment, els projectes més complexos tenen un procés de compra més llarg. Per tant, hi ha més fases en el procés d'estimació de vendes. A principis del procés, l'equip de vendes utilitza l'entrada dels administradors del compte i els experts de la matèria (SME) per crear una estimació d'alt nivell per a cada component diferent del treball que s'ofereix. Aquests components de treball es representen amb línies d'oferta. 

Podeu crear una estimació d'alt nivell de l'oferta. Amb el temps, aquesta estimació d'alt nivell es reemplaçarà per una estimació més detallada basada en un pla de projecte que creeu amb les plantilles de projecte estandarditzades. Aquestes plantilles us ajuden a construir una planificació i determinen els valors monetaris de l'oferta i els seus components (línies d'oferta). 

Podeu crear diverses ofertes per a un projecte i agrupar-les en un únic registre d'oportunitat. Eventualment, una d'aquestes ofertes es marca com a **Tancada com a guanyada** i es crea un contracte de projecte o una declaració de treball (SOW). Un contracte de projecte té el valor contractat per a cada component (línia de contracte) que el client accepta per al seu lliurament. Normalment es crea un SOW com a document del Microsoft Word. Totes les factures que s'envien al client en el transcurs de l'enviament del projecte fan referència al contracte del projecte o SOW.

També podeu crear ofertes alternatives en un registre d'oportunitat o configurar el sistema per tal que es creï un contracte de projecte quan es guanya una oferta. En aquest cas, podeu adjuntar un document del Word que representi el SOW al registre de contracte del projecte.

## <a name="configure-the-sales-process"></a>Configuració del procés de vendes
Podeu utilitzar els fluxos del procés de negoci per configurar el procés de vendes. Aquests fluxos proporcionen una interfície visual guiada per fer avançar les ofertes per les fases del procés de venda.

Per exemple, pot ser que l'empresa tingui les sis fases següents en el procés de vendes:

1. Qualifica
2. Aproximat
3. Revisió interna
4. Contracte
5. Lliura
6. Tanca 
 
La vostra organització podria utilitzar entitats diferents per representar la mateixa oferta a mesura que evoluciona. A principis del procés de vendes, un acord està representat per l'entitat Oportunitat. A mesura que passa el temps i hi ha més detalls que sorgeixen, podríeu utilitzar estimacions d'alt nivell per crear una o diverses ofertes. Si una d'aquestes ofertes la revisen parts interessades internes i del client, l'entitat Oferta representa el tracte. Quan el client accepta l'oferta, un contracte o SOW del projecte representa el tracte. Per admetre aquest comportament, els BPF s'estructuren de manera que cada fase del procés es vincula a una altra taula de base de dades.

La fase **Qualificació** en el procés de venda pot basar-se en una entitat Oportunitat. Les fases **Estimació** i **Revisió interna** poden basar-se en una entitat Oferta. Les fases **Contracte**, **Lliurament** i **Tancament** poden basar-se en una entitat Contracte del projecte.

A mesura que l'oportunitat avanci a través de les fases, se us demanarà que creeu el registre de l'entitat adient per ajudar i guiar-vos pel procés. Les fases poden ser condicionals. Per exemple, si necessiteu una revisió interna d'una oferta només si l'oferta utilitza una llista de preus personalitzada, podeu configurar aquesta condició en la fase adequada del procés de negoci. Llavors, la fase **Revisió interna** només es mostra per a les ofertes que utilitzen una llista de preus personalitzada. Per a tots els altres negocis i ofertes, l'etapa **Estimació** va seguida de la fase **Contracte**.

> [!NOTE]
> El Project Operations té pàgines específiques dels registres d'entitat Oportunitat, Oferta, Comanda i Factura. Heu de crear aquests registres mitjançant les pàgines d'informació del projecte per a aquestes entitats. Si no és així, no podreu obrir els registres des de la pàgina **Informació del projecte**. Si voleu obrir un registre des de la pàgina **Informació del projecte**, heu de suprimir el registre i tornar-lo a crear amb la pàgina **Informació del projecte** on la lògica empresarial per a cadascun d'aquests tipus d'entitat garanteix que el camp **Tipus** del registre es defineix correctament i tots els conceptes obligatoris s'inicialitzen correctament.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Seguiment de revisions a ofertes i plans de projecte del cicle de venda
Al Project Operations, no podeu fer el seguiment de les revisions fetes en una oferta. En lloc d'això, heu de marcar l'oferta existent **Tancada com a perduda** i, a continuació, crear una oferta nova. Podeu copiar una oferta o clonar una oferta basada en projectes.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Seguiment de comentaris i aprovacions d'ofertes i contractes de projectes
Podeu administrar la revisió i l'aprovació de les ofertes i els contractes de projecte mitjançant el mur de registres i els missatges. La vostra organització pot crear fluxos de treball i complements personalitzats per assignar, redirigir, agreujar i administrar les notificacions dels elements de treball de revisió i aprovació.


[!INCLUDE[footer-include](../includes/footer-banner.md)]