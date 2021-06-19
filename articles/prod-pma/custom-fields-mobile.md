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
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="641ce-103">Implementar camps personalitzats per a l'aplicació mòbil del Microsoft Dynamics 365 Project Timesheet a l'iOS i l'Android</span><span class="sxs-lookup"><span data-stu-id="641ce-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="641ce-104">Aquest tema proporciona patrons habituals per a l'ús d'extensions per implementar camps personalitzats.</span><span class="sxs-lookup"><span data-stu-id="641ce-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="641ce-105">Es cobreixen els temes següents:</span><span class="sxs-lookup"><span data-stu-id="641ce-105">The following topics are covered:</span></span>

- <span data-ttu-id="641ce-106">Els diversos tipus de dades que admet el marc de camps personalitzats</span><span class="sxs-lookup"><span data-stu-id="641ce-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="641ce-107">Com mostrar els camps només de lectura o editables en entrades del full d'hores i desar els valors proporcionats per l'usuari de nou a la base de dades</span><span class="sxs-lookup"><span data-stu-id="641ce-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="641ce-108">Com mostrar els camps només de lectura a la capçalera del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="641ce-109">Com integrar altres lògiques empresarials personalitzades per introduir valors per defecte als camps i fer una validació addicional</span><span class="sxs-lookup"><span data-stu-id="641ce-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="641ce-110">Audiència</span><span class="sxs-lookup"><span data-stu-id="641ce-110">Audience</span></span>

<span data-ttu-id="641ce-111">Aquest tema està dissenyat per a desenvolupadors que integren els seus camps personalitzats a l'aplicació mòbil  del Microsoft Dynamics 365 Project Timesheet que està disponible per a Apple iOS i Google Android.</span><span class="sxs-lookup"><span data-stu-id="641ce-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="641ce-112">S'assumeix és que els lectors estan familiaritzats amb el desenvolupament amb X++ i la funcionalitat de full d'hores del projecte.</span><span class="sxs-lookup"><span data-stu-id="641ce-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="641ce-113">Contracte de dades: classe X++ TSTimesheetCustomField</span><span class="sxs-lookup"><span data-stu-id="641ce-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="641ce-114">La classe **TSTimesheetCustomField** és la classe de contracte de dades d'X++ que representa informació sobre un camp personalitzat per a la funcionalitat de full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="641ce-115">Les llistes dels objectes de camp personalitzats es passen tant al contracte de dades TSTimesheetDetails com al contracte de dades de TSTimesheetEntry per mostrar els camps personalitzats a l'aplicació mòbil.</span><span class="sxs-lookup"><span data-stu-id="641ce-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="641ce-116">**TSTimesheetDetails**: contracte de la capçalera del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="641ce-117">**TSTimesheetEntry**: contracte de transacció del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="641ce-118">Els grups d'aquests objectes que tenen la mateixa informació de projecte i el valor **timesheetLineRecId** constitueixen una línia.</span><span class="sxs-lookup"><span data-stu-id="641ce-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="641ce-119">fieldBaseType (tipus)</span><span class="sxs-lookup"><span data-stu-id="641ce-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="641ce-120">La propietat **FieldBaseType** de l'objecte **TsTimesheetCustom** determina el tipus de camp que es mostra a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="641ce-121">Els valors de **Tipus** següents estan admesos.</span><span class="sxs-lookup"><span data-stu-id="641ce-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="641ce-122">Valor de Tipus</span><span class="sxs-lookup"><span data-stu-id="641ce-122">Types value</span></span> | <span data-ttu-id="641ce-123">Type</span><span class="sxs-lookup"><span data-stu-id="641ce-123">Type</span></span>              | <span data-ttu-id="641ce-124">Notes</span><span class="sxs-lookup"><span data-stu-id="641ce-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="641ce-125">0</span><span class="sxs-lookup"><span data-stu-id="641ce-125">0</span></span>           | <span data-ttu-id="641ce-126">Cadena (i Enum)</span><span class="sxs-lookup"><span data-stu-id="641ce-126">String (and Enum)</span></span> | <span data-ttu-id="641ce-127">El camp es mostra com un camp de text.</span><span class="sxs-lookup"><span data-stu-id="641ce-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="641ce-128">1</span><span class="sxs-lookup"><span data-stu-id="641ce-128">1</span></span>           | <span data-ttu-id="641ce-129">Integer</span><span class="sxs-lookup"><span data-stu-id="641ce-129">Integer</span></span>           | <span data-ttu-id="641ce-130">El valor es mostra com un nombre sense posicions decimals.</span><span class="sxs-lookup"><span data-stu-id="641ce-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="641ce-131">2</span><span class="sxs-lookup"><span data-stu-id="641ce-131">2</span></span>           | <span data-ttu-id="641ce-132">Real</span><span class="sxs-lookup"><span data-stu-id="641ce-132">Real</span></span>              | <span data-ttu-id="641ce-133">El valor es mostra com un nombre amb posicions decimals.</span><span class="sxs-lookup"><span data-stu-id="641ce-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="641ce-134">Per mostrar el valor real com a moneda a l'aplicació, utilitzeu la propietat **fieldExtenededType**.</span><span class="sxs-lookup"><span data-stu-id="641ce-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="641ce-135">Podeu utilitzar la propietat **numberOfDecimals** per definir el nombre de posicions decimals que es mostren.</span><span class="sxs-lookup"><span data-stu-id="641ce-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="641ce-136">3</span><span class="sxs-lookup"><span data-stu-id="641ce-136">3</span></span>           | <span data-ttu-id="641ce-137">Date</span><span class="sxs-lookup"><span data-stu-id="641ce-137">Date</span></span>              | <span data-ttu-id="641ce-138">Els formats de data estan determinats pel paràmetre **Format de les dates, hores i números** que s' especifica a la **Preferència de llengua i de país/regió** a **Opcions de l'usuari**.</span><span class="sxs-lookup"><span data-stu-id="641ce-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="641ce-139">4</span><span class="sxs-lookup"><span data-stu-id="641ce-139">4</span></span>           | <span data-ttu-id="641ce-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="641ce-140">Boolean</span></span>           | |
| <span data-ttu-id="641ce-141">15</span><span class="sxs-lookup"><span data-stu-id="641ce-141">15</span></span>          | <span data-ttu-id="641ce-142">GUID</span><span class="sxs-lookup"><span data-stu-id="641ce-142">GUID</span></span>              | |
| <span data-ttu-id="641ce-143">16</span><span class="sxs-lookup"><span data-stu-id="641ce-143">16</span></span>          | <span data-ttu-id="641ce-144">Int64</span><span class="sxs-lookup"><span data-stu-id="641ce-144">Int64</span></span>             | |

- <span data-ttu-id="641ce-145">Si la propietat **stringOptions** no està proporcionada a l'objecte **TSTimesheetCustomField**, es proporciona un camp de text lliure a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="641ce-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="641ce-146">La propietat **stringLength** es pot utilitzar per definir la longitud de cadena màxima que poden introduir els usuaris.</span><span class="sxs-lookup"><span data-stu-id="641ce-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="641ce-147">Si la propietat **stringOptions** està proporcionada a l'objecte **TSTimesheetCustomField**, aquests elements de llista són els únics valors que els usuaris poden seleccionar mitjançant botons d'opció (botons de selecció).</span><span class="sxs-lookup"><span data-stu-id="641ce-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="641ce-148">En aquest cas, el camp de cadena pot actuar com un valor d'enumeració per a la finalitat de l'entrada de l'usuari.</span><span class="sxs-lookup"><span data-stu-id="641ce-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="641ce-149">Per desar el valor a la base de dades com una enumeració, heu d'assignar manualment el valor de cadena al valor de l'enumeració abans de desar-lo a la base de dades mitjançant la cadena d'ordres (vegeu la secció "Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada de temps de l'aplicació a la base de dades" més endavant en aquest tema per veure un exemple).</span><span class="sxs-lookup"><span data-stu-id="641ce-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="641ce-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="641ce-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="641ce-151">Podeu utilitzar aquesta propietat per formatar els valors reals com a moneda.</span><span class="sxs-lookup"><span data-stu-id="641ce-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="641ce-152">Aquest mètode només és aplicable quan el valor **fieldBaseType** és **Real**.</span><span class="sxs-lookup"><span data-stu-id="641ce-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="641ce-153">**TSCustomFieldExtendedType:None**: no s'aplica cap format.</span><span class="sxs-lookup"><span data-stu-id="641ce-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="641ce-154">**TSCustomFieldExtendedType::Currency**: formata el valor com a moneda.</span><span class="sxs-lookup"><span data-stu-id="641ce-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="641ce-155">Quan el format de moneda està actiu, el camp **stringValue** es pot utilitzar per enviar el codi de moneda que s'ha de mostrar a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="641ce-156">El valor és un valor només de lectura.</span><span class="sxs-lookup"><span data-stu-id="641ce-156">The value is a read-only value.</span></span>

    <span data-ttu-id="641ce-157">El camp **realValue** conté la quantitat de diners que s'ha de desar a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="641ce-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="641ce-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="641ce-159">Podeu utilitzar aquesta propietat per especificar on hauria d'aparèixer el camp personalitzat a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="641ce-160">**TSCustomFieldSection::Header**: el camp es mostrarà a la secció **Visualitza més detalls** de l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="641ce-161">Aquests camps són sempre només de lectura.</span><span class="sxs-lookup"><span data-stu-id="641ce-161">These fields are always read-only.</span></span>
- <span data-ttu-id="641ce-162">**TSCustomFieldSection::Line**: el camp apareixerà després de tots els camps de fàbrica en entrades del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="641ce-163">Aquests camps poden ser editables o només de lectura.</span><span class="sxs-lookup"><span data-stu-id="641ce-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="641ce-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="641ce-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="641ce-165">Aquesta propietat identifica el camp quan els valors que proporciona l'aplicació es desen a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="641ce-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="641ce-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="641ce-167">Aquesta propietat identifica el camp quan els valors que proporciona l'aplicació es desen a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="641ce-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="641ce-168">isEditable (NoYes)</span></span>

<span data-ttu-id="641ce-169">Definiu aquesta propietat a **Yes** per especificar que els usuaris puguin editar el camp de la secció d'entrada del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="641ce-170">Definiu la propietat a **No** per fer que el camp sigui només de lectura.</span><span class="sxs-lookup"><span data-stu-id="641ce-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="641ce-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="641ce-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="641ce-172">Definiu aquesta propietat a **Yes** per especificar que el camp de la secció d'entrada del full d'hores és obligatori.</span><span class="sxs-lookup"><span data-stu-id="641ce-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="641ce-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="641ce-173">label (str)</span></span>

<span data-ttu-id="641ce-174">Aquesta propietat especifica l'etiqueta que es mostra al costat del camp a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="641ce-175">stringOptions (llista de cadenes)</span><span class="sxs-lookup"><span data-stu-id="641ce-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="641ce-176">Aquesta propietat només és aplicable quan **fieldBaseType** està definit com a **String**.</span><span class="sxs-lookup"><span data-stu-id="641ce-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="641ce-177">Si es defineix **stringOptions**, els valors de cadena que estan disponibles per a la selecció mitjançant els botons d'opció (botons de selecció) s'especifiquen per les cadenes de la llista.</span><span class="sxs-lookup"><span data-stu-id="641ce-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="641ce-178">Si no es proporciona cap cadena, es permet l'entrada de text lliure al camp de cadena (vegeu la secció "Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada del full d'hores de l'aplicació de nou a la base de dades" més endavant en aquest tema per veure un exemple).</span><span class="sxs-lookup"><span data-stu-id="641ce-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="641ce-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="641ce-179">stringLength (int)</span></span>

<span data-ttu-id="641ce-180">Aquesta propietat especifica la longitud màxima d'un camp de cadena.</span><span class="sxs-lookup"><span data-stu-id="641ce-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="641ce-181">Només és aplicable quan **fieldBaseType** està definit com a **String**.</span><span class="sxs-lookup"><span data-stu-id="641ce-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="641ce-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="641ce-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="641ce-183">Aquesta propietat especifica el nombre de decimals que es mostren per a un camp real.</span><span class="sxs-lookup"><span data-stu-id="641ce-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="641ce-184">Només és aplicable quan **fieldBaseType** està definit com a **Real**.</span><span class="sxs-lookup"><span data-stu-id="641ce-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="641ce-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="641ce-185">orderSequence (int)</span></span>

<span data-ttu-id="641ce-186">Aquesta propietat controla l'ordre en què es mostren els camps personalitzats a l'aplicació quan s'especifica més d'un camp personalitzat.</span><span class="sxs-lookup"><span data-stu-id="641ce-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="641ce-187">Els camps que tenen nombres menors es mostren en primer lloc.</span><span class="sxs-lookup"><span data-stu-id="641ce-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="641ce-188">booleanValue (boolean)</span><span class="sxs-lookup"><span data-stu-id="641ce-188">booleanValue (boolean)</span></span>

<span data-ttu-id="641ce-189">Per als camps del tipus **Boolean**, aquesta propietat envia el valor booleà del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="641ce-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="641ce-190">guidValue (guid)</span></span>

<span data-ttu-id="641ce-191">Per als camps del tipus **GUID**, aquesta propietat envia el valor d'identificador únic global (GUID) del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="641ce-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="641ce-192">int64Value (int64)</span></span>

<span data-ttu-id="641ce-193">Per als camps del tipus **Int64**, aquesta propietat envia el valor int64 del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="641ce-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="641ce-194">intValue (int)</span></span>

<span data-ttu-id="641ce-195">Per als camps del tipus **Int**, aquesta propietat envia el valor int del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="641ce-196">realValue (real)</span><span class="sxs-lookup"><span data-stu-id="641ce-196">realValue (real)</span></span>

<span data-ttu-id="641ce-197">Per als camps del tipus **Real**, aquesta propietat envia el valor real del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="641ce-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="641ce-198">stringValue (str)</span></span>

<span data-ttu-id="641ce-199">Per als camps del tipus **String**, aquesta propietat envia el valor de cadena del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="641ce-200">També s'utilitza per als camps del tipus **Real** que tenen el format de moneda.</span><span class="sxs-lookup"><span data-stu-id="641ce-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="641ce-201">Per a aquests camps, la propietat s'utilitza per enviar el codi de la moneda a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="641ce-202">dateValue (date)</span><span class="sxs-lookup"><span data-stu-id="641ce-202">dateValue (date)</span></span>

<span data-ttu-id="641ce-203">Per als camps del tipus **Date**, aquesta propietat envia el valor de data del camp entre el servidor i l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="641ce-204">Mostrar i desar un camp personalitzat a la secció d'entrada del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="641ce-205">A continuació es mostra una captura de pantalla de l'aplicació mòbil d'una creació d'entrades del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="641ce-206">Mostra els camps de fàbrica i un camp personalitzat a la secció "Entrada de temps" anomenat "Cadena de prova" amb un valor d'enumeració de "Segona opció" que ja s'ha definit.</span><span class="sxs-lookup"><span data-stu-id="641ce-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![Camp personalitzat de cadena de prova a l'aplicació](media/timesheet-entry.jpg)



<span data-ttu-id="641ce-208">A continuació es mostra una captura de pantalla de l'aplicació mòbil de l'usuari seleccionant una de les opcions de l'enumeració disponible per al camp personalitzat "Cadena de prova".</span><span class="sxs-lookup"><span data-stu-id="641ce-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="641ce-209">Les dues opcions són "Primera opció" i "Segona opció", que es mostren com a botons de selecció.</span><span class="sxs-lookup"><span data-stu-id="641ce-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="641ce-210">La segona opció està seleccionada actualment.</span><span class="sxs-lookup"><span data-stu-id="641ce-210">The second option is currently selected.</span></span>

![Botons d'opció (botons de selecció) per al camp personalitzat Cadena de prova](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="641ce-212">Ampliar la taula TSTimesheetLine perquè tingui un camp personalitzat</span><span class="sxs-lookup"><span data-stu-id="641ce-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="641ce-213">En escenaris típics, és probable que les dades d'un camp personalitzat a la secció d'entrades del full d'hores es desin a la taula TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="641ce-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="641ce-214">No obstant, es poden utilitzar altres taules si les dades es poden recuperar basant-se en un registre TSTimesheetTrans que es proporciona o bé si no té un context de registre específic (per exemple, si el camp es defineix com a només de lectura en els paràmetres del projecte).</span><span class="sxs-lookup"><span data-stu-id="641ce-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="641ce-215">Tingueu en compte que els camps personalitzats no cal que tinguin registres de suport a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="641ce-216">Es poden generar de manera dinàmica basant-se en la lògica d'X++.</span><span class="sxs-lookup"><span data-stu-id="641ce-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="641ce-217">Aquest enfocament pot ser útil en escenaris de només de lectura (vegeu la secció "Utilitzar la cadena d'odres a la classe TSTimesheetDetails, mètode buildCustomFieldListForHeader per omplir els detalls del full d'hores" per veure un exemple de valors de camp personalitzats generats dinàmicament.)</span><span class="sxs-lookup"><span data-stu-id="641ce-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="641ce-218">A continuació es mostra una captura de pantalla del Visual Studio de l'arbre d'objectes de l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="641ce-219">Mostra una extensió de la taula TSTimesheetLine amb el camp TestLineString afegit com a camp personalitzat.</span><span class="sxs-lookup"><span data-stu-id="641ce-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![Cadena de línia](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="641ce-221">Utilitzar la cadena d'ordres en el mètode buildCustomFieldList de la classe TSTimesheetSettings per mostrar un camp a la secció d'entrada del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="641ce-222">Aquest codi controla la configuració de visualització del camp a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="641ce-223">Per exemple, controla el tipus de camp, l'etiqueta, si el camp és obligatori i en quina secció apareix el camp.</span><span class="sxs-lookup"><span data-stu-id="641ce-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="641ce-224">A l'exemple següent es mostra un camp de cadena a les entrades de temps.</span><span class="sxs-lookup"><span data-stu-id="641ce-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="641ce-225">Aquest camp té dues opcions, **Primera opció** i **Segona opció**, que estan disponibles mitjançant botons d'opció (botons de selecció).</span><span class="sxs-lookup"><span data-stu-id="641ce-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="641ce-226">El camp de l'aplicació està associat amb el camp **TestLineString** que s'afegeix a la taula TSTimesheetLine.</span><span class="sxs-lookup"><span data-stu-id="641ce-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="641ce-227">Fixeu-vos en l'ús del mètode **TSTimesheetCustomField::newFromMetatdata()** per simplificar la inicialització de les propietats d'un camp personalitzat: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength** i **numberOfDecimals**.</span><span class="sxs-lookup"><span data-stu-id="641ce-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="641ce-228">També podeu configurar aquests paràmetres manualment, com preferiu.</span><span class="sxs-lookup"><span data-stu-id="641ce-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="641ce-229">Utilitzar la cadena d'ordres en el mètode buildCustomFieldListForEntry de la classe TSTimesheetEntry per introduir valors en una entrada del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="641ce-230">El mètode **buildCustomFieldListForEntry** s'utilitza per introduir valors a les línies del full d'hores desat a l'aplicació mòbil.</span><span class="sxs-lookup"><span data-stu-id="641ce-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="641ce-231">Es necessita un registre TSTimesheetTrans com a paràmetre.</span><span class="sxs-lookup"><span data-stu-id="641ce-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="641ce-232">Els camps d'aquest registre es poden utilitzar per emplenar el valor del camp personalitzat a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="641ce-233">Utilitzar la cadena d'ordres a la classe TSTimesheetEntryService per desar una entrada del full d'hores de l'aplicació de nou a la base de dades</span><span class="sxs-lookup"><span data-stu-id="641ce-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="641ce-234">Per desar un camp personalitzat a la base de dades en l'ús típic, heu d'ampliar diversos mètodes:</span><span class="sxs-lookup"><span data-stu-id="641ce-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="641ce-235">El mètode **timesheetLineNeedsUpdating** s'utilitza per determinar si l'usuari ha canviat el registre de la línia a l'aplicació i s'ha de desar a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="641ce-236">Si el rendiment no és una preocupació, aquest mètode es pot simplificar per tal que sempre retorni **true**.</span><span class="sxs-lookup"><span data-stu-id="641ce-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="641ce-237">Es poden ampliar els mètodes **populateTimesheetLineFromEntryDuringCreate** i **populateTimesheetLineFromEntryDuringUpdate** de manera que introdueixin els valors al registre de la base de dades TSTimesheetLine del registre de contracte de dades TSTimesheetEntry que es proporciona.</span><span class="sxs-lookup"><span data-stu-id="641ce-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="641ce-238">A l'exemple següent, observeu com l'assignació entre el camp de la base de dades i el camp d'entrada es fa manualment mitjançant codi X++.</span><span class="sxs-lookup"><span data-stu-id="641ce-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="641ce-239">El mètode **populateTimesheetWeekFromEntry** també es pot ampliar si el camp personalitzat que s'assigna a l'objecte **TSTimesheetEntry** ha d'escriure a la taula de la base de dades TSTimesheetLineweek.</span><span class="sxs-lookup"><span data-stu-id="641ce-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="641ce-240">L'exemple següent Desa el valor **firstOption** o **secondOption** que l'usuari seleccioni a la base de dades com un valor de cadena sense processar.</span><span class="sxs-lookup"><span data-stu-id="641ce-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="641ce-241">Si el camp de la base de dades és un camp del tipus **Enum**, aquests valors es poden assignar manualment a un valor d'enumeració i després es desen en un camp d'enumeració a la taula de la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="641ce-242">Mostrar un camp personalitzat a la secció de capçalera del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="641ce-243">A continuació es mostra una captura de l'aplicació mòbil de la pantalla d'un usuari visualitzant un full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="641ce-244">El botó "Més informació" s'ha seleccionat a la cantonada superior dreta per mostrar l'opció "Visualitza més detalls".</span><span class="sxs-lookup"><span data-stu-id="641ce-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![Ordre Visualitza més detalls](media/show-more.png)

<span data-ttu-id="641ce-246">A continuació es mostra una captura de l'aplicació mòbil que mostra la secció "Més" d'un full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="641ce-247">Un camp personalitzat anomenat "Relació d'ús d'aquest full d'hores (camp personalitzat calculat)" s'ha afegit a la secció de capçalera del full d'hores.</span><span class="sxs-lookup"><span data-stu-id="641ce-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="641ce-248">Un valor només de lectura "0.667" es defineix en el camp personalitzat.</span><span class="sxs-lookup"><span data-stu-id="641ce-248">A read-only value of "0.667" is set on the custom field.</span></span>

![Secció Més](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="641ce-250">Ampliar la taula TSTimesheetTable perquè tingui un camp personalitzat</span><span class="sxs-lookup"><span data-stu-id="641ce-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="641ce-251">En escenaris típics, és probable que les dades d'un camp personalitzat a la secció de capçalera es recuperin de la taula TSTimesheetHeader.</span><span class="sxs-lookup"><span data-stu-id="641ce-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="641ce-252">No obstant, es poden utilitzar altres taules si les dades es poden recuperar basant-se en un registre TSTimesheetTable que es proporciona o bé si no té un context de registre específic (per exemple, si el camp es defineix com a només de lectura en els paràmetres del projecte).</span><span class="sxs-lookup"><span data-stu-id="641ce-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="641ce-253">Tingueu en compte que els camps personalitzats no cal que tinguin registres de suport a la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="641ce-254">Es poden generar de manera dinàmica basant-se en la lògica d'X++.</span><span class="sxs-lookup"><span data-stu-id="641ce-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="641ce-255">L'exemple següent mostra aquest enfocament.</span><span class="sxs-lookup"><span data-stu-id="641ce-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="641ce-256">Els camps de la secció de capçalera són sempre només de lectura a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="641ce-257">Utilitzar la cadena d'ordres en el mètode buildCustomFieldList de la classe TSTimesheetSettings per mostrar un camp a la secció de capçalera</span><span class="sxs-lookup"><span data-stu-id="641ce-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="641ce-258">Aquest codi controla la configuració de visualització del camp a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="641ce-259">Per exemple, controla el tipus de camp, l'etiqueta, si el camp és obligatori i en quina secció apareix el camp.</span><span class="sxs-lookup"><span data-stu-id="641ce-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="641ce-260">A l'exemple següent es mostra un valor calculat a la secció de capçalera de l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="641ce-261">Utilitzar la cadena d'ordres en el mètode buildCustomFieldListForHeader de la classe TSTimesheetDetails per emplenar els detalls d'un full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="641ce-262">El mètode **buildCustomFieldListForHeader** s'utilitza per emplenar els detalls de la capçalera del full d'hores a l'aplicació mòbil.</span><span class="sxs-lookup"><span data-stu-id="641ce-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="641ce-263">Es necessita un registre TSTimesheetTable com a paràmetre.</span><span class="sxs-lookup"><span data-stu-id="641ce-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="641ce-264">Els camps d'aquest registre es poden utilitzar per emplenar el valor del camp personalitzat a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="641ce-265">L'exemple següent no llegeix cap valor de la base de dades.</span><span class="sxs-lookup"><span data-stu-id="641ce-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="641ce-266">En lloc d'això, utilitza la lògica d'X++ per generar un valor calculat que es mostrarà a l'aplicació.</span><span class="sxs-lookup"><span data-stu-id="641ce-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="641ce-267">Altres oportunitats de configurabilitat i extensibilitat</span><span class="sxs-lookup"><span data-stu-id="641ce-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="641ce-268">Afegir una validació addicional per a l'aplicació</span><span class="sxs-lookup"><span data-stu-id="641ce-268">Adding additional validation for the app</span></span>

<span data-ttu-id="641ce-269">La lògica existent per a la funcionalitat del full d'hores al nivell de la base de dades continuarà funcionant de la manera que s'esperava.</span><span class="sxs-lookup"><span data-stu-id="641ce-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="641ce-270">Per interrompre la finalització de l'operació de desament o enviament i mostrar un missatge d'error específic, podeu afegir **throw error("missatge a l'usuari")** al codi mitjançant una extensió de la cadena d'ordres.</span><span class="sxs-lookup"><span data-stu-id="641ce-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="641ce-271">Aquí teniu tres exemples de mètodes útils ampliables:</span><span class="sxs-lookup"><span data-stu-id="641ce-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="641ce-272">Si **validateWrite** a la taula TSTimesheetLine retorna **false** durant una operació de desament per a una línia del full d'hores, es mostrarà un missatge d'error a l'aplicació mòbil.</span><span class="sxs-lookup"><span data-stu-id="641ce-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="641ce-273">Si **validateSubmit** a la taula TSTimesheetTable retorna **false** durant una operació d'enviament a l'aplicació, es mostra un missatge d'error a l'usuari.</span><span class="sxs-lookup"><span data-stu-id="641ce-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="641ce-274">La lògica que emplena els camps (per exemple, **Propietat de la línia**) durant el mètode **insert** a la taula de TSTimesheetLine continuarà executant-se.</span><span class="sxs-lookup"><span data-stu-id="641ce-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="641ce-275">Amagar i marcar camps de fàbrica com a només de lectura mitjançant la configuració</span><span class="sxs-lookup"><span data-stu-id="641ce-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="641ce-276">A la llista de paràmetres del projecte, podeu crear camps de només de lectura o ocults a l'aplicació mòbil.</span><span class="sxs-lookup"><span data-stu-id="641ce-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="641ce-277">Definiu les opcions de la secció **Fulls d'hores mòbils** a la pestanya **Full d'hores** de la pàgina **Paràmetres de l'administració de projectes i la comptabilitat**.</span><span class="sxs-lookup"><span data-stu-id="641ce-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![Paràmetres del projecte](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="641ce-279">Canviar les activitats disponibles per a la selecció mitjançant extensions</span><span class="sxs-lookup"><span data-stu-id="641ce-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="641ce-280">Les activitats que estan disponibles per a la selecció d'un projecte s'emplenen mitjançant els mètodes **getActivitiesForProject()** i **getActivityQuery()** a la classe **TsTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="641ce-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="641ce-281">Podeu utilitzar la cadena d'ordres per canviar aquest comportament per tal que coincideixi amb el vostre escenari empresarial per a les activitats disponibles per a la selecció d'un projecte concret.</span><span class="sxs-lookup"><span data-stu-id="641ce-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="641ce-282">Introduir una categoria de projecte per defecte en entrades del full d'hores</span><span class="sxs-lookup"><span data-stu-id="641ce-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="641ce-283">L'entrada d'una categoria de projecte per defecte en les entrades del full d'hores es produeix en tres nivells.</span><span class="sxs-lookup"><span data-stu-id="641ce-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="641ce-284">Podeu utilitzar la cadena d'ordres per ampliar el comportament en qualsevol o tots aquests nivells per aconseguir el comportament desitjat.</span><span class="sxs-lookup"><span data-stu-id="641ce-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="641ce-285">S'utilitza la jerarquia següent:</span><span class="sxs-lookup"><span data-stu-id="641ce-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="641ce-286">L'aplicació prova de col·locar la categoria per defecte del recurs del projecte.</span><span class="sxs-lookup"><span data-stu-id="641ce-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="641ce-287">Aquesta categoria per defecte es defineix als mètodes **getCurrentUserResource** i **getDelegatedResourcesForCurrentUser** a la classe **TSTimesheetSettingsService**.</span><span class="sxs-lookup"><span data-stu-id="641ce-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="641ce-288">Si la categoria per defecte no es proporciona al nivell de recursos del projecte, l'aplicació prova de recuperar-la de l'activitat del projecte.</span><span class="sxs-lookup"><span data-stu-id="641ce-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="641ce-289">Aquesta categoria per defecte es defineix en el mètode **getActivitiesForProject** a la classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="641ce-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="641ce-290">Si la categoria per defecte no es proporciona al nivell d'activitat del projecte, la categoria per defecte s'obté dels paràmetres del projecte.</span><span class="sxs-lookup"><span data-stu-id="641ce-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="641ce-291">Aquesta categoria per defecte es defineix en el mètode **getProjectDetailsbyRule** a la classe **TSTimesheetProjectService**.</span><span class="sxs-lookup"><span data-stu-id="641ce-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]