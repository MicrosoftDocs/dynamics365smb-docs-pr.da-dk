---
title: Oprette et kreditorkort for at registrere en ny leverandør | Microsoft Docs
description: Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f1028b91101f8faa38d4d4d5d2695ee498ff6d2e
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5772650"
---
# <a name="register-new-vendors"></a><span data-ttu-id="c694b-103">Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="c694b-103">Register New Vendors</span></span>

<span data-ttu-id="c694b-104">Kreditorer leverer de produkter, du sælger.</span><span class="sxs-lookup"><span data-stu-id="c694b-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="c694b-105">Hver kreditor, som du køber fra, skal registreres som et kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="c694b-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="c694b-106">Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="c694b-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="c694b-107">Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere.</span><span class="sxs-lookup"><span data-stu-id="c694b-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="c694b-108">En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="c694b-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="c694b-109">Du kan finde flere oplysninger i [Opsætning af indkøb](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="c694b-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="c694b-110">Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c694b-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="c694b-111">Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="c694b-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="c694b-112">Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-112">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="c694b-113">Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>
<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3PZtd?rel=0]

## <a name="adding-new-vendors"></a><span data-ttu-id="c694b-114">Tilføjelse af nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="c694b-114">Adding new vendors</span></span>

<span data-ttu-id="c694b-115">Hvis du vil registrere en ny kreditor, skal du udfylde et kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="c694b-115">To register a new vendor, you must fill in a vendor card.</span></span> <span data-ttu-id="c694b-116">Du kan oprette skabeloner til forskellige kreditorprofiler, eller du kan tilføje kreditorer uden skabeloner.</span><span class="sxs-lookup"><span data-stu-id="c694b-116">You can establish templates for different vendor profiles, or you can add vendors without templates.</span></span> <span data-ttu-id="c694b-117">Du kan også oprette en kreditor ud fra en kontakt.</span><span class="sxs-lookup"><span data-stu-id="c694b-117">You can also create a vendor from a contact.</span></span> <span data-ttu-id="c694b-118">Du kan finde flere oplysninger i [Sådan oprettes en debitor-, kreditor-, medarbejder- eller bankkonto fra en kontakt](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span><span class="sxs-lookup"><span data-stu-id="c694b-118">For more information, see [To create a customer, vendor, employee, or bank account from a contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).</span></span>  

> [!NOTE]  
> <span data-ttu-id="c694b-119">Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk en side, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-119">If vendor templates exist for different vendor types, then a page appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="c694b-120">Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-120">If only one vendor template exists, then new vendor cards always use that template.</span></span>  

### <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="c694b-121">Sådan oprettes et nyt kreditorkort</span><span class="sxs-lookup"><span data-stu-id="c694b-121">To create a new vendor card</span></span>

1. <span data-ttu-id="c694b-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c694b-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c694b-123">På siden **Kreditorer** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c694b-123">On the **Vendors** page, Choose **New**.</span></span>

    <span data-ttu-id="c694b-124">Hvis der er mere end én kreditorskabelon, åbnes der automatisk en side, hvor du kan vælge en kreditorskabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-124">If more than one vendor template exists, then a page opens from which you can select a vendor template.</span></span> <span data-ttu-id="c694b-125">I dette tilfælde skal du følge de næste to trin.</span><span class="sxs-lookup"><span data-stu-id="c694b-125">In that case, follow the next two steps.</span></span>
    1. <span data-ttu-id="c694b-126">På siden **Vælg en skabelon til en ny kreditor** skal du vælge den skabelon, som du vil bruge til det nye kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="c694b-126">On the **Select a template for a new vendor** page, choose the template that you want to use for the new vendor card.</span></span>
    2. <span data-ttu-id="c694b-127">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c694b-127">Choose the **OK** button.</span></span> <span data-ttu-id="c694b-128">Et nyt kreditorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c694b-128">A new vendor card opens with some fields filled with information from the template.</span></span>
3. <span data-ttu-id="c694b-129">Fortsæt med at udfylde eller ændre felterne på kreditorkortet efter behov.</span><span class="sxs-lookup"><span data-stu-id="c694b-129">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!TIP]  
    > <span data-ttu-id="c694b-130">Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Kreditornr.**.</span><span class="sxs-lookup"><span data-stu-id="c694b-130">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Vendor No.** field.</span></span> <span data-ttu-id="c694b-131">Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)</span><span class="sxs-lookup"><span data-stu-id="c694b-131">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="c694b-132">Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="c694b-132">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="c694b-133">Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-133">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="c694b-134">Du kan finde flere oplysninger i afsnittet [Sådan gemmes kreditorkortet som en skabelon](#to-save-the-vendor-card-as-a-template).</span><span class="sxs-lookup"><span data-stu-id="c694b-134">For more information, see the [To save the vendor card as a template](#to-save-the-vendor-card-as-a-template) section.</span></span>

### <a name="deleting-vendor-cards"></a><span data-ttu-id="c694b-135">Sletning af kreditorkort</span><span class="sxs-lookup"><span data-stu-id="c694b-135">Deleting vendor cards</span></span>

<span data-ttu-id="c694b-136">Hvis du har bogført en postering for en kreditor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision.</span><span class="sxs-lookup"><span data-stu-id="c694b-136">If you have posted a transaction for a vendor, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="c694b-137">Hvis du vil slette kreditorkort med poster, skal du kontakte din Microsoft-partner for at gøre dette via kode.</span><span class="sxs-lookup"><span data-stu-id="c694b-137">To delete vendor cards with ledger entries, contact your Microsoft partner to do so through code.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="c694b-138">Sådan gemmes kreditorkortet som en skabelon</span><span class="sxs-lookup"><span data-stu-id="c694b-138">To save the vendor card as a template</span></span>

1. <span data-ttu-id="c694b-139">På siden **Kreditorkort** skal du vælge handlingen **Gem som skabelon**.</span><span class="sxs-lookup"><span data-stu-id="c694b-139">On the **Vendor Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="c694b-140">Siden **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.</span><span class="sxs-lookup"><span data-stu-id="c694b-140">The **Vendor Template** page opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="c694b-141">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c694b-141">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="c694b-142">Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="c694b-142">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="c694b-143">Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="c694b-143">The **Dimension Templates** page opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="c694b-144">Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c694b-144">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="c694b-145">Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="c694b-145">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="c694b-146">Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="c694b-146">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="c694b-147">Se også</span><span class="sxs-lookup"><span data-stu-id="c694b-147">See Also</span></span>

[<span data-ttu-id="c694b-148">Flette dublerede poster</span><span class="sxs-lookup"><span data-stu-id="c694b-148">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="c694b-149">Oprette nummerserie</span><span class="sxs-lookup"><span data-stu-id="c694b-149">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="c694b-150">Køb</span><span class="sxs-lookup"><span data-stu-id="c694b-150">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="c694b-151">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="c694b-151">Record Purchases</span></span>](purchasing-how-record-purchases.md)  
<span data-ttu-id="c694b-152">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c694b-152">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  

[!INCLUDE[footer-include](includes/footer-banner.md)]