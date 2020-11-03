---
title: Crèdits i factures corregides
description: Aquest tema proporciona informació sobre factures corregides al Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072323"
---
# <a name="credits-and-corrected-invoices"></a>Crèdits i factures corregides

_**S'aplica a:** implementació bàsica: tracte de facturació proforma_

Una factura confirmada del projecte es pot corregir per processar canvis o crèdits com s'hagin negociat amb el client i l'administrador del projecte.

Per fer modificacions a una factura confirmada, obriu la factura confirmada i seleccioneu **Corregeix aquesta factura**. 

> [!NOTE]
> Aquesta selecció no està disponible tret que es confirmi una factura de projecte.

Es crea un nou esborrany de factura a partir de la factura confirmada. Tots els detalls de la línia de factura de la factura confirmada anteriorment es copien al nou esborrany. Els següents són alguns dels punts clau per entendre els detalls de la línia sobre la nova factura corregida:

- Totes les quantitats s'actualitzen a zero. L'aplicació assumeix que tots els elements facturats estan completament acreditats. Si cal, podeu actualitzar manualment aquestes quantitats per reflectir la quantitat que s'està facturant i no la quantitat que s'està acreditant. Segons la quantitat que introduïu, l'aplicació calcula la quantitat acreditada. Aquesta quantitat es reflecteix en els valor reals que es creen quan es confirma la factura corregida. Si s'introdueixen canvis en l'import de l'impost, s'ha d'introduir l'import de l'impost correcte i no l'import de l'impost que s'ha acreditat.
- Les línies de contracte basades en productes confirmades prèviament no es copien. No s'admet el processament de correccions en una factura de projecte basada en productes.
- Les correccions de fites sempre es processen com a crèdits complets.
- Es poden corregir els imports de bestreta o d'avançament si s'ha facturat al client un import incorrecte.
- Les conciliacions de retencions i avançaments es poden corregir si s'ha utilitzat un import incorrecte per conciliar els càrrecs d'una factura confirmada prèviament.

> [!IMPORTANT]
> Els detalls de la línia de factura que són correccions a altres càrrecs ja facturat tenen el camp **Correcció** establert a **Sí**. Les factures que han corregit els detalls de la línia de factura tenen un camp anomenat **Té correccions** que també s'estableix a **Sí**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Valors reals creats a la confirmació d'una factura correctiva:

A continuació es mostren els valors reals creats per l'aplicació a la confirmació d'una correcció segons les operacions realitzades en l'esborrany de factura correctiva abans de la confirmació.

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
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmeu la correcció d'un avançament o bestreta facturat.<strong></strong>
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
Es crea un valor real de reversió de vendes facturades per l'import de la bestreta o l'avançament per revertir les vendes facturades originals.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Es crea un nou valor real de vendes facturades per a l'import corregit en la línia de factura corregida basada en una bestreta o avançament.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda no facturada de l'import negatiu de la línia de factura corregida basada en una bestreta o avançament que s'utilitzarà per a la conciliació.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmació de la correcció d'una bestreta o avançament conciliat prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Reversió de vendes no facturada de la bestreta o avançament creat per a la conciliació. Aquest import és positiu i està destinada a cancel·lar el negatiu creat quan es va crear la conciliació anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de reversió de vendes facturades per l'import de la factura anterior.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Nou valor real de vendes facturades per a l'import de bestreta corregit que s'aplica a la factura corregida.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Valor real de venda no facturada amb un import negatiu de la bestreta o avançament restant corregir que s'utilitzarà per a la conciliació en factures posteriors.
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
L'estat de facturació o factura de la fita de la línia de contracte del projecte s'actualitza a **A punt per a la facturació**.
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
No admesos </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Crèdits i correccions d'una línia de contracte basada en productes facturada prèviament.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
No admesos </p>
            </td>
        </tr>
    </tbody>
</table>