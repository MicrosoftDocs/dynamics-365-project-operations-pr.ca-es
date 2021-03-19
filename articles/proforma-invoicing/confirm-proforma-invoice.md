---
title: Confirmació d'una factura proforma
description: En aquest tema, podreu obtenir informació sobre la confirmació d'una factura proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287856"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmació d'una factura proforma

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Després que es confirmi una factura proforma, l'estat de la factura del projecte s'actualitza a **Confirmada**. Quan es confirma una factura, es converteix en només de lectura. En el futur, la factura només es pot corregir si hi ha correccions o crèdits iniciats pel client, o quan la factura es marca com a pagada.

La taula següent enumera els valors reals creats pel sistema. Aquests valors reals es creen quan es realitzen certes operacions sobre l'esborrany de la factura del projecte abans de confirmar-la.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Escenari</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Valors reals creats en la confirmació</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacció de temps sense cap modificació a l'esborrany de factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda facturada per les hores i quantitat en l'aprovació de temps original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació d'una transacció de temps editada per reduir la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada no imputable per a les hores i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació d'una transacció de temps editada per augmentar la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturades per les hores i l'import en l'aprovació de temps original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar una transacció de despeses sense cap modificació a l'esborrany de factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda facturada per la quantitat i quantitat en l'aprovació de despeses original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació d'una transacció de despesa editada per reduir la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada no imputable per a la quantitat i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda sense facturar i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació d'una transacció de despesa editada per augmentar la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes sense facturar per la quantitat i quantitat en l'aprovació de despeses original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per a la quantitat i l'import en el detall de la línia de factura editada, reversió del valor real de venda no facturada i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació d'una tarifa.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturades per a l'import de la taxa en la línia del llibre diari original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda facturada per la quantitat i quantitat en la línia del llibre diari de taxa original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturació d'una fita.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Valor real de vendes facturades per l'import de la fita a la fita original a la línia de contracte del projecte.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]