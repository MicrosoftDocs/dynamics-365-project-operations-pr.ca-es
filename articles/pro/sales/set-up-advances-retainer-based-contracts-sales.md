---
title: Avançaments i contractes de bestreta
description: Aquest tema proporciona informació sobre els models de contractació basats en bestretes i els avançaments al Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5b4e2e0bfd0da02c3386978ce732232631f10421
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994214"
---
# <a name="advances-and-retainer-based-contracts"></a>Avançaments i contractes de bestreta


_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització, implementació lleugera per a la facturació proforma_

El Dynamics 365 Project Operations admet els contractes de bestreta. Un contracte basat en bestreta és un conjunt negociat de pagaments igualment distribuïts que es facturaran al client facturat durant tota la duració d'un projecte. Aquest tipus de contracte s'utilitza normalment per als models de facturació de temps i material o basats en consum quan és necessari proporcionar al client una factura previsible i un calendari de pagament. Els ingressos reals acumulats cada període es concilien amb el pagament rebut pel client al començament del període. D'acord amb el concepte del model de facturació de temps i material, els valors d'ingressos acumulats en cada període poden variar amb els costos incorreguts. Si els ingressos acumulats són superiors a la quantitat rebuda al començament del període, l'empresa de lliurament del projecte podria:

- Facturar al client només per l'excés 
- Ajornar la conciliació dels ingressos al següent període de facturació i realitzar una factura final a la fi del projecte per a qualsevol ingrés no conciliat que quedi

La principal diferència entre un model de contractació basat en bestretes i un model de contracte de preu fix al Project Operations és que en el model de contracte de preu fix, l'import de la factura no està vinculat als costos incorreguts. La facturació segueix un enfocament basat en fites que s'alinea amb els costos incorreguts per a aquest període. En un contracte basat en bestretes, els ingressos que es poden facturar es registren segons el mètode de facturació de la línia de contracte. Quan el mètode de facturació és de temps i el material, els ingressos facturables estan vinculats als costos incorreguts en un període determinat i poden variar d'un període a un altre. No obstant això, només es factura al client per l'import de la bestreta periòdica. El sistema utilitza una altra factura al final del període per conciliar els ingressos facturables registrats durant el període amb la quantitat per la qual es va facturar al client al començament del període.

L'avantatge d'aquest mètode és que els costos del client esdevenen predictibles a la planificació de bestretes a diferència d'un model típic de temps i material. L'organització que lliura el projecte també té marge per cobrir el risc de recuperar els costos incorreguts a causa de qualsevol augment de l'abast que un model de preu fix no hauria permès.

A més d'una planificació periòdica basada en bestretes, el Project Operations pot registrar un avançament únic d'un client i conciliar-lo amb els diferents components de cost del projecte.

La bestreta al Project Operations no està disponible per al seu ús fins que es factura al client. Això s'indica amb els següents camps de la subquadrícula per a avançaments i bestretes.

| Camp | Descripció | Impacte descendent |
| --- | --- | --- |
| Import disponible | Import disponible utilitzar-lo en el registre de bestreta o d'avançament. | Fins que l'avançament o bestreta es facturi, no està disponible per utilitzar-se, cosa que significa que la quantitat disponible serà zero. |
| Import utilitzat | Import que ja s'utilitza en la bestreta o l'avançament. | Un avançament o bestreta es pot conciliar parcialment amb una factura amb costos reals que tindran una part marcada com a ja utilitzada o consumida. La resta de l'import de l'avançament o bestreta està disponible per a conciliar-lo en una factura futura amb costos reals. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]