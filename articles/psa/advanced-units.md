---
title: Grups d'unitats i unitats
description: Aquest article proporciona informació sobre grups i unitats d'unitats.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933388"
---
# <a name="unit-groups-and-units"></a>Grups d'unitats i unitats

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Els grups d'unitats i les unitats són entitats bàsiques del Microsoft Dynamics 365. Una unitat és una sola unitat de mesura, i es poden agrupar diverses unitats en grups d'unitats. A vegades es fa referència a un grup d'unitats com una planificació d'unitat a la interfície d'usuari (IU) del Dynamics 365. 

Aquí hi ha alguns exemples d'unitats i grups d'unitats:
 
- **Grup d'unitats**: distància 
    - **Unitats**: milla, quilòmetre, etcètera.
- **Grup d'unitats**: temps
    - **Unitats**: hora, dia, setmana, etcètera. 

Quan configureu diverses unitats en un grup d'unitats, també heu de configurar un factor de conversió entre ells designant la primera unitat que configureu com a unitat principal o per defecte del grup d'unitats. 

Per exemple, en un grup d'unitats **Temps**, si configureu **Hora** com a primera unitat, el sistema designa **Hora** com a unitat per defecte. Si la unitat següent que configureu és **Dia**, heu de configurar un factor de conversió de **Dia** a **Hora**. Si, a continuació, afegiu **Setmana** com a tercera unitat, heu de configurar un factor de conversió per a **Setmana** en termes de **Dia** o **Hora**. 

A la imatge següent es mostra una configuració d'exemple per a la unitat **Dia**, on el camp **Quantitat** mostra el nombre d'hores que hi ha en un dia, i **Setmana**, en què el camp **Quantitat** mostra el nombre de dies que hi ha en una setmana.

> ![Grup d'unitats: pàgina d'informació.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Utilitzar unitats i grups d'unitats

El Dynamics 365 Project Service Automation utilitza unitats i grups d'unitats per processar estimacions i entrades, tant per a les despeses com per al temps. 

Per a les despeses, cada categoria de despesa té un grup d'unitats i una unitat per defecte. Aquests valors s'introdueixen com a valors per defecte a les entrades de la llista de preus per a les categories de despesa. 

Per exemple, teniu una categoria de despesa que s'anomena **Quilometratge**. Té un grup d'unitats que es diu **Distància** i una unitat per defecte que s'anomena **Milla**. Si configureu el grup d'unitats **Distància** per tal que tingui dues unitats (**Milla** i **Quilòmetre**), podeu definir dos preus per a la categoria **Quilometratge** en una llista de preus: preu per milla i preu per quilòmetre.

| Categoria de despesa  | Grup d'unitats  | Unit      | Mètode de càlcul de preus  | Preu per unitat  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Quilometratge           | Distància      | Milla      | Preu per unitat    | 10 USD            |
| Quilometratge           | Distància      | Quilòmetre | Preu per unitat    |  6 USD            |

Quan introduïu una despesa en un projecte, el sistema determina el preu mitjançant la combinació de la categoria i la unitat de la despesa. 

| Descripció de la despesa        | Categoria de despesa  | Unit  | Quantitat  | Preu per unitat   |
|----------------------------|---------------------|-------|-----------|----------------|
| Conduir a la ubicació del client | Quilometratge             | Milla  | 10        | 10 USD         |

Per al temps, cada capçalera de la llista de preus té un camp **Unitat de temps per defecte**. El valor es defineix en crear la capçalera de la llista de preus. Aquesta unitat s'utilitza per definir tots els preus basats en funcions en aquesta llista de preus.

Les línies d'estimació del camp **Temps a l'oferta** es poden expressar en qualsevol unitat de temps. No obstant, les línies d'estimació dels projectes i les entrades de temps dels projectes només poden utilitzar la unitat de temps **Hora**. Si la unitat de l'entrada de temps o de la línia d'estimació no coincideix amb la unitat de la línia de la llista de preus per a aquesta funció, el sistema converteix el preu en les unitats definides a l'estimació del projecte o en la transacció de valors reals del projecte.

A l'exemple següent es mostra com el PSA utilitza el grup d'unitats, les unitats i els factors de conversió.
- Unitats

   - **Grup d'unitats**: temps 
   - **Unitats**: hora 
    
    - **Dia**: factor de conversió de 8 hores       
    - **Setmana**: factor de conversió de 40 hores  
        
- Configuració de la llista de preus al Projecte A:

    - **Nom**: preus de les vendes al Regne Unit el 2016 
    - **Unitat de temps per defecte**: dia 
    - **Moneda**: GBP

| Funció      | Grup d'unitats | Unit | Unitat organitzativa | Preu   |
|-----------|------------|------|---------------------|---------|
| Desenvolupador | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Entrada de temps

A la taula següent es mostra la transacció del costat de vendes resultant creada pel PSA per a un projecte de tres hores.


| Projecte   | Tasca    | Funció      | Quantitat | Unit  | Preu per unitat | Import de vendes no facturades |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projecte A | Disseny  | Desenvolupador | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>PMF d'unitats de temps

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>El PSA converteix a diferents unitats en el cas de les despeses?
No. La conversió d'unitats funciona només per als temps. Per a les despeses, si el sistema no pot trobar un preu per a la combinació de la categoria de despesa i d'unitat, el preu es defineix com a 0,00 per defecte.

### <a name="why-does-psa-convert-time-units"></a>Per què el PSA converteix les unitats de temps?
En alguns països o regions, hi ha un requisit legal perquè les tarifes de facturació es configurin en dies. La negociació de preu i el descompte durant el cicle d'oferta es fa mitjançant l'ús de les tarifes de dia per a cada funció facturable. L'estimació de la planificació i l'entrada de temps es fan en hores. Per admetre aquesta diferència a les unitats de temps, el PSA converteix les unitats de temps.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Es poden canviar les unitats de temps a les estimacions de projecte?
No. L'estimació de planificació es restringeix actualment a hores i no es pot canviar.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Poden editar-se, suprimir i afegir unitats i grups d'unitats?
Sí. Exceptuant el grup d'unitats **Temps** i la unitat **Hores**, totes les unitats es poden suprimir o editar i es poden afegir unitats noves. A PSA, el grup d'unitats **Temps** i la unitat **Hora** no es poden suprimir. No obstant, es poden actualitzar amb un text traduït del camp **Nom**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
