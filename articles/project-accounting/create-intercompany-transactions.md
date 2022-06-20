---
title: Creació de transaccions entre empreses
description: En aquest article s'ofereix informació sobre com crear transaccions interempresases.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: da6fd8e0e6bfe2e2543f5c4a453ed769e412f1e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919358"
---
# <a name="create-intercompany-transactions"></a>Creació de transaccions entre empreses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Les transaccions entre empreses són transaccions de temps i de despeses d'un contracte de projecte que pertany a una empresa o unitat d'organització, mentre que els recursos del contracte de projecte formen part d'una altra empresa o unitat d'organització.

Quan s'aprova una transacció entre empreses, es creen les operacions reals següents

| **Tipus de transacció** | **Llista de preus aplicada** | **Moneda de transacció** |
| --- | --- | --- |
| Cost | Llista de preus de cost de la unitat de contractació | Moneda de la línia de preu |
| Vendes no facturades. Aquestes es creen només per als valors reals que estan associats amb una línia de contracte amb el tipus, l'hora i el material de facturació. | Llista de preus de venda de projecte de contracte | Moneda del contracte |
| Cost de la unitat de recursos | Llista de preus de cost de la unitat de recursos | Moneda de la línia de preu |
| Vendes entre unitats d'organització | Llista de preus de cost de la unitat de contractació | Moneda de la línia de preu |

El cost, el cost unitari de recursos i els preus i la moneda de transacció de venda entre unitats d'organització es regeixen per la **unitat d'organització**. Això és important recordar-ho a l'hora de decidir la manera d'estructurar empreses i unitats organitzatives en la implementació.

Quan creeu registres d'oportunitat, oferta, contracte de projecte i projecte, el sistema verifica que la moneda de la unitat de contractació coincideixi amb el moneda comptable de l'empresa contractant. Quan no són iguals, aquests registres no es poden crear. La moneda de la unitat organitzativa es defineix al Dynamics 365 Project Operations anant a **Dataverse** > **Configuració** > **Unitats organitzatives**. La moneda comptable d'una empresa es defineix en Dynamics 365 Finance anant al **Llibre major** > **general de la configuració** > **del llibre major**. La moneda se sincronitza amb l'entorn de Dataverse mitjançant el mapa d'escriptura dual de llibres majors.

El sistema crea costos unitaris de recursos i valors reals de vendes entre unitats d'organització en les situacions següents:

  - Quan la unitat de recursos és diferent de la unitat de contractació
  - Quan l'empresa de recursos és diferent de l'empresa de contractació

No obstant això, només les operacions que tinguin una empresa de recursos diferent de l'empresa contractant es transferiran a l'entorn Dynamics 365 Finance per a una comptabilitat addicional.

La comptabilització per a valors reals del projecte es registra en el diari d'integració de Project Operations a Finances. El sistema crea les línies de diari següents.

| **Tipus de transacció** | **Persona jurídica** | **Crea una transacció de projecte sobre la publicació** | **Valors per defecte de la dimensió financera des de** | **Grup d'impostos de les vendes de facturació i grup d'impostos de les vendes d'element de facturació per defecte** |
| --- | --- | --- | --- | --- |
| Cost | No s'afegeix al diari d'integració | N/D | N/D | N/D |
| Vendes no facturades | El diari d'integració d'entitat jurídica prestatària | Sí | Project | **Grup d'impostos de les vendes de facturació**: segons el **client del contracte** <br/> **Grup d'impostos de les vendes d'element de facturació**: de la categoria de projecte d'entitat jurídica actual a la línia de diari |
| Cost de la unitat de recursos | Diari d'integració d'entitat jurídica prestadora | No | Client interempresa | **Grup d'impostos de les vendes de facturació**: segons el **client interempresa** <br/> **Grup d'impostos de les vendes d'element de facturació**: de la categoria de projecte d'entitat jurídica actual a la línia de diari |
| Vendes entre unitats organitzatives | Diari d'integració d'entitat jurídica prestadora | No | Client interempresa | **Grup d'impostos de les vendes de facturació**: segons el **client interempresa** <br/> **Grup d'impostos de les vendes d'element de facturació**: de la categoria de projecte d'entitat jurídica actual a la línia de diari |

### <a name="example-intercompany-transactions"></a>Exemple: transaccions entre empreses

Molly Clark, desenvolupador que treballa a GBPM registra 10 hores de feina en un projecte d'USPM Adventure Works, que és aprovat pel director del projecte. El cost del desenvolupador en GBPM és de 88 GBP per hora. GBPM facturà a USPM 120 USD per hora de desenvolupador. USPM facturarà al client Adventure Works 200 USD per al treball realitzat pel recurs de GBPM. Per obtenir més informació, vegeu [Configuració de la facturació entre empreses](configure-intercompany-invoicing.md).

1. A Project Operations, aneu a **Recursos** i seleccioneu **Molly Clark** a la llista. A la pestanya **Planificació**, al camp **Empresa**, seleccioneu **GBPM**.
2. Aneu a **Vendes** > **Clients** i seleccioneu **Crea** per crear un nou registre de client per a Adventure Works.
    1. Definiu l'empresa com a **USPM**.
    2. Definiu el **Tipus de relació** com a **Client**.
    3. Seleccioneu el **Grup de clients 10 - Nacionals**.
    4. Definiu la moneda com a **USD**.
    5. Desar el registre.
3. Aneu a **Vendes** > **Contractes de projecte** i creeu un contracte de projecte nou per a Adventure Works.
    1. Definiu l'empresa propietària com a **USPM** i la unitat de contractació com a **Contoso Robotics US**.
    2. Seleccioneu Adventure Works com a client.
    3. Seleccioneu una llista de preus de productes i deseu el registre.
    4. A la pestanya **Línies de contracte**, creeu una línia de contracte nova. Definiu-ne el nom i seleccioneu **Temps i materials** com a mètode de facturació.
    5. Creeu un projecte nou i associeu-lo a aquesta línia de contracte.
4. Inicieu la sessió com a recurs, **Molly Clark**. Aneu a **Projectes** > **Entrades de temps** i creeu una entrada de temps per al projecte d'Adventure Works.
5. Inicieu la sessió com a Director del projecte. Aneu a **Projectes** > **Aprovacions** i aproveu la transacció d'entrada de temps registrada per Molly Clark.
6. Aneu al projecte d'Adventure Works i seleccioneu **Relacionat** > **Valors reals**. Es creen les transaccions reals següents.

| **Tipus de transacció** | **Preu** | **Moneda de transacció** | **Import** |
| --- | --- | --- | --- |
| Cost | 120 | USD | 1200 |
| Vendes no facturades | 200 | USD | 2000 |
| Cost de la unitat de recursos | 88 | GBP | 880 |
| Vendes entre unitats d'organització | 120 | USD | 1200 |

7. Inicieu la sessió com a comptable d'USPM. Obriu la instància de Finances de Project Operations i seleccioneu l'empresa **USPM**. 
8. Aneu a **Gestió de projectes i comptabilitat** > **Periòdic** > **Project Operations sobre Customer Engagement** > **Importa de la taula intermèdia** i seleccioneu d'executar el procés periòdic. Aquest procés periòdic s'afegirà al diari d'integració de Project Operations.
9. Aneu a **Gestió de projectes i comptabilitat** > **Diaris** > **Diari d'integració de Project Operations** i reviseu les línies de diari. El sistema crea la línia següent.

    | **Tipus de transacció** | **Preu** | **Moneda de transacció** | **Import** |
    | --- | --- | --- | --- |
    | Vendes no facturades | 200 | USD | 2000 |

    Si el sistema està configurat per meritar ingressos per a aquest projecte, es publica el següent:

    - Dèbit: projecte - valor de vendes WIP 200 USD
    - Crèdit: projecte - ingressos acumulats 200 USD

    Aquesta venda no facturada ja està a punt per facturar. La factura del client Adventure Works es pot publicar financerament quan cal.

10. Inicieu la sessió com a comptable de **GBPM**. Obriu la instància de Finances de Project Operations i obriu l'empresa **GBPM**. 
11. Aneu a **Administració i comptabilitat del projecte** > **Periòdic** > **Integració del Project Operations** > **Importació des de la taula de còpia intermèdia** i executeu el procés periòdic per emplenar el llibre diari d'integració del Project Operations.
12. Aneu a **Gestió de projectes i comptabilitat** > **Diaris** > **Diari d'integració de Project Operations** i reviseu les línies. El sistema crea les línies següents.

    | **Tipus de transacció** | **Preu** | **Moneda de transacció** | **Import** |
    | --- | --- | --- | --- |
    | Cost de la unitat de recursos | 88 | GBP | 880 |
    | Vendes entre unitats d'organització | 120 | USD | 1200 |

    La publicació d'aquests registres té com a resultat les transaccions de vals següents:

    - Dèbit: cost del projecte 88 GBP
    - Crèdit: assignació de nòmina 88 GBP

    Si el sistema està configurat per meritar ingressos entre empreses, es publica el següent:

    - Dèbit: projecte - valor de vendes WIP 120 USD
    - Crèdit: projecte - ingressos acumulats 120 USD

    El sistema ja està preparat per crear una factura de client interempresa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
