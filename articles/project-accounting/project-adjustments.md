---
title: Ajustos del projecte
description: Aquest article proporciona informació sobre els ajustos del projecte.
author: ryansandness
ms.date: 11/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 52a262adce2bb624bc088e50858e25824f845e5c
ms.sourcegitcommit: bb03ac64e01112c93bb24035a51653a0a88cd5fc
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788361"
---
# <a name="project-adjustments"></a>Ajustos del projecte

_**S'aplica a:** Project Operations per a escenaris basats en producció/mantinguts en existències_

## <a name="adjustments-overview"></a>Visió general dels ajustos

Podeu configurar Microsoft Dynamics 365 Project Operations perquè els usuaris puguin fer canvis a les transaccions comptabilitzades. Podeu ajustar les transaccions del projecte individualment o podeu seleccionar diverses transaccions alhora en una llista de totes les transaccions del projecte. Els ajustos del projecte s'utilitzen, per exemple, per actualitzar massivament l'estat facturable, tornar a calcular el cost després d'un canvi de configuració o actualitzar les fonts de finançament.

Els usuaris poden accedir a la funcionalitat d'ajust del projecte de diverses maneres:

- Mitjançant la pàgina Ajusta les transaccions a la **qual es pot accedir des** de l'Administració de **projectes i la configuració comptable** \> **·**.
- Mitjançant el **botó Ajust** de la pàgina Comptabilització de transaccions del projecte a la **qual es pot accedir des** de Gestió de **projectes i transaccions comptables** \> **·**.
- Mitjançant el **botó Ajust** de la **pàgina Posted project transactions** en el context d'un projecte. Es pot accedir a aquesta pàgina des de **Project Management i comptabilitat** \> **de tots els projectes**.

Per permetre els ajustos, heu d'habilitar un o més estats de transacció des de **Project Management i accounting** \> **Project Management i paramaters comptables** a la pestanya General **de l'apartat**  **Permet l'ajust de l'estat** de les transaccions. Alguns exemples d'estats de transacció són les transaccions comptabilitzades, les transaccions facturades o les transaccions eliminades. Qualsevol estat de transacció que estigui definit com a **No** tindrà transaccions en aquest estat que no apareixeran al procés d'ajust com a seleccionables per a l'ajust.

Actualment, una opció de configuració que s'anomena **Crea sempre una transacció** d'ajust està disponible als paràmetres d'administració de projectes i comptabilitat. Podeu desactivar aquesta opció per actualitzar la transacció original en lloc de crear transaccions noves durant l'ajust en un subconjunt d'escenaris. S'ha anunciat que aquest paràmetre quedarà obsolet abans de l'1 de març de 2023. Després de l'1 de març de 2023, el sistema sempre es comportarà com si l'opció estigués habilitada.

## <a name="adjustments-process-flow"></a>Ajustos del flux del procés

Els passos següents mostren el flux típic per processar els ajustos.

1. Obriu la **pàgina Ajustos** del projecte.
2. Seleccioneu **Selecciona** per cercar transaccions que compleixin els criteris d'ajust esperats.
3. A la llista de transaccions, seleccioneu totes les transaccions o un subconjunt de les transaccions per ajustar-les.
4. Seleccioneu **Ajusta** i modifiqueu els atributs de la línia. Com a alternativa, si els valors s'han especificat manualment durant l'entrada de la transacció, podeu seleccionar introduir els valors predeterminats del sistema.
5. Es retorna la llista de transaccions i apareix una marca de verificació a la columna Pendent d'ajust **per** indicar on s'han fet els canvis. Els ajustos que tenen canvis pendents es mostren a la meitat inferior de la pàgina. Allà, podeu fer canvis detallats addicionals més enllà del que es mostrava a la pàgina anterior.
6. Seleccioneu **Publica** per publicar les transaccions d'ajust.

En funció de la configuració, normalment es creen transaccions noves per a l'ajust.

- El **camp Estat** de la factura de la transacció original està definit com a **Ajustat**.
- Es crea una transacció de reversió per revertir la transacció original i el **camp Estat** es defineix com a **Ajustat**.
- Es crea una nova transacció que té els canvis que es van fer durant el procés d'ajust.

### <a name="selecting-multiple-posted-project-transactions-at-a-time-for-adjustments-and-credit-notes"></a>Selecció de diverses transaccions de projecte publicades alhora per a ajustos i notes de crèdit

Una nova característica que es va introduir a la versió 10.0.30 permet seleccionar diverses transaccions per ajustar-les alhora des de la **pàgina Transaccions** publicades del projecte.

Abans de poder utilitzar aquesta funció, ha d'estar habilitada al vostre sistema. Els administradors poden utilitzar l'espai **de treball De gestió** de funcions per comprovar l'estat de la característica i habilitar-la si és necessari. A l'espai **de treball Gestió** de característiques, cerqueu i seleccioneu **Transaccions de projecte comptabilitzades amb diverses seleccions per als ajustos i les notes de** crèdit i, a continuació, seleccioneu **Habilita ara**.

Aquesta característica permet la següent funcionalitat clau:

- S'hi pot accedir des de la pàgina de transacció publicada dins d'un projecte mitjançant el botó d'ajust **existent** .
- Permet un control de selecció de diverses files a la pàgina Transaccions publicades **del** projecte. Podeu aplicar filtres a la pàgina de llista i seleccionar els registres abans de començar els ajustos.
- Desactiva el **botó Ajusta** si no es pot ajustar una sola transacció o si seleccioneu una combinació de notes de crèdit i diaris junts en lloc de fer-ho individualment.
- A causa de l'addició del control de selecció de diverses files, l'enllaç **Cost** compromès de la cinta ja no es desactiva si se seleccionen diverses files.
- Afegeix el següent missatge d'advertència: "Heu seleccionat més de registres (número seleccionat) per ajustar-los. Continuar amb aquesta acció pot trigar un temps. Estàs segur que t'agradaria continuar amb aquesta acció?"

Aquesta funció també elimina el pas 2 del flux de procés que es va descriure anteriorment en aquest article. Per tant, totes les transaccions seleccionades abans d'obrir la **pàgina Ajusta les transaccions** s'inclouran a la llista de transaccions per ajustar-les. No cal que utilitzeu el **botó Selecciona** per cercar-los.

> [!NOTE] 
> Fins i tot si aquesta funció està inhabilitada, encara podeu seleccionar diversos registres per ajustar-los. Tanmateix, només quedarà *seleccionat* un registre i el quadre de diàleg Selecciona les **transaccions** apareixerà immediatament després de seleccionar obrir ajustos.

## <a name="adjustment-transaction-statuses-that-can-be-enabled-or-disabled-for-adjustments"></a>Ajustar els estats de les transaccions que es poden activar o desactivar per als ajustos

Els estats següents es poden habilitar o desactivar a la **pestanya General** de la **pàgina Paràmetres comptables** i d'administració del projecte:

- Publicada
- Proposta de factura
- Facturat
- Aproximat
- Eliminat
- Balanç inicial (hora)

## <a name="adjustment-parameters"></a>Paràmetres d'ajust

Aquests paràmetres s'enumeren a la **pàgina Gestió de projectes i paràmetres comptables** de la **pestanya General** del grup Ajust **i modificaran el** comportament de com es processen els ajustos. 

| Nom del paràmetre | Descripció |
|----------------|-------------
| Creeu sempre una transacció d'ajust | Si s'habilita aquest paràmetre, el procés d'ajust sempre crearà una nova transacció reversible i una nova transacció ajustada quan hi hagi un impacte financer o d'informes. Si el paràmetre està desactivat, el procés d'ajust actualitzarà la transacció original en lloc de crear una reversió i una transacció nova per a un escenari com ara una actualització del text de la transacció. |
| Camp d'autoupdate | Si s'habilita aquest paràmetre, el sistema recalcularà el preu de cost i el preu de venda. |
| Utilitzeu la data d'ajust com a projecte nou | Aquest paràmetre s'utilitza per moure transaccions a una futura període fiscal abans que el sistema admetés aquesta funció. No et recomanem que l'utilitzis perquè canvia la data de negoci de la transacció i quedarà obsoleta en una versió futura. |
| Permetre activitats tancades | Normalment, no es poden crear transaccions per a activitats tancades. Si aquest paràmetre està habilitat, aquest comportament queda anul·lat. Per tant, es poden crear ajustos per a activitats tancades. |
