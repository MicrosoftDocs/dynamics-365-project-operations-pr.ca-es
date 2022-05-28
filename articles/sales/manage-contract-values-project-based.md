---
title: Treballar amb línies de contracte basades en projectes
description: Aquest tema proporciona informació sobre les línies de contracte basades en projectes.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f67c0447c0b2a23d6f7d03dfc5ac7800943bbf36
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595164"
---
# <a name="work-with-projectbased-contract-lines"></a>Treballar amb línies de contracte basades en projectes

Les línies de contracte basades en projectes al Dynamics 365 Project Operations estan dissenyades per contenir l'estimació i els acords de facturació per a components específics del treball del projecte en una interacció. L'estructura d'una línia de contracte basada en projectes s'amplia per a les estimacions del projecte i els escenaris de facturació amb els següents conceptes:

- Mètode de facturació
- Assignació de projectes i tasques
- Classes de transaccions incloses
- Límit que no s’ha de superar
- Configuració de la imputabilitat
- Estimacions amb detalls de línia de contracte
- Clients de línia de contracte

Els següents camps s'inclouen a la pestanya **General** de les línies de contracte basades en projectes. Aquests camps ajuden a establir les bases per a una estimació detallada i exhaustiva des de zero i les disposicions de facturació per al treball basat en projectes.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| **Nom** | Nom de la línia de contracte que identifica el component discret del contracte que s'estima. Per a un contracte de projecte creat a partir d'una oferta, aquest valor es copia d'un valor corresponent de la línia d'oferta basada en el projecte. | Aquest valor de camp es copia a la línia de factura del projecte que es crea a partir d'aquesta línia de contracte quan es crea la factura. |
| **Mètode de facturació** | En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta. Aquest és un conjunt d'opcions que representa els dos principals models de contractació admesos pel Project Operations:</br>- **Preu fix**</br>- **Temps i material** | En funció del mètode de facturació de la línia de contracte a la qual es fa referència, es processarà la transacció de valors reals. Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de temps i material, es crea un registre de cost i de valor real de vendes no facturades. Si la línia de contracte a la qual fa referència el valor real té un mètode de facturació de preu fix, només es crea un valor real de cost. |
| **Project** | Utilitzeu aquest camp per identificar el projecte que s'utilitzarà per lliurar el treball en aquesta interacció. | El valor en aquest camp s'utilitza conjuntament amb els camps **Tasques incloses** i **Classes de transacció incloses** per resoldre la referència de la línia de contracte en un registre de línia real o estimat. |
| **Inclou el temps** | Una marca indica si les transaccions de temps o els costos laborals del projecte seleccionat s'inclouen en aquesta línia de contracte. Un valor **No** indica que les transaccions de temps o els costos laborals no s'inclouran en aquesta línia de contracte. Un valor **Sí** indica que s'inclouran. | Aquest valor de camp s'utilitza conjuntament amb el projecte per resoldre la referència de la línia de contracte en un registre de línia real o estimat. |
| **Inclou la despesa** | Una marca indica si els costos de despesa del projecte seleccionat s'inclouran en aquesta línia de contracte. Un valor **No** indica que el cost de despesa no s'inclourà en aquesta línia de contracte. Un valor **Sí** indica que s'inclourà. | Aquest valor de camp s'utilitza conjuntament amb el projecte per resoldre la referència de la línia de contracte en un registre de línia real o estimat. |
| **Inclou la taxa** | Una marca indica si els càrrecs del projecte seleccionat s'inclouran en aquesta línia de contracte. Un valor **No** indica que els càrrecs no s'inclouran en aquesta línia de contracte. Un valor **Sí** indica que s'inclouran. | Aquest valor de camp s'utilitza conjuntament amb el projecte per resoldre la referència de la línia de contracte en un registre de línia real o estimat. |
| **Import contractat** | En una línia de contracte de preu fix, és el valor acordat que es facturarà al client per a tots els components de treball associats amb aquesta línia de contracte. En una línia de contracte de temps i material, aquest import és un valor estimat del que es facturarà al client per a tots els components de treball associats a aquesta línia de contracte. En un contracte de projecte creat a partir d'una oferta, aquest valor es copia del camp corresponent de la línia d'oferta. Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import dels detalls de la línia de contracte. | Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports als detalls de la línia. En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'import abans de l'impost a les fites de facturació periòdiques. |
| **Impost estimat** | L'usuari pot editar aquest camp per introduir l'import d'impostos estimat en la línia de contracte. Quan una línia de contracte basada en un projecte té detalls de la línia, aquest camp no es pot editar i es resumeix a partir de l'import d'impostos dels detalls de la línia de contracte. | Quan la línia de contracte té detalls de la línia, aquest valor es pot modificar canviant els imports d'impostos als detalls de la línia. En una línia de contracte de preu fix, aquest valor s'utilitza per generar l'impost a les fites de facturació periòdiques. |
| **Import contractat després d’impostos** | Import de la línia de contracte després de l'impost. Aquest camp és de només lectura i es calcula com a **Import contractat + Impostos**. | En una línia de contracte de preu fix, aquest valor s'utilitza per generar fites de facturació periòdiques. |
| **Límit que no s’ha de superar** | L'usuari pot editar aquest camp i només està disponible en línies de contracte basades en projectes que tenen un mètode de facturació de temps i material. | L'usuari pot editar aquest camp. Quan un valor real de temps o despesa fa referència a aquesta línia de contracte per temps i material, l'import del valor real s'avalua amb el límit que no es pot superar d'aquesta línia de contracte després de tenir en compte els imports ja gastats i compromesos. |
| **Pressupost del client** | Aquest camp és editable i es copia del camp corresponent de la línia d'oferta si el contracte s'ha creat a partir d'una oferta. | Aquest camp només s'utilitza per a informació i no té cap importància descendent. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Regla de validació per a les opcions a la pestanya General de línies de contracte basades en projectes

Regla: un projecte i una classe de transacció determinada només es poden incloure en una línia de contracte basada en projectes en un contracte.

| Contracte | Línia de contracte | Project | Inclou el temps | Inclou la despesa | Inclou el càrrec | Vàlid/No és vàlid | Raó                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Sí          | Sí             | Sí         | No és vàlid       | Infringeix la regla. El temps, les despeses i els càrrecs del projecte P1 s'inclouen en les dues línies de contracte, CL1 i CL2.                                                                                       |
| C1       | CL2           | P1      | Sí          | Sí             | Sí         | No és vàlid       | Infringeix la regla. El temps, les despeses i els càrrecs del projecte P1 s'inclouen en les dues línies de contracte, CL1 i CL2.                                                                                       |
| C1       | CL1           | P1      | Sí          | No              | Sí         | No és vàlid       | Infringeix la regla. El temps i els càrrecs del projecte P1 s'inclouen en les dues línies de contracte, CL1 i CL2.                                                                                                   |
| C1       | CL2           | P1      | Sí          | Sí             | Sí         | No és vàlid       | Infringeix la regla. El temps i els càrrecs del projecte P1 s'inclouen en les dues línies de contracte, CL1 i CL2.                                                                                                   |
| C1       | CL1           | P1      | Sí          | No              | Sí         | Vàlid           | El temps i els càrrecs del projecte P1 s'inclouen a CL1. La despesa en el projecte P1 s'inclou a CL2. </br>   No hi ha superposició en el que s'inclou en cada línia de contracte i, per tant, és vàlid.  |
| C1       | CL2           | P1      | No           | Sí             | No          | Vàlid           | El temps i els càrrecs del projecte P1 s'inclouen a CL1. La despesa en el projecte P1 s'inclou a CL2. </br>   No hi ha superposició en el que s'inclou en cada línia de contracte i, per tant, és vàlid.  |
| C1       | CL1           | P1      | Sí          | Sí             | Sí         | No és vàlid       | Infringeix la regla. El temps, les despeses i els càrrecs del projecte P1 s'inclouen en les línies dels dos contractes.                                                                                               |
| CL2      | CL2           | P1      | Sí          | Sí             | Sí         | No és vàlid       | Infringeix la regla. El temps, les despeses i els càrrecs del projecte P1 s'inclouen en les línies dels dos contractes.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]