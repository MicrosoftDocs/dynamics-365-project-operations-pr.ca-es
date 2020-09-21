---
title: Facturació entre empreses
description: En aquest article es proporciona informació i exemples sobre la facturació entre empreses per als projectes.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749439"
---
# <a name="intercompany-invoicing"></a>Facturació entre empreses

[!include [banner](../includes/banner.md)]

En aquest article es proporciona informació i exemples sobre la facturació entre empreses per als projectes.

La vostra organització pot tenir diverses divisions, filials i altres entitats jurídiques que es transfereixen productes i serveis entre si per als projectes. L'entitat jurídica que proporciona el servei o producte s'anomena *entitat jurídica prestadora* i l'entitat jurídica que rep el servei o producte s'anomena *entitat jurídica prestatària*. 

A la il·lustració següent es mostra un escenari típic on hi ha dues entitats jurídiques, SI FR (l'entitat legal prestatària) i SI USA (l'entitat legal prestadora), que comparteixen recursos per lliurar un projecte per al client A. Per a aquest escenari, SI FR es contracta per lliurar el treball al client A. 

[![Exemple de facturació entre empreses](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

L'objectiu és fer que el control de costos, el reconeixement d'ingressos, els impostos i el preu de transferència per a les transaccions de projecte entre empreses siguin més flexibles i potents. A més, es proporcionen les capacitats següents:

-   Crear factures de clients en un projecte d'una entitat legal prestatària mitjançant l'ús de fulls horaris, despeses i factures de proveïdors entre empreses en una entitat legal prestadora.
-   Donar suport als càlculs fiscals i els costos indirectes.
-   Ajornar el reconeixement d'ingressos en una entitat legal prestadora i quan una entitat legal prestatària hauria de reconèixer el cost.
-   Acumular ingressos de treball en curs (WIP) a l'entitat legal prestadora.
-   Definiu els preus de transferència, que es poden basar en diversos models de preu. A continuació trobareu alguns exemples:
    -   **Quantitat**: la quantitat que introduïu al camp **Preu** és el cost real per quantitat o unitat.
    -   **Import dels càrrecs**: el preu i cost per transacció més la quantitat de despeses que introduïu al camp **Preu**.
    -   **Percentatge de càrrecs**: el preu de la transferència és el preu i el cost per transacció multiplicat pel percentatge de càrrecs que introduïu en el camp **Preus**.
    -   **Percentatge del preu de vendes**: percentatge del preu de vendes que es transfereix a l'entitat jurídica prestadora.
    -   **Import per sota de preu de vendes** import que l'entitat legal prestatària reté dels preus de les vendes abans de la transferència a l'entitat legal prestadora.
    -   **Relació de contribució**: el nombre que introduïu en el camp **Preu** és la relació de contribució, que s'expressa com a percentatge del preu de vendes.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Exemple 1: configuració dels paràmetres per a la facturació entre empreses
En aquest exemple, USSI és una entitat legal prestadora i els seus recursos informen del temps per a l'entitat legal prestatària, FRSI, propietària del contracte amb el client final. Les hores i despeses que els empleats d'USSI informen es poden incloure a la factura del projecte que genera FRSI. A més, hi ha un tercer origen de transaccions que es poden originar a partir de l'entitat legal prestadora (USSI en aquest exemple) quan proporciona serveis de proveïdors compartits a les filials (com ara FRSI) i, a continuació, passa aquests costos en projectes dins d'aquestes filials. Tots els documents de factures i els càlculs d'impostos coincidents els completa Finance. 

Per a aquest exemple, FRSI ha de ser client a l'entitat jurídica USSI i USSI ha de ser un proveïdor de l'entitat jurídica FRSI. A continuació, podeu configurar una relació entre empreses entre les dues entitats jurídiques. El procediment següent mostra com configurar els paràmetres per tal que ambdues entitats jurídiques puguin participar en la facturació entre empreses.

1. Configurar FRSI com a client a l'entitat jurídica USSI i configurar USSI com a proveïdor a l'entitat jurídica FRSI. Hi ha tres punts d'entrada per als passos necessaris per a aquesta tasca.

   | Pas |                                                       Punt d'entrada                                                        |                                                                                                                                                                                               Descripció                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | A USSI, feu clic a <strong>Compte a cobrar</strong> &gt; <strong>Clients</strong> &gt; <strong>Tots els clients</strong>. |                                                                                                                                                                  Creeu un registre de client nou per a FRSI i seleccioneu el grup de clients.                                                                                                                                                                  |
   |  N   |    A FRSI, feu clic a <strong>Compte a pagar</strong> &gt; <strong>Proveïdors</strong> &gt; <strong>Tots els proveïdors</strong>.     |                                                                                                                                                                    Creeu un registre de proveïdor nou per a USSI i seleccioneu el grup de proveïdors.                                                                                                                                                                    |
   |  C   |                                  A FRSI, obriu el registre del proveïdor que acabeu de crear.                                  | A la subfinestra d'acció, a la pestanya <strong>General</strong>, al grup <strong>Configura</strong>, feu clic a <strong>Entre empreses</strong>. A la pàgina <strong>Entre empreses</strong>, a la pestanya <strong>Relació comercial</strong>, definiu el control lliscant <strong>Actiu</strong> a <strong>Sí</strong>. Al camp <strong>Empresa del client</strong>, seleccioneu el registre de client que heu creat en el pas A. |


2. Feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Paràmetres d'administració de projectes i comptabilitat** i, a continuació, feu clic a la pestanya **Entre empreses** . La manera de configurar els paràmetres depèn de si sou l'entitat jurídica prestatària o l'entitat jurídica prestadora.
   -   Si sou l'entitat jurídica prestatària, seleccioneu la categoria de contractació que s'ha d'utilitzar per assignar les factures dels proveïdors, que es generen automàticament.
   -   Si sou l'entitat jurídica prestadora, per a cada entitat prestatària, seleccioneu una categoria de projecte per defecte per a cada tipus de transacció. Les categories de projecte s'utilitzen per a la configuració tributària quan la categoria facturada a les transaccions entre empreses només existeix a l'entitat jurídica prestatària. Podeu triar acumular els ingressos per a les transaccions entre empreses. Aquesta acumulació es fa quan es publiquen les transaccions i, a continuació, s'inverteix quan es comptabilitza la factura entre empreses.

3. Feu clic a **Administració de projectes i comptabilitat** &gt; **Configuració** &gt; **Preus** &gt; **Preu de transferència**.
4. Seleccioneu una moneda, un tipus de transacció i un model de preu de transferència. La moneda que s'utilitza a la factura és la moneda configurada al registre de client per a l'entitat jurídica prestatària a l'entitat jurídica prestadora. La moneda s'utilitza per fer coincidir les entrades de la taula de preus de transferència.
5. Feu clic a **Llibre major general** &gt; **Configuració de la comptabilització** &gt; **Comptabilitat entre empreses** i configureu una relació per a USSI i FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Exemple 2: creació i publicació d'un full d'hores entre empreses
USSI, l'entitat jurídica prestadora, ha de crear i comptabilitzar el full d'hores per a un projecte de FRSI, l'entitat jurídica prestatària. Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.

| Pas | Punt d'entrada                                                                       | Descripció                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Administració de projectes i comptabilitat** &gt; **Fulls d'hores** &gt; **Tots els fulls d'hores** | Creeu un full d'hores nou. A la línia del full d'hores, al camp **Entitat jurídica**, seleccioneu **FRSI**. Al camp **ID del projecte**, seleccioneu el projecte a FRSI. Introduïu les hores per a cada dia de la setmana. |
| N    | Pàgina **Full d'hores**                                                                | Quan el flux de treball s'executi, publiqueu el full d'hores i anoteu el número del val.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Exemple 3: creació i publicació d'una factura a un proveïdor entre empreses
USSI, l'entitat jurídica prestadora, ha de crear i comptabilitzar la factura per a un proveïdor entre empreses per a un projecte de FRSI, l'entitat jurídica prestatària. Aquesta factura de proveïdor representa el treball i les despeses externalitzats que han realitzat els proveïdors pagats per USSI. Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.

| Pas | Punt d'entrada                                                                                      | Descripció                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Comptes a pagar** &gt; **Factures** &gt; **Factures de proveïdors obertes** &gt; **Nova factura de proveïdor** | Creeu una factura de proveïdor nova i introduïu els serveis que s'han fet en el projecte de FRSI.                                                                                                                                                                                  |
| N    | La pàgina **Factura de proveïdor**                                                                      | Introduïu les línies que representen els serveis externalitzats en nom de FRSI. A FastTab **Detalls de la línia**, a la pestanya **Projecte** de la línia de factura, al camp **Empresa del projecte**, introduïu **FRSI**. Introduïu el projecte i la informació corresponent. A continuació, comptabilitzeu la factura del proveïdor. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Exemple 4: creació i publicació de la factura entre empreses
USSI, l'entitat jurídica prestadora, ha de crear i publicar la factura entre empreses. Hi ha dos punts d'entrada per als passos necessaris per a aquesta tasca.

| Pas | Punt d'entrada                                                                                             | Descripció                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factura de client entre empreses**  | Feu clic a **Nou** per obrir la pàgina **Crea una factura entre empreses**.                                                                                  |
| N    | **Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factures de client entre empreses** | A la pàgina **Crea una factura entre empreses**, introduïu l'entitat jurídica, especifiqueu la transacció que s'ha d'incloure i, a continuació, feu clic a **Cerca**. |
| C    | **Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Factures de client entre empreses** | Seleccioneu les transaccions que voleu facturar o feu clic a **Selecciona-ho tot** per facturar totes les transaccions a la llista i, a continuació, feu clic a **D'acord**.                  |
| D    | La pàgina **Factura entre empreses**                                                                       | Es mostra la proposta de factura de client entre empreses.                                                                                             |
| E    | La pàgina **Factura entre empreses**                                                                       | Feu clic a **Comptabilitza**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Exemple 5: comptabilització de la factura del proveïdor i facturació al client
Quan l'entitat jurídica prestadora, USSI, comptabilitza la factura del client entre empreses, es crea una factura de proveïdor pendent coincident a l'entitat jurídica prestatària, FRSI. Un cop comptabilitzada aquesta factura del proveïdor, FRSI també factura al client del projecte les hores que ha introduït USSI. Hi ha tres punts d'entrada per als passos necessaris per a aquesta tasca.

| Pas | Punt d'entrada                                                                                        | Descripció                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Comptes a pagar** &gt; **Factures** &gt; **Factures de proveïdors pendents**                            | Reviseu la factura per comprovar que s'inclouen els valors del full d'hora i, a continuació, comptabilitzeu la factura del proveïdor.                  |
| N    | **Administració de projectes i comptabilitat** &gt; **Factures del projecte** &gt; **Propostes de factura del projecte** | Creeu una factura de projecte nova per al projecte i verifiqueu que es mostrin les transaccions d'hora que s'han comptabilitzat.            |
| C    | La pàgina **Factura del projecte**                                                                       | Seleccioneu la factura del projecte i, a continuació, feu clic a **Visualitza els detalls** per revisar l'import del cost i de les vendes. A continuació, comptabilitzeu la factura. |


Per obtenir més informació, vegeu [Configurar la facturació del projecte entre empreses](tasks/configure-intercompany-project-invoicing.md).


