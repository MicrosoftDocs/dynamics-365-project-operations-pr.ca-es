---
title: Com puc personalitzar el flux del procés de negoci del Project Stages?
description: Informació general sobre com personalitzar el flux del procés de negoci de les fases del projecte.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 15540f524fb8fca8f69a2249f783289ba683cad7dabbf58ecbf620d147e5d491
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002949"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Com puc personalitzar el flux del procés de negoci del Project Stages?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Hi ha una limitació coneguda en les versions anteriors de l'aplicació del Project Service que els noms de les etapes en el flux del procés de negoci del Project Stages han de coincidir exactament amb els noms esperats en anglès (**Quote**, **Plan**, **Close**). En cas contrari, la lògica empresarial, que es basa en els noms de les etapes en anglès, no funcionarà com s'espera. És per això que no hi ha accions familiars com **Canvia el procés** o **Edita el procés** disponibles al formulari del projecte i no es recomana personalitzar el flux del procés de negoci. 

Aquesta limitació s'ha corregit a la versió 2.4.5.48 i posterior. Aquest article proporciona solucions alternatives suggerides per si ha de personalitzar el flux del procés de negoci predeterminat en versions anteriors.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>La lògica empresarial requereix una coincidència exacta amb els noms de les etapes en anglès

El flux del procés de negoci del Project Stages inclou la lògica empresarial que impulsa els següents comportaments en l'aplicació:
- Quan el projecte està associat a una oferta, el codi estableix el flux del procés de negoci en l'etapa de **Quote**.
- Quan el projecte està associat a un contracte, el codi estableix el flux del procés de negoci en l'etapa de **Plan**.
- Quan el flux del procés de negoci avança fins a l'etapa **Close**, el registre del projecte es desactiva. Quan el projecte està desactivat, el formulari del projecte i l'estructura del desglossament del treball (WBS) es configuren com de només lectura, es publiquen les reserves de recursos amb nom i es desactiven les llistes de preus associades.

Aquesta lògica empresarial es basa en els noms en anglès per a les etapes del projecte. Aquesta dependència dels noms d'etapa en anglès és la principal raó per la qual no es recomana personalitzar el flux del procés de negoci del Project Stages, i per la qual no es veuen les accions comunes com **Canvia el procés** o **Edita el procés** a l'entitat del projecte.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Què passa si els noms de les etapes no coincideixen amb els noms en anglès?

En la versió 1.x de l'aplicació Project Service a la plataforma 8.2, quan els noms d'etapa en el flux del procés de negoci no coincideixen exactament amb els noms d'etapa en anglès, s'omet la lògica empresarial que estableix la fase correcta per a ofertes o contractes, o que tanca el projecte. No es mostren missatges d'error. Per tant, sembla que podeu personalitzar el flux del procés de negoci del Project Stages. No obstant això, no veureu cap dels processos automàtics treballant per a ofertes, contractes ni tancament de projecte.

A l'aplicació del Project Service versió 2.4.4.30 o anterior a la plataforma 9.0, hi va haver un canvi arquitectònic significatiu en els fluxos del procés de negoci que va requerir una reescriptura de la lògica empresarial. Com a resultat, si els noms d'etapa del procés no coincideixen amb els noms en anglès esperats, apareixerà un missatge d'error. 

Per tant, si desitgeu personalitzar el flux del procés de negoci del Project Stages per a l'entitat del projecte, només podreu afegir noves etapes al flux predeterminat per l'entitat del projecte, si manteniu les fases **Quote**, **Plan** i **Close** tal com estan. Aquesta restricció garanteix que no apareguin errors de lògica empresarial que esperen els noms de les fases en anglès en el flux del procés de negoci.

En la versió 2.4.5.48 o posterior, la lògica empresarial descrita en aquest article s'ha eliminat del flux del procés de negoci predeterminat per l'entitat del projecte. L'actualització a aquesta versió o posterior permetrà personalitzar o reemplaçar el flux del procés de negoci predeterminat per un de propi. 

## <a name="workarounds-for-earlier-versions"></a>Solucions provisionals per a versions anteriors

Si l'actualització no és una opció, podeu personalitzar el flux del procés de negoci del Project Stages per a l'entitat del projecte d'una d'aquestes dues maneres:

1. Afegiu fases addicionals a la configuració per defecte i conserveu els noms en anglès per a **Quote**, **Plan** i **Close**.


![Captura de pantalla que mostra com afegir fases a la configuració per defecte.](media/FAQ-Customize-BPF-1.png)
 
2. Creu el vostre propi flux del procés de negoci i convertiu-lo en el flux principal per a l'entitat del projecte i podreu tenir els noms que vulgueu per a les fases. No obstant això, si voleu utilitzar les mateixes fases de projecte estàndard **Quote**, **Plan** i **Close**, heu de realitzar algunes personalitzacions que eliminaran els vostres noms personalitzats. La lògica més complexa es troba en el tancament del projecte però la podeu activar simplement desactivant el registre del projecte.

![Personalització del BPF.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Consideracions addicionals per a l'aplicació Project Service versió 2.4.4.30 o anterior a la plataforma 9.

Al Project Service 2.4.4.30 o anterior a la plataforma 9.0, amb un flux del procés de negoci personalitzat, el camp **Nom de fase** en l'entitat de projecte que s'utilitza en el gràfic **Projecte per fase** i les vistes de llista de projectes no s'actualitzaran, perquè està acoblat al flux del procés de negoci de les fases del projecte per defecte. Podeu solucionar aquest problema amb els passos següents:

- Afegiu un camp personalitzat per capturar la fase del flux del procés de negoci actual que s'actualitza a mesura que l'usuari avança a través del flux personalitzat.

- Modifiqueu el gràfic **Projecte per fase** perquè funcioni amb el vostre camp personalitzat en lloc de amb la configuració predeterminada.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Passos per crear el vostre propi flux del procés de negoci per a l'entitat del projecte

Per crear el vostre propi flux del procés de negoci per a l'entitat del projecte, feu el següent:

1. Aneu a **Configuració** > **Centre de processos**. No copieu el flux del procés de negoci de les Etapes del projecte perquè aquesta acció també copia la lògica de negocis del Project Service.

  ![Crear un procés.](media/FAQ-Customize-BPF-3.png)

2. Utilitzeu el Dissenyador de processos per crear els noms de fases que desitgeu. Si desitgeu la mateixa funcionalitat que les fases predeterminades per a **Quote**, **Plan** i **Close**, haureu de crear-la en funció dels noms de fase del flux del procés de negoci personalitzats.

   ![Captura de pantalla del dissenyador de processos utilitzat per personalitzar BPF.](media/FAQ-Customize-BPF-4.png) 

3. En el Dissenyador de processos, feu clic a **Flux del procés de la comanda** per fer que el flux del procés de negoci personalitzat sigui el flux principal per a l'entitat del projecte, moveu-lo per sobre del flux de les Fases del projecte al principi de la llista.


   [Captura de pantalla de l'ús del Flux del procés de la comanda](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Els següents passos s'apliquen a l'aplicació del Project Service 2.4.4.30 o anterior a la plataforma 9.0

4. Afegiu un camp personalitzat nou a l'entitat del projecte per capturar les fases personalitzades al vostre flux del procés de negoci personalitzat. Us cal afegir lògica empresarial (complement/flux de treball) per actualitzar aquest camp quan s'actualitzi la fase en el flux del procés de negoci personalitzat.

   ![Captura de pantalla de la personalització de l'entitat del projecte.](media/FAQ-Customize-BPF-6-720.png)

5. Modifiqueu el gràfic **Projecte per fase** per usar el vostre camp personalitzat nou per a les fases.

   ![Captura de pantalla de l'ús del gràfic Projecte per fase.](media/FAQ-Customize-BPF-7-720.png)

6. Modifiqueu les vistes de l'entitat del projecte per incloure el vostre camp personalitzat nou per a les fases.

   ![Captura de pantalla de la modificació de les visualitzacions de l'entitat del projecte.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]