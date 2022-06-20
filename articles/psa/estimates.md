---
title: Estimacions
description: Aquest article proporciona informació sobre les estimacions a Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: fdd8fa033131500956249b1bdabc135b5057bbc1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920508"
---
# <a name="estimates"></a>Estimacions

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

En una oferta basada en un projecte, podeu utilitzar l'entitat Detall de la línia d'oferta per estimar el treball que es necessita per lliurar un projecte. A continuació, podeu compartir aquesta estimació amb el client.

Les línies d'oferta basades en el projecte no han de tenir els detalls de la línia d'oferta. D'altra banda, pot haver-hi molts detalls de la línia d'oferta. Els detalls de la línia d'oferta s'utilitzen per estimar el temps, les despeses o les taxes. El PSA no permet l'estimació de materials als detalls de la línia d'oferta. Això s'anomena classes de transaccions. Els imports de taxes previstos també es poden introduir en una classe de transacció.

A banda de les classes de transacció, els detalls de la línia d'oferta tenen un tipus de transacció. El PSA admet dos tipus de transacció per als detalls de la línia d'oferta: **Cost** i **Contracte de projecte**.

## <a name="estimate-by-using-a-contract"></a>Estimació mitjançant un contracte

Si heu utilitzat una oferta del PSA en crear un contracte basat en un projecte, l'estimació que heu fet per a cada línia d'oferta de l'oferta es copia al contracte del projecte. L'estructura d'un contracte de projecte és com l'estructura d'una oferta de projecte amb línies, detalls de línia i planificacions de factura.

Les estimacions es poden fer directament en un contracte de projecte, com en una oferta de projecte. Per a un pressupost de projecte, l'estimació es fa mitjançant les línies del contracte i els detalls de la línia de contracte. Els detalls de la línia de contracte també es poden generar des d'un pla de projecte que s'hagi creat amb l'enfocament d'estimació de baix a dalt.

Els detalls de la línia de contracte es poden utilitzar per estimar el temps, les despeses o les taxes. Els imports de taxes previstos també es poden introduir en un detall de línia de contracte.

El PSA no permet l'estimació de materials als detalls de la línia de contracte.

Els processos admesos en un contracte de projecte són la creació i la confirmació de factures. La creació de factures crea un esborrany d'una factura basada en projectes que inclou tots els valors reals de vendes no facturades fins a la data actual.

La confirmació fa que el contracte sigui només de lectura i canvia l'estat d'**Esborrany** a **Confirmat**. Després d'haver dut a terme aquesta acció, no es pot desfer. Com que aquesta acció és permanent, és una pràctica més recomanable mantenir el contracte en un estat d'**Esborrany**.

L'única diferència entre els esborranys de contractes i els contractes confirmats és el seu estat i el fet que els esborranys de contractes es puguin editar mentre que els contractes confirmats no ho permeten. Els valors reals de creació i seguiment de factures es poden fer tant en esborranys de contractes com en contractes confirmats.

El PSA no admet canviar comandes sobre contractes o projectes.

## <a name="estimating-projects"></a>Estimació de projectes

Podeu estimar el temps i les despeses als projectes. El PSA no permet l'estimació de materials ni taxes als projectes.

Les estimacions de temps es generen en crear una tasca i identifiquen els atributs d'un recurs genèric que són necessaris per fer la tasca. Les estimacions de temps es generen a partir de tasques de planificació. Les estimacions de temps no es creen si creeu membres de l'equip genèric fora del context de la planificació.

Les estimacions de despesa s'introdueixen a la quadrícula a la pàgina **Estimacions**.

## <a name="understanding-estimation"></a>Comprendre les estimacions

Utilitzeu la taula següent com a guia per comprendre la lògica empresarial en la fase d'estimació.

| Escenari                                                                                                                                                                                                                                                                                                                                          | Registre d'entitat                                                                                                                                                                                                       | Tipus de transacció | Classe de la transacció | Informació addicional                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Quan hàgiu d'estimar el valor de vendes del temps en una oferta                                                                                                                                                                                                                                                                                    | Es crea un registre del detall de la línia d'oferta (QLD)                                                                                                                                                                               | Contracte de projecte | Time        | El camp d'origen de transacció a la fila de QLD de la part de vendes fa referència al QLD del costat de cost |
|                                                                                                                                                                                                                                                                                     | El sistema crea un segon registre de QLD per emmagatzemar els valors de cost corresponents. Tots els camps que no siguin monetaris es copien des del QLD de vendes al QLD de cost pel sistema.                                                                                                                                                                               | Cost | Time        | El camp d'origen de transacció a la fila de detall de la línia d'oferta (QLD) de la part de vendes fa referència al QLD del costat de cost |
| Quan hàgiu d'estimar el valor de vendes del temps en un contracte                                                                                                                                                                                                                                                                                 | Es crea un registre del detall de la línia de contracte del projecte (CLD)                                                                                                                                                                    | Contracte de projecte | Time        | El camp Origen de transacció a la fila de CLD de la part de vendes fa referència al CLD de cost      |
|                                                                                                                                                                                                                                                                                  | El sistema crea un segon registre de CLD per emmagatzemar els valors de cost corresponents. Tots els camps que no siguin monetaris es copien des del CLD de vendes al CLD de cost pel sistema.                                                                                                                                                                    | Cost | Time        | El camp Origen de transacció a la fila de CLD de la part de vendes fa referència al CLD de cost      |
| Quan l'usuari descriu un recurs d'una tasca de projecte                                                                                                                                                                                                                                                                                            | El registre de la línia d'estimacions per mostrar el valor de vendes de la tasca es crea quan es crea una tasca amb totes les dimensions de preus necessàries. Les funcions i les unitats organitzatives són les dimensions de preus OOB del Project Service | Contracte de projecte | Time        |                                                                                   |
|     | El registre de la línia d'estimacions per mostrar el valor de cost de la tasca es crea quan es crea una tasca amb totes les dimensions de preus necessàries. Tots els camps que no siguin monetaris es copien des de la línia d'estimacions de vendes a la línia d'estimacions de cost pel sistema. La unitat de funció i organització són les dimensions de preus OOB del PSA per a tarifes de costos i factures.                                                                                                                                                                                                                | Cost             | Time           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personalitzar les entitats Detall de la línia d'oferta i Detalls de la línia de contracte

Si heu afegit un camp personalitzat al detall de la línia d'oferta i voleu que el sistema introdueixi el valor del camp com a valor per defecte a la línia de cost relacionada que crea, utilitzeu les eines de registre de connectors PreOperationContractLineDetailUpdate i PreOperationQuoteLineDetailUpdate. Aquests complements s'han de tornar a registrar després que es canviï el detall de la línia d'oferta o el detall de la línia de contracte. Seguiu aquests passos per completar el procés.

1. Obriu el PluginRegistrationTool i connecteu-vos a la instància en línia.
2. Seleccioneu **Cerca** i cerqueu el complement que voleu actualitzar.

    ![Quadre de diàleg Arbre de cerca.](media/basic-guide-19.png)

3. Seleccioneu el complement i, a continuació, a la pàgina principal, seleccioneu **Selecciona**.
4. Seleccioneu el pas del complement que voleu actualitzar, feu clic amb el botó dret i, a continuació, seleccioneu **Actualitza**.

    ![Seleccionar un pas en el complement.](media/basic-guide-20.png)

5. Al quadre de diàleg **Actualitza el pas existent**, al camp **Atributs de filtratge**, seleccioneu el botó de punts suspensius (**...**):
 
    ![Quadre de diàleg Actualitza el pas existent.](media/basic-guide-21.png)

6. Al quadre de diàleg **Selecció d'atributs**, seleccioneu les caselles de selecció per als atributs personalitzats.

    ![Quadre de diàleg Selecció d'atributs.](media/basic-guide-22.png)

7. Seleccioneu **D'acord** per tancar el quadre de diàleg i, a continuació, seleccioneu **Actualitza el pas**.
 
    ![Botó Actualitza el pas.](media/basic-guide-23.png)

8. Repetiu els passos de l'1 al 7 per al segon complement.
9. Tanqueu el PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
