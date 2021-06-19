---
title: Confirmació d'una factura de projecte proforma
description: Aquest tema proporciona informació sobre la confirmació de factures de projecte proforma a Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004114"
---
# <a name="confirm-a-proforma-project-invoice"></a>Confirmació d'una factura de projecte proforma 

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_


Després que es confirmi una factura proforma, l'estat de la factura del projecte s'actualitza a **Confirmada**. Quan es confirma una factura, es converteix en només de lectura. Més endavant, la factura només es pot corregir si hi ha correccions o abonaments iniciats pels clients.

La taula següent enumera els valors reals creats pel sistema. Aquests valors reals es creen quan es realitzen certes operacions sobre l'esborrany de la factura del projecte abans de confirmar-la.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Escenari</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Valors reals creats en la confirmació</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació d'un avançament o bestreta </p>
            </td>
            <td width="408" valign="top">
                <p>
Una valor real de vendes facturades del tipus <strong>Bestreta</strong> es crea per a l'import de l'avançament o bestreta.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda no facturada de l'import negatiu de la bestreta o avançament que s'utilitzarà per a la conciliació.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Després de reconciliar completament una bestreta o avançament en una factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació. Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de vendes facturades per l'import d'aquesta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Després de reconciliar parcialment una bestreta o avançament en una factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació. Aquest import és positiu perquè està destinada a cancel·lar el negatiu creat quan es va facturar la bestreta o avançament.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de vendes facturades per l'import d'aquesta factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda no facturada negatiu de l'import de la bestreta o avançament restant que s'utilitzarà per a factures futures.
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
Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió del valor real de venda i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada no imputable per les hores i l'import restants després de deduir les xifres corregides en el detall de la línia de factura editada, reversió del valor real de venda i valor real de venda facturada equivalent.
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
Valor real de venda facturada per la quantitat i quantitat en l'aprovació de despeses original </p>
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
Facturar una transacció de material sense edicions a l'esborrany de la factura.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació d'ús de materials original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un valor real de vendes facturades per a la quantitat i l'import a la aprovació d'ús de materials original.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació d'una transacció de materials que s'ha editat per reduir la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació de temps original.
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
Facturació d'una transacció de materials que s'ha editat per augmentar la quantitat.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversió de vendes no facturades per a la quantitat i l'import a la aprovació d'ús de materials original.
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
        <tr>
            <td width="216" valign="top">
                <p>
Facturar una línia de contracte basada en productes.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Valor real de venda facturada per a la línia de producte amb la quantitat i quantitat provinents de la línia de contracte basada en el producte.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
