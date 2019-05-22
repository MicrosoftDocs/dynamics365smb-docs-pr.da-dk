---
title: Sådan angiver du data i felter | Microsoft Docs
description: Få mere at vide om generelle funktioner, der hjælper dig med at indtaste data i felter.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252454"
---
# <a name="entering-data"></a><span data-ttu-id="25bff-103">Angivelse af data</span><span class="sxs-lookup"><span data-stu-id="25bff-103">Entering Data</span></span>

<span data-ttu-id="25bff-104">Der er mange generelle funktioner, der hjælper dig med at indtaste data data lettere, hurtigere og mere nøjagtigt.</span><span class="sxs-lookup"><span data-stu-id="25bff-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="25bff-105">De generelle funktioner til indtastning af data er beskrevet i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="25bff-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="25bff-106">Tastaturgenveje</span><span class="sxs-lookup"><span data-stu-id="25bff-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="25bff-107">Der er adskillige tastaturgenveje, du kan bruge, når du vil arbejde uden mus, og som gør dataindtastning hurtigere, især i forbindelse med store poster og gentagne indtastningsopgaver.</span><span class="sxs-lookup"><span data-stu-id="25bff-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="25bff-108">Du kan finde flere oplysninger om genveje i [Tastaturgenveje](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="25bff-109">Nogle af genvejene er beskrevet i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="25bff-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="25bff-110">Fremskynde dataindtastning ved hjælp af genveje</span><span class="sxs-lookup"><span data-stu-id="25bff-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="25bff-111">Genvej er en funktion, der er designet til dataindtastning med brug af tastatur.</span><span class="sxs-lookup"><span data-stu-id="25bff-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="25bff-112">Genvej fungerer på felter (f.eks. på kortider) og i lister (rækker og kolonner).</span><span class="sxs-lookup"><span data-stu-id="25bff-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="25bff-113">Det er nyttige, når du udfører gentagne indtastningsopgaver, der kræver oprettelse af flere poster i rækkefølge, f.eks. en kørsel med salgsordrer eller registrering af nye varer.</span><span class="sxs-lookup"><span data-stu-id="25bff-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="25bff-114">Du er muligvis allerede fortrolig med brugen af tabulatortasten til at navigere fra ét felt på en side til næste redigerbare felt.</span><span class="sxs-lookup"><span data-stu-id="25bff-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="25bff-115">En ulempe ved at bruge tabulatortasten er, at den altid går til næste felt i rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="25bff-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="25bff-116">Genvej gør det muligt at ændre denne fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="25bff-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="25bff-117">Med genvej kan du bruge Enter-tasten til udelukkende at navigere blandt de felter, du er interesseret i, og overspringe ikke-redigerbare felter og felter, som du normalt ikke udfylder.</span><span class="sxs-lookup"><span data-stu-id="25bff-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="25bff-118">Du har muligvis allerede bemærket denne funktionsmåde på nogle sider.</span><span class="sxs-lookup"><span data-stu-id="25bff-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="25bff-119">Det skyldes, at programmet allerede angiver, hvilke felter der skal medtages, når du trykker på Enter, og hvilke der skal springes over.</span><span class="sxs-lookup"><span data-stu-id="25bff-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="25bff-120">Du kan tilpasse genvej ved at tilpasse dit arbejdsområde og optimere den måde, du indtaster data på hver side.</span><span class="sxs-lookup"><span data-stu-id="25bff-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="25bff-121">Sådan fungerer genvej</span><span class="sxs-lookup"><span data-stu-id="25bff-121">How Quick Entry Works</span></span>

<span data-ttu-id="25bff-122">Hvert felt kan markeres som enten *medtaget i genvej* eller *udelukket fra genvej*.</span><span class="sxs-lookup"><span data-stu-id="25bff-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="25bff-123">Felter, der indgår i genvej, medtages i stien, når du trykker på Enter. Felter, der er udelukket fra genvej, medtages ikke.</span><span class="sxs-lookup"><span data-stu-id="25bff-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="25bff-124">Når du er færdig med at angive data i et felt, du blot trykke på Enter for at bekræfte ændringerne og gå til næste felt.</span><span class="sxs-lookup"><span data-stu-id="25bff-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="25bff-125">Hvis du vil vende retningen og gå til det forrige felt, skal du trykke på Shift+Enter.</span><span class="sxs-lookup"><span data-stu-id="25bff-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="25bff-126">Du kan finde flere oplysninger om genveje i [Tastaturgenveje i genvej](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="25bff-126">For more information about shortcuts, see [Quick Entry keyboard shortcuts](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="25bff-127">Tip</span><span class="sxs-lookup"><span data-stu-id="25bff-127">Tips and tricks</span></span>
<span data-ttu-id="25bff-128">Følgende indeholder nyttige oplysninger om brugen af genvej.</span><span class="sxs-lookup"><span data-stu-id="25bff-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="25bff-129">Den findes i alle redigerbare felter.</span><span class="sxs-lookup"><span data-stu-id="25bff-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="25bff-130">Den kan også bruges på tværs af kolonner og rækker.</span><span class="sxs-lookup"><span data-stu-id="25bff-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="25bff-131">Den forhindrer ikke adgang til andre elementer på en side, f.eks. handlinger.</span><span class="sxs-lookup"><span data-stu-id="25bff-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="25bff-132">De er stadig tilgængelige ved hjælp af tabulatortasten og Shift+Tab.</span><span class="sxs-lookup"><span data-stu-id="25bff-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="25bff-133">Oversigtspanelerne behøver ikke at blive udvidet for at få genvej til at fungere.</span><span class="sxs-lookup"><span data-stu-id="25bff-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="25bff-134">Hvis næste genvejsfelt er placeret i et skjult oversigtspanel, udvides det pågældende oversigtspanel automatisk og fokuserer på det angivne felt.</span><span class="sxs-lookup"><span data-stu-id="25bff-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="25bff-135">Genvej fungerer, uanset om felter skal udfyldes.</span><span class="sxs-lookup"><span data-stu-id="25bff-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="25bff-136">Det er derfor en god ide at sikre, at obligatoriske felter er medtaget i genvej.</span><span class="sxs-lookup"><span data-stu-id="25bff-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="25bff-137">Som standard medtages de fleste felter automatisk i genvej.</span><span class="sxs-lookup"><span data-stu-id="25bff-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="25bff-138">Så til at starte med skal du derfor sandsynligvis udelukke felter fra genvej.</span><span class="sxs-lookup"><span data-stu-id="25bff-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="25bff-139">Sådan ændres genvejsfelter</span><span class="sxs-lookup"><span data-stu-id="25bff-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="25bff-140">Hvis du vil ændre, hvilke felter der medtages i eller udelukkes fra genvej på en side, kan du bruge tilpasning.</span><span class="sxs-lookup"><span data-stu-id="25bff-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="25bff-141">Start tilpasning ved at vælge ikonet ![Indstillinger](media/ui-experience/settings_icon_small.png "ikonet Indstillinger til rollecenter") og derefter **Tilpas**.</span><span class="sxs-lookup"><span data-stu-id="25bff-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="25bff-142">Markér et felt, du vil ændre, eller markér på lister den tilsvarende kolonneoverskrift, og vælg derefter enten **Medtag i genvej** eller **Udeluk fra genvej**.</span><span class="sxs-lookup"><span data-stu-id="25bff-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="25bff-143">Du kan finde flere oplysninger om tilpasning under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="25bff-144">Obligatoriske felter</span><span class="sxs-lookup"><span data-stu-id="25bff-144">Mandatory Fields</span></span>

<span data-ttu-id="25bff-145">Når du indtaster data på sider, er visse felter markeret med en rød stjerne.</span><span class="sxs-lookup"><span data-stu-id="25bff-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="25bff-146">Den røde stjerne betyder, at feltet skal udfyldes for at fuldføre en bestemt proces, der bruger feltet, f.eks. bogføring af en transaktion, der bruger værdien i feltet.</span><span class="sxs-lookup"><span data-stu-id="25bff-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="25bff-147">Selv om feltet indeholder en rød stjerne, er du ikke tvunget til at udfylde feltet, før du fortsætter til andre felter eller lukker siden.</span><span class="sxs-lookup"><span data-stu-id="25bff-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="25bff-148">Den røde stjerne tjener kun som en påmindelse om, at du vil blive blokeret fra at udføre en bestemt proces.</span><span class="sxs-lookup"><span data-stu-id="25bff-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="25bff-149">Søge efter data mens du skriver</span><span class="sxs-lookup"><span data-stu-id="25bff-149">Finding Data As You Type</span></span>

 <span data-ttu-id="25bff-150">Når du begynder at indtaste tegn i et felt, vises en rulleliste med mulige feltværdier.</span><span class="sxs-lookup"><span data-stu-id="25bff-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="25bff-151">Listen ændres, når du skriver flere tegn, og du kan vælge den korrekte værdi, når den vises.</span><span class="sxs-lookup"><span data-stu-id="25bff-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="25bff-152">Mange felter har en knap med en nedadgående pil, som du kan vælge.</span><span class="sxs-lookup"><span data-stu-id="25bff-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="25bff-153">Når du vælger pilen, vises en liste med data, som du kan vælge at indtaste i feltet.</span><span class="sxs-lookup"><span data-stu-id="25bff-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="25bff-154">Knappen har to funktioner afhængigt af felttypen:</span><span class="sxs-lookup"><span data-stu-id="25bff-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="25bff-155">Valg – viser oplysninger fra en anden tabel, som du kan indtaste i feltet.</span><span class="sxs-lookup"><span data-stu-id="25bff-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="25bff-156">Du kan vælge én enkelt dataangivelse ad gangen.</span><span class="sxs-lookup"><span data-stu-id="25bff-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="25bff-157">Rullemenu – viser det sæt indstillinger, der findes til feltet.</span><span class="sxs-lookup"><span data-stu-id="25bff-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="25bff-158">Du kan kun vælge én af indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="25bff-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="25bff-159">Kopiere og indsætte felter og linjer</span><span class="sxs-lookup"><span data-stu-id="25bff-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="25bff-160">Du kan kopiere en eller flere rækker fra en liste eller et enkelt felt på en side og derefter indsætte det, du har kopieret på den samme side, en anden side eller et eksternt dokument (som Microsoft Excel og e-mails i Outlook).</span><span class="sxs-lookup"><span data-stu-id="25bff-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="25bff-161">Kort sagt, når du vil kopiere, skal du trykke på CTRL + C (cmd + C i macOS) på tastaturet.</span><span class="sxs-lookup"><span data-stu-id="25bff-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="25bff-162">Når du vil indsætte, skal du trykke på CTRL + V (cmd + V i macOS).</span><span class="sxs-lookup"><span data-stu-id="25bff-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="25bff-163">Hvis du på en liste vil kopiere feltet i den samme kolonne i rækken ovenfor og indsætte det i den aktuelle række, skal du bare trykke på F8.</span><span class="sxs-lookup"><span data-stu-id="25bff-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="25bff-164">Du kan finde flere oplysninger i [Kopiere og indsætte i Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="25bff-165">Fokusere på linjevarer</span><span class="sxs-lookup"><span data-stu-id="25bff-165">Focusing on Line Items</span></span>

<span data-ttu-id="25bff-166">Når du arbejder med dokumenter, som indeholder en del med linjevarer, f.eks. en salgsordre eller fakturaside, kan du skifte visningen til udelukkende at fokusere på linjevarer, hvilket reelt udvider delen med linjevarer, så den optager ret meget af hele arbejdsområdet – og skjuler andre dele af siden undtagen handlingsområdet øverst.</span><span class="sxs-lookup"><span data-stu-id="25bff-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="25bff-167">Det giver dig et bedre overblik over linjevarerne og giver mere plads til at arbejde med dem.</span><span class="sxs-lookup"><span data-stu-id="25bff-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="25bff-168">Dette er især nyttige, når du arbejder med store lister med linjevarer, og der ønskes hurtig dataindtastning.</span><span class="sxs-lookup"><span data-stu-id="25bff-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="25bff-169">En anden fordel er, at det også indeholder avancerede filterfunktioner, som på andre lister, så det bliver endnu nemmere at gennemse og søge gennem linjevarer.</span><span class="sxs-lookup"><span data-stu-id="25bff-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switch-the-focus-on-and-off"></a><span data-ttu-id="25bff-170">Slå fokus til og fra</span><span class="sxs-lookup"><span data-stu-id="25bff-170">Switch the Focus On and Off</span></span>

<span data-ttu-id="25bff-171">Når du vil fokusere på linjevarer, skal du markeret et vilkårligt sted i delen med linjevarer og derefter vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") i øverste højre hjørne eller trykke på Ctrl+Shift+F12.</span><span class="sxs-lookup"><span data-stu-id="25bff-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="25bff-172">For at vende tilbage til normal visning skal du vælge ![Ikonet Fokustilstand](media/focus-mode.png "Ikonet Fokustilstand") eller trykke på Ctrl+Shift+F12 igen.</span><span class="sxs-lookup"><span data-stu-id="25bff-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="25bff-173">Filtrere linjevarerne</span><span class="sxs-lookup"><span data-stu-id="25bff-173">Filtering the Line Items</span></span>

<span data-ttu-id="25bff-174">Du starter filtrering ved at vælge ![Ikonet Filterrude](media/open-filter-pane-icon.png "Ikonet Filterrude") øverst på listen eller ved at trykke på **Shift+F3** for at åbne filterruden.</span><span class="sxs-lookup"><span data-stu-id="25bff-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="25bff-175">Du arbejder med filterruden, på samme måde som du arbejder med andre lister.</span><span class="sxs-lookup"><span data-stu-id="25bff-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="25bff-176">Du kan finde flere oplysninger i [Filtrering](ui-enter-criteria-filters.md#Filtering).</span><span class="sxs-lookup"><span data-stu-id="25bff-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="25bff-177">Filtrering er især nyttig, når du får vist og analyserer længere dokumenter.</span><span class="sxs-lookup"><span data-stu-id="25bff-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="25bff-178">Antag f.eks., at du åbner en bogført salgsfaktura og filtrerer linjevarerne for at få vist alle linjevarer med en individuel rabat over 5 % eller filtrerer for udelukkende at få vist cykeltilbehør med 'pro' i navnet.</span><span class="sxs-lookup"><span data-stu-id="25bff-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="25bff-179">Angive mængder ved beregning</span><span class="sxs-lookup"><span data-stu-id="25bff-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="25bff-180">Når du angiver tal i mængdefelter, f.eks. i feltet **Antal** på en varekladdelinje, kan du angive formlen i stedet for summen af mængden.</span><span class="sxs-lookup"><span data-stu-id="25bff-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="25bff-181">Eksempler</span><span class="sxs-lookup"><span data-stu-id="25bff-181">Examples</span></span>  

-   <span data-ttu-id="25bff-182">Hvis du skriver 19+19, beregnes feltet til 38.</span><span class="sxs-lookup"><span data-stu-id="25bff-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="25bff-183">Hvis du skriver 41-9, beregnes feltet til 32.</span><span class="sxs-lookup"><span data-stu-id="25bff-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="25bff-184">Hvis du skriver 12\*4, beregnes feltet til 48.</span><span class="sxs-lookup"><span data-stu-id="25bff-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="25bff-185">Hvis du skriver 12/4, beregnes feltet til 3.</span><span class="sxs-lookup"><span data-stu-id="25bff-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="25bff-186">Angivelse af negative tal</span><span class="sxs-lookup"><span data-stu-id="25bff-186">Entering Negative Numbers</span></span>

<span data-ttu-id="25bff-187">Du kan angive negative tal på to måder.</span><span class="sxs-lookup"><span data-stu-id="25bff-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="25bff-188">Tallet -20,5 kan angives som:</span><span class="sxs-lookup"><span data-stu-id="25bff-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="25bff-189">-20,5</span><span class="sxs-lookup"><span data-stu-id="25bff-189">-20.5</span></span>  

    <span data-ttu-id="25bff-190">eller</span><span class="sxs-lookup"><span data-stu-id="25bff-190">or</span></span>
-   <span data-ttu-id="25bff-191">20,5-</span><span class="sxs-lookup"><span data-stu-id="25bff-191">20.5-</span></span>  

 <span data-ttu-id="25bff-192">I begge tilfælde registreres beløbet som -20,5.</span><span class="sxs-lookup"><span data-stu-id="25bff-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="25bff-193">Hvis det sidste tegn i udtrykket er et **+** eller et **-**, registreres hele udtrykket med det tegn.</span><span class="sxs-lookup"><span data-stu-id="25bff-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="25bff-194">Eksempel, **10-20+** medfører 10 og ikke -10.</span><span class="sxs-lookup"><span data-stu-id="25bff-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="25bff-195">Indtaste datoer og tidspunkter</span><span class="sxs-lookup"><span data-stu-id="25bff-195">Entering Dates and Times</span></span>

<span data-ttu-id="25bff-196">Du kan angive datoer og klokkeslæt i alle de felter, der er angivet specielt til datoer (datofelter).</span><span class="sxs-lookup"><span data-stu-id="25bff-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="25bff-197">Du kan angive datoer med eller uden separatorer.</span><span class="sxs-lookup"><span data-stu-id="25bff-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="25bff-198">Måden, du angiver datoer og klokkeslæt på, afhænger af dine indstillinger i **Område**.</span><span class="sxs-lookup"><span data-stu-id="25bff-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="25bff-199">Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="25bff-200">Angive datoer</span><span class="sxs-lookup"><span data-stu-id="25bff-200">Entering Dates</span></span>

<span data-ttu-id="25bff-201">For datofelter kan du enten bruge datavælgeren, som gør det muligt at vælge en dato i en kalender, eller du kan angive datoer manuelt.</span><span class="sxs-lookup"><span data-stu-id="25bff-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="25bff-202">Denne sektion indeholder en kort oversigt over, hvordan du angiver datoer.</span><span class="sxs-lookup"><span data-stu-id="25bff-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="25bff-203">Du kan finde flere oplysninger i [Arbejde med kalenderdatoer og klokkeslæt](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="25bff-204">Hvis du vil indtaste datoen manuelt, kan du indtaste to, fire, seks eller otte cifre:</span><span class="sxs-lookup"><span data-stu-id="25bff-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="25bff-205">Hvis du kun indtaster to tal, fortolkes dette som dagen og måneden og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="25bff-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="25bff-206">Hvis du indtaster fire tal, fortolkes dette som dagen og måneden, og året indsættes ud fra arbejdsdatoen.</span><span class="sxs-lookup"><span data-stu-id="25bff-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="25bff-207">Hvis datoen falder inden for 01-01-1930 og 31-12-2029, kan du nøjes med to tal for året, ellers skal året angives med fire cifre.</span><span class="sxs-lookup"><span data-stu-id="25bff-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="25bff-208">Du kan også indtaste datoen som en ugedag efterfulgt af ugenummeret og evt. året (f.eks. betyder Man25 eller man25 mandag i uge 25).</span><span class="sxs-lookup"><span data-stu-id="25bff-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="25bff-209">I stedet for en bestemt dato kan du indtaste én af disse koder.</span><span class="sxs-lookup"><span data-stu-id="25bff-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="25bff-210">Kode</span><span class="sxs-lookup"><span data-stu-id="25bff-210">Code</span></span>|<span data-ttu-id="25bff-211">Resultat</span><span class="sxs-lookup"><span data-stu-id="25bff-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="25bff-212">d</span><span class="sxs-lookup"><span data-stu-id="25bff-212">t</span></span>|<span data-ttu-id="25bff-213">Dette angiver dags dato (computerens systemdato).</span><span class="sxs-lookup"><span data-stu-id="25bff-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="25bff-214">p</span><span class="sxs-lookup"><span data-stu-id="25bff-214">p</span></span>|<span data-ttu-id="25bff-215">Dette angiver en regnskabsperiode, hvor `p`betyder den første regnskabsperiode, `p2` betyder den anden regnskabsperiode osv.</span><span class="sxs-lookup"><span data-stu-id="25bff-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="25bff-216">a</span><span class="sxs-lookup"><span data-stu-id="25bff-216">w</span></span>|<span data-ttu-id="25bff-217">Dette angiver den arbejdsdato, der er angivet i programmet.</span><span class="sxs-lookup"><span data-stu-id="25bff-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="25bff-218">Hvis du vil ændre arbejdsdatoen, kan du se i [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="25bff-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="25bff-219">Det er en fordel at anvende en arbejdsdato, hvis du har mange transaktioner at udføre på en dato, der ikke er dags dato.</span><span class="sxs-lookup"><span data-stu-id="25bff-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="25bff-220">c</span><span class="sxs-lookup"><span data-stu-id="25bff-220">c</span></span>|<span data-ttu-id="25bff-221">Dette angiver, at datoen efter `c`er en ultimodato, f.eks. `C123101`.</span><span class="sxs-lookup"><span data-stu-id="25bff-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="25bff-222">Angive klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="25bff-222">Entering Times</span></span>

<span data-ttu-id="25bff-223">Når du angiver klokkeslæt, kan du indsætte en vilkårlig separator mellem tidsenhederne, men det er ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="25bff-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="25bff-224">Det er ikke nødvendigt at skrive minutter, sekunder eller AM/PM.</span><span class="sxs-lookup"><span data-stu-id="25bff-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="25bff-225">I den følgende tabel kan du se, hvordan du kan indtaste klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="25bff-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="25bff-226">Post</span><span class="sxs-lookup"><span data-stu-id="25bff-226">Entry</span></span>|<span data-ttu-id="25bff-227">Fortolkning</span><span class="sxs-lookup"><span data-stu-id="25bff-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="25bff-228">5</span><span class="sxs-lookup"><span data-stu-id="25bff-228">5</span></span>|<span data-ttu-id="25bff-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-229">05:00:00</span></span>|  
|<span data-ttu-id="25bff-230">5:30</span><span class="sxs-lookup"><span data-stu-id="25bff-230">5:30</span></span>|<span data-ttu-id="25bff-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="25bff-231">05:30:00</span></span>|  
|<span data-ttu-id="25bff-232">0530</span><span class="sxs-lookup"><span data-stu-id="25bff-232">0530</span></span>|<span data-ttu-id="25bff-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="25bff-233">05:30:00</span></span>|  
|<span data-ttu-id="25bff-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="25bff-234">5:30:5</span></span>|<span data-ttu-id="25bff-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="25bff-235">05:30:05</span></span>|  
|<span data-ttu-id="25bff-236">053005</span><span class="sxs-lookup"><span data-stu-id="25bff-236">053005</span></span>|<span data-ttu-id="25bff-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="25bff-237">05:30:05</span></span>|  
|<span data-ttu-id="25bff-238">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="25bff-238">5:30:5,50</span></span>|<span data-ttu-id="25bff-239">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="25bff-239">05:30:05.5</span></span>|  
|<span data-ttu-id="25bff-240">053005050</span><span class="sxs-lookup"><span data-stu-id="25bff-240">053005050</span></span>|<span data-ttu-id="25bff-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="25bff-241">05:30:05.05</span></span>|  

 <span data-ttu-id="25bff-242">Du skal skrive to tal for hver tidsenhed, hvis du ikke angiver en separator.</span><span class="sxs-lookup"><span data-stu-id="25bff-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="25bff-243">Angive dato/klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="25bff-243">Entering Datetimes</span></span>

<span data-ttu-id="25bff-244">Når du angiver dato/klokkeslæt skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="25bff-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="25bff-245">I den følgende tabel kan du se, hvordan du kan skrive dato og klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="25bff-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="25bff-246">Post</span><span class="sxs-lookup"><span data-stu-id="25bff-246">Entry</span></span>|<span data-ttu-id="25bff-247">Fortolkning</span><span class="sxs-lookup"><span data-stu-id="25bff-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="25bff-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="25bff-248">131202 132455</span></span>|<span data-ttu-id="25bff-249">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="25bff-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="25bff-250">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="25bff-250">1-12-02 10</span></span>|<span data-ttu-id="25bff-251">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="25bff-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="25bff-252">1.12.02 5</span></span>|<span data-ttu-id="25bff-253">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="25bff-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="25bff-254">1.12.02</span></span>|<span data-ttu-id="25bff-255">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="25bff-256">11 12</span><span class="sxs-lookup"><span data-stu-id="25bff-256">11 12</span></span>|<span data-ttu-id="25bff-257">11-løbende måned-løbende år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="25bff-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="25bff-258">1112 12</span></span>|<span data-ttu-id="25bff-259">11-12-aktuelt år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="25bff-260">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="25bff-260">t or today</span></span>|<span data-ttu-id="25bff-261">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="25bff-262">t tid</span><span class="sxs-lookup"><span data-stu-id="25bff-262">t time</span></span>|<span data-ttu-id="25bff-263">dags dato aktuelt klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="25bff-263">today's date actual time</span></span>|  
|<span data-ttu-id="25bff-264">d 10:30</span><span class="sxs-lookup"><span data-stu-id="25bff-264">t 10:30</span></span>|<span data-ttu-id="25bff-265">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="25bff-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="25bff-266">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="25bff-266">t 3:3:3</span></span>|<span data-ttu-id="25bff-267">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="25bff-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="25bff-268">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="25bff-268">w or workdate</span></span>|<span data-ttu-id="25bff-269">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="25bff-270">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="25bff-270">m or Monday</span></span>|<span data-ttu-id="25bff-271">Mandag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-272">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="25bff-272">tu or Tuesday</span></span>|<span data-ttu-id="25bff-273">Tirsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-274">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="25bff-274">we or Wednesday</span></span>|<span data-ttu-id="25bff-275">Onsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-276">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="25bff-276">th or Thursday</span></span>|<span data-ttu-id="25bff-277">Torsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-278">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="25bff-278">f or Friday</span></span>|<span data-ttu-id="25bff-279">Fredag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-280">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="25bff-280">s or Saturday</span></span>|<span data-ttu-id="25bff-281">Lørdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-282">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="25bff-282">su or Sunday</span></span>|<span data-ttu-id="25bff-283">Søndag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="25bff-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="25bff-284">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="25bff-284">tu 10:30</span></span>|<span data-ttu-id="25bff-285">Tirsdag i den aktuelle uge 10:30:00</span><span class="sxs-lookup"><span data-stu-id="25bff-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="25bff-286">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="25bff-286">tu 3:3:3</span></span>|<span data-ttu-id="25bff-287">Tirsdag i den aktuelle uge 03:03:03</span><span class="sxs-lookup"><span data-stu-id="25bff-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="25bff-288">Angivelse af varighed</span><span class="sxs-lookup"><span data-stu-id="25bff-288">Entering Duration</span></span>

<span data-ttu-id="25bff-289">Du angiver varighed ved at skrive et tal efterfulgt af en måleenhed.</span><span class="sxs-lookup"><span data-stu-id="25bff-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="25bff-290">Her er nogle eksempler.</span><span class="sxs-lookup"><span data-stu-id="25bff-290">Here are some examples.</span></span>  

|<span data-ttu-id="25bff-291">Varighed</span><span class="sxs-lookup"><span data-stu-id="25bff-291">Duration</span></span>|<span data-ttu-id="25bff-292">Enhed\*\*</span><span class="sxs-lookup"><span data-stu-id="25bff-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="25bff-293">2t</span><span class="sxs-lookup"><span data-stu-id="25bff-293">2h</span></span>|<span data-ttu-id="25bff-294">2 timer</span><span class="sxs-lookup"><span data-stu-id="25bff-294">2 hrs</span></span>|  
|<span data-ttu-id="25bff-295">6t 30 m</span><span class="sxs-lookup"><span data-stu-id="25bff-295">6h 30 m</span></span>|<span data-ttu-id="25bff-296">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="25bff-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="25bff-297">6,5t</span><span class="sxs-lookup"><span data-stu-id="25bff-297">6.5h</span></span>|<span data-ttu-id="25bff-298">6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="25bff-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="25bff-299">90m</span><span class="sxs-lookup"><span data-stu-id="25bff-299">90m</span></span>|<span data-ttu-id="25bff-300">1 time 30 min</span><span class="sxs-lookup"><span data-stu-id="25bff-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="25bff-301">2d 6t 30m</span><span class="sxs-lookup"><span data-stu-id="25bff-301">2d 6h 30m</span></span>|<span data-ttu-id="25bff-302">2 dage 6 timer 30 min</span><span class="sxs-lookup"><span data-stu-id="25bff-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="25bff-303">2d 6t 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="25bff-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="25bff-304">2 dage 6 timer 30 min 56 sek 600 msek</span><span class="sxs-lookup"><span data-stu-id="25bff-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="25bff-305">Du kan også skrive et tal, der så automatisk konverteres til en varighed.</span><span class="sxs-lookup"><span data-stu-id="25bff-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="25bff-306">Det tal, du skriver, konverteres i overensstemmelse med den standardmåleenhed, der er angivet i feltet Varighed.</span><span class="sxs-lookup"><span data-stu-id="25bff-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="25bff-307">Du kan se, hvilken måleenhed, der anvendes i feltet Varighed, ved at skrive et tal og se, hvilken måleenhed tallet konverteres til.</span><span class="sxs-lookup"><span data-stu-id="25bff-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="25bff-308">Tallet 5 konverteres til 5 timer, hvis måleenheden er timer.</span><span class="sxs-lookup"><span data-stu-id="25bff-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="25bff-309">Se også</span><span class="sxs-lookup"><span data-stu-id="25bff-309">See Also</span></span>  
 [<span data-ttu-id="25bff-310">Sortering af, søgning i og filtrering af lister</span><span class="sxs-lookup"><span data-stu-id="25bff-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="25bff-311">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="25bff-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
