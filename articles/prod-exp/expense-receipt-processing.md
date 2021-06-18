---
title: Processament de rebuts de despeses
description: Aquest tema proporciona informació sobre el processament del reconeixement òptic de caràcters (OCR) per als rebuts. Aquesta característica està dissenyada per millorar l'experiència de l'usuari en crear informes de despeses al Microsoft Dynamics 365 Finance.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993494"
---
# <a name="expense-receipt-processing"></a>Processament de rebuts de despeses

L'entrada de despesa s'ha millorat mitjançant la introducció del reconeixement òptic de caràcters (OCR) per al processament de rebuts. Aquesta característica està dissenyada per millorar l'experiència de l'usuari en crear informes de despeses.

## <a name="key-features"></a>Característiques destacades

- El nom del comerciant, la data i la quantitat total s'extreuen dels rebuts.
- La característica intenta fer coincidir els rebuts no adjunts a transaccions de despeses no adjuntes.
- Els usuaris poden crear transaccions de despeses introduïdes manualment des dels rebuts.

## <a name="usage-examples"></a>Exemples d'ús

Per adjuntar automàticament els rebuts que inclouen transaccions de targetes de crèdit quan es crea un informe de despeses, feu el següent:

  1. Obriu l'àrea de treball **Administració de despeses**.
  2. A la pestanya **Rebuts**, verifiqueu que hi hagi rebuts no adjunts. També podeu carregar els rebuts a la pestanya **Rebuts**.
  3. A la pestanya **Despeses**, verifiqueu que hi hagi despeses no adjuntes. Normalment, l'administrador de despeses importa aquestes despeses del proveïdor de la targeta de crèdit.
  4. Seleccioneu **Informe de despeses nou**. Heu de tenir en compte que podeu incloure despeses i rebuts, ara també, quan creeu un informe de despeses. Si afegiu despeses i rebuts, la coincidència automàtica dels rebuts amb les despeses s'activa.

Per crear una despesa o fer coincidir una despesa d'un rebut, feu el següent:

  1. A l'informe de despeses, a la pestanya **Rebuts**, adjunteu un rebut seleccionant **Afegeix rebuts**.
  2. A la imatge carregada del rebut, observeu les opcions **Crea** i **Fes coincidir**.

      - Seleccioneu **Crea** per crear una transacció de despeses introduïda manualment i empleneu els valors que s'extreuen del rebut.
      - Si seleccioneu **Fes coincidir**, el sistema prova de fer coincidir una despesa existent amb el justificant.

## <a name="installation"></a>Instal·lació

Aquesta característica funciona en combinació amb la característica **Informes de despeses reinventats** per ajudar a simplificar l'experiència de despesa. Aquesta característica només està disponible per a entorns del nivell 2 o superior, que són espai aïllat i producció.

Per utilitzar aquestes capacitats de despesa avançada, instal·leu el complement Servei d'administració de despeses per al Microsoft Dynamics 365 Finance i activeu les característiques a la instància. Podeu accedir al complement des del projecte al Microsoft Dynamics Lifecycle Services (LCS).

1. Inicieu la sessió al LCS i obriu l'entorn desitjat.
2. Aneu a **Detalls complets**.
3. Seleccioneu **Mantén** o desplaceu-vos avall al FastTab **Complements de l'entorn**.
4. Seleccioneu **Instal·la un complement nou**.
5. Seleccioneu **Servei d'administració de despeses**.
6. Seguiu la guia d'instal·lació i accepteu els termes i les condicions.
7. Seleccioneu **Instal·la**.

A l'àrea de treball **Administració de funcions**, activeu les característiques següents:

- Informes de despeses reimaginats
- Coincidència automàtica i creació de despeses des del rebut

Quan activeu aquestes característiques es produeixen les següents accions:

- L'àrea de treball **Administració de despeses** existent se substitueix per la nova àrea de treball.
- S'afegirà un element de menú nou per a la visibilitat del camp de despeses.
- Encara podeu obrir la pàgina **Informes de despeses** anterior anant a **Administració de despeses > Les meves despeses > Informes de despeses**.
- Els fluxos de treball i les aprovacions encara us porten a la pàgina d'informes de despeses existent.
- Els rebuts es processaran mitjançant el Microsoft Azure Cognitive Services i s'extrauran i s'afegiran les metadades.
- S'ha afegit una opció que us permet crear un informe de despeses que inclogui rebuts coincidents no adjunts.
- Una opció afegida als informes de despeses us permet crear una línia de despesa a partir d'un rebut o intenta fer coincidir un rebut existent amb una línia de despesa existent.

Per a més informació sobre els informes de despeses reinventats, vegeu [Informes de despeses reinventats](ExpenseWorkspaceNew.md).

## <a name="frequently-asked-questions"></a>Preguntes més freqüents

**Microsoft utilitza les meves dades per als seus models?**

No, Microsoft ha creat un model d'aprenentatge automàtic general per al servei de processament de rebuts. Aquest model no es basa en els rebuts que heu carregat.

**On està disponible i on es processa aquesta característica?**

Actualment, s'admeten els Estats Units.

**On van els meus rebuts?**

El Finance es posarà en contacte amb el Cognitive Services per extreure les dades dels camps. El Cognitive Services conservarà una còpia del rebut fins a 24 hores mentre es produeix el processament. Després de completar el processament, el Cognitive Services eliminarà el rebut. Els rebuts es continuen emmagatzemant al Finance.

Per obtenir més informació, vegeu [Habilitar la comprensió de rebuts amb la funcionalitat nova del reconeixedor de formularis](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]