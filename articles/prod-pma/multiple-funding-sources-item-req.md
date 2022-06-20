---
title: Requisits d'articles per als contractes de projecte amb diversos orígens de finançament
description: En aquest article s'ofereix informació sobre com configurar i utilitzar els requisits d'elements amb diverses fonts de finançament.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a54ca1ec5e78d9d0af7b67914f6a63154c7347d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931180"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisits d'articles per als contractes de projecte amb diversos orígens de finançament

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Alguns acords contractuals per a lliuraments basats en projectes poden requerir múltiples fonts de finançament. En aquest article s'explica com seleccionar i configurar les fonts de finançament desitjades quan es requereixen múltiples fonts per a un contracte de projecte o projecte.

## <a name="terminology"></a>Terminologia

- **Font de** finançament: l'entitat que finança el contracte de treball del projecte. Aquesta entitat pot ser una organització interna o un compte de factura extern (client o subvenció).
- **Client** del projecte: l'entitat a la qual es lliura el treball del projecte.
- **Compte** de factura: l'entitat externa que paga el treball del projecte.

## <a name="example"></a>Exemple

Contoso ha guanyat un contracte de renovació d'equips amb dos dels seus clients: Adatum US i Adatum Corporate. El contracte inclou serveis de maquinari i instal·lació que es lliuraran a Adatum US (el client del projecte). El maquinari serà finançat per Adatum Corporate (compte de factura 1), i els treballs d'instal·lació seran finançats per Adatum US (compte de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar regles per defecte del compte de factura per als requisits de l'element

### <a name="prerequisites"></a>Requisits previs

- Microsoft Dynamics 365 Les finances i les operacions **versió 10.0.27 o posterior** es requereixen per utilitzar requisits d'elements que tinguin diversos comptes de factura.
- L'administrador del sistema ha d'habilitar els requisits Permet l'element **amb diverses fonts de finançament per a la funció d'escenaris emmagatzemats/basats** en la producció del projecte a l'àrea **de treball de gestió** de funcions.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar les regles per defecte del compte de factura

Per configurar les regles per defecte del compte de factura, seguiu aquests passos.

1. Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres de l'administració de projectes i comptabilitat**.
1. A la **pestanya General**, a la **secció Ordres** de vendes i requisits d'element, definiu l'opció **Permet els projectes amb múltiples fonts de** finançament a **Sí**.
1. **Al camp Client** per defecte, especifiqueu d'on prové per defecte el client de lliurament del projecte al requisit de l'element:

    - **De la font de** finançament- El client de lliurament de projectes predeterminats prové de la font de finançament. Si hi ha diverses fonts de finançament associades al contracte del projecte, s'utilitzarà la primera font de finançament de la llista.
    - **Des del projecte** : el client de lliurament de projectes per defecte prové del client seleccionat al camp Compte de **registre** del projecte.

1. Opcional: definiu o canvieu el compte de factura per defecte als registres del projecte:

    1. Aneu a **Projectes** \> **de gestió de projectes i comptabilitat** \> **Tots els projectes** i obriu els detalls del registre del projecte.
    2. A la **pestanya General**, definiu o actualitzeu el **camp Compte de** factura per defecte. El compte que especifiqueu s'utilitzarà com a compte de factura per defecte per als requisits d'element nous que es creen per al projecte. Si deixeu el camp en blanc, el compte de factura de la primera font de finançament del contracte del projecte s'utilitzarà per defecte. No obstant això, els usuaris podran canviar el compte quan desin el registre.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccioneu el compte de factura que s'utilitzarà quan creeu un requisit d'element

Per seleccionar el compte de factura que s'utilitzarà quan creeu un requisit d'element, seguiu aquests passos.

1. Aneu a **Gestió de projectes i comptabilitat** \> **de projectes** \> **Tots els projectes** i seleccioneu el registre del projecte.
1. A la **pestanya Pla**, seleccioneu **Requisits** de l'element.
1. Crea un registre de requisit d'element nou.

    - Per defecte, el **camp Compte factura** del registre està definit com a compte de factura definit per al projecte. Podeu canviar el valor del **camp Compte factura** i desar-lo. Un cop desat el registre, ja no podeu actualitzar el valor del **compte** factura. Si heu d'actualitzar el valor del **compte** factura del requisit de l'element, suprimiu el requisit d'element existent i, a continuació, creeu-ne un de nou que tingui el valor desitjat.
    - Per defecte, el **camp Client** per al requisit de l'element s'estableix en funció del **valor de client** per defecte que s'estableix a la **pàgina Gestió de projectes i paràmetres comptables**.

    Quan es desa el registre de requisit d'element, el sistema l'associa amb el registre de capçalera de l'ordre de **vendes de requisits d'element**. Si cap capçalera de comanda de vendes oberta té el compte de factura seleccionat, el sistema en crearà un i hi associarà la línia de requisits de l'element.

> [!NOTE]
> Els requisits de l'element sempre es facturen completament al compte de factura que es defineix al registre. Actualment, el sistema no admet les regles d'assignació de finançament que tenen requisits d'elements i no dividirà la publicació en funció de la configuració de les regles d'assignació de finançament.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crear un requisit d'element a partir d'un registre de previsió d'elements

Per crear un requisit d'element a partir d'un registre de previsió d'elements, seguiu aquests passos.

1. Aneu a **Gestió de projectes i comptabilitat** \> **de projectes** \> **Tots els projectes** i seleccioneu el registre del projecte.
1. A la **pestanya Pla**, seleccioneu **Previsions d'elements**.
1. Crea un registre de previsió d'elements nou.
1. Opcional: a la **pestanya Projecte**, al camp Origen del **finançament**, seleccioneu el compte de factura desitjat.
1. Seleccioneu **Crea un requisit** d'element i confirmeu el missatge que rebeu.

    > [!NOTE]
    > El sistema copia el valor d'origen **del** finançament del registre de previsió de l'element al registre de requisit d'element acabat de crear.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Compte de factura per defecte quan el sistema crea automàticament un requisit d'element a partir d'una línia de comanda de compra

Si l'opció **Crea un requisit** d'element està establerta com a Sí **a** la **pàgina Gestió de projectes i paràmetres comptables**, el sistema crea automàticament un requisit d'element quan es desa una línia de comanda de compra de projecte nova. Per defecte, els **camps Compte** factura i **Requisit d'element** s'estableixen al valor del camp Compte **de** factura per defecte del registre del projecte. Actualment, el sistema no admet l'actualització ni el canvi del compte de factura dels registres d'aquest tipus.
