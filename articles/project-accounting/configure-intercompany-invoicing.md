---
title: Configuració de la facturació entre empreses
description: En aquest article es proporciona informació i exemples sobre la configuració de la facturació entre empreses per a projectes.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ae0c2662bb6b2789ab520f08c7c21935b651ced5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929341"
---
# <a name="configure-intercompany-invoicing"></a>Configuració de la facturació entre empreses

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Seguiu aquests passos per configurar la facturació entre empreses per a projectes al Dynamics 365 Project Operations. Les transaccions entre empreses són transaccions de temps i de despeses d'un contracte de projecte que pertany a una empresa o unitat d'organització, mentre que els recursos del contracte de projecte formen part d'una altra empresa o unitat d'organització.

## <a name="example-configure-intercompany-invoicing"></a>Exemple: Configuració de la facturació entre empreses

A l'exemple següent, Contoso Robotics USA (USPM) és l'entitat jurídica prestatària i Contoso Robotics UK (GBPM) és l'entitat jurídica prestadora. 

1. **Configurar la comptabilitat interempresa entre entitats jurídiques**. Cada parell d'entitats jurídiques prestatària i prestadora s'ha de configurar a la pàgina de [Comptabilitat entre empreses](/dynamics365/finance/general-ledger/intercompany-accounting-setup) del Llibre major.
    
    1. Al Dynamics 365 Finance, aneu a **Llibre major** > **Configuració de comptabilització** > **Comptabilitat entre empreses**. Creeu un registre amb la informació següent:

        - **Empresa d'origen** = **GBPM**
        - **Empresa de destinació** = **USPM**

2. **Configurar la relació comercial entre entitats jurídiques**. El registre de client que representa l'entitat jurídica prestatària s'ha de crear a l'entitat jurídica prestadora. El registre de proveïdor que representa l'entitat jurídica prestadora s'ha de crear a l'entitat jurídica prestatària.

     1. A Finances, seleccioneu l'entitat jurídica **GBPM**.
     2. Aneu a **Comptes a cobrar** > **Client** > **Tots els clients**. Creeu un registre nou per a l'entitat jurídica, **USPM**.
     3. Expandiu **Nom**, filtreu els registres per **Tipus** i seleccioneu **Entitats jurídiques**. 
     4. Cerqueu i seleccioneu el registre de client per a **Contoso Robotics USA (USPM)**.
     5. Seleccioneu **Utilitza la coincidència**. 
     6. Seleccioneu el grup de clients **50: clients entre empreses** i, a continuació, deseu el registre.
     7. Seleccioneu l'entitat jurídica **USPM**.
     8. Aneu a **Comptes a pagar** > **Proveïdors** > **Tots els proveïdors**. Creeu un registre nou per a l'entitat jurídica, **GBPM**.
     9. Expandiu **Nom**, filtreu els registres per **Tipus** i seleccioneu **Entitats jurídiques**. 
     10. Cerqueu i seleccioneu el registre de client per a **Contoso Robotics UK (GBPM)**.
     11. Seleccioneu **Utilitza la coincidència**, seleccioneu el grup de proveïdors i, a continuació, deseu el registre.
     12. Al registre de proveïdor, seleccioneu **General** > **Configuració** > **Entre empreses**.
     13. A la pestanya **Relació comercial**, definiu **Actiu** com a **Sí**.
     14. Definiu el camp **Empresa client** com a **GBPM** i a **Registre del meu compte**, seleccioneu el registre de client que heu creat abans en el procediment.

3. **Establir la configuració entre empreses als paràmetres de gestió de projectes i comptabilitat**. 

    1. Seleccioneu l'entitat jurídica **USPM** i aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Paràmetres de gestió de projectes i comptabilitat**.
    2. A la pestanya **Entre empreses**, seleccioneu la categoria de contractació que s'ajusti a les factures de proveïdor que es generen automàticament.
    3. A **Categoria per defecte**, seleccioneu **Recursos entre empreses**.
    4. Seleccioneu l'entitat jurídica **GBPM** i aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Paràmetres de gestió de projectes i comptabilitat**.
    5. A la pestanya **Entre empreses**, seleccioneu una categoria de projecte per defecte per a cada tipus de transacció. Les categories de projecte s'utilitzen per a la configuració tributària quan la categoria facturada a les transaccions entre empreses només existeix a l'entitat jurídica prestatària. Podeu triar acumular els ingressos per a les transaccions entre empreses. La meritació es produeix quan les transaccions es comptabilitzen a través del diari d'integració de Project Operations a l'entitat jurídica prestadora. El diari es reverteix quan es comptabilitza la factura entre empreses.
    6. Al grup **En prestar recursos**, seleccioneu **...** > **Nou**. 
    7. A la quadrícula, seleccioneu la informació següent:

          - **Entitat jurídica prestatària** = **USPM**
          - **Merita beneficis** = **Sí**
          - **Categoria de cronologia per defecte** = **Per defecte: hora**
          - **Categoria de despesa per defecte** = **Per defecte: despesa**

4. **Definiu els comptes de costos i d'ingressos entre empreses a la configuració de la comptabilització del Llibre major**. El compte d'ingressos entre empreses s'abona quan la factura de client entre empreses es comptabilitza a l'entitat jurídica prestadora. El compte de costos entre empreses es carrega quan la factura de proveïdor pendent corresponent es comptabilitza a l'entitat jurídica prestatària. Aquests comptes es configuren a les entitats jurídiques corresponents. 
      
     1. A Finances, seleccioneu l'entitat jurídica prestatària **USPM**. 
     2. Aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Comptabilització** > **Configuració de la comptabilització al Llibre major**. 
     3. A la pestanya **Comptes de costos**, a **Tipus de compte de llibre major**, seleccioneu **Cost entre empreses**. Creeu un registre nou amb la informació següent:
      
        - **Entitat jurídica prestadora** = **GBPM**
        - **Compte principal** = Seleccioneu el compte principal per al cost entre empreses. Aquesta configuració és necessària. La configuració s'utilitza per als fluxos entre empreses a Finances, però no en fluxos entre empreses relacionats amb el projecte. Aquesta selecció no té cap impacte descendent. 
        
     4. Seleccioneu l'entitat jurídica prestadora, **GBPM**. 
     5. Aneu a **Gestió de projectes i comptabilitat** > **Configuració** > **Comptabilització** > **Configuració de la comptabilització al Llibre major**. 
     6. A la pestanya **Comptes d'ingressos**, a **Tipus de compte de llibre major**, seleccioneu **Ingrés entre empreses**. Creeu un registre nou amb la informació següent:

        - **Entitat jurídica prestatària** = **USPM**
        - **Compte principal** = Seleccioneu el compte principal per a l'ingrés entre empreses. Aquesta configuració és necessària. La configuració s'utilitza per als fluxos entre empreses a Finances, però no en fluxos entre empreses relacionats amb el projecte. Aquesta selecció no té cap impacte descendent. 

5. **Configurar els preus de transferència per a mà d'obra**. El preu de transferència entre empreses es configura a Project Operations a Dataverse. Configureu les [tarifes de cost de la mà d'obra](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) i les [tarifes de facturació de la mà d'obra](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) per a la facturació entre empreses. Els preus de transferència no s'admeten per a les transaccions de despeses entre empreses. El preu de venda entre unitats d'organització sempre es definirà amb el mateix valor que el preu de cost de la unitat de recursos.

      El cost de recurs de desenvolupador a Contoso Robotics UK és de 88 GBP per hora. Contoso Robotics UK facturarà a Contoso Robotics USA 120 USD per cada hora que aquest recurs hagi treballat en projectes dels EUA. Contoso Robotics USA facturarà al client Adventure Works 200 USD per a la feina feta pel recurs de desenvolupador de Contoso Robotics UK.

      1. A Project Operations, a Dataverse, aneu a **Venda** > **Llistes de preus**. Creeu una llista de preus de cost nova anomenada **Tarifes de cost de Contoso Robotics UK.** 
      2. A la llista de preus de cost, creeu un registre amb la informació següent:
         - **Funció** = **Desenvolupador**
         - **Cost** = **88 GBP**
      3. Aneu a **Configuració** > **Unitats organitzatives** i adjunteu aquesta llista de preus a la unitat organitzativa **Contoso Robotics UK**.
      4. Aneu a **Venda** > **Llistes de preus**. Creeu una llista de preus de cost anomenada **Tarifes de cost de Contoso Robotics USA**. 
      5. A la llista de preus de cost, creeu un registre amb la informació següent:
          - **Funció** = **Desenvolupador**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Cost** = **120 USD**
      6. Aneu a **Configuració** > **Unitats organitzatives** i adjunteu la llista de preus **Tarifes de cost de Contoso Robotics USA** a la unitat organitzativa **Contoso Robotics USA**.
      7. Aneu a **Venda** > **Llistes de preus**. Creeu una llista de preus de venda anomenada **Tarifes de facturació d'Adventure Works**. 
      8. A la llista de preus de venda, creeu un registre amb la informació següent:
          - **Funció** = **Desenvolupador**
          - **Empresa de recursos** = **Contoso Robotics UK**
          - **Tarifa de facturació** = **200 USD**
      9. Aneu a **Vendes** > **Contractes de projectes** i adjunteu la llista de preus **Tarifes de facturació d'Adventure Works** a la llista de preus del projecte Adventure Works del contracte del projecte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
