---
title: Llibre diari d'integració del Project Operations
description: Aquest article proporciona informació sobre com treballar amb la revista Integration in Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106263"
---
# <a name="integration-journal-in-project-operations"></a>Llibre diari d'integració del Project Operations

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Les entrades de temps, despeses, tarifes i materials creen **transaccions reals** que representen la visió operativa del treball realitzat contra un projecte. El Dynamics 365 Project Operations proporciona als comptables una eina per revisar les transaccions i ajustar els atributs comptables segons calgui. Un cop finalitzada la revisió i els ajustos, les transaccions es comptabilitzen al llibre diari del projecte i al llibre diari general. Un comptable pot realitzar aquestes activitats mitjançant el **diari Project Operations Integration** (**Dynamics 365 Finance** > **Project management and accounting** > **Journals** > **Project Operations Integration** journal.

![Flux del diari d'integració.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Crear registres al diari d'integració del Project Operations

Els registres al diari d'integració del Project Operations es creen mitjançant un procés periòdic, **Importa de la taula intermèdia**. Podeu executar aquest procés anant a **Dynamics 365 Finance** > **Gestió de projectes i comptabilitat d'operacions** > **periòdiques** > **del projecte Integració d'operacions** > **import des de la taula** de posada en escena. Podeu executar el procés de manera interactiva o configurar el procés perquè s'executi en segon pla segons calgui.

Quan s'executa el procés periòdic, es troben els valors reals que encara no s'han afegit al diari d'integració del Project Operations. Es crea una línia del llibre diari per a cada transacció real.
El sistema agrupa les línies de diari en revistes separades en funció del valor seleccionat al camp de la **revista** Period unit on Project Operations Integration (**Finance** > **Project Management and accounting** > **Setup** > **Project management and accounting Accounting Project management and accounting parameters**, **Project Operations on Dynamics 365 Customer Engagement** tab). Els valors possibles per a aquest camp inclouen:

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
    - Si **la categoria** Transaccions no està definida al Projecte real, el sistema utilitza el valor del camp Valors per defecte de la **categoria Projecte a la** pestanya Operacions **del projecte a Dynamics 365 Customer Engagement** de la **pàgina Administració del projecte i paràmetres comptables**.
  - El camp **Recurs** representa el recurs de projecte relacionat amb aquesta transacció. El recurs s'utilitza com a referència a les propostes de factura del projecte als clients.
  - El **camp Tipus de canvi** mor per defecte del tipus **de canvi de** divises establert en Dynamics 365 Finance. Si falta la configuració del tipus de canvi, el procés periòdic **Importa de l'intermedi** no afegirà el registre a un diari i s'afegirà un missatge d'error al registre d'execució de la feina.
  - El camp **Propietat de la línia** representa el tipus de facturació als valors reals del projecte. La propietat de línia i l'assignació del tipus de facturació es defineixen a la **pestanya Operacions del projecte a Dynamics 365 Customer Engagement** de la **pàgina Administració del projecte i paràmetres comptables**.

Només es poden actualitzar els atributs comptables següents a les línies del llibre diari d'integració del Project Operations:

- **Grup d'impostos de les vendes de facturació** i **Grup d'impostos de les vendes d'articles de facturació**
- **Dimensions financeres** (mitjançant l'acció **Distribueix els imports**)

Les línies de diari d'integració es poden suprimir. Tanmateix, totes les línies no publicades es tornaran a inserir al diari després de tornar a executar el procés d'importació des de la **posada en escena** periòdica.

### <a name="post-the-project-operations-integration-journal"></a>Publicar el diari d'integració d'operacions del projecte

Quan comptabilitzeu el diari d'integració, es creen transaccions al subdiari del projecte i al diari general. S'utilitzen en la facturació dels clients descendent, el reconeixement d'ingressos i els informes financers.

El diari d'integració del Project Operations seleccionat es pot publicar mitjançant **Post** a la pàgina del diari d'integració project operations. Totes les revistes es poden publicar automàticament executant un procés a **la revista** > **d'integració** > **post Project Operations de Periodics** Project Operations.

La publicació es pot realitzar de manera interactiva o per lots. Tingueu en compte que totes les revistes que tinguin més de 100 línies es publicaran automàticament en un lot. Per obtenir un millor rendiment quan les revistes que tenen moltes línies es publiquen en un lot, habiliteu el diari d'integració **Post Project Operations mitjançant la funció de diverses tasques** per lots a l'espai **de treball de gestió** de funcions. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transferiu totes les línies que tenen errors de publicació a una nova revista

> [!NOTE]
> Per utilitzar aquesta capacitat, habiliteu Transferir totes les **línies amb la publicació d'errors a una nova funció de diari** d'integració del Project Operations a l'espai de treball De gestió **de** funcions.

Durant la publicació al diari d'integració project operations, el sistema valida totes les línies de la revista. El sistema publica totes les línies que no tenen errors i crea un nou diari per a totes les línies que tenen errors de publicació. Per revisar les revistes que tenen línies d'error de publicació, aneu a **Gestió de projectes i comptabilitat** > **Revista d'integració** > **de Project** Operations i filtreu les revistes mitjançant el camp Original de la **revista**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
