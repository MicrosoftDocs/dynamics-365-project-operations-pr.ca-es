---
title: Implementar camps personalitzats per a l'aplicació mòbil del Microsoft Dynamics 365 Project Timesheet a l'iOS i l'Android
description: Aquest tema proporciona patrons habituals per a l'ús d'extensions per implementar camps personalitzats.
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: ca-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003007"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>Implementar camps personalitzats per a l'aplicació mòbil del Microsoft Dynamics 365 Project Timesheet a l'iOS i l'Android

[!include [banner](../includes/banner.md)]

Aquest tema proporciona patrons habituals per a l'ús d'extensions per implementar camps personalitzats. Es cobreixen els temes següents:

- Els diversos tipus de dades que admet el marc de camps personalitzats
- Com mostrar els camps només de lectura o editables en entrades del full d'hores i desar els valors proporcionats per l'usuari de nou a la base de dades
- Com mostrar els camps només de lectura a la capçalera del full d'hores
- Com integrar altres lògiques empresarials personalitzades per introduir valors per defecte als camps i fer una validació addicional

## <a name="audience"></a>Audiència

Aquest tema està dissenyat per a desenvolupadors que integren els seus camps personalitzats a l'aplicació mòbil  del Microsoft Dynamics 365 Project Timesheet que està disponible per a Apple iOS i Google Android. S'assumeix és que els lectors estan familiaritzats amb el desenvolupament amb X++ i la funcionalitat de full d'hores del projecte.

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>Contracte de dades: classe X++ TSTimesheetCustomField

La classe **TSTimesheetCustomField** és la classe de contracte de dades d'X++ que representa informació sobre un camp personalitzat per a la funcionalitat de full d'hores. Les llistes dels objectes de camp personalitzats es passen tant al contracte de dades TSTimesheetDetails com al contracte de dades de TSTimesheetEntry per mostrar els camps personalitzats a l'aplicació mòbil.

- **TSTimesheetDetails**: contracte de la capçalera del full d'hores.
- **TSTimesheetEntry**: contracte de transacció del full d'hores. Els grups d'aquests objectes que tenen la mateixa informació de projecte i el valor **timesheetLineRecId** constitueixen una línia.

### <a name="fieldbasetype-types"></a>fieldBaseType (tipus)

La propietat **FieldBaseType** de l'objecte **TsTimesheetCustom** determina el tipus de camp que es mostra a l'aplicació. Els valors de **Tipus** següents estan admesos.

| Valor de Tipus | Type              | Notes |
|-------------|-------------------|-------|
| 0           | Cadena (i Enum) | El camp es mostra com un camp de text. |
| 1           | Integer           | El valor es mostra com un nombre sense posicions decimals. |
| 2           | Real              | El valor es mostra com un nombre amb posicions decimals.<p>Per mostrar el valor real com a moneda a l'aplicació, utilitzeu la propietat **fieldExtenededType**. Podeu utilitzar la propietat **numberOfDecimals** per definir el nombre de posicions decimals que es mostren.</p> |
| 3           | Date              | Els formats de data estan determinats pel paràmetre **Format de les dates, hores i números** que s' especifica a la **Preferència de llengua i de país/regió** a **Opcions de l'usuari**. |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- Si la propietat **stringOptions** no està proporcionada a l'objecte **TSTimesheetCustomField**, es proporciona un camp de text lliure a l'usuari.

    La propietat **stringLength** es pot utilitzar per definir la longitud de cadena màxima que poden introduir els usuaris.

- Si la propietat **stringOptions** està proporcionada a l'objecte **TSTimesheetCustomField**, aquests elements de llista són els únics valors que els usuaris poden seleccionar mitjançant botons d'opció (botons de selecció).

    En aquest cas, el camp de cadena pot actuar com un valor d'enumeració per a la finalitat de l'entrada de l'usuari. Per desar el valor a la base de dades com una enumeració, heu d'assignar manualment el valor de cadena al valor de l'enumeració abans de desar-lo a la base de dades mitjançant la cadena d'ordres (vegeu la secció "Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada de temps de l'aplicació a la base de dades" més endavant en aquest tema per veure un exemple).

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

Podeu utilitzar aquesta propietat per formatar els valors reals com a moneda. Aquest mètode només és aplicable quan el valor **fieldBaseType** és **Real**.

- **TSCustomFieldExtendedType:None**: no s'aplica cap format.
- **TSCustomFieldExtendedType::Currency**: formata el valor com a moneda.

    Quan el format de moneda està actiu, el camp **stringValue** es pot utilitzar per enviar el codi de moneda que s'ha de mostrar a l'aplicació. El valor és un valor només de lectura.

    El camp **realValue** conté la quantitat de diners que s'ha de desar a la base de dades.

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

Podeu utilitzar aquesta propietat per especificar on hauria d'aparèixer el camp personalitzat a l'aplicació.

- **TSCustomFieldSection::Header**: el camp es mostrarà a la secció **Visualitza més detalls** de l'aplicació. Aquests camps són sempre només de lectura.
- **TSCustomFieldSection::Line**: el camp apareixerà després de tots els camps de fàbrica en entrades del full d'hores. Aquests camps poden ser editables o només de lectura.

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

Aquesta propietat identifica el camp quan els valors que proporciona l'aplicació es desen a la base de dades.

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

Aquesta propietat identifica el camp quan els valors que proporciona l'aplicació es desen a la base de dades.

### <a name="iseditable-noyes"></a>isEditable (NoYes)

Definiu aquesta propietat a **Yes** per especificar que els usuaris puguin editar el camp de la secció d'entrada del full d'hores. Definiu la propietat a **No** per fer que el camp sigui només de lectura.

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

Definiu aquesta propietat a **Yes** per especificar que el camp de la secció d'entrada del full d'hores és obligatori.

### <a name="label-str"></a>label (str)

Aquesta propietat especifica l'etiqueta que es mostra al costat del camp a l'aplicació.

### <a name="stringoptions-list-of-strings"></a>stringOptions (llista de cadenes)

Aquesta propietat només és aplicable quan **fieldBaseType** està definit com a **String**. Si es defineix **stringOptions**, els valors de cadena que estan disponibles per a la selecció mitjançant els botons d'opció (botons de selecció) s'especifiquen per les cadenes de la llista. Si no es proporciona cap cadena, es permet l'entrada de text lliure al camp de cadena (vegeu la secció "Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada del full d'hores de l'aplicació de nou a la base de dades" més endavant en aquest tema per veure un exemple).

### <a name="stringlength-int"></a>stringLength (int)

Aquesta propietat especifica la longitud màxima d'un camp de cadena. Només és aplicable quan **fieldBaseType** està definit com a **String**.

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

Aquesta propietat especifica el nombre de decimals que es mostren per a un camp real. Només és aplicable quan **fieldBaseType** està definit com a **Real**.

### <a name="ordersequence-int"></a>orderSequence (int)

Aquesta propietat controla l'ordre en què es mostren els camps personalitzats a l'aplicació quan s'especifica més d'un camp personalitzat. Els camps que tenen nombres menors es mostren en primer lloc.

### <a name="booleanvalue-boolean"></a>booleanValue (boolean)

Per als camps del tipus **Boolean**, aquesta propietat envia el valor booleà del camp entre el servidor i l'aplicació.

### <a name="guidvalue-guid"></a>guidValue (guid)

Per als camps del tipus **GUID**, aquesta propietat envia el valor d'identificador únic global (GUID) del camp entre el servidor i l'aplicació.

### <a name="int64value-int64"></a>int64Value (int64)

Per als camps del tipus **Int64**, aquesta propietat envia el valor int64 del camp entre el servidor i l'aplicació.

### <a name="intvalue-int"></a>intValue (int)

Per als camps del tipus **Int**, aquesta propietat envia el valor int del camp entre el servidor i l'aplicació.

### <a name="realvalue-real"></a>realValue (real)

Per als camps del tipus **Real**, aquesta propietat envia el valor real del camp entre el servidor i l'aplicació.

### <a name="stringvalue-str"></a>stringValue (str)

Per als camps del tipus **String**, aquesta propietat envia el valor de cadena del camp entre el servidor i l'aplicació. També s'utilitza per als camps del tipus **Real** que tenen el format de moneda. Per a aquests camps, la propietat s'utilitza per enviar el codi de la moneda a l'aplicació.

### <a name="datevalue-date"></a>dateValue (date)

Per als camps del tipus **Date**, aquesta propietat envia el valor de data del camp entre el servidor i l'aplicació.

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>Mostrar i desar un camp personalitzat a la secció d'entrada del full d'hores

A continuació es mostra una captura de pantalla de l'aplicació mòbil d'una creació d'entrades del full d'hores. Mostra els camps de fàbrica i un camp personalitzat a la secció "Entrada de temps" anomenat "Cadena de prova" amb un valor d'enumeració de "Segona opció" que ja s'ha definit.

![Camp personalitzat de cadena de prova a l'aplicació](media/timesheet-entry.jpg)



A continuació es mostra una captura de pantalla de l'aplicació mòbil de l'usuari seleccionant una de les opcions de l'enumeració disponible per al camp personalitzat "Cadena de prova".  Les dues opcions són "Primera opció" i "Segona opció", que es mostren com a botons de selecció. La segona opció està seleccionada actualment.

![Botons d'opció (botons de selecció) per al camp personalitzat Cadena de prova](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>Ampliar la taula TSTimesheetLine perquè tingui un camp personalitzat

En escenaris típics, és probable que les dades d'un camp personalitzat a la secció d'entrades del full d'hores es desin a la taula TSTimesheetLine. No obstant, es poden utilitzar altres taules si les dades es poden recuperar basant-se en un registre TSTimesheetTrans que es proporciona o bé si no té un context de registre específic (per exemple, si el camp es defineix com a només de lectura en els paràmetres del projecte).

Tingueu en compte que els camps personalitzats no cal que tinguin registres de suport a la base de dades. Es poden generar de manera dinàmica basant-se en la lògica d'X++. Aquest enfocament pot ser útil en escenaris de només de lectura (vegeu la secció "Utilitzar la cadena d'odres a la classe TSTimesheetDetails, mètode buildCustomFieldListForHeader per omplir els detalls del full d'hores" per veure un exemple de valors de camp personalitzats generats dinàmicament.)

A continuació es mostra una captura de pantalla del Visual Studio de l'arbre d'objectes de l'aplicació. Mostra una extensió de la taula TSTimesheetLine amb el camp TestLineString afegit com a camp personalitzat.

![Cadena de línia](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>Utilitzar la cadena d'ordres en el mètode buildCustomFieldList de la classe TSTimesheetSettings per mostrar un camp a la secció d'entrada del full d'hores

Aquest codi controla la configuració de visualització del camp a l'aplicació. Per exemple, controla el tipus de camp, l'etiqueta, si el camp és obligatori i en quina secció apareix el camp.

A l'exemple següent es mostra un camp de cadena a les entrades de temps. Aquest camp té dues opcions, **Primera opció** i **Segona opció**, que estan disponibles mitjançant botons d'opció (botons de selecció). El camp de l'aplicació està associat amb el camp **TestLineString** que s'afegeix a la taula TSTimesheetLine.

Fixeu-vos en l'ús del mètode **TSTimesheetCustomField::newFromMetatdata()** per simplificar la inicialització de les propietats d'un camp personalitzat: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** i **numberOfDecimals**. També podeu configurar aquests paràmetres manualment, com preferiu.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>Utilitzar la cadena d'ordres en el mètode buildCustomFieldListForEntry de la classe TSTimesheetEntry per introduir valors en una entrada del full d'hores

El mètode **buildCustomFieldListForEntry** s'utilitza per introduir valors a les línies del full d'hores desat a l'aplicació mòbil. Es necessita un registre TSTimesheetTrans com a paràmetre. Els camps d'aquest registre es poden utilitzar per emplenar el valor del camp personalitzat a l'aplicació.

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada del full d'hores de l'aplicació de nou a la base de dades

Per desar un camp personalitzat a la base de dades en l'ús típic, heu d'ampliar diversos mètodes:

- El mètode **timesheetLineNeedsUpdating** s'utilitza per determinar si l'usuari ha canviat el registre de la línia a l'aplicació i s'ha de desar a la base de dades. Si el rendiment no és una preocupació, aquest mètode es pot simplificar per tal que sempre retorni **true**.
- Es poden ampliar els mètodes **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** de manera que introdueixin els valors al registre de la base de dades TSTimesheetLine del registre de contracte de dades TSTimesheetEntry que es proporciona. A l'exemple següent, observeu com l'assignació entre el camp de la base de dades i el camp d'entrada es fa manualment mitjançant codi X++.
- El mètode **populateTimesheetWeekFromEntry** també es pot ampliar si el camp personalitzat que s'assigna a l'objecte **TSTimesheetEntry** ha d'escriure a la taula de la base de dades TSTimesheetLineweek.

> [!NOTE]
> L'exemple següent Desa el valor **firstOption** o **secondOption** que l'usuari seleccioni a la base de dades com un valor de cadena sense processar. Si el camp de la base de dades és un camp del tipus **Enum**, aquests valors es poden assignar manualment a un valor d'enumeració i després es desen en un camp d'enumeració a la taula de la base de dades.

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>Mostrar un camp personalitzat a la secció de capçalera del full d'hores

A continuació es mostra una captura de l'aplicació mòbil de la pantalla d'un usuari visualitzant un full d'hores. El botó "Més informació" s'ha seleccionat a la cantonada superior dreta per mostrar l'opció "Visualitza més detalls".  

![Ordre Visualitza més detalls](media/show-more.png)

A continuació es mostra una captura de l'aplicació mòbil que mostra la secció "Més" d'un full d'hores. Un camp personalitzat anomenat "Relació d'ús d'aquest full d'hores (camp personalitzat calculat)" s'ha afegit a la secció de capçalera del full d'hores. Un valor només de lectura "0.667" es defineix en el camp personalitzat.

![Secció Més](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>Ampliar la taula TSTimesheetTable perquè tingui un camp personalitzat

En escenaris típics, és probable que les dades d'un camp personalitzat a la secció de capçalera es recuperin de la taula TSTimesheetHeader. No obstant, es poden utilitzar altres taules si les dades es poden recuperar basant-se en un registre TSTimesheetTable que es proporciona o bé si no té un context de registre específic (per exemple, si el camp es defineix com a només de lectura en els paràmetres del projecte).

Tingueu en compte que els camps personalitzats no cal que tinguin registres de suport a la base de dades. Es poden generar de manera dinàmica basant-se en la lògica d'X++. L'exemple següent mostra aquest enfocament.

Els camps de la secció de capçalera són sempre només de lectura a l'aplicació.

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>Utilitzar la cadena d'ordres en el mètode buildCustomFieldList de la classe TSTimesheetSettings per mostrar un camp a la secció de capçalera

Aquest codi controla la configuració de visualització del camp a l'aplicació. Per exemple, controla el tipus de camp, l'etiqueta, si el camp és obligatori i en quina secció apareix el camp.

A l'exemple següent es mostra un valor calculat a la secció de capçalera de l'aplicació.

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>Utilitzar la cadena d'ordres en el mètode buildCustomFieldListForHeader de la classe TSTimesheetDetails per emplenar els detalls d'un full d'hores

El mètode **buildCustomFieldListForHeader** s'utilitza per emplenar els detalls de la capçalera del full d'hores a l'aplicació mòbil. Es necessita un registre TSTimesheetTable com a paràmetre. Els camps d'aquest registre es poden utilitzar per emplenar el valor del camp personalitzat a l'aplicació. L'exemple següent no llegeix cap valor de la base de dades. En lloc d'això, utilitza la lògica d'X++ per generar un valor calculat que es mostrarà a l'aplicació.


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>Altres oportunitats de configurabilitat i extensibilitat

### <a name="adding-additional-validation-for-the-app"></a>Afegir una validació addicional per a l'aplicació

La lògica existent per a la funcionalitat del full d'hores al nivell de la base de dades continuarà funcionant de la manera que s'esperava. Per interrompre la finalització de l'operació de desament o enviament i mostrar un missatge d'error específic, podeu afegir **throw error("missatge a l'usuari")** al codi mitjançant una extensió de la cadena d'ordres. Aquí teniu tres exemples de mètodes útils ampliables:

- Si **validateWrite** a la taula TSTimesheetLine retorna **false** durant una operació de desament per a una línia del full d'hores, es mostrarà un missatge d'error a l'aplicació mòbil.
- Si **validateSubmit** a la taula TSTimesheetTable retorna **false** durant una operació d'enviament a l'aplicació, es mostra un missatge d'error a l'usuari.
- La lògica que emplena els camps (per exemple, **Propietat de la línia**) durant el mètode **insert** a la taula de TSTimesheetLine continuarà executant-se.

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>Amagar i marcar camps de fàbrica com a només de lectura mitjançant la configuració

A la llista de paràmetres del projecte, podeu crear camps de només de lectura o ocults a l'aplicació mòbil. Definiu les opcions de la secció **Fulls d'hores mòbils** a la pestanya **Full d'hores** de la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.

![Paràmetres del projecte](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>Canviar les activitats disponibles per a la selecció mitjançant extensions

Les activitats que estan disponibles per a la selecció d'un projecte s'emplenen mitjançant els mètodes **getActivitiesForProject()** i **getActivityQuery()** a la classe **TsTimesheetProjectService**. Podeu utilitzar la cadena d'ordres per canviar aquest comportament per tal que coincideixi amb el vostre escenari empresarial per a les activitats disponibles per a la selecció d'un projecte concret.

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>Introduir una categoria de projecte per defecte en entrades del full d'hores

L'entrada d'una categoria de projecte per defecte en les entrades del full d'hores es produeix en tres nivells. Podeu utilitzar la cadena d'ordres per ampliar el comportament en qualsevol o tots aquests nivells per aconseguir el comportament desitjat. S'utilitza la jerarquia següent:

1. L'aplicació prova de col·locar la categoria per defecte del recurs del projecte. Aquesta categoria per defecte es defineix als mètodes **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** a la classe **TSTimesheetSettingsService**.
2. Si la categoria per defecte no es proporciona al nivell de recursos del projecte, l'aplicació prova de recuperar-la de l'activitat del projecte. Aquesta categoria per defecte es defineix en el mètode **getActivitiesForProject** a la classe **TSTimesheetProjectService**.
3. Si la categoria per defecte no es proporciona al nivell d'activitat del projecte, la categoria per defecte s'obté dels paràmetres del projecte. Aquesta categoria per defecte es defineix en el mètode **getProjectDetailsbyRule** a la classe **TSTimesheetProjectService**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]