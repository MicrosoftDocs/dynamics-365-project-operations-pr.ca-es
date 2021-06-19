---
title: Creació de factures entre empreses de clients i proveïdors
description: En aquest tema es proporciona informació sobre com crear factures de proveïdor i de client interempresa.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: eb9e49fee4d4a52ec53e0919c2d32c224f04df66
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010954"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Creació de factures entre empreses de clients i proveïdors

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Un comptable del projecte d'una entitat jurídica prestadora crea una factura de client interempresa per als costos del projecte que s'estan transferint a l'entitat prestatària. Després que s'aprovi i publiqui la factura de client interempresa, l'entitat jurídica prestadora envia la factura interempresa a l'entitat jurídica prestatària.

El comptable del projecte per a l'entitat jurídica prestadora pot configurar un procés per lots per generar factures interempresa de manera periòdica. El comptable del projecte especifica els criteris, com ara projectes específics, per crear factures interempresa en un lot.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Creació manual d'una factura de client interempresa per a transaccions de projecte 

Utilitzeu aquest procediment per crear manualment una factura de client interempresa per a transaccions de projecte. Cerqueu hores comptabilitzades pels treballadors en projectes de les entitats jurídiques prestatàries i despeses en què ha incorregut la vostra entitat jurídica en nom d'entitats jurídiques prestatàries. Podeu fer cerques per nom d'entitat jurídica, número de contracte de projecte, número de projecte, interval de dates o qualsevol combinació d'aquestes opcions. Als resultats de la cerca, seleccioneu les transaccions que voleu afegir a una factura interempresa. 

Cal fer els passos següents a l'entitat jurídica prestadora. 

1. Al Dynamics 365 Finance, aneu a **Gestió de projectes i comptabilització** > **Factures del projecte** > **Factures de client interempresa**. A la pàgina de **Factures de clients interempresa**, a la subfinestra d'Acció, seleccioneu **Crea**.
2. A la pàgina **Crea una factura interempresa**, al camp **Entitat jurídica**, seleccioneu una entitat jurídica prestatària.
3. Opcional: introduïu un contracte de projecte i un número de projecte específics.
4. Restringiu la cerca seleccionant un interval de dates. Introduïu dates específiques als camps **Data d'inici** i **Data de finalització**. Només les transaccions entre empreses que es publiquen dins d'aquest interval de dates es visualitzen als resultats de la cerca.
5. Definiu el **Paràmetre de línia de diari avançada del projecte** en **Sí** i seleccioneu **Cerca**.
6. Als resultats de la cerca, seleccioneu les transaccions que voleu incloure a la proposta de factura entre empreses i, a continuació, seleccioneu **D'acord**.
7. A la pàgina **Factura de client interempresa**, es mostren les transaccions de projecte entre empreses que heu seleccionat als resultats de la cerca. Per modificar les transaccions abans d'enviar la factura a l'entitat jurídica prestatària, feu el següent:
  
    1. A la pàgina **Factura de client entre empreses**, obriu els detalls de la factura i, a continuació, seleccioneu **Afegeix línia**.
    2. Per suprimir una línia, seleccioneu-la i feu clic a **Suprimeix**.
    3. Visualitzeu els comentaris, les raons, les mesures financeres i altres dades sobre una línia seleccionada als detalls de la línia de factura.
    
8. Per publicar la factura de client interempresa, a la subfinestra d'Acció, seleccioneu **Publica**.

> [!NOTE]
> Si l'organització requereix que es revisin les factures entre empreses abans que es publiquin, un administrador del sistema podria configurar un flux de treball per a factures entre empreses. Si no hi ha configurat un flux de treball per a les factures entre empreses, podeu publicar la factura.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Creació d'una feina per lots per a les factures entre empreses

Podeu crear diverses factures entre empreses al mateix temps per a totes les entitats jurídiques prestatàries. Mitjançant la funcionalitat de cerca, podeu per exemple cercar totes les transaccions que siguin publicades pels treballadors prestats i que estiguin relacionades amb projectes gestionats per altres entitats jurídiques. A continuació, per a cada entitat jurídica prestatària, podeu crear una factura entre empreses per a les transaccions proporcionades als resultats de la cerca.

1. Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Factures del projecte** > **Crear factures de client interempresa**.
2. A la pàgina **Crea factures de client interempresa**, al camp **Empresa**, seleccioneu una entitat jurídica a la qual facturar. Si no seleccioneu cap empresa, es visualitzen totes les transaccions que compleixen els criteris de cerca per a totes les entitats jurídiques prestatàries.
3. A **Crea una factura per**, seleccioneu si voleu crear una factura per a transaccions entre empreses basada en un projecte o en una entitat jurídica prestatària.
4. Opcional: per seleccionar un projecte i un contracte de projecte específics per crear factures entre empreses, feu clic a **Selecciona**. A la pàgina **Consulta**, al camp **Criteris**, seleccioneu el contracte de projecte, el número de projecte o tots dos i, a continuació, seleccioneu **D'acord**.
5. A la pestanya **Per lots**, configureu un procés per lots per crear factures entre empreses de manera periòdica. Per obtenir més informació, vegeu [Enviar una feina de processament per lots des d'un formulari](/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Per publicar les factures entre empreses, a la subfinestra d'Acció, seleccioneu **Publica**.

> [!NOTE]
> Si l'organització requereix que es revisin les factures entre empreses abans que es publiquin, un administrador del sistema podria configurar un flux de treball per a factures entre empreses. Si no hi ha configurat un flux de treball per a les factures entre empreses, podeu publicar les factures.

## <a name="post-the-intercompany-vendor-invoice"></a>Publicar la factura de proveïdor interempresa

Un comptable del projecte de l'entitat jurídica prestatària pot revisar les factures de proveïdor interempresa pendents quan es comptabilitza la factura de client interempresa corresponent. A Finances, a l'entitat jurídica prestatària, aneu a **Compte a pagar** > **Factures** > **Factura de proveïdor pendent**. El número de factura pendent coincidirà amb el número de factura de client interempresa. Verifiqueu que la factura és correcta i després publiqueu-la. La publicació de la factura de proveïdor interempresa crea un subllibre de projecte i un llibre major que reflecteix els costos de transacció a l'entitat jurídica prestatària.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
