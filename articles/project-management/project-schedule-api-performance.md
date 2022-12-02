---
title: Rendiment d'API de planificació de projectes
description: Aquest article proporciona informació sobre els paràmetres de rendiment de les API de planificació del projecte i identifica pràctiques recomanades per a un ús òptim.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: ca-ES
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911170"
---
# <a name="project-schedule-api-performance"></a>Rendiment d'API de planificació de projectes

_**S'aplica a:** Project Operations per a escenaris basats en recursos/no mantinguts en existències, implementació bàsica: tracte de facturació proforma, Project for the web_

Aquest article proporciona informació sobre els paràmetres de rendiment de les interfícies de programació d'aplicacions (API) de planificació del projecte i identifica pràctiques recomanades per optimitzar l'ús.

## <a name="project-scheduling-service"></a>Servei de planificació de projectes
El servei de planificació de projectes és un servei de diversos inquilins que s'executa al Microsoft Azure. Està dissenyat per millorar la interacció proporcionant una experiència ràpida i fluïda quan els usuaris treballen en projectes. Aquesta millora s'aconsegueix acceptant sol·licituds de canvi, processant-les i retornant immediatament el resultat. El servei continua de manera asíncrona al Dataverse i no bloqueja les altres operacions que duen a terme els usuaris.

Les API de planificació de projectes es basen en el Servei de planificació de projectes per executar sol·licituds que es descriuen amb més detall a les seccions posteriors d'aquest article.

Les API de planificació de projectes estan dissenyades per treballar amb les entitats d'estructura del desglossament del treball (WBS) següents:

  - Project
  - Tasca del projecte
  - Dependència de les tasques del projecte
  - Membre de l'equip del projecte
  - Assignació de recursos
  
Tant els camps estàndard com els camps personalitzats estan admesos. Sempre que no s'especifiqui el contrari, s'admeten totes les operacions habituals, com ara la creació, l'actualització i la supressió. Per obtenir més informació, vegeu [Utilitzar les API de planificació de projectes per realitzar operacions i planificar entitats](schedule-api-preview.md).

Com a part de les API de planificació de projectes, s'ha afegit un patró d'unitat de treball. Aquest patró es coneix com a OperationSet i es pot utilitzar quan cal processar diverses sol·licituds en una única transacció.

A la il·lustració següent es mostra el flux que seguirà un associat quan utilitzi aquesta característica.

![Dataverse i el flux del servei de planificació de projectes.](./media/dataverse-project-scheduling-service-flow.png)

**Pas 1**: un client fa una crida d'API a un extrem de protocol de dades obert (OData) Dataverse per crear un OperationSet.

**Pas 2**: després de crear el nou OperationSet, es retorna un valor **OperationSetId**.

**Pas 3**: el client utilitza el valor **OperationSetId** per fer una altra sol·licitud d'API de planificació de projectes. El resultat és una sol·licitud de creació, actualització o supressió d'una entitat de planificació. Quan es fa aquesta sol·licitud, es duu a terme la validació de metadades. Si es produeix un error en la validació, la sol·licitud acaba i es retorna un error.

**Passos 4a-4c**: aquests passos representen la fase ACCEPT. El client crida l'API **ExecuteOperationSetV1**, que envia tots els canvis al servei de planificació de projectes en un lot. El servei de planificació de projectes executa les seves pròpies validacions segons les sol·licituds del lot. Qualsevol error de validació desfà el lot i retorna una excepció a l'element de crida. Si el servei de planificació de projectes accepta correctament el lot, l'estat d'OperationSet s'actualitza per reflectir el fet que l'OperationSet s'està processant amb el servei de planificació de projectes.

**Pas 5**: aquest pas representa la fase PERSIST. El servei de planificació de projectes escriu de manera asíncrona el lot al Dataverse en una transacció. Si l'operació d'escriptura es completa correctament, l'OperationSet es marca com a **Completat**. Tots els errors es tornen a desplegar a la transacció i el lot, i l'OperationSet es marca com a **Error**.

## <a name="performance-methodology"></a>Metodologia de rendiment
El temps d'execució es defineix com el moment des de la crida de l'API **ExecuteOperationSetV1** fins que el servei de planificació de projectes ha acabat d'escriure al Dataverse. Totes les operacions s'executen 2.200 vegades en combinació i s'informa dels mesuraments de temps d'execució P99. Es mesuren les operacions d'un sol registre i massives.

Per a una operació d'un sol registre, l'OperationSet conté una sol·licitud. Per a les operacions massives, conté 20, 50 o 100 sol·licituds. Cada mida massiva s'informa per separat.

Aquestes operacions s'executen en una implementació de l'UR 15 Project Operations Lite a l'Amèrica del Nord.

## <a name="results"></a>Resultats
### <a name="create-operations"></a>Crear operacions
#### <a name="single-record-create-operations"></a>Operacions de creació d'un sol registre
A la taula següent es mostren els temps d'execució per a la creació d'un sol registre. Les hores són en segons.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipus&nbsp;&nbsp;&nbsp;de registre</th>
    <th class="tg-0lax" colspan="2">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tasca</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assignació</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre de l'equip</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependència</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operacions de creació massiva
A la taula següent es mostren els temps d'execució per a la creació de molts registres. En concret, Microsoft ha mesurat els temps d'execució per a la creació de 20, 50 i 100 registres en un únic OperationSet. Les hores són en segons.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipus&nbsp;&nbsp;&nbsp;de registre</th>
    <th class="tg-0lax" colspan="6">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registres</th>
    <th class="tg-0lax" colspan="2">50 registres</th>
    <th class="tg-0lax" colspan="2">100 registres</th>
  </tr>
  <tr>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tasca</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assignació</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependència</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Les operacions de creació massiva a les entitats **Projecte** i **Membre de l'equip** no s'inclouen en aquesta taula, perquè el temps d'execució d'aquestes operacions s'assembla al temps d'execució quan l'API per crear un sol registre es crida diverses vegades. Aquestes API s'executen immediatament al Dataverse.

A la il·lustració següent es mostra un traçat de les hores d'execució de les entitats **Tasca**, **Assignació** i **Dependència** quan es creen 20, 50 i 100 registres i s'utilitzen tots els camps compatibles.

![Gràfic de temps d'execució de la creació de registres.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operacions d'actualització
#### <a name="single-record-update-operations"></a>Operacions d'actualització d'un sol registre
A la taula següent es mostren els temps d'execució per a les actualitzacions d'un sol registre. Les hores són en segons.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipus&nbsp;&nbsp;&nbsp;de registre</th>
    <th class="tg-0lax" colspan="2">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">Camps obligatoris </th>
    <th class="tg-0lax">Tots els camps admesos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tasca</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre de l'equip</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les operacions d'actualització a les entitats **Assignacions de recursos** i **Dependència de tasques del projecte** no estan admeses.

#### <a name="bulk-update-operations"></a>Operacions d'actualització massiva
A la taula següent es mostren els temps d'execució per a les actualitzacions de molts registres. En concret, Microsoft ha mesurat els temps d'execució per a les actualitzacions de 20, 50 i 100 registres en un únic OperationSet. Les hores són en segons.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Tipus&nbsp;&nbsp;&nbsp;de registre</th>
    <th class="tg-0lax" colspan="6">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 registres</th>
    <th class="tg-0lax" colspan="2">50 registres</th>
    <th class="tg-0lax" colspan="2">100 registres</th>
  </tr>
  <tr>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
    <th class="tg-0lax">Camps obligatoris</th>
    <th class="tg-0lax">Tots els camps admesos</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tasca</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre de l'equip</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les operacions d'actualització a les entitats **Assignacions de recursos** i **Dependència de tasques del projecte** no estan admeses.

A la il·lustració següent es mostra un traçat de les hores d'execució de les entitats Tasca i Membre de l'equip quan s'actualitzen 20, 50 i 100 registres i s'utilitzen tots els camps compatibles.

![Gràfic de temps d'execució d'actualització de registres.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operacions de supressió
#### <a name="single-record-delete-operations"></a>Operacions de supressió d'un sol registre
A la taula següent es mostren els temps d'execució per a la supressió d'un sol registre. Les hores són en segons.

| Tipus de registre | Temps  |
|-------------|-------|
| Tasca        | 20.12 |
| Assignació  | 10.86 |
| Membre de l'equip | 12.52 |
| Dependència  | 20.89 |

> [!NOTE]
> Les operacions de supressió de l'entitat **Projecte** no estan admeses.

#### <a name="bulk-delete-operations"></a>Operacions de supressió massiva
A la taula següent es mostren els temps d'execució per a la supressió de molts registres. En concret, Microsoft ha mesurat els temps d'execució per a la supressió de 20, 50 i 100 registres en un únic OperationSet. Les hores són en segons.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Tipus&nbsp;&nbsp;&nbsp;de registre</th>
    <th class="tg-0lax" colspan="3">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 registres</th>
    <th class="tg-0lax">50 registres</th>
    <th class="tg-0lax">100 registres</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tasca</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Assignació</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre de l'equip</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependència</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les operacions de supressió de l'entitat **Projecte** no estan admeses.

A la il·lustració següent es mostra un traçat de les hores d'execució de les entitats **Tasca**, **Assignació**, **Membre de l'equip** i **Dependència** quan se suprimeixen 20, 50 i 100 registres.

![Gràfic de temps d'execució de la supressió de registres.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observacions
Per a cada operació de registre, l'API **ExecuteOperationSet** triga aproximadament 800 mil·lisegons per enviar una sol·licitud al servei de planificació de projectes. El servei de planificació de projectes triga aproximadament cinc segons a processar la càrrega i a cridar el Dataverse. La resta del temps d'execució es dedica a executar lògica empresarial i escriure dades a la base de dades del Dataverse.

Quan es creen, s'actualitzen o se suprimeixen 100 registres, l'API **ExecuteOperationSet** triga aproximadament tres segons a enviar la sol·licitud al servei de planificació de projectes. El servei de planificació de projectes triga aproximadament cinc segons a processar les sol·licituds i a cridar el Dataverse. Les operacions massives han de pagar un **impost de servei de planificació de projectes** cada vegada, per a tots els registres de l'OperationSet. Per tant, les operacions massives tenen un temps d'execució mitjà significativament inferior a les operacions d'un sol registre.

## <a name="scenarios"></a>Escenaris
A la taula següent es mostren els temps d'execució quan s'utilitzen les API de planificació de projectes per aconseguir escenaris específics. Les hores són en segons.

| Escenari                                                                   | Temps  |
|----------------------------------------------------------------------------|-------|
| Creeu un projecte que tingui 40 tasques.                                      | 36.01 |
| Creeu un projecte que tingui 40 tasques i 20 dependències.                  | 38.11 |
| Creeu un projecte que tingui 40 tasques i 30 assignacions.                   | 60.17 |
| Creeu un projecte que tingui 40 tasques, 20 dependències i 30 assignacions. | 60.27 |

## <a name="best-practices"></a>Procediments recomanats
Segons els resultats de l'escenari anterior, les API tenen un rendiment millor en les condicions següents:

  - Agrupeu tantes operacions com sigui possible. El temps d'execució mitjà per a les operacions massives és millor que el temps d'execució mitjà per a les operacions d'un sol registre. Com més petit sigui el nombre d'OperationSets que s'utilitzi, més curt serà el temps d'execució mitjà.
  - Definiu només els atributs mínims necessaris per aconseguir el vostre escenari. Sigueu selectiu sobre els tipus de camps no obligatoris inclosos en una sol·licitud d'OperationSet. Els camps que contenen claus externes o camps de valor consolidat afectaran negativament el rendiment.
