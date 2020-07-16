---
title: Oprette et debitorkort for at registrere nye kunder | Microsoft Docs
description: Beskriver, hvordan du opretter et debitorkort for at registrere oplysninger om hver ny kunde, du sælger til.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 06/24/2020
ms.author: sgroespe
ms.openlocfilehash: cc48c7c55edac8af9333dd04661a828c528621b8
ms.sourcegitcommit: 63102669366eb26f9c32729848170bc2e5c4d6ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/25/2020
ms.locfileid: "3503969"
---
# <a name="register-new-customers"></a><span data-ttu-id="99128-103">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="99128-103">Register New Customers</span></span>

<span data-ttu-id="99128-104">Debitorer er kilden til din indtægt.</span><span class="sxs-lookup"><span data-stu-id="99128-104">Customers are the source of your income.</span></span> <span data-ttu-id="99128-105">Du skal registrere hver debitor, du sælger til som et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="99128-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="99128-106">Debitorkort indeholder de oplysninger, som er en forudsætning for at sælge produkter til debitoren.</span><span class="sxs-lookup"><span data-stu-id="99128-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="99128-107">Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="99128-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="99128-108">Før du kan registrere nye debitorer, skal du oprette forskellige salgskoder, som du kan vælge mellem, når du udfylder debitorkort.</span><span class="sxs-lookup"><span data-stu-id="99128-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="99128-109">Der er flere oplysninger i [Konfigurere salg](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="99128-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3PZsM]

## <a name="adding-new-customers"></a><span data-ttu-id="99128-110">Tilføje nye debitorer</span><span class="sxs-lookup"><span data-stu-id="99128-110">Adding new customers</span></span>

<span data-ttu-id="99128-111">Hvis du vil registrere en ny debitor, skal du udfylde et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="99128-111">To register a new customer, you must fill in a customer card.</span></span> <span data-ttu-id="99128-112">Du kan oprette skabeloner til forskellige debitorprofiler, eller du kan tilføje debitorer uden skabeloner.</span><span class="sxs-lookup"><span data-stu-id="99128-112">You can establish templates for different customer profiles, or you can add customers without templates.</span></span>  

> [!NOTE]  
> <span data-ttu-id="99128-113">Hvis der er debitorskabeloner for forskellige debitortyper, vises der automatisk på side, når du opretter et nyt debitorkort, hvorfra du kan vælge en passende skabelon.</span><span class="sxs-lookup"><span data-stu-id="99128-113">If customer templates exist for different customer types, then a page appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="99128-114">Hvis der kun er én debitorskabelon, bruger nye debitorkort altid denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="99128-114">If only one customer template exists, then new customer cards always use that template.</span></span>  

### <a name="to-create-a-new-customer-card"></a><span data-ttu-id="99128-115">Sådan oprettes et nyt debitorkort</span><span class="sxs-lookup"><span data-stu-id="99128-115">To create a new customer card</span></span>

1. <span data-ttu-id="99128-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="99128-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="99128-117">På siden **Debitorer** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="99128-117">On the **Customers** page, choose the **New** action.</span></span>

    <span data-ttu-id="99128-118">Hvis der kun er ét debitorbilag, åbnes der et nyt debitorkort, hvor nogle felter er udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="99128-118">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="99128-119">Hvis der er mere end én debitorskabelon, åbnes der automatisk på side, hvor du kan vælge en debitorskabelon.</span><span class="sxs-lookup"><span data-stu-id="99128-119">If more than one customer template exists, then a page opens from which you can select a customer template.</span></span> <span data-ttu-id="99128-120">I dette tilfælde skal du følge de næste to trin.</span><span class="sxs-lookup"><span data-stu-id="99128-120">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="99128-121">På siden **Vælg en skabelon til en ny debitor** skal du vælge den skabelon, som du vil bruge til det nye debitorkort.</span><span class="sxs-lookup"><span data-stu-id="99128-121">On the **Select a template for a new customer** page, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="99128-122">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="99128-122">Choose the **OK** button.</span></span> <span data-ttu-id="99128-123">Et nyt debitorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="99128-123">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="99128-124">Fortsæt med at udfylde eller ændre felterne på debitorkortet efter behov.</span><span class="sxs-lookup"><span data-stu-id="99128-124">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="99128-125">I oversigtspanelet **Salgspriser** kan du se specialpriser eller rabatter, som du tildeler til debitoren, hvis bestemte kriterier opfyldes, f.eks. vare, mindste ordrestørrelse eller slutdato.</span><span class="sxs-lookup"><span data-stu-id="99128-125">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="99128-126">Hver række repræsenterer en specialpris- eller en linjerabat.</span><span class="sxs-lookup"><span data-stu-id="99128-126">Each row represents a special price or line discount.</span></span> <span data-ttu-id="99128-127">Hver kolonne repræsenterer et kriterium, der skal anvendes for at garantere den specialpris, du angiver i feltet **Enhedspris** eller den linjerabat, som du angiver i feltet **Linjerabatpct.**</span><span class="sxs-lookup"><span data-stu-id="99128-127">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="99128-128">Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="99128-128">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="99128-129">Debitoren er nu registreret, og debitorkortet er klar til at blive brugt i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="99128-129">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="99128-130">Hvis du vil bruge dette debitorkort som skabelon, når du opretter nye debitorkort, kan du gemme det som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="99128-130">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="99128-131">Du kan finde flere oplysninger i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="99128-131">For more information, see the following section.</span></span>  

### <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="99128-132">Sådan gemmes debitorkortet som en skabelon</span><span class="sxs-lookup"><span data-stu-id="99128-132">To save the customer card as a template</span></span>

1. <span data-ttu-id="99128-133">På siden **Debitorkort** skal du vælge handlingen **Gem som skabelon**.</span><span class="sxs-lookup"><span data-stu-id="99128-133">On the **Customer Card** page, choose the **Save as Template** action.</span></span> <span data-ttu-id="99128-134">Siden **Debitorskabelon** åbnes med debitorkortet som skabelon.</span><span class="sxs-lookup"><span data-stu-id="99128-134">The **Customer Template** page opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="99128-135">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="99128-135">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="99128-136">Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="99128-136">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="99128-137">Siden **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for debitoren.</span><span class="sxs-lookup"><span data-stu-id="99128-137">The **Dimension Templates** page opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="99128-138">Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="99128-138">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="99128-139">Når du har fuldført skabelonen for den nye debitor, skal du vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="99128-139">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="99128-140">Debitorskabelonen føjes til listen over debitorskabeloner, så du kan bruge den til at oprette nye debitorkort.</span><span class="sxs-lookup"><span data-stu-id="99128-140">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="deleting-customer-cards"></a><span data-ttu-id="99128-141">Slette debitorkort</span><span class="sxs-lookup"><span data-stu-id="99128-141">Deleting customer cards</span></span>

<span data-ttu-id="99128-142">Hvis du har bogført en postering for en debitor, kan du ikke slette kortet, da posterne muligvis er nødvendige med henblik på revision.</span><span class="sxs-lookup"><span data-stu-id="99128-142">If you have posted a transaction for a customer, you cannot delete the card because the ledger entries may be needed for auditing.</span></span> <span data-ttu-id="99128-143">Hvis du vil slette debitorkort med poster, skal du kontakte Microsoft-partneren for at gøre dette via kode.</span><span class="sxs-lookup"><span data-stu-id="99128-143">To delete customer cards with ledger entries, contact to Microsoft partner to do so through code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="99128-144">Se også</span><span class="sxs-lookup"><span data-stu-id="99128-144">See Also</span></span>

[<span data-ttu-id="99128-145">Definere betalingsformer</span><span class="sxs-lookup"><span data-stu-id="99128-145">Defining Payment Methods</span></span>](finance-payment-methods.md)  
[<span data-ttu-id="99128-146">Flette dublerede poster</span><span class="sxs-lookup"><span data-stu-id="99128-146">Merge Duplicate Records</span></span>](sales-how-merge-duplicate-records.md)  
[<span data-ttu-id="99128-147">Oprette nummerserie</span><span class="sxs-lookup"><span data-stu-id="99128-147">Create Number Series</span></span>](ui-create-number-series.md)  
[<span data-ttu-id="99128-148">Salg</span><span class="sxs-lookup"><span data-stu-id="99128-148">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="99128-149">Konfigurere salg</span><span class="sxs-lookup"><span data-stu-id="99128-149">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="99128-150">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="99128-150">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
