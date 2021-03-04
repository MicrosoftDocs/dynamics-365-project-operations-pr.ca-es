---
title: Pàgina d'inici de dimensions de preus i de costos
description: Aquest tema proporciona una visió general de les dimensions de preus.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151286"
---
# <a name="pricing-and-costing-dimensions-home-page"></a>Pàgina d'inici de dimensions de preus i de costos

[!include [banner](../includes/psa-now-project-operations.md)]

Les dimensions que s'utilitzen per definir els preus del treball i els costos en organitzacions basades en projectes tenen la influència dels atributs següents:

- Persones que fan una feina semblant a la seva experiència, funció o zona geogràfica
- Feina que cal per dur a terme semblant a la seva complexitat o hora del dia

Donada la naturalesa típica d'aquestes atributs del treball i de les persones necessàries per dur a terme el treball, hi ha dos tipus de valors de dimensió de preus disponibles al Project Service Automation: 

- **Conjunts d'opcions**: atributs que són enumeracions fixes per a un conjunt de valors.
- **Valors basats en entitats**: atributs que poden tenir un conjunt variat de valors que són finits però que poden canviar amb el temps.

## <a name="pricing-dimensions"></a>Dimensions de preus

El PSA inclou de sèrie un conjunt de dimensions de preus per defecte. Podeu visualitzar-los anant a **Project Service** > **Paràmetres**. Al registre de paràmetre, a la pestanya **Dimensions de preus basades en l'import**, comproveu que la funció **msdyn_resourcecategory** i la unitat organitzativa de recursos **msdyn_organizationalunit** tinguin els camps **Aplicable a les vendes** i **Aplicable al cost** definits com a **Sí**. Això us permetrà configurar el preu i el cost de cada combinació de funció i unitat organitzativa.

![Captura de pantalla dels paràmetres del Project Service amb "Aplicable a les vendes" ressaltat](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> Si heu estat utilitzant els camps de fàbrica de funció i unitat organitzativa com a dimensions de preus abans de la versió 3 del PSA, no hi haurà cap canvi observable. Podeu continuar utilitzant el Project Service com de costum. 

Si heu de posar un preu o un cost als recursos mitjançant atributs addicionals, podeu crear camps, entitats i dimensions personalitzats. Per obtenir més informació, vegeu els temes següents, però fixeu-vos que heu d'emplenar els procediments en l'ordre que es detalla a continuació:

- [Crear camps i entitats personalitzats](create-custom-fields-entities.md)
- [Afegir camps personalitzats a la configuració de preus i a entitats transaccionals](field-references.md)
- [Configuració de camps personalitzats com a dimensions de preus](set-up-pricing-dimensions.md)
- [Actualitzar els atributs de complement per incloure noves dimensions de preus](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a>Posar preu al temps de recursos humans
Com una organització posa preu al temps de recursos humans és sovint una consideració estratègica important que afecta directament la rendibilitat de l'organització. Treballeu amb els equips de finances i els caps de pràctiques quan la vostra organització estigui a punt per identificar com vol configurar la tarifa de facturació i el cost per al temps de recursos humans.

Altres consideracions sobre el preu inclouen la reutilització de camps o entitats que no són actualment dimensions de preus però que s'apliquen com una dimensió de preus per a la vostra organització. Els camps com ara **Categoria de transacció** (**msdyn_transactioncategory**) i **Recursos que es poden reservar** (**bookableresource**) són exemples de dimensions candidates. 

Tingueu en compte si la dimensió de preus ha de ser una taula o un conjunt d'opcions. Si preveieu canvis dels valors d'una dimensió que excedirà els 10 o 12 i necessiteu atributs addicionals sobre aquests valors, creeu una entitat en comptes d'un conjunt d'opcions. El manteniment d'un conjunt d'opcions, com afegir o eliminar valors, requereix un administrador o un desenvolupador, mentre que la majoria d'usuaris empresarials poden afegir una fila nova a una taula.

A l'exemple següent es mostren les tarifes de facturació que estan configurades en funció de la funció i de la unitat organitzativa de recursos a la qual pertany el recurs. Els percentatges de costos normalment es basen en la banda de salari de l'empleat i en la unitat organitzativa a la qual pertanyen. En aquest exemple, les taules de tarifes de facturació i de percentatge de cost s'assemblen al següent.

**Tarifes de facturació d'exemple**

| Funció        | Unitat organitzativa    |Unit      |Preu      |Moneda  |
| ------------|-------------|----------|----------:|----------|
| Desenvolupador   | Contoso EUA  |Hour | 200|USD     |
| Desenvolupador   | Contoso India |Hour|   112|USD     |


**Percentatge de costos d'exemple**

| Banda de salari     | Unitat organitzativa    |Unit      |Preu      |Moneda  |
| ----------------|-------------|----------|----------:|----------|
| La meva empresa_banda1 | Contoso EUA  |Hour | 145|USD     |
| La meva empresa_banda2 | Contoso India |Hour|   67|USD     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]