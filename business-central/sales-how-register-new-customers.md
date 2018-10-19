---
title: Oprette et debitorkort for at registrere nye kunder | Microsoft Docs
description: "Beskriver, hvordan du opretter et debitorkort for at registrere oplysninger om hver ny kunde, du sælger til."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: client
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: c249e186395df580e55a806fe7446f4d13c7b786
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="register-new-customers"></a><span data-ttu-id="ccb5c-103">Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="ccb5c-103">Register New Customers</span></span>
<span data-ttu-id="ccb5c-104">Debitorer er kilden til din indtægt.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-104">Customers are the source of your income.</span></span> <span data-ttu-id="ccb5c-105">Du skal registrere hver debitor, du sælger til som et debitorkort.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-105">You must register each customer you sell to as a customer card.</span></span> <span data-ttu-id="ccb5c-106">Debitorkort indeholder de oplysninger, som er en forudsætning for at sælge produkter til debitoren.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-106">Customer cards hold the information that is required to sell products to the customer.</span></span> <span data-ttu-id="ccb5c-107">Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md) og [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="ccb5c-107">For more information, see [Invoice Sales](sales-how-invoice-sales.md) and [Register New Items](inventory-how-register-new-items.md).</span></span>  

<span data-ttu-id="ccb5c-108">Før du kan registrere nye debitorer, skal du oprette forskellige salgskoder, som du kan vælge mellem, når du udfylder debitorkort.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-108">Before you can register new customers, you must set up various sales codes that you can select from when you fill in customer cards.</span></span> <span data-ttu-id="ccb5c-109">Der er flere oplysninger i [Konfigurere salg](sales-setup-sales.md).</span><span class="sxs-lookup"><span data-stu-id="ccb5c-109">For more information, see [Setting Up Sales](sales-setup-sales.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="ccb5c-110">Hvis der er debitorskabeloner for forskellige debitortyper, vises der automatisk et vindue, når du opretter et nyt debitorkort, hvorfra du kan vælge en passende skabelon.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-110">If customer templates exist for different customer types, then a window appears when you create a new customer card from where you can select an appropriate template.</span></span> <span data-ttu-id="ccb5c-111">Hvis der kun er én debitorskabelon, bruger nye debitorkort altid denne skabelon.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-111">If only one customer template exists, then new customer cards always use that template.</span></span>

## <a name="to-create-a-new-customer-card"></a><span data-ttu-id="ccb5c-112">Sådan oprettes et nyt debitorkort</span><span class="sxs-lookup"><span data-stu-id="ccb5c-112">To create a new customer card</span></span>
1. <span data-ttu-id="ccb5c-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customers**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ccb5c-114">I vinduet **Debitorer** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-114">In the **Customers** window, choose the **New** action.</span></span>

    <span data-ttu-id="ccb5c-115">Hvis der kun er ét debitorbilag, åbnes der et nyt debitorkort, hvor nogle felter er udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-115">If only one customer template exists, then a new customer card opens with some fields filled with information from the template.</span></span>

    <span data-ttu-id="ccb5c-116">Hvis der er mere end én debitorskabelon, åbnes der automatisk et vindue, hvor du kan vælge en debitorskabelon.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-116">If more than one customer template exists, then a window opens from which you can select a customer template.</span></span> <span data-ttu-id="ccb5c-117">I dette tilfælde skal du følge de næste to trin.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-117">In that case, follow the next two steps.</span></span>
3. <span data-ttu-id="ccb5c-118">I vinduet **Vælg en skabelon til en ny debitor** skal du vælge den skabelon, som du vil bruge til det nye debitorkort.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-118">In the **Select a template for a new customer** window, choose the template that you want to use for the new customer card.</span></span>
4. <span data-ttu-id="ccb5c-119">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-119">Choose the **OK** button.</span></span> <span data-ttu-id="ccb5c-120">Et nyt debitorkort åbnes med nogle felter udfyldt med oplysninger fra skabelonen.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-120">A new customer card opens with some fields filled with information from the template.</span></span>  
5. <span data-ttu-id="ccb5c-121">Fortsæt med at udfylde eller ændre felterne på debitorkortet efter behov.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-121">Proceed to fill or change fields on the customer card as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="ccb5c-122">I oversigtspanelet **Salgspriser** kan du se specialpriser eller rabatter, som du tildeler til debitoren, hvis bestemte kriterier opfyldes, f.eks. vare, mindste ordrestørrelse eller slutdato.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-122">On the **Sales Prices** FastTab, you can view special prices or discounts that you grant for the customer if certain criteria are met, such as item, minimum order quantity, or ending date.</span></span> <span data-ttu-id="ccb5c-123">Hver række repræsenterer en specialpris- eller en linjerabat.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-123">Each row represents a special price or line discount.</span></span> <span data-ttu-id="ccb5c-124">Hver kolonne repræsenterer et kriterium, der skal anvendes for at garantere den specialpris, du angiver i feltet **Enhedspris** eller den linjerabat, som du angiver i feltet **Linjerabatpct.**</span><span class="sxs-lookup"><span data-stu-id="ccb5c-124">Each column represents a criterion that must apply to warrant the special price that you enter in the **Unit Price** field, or the line discount that you enter in the **Line Discount %** field.</span></span> <span data-ttu-id="ccb5c-125">Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).</span><span class="sxs-lookup"><span data-stu-id="ccb5c-125">For more information, see [Record Sales Price, Discount, and Payment Agreements](sales-how-record-sales-price-discount-payment-agreements.md).</span></span>

<span data-ttu-id="ccb5c-126">Debitoren er nu registreret, og debitorkortet er klar til at blive brugt i salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-126">The customer is now registered, and the customer card is ready to be used on sales documents.</span></span>

<span data-ttu-id="ccb5c-127">Hvis du vil bruge dette debitorkort som skabelon, når du opretter nye debitorkort, kan du gemme det som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-127">If you want to use this customer card as a template when you create new customer cards, you can save it as a template.</span></span> <span data-ttu-id="ccb5c-128">Du kan finde flere oplysninger i følgende afsnit.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-128">For more information, see the following section.</span></span>

## <a name="to-save-the-customer-card-as-a-template"></a><span data-ttu-id="ccb5c-129">Sådan gemmes debitorkortet som en skabelon</span><span class="sxs-lookup"><span data-stu-id="ccb5c-129">To save the customer card as a template</span></span>
1. <span data-ttu-id="ccb5c-130">I vinduet **Debitorkort** skal du vælge handlingen **Gem som skabelon**.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-130">In the **Customer Card** window, choose the **Save as Template** action.</span></span> <span data-ttu-id="ccb5c-131">Vinduet **Debitorskabelon** åbnes med debitorkortet som skabelon.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-131">The **Customer Template** window opens showing the customer card as a template.</span></span>
2. <span data-ttu-id="ccb5c-132">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-132">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="ccb5c-133">Hvis du vil genbruge dimensioner i kladder, skal du vælge handlingen **Dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-133">To reuse dimensions in templates, choose the **Dimensions** action.</span></span> <span data-ttu-id="ccb5c-134">Vinduet **Skabeloner til dimensioner** åbnes med alle dimensionsværdikoder, der er konfigureret for debitoren.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-134">The **Dimension Templates** window opens showing any dimension codes that are set up for the customer.</span></span>
4. <span data-ttu-id="ccb5c-135">Rediger eller angiv dimensionskoder, der skal gælde for nye debitorkort, oprettes ved hjælp af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-135">Edit or enter dimension codes that will apply to new customer cards created by using the template.</span></span>  
5. <span data-ttu-id="ccb5c-136">Når du har fuldført skabelonen for den nye debitor, skal du vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-136">When you have completed the new customer template, choose the **OK** button.</span></span>

<span data-ttu-id="ccb5c-137">Debitorskabelonen føjes til listen over debitorskabeloner, så du kan bruge den til at oprette nye debitorkort.</span><span class="sxs-lookup"><span data-stu-id="ccb5c-137">The customer template is added to the list of customer templates, so that you can use it to create new customer cards.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccb5c-138">Se også</span><span class="sxs-lookup"><span data-stu-id="ccb5c-138">See Also</span></span>
[<span data-ttu-id="ccb5c-139">Oprette nummerserie</span><span class="sxs-lookup"><span data-stu-id="ccb5c-139">Create Number Series</span></span>](ui-create-number-series.md)  
<span data-ttu-id="ccb5c-140">[Salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="ccb5c-140">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="ccb5c-141">[Konfigurere salg](sales-setup-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="ccb5c-141">[Setting Up Sales](sales-setup-sales.md)  </span></span>  
<span data-ttu-id="ccb5c-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ccb5c-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

