---
title: Productes
description: En aquest tema es proporciona informació sobre el catàleg de productes que podeu utilitzar per proporcionar informació als clients sobre els productes i els preus que ofereix l'organització.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 30633a7445baaf99af5be5c88e35b24824022b93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121251"
---
# <a name="products"></a>Productes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

Els productes són la columna vertebral del vostre negoci. Un catàleg de productes al Dynamics 365 Sales Professional és una col·lecció de productes que inclou la informació sobre els preus. Per fer més fàcil que els representants de vendes puguin incrementar les vendes, podeu crear ràpidament un catàleg de productes.

## <a name="add-a-product"></a>Afegir un producte

1.  Assegureu-vos que teniu la funció Administrador del sistema o Administrador de Sales Professional per poder afegir productes al Dynamics 365 Sales Professional.
2.  En el mapa del lloc, a **Configuració**, seleccioneu **Productes**.
3.  Seleccioneu **Afegeix un producte** i empleneu la següent informació:

    -  **Nom**
    -  **Identificador del producte**
    -  **Família principal**: seleccioneu una família de productes principal per al producte. Si esteu creant un producte secundari en una família de productes, aquí es completa el nom de la família de productes principal. Aquesta acció no es pot canviar després desar el registre.
    -  **Vàlid des de**/**Vàlid fins a**: definiu el període de validesa del producte seleccionant una data **Vàlid des de** i **Vàlid fins a**.
    -  **Grup d'unitats**: seleccioneu un grup d'unitats. Un grup d'unitats és una col·lecció de diferents unitats en les quals es ven un producte i defineix la manera com els elements individuals s'agrupen en quantitats més grans. Per exemple, si afegiu llavors com a producte, és possible que hàgiu creat un grup d'unitats anomenat "Llavors" i hàgiu definit la seva unitat principal com a "paquet".
    -  **Unitat per defecte**: seleccioneu la unitat més comuna en la qual es vendrà el producte. Les unitats són les quantitats o mesures en les quals vendreu els productes. Per exemple, si afegiu les llavors com a producte, les podeu vendre en paquets, caixes o palets. Cadascuna es converteix en una unitat de producte. Si les llavors es venen majoritàriament en paquets, seleccioneu aquest format com la unitat.
    -  **Llista de preus per defecte**: si el producte és nou, aquest camp és només de lectura. Per poder seleccionar una llista de preus per defecte, primer heu d'emplenar tots els camps obligatoris i, a continuació, desar el registre. Tot i que la llista de preus per defecte no és necessària, després de desar el registre del producte és una bona idea definir una llista de preus per defecte per a cada producte. Així, si un registre de client no conté cap llista de preus, el Sales podrà utilitzar la llista de preus per defecte per generar ofertes, comandes i factures.
    -  **Decimals admesos**: heu d'escriure un nombre enter comprès entre 0 i 5. Si el producte no es pot dividir en quantitats fraccionals, escriviu 0. La precisió del camp **Quantitat** al registre de l'oferta, comanda o producte de la factura es valida en funció del valor d'aquest camp si el producte no té una llista de preus associada.
    -  **Tema**: podeu associar aquest producte a un tema. Podeu utilitzar els temes per ordenar per categories els productes i per filtrar els informes.

4.  Seleccioneu **Desa**.
5.  A la pestanya **Detalls addicionals**, a la secció **Elements de la llista de preus**, seleccioneu **Més ordres** i, a continuació, seleccioneu **Afegeix nou element de la llista de preus**.
7.  A la pestanya **Detalls addicionals**, a la secció **Relació de productes**, seleccioneu la icona **Més ordres** i, a continuació, seleccioneu **Afegeix una relació de producte nova.**
8.  Al formulari **Relació de producte nova**, introduïu els següents detalls i, a la barra d'ordres, seleccioneu **Desa i tanca**:

    -   **Producte relacionat**: seleccioneu el producte que voleu afegir com a producte relacionat al registre de producte existent en el qual esteu treballant.
    -   **Tipus de relació de vendes**: seleccioneu si voleu afegir el producte com un increment de venda, una venda creuada o un producte substitut.
    -   **Direcció**: seleccioneu si la relació entre els productes serà unidireccional o bidireccional. Si seleccioneu Unidireccional, el producte que seleccioneu a **Producte relacionat** es mostrarà com una recomanació per al producte existent, però no viceversa.

9.  Al formulari Producte, seleccioneu **Desa**.

## <a name="import-products"></a>Importar productes

Podeu utilitzar les plantilles d'importació per incloure massivament dades del producte al Dynamics 365 Sales.

## <a name="revise-a-product"></a>Revisar un producte

Manteniu l'inventari de productes actualitzat per revisar ràpidament les propietats dels productes segons calgui, i tornar a publicar la informació per tal que els vostres agents de vendes puguin veure els últims canvis a l'inventari.

1.  Assegureu-vos que teniu una de les funcions de seguretat o permisos equivalents següents: administrador del sistema, personalitzador del sistema, cap de vendes, vicepresident de vendes, vicepresident de màrqueting o director general.
2.  En el mapa del lloc, seleccioneu **Productes**.
3.  Obriu el producte actiu que voleu canviar i, a la barra d'ordres, seleccioneu **Revisa**.
4.  Al quadre de diàleg **Confirma la revisió**, seleccioneu **Confirma**. Això canviarà l'estat del producte a **En procés de revisió**.
5.  Quan hàgiu acabat de fer els canvis, seleccioneu **Publica** a la barra d'ordres.

    > [!TIP]
    > Per revertir els canvis i continuar amb l'última versió activa del producte, seleccioneu **Reverteix**. Això reverteix l'estat del producte a **Actiu**.

## <a name="clone-a-product"></a>Clonar un producte 

Si heu de crear un producte nou, podeu clonar-ne un d'existent per estalviar temps. La clonació crea una còpia del registre original amb tots els detalls amb l'excepció del nom i l'identificador.

1.  Assegureu-vos que teniu una de les funcions de seguretat o permisos equivalents següents: administrador del sistema, personalitzador del sistema, cap de vendes, vicepresident de vendes, vicepresident de màrqueting o director general.
2.  En el mapa del lloc, seleccioneu **Productes**.
3.  Seleccioneu un registre de producte que voleu clonar i, a la barra d'ordres, seleccioneu **Clona**. Apareix un quadre de diàleg de confirmació.
4.  Seleccioneu **Confirma**.

S'obrirà un nou registre de producte amb els mateixos detalls que l'original, excepte el nom i l'identificador.

## <a name="retire-a-product"></a>Retirada d'un producte 

Si la vostra organització ja no ven un producte, retireu-lo per tal que el producte ja no estigui disponible per als vostres agents de vendes.

1.  Assegureu-vos que teniu la funció Administrador del sistema o Administrador del Sales Professional o permisos equivalents.
2.  En el mapa del lloc, seleccioneu **Productes**.
3.  Obriu el producte actiu que voleu retirar i, a la barra d'ordres, seleccioneu **Retira**.
4.  Al quadre de diàleg **Confirma la retirada**, seleccioneu **Confirma**.


## <a name="delete-a-product"></a>Suprimir un producte

Per deixar de vendre un producte, suprimiu-lo.

> [!IMPORTANT]
> Un registre suprimit no es pot recuperar.

1.  Assegureu-vos que teniu la funció Administrador del sistema o Administrador del Sales Professional o permisos equivalents.
2.  En el mapa del lloc, seleccioneu **Productes**.
3.  Seleccioneu el registre de producte que voleu suprimir i, a la barra d'ordres, seleccioneu **Suprimeix**.
4.  Al quadre de diàleg **Confirmació de la supressió**, trieu **Continua**.
 
 ## <a name="quantity-factors-for-products"></a>Factors de quantitat per a productes

Els factors de quantitat admeten la venda de productes basats en subscripcions. Per als productes basats en subscripcions, la quantitat de l'oferta o la línia de contracte del projecte s'expressa com el nombre de mesos d'usuari.

Normalment, el preu del programari de subscripció s'emmagatzema al catàleg com el preu per usuari i per mes. Tanmateix, podeu utilitzar altres descripcions de temps en el seu lloc. Durant el procés de vendes, el preu de la línia d'oferta sol ser el preu per usuari per mes que ha estat negociat i descomptat per l'agent de vendes de TI. Cada operació té un nombre diferent d'usuaris i un nombre diferent de mesos de subscripció. La quantitat que s'utilitza per calcular la quantitat de la línia d'oferta és un producte del nombre d'usuaris i el nombre de mesos de subscripció.

Els factors de quantitat depenen dels atributs del producte. Quan configureu propietats específiques per a un producte, podeu marcar un subconjunt d'aquestes propietats, o bé totes les propietats, com a factors de quantitat.

El sistema valida que només les propietats numèriques o les propietats dels productes que tenen un tipus de dades numèric es marquen com a factors de quantitat. Quan un producte amb factors de quantitat configurats s'afegeix a una línia d'oferta, el camp **Quantitat** de la línia d'oferta es converteix en un camp de només de lectura. Després d'introduir els valors per a les propietats dels productes que són factors de quantitat, es calcula la quantitat de la línia d'oferta.

Per exemple, si hi ha les propietats següents: 

- **Nombre d'usuaris**: el nombre d'usuaris 
- **Nombre de mesos**: el nombre de mesos de subscripció
- **SKU de producte** 

Les propietats **Nombre d'usuaris** i **Nombre de mesos** es poden marcar com a factors de quantitat per editar les propietats de la línia de productes. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]