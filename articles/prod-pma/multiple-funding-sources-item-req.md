---
title: Requisits d'articles per als contractes de projecte amb diversos orígens de finançament
description: En aquest article es proporciona informació sobre com configurar i utilitzar els requisits dels articles amb diverses fonts de finançament.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028461"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Requisits d'articles per als contractes de projecte amb diversos orígens de finançament

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

Alguns acords contractuals per a lliuraments basats en projectes podrien necessitar diverses fonts de finançament. En aquest article s'explica com seleccionar i configurar les fonts de finançament desitjades quan es requereixen diverses fonts per a un projecte o un contracte de projecte.

## <a name="terminology"></a>Terminologia

- **Font de finançament**: l'entitat que finança el treball del contracte del projecte. Aquesta entitat pot ser una organització interna o un compte de factura extern (client o subvenció).
- **Client del projecte**: l'entitat a què es lliura el treball del projecte.
- **Compte de la factura**: l'entitat externa que paga el treball del projecte.

## <a name="example"></a>Exemple

Contoso ha guanyat un contracte de renovació d'equipament amb dos dels seus clients: Adatum US i Adatum Corporate. El contracte inclou serveis de maquinari i instal·lació que es lliuraran a Adatum US (el client del projecte). Adatum Corporate (compte de factura 1) finançarà el maquinari i les activitats d'instal·lació les finançarà Adatum US (compte de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar les regles per defecte del compte de factura per als requisits dels elements

### <a name="prerequisites"></a>Requisits previs

- Cal el Microsoft Dynamics 365 Finance **versió 10.0.27 o posterior** per utilitzar els requisits dels articles que tenen diversos comptes de factura.
- L'administrador del sistema ha d'habilitar la característica **Permet els requisits d'elements amb diverses fonts de finançament per a escenaris del Project Operations mantinguts en existències / basats en producció** a l'àrea de treball **Administració de característiques**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar les regles per defecte del compte de factura

Per configurar les regles per defecte del compte de factura, seguiu aquests passos.

1. Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres de l'administració de projectes i comptabilitat**.
1. A la pestanya **General**, a la secció **Requisits de comandes de vendes i elements**,definiu l'opció **Permet els projectes amb diverses fonts de finançament** en **Sí**.
1. Al camp **Client per defecte**, especifiqueu d'on prové per defecte el client de lliurament del projecte al requisit de l'article:

    - **De font de finançament**: el client de lliurament de projecte per defecte prové de la font de finançament. Si hi ha diverses fonts de finançament associades amb el contracte de projecte, s'utilitzarà la primera font de finançament de la llista.
    - **De projecte**: el client de lliurament del projecte per defecte prové del client que se selecciona al camp **Compte de registre del projecte**.

1. Opcional: definiu o canvieu el compte de factura per defecte als registres de projecte:

    1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes** i obriu els detalls del registre del projecte.
    2. A la pestanya **General**, definiu o actualitzeu el camp **Compte de factura per defecte**. El compte que especifiqueu s'utilitzarà com a compte de factura per defecte per als nous requisits d'element creats per al projecte. Si deixeu el camp en blanc, el compte de factura de la primera font de finançament del contracte del projecte s'utilitzarà per defecte. Tanmateix, els usuaris podran canviar el compte quan desin el registre.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccioneu el compte de factura que voleu utilitzar quan creeu un requisit d'element

Per seleccionar el compte de factura que voleu utilitzar quan creeu un requisit d'element, seguiu aquests passos.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes** i seleccioneu el registre del projecte.
1. A la pestanya **Pla**, seleccioneu **Requisits d'element**.
1. Creeu un nou registre de requisit d'element.

    - Per defecte, el camp **Compte de factura** del registre es defineix com el compte de factura definit per al projecte. Podeu canviar el valor del camp **Compte de factura** i després desar el registre. Un cop desat el registre, ja no podeu actualitzar el valor de **Compte de factura**. Si heu d'actualitzar el valor de **Compte de factura** per al requisit de l'element, suprimiu el requisit d'element existent i creeu-ne un de nou amb el valor desitjat.
    - Per defecte, el camp **Client** del requisit d'element es defineix segons el valor de **Client per defecte** que es defineix a la pàgina **Paràmetres d'administració de projectes i comptabilitat**.

    Quan es desa el registre de requisit de l'element, el sistema l'associa amb el registre de capçalera de **Comanda de vendes de requisit d'element**. Si no hi ha cap capçalera de comanda de vendes oberta que tingui el compte de factura seleccionat, el sistema en crearà un i li associarà la línia de requisit de l'element.

> [!NOTE]
> Els requisits dels elements sempre es facturen totalment al compte de factura que es defineix al registre. Actualment, el sistema no admet les regles d'assignació de finançament que tenen requisits d'element i no es dividirà la comptabilització segons la configuració de les regles d'assignació de finançament.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crear un requisit d'element a partir d'un registre de previsió d'elements

Per crear un requisit d'element a partir d'un registre de previsió d'elements, seguiu aquests passos.

1. Aneu a **Administració de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes** i seleccioneu el registre del projecte.
1. A la pestanya **Pla**, seleccioneu **Previsions d'element**.
1. Creeu un nou registre de previsió d'element.
1. Opcional: a la pestanya **Projecte**, al camp **Font de finançament**, seleccioneu el compte de factura que vulgueu.
1. Seleccioneu **Crea el requisit d'element** i confirmeu el missatge que rebeu.

    > [!NOTE]
    > El sistema copia el valor de **Font de finançament** del registre de previsió d'elements al registre de requisit d'elements acabat de crear.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Compte de factura per defecte quan el sistema crea automàticament un requisit d'element a partir d'una línia de comanda de compra

Si l'opció **Crea un requisit d'element** es defineix com a **Sí** a la pàgina **Paràmetres d'administració de projectes i comptabilitat**, el sistema crea automàticament un requisit d'element quan es desa una nova línia de comanda de compra de projecte. Per defecte, els camps **Compte de factura** i **Requisit d'element** es defineixen en el valor del camp **Compte de factura per defecte** al registre de projecte. Actualment, el sistema no admet l'actualització ni el canvi del compte de factura per als registres d'aquest tipus.
