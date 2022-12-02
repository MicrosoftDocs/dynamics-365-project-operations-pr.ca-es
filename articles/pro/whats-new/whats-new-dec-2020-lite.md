---
title: 'Novetats de desembre de 2020: implementació bàsica del Project Operations; tracte de facturació proforma'
description: 'Aquest article proporciona informació sobre les actualitzacions de qualitat disponibles en el llançament de desembre de 2020 de la implementació bàsica del Project Operations: tracte de facturació proforma.'
author: sigitac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 3c23e13919540913755223634a24802ff3064f10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924050"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Novetats de desembre de 2020: implementació bàsica del Project Operations; tracte de facturació proforma

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Aquest article s'aplica als components i versions següents del Dynamics 365 Project Operations:

  - Project Operations en entorn del Dataverse versió 4.5.0.134 

A la taula següent s'enumeren les actualitzacions al Project Operations a la versió 4.5.0.134 de Dataverse.

| **Àrea de característiques** | **Número de referència** | **Actualització de qualitat** |
| --- | --- | --- |
| Facturació i preus | 1986009 | Les línies del llibre diari creades manualment tenen un rendiment incoherent quan es confirma abans que el projecte s'hagi enllaçat o desenllaçat d'una línia de contracte. |
| Facturació i preus | 2014153 | Els productes no es facturen quan es duu a terme des de la planificació de factures. |
| Facturació i preus | 2014159 | Els productes no s'estiren quan la factura s'actualitza per a les transaccions. |
| Facturació i preus | 2028174 | Les actualitzacions dels detalls de la línia de factura han de seguir la lògica del diari de correcció. |
| Facturació i preus | 2028315 | Correccions de comportament de quadrícula incrustada editable. |
| Facturació i preus | 2031070 | L'ajustament dels detalls de la línia de factura correctiva s'ha de fer seguint la lògica del diari de correcció. |
| Facturació i preus | 2034186 | Ha de poder actualitzar un projecte en una línia de contracte. |
| Facturació i preus | 2034206 | L'estat d'ajustament s'ha de definir durant la reversió actual mentre es desvincula un projecte d'una línia de contracte. |
| Facturació i preus | 2040871 | Actualitzacions a les cel·les Permet unitat i Grup d'unitats a la quadrícula d'estimacions de Despesa. |
| Facturació i preus | 2053754 | Els valors reals creats a partir d'edicions de factura no es marquen amb l'estat d'ajustament ni l'estat de facturació. |
| Facturació i preus | 2057874 | Connexió de transacció correcta creada durant l'edició del detall de la línia de factura. |
| Facturació i preus | 2057875 | Orígens de transacció correcta creats durant l'edició del detall de la línia de factura. |
| Facturació i preus | 2057944 | Estat que no es pot superar establert com a Compromès per als valors reals que no estan preparats per a la facturació des d'una correcció de factura. |
| Facturació i preus | 2057963 | Dividiu el privilegi Create\_Product del privilegi Create\_ProjectContract. |
| Facturació i preus | 2067622 | La icona de processament s'ha de mostrar mentre es generen fites. |
| Facturació i preus | 2067624 | L'import contractat ha d'estar marcat com a recomanat per a l'empresa en generar fites. |
| Facturació i preus | 2086880 | Amaga el botó **Suggeriment** a la franja per a les línies d'oferta basada en projecte. |
| Implementació i configuració | 2101152 | El nou entorn creat mitjançant la plantilla de Project Operations des del centre d'administració de Power Platform ha de tenir realitzades totes les operacions posteriors a la instal·lació. |
|   Administració d'oportunitats | 2022204 | La quadrícula de facturació basada en el projecte de la pestanya **Facturació de la tasca** a la pàgina **Projecte** hauria d'amagar la quadrícula basada en projecte si no hi ha cap oferta/línia de contracte amb **Totes les tasques** i viceversa. |
|   Administració d'oportunitats | 2086601 | Les funcions i categories que es poden desactivar no es poden copiar a funcions Imputables ni a la llista de categories Imputables a les línies d'oferta i les línies de contracte. |
| Planificació i seguiment de projectes | 1949065 | La visibilitat de dades funciona correctament amb un zoom del 200% |
| Planificació i seguiment de projectes | 2046317 | Capacitat de canviar el nom de l'entitat del projecte a Project Operations |
| Planificació i seguiment de projectes | 2057171 | Missatge d'error actualitzat quan el camp **Data d'inici del projecte** està buit a la pàgina **Projecte**. |
| Planificació i seguiment de projectes | 2057197 | La còpia de la línia d'estimació amb referència de tasca no està admesa. |
| Planificació i seguiment de projectes | 2060687 | L'advertiment de fus horari ara desapareix després d'un temps concret. |
| Administració de recursos | 1832887 | L'ID de categoria de recurs per defecte ha de ser estàtic per garantir càrregues de dades repetibles per a entorns de Dataverse i de Finances. |
| Temps i despeses | 2034882 | El botó **Nou** es visualitza dues vegades a la barra d'ordres per a les entrades de temps quan Dynamics 365 Field Service està instal·lat. |
| Temps i despeses | 2056028 | Actualitza la pàgina **Edició de temps** per incloure la línia de temps. |
| Temps i despeses | 1983747 | El gràfic d'entrada de temps mostra dades addicionals. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]