---
title: Angive layoutet for en check | Microsoft Docs
description: Du kan designe og udskrive checks i forskellige formater i overensstemmelse med standarderne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: print check, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 479281e24bffb824f9fc8499bb34ab6b11311a52
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183664"
---
# <a name="select-a-check-layout"></a><span data-ttu-id="4fc79-103">Vælge et checklayout</span><span class="sxs-lookup"><span data-stu-id="4fc79-103">Select a Check Layout</span></span>
<span data-ttu-id="4fc79-104">Du kan udforme dine checks i overensstemmelse med de lokale myndigheders standarder.</span><span class="sxs-lookup"><span data-stu-id="4fc79-104">You can design your checks to conform with the standards set by the local authorities.</span></span> <span data-ttu-id="4fc79-105">Checkbilleder kan udskrives på engelsk, fransk eller spansk.</span><span class="sxs-lookup"><span data-stu-id="4fc79-105">Check images can be printed in English, French, or Spanish.</span></span>

<span data-ttu-id="4fc79-106">Checks er designet til udskrivning i amerikanske og canadiske checkbilledformater i et checkfølgebrevformat eller et følgebrev-følgebrevcheckformat.</span><span class="sxs-lookup"><span data-stu-id="4fc79-106">Checks are designed to print in both the United States and Canadian check image formats in either a check-stub-check format or a stub-stub-check format.</span></span>

## <a name="to-select-a-check-layout"></a><span data-ttu-id="4fc79-107">Sådan vælges et checklayout</span><span class="sxs-lookup"><span data-stu-id="4fc79-107">To select a check layout</span></span>
1. <span data-ttu-id="4fc79-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rapportvalg - Bankkonto**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="4fc79-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Report Selections Bank Account**, and then choose the related link.</span></span>
2. <span data-ttu-id="4fc79-109">På siden **Rapportvalg - bankkonto** skal du vælge feltet **Check** i feltet **Forbrug**.</span><span class="sxs-lookup"><span data-stu-id="4fc79-109">On the **Report Selection - Bank Acc.** page, in the **Usage** field, select **Check**.</span></span>
3. <span data-ttu-id="4fc79-110">Vælg et af følgende rapport-id'er.</span><span class="sxs-lookup"><span data-stu-id="4fc79-110">Select one of the following report IDs.</span></span>

| <span data-ttu-id="4fc79-111">Rapport-id</span><span class="sxs-lookup"><span data-stu-id="4fc79-111">Report ID</span></span> | <span data-ttu-id="4fc79-112">Rapportnavn</span><span class="sxs-lookup"><span data-stu-id="4fc79-112">Report Name</span></span> | <span data-ttu-id="4fc79-113">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4fc79-113">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4fc79-114">1401</span><span class="sxs-lookup"><span data-stu-id="4fc79-114">1401</span></span> |<span data-ttu-id="4fc79-115">Check</span><span class="sxs-lookup"><span data-stu-id="4fc79-115">Check</span></span> |<span data-ttu-id="4fc79-116">Dette er standardrapporten.</span><span class="sxs-lookup"><span data-stu-id="4fc79-116">This is the default report.</span></span> |
| <span data-ttu-id="4fc79-117">10411</span><span class="sxs-lookup"><span data-stu-id="4fc79-117">10411</span></span> |<span data-ttu-id="4fc79-118">Check (følgebrev/følgebrev/check)</span><span class="sxs-lookup"><span data-stu-id="4fc79-118">Check (Stub/Stub/Check)</span></span> |<span data-ttu-id="4fc79-119">Denne rapport er designet til at udskrive check i et følgebrev/følgebrev/check-format.</span><span class="sxs-lookup"><span data-stu-id="4fc79-119">This report is designed to print checks in a stub/stub/check format.</span></span> |
| <span data-ttu-id="4fc79-120">10412</span><span class="sxs-lookup"><span data-stu-id="4fc79-120">10412</span></span> |<span data-ttu-id="4fc79-121">Check (følgebrev/check/følgebrev)</span><span class="sxs-lookup"><span data-stu-id="4fc79-121">Check (Stub/Check/Stub)</span></span> |<span data-ttu-id="4fc79-122">Denne rapport er designet til at udskrive check i et følgebrev/check/følgebrev-format.</span><span class="sxs-lookup"><span data-stu-id="4fc79-122">This report is designed to print checks in a stub/check/stub format.</span></span> |
| <span data-ttu-id="4fc79-123">10413</span><span class="sxs-lookup"><span data-stu-id="4fc79-123">10413</span></span> |<span data-ttu-id="4fc79-124">Tre checks pr. side</span><span class="sxs-lookup"><span data-stu-id="4fc79-124">Three Checks per Page</span></span> |<span data-ttu-id="4fc79-125">Denne rapport er udviklet til at udskrive tre checks på hver side.</span><span class="sxs-lookup"><span data-stu-id="4fc79-125">This report is designed to print three checks on each page.</span></span> |

<span data-ttu-id="4fc79-126">Når du har oprettet checklayout, kan du udskrive check på siden **Udbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="4fc79-126">When you have set up check layouts, you can print checks from the **Payment Journal** page.</span></span> <span data-ttu-id="4fc79-127">Du kan finde flere oplysninger i [Arbejde med checks](payables-how-work-checks.md).</span><span class="sxs-lookup"><span data-stu-id="4fc79-127">For more information, see [Work with Checks](payables-how-work-checks.md).</span></span>

<span data-ttu-id="4fc79-128">Hvis du vil ændre et af disse standardchecklayout, skal du bruge enten Word eller RDLC-integration til at gøre det.</span><span class="sxs-lookup"><span data-stu-id="4fc79-128">To change one of these default check layouts, use either the Word or the RDLC integration to do so.</span></span> <span data-ttu-id="4fc79-129">Du kan finde flere oplysninger i [Oprette og ændre et brugerdefineret rapportlayouts](ui-how-create-custom-report-layout.md).</span><span class="sxs-lookup"><span data-stu-id="4fc79-129">For more information, see [Create and Modify Custom Report Layouts](ui-how-create-custom-report-layout.md).</span></span>

## <a name="using-micr-and-security-fonts"></a><span data-ttu-id="4fc79-130">Bruge MICR og sikkerhedsskrifttyper</span><span class="sxs-lookup"><span data-stu-id="4fc79-130">Using MICR and Security Fonts</span></span>
<span data-ttu-id="4fc79-131">Onlineversionen af [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder forudinstallerede skrifttyper på de servere, der kan bruges, når checklayout defineres.</span><span class="sxs-lookup"><span data-stu-id="4fc79-131">The online version of [!INCLUDE[d365fin](includes/d365fin_md.md)] contains pre-installed fonts on the servers that can be used when defining check layouts.</span></span> <span data-ttu-id="4fc79-132">Følgende dispositioner viser, hvilke skrifttyper der er tilgængelige og indeholder hyperlinks til detaljerede oplysninger fra tredjepartsleverandører af skrifttyperne.</span><span class="sxs-lookup"><span data-stu-id="4fc79-132">The following outlines which fonts are available and has links to detailed information by the 3rd-party suppliers of the fonts.</span></span>

> [!Important]
> <span data-ttu-id="4fc79-133">MICR og sikkerhedsskrifttyper til checks i Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] licenseres i en skrifttypepakke fra IDAutomation.com, Inc. Disse produkter må kun anvendes som led i og i forbindelse med Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4fc79-133">MICR and check security fonts in Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)] are licensed in a font package from IDAutomation.com, Inc. These products may only be used as part of and in connection with Microsoft Dynamics [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="4fc79-134">I opdatering 15.3 og nyere er der installeret MICR-skrifttyper (Magnetic Ink Character Recognition), som kan bruges.</span><span class="sxs-lookup"><span data-stu-id="4fc79-134">In update 15.3 and newer, Magnetic Ink Character Recognition (MICR) fonts are installed and available to use.</span></span> <span data-ttu-id="4fc79-135">Både E-13B- og CMC-7-standarder understøttes.</span><span class="sxs-lookup"><span data-stu-id="4fc79-135">Both the E-13B and the CMC-7 standards are supported.</span></span> <span data-ttu-id="4fc79-136">Ud over MICR-skrifttyper er særlige sikkerhedsskrifttyper tilgængelige, så du kan oprette tekst, navne, beløb og valutasymbolerne dollar, euro, pund og yen, som er svære at ændre, når en check først er udskrevet.</span><span class="sxs-lookup"><span data-stu-id="4fc79-136">In addition to MICR fonts, special security fonts are available to generate text, names, amounts, and the currency symbols Dollar, Euro, Pound, and Yen, which are hard to tamper with once a check has been printed.</span></span>

> [!NOTE]
> <span data-ttu-id="4fc79-137">Af hensyn til sikkerheden og af juridiske årsager kan du ikke overføre brugerdefinerede skrifttyper til [!INCLUDE[d365fin](includes/d365fin_md.md)]-miljøet.</span><span class="sxs-lookup"><span data-stu-id="4fc79-137">For security and legal reasons, you cannot upload custom fonts to the [!INCLUDE[d365fin](includes/d365fin_md.md)] environment.</span></span>

### <a name="micr-e-13b-specifications"></a><span data-ttu-id="4fc79-138">MICR E-13B-specifikationer</span><span class="sxs-lookup"><span data-stu-id="4fc79-138">MICR E-13B Specifications</span></span>
<span data-ttu-id="4fc79-139">Følgende opsummerer specifikationer for de MICR E-13B-skrifttyper, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.</span><span class="sxs-lookup"><span data-stu-id="4fc79-139">The following summarizes specifications for the MICR E-13B fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="4fc79-140">![MICR E-13B-specifikationer](media/font_MICR_E-13B_Specifications.png "MICR E-13B-specifikationer")</span><span class="sxs-lookup"><span data-stu-id="4fc79-140">![MICR E-13B Specifications](media/font_MICR_E-13B_Specifications.png "MICR E-13B Specifications")</span></span>

<span data-ttu-id="4fc79-141">Den komplette specifikation af MICR E-13B-skrifttyper findes i leverandørens dokumentation her: (https://www.idautomation.com/micr-fonts/e13b/).</span><span class="sxs-lookup"><span data-stu-id="4fc79-141">The full specification of MICR E-13B fonts can be found in the supplier's documentation here: (https://www.idautomation.com/micr-fonts/e13b/).</span></span>

### <a name="micr-cmc-7-specifications"></a><span data-ttu-id="4fc79-142">MICR CMC-7-specifikationer</span><span class="sxs-lookup"><span data-stu-id="4fc79-142">MICR CMC-7 Specifications</span></span>
<span data-ttu-id="4fc79-143">Følgende CMC-7-skrifttyper er tilgængelige i [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span><span class="sxs-lookup"><span data-stu-id="4fc79-143">The following CMC-7 fonts are available in [!INCLUDE[d365fin](includes/d365fin_md.md)] online:</span></span>

- <span data-ttu-id="4fc79-144">IDAutomationCMC7</span><span class="sxs-lookup"><span data-stu-id="4fc79-144">IDAutomationCMC7</span></span>
- <span data-ttu-id="4fc79-145">IDAutomationCMC7n10</span><span class="sxs-lookup"><span data-stu-id="4fc79-145">IDAutomationCMC7n10</span></span>
- <span data-ttu-id="4fc79-146">IDAutomationCMC7n25</span><span class="sxs-lookup"><span data-stu-id="4fc79-146">IDAutomationCMC7n25</span></span>
-   <span data-ttu-id="4fc79-147">IDAutomationCMC7n40</span><span class="sxs-lookup"><span data-stu-id="4fc79-147">IDAutomationCMC7n40</span></span>

<span data-ttu-id="4fc79-148">Følgende opsummerer specifikationer for de MICR CMC-7-skrifttyper, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.</span><span class="sxs-lookup"><span data-stu-id="4fc79-148">The following summarizes specifications for the MICR CMC-7 fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="4fc79-149">![MICR CMC-7-specifikationer](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7-specifikationer")</span><span class="sxs-lookup"><span data-stu-id="4fc79-149">![MICR CMC-7 Specifications](media/font_MICR_CMC-7_Specifications.png "MICR CMC-7 Specifications")</span></span>

<span data-ttu-id="4fc79-150">Den komplette specifikation af MICR CMC-7-skrifttyper findes i leverandørens dokumentation her: (http://www.idautomation.com/micr-fonts/cmc7/).</span><span class="sxs-lookup"><span data-stu-id="4fc79-150">The full specification of MICR CMC-7 fonts can be found in the supplier's documentation here: (http://www.idautomation.com/micr-fonts/cmc7/).</span></span>

### <a name="secure-font-specifications"></a><span data-ttu-id="4fc79-151">Specifikationer for sikre skrifttyper</span><span class="sxs-lookup"><span data-stu-id="4fc79-151">Secure Font Specifications</span></span>
<span data-ttu-id="4fc79-152">Følgende opsummerer specifikationer for sikkerhedsskrifttyper til checks, som kan være nyttige, når du kalibrerer skrifttyper til at kunne bruges i checklayout på specifikke MICR-printere.</span><span class="sxs-lookup"><span data-stu-id="4fc79-152">The following summarizes specifications for check security fonts that may be useful when calibrating fonts to be on check layouts with specific MICR printers.</span></span>

<span data-ttu-id="4fc79-153">![Specifikationer for sikkerhedsskrifttyper til checks](media/font_check-security-font_Specifications.png "Specifikationer for sikkerhedsskrifttyper til checks")</span><span class="sxs-lookup"><span data-stu-id="4fc79-153">![Check Security Font Specifications](media/font_check-security-font_Specifications.png "Check Security Font Specifications")</span></span>

<span data-ttu-id="4fc79-154">Den komplette specifikation af sikkerhedsskrifttyper til checks findes i leverandørens dokumentation her: (https://www.idautomation.com/security-fonts/).</span><span class="sxs-lookup"><span data-stu-id="4fc79-154">The full specification of check security fonts can be found in the supplier's documentation here: (https://www.idautomation.com/security-fonts/).</span></span>

<span data-ttu-id="4fc79-155">Skrifttyper til andre formål er også tilgængelige i [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="4fc79-155">Fonts for other purposes are also available in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="4fc79-156">Du kan finde flere oplysninger i [Tilgængelige skrifttyper](ui-fonts.md)</span><span class="sxs-lookup"><span data-stu-id="4fc79-156">For more information, see [Available Fonts](ui-fonts.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="4fc79-157">Se også</span><span class="sxs-lookup"><span data-stu-id="4fc79-157">See Also</span></span>
[<span data-ttu-id="4fc79-158">Sådan opretter og ændrer du Brugerdefinerede rapportlayouts</span><span class="sxs-lookup"><span data-stu-id="4fc79-158">Create and Modify Custom Report Layouts</span></span>](ui-how-create-custom-report-layout.md)  
[<span data-ttu-id="4fc79-159">Skrifttyper i Business Central</span><span class="sxs-lookup"><span data-stu-id="4fc79-159">Fonts in Business Central</span></span>](ui-fonts.md)  
[<span data-ttu-id="4fc79-160">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="4fc79-160">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="4fc79-161">[Bankkontoafstemning](bank-manage-bank-accounts.md) </span><span class="sxs-lookup"><span data-stu-id="4fc79-161">[Reconciling Bank Accounts](bank-manage-bank-accounts.md) </span></span>  
[<span data-ttu-id="4fc79-162">Fuldførelse af periodeafslutningsprocesser</span><span class="sxs-lookup"><span data-stu-id="4fc79-162">Completing Period-End Processes</span></span>](year-how-complete-period-end-processes.md)  
<span data-ttu-id="4fc79-163">[Arbejde med [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4fc79-163">[Working with [!INCLUDE[prodshort](includes/prodshort.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4fc79-164">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="4fc79-164">General Business Functionality</span></span>](ui-across-business-areas.md)
