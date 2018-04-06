---
title: "Oprette et kreditorkort for at registrere en ny leverandør | Microsoft Docs"
description: "Lær, hvordan du opretter et kreditorkort for at registrere en ny kreditor eller leverandør."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: supplier
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f154aeaf4bd7d9960dc4f586b9e3054b76eb5e7e
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="register-new-vendors"></a><span data-ttu-id="be12f-103">Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="be12f-103">Register New Vendors</span></span>
<span data-ttu-id="be12f-104">Kreditorer leverer de produkter, du sælger.</span><span class="sxs-lookup"><span data-stu-id="be12f-104">Vendors provide the products that you sell.</span></span> <span data-ttu-id="be12f-105">Hver kreditor, som du køber fra, skal registreres som et kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="be12f-105">Each vendor that you purchase from must be registered as a vendor card.</span></span>

<span data-ttu-id="be12f-106">Før du kan registrere nye kreditorer, skal du oprette forskellige købskoder, som du kan vælge mellem, når du udfylder kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="be12f-106">Before you can register new vendors, you must set up various purchase codes that you can select from when you fill vendor cards.</span></span> <span data-ttu-id="be12f-107">Når alle de obligatoriske stamoplysninger er oprettet, skan du udføre yderligere konfiguration af kreditoren, f.eks. prioritere kreditoren i forbindelse med betaling og få vist de varer, som kreditoren og andre kreditorer kan levere.</span><span class="sxs-lookup"><span data-stu-id="be12f-107">When all of the required master data is created, you can perform additional configuration of the vendor, such as prioritize the vendor for payment purposes and list items that the vendor and other vendors can supply.</span></span> <span data-ttu-id="be12f-108">En anden gruppe opsætningsopgaver for kreditorer er at registrere aftaler vedrørende rabatter, priser og betalingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="be12f-108">Another group of setup tasks for vendors is to record your agreements concerning discounts, prices, and payment methods.</span></span> <span data-ttu-id="be12f-109">Du kan finde flere oplysninger under [Opsætning af indkøb](purchasing-setup-purchasing.md).</span><span class="sxs-lookup"><span data-stu-id="be12f-109">For more information, see [Setting Up Purchasing](purchasing-setup-purchasing.md).</span></span>

<span data-ttu-id="be12f-110">Kreditorkortene indeholde de oplysninger, som er en forudsætning for at købe produkter fra kreditoren.</span><span class="sxs-lookup"><span data-stu-id="be12f-110">Vendor cards hold the information that is required to buy products from the vendor.</span></span> <span data-ttu-id="be12f-111">Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="be12f-111">For more information, see [Record Purchases](purchasing-how-record-purchases.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="be12f-112">Hvis der er kreditorskabeloner til forskellige kreditortyper, vises der automatisk et vindue, når du opretter et nyt kreditorkort, hvorfra du kan vælge en passende skabelon.</span><span class="sxs-lookup"><span data-stu-id="be12f-112">If vendor templates exist for different vendor types, then a window appears when you create a new vendor card from where you can select an appropriate template.</span></span> <span data-ttu-id="be12f-113">Hvis der kun er én kreditorskabelon, bruger nye kreditorkort altid denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="be12f-113">If only one vendor template exists, then new vendor cards always use that template.</span></span>

## <a name="to-create-a-new-vendor-card"></a><span data-ttu-id="be12f-114">Sådan oprettes et nyt kreditorkort</span><span class="sxs-lookup"><span data-stu-id="be12f-114">To create a new vendor card</span></span>
1. <span data-ttu-id="be12f-115">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="be12f-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>  
2. <span data-ttu-id="be12f-116">I vinduet **Kreditorer** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="be12f-116">In the **Vendors** window, Choose **New**.</span></span>

    <span data-ttu-id="be12f-117">Hvis der er mere end én kreditorskabelon, åbnes der automatisk et vindue, hvor du kan vælge en kreditorskabelon.</span><span class="sxs-lookup"><span data-stu-id="be12f-117">If more than one vendor template exists, then a window opens from which you can select a vendor template.</span></span> <span data-ttu-id="be12f-118">I dette tilfælde skal du følge de næste to trin.</span><span class="sxs-lookup"><span data-stu-id="be12f-118">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="be12f-119">I vinduet **Vælg en skabelon til en ny kreditor** skal du vælge den skabelon, som du vil bruge til det nye kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="be12f-119">In the **Select a template for a new vendor** window, choose the template that you want to use for the new vendor card.</span></span>
4. <span data-ttu-id="be12f-120">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="be12f-120">Choose the **OK** button.</span></span> <span data-ttu-id="be12f-121">Et nyt kreditorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="be12f-121">A new vendor card opens with some fields filled with information from the template.</span></span>
5. <span data-ttu-id="be12f-122">Fortsæt med at udfylde eller ændre felterne på kreditorkortet efter behov.</span><span class="sxs-lookup"><span data-stu-id="be12f-122">Proceed to fill or change fields on the vendor card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="be12f-123">Hvis du ikke på forhånd kender den faktureringsadresse, der skal bruges til alle fakturaer fra en kreditor, skal du ikke udfylde feltet **Faktureringsleverandørnr.** på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="be12f-123">If you do not know the invoicing address that will be used for every invoice from a vendor, do not fill in the **Pay-to** field.</span></span> <span data-ttu-id="be12f-124">Vælg i stedet nummeret, efter du har oprettet et dokumenthoved (købsrekvisition, ordre eller faktura)</span><span class="sxs-lookup"><span data-stu-id="be12f-124">Instead, choose the pay-to vendor number after you have set up a purchase quote, order, or invoice header.</span></span>

<span data-ttu-id="be12f-125">Kreditoren er nu registreret, og kreditorkortet er klar til at blive brugt i købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="be12f-125">The vendor is now registered, and the vendor card is ready to be used on purchase documents.</span></span>

<span data-ttu-id="be12f-126">Hvis du vil bruge dette kreditorkort som skabelon, når du opretter nye kreditorkort, kan du gemme det som en kreditorskabelon.</span><span class="sxs-lookup"><span data-stu-id="be12f-126">If you want to use this vendor card as a template when you create new vendor cards, you can save it as a vendor template.</span></span> <span data-ttu-id="be12f-127">Du kan finde flere oplysninger i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="be12f-127">For more information, see the following section.</span></span>

## <a name="to-save-the-vendor-card-as-a-template"></a><span data-ttu-id="be12f-128">Sådan gemmes kreditorkortet som en skabelon</span><span class="sxs-lookup"><span data-stu-id="be12f-128">To save the vendor card as a template</span></span>
1. <span data-ttu-id="be12f-129">I vinduet **Kreditorkort** skal du vælge handlingen **Gem som skabelon**.</span><span class="sxs-lookup"><span data-stu-id="be12f-129">In the **Vendor Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="be12f-130">Vinduet **Kreditorskabelon** åbnes og viser kreditorkortet som skabelon.</span><span class="sxs-lookup"><span data-stu-id="be12f-130">The **Vendor Template** window opens showing the vendor card as a template.</span></span>
2. <span data-ttu-id="be12f-131">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="be12f-131">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="be12f-132">Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="be12f-132">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="be12f-133">Vinduet **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for kreditoren.</span><span class="sxs-lookup"><span data-stu-id="be12f-133">The **Dimension Templates** window opens showing any dimension codes that are set up for the vendor.</span></span>
4. <span data-ttu-id="be12f-134">Rediger eller angiv dimensionskoder, der skal gælde for nye kreditorkort, oprettes ved hjælp af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="be12f-134">Edit or enter dimension codes that will apply to new vendor cards created by using the template.</span></span>
5. <span data-ttu-id="be12f-135">Når du har fuldført skabelonen for den nye kreditor, skal du vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="be12f-135">When you have completed the new vendor template, choose the **OK** button.</span></span>  
   <span data-ttu-id="be12f-136">Kreditorskabelonen føjes til listen over kreditorskabeloner, så du kan bruge den til at oprette nye kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="be12f-136">The vendor template is added to the list of vendor templates, so that you can use it to create new vendor cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="be12f-137">Se også</span><span class="sxs-lookup"><span data-stu-id="be12f-137">See Also</span></span>
[<span data-ttu-id="be12f-138">Køb</span><span class="sxs-lookup"><span data-stu-id="be12f-138">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="be12f-139">[Registrere køb](purchasing-how-record-purchases.md) </span><span class="sxs-lookup"><span data-stu-id="be12f-139">[Record Purchases](purchasing-how-record-purchases.md) </span></span>  
<span data-ttu-id="be12f-140">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="be12f-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

