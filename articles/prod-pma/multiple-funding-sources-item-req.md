---
title: Requisits d'articles per als contractes de projecte amb diversos orígens de finançament
description: En aquest article es proporciona informació sobre com configurar i utilitzar els requisits dels elements amb múltiples fonts de finançament.
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

Alguns acords contractuals per a lliurables basats en projectes poden requerir diverses fonts de finançament. En aquest article s'explica com seleccionar i configurar les fonts de finançament desitjades quan es requereixen diverses fonts per a un projecte o contracte de projecte.

## <a name="terminology"></a>Terminologia

- **Font de** finançament – L'entitat que finança l'obra del contracte del projecte. Aquesta entitat pot ser una organització interna o un compte de factura externa (client o subvenció).
- **Client del** projecte: l'entitat a la qual es lliura el treball del projecte.
- **Compte** de factura - L'entitat externa que paga el treball del projecte.

## <a name="example"></a>Exemple

Contoso ha guanyat un contracte de renovació d'equips amb dos dels seus clients: Adatum US i Adatum Corporate. El contracte inclou els serveis de hardware i instal·lació que seran lliurats a Adatum US (el client del projecte). El maquinari serà finançat per Adatum Corporate (compte de factura 1), i els treballs d'instal·lació seran finançats per Adatum US (compte de factura 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurar regles per defecte del compte de factura per als requisits dels articles

### <a name="prerequisites"></a>Requisits previs

- Microsoft Dynamics 365 La **versió financera 10.0.27 o posterior** està obligada a utilitzar requisits d'articles que tinguin diversos comptes de factures.
- L'administrador del sistema ha d'habilitar els requisits de Permetre l'element **amb diverses fonts de finançament per a la funció d'escenaris basats en la producció o operacions** de projecte a l'espai **de treball de gestió** de funcions.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurar les regles per defecte del compte de factura

Per configurar les regles per defecte del compte de factura, seguiu aquests passos.

1. Aneu a **Administració de projectes i comptabilitat** \> **Configuració** \> **Paràmetres de l'administració de projectes i comptabilitat**.
1. A la **pestanya General**, a la **secció Comandes de vendes i Requisits** de l'article, definiu l'opció **Permet per a projectes amb diverses fonts de** finançament a **Sí**.
1. **Al camp Client per defecte**, especifiqueu d'on prové per defecte el client de lliurament del projecte del requisit de l'element:

    - **De la font de** finançament - El client predeterminat de lliurament del projecte prové de la font de finançament. Si diverses fonts de finançament estan associades al contracte del projecte, s'utilitzarà la primera font de finançament de la llista.
    - **From project** - El client de lliurament de projecte per defecte prové del client seleccionat al **camp compte** del registre del projecte.

1. Opcional: definiu o canvieu el compte de factura per defecte als registres del projecte:

    1. Aneu a **Gestió de projectes i comptabilitat** \> **Tots** \> **els projectes** i obriu els detalls del registre del projecte.
    2. A la **pestanya General**, definiu o actualitzeu el **camp Compte** de factura per defecte. El compte que especifiqueu s'utilitzarà com a compte de factura per defecte per als requisits d'element nous que es creïn per al projecte. Si deixeu el camp en blanc, s'utilitzarà per defecte el compte de factura de la primera font de finançament del contracte del projecte. Tanmateix, els usuaris podran canviar el compte quan desin el registre.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Seleccionar el compte de factura que voleu utilitzar quan creeu un requisit d'element

Per seleccionar el compte de factura que voleu utilitzar quan creeu un requisit d'element, seguiu aquests passos.

1. Aneu a **Gestió de projectes i comptabilitat** \> **Tots** \> **els projectes** i seleccioneu el registre del projecte.
1. A la **pestanya Pla**, seleccioneu **Requisits** de l'element.
1. Creeu un registre de requisits d'element nou.

    - Per defecte, el **camp Compte** factura del registre es defineix al compte de factura definit per al projecte. Podeu canviar el valor del camp Compte **de** factura i desar el registre. Un cop desat el registre, ja no podreu actualitzar el valor del **compte** factura. Si heu d'actualitzar el valor del **compte** factura per al requisit de l'article, suprimiu el requisit d'element existent i, a continuació, creeu-ne un de nou que tingui el valor desitjat.
    - Per defecte, el **camp Client per al** requisit d'element s'estableix en funció del valor per defecte del **client** que es defineix a la **pàgina Paràmetres comptables** i d'administració del projecte.

    Quan es desa el registre de requisits de l'element, el sistema l'associa amb el registre de capçalera de la comanda **de vendes del requisit de l'element**. Si cap capçalera de comanda de venda oberta té el compte de factura seleccionat, el sistema en crearà un i hi associarà la línia de requisits de l'article.

> [!NOTE]
> Els requisits de l'article sempre es facturen completament al compte de factura que s'estableix al registre. Actualment, el sistema no admet regles d'assignació de finançament que tinguin requisits d'articles i no dividirà la publicació en funció de la configuració de les regles d'assignació de finançament.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Crear un requisit d'element a partir d'un registre de previsió d'elements

Per crear un requisit d'element a partir d'un registre de previsió d'elements, seguiu aquests passos.

1. Anar a **Gestió de projectes i comptabilitat** \> **Projectes** \> **Tots els projectes** i seleccioneu el registre del projecte.
1. A la **pestanya Pla**, seleccioneu **Previsions** d'elements.
1. Creeu un registre de previsió d'elements nou.
1. Opcional: a la **pestanya Projecte**, al **camp Font de finançament**, seleccioneu el compte de factura que vulgueu.
1. Seleccioneu **Crea un requisit d'element** i confirmeu el missatge que rebeu.

    > [!NOTE]
    > El sistema copia el valor de la **font** de finançament del registre de previsió d'elements al registre de requisits d'elements de nova creació.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Compte de factura predeterminat quan el sistema crea automàticament un requisit d'element a partir d'una línia de comanda de compra

Si l'opció Crea un **requisit** d'element està definida com a **Sí** a la **pàgina Administració del projecte i paràmetres comptables**, el sistema crea automàticament un requisit d'element quan es desa una línia d'ordre de compra de projecte nova. Per defecte, els **camps Compte** de factura i **Requisit** de l'element es defineixen al valor del camp Compte **de** factura per defecte del registre de projecte. Actualment, el sistema no admet actualitzar ni canviar el compte de factura per a registres d'aquest tipus.
