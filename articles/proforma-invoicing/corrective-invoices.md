---
title: Factures basades en projecte de correcció
description: Aquest tema proporciona informació sobre com crear i confirmar factures basades en projecte correctives a Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012259"
---
# <a name="corrective-project-based-invoices"></a>Factures basades en projecte de correcció

_**S'aplica a:** Project Operations per a escenaris basats en recursos/sense cotització_

Una factura confirmada del projecte es pot corregir per processar canvis o crèdits com s'hagin negociat amb el client i l'administrador del projecte.

Per fer modificacions a una factura confirmada, obriu la factura confirmada i seleccioneu **Corregeix aquesta factura**. 

> [!NOTE]
> Aquesta selecció no està disponible tret que es confirmi una factura de projecte o si la factura basada en projecte té avançaments o bestretes o retencions o conciliacions d'avançaments o bestretes.

Es crea un nou esborrany de factura a partir de la factura confirmada. Tots els detalls de la línia de factura de la factura confirmada anteriorment es copien al nou esborrany. Els següents són alguns dels punts clau per entendre els detalls de la línia sobre la nova factura corregida:

- Totes les quantitats s'actualitzen a zero. El Dynamics 365 Project Operations assumeix que tots els elements facturats s'abonen totalment. Si cal, podeu actualitzar manualment aquestes quantitats per reflectir la quantitat que s'està facturant i no la quantitat que s'està acreditant. Segons la quantitat que introduïu, l'aplicació calcula la quantitat acreditada. Aquesta quantitat es reflecteix en els valor reals que es creen quan es confirma la factura corregida. Si s'introdueixen canvis en l'import de l'impost, s'ha d'introduir l'import de l'impost correcte i no l'import de l'impost que s'ha acreditat.
- Les correccions de fites sempre es processen com a crèdits complets.


> [!IMPORTANT]
> Per als detalls de la línia de factura que són correccions a altres càrrecs ja facturats, el camp **Correcció** es defineix com a **Sí**. Per a les factures que tenen detalls de línia de factura de correcció, el camp **Té correccions** es defineix com a **Sí**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Valors reals creats quan es confirma una factura de correcció

A la taula següent es mostraran els valors reals que es creen quan es confirma una factura correctiva.

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
Facturació del crèdit complet d'una transacció de temps facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per les hores i l'import en el detall de la línia de factura original per al temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de vendes no facturades per les hores i l'import en el detall de la línia de factura original per al temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació del crèdit parcial en una transacció de temps.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per les hores i l'import facturat en el detall de la línia de factura original per al temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per les hores i l'import en el detall de la línia de factura editada, reversió d'això i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per les hores restants i import després de deduir les xifres corregides en el detall de la línia de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació del crèdit complet d'una transacció de despeses facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a la despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a la despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació del crèdit parcial d'una transacció de despeses facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a una despesa.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura corregida, reversió d'això i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturar el crèdit complet d'una transacció de materials prèviament facturada.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversió de vendes facturades per a la quantitat i l'import del detall de línia de factura original per a materials.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nou valor real de vendes no facturades per a la quantitat i l'import del detall de línia de factura original per a materials.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturació del crèdit parcial d'una transacció de material.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Una reversió de vendes facturades per a la quantitat i l'import facturats al detall de línia de factura original per a materials.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nou valor real de vendes no facturades que es poden cobrar per la quantitat i l'import del detall de la línia de factura editat, una reversió d'aquesta i una venda facturada equivalent real.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per la quantitat restant i import després de deduir les xifres corregides en el detall de la línia de factura.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació del crèdit complet d'una transacció d'impostos facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per la quantitat i l'import en el detall de la línia de factura original per a l'impost.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de vendes sense facturar per la quantitat i l'import en el detall de la línia de factura original per a l'impost.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturació del crèdit parcial d'una transacció d'impostos facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per la quantitat i l'import facturat en el detall de la línia de factura original per a l'impost.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de venda no facturada imputable per la quantitat i l'import en el detall de la línia de factura correctiva editada, reversió d'això i valor real de venda facturada equivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturació del crèdit complet d'una fita facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes facturades per l'import en el detall de la línia de factura original per a la fita.
                </p>
                <p>
L'estat de la factura de la fita s'actualitza de <b>Factura de client comptabilitzada</b> a <b>Preparat per a facturació</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturació del crèdit parcial d'una fita facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
No s'admet aquest escenari.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
