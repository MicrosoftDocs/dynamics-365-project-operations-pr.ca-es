---
title: Administració de propostes de factura de projecte
description: En aquest article s'ofereixen detalls sobre el processament de factures orientades al client amb el Projecte Operacions per a escenaris basats en recursos o no emmagatzemats.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ef6003499f1372a51d7d1606db6f5bf9722a369d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927822"
---
# <a name="manage-project-invoice-proposals"></a>Administració de propostes de factura de projecte

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

El departament de facturació pot processar les propostes de factura de projecte quan es compleixen les dues condicions següents:

  - L'administrador del projecte confirma la factura de proforma al Microsoft Dataverse.
  - Totes les transaccions de vendes no facturades materials i de sempre que s'inclouen a la factura de proforma es publiquen mitjançant el llibre diari de la integració del Dynamics365 **Project Operations**.

Utilitzeu els passos següents per completar una proposta de factura del projecte el Dynamics 365 Finance.

1. Reviseu la informació de facturació per a transaccions de temps i materials i publiqueu el llibre diari de la **integració de Project Operations**.
2. Reviseu la informació de facturació de les fites de facturació de preus fixos.
3. Revisió i formatació d'una proposta de factura del projecte.
4. Publicació i impressió de factures del projecte.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Administrar la informació de facturació al diari llibre de la integració de Project Operations

Els valors reals del projecte creat al Dataverse són revisats i publicats a Finances per part del comptable del projecte. Per a més informació sobre com treballar amb el diari d'integració, vegeu [Diari d'integració al Project Operations](../project-accounting/project-operations-integration-journal.md).

Els valors reals de cost i els valors reals de vendes no facturades s'afegeixen al diari d'integració com a línies independents:

  - El preu de cost d'unitat i l'import de cost en el valor real de cost ve per defecte de la transacció del valor real de cost del projecte al Dataverse.
  - El preu de venda i l'import de vendes unitàries en les transaccions de vendes no facturades venen per defecte de la transacció de vendes no facturades del valor real del projecte al Dataverse.

### <a name="billing-sales-tax"></a>Impost de vendes de facturació

El càlcul de l'impost de vendes per a la facturació està determinat pel camp **Grup d'impostos de vendes de facturació** i **Grup d'impostos de vendes d'elements de facturació** en un registre de vendes no facturades a la línia del llibre diari **Integració a Project Operations**. Per defecte, el sistema estableix aquests valors de camp en funció de la pestanya **Finances** a la pàgina **Paràmetres de comptabilitat i de gestió del projecte**.

- **El mètode del grup d'impostos de vendes** determina la lògica per defecte del grup d'impostos de vendes de facturació:
  
  - **Projecte**: sempre per defecte és el grup d'impostos de vendes de facturació del projecte. Per revisar o canviar el grup d'impostos de vendes de facturació per defecte d'un projecte, seleccioneu **Mostra la comptabilitat per defecte** a la pàgina **Tots els projectes**.
  - **Contracte del projecte**: sempre per defecte és el grup d'impostos de vendes de facturació del contracte del projecte. Per revisar o canviar el grup d'impostos de vendes de facturació per defecte d'un contracte de projecte, seleccioneu **Mostra la comptabilitat per defecte** a la pàgina **Contractes de projecte**.
  - **Client**: sempre per defecte és el grup d'impostos de vendes de facturació del client.
  - **Cerca**: cercarà en totes les entitats anteriors i seleccionarà el primer valor disponible. La cerca s'inicia amb l'entitat **projecte**, llavors l'entitat **contracte del projecte** i, finalment, l'entitat **client**.

- **El mètode del grup d'impostos de vendes d'elements** determina la lògica per defecte del grup d'impostos de vendes d'elements de facturació:
  
  - Per als tipus de transaccions de temps, despesa i tarifa, el grup d'impostos de vendes d'articles de facturació sempre vindrà per defecte de l'entitat **categoria del projecte**.
  - Per als tipus de transaccions materials, el grup d'impostos de les vendes d'articles de facturació per defecte es basa en l'ajustament **mètode del grup d'impostos de les vendes d'articles** als **paràmetres de comptabilitat i gestió**. El número d'elements és per defecte el grup d'impostos de vendes d'elements de l'entitat del **producte publicat**. La categoria és per defecte el grup d'impostos de vendes d'elements de l'entitat de la **categoria del projecte**.

### <a name="financial-dimensions"></a>Dimensions financeres

Les propietats financeres per als registres de vendes no facturats en el llibre diari de la **integració al Project Operations** ve per defecte de l'entitat **projecte**. Per revisar i ajustar les propietats financeres, seleccioneu **Imports de distribució**. Si heu de canviar les mesures financeres del registre de vendes no facturades després de publicar el llibre diari d'integració però abans de confirmar la factura de Proforma, aneu a **Tots els projectes** > **Gestiona** > **Transaccions publicades**, seleccioneu la transacció i, a continuació, seleccioneu **Procés** > **Ajustament de la comptabilitat**.

### <a name="exchange-rates"></a>Tipus de canvi.

La moneda de transacció no facturada al Dataverse es fa servir com com a moneda de transacció a Finances i es converteix a la moneda de comptabilitat de l'empresa amb els tipus de canvi definits a Finances.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Administra els atributs financers de les fites de facturació 

Les línies de contracte del projecte que fan servir el mètode de facturació de preu fix es facturen mitjançant [fites de preu fix](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). El comptable del projecte pot revisar les fites de facturació de Finances anant a **Administració i comptabilitat del projecte** > **Tots els projectes** > **Administra** > **Transaccions al compte**.

### <a name="billing-sales-tax"></a>Impost de vendes de facturació

Els valors **grup d'impostos de vendes** i **grup d'impostos de vendes d'elements** venen per defecte de la configuració quan es crea una fita de facturació nova al Dataverse. Per defecte, el sistema estableix els valors d'aquests camps en funció de la configuració de la pestanya **Finances** a la pàgina **Paràmetres de comptabilitat i de gestió del projecte**.

- **El mètode del grup d'impostos de vendes** determina la lògica per defecte del **grup d'impostos de vendes de facturació**:

    - **Projecte** sempre per defecte és el grup d'impostos de vendes de facturació del projecte. Per revisar o canviar el grup d'impostos de vendes per defecte d'un projecte, seleccioneu **Mostra la comptabilitat per defecte** a la pàgina **Tots els projectes**.
    - **Contracte del projecte**: sempre serà per defecte el grup d'impostos de vendes de facturació del contracte del projecte. Per revisar o canviar el grup d'impostos de vendes de facturació per defecte d'un contracte de projecte, seleccioneu **Mostra la comptabilitat per defecte** a la pàgina **Contractes de projecte**.
    - **Client**: sempre serà per defecte el grup d'impostos de vendes de facturació del client.
    - **Cerca**: cercarà en totes les entitats d'aquesta llista i seleccionarà el primer valor disponible. La cerca s'inicia amb l'entitat **projecte**, llavors l'entitat **contracte del projecte** i, llavors, l'entitat **client**.

- El **Grup d'impostos sobre les vendes d'elements de fites de preu fix** s'utilitza com a valor per defecte al camp **Grup d'impostos sobre les vendes d'elements** per a la fita de facturació. El comptable pot revisar i modificar aquest valor a la pàgina **Transaccions en compte**. El sistema utilitza el valor de la transacció a compte en crear una línia de factura de projecte de factura.
 

### <a name="financial-dimensions"></a>Dimensions financeres

Les propietats financeres per defecte de la fita de facturació de preu fix es defineix a les línies de contracte del projecte. Aneu a **Contractes del projecte** > **Mostra la comptabilitat per defecte** i, a la pestanya **Línies de contracte**, seleccioneu **línia de contracte de preu** i, a continuació, definiu els valors de les propietats financeres que voleu establir per defecte.

El comptable del projecte pot editar la informació sobre l'impost de vendes i les propietats financeres sobre les fites de la factura fins que es creï la proposta de factura del projecte.


## <a name="create-project-invoice-proposals"></a>Creació de propostes de factura de projecte

Al mòdul **Administració i comptabilitat del projecte** es poden revisar les propostes de factura anant a **Factures del projecte** > **Propostes de factura del projecte**.

La capçalera de la proposta de factura del projecte es crea a Finances quan la factura de Proforma es confirma al Dataverse. Per simplificar la reconciliació, el sistema defineix el número de la proposta de factura del projecte a Finances igual a l'identificador de factura de Proforma al Dataverse. Com que les factures de Proforma no necessàriament es confirmen en el mateix ordre en què es creen, la seqüència de números de la proposta de factura del projecte a Finances ha de permetre canvis a un nombre inferior i superior. Configureu les seqüències de números seguint els passos següents:

1. A Finances, aneu a **Administració de l'organització** > **Seqüències de nombres** > **Seqüències de nombres**.
2. Al filtre **Àrea**, seleccioneu **Projectes**.
3. Al filtre **Referència**, seleccioneu **Proposta de factura**.
4. Utilitzeu el camp **Empresa** per filtrar cada entitat legal amb la integració al Dataverse del Project Operations habilitada.
5. Obriu **Detalls de la seqüència de nombres** i a la pestanya **General** trieu:

    - **Permetre canvis d'usuari: en un nombre inferior** = **Sí**
    - **Permetre canvis d'usuari: en un nombre superior** = **Sí**

El sistema afegeix les línies de la proposta de factura del projecte mitjançant el procés periòdic **Importació des de la taula de presentació** (**Administració i comptabilitat de projectes** > **Periòdic** > **Integració al Project Operations** > **Importa des de la taula de presentació**). Aquest procés es pot executar manualment o mitjançant un horari periòdic. El sistema no afegirà línies al document de proposta de factura fins que totes les línies estiguin a punt per facturar. Les transaccions horàries i materials estan a punt per facturar-se només si es publiquen mitjançant el llibre diari de la **integració de Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Formatació i impressió de les propostes de factura

El comptable del projecte pot personalitzar una impressió de factura del projecte mitjançant la pàgina **Formatació de la proposta de factura** i les funcions d'administració d'impressió.

### <a name="format-invoice-proposals"></a>Formatació de les propostes de factura

La pàgina **Formatació de les propostes de factura** permet que les transaccions amb agrupacions personalitzades es mostrin a la factura del projecte del client.

1. A la pàgina **Proposta de factura del projecte**, seleccioneu **Imprimeix** > **Formatació de la proposta de factura**.
2. Seleccioneu **Nou** per crear un agrupament nou per a la còpia impresa de la factura del projecte.
3. Al camp **Detall/Resum**, seleccioneu les opcions per a aquest agrupament:

    - Seleccioneu **Detall** per imprimir els detalls de les transaccions de la factura del client.
    - Seleccioneu **Resum** per imprimir el resum de les transaccions de la factura del client.

> [!NOTE]
> La selecció al camp **Detall/Resum** de la pàgina **Formatació de la proposta de factura** invalida l'opció seleccionada al camp **Formatació de la factura** de la pàgina **Propostes de factura** per imprimir una factura detallada o una de resumida.

- Seleccioneu les línies de transacció que voleu incloure en aquesta secció a la pestanya **Transaccions disponibles** i seleccioneu **Inclou transaccions** per desplaçar-les a la pestanya **Transaccions seleccionades**.
- Seleccioneu **Desplaça amunt** i **Desplaça avall** per canviar l'ordre de les seccions.
- Seleccioneu **Imprimeix la visualització prèvia** per obtenir el format de visualització prèvia de la factura.

### <a name="print-management"></a>Administració d'impressió

L'administració d'impressió utilitza diferents fitxers d'informe per imprimir, especificar destinacions i personalitzar el text dels peus de pàgina per a la factura. L'administració d'impressió es pot configurar en el nivell del mòdul, però aquesta configuració es pot sobreescriure per a un client, un contracte o una proposta de factura específics. Per accedir a aquesta funció a la pàgina **Proposta de factura del projecte**, seleccioneu **Impressió** > **Administració d'impressió**.

La configuració de l'administració d'impressió es visualitza com una visualització d'arbre, on cada nivell de node mostra els documents disponibles per ajustar-los. Podeu assignar còpies impreses personalitzades al mòdul, al client, al contracte o al nivell de document de proposta de factura. Per modificar la còpia impresa del document original, expandiu el node desitjat i seleccioneu **Element original**. Al camp **Format d'informe**, seleccioneu el format d'informe que voleu utilitzar per imprimir. Podeu utilitzar formats d'informe personalitzats mitjançant el [marc de l'administració de documents de l'empresa](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Publicació de les propostes de factura

Quan la factura s'ha revisat i editat, i les línies de proposta de la factura són satisfactòries, comproveu el total de la factura i l'impost de vendes. Al grup **Detalls**, seleccioneu **Totals** i, a continuació, seleccioneu **Publica** per publicar la factura.

Per visualitzar la factura abans de publicar-la, desactiveu la casella de selecció **Publica**. **Pro forma** s'imprimirà a la factura per indicar que es tracta d'una factura d'exemple. Per imprimir la factura, activeu la casella de selecció **Imprimeix la factura**.

A banda de la pàgina **Proposta de factura**, també es poden publicar propostes de factura per mitjà de l'execució de feina periòdica, **Publica propostes de factura**. Per trobar aquesta feina, aneu a **Administració i comptabilitat del projecte** > **Periòdiques** > **Factures de projecte** > **Publica propostes de factura**.

En aquesta pàgina es mostren totes les propostes de factura preparades per publicar-les. Per planificar la publicació de propostes de factura, seleccioneu **Lot**. Definiu el **Paràmetre de processament per lots** en **Sí** i definiu la periodicitat del processament per lots seleccionant **Periodicitat**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
