---
title: Despeses amb el mòbil
description: En aquest tema es proporciona informació l'administració de despeses amb l'àrea de treball mòbil.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3185c80c792dfe537f4974fa276eafbd16813131
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897034"
---
# <a name="expense-using-mobile"></a>Despeses amb el mòbil

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

En aquest tema es proporciona informació l'àrea de treball mòbil **Administració de despeses**. Aquesta àrea de treball permet que els usuaris capturin i carreguin un rebut per tal que el puguin adjuntar a un informe de despeses més endavant. Els usuaris també poden crear ràpidament una línia de despesa mitjançant un rebut adjunt i crear i administrar els informes de despeses. A més, els aprovadors poden utilitzar l'àrea de treball mòbil **Administració de despeses** per veure els informes de despeses que se'ls assignin i aprovar o rebutjar aquests informes de despeses.

Aquesta àrea de treball mòbil està dissenyada per utilitzar-se amb l'aplicació mòbil Dynamics 365 Unified Ops.

Moltes organitzacions requereixen que s'adjunti una còpia d'un rebut a un informe de despeses relacionat amb una despesa de viatge o de negocis que un empleat envia per al reemborsament. L'àrea de treball mòbil **Administració de despeses** permet que els usuaris creïn ràpidament noves línies de despeses al dispositiu mòbil de la seva elecció mitjançant una foto adjunta d'un rebut. D'altra banda, els usuaris poden capturar una foto d'un rebut i després adjuntar-la a un informe de despeses més endavant. Els empleats també poden crear i administrar els informes de despeses i, a continuació, enviar-los per a la seva aprovació i reemborsament mitjançant el dispositiu mòbil.

Específicament, l'àrea de treball mòbil **Administració de despeses** permet que els usuaris realitzin aquestes tasques:

- Fer una foto d'un rebut. Carregar la foto del rebut i adjuntar-la a un informe de despeses més endavant.
- Carregar un fitxer com a rebut capturat. A continuació, podeu adjuntar aquest fitxer a un informe de despeses més endavant.
- Crear una línia de cost nova mitjançant un rebut adjunt. A continuació, podeu afegir l'element de la línia a un informe de despeses més endavant i enviar-lo per a la seva aprovació i reemborsament.

També podeu utilitzar aquestes característiques:

- Crear un informe de despeses nou.
- Adjuntar transaccions de targeta de crèdit i altres despeses creades prèviament a un informe de despeses.
- Crear despeses noves per a un informe de despeses.
- Adjuntar un rebut a qualsevol despesa per a un informe de despeses, o bé, fent una foto del rebut o carregant un fitxer com a rebut capturat.
- En funció de la norma de despeses de l'empresa, afegir la llista de convidats a una despesa.
- En funció de la norma de despeses de l'empresa, desglossar les despeses.
- Enviar un informe de despeses per a la seva aprovació i reemborsament.
- Aprovar o rebutjar els informes de despeses en què sou un aprovador assignat.

## <a name="prerequisites"></a>Requisits previs
Els prerequisits difereixen, segons la versió que s'hagi implementat per a la vostra organització.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Requisits previs si utilitzeu el Dynamics 365 Finance 
Si el Finance s'ha implementat per a la vostra organització, l'administrador del sistema ha de publicar l'àrea de treball mòbil **Administració de despeses**. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Requisits previs si utilitzeu la versió 1611 amb l'actualització de la plataforma 3 o posterior
Si la versió 1611 amb l'actualització de la plataforma 3 o posterior s'ha implementat per a la vostra organització, l'administrador del sistema ha de completar els requisits previs següents. 

<table>
<thead>
<tr class="header">
<th>Requisit previ</th>
<th>Funció</th>
<th>Descripció</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implementeu la 4019015 KB.</td>
<td>Administrador del sistema</td>
<td>La KB 4019015 és una actualització d'X++ o correcció de les metadades que conté l'àrea de treball mòbil <strong>Administració de despeses</strong>. Per implementar la 4019015 KB, l'administrador del sistema ha de seguir aquests passos.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Baixeu les actualitzacions del Lifecycle Services</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Instal·leu la correcció de metadades</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Creeu un paquet implementable</a> que contingui els models <strong>ApplicationSuite</strong> i <strong>ExpenseMobile</strong> i, a continuació, carregueu el paquet implementable al LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Apliqueu el paquet implementable</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publiqueu l'àrea de treball mòbil <strong>Administració de despeses</strong>.</td>
<td>Administrador del sistema</td>
<td>Vegeu <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publicar una àrea de treball mòbil</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Baixar i instal·lar l'aplicació mòbil del Dynamics 365 Unified Ops
Baixeu i instal·leu l'aplicació mòbil del Dynamics 365 Unified Ops:

- [Per a telèfons Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Per a iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Iniciar la sessió a l'aplicació mòbil
1. Inicieu l'aplicació al dispositiu mòbil.
2. Introduïu l'URL del Dynamics 365.
4. La primera vegada que inicieu la sessió, se us demanarà el vostre nom d'usuari i la vostra contrasenya. Introduïu les vostres credencials.
5. Després d'iniciar la sessió, es mostren les àrees de treball disponibles per a la vostra empresa. Si l'administrador del sistema publica una àrea de treball nova més tard, haureu d'actualitzar la llista d'àrees de treball mòbils.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturar un rebut mitjançant l'àrea de treball mòbil Administració de despeses

1. Al dispositiu mòbil, obriu l'àrea de treball **Administració de despeses**.
2. Seleccioneu **Captura el rebut**.
3. Seleccioneu **Fes una foto** o **Tria una imatge**.
4. Seguiu un d'aquests passos:

   - Si heu seleccionat **Fes una foto**, seguiu aquests passos:

      1. Se us dirigirà a la càmera del dispositiu mòbil per tal que pugueu fer una foto del rebut. 
      2. Quan hàgiu acabat de fer una foto, seleccioneu **D'acord** per acceptar la foto.
      3. Opcional: introduïu un nom per a la foto i introduïu-hi les notes.

    - Si heu seleccionat **Tria una imatge**, seguiu aquests passos:

        1. Seleccioneu una imatge de la llista.
        2. Opcional: introduïu un nom per a la imatge i introduïu-hi les notes.

5. Seleccioneu **Fet**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Introduir ràpidament les despeses mitjançant l'àrea de treball mòbil Administració de despeses

1. Al dispositiu mòbil, obriu l'àrea de treball **Administració de despeses**.
2. Seleccioneu **Entrada ràpida de despesa**.
3. Seleccioneu la categoria de despesa. Veureu una llista de categories de despesa que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si la categoria no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per categoria de despesa o canvieu a la cerca per tipus de despesa.
4. Introduïu la data de la transacció de la despesa.
5. Opcional: introduïu el comerciant per a la despesa.
6. Escriviu l'import de la despesa.
7. Seleccioneu la moneda de la despesa. Veureu una llista de codis de moneda que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 400 monedes, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si la moneda no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per moneda o canvieu a la cerca per nom.
8. Seleccioneu **Fes una foto** o **Tria una imatge**.
9. Seguiu un d'aquests passos:

    - Si heu seleccionar **Fes una foto**, se us dirigirà a la càmera del dispositiu mòbil per tal que pugueu fer una foto del rebut. Quan hàgiu acabat de fer una foto, seleccioneu **D'acord** per acceptar la foto.
    - Si heu seleccionat **Tria una imatge**, seleccioneu una imatge a la llista.

10. Seleccioneu **Fet**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Aprovar un informe de despeses mitjançant l'àrea de treball mòbil Administració de despeses (si utilitzeu l'actualització de juliol de 2017)

1. Al dispositiu mòbil, obriu l'àrea de treball **Administració de despeses**.
2. **Aprovacions de despeses** mostra el nombre d'informes de despeses que teniu assignats per a la seva aprovació. El nombre s'actualitza aproximadament cada 30 minuts. Seleccioneu **Aprovacions de despeses**.

    Es mostra la llista d'informes de despeses que teniu assignats per a la seva aprovació.
    
3. Seleccioneu un informe de despeses per veure els detalls de la despesa.
4. Seleccioneu una despesa per veure'n els detalls. La informació que es mostra per a una despesa inclou tots els detalls del rebut, convidats i desglossament.
5. A la pàgina **Informe de despeses**, seleccioneu si aproveu o rebutgeu l'informe de despeses.
6. Introduïu qualsevol comentari per a l'acció d'aprovació.
7. Seleccioneu **Fet**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Crear un informe de despeses nou i enviar-lo per a l'aprovació mitjançant l'àrea de treball mòbil Administració de despeses (si utilitzeu l'actualització de juliol de 2017)

1. Al dispositiu mòbil, obriu l'àrea de treball **Administració de despeses**.
2. Seleccioneu **Entrada de despesa**.
3. Seleccioneu **Informe nou** o seleccioneu un informe de despesa existent a la llista.
4. Per a informes de despeses nous, introduïu la finalitat i qualsevol informació addicional que estigui disponible. Aquesta informació varia segons com es configuri l'administració de despeses per a l'empresa.
5. Seleccioneu **Fet**.
6. Per afegir despeses existents, com ara transaccions amb targeta de crèdit, a l'informe de despeses, seleccioneu **Adjunta**.
7. A la llista, seleccioneu una o més despeses.
8. Seleccioneu **Fet**.
9. Per afegir una nova despesa a l'informe de despeses, seleccioneu **Despesa nova**.
10. Seleccioneu la categoria de la despesa. Veureu una llista de categories de despesa que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si la categoria no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per categoria de despesa o canvieu a la cerca per tipus de despesa.
11. Opcional: introduïu el comerciant per a la despesa.
12. Introduïu la data de la transacció de la despesa.
13. Escriviu l'import de la despesa.
14. Seleccioneu la moneda de la despesa. Veureu una llista de codis de moneda que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 400 monedes, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si la moneda no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per moneda o canvieu a la cerca per nom.
15. Seleccioneu **Fet**.
16. Per afegir més detalls a la despesa, seleccioneu **Afegeix més detalls**. Els camps que estan disponibles depenen de la configuració de l'administració de despeses per a la vostra empresa.
17. Si la norma de l'empresa requereix un rebut per a la despesa, seleccioneu **Rebuts** i seguiu aquests passos:

    1. Seleccioneu **Captura un rebut** o **Adjunta un rebut**.
    2. Seguiu un d'aquests passos:

        - Si heu seleccionat **Captura un rebut**, seguiu aquests passos:

            1. Seleccioneu **Fes una foto** o **Tria una imatge**.
            2. Seguiu un d'aquests passos:

                - Si heu seleccionat **Fes una foto**, seguiu aquests passos:

                    1. Se us dirigirà a la càmera del dispositiu mòbil per tal que pugueu fer una foto del rebut. Quan hàgiu acabat de fer una foto, seleccioneu **D'acord** per acceptar la foto.
                    2. Opcional: introduïu un nom per a la foto i introduïu-hi les notes.

                - Si heu seleccionat **Tria una imatge**, seguiu aquests passos:

                    1. Seleccioneu una imatge de la llista.
                    2. Opcional: introduïu un nom per a la imatge i introduïu-hi les notes.

            3.  Seleccioneu **Fet**.

        - Si heu seleccionat **Adjunta un rebut**, seguiu aquests passos:

            1.  A la llista, seleccioneu una o més imatges.
            2.  Seleccioneu **Fet**.

    3. Seleccioneu el botó **Enrere** per tornar als detalls de la despesa.

18. Si la norma de l'empresa requereix els convidats per a la despesa, seleccioneu **Convidats** i seguiu aquests passos:

    1. Seleccioneu **Convidat**, **Convidats anteriors** o **Companys de feina**.
    2. Seguiu un d'aquests passos:

        - Si heu seleccionat **Convidat**, seguiu aquests passos:

            1. Introduïu el nom del convidat.
            2. Opcional: introduïu l'organització i/o el país del convidat.
            3. Opcional: introduïu el càrrec del convidat.
            4. Seleccioneu **Fet**.

        - Si heu seleccionat **Convidats anteriors**, seguiu aquests passos:

            1. A la llista, seleccioneu un o diversos convidats anteriors. Podeu veure una llista dels convidats anteriors que heu afegit a informes de despeses anteriors carregats a l'aplicació per utilitzar-los fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si el convidat anterior no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per nom, o canvieu a la cerca per organització, país o càrrec.
            2. Seleccioneu **Fet**.

        - Si heu seleccionat **Companys de feina**, seguiu aquests passos:

            1. A la llista, seleccioneu un o més companys de feina. Veureu una llista de companys de feina que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si el company de feina no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu per nom, o canvieu a la cerca per empresa o càrrec.
            2. Seleccioneu **Fet**.

    3. Seleccioneu el botó **Enrere** per tornar als detalls de la despesa.

19. Si la norma de l'empresa requereix que la despesa es desglossi, seleccioneu **Desglossa** i seguiu aquests passos:

    1. Seleccioneu la primera data que es desglossarà.
    2. Seleccioneu **Afegeix un desglossament**.
    3. Seleccioneu la subcategoria del desglossament de la despesa. Veureu una llista de subcategories de despesa que s'han carregat a la vostra aplicació per a l'ús fora de línia. Per defecte, es carreguen 50 elements, però un desenvolupador pot canviar aquest número. Per obtenir més informació, els desenvolupadors haurien de consultar [Plataforma mòbil](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si la subcategoria no es troba a la llista, seleccioneu **Cerca** per fer una cerca en línia. Cerqueu pel nom de la subcategoria de despesa.
    4. Introduïu l'import de la transacció per al desglossament.
    5. Editeu la data de la transacció si cal.
    6. Seleccioneu **Fet**.
    7. Repetiu els passos anteriors fins que hàgiu acabat d'afegir tots els desglossaments per a la data seleccionada.
    8. Per als dies addicionals, podeu seleccionar **Copia al dia següent** per copiar el desglossament al dia següent. O bé, podeu seleccionar la data de desglossament i, a continuació, afegir-hi desglossaments com heu fet per a la primera data.
    9. Després d'haver acabat de desglossar la despesa, seleccioneu el botó **Enrere** per tornar als detalls de la despesa.

20. Seleccioneu el botó **Enrere** per tornar a la pàgina **Informe de despeses**.
21. Repetiu els passos anteriors fins que hàgiu acabat d'afegir totes les despeses.
22. Seleccioneu **Envia**.
23. Introduïu qualsevol comentari per a l'aprovador.
24. Seleccioneu **Fet**.
