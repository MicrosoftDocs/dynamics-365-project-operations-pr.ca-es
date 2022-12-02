---
title: Llibre diari d'integració del Project Operations
description: Aquest article proporciona informació sobre com treballar amb el diari d'integració al Project Operations.
author: sigitac
ms.date: 09/22/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e947fe895a1caa9c9ea092597957a859cd8d61c9
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541065"
---
# <a name="integration-journal-in-project-operations"></a>Llibre diari d'integració del Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Les entrades de temps, despesa, tarifa i material creen transaccions de **Valor real** que representen la visualització operativa del treball completat en relació amb un projecte. El Dynamics 365 Project Operations proporciona als comptables una eina per revisar les transaccions i ajustar els atributs comptables segons calgui. Un cop finalitzada la revisió i els ajustos, les transaccions es comptabilitzen al llibre diari del projecte i al llibre diari general. Un comptable pot realitzar aquestes activitats a través del diari **Integració del Project Operations** (**Dynamics 365 Finance** > **Administració de projectes i comptabilitat** > **Diaris** > **Integració del Project Operations**.

![Flux del diari d'integració.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear registres al diari d'integració del Project Operations

Els registres al diari d'integració del Project Operations es creen mitjançant un procés periòdic, **Importa de la taula intermèdia**. Podeu executar aquest procés anant a **Dynamics 365 Finance** > **Administració de projectes i comptabilitat** > **Periòdic** > **Integració del Project Operations** > **Importa d'una taula intermèdia**. Podeu executar el procés de manera interactiva o configurar el procés perquè s'executi en segon pla segons calgui.

Quan s'executa el procés periòdic, es troben els valors reals que encara no s'han afegit al diari d'integració del Project Operations. Es crea una línia del llibre diari per a cada transacció real.
El sistema agrupa les línies de diari en diaris separats en funció del valor seleccionat en el camp **Unitat periòdica al diari d'integració del Project Operations** (**Finance** > **Administració de projectes i comptabilitat** > **Configuració** > **Paràmetres de l'administració de projectes i la comptabilitat**, pestanya **Project Operations al Dynamics 365 Customer Engagement**). Els valors possibles per a aquest camp inclouen:

  - **Dies**: els valors reals s'agrupen per data de transacció. Es crea un diari separat per a cada dia.
  - **Mesos**: els valors reals s'agrupen per mes natural. Es crea un diari separat per a cada mes.
  - **Anys**: els valors reals s'agrupen per any natural. Es crea un diari separat per a cada any.
  - **Totes**: totes les transaccions de valors reals s'inclouen en el mateix diari d'integració. Si el diari no està disponible quan s'executa el procés periòdic; per exemple, si el diari està en procés de publicar transaccions, es crea un diari nou.

Les línies del llibre diari es creen a partir dels valors reals del projecte. La llista següent inclou algunes de les regles per defecte i de transformació més notables:

  - Cada transacció de valor real del projecte té una línia al diari d'integració del Project Operations. Les transaccions de costos i vendes no facturades per al tipus de facturació de temps i material es mostren en línies separades.
  - El camp **Data** representa la data de la transacció. El camp **Data comptable** representa la data en què es registra l'operació al llibre comptable. Si la data comptable es troba en un [període financer tancat](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end) i el paràmetre **Estableix automàticament la data comptable al període del llibre comptable obert** s'estableix a la pestanya **Financer** de la pàgina **Paràmetres de l'administració de projectes i comptabilitat**, el sistema ajustarà la data comptable de l'operació a la primera data del pròxim període del llibre comptable obert.
  - El camp **Comprovant** mostra el número de comprovant per a cada transacció real. La seqüència de números de comprovant es defineix a la pestanya **Seqüències numèriques**, a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**. A cada línia se li assigna un número nou. Un cop comptabilitzat el comprovant, podeu veure com es relacionen els costos i les transaccions de vendes no facturades seleccionant **Comprovants relacionats** a la pàgina **Transacció de comprovant**.
  - El camp **Categoria** representa una transacció de projecte i per defecte té el valor en funció de la categoria de transacció del valor real del projecte relacionat.
    - Si **Categoria de transacció** es defineix al valor real del projecte i hi ha una **Categoria de projecte** relacionada en una entitat jurídica determinada, la categoria per defecte és aquesta categoria de projecte.
    - Si **Categoria de transacció** no s'ha definit al valor real del projecte, el sistema utilitza el valor del camp **Valors per defecte de la categoria de projecte** a la pestanya **Project Operations al Dynamics 365 Customer Engagement** de la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.
  - El camp **Recurs** representa el recurs de projecte relacionat amb aquesta transacció. El recurs s'utilitza com a referència a les propostes de factura del projecte als clients.
  - El camp **Tipus de canvi** pren per defecte el **Tipus de canvi de moneda** establert al Dynamics 365 Finance. Si falta la configuració del tipus de canvi, el procés periòdic **Importa de l'intermedi** no afegirà el registre a un diari i s'afegirà un missatge d'error al registre d'execució de la feina.
  - El camp **Propietat de la línia** representa el tipus de facturació als valors reals del projecte. L'assignació de propietats de línia i tipus de facturació es defineix a la pestanya **Project Operations al Dynamics 365 Customer Engagement** a la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.

Només es poden actualitzar els atributs comptables següents a les línies del llibre diari d'integració del Project Operations:

- **Grup d'impostos de les vendes de facturació** i **Grup d'impostos de les vendes d'articles de facturació**
- **Dimensions financeres** (mitjançant l'acció **Distribueix els imports**)

Es poden suprimir les línies del diari d'integració. Amb tot, però qualsevol línia sense comptabilitzar s'inserirà de nou al llibre diari després de tornar a executar el procés periòdic **Importa de l'intermedi**.

### <a name="post-the-project-operations-integration-journal"></a>Publicar el diari d'integració del Project Operations

Quan comptabilitzeu el diari d'integració, es creen transaccions al subdiari del projecte i al diari general. S'utilitzen en la facturació dels clients descendent, el reconeixement d'ingressos i els informes financers.

El diari d'integració amb el Project Operations seleccionat es pot publicar mitjançant **Publica** a la pàgina del diari d'integració del Project Operations. Tots els diaris es poden publicar automàticament executant un procés a **Periódics** > **Integració del Project Operations** > **Publica el diari d'integració del Project Operations**.

La publicació es pot fer de manera interactiva o per lots. Heu de tenir en compte que tots els diaris que tenen més de 100 línies es publicaran automàticament en un lot. Per millorar el rendiment quan es publiquen diaris que tenen moltes línies en un lot, habiliteu la característica **Publica el diari d'integració del Project Operations amb diverses tasques per lots** a l'àrea de treball **Administració de la característica**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferir totes les línies que tenen errors de publicació en un nou diari

> [!NOTE]
> Per utilitzar aquesta capacitat, habiliteu la característica **Transfereix totes les línies amb errors de publicació en un nou diari d'integració del Project Operations** a l'àrea de treball **Administració de la característica**.

Aquesta característica ajuda a millorar l'experiència amb la integració del Project Operations. Quan està habilitat, els problemes de temporització de l'escriptura doble ja no impedeixen la publicació de diaris vàlids. Durant la publicació en el diari d'integració del Project Operations, el sistema valida cada línia del diari. Publica totes les línies que no tenen errors i crea un diari nou per a totes les línies que tenen errors de publicació.

Per revisar els diaris que tenen línies amb errors de publicació, aneu a **Administració de projectes i comptabilitat** \> **Diaris** \> **Diari d'integració del Project Operations** i filtreu la llista de diaris mitjançant el camp **Diari original**. A la il·lustració següent es mostra un exemple en què els diaris de la pàgina **Diari de la integració del Project Operations** s'ha filtrat d'aquesta manera.

![Diari original mostrat a la pàgina del diari d'integració del Project Operations.](./media/transferLines-originalJournal.png)

Si es configura un treball per lots periòdic per publicar el diari d'integració, la publicació es tornarà a intentar i els diaris es publicaran si el problema de temporització s'ha corregit. La resta de diaris s'han d'investigar manualment revisant els registres i realitzant l'acció necessària.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
