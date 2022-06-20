---
title: Moneda
description: En aquest article s'ofereix informació sobre com afegir i suprimir tipus de moneda a les operacions del projecte.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0fbfd1039fe0a7401376bb8c27b118297fdc87f5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921520"
---
# <a name="currency"></a>Moneda

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_



Les monedes determinen els preus dels productes del catàleg de productes i el cost de les transaccions, com ara les comandes de venda. Si els clients estan repartits per zones geogràfiques, afegiu les seves divises per gestionar les seves transaccions. Afegiu les divises més adequades per a les necessitats empresarials actuals i futures.  

> [!NOTE]
> Si el vostre entorn és un entorn del Common Data Service, esteu al Centre d'administració del Power Platform i seleccioneu la pàgina **Monedes** (**Entorns** > [seleccioneu un entorn] > **Configuració** > **Empresa** > **Monedes**), la pàgina estarà en blanc. Això es deu al fet que la definició d'una moneda no està admesa en entorns del Common Data Service.

## <a name="add-a-currency"></a>Afegir una moneda  
Abans d'iniciar aquest procediment, comproveu que la funció de seguretat inclogui permisos d'administració del sistema. 

1. Al centre d'administració del Power Platform, seleccioneu un entorn. 
2. Seleccioneu **Configuració** > **Negoci**.
3. Seleccioneu **Monedes**.  
4. Seleccioneu **Crea**.  
5. Empleneu la informació segons calgui.  


   |          Camp          |                                                                                                                                                                                                                                                                                                                                                                            Descripció                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Tipus de moneda**    | - **Sistema**: seleccioneu aquesta opció si voleu utilitzar les divises disponibles a les aplicacions basades en models del Dynamics 365. Seleccioneu **Cerca** per cercar una moneda. Quan seleccioneu un codi de divisa, **el nom de la divisa** i el **símbol monetari** s'afegeixen automàticament a la divisa seleccionada.<br />- **Personalitzat**: seleccioneu aquesta opció si voleu afegir una divisa que no està disponible a les aplicacions basades en models del Dynamics 365. En aquest cas. heu d'introduir manualment els valors de **Codi de moneda**, **Precisió de divisa**, **Nom de la moneda**, **Símbol monetari** i **Conversió de moneda**. |
   |    **Codi de moneda**    |                                                                                                                                                                                                                                                                                                                                            Forma curta de la moneda. Per exemple, **USD** per als dòlars d'Estats Units.                                                                                                                                                                                                                                                                                                                                            |
   | **Precisió de la moneda**  |                                                                                                                                                                                  Escriviu el nombre de decimals que voleu que s'utilitzin per a la moneda.  Podeu afegir un valor entre 0 i 4. **Nota**: si heu definit un valor de precisió al quadre de diàleg **Configuració del sistema**, el valor apareixerà aquí.                                                                                                                                                                                  |
   |    **Nom de la moneda**    |                                                                                                                                                                                                                                         Si heu seleccionat un codi de moneda de la llista de monedes disponibles a les aplicacions basades en models del Dynamics 365, el nom de la moneda del codi seleccionat es mostra aquí. Se heu seleccionat **Personalitzat** com el codi de la moneda, escriviu el nom de la moneda.                                                                                                                                                                                                                                          |
   |   **Símbol monetari**   |                                                                                                                                                                                                                                                                      Si heu seleccionat un codi de moneda de la llista de monedes disponibles, el símbol de la moneda seleccionada es mostra aquí. Se heu seleccionat **Personalitzat** com el codi de la moneda, introduïu el símbol de la nova moneda.                                                                                                                                                                                                                                                                       |
   | **Conversió de moneda** |                                                                                                                                                                                                                                     Escriviu el valor de la moneda seleccionada en referència a un dòlar dels Estats Units. Aquesta és la quantitat a la qual es converteix la moneda seleccionada a la moneda base. **Important:** Assegureu-vos d'actualitzar aquest valor tan sovint com sigui necessari per evitar els càlculs inexactes a les vostres transaccions.                                                                                                                                                                                                                                      |


6. Quan acabeu de fer els canvis, seleccioneu **Desa** o **Desa i tanca** a la barra d'ordres.  

   > [!TIP]
   >  Per editar una moneda, seleccioneu la moneda i introduïu o seleccioneu els nous valors.  

## <a name="delete-a-currency"></a>Suprimir una moneda  

1. Al centre d'administració del Power Platform, seleccioneu un entorn. 
2. Seleccioneu **Configuració** > **Negoci**.
3. Seleccioneu **Monedes**.  
4. De la llista de monedes, seleccioneu la moneda que voleu suprimir.  
5. Seleccioneu **Suprimeix**.  
6. Confirmar la supressió.  

> [!IMPORTANT]
>  Les monedes que utilitzen altres registres no es poden suprimir, només es poden desactivar. La desactivació dels registres de moneda no suprimeix la informació de moneda emmagatzemada als registres existents, com les oportunitats o les comandes. No obstant això, no podreu seleccionar la moneda desactivada per a les noves transaccions.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]