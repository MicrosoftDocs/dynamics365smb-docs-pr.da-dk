---
title: "Oprette og bruge standardlinjer til tilbagevendende salg og køb | Microsoft Docs"
description: "Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 85d15de13739e944ff8817b402b37ae1c7e1b144
ms.openlocfilehash: 980a0646317c2b5c02c0eadcde9ba984c11580c4
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="1001f-103">Fremgangsmåde: Oprette gentagne salgs- og købslinjer</span><span class="sxs-lookup"><span data-stu-id="1001f-103">How to: Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="1001f-104">Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.</span><span class="sxs-lookup"><span data-stu-id="1001f-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="1001f-105">Følgende procedure viser, hvordan du arbejder med standardsalgslinjer.</span><span class="sxs-lookup"><span data-stu-id="1001f-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="1001f-106">Det fungerer på samme måde for standardkøbslinjer.</span><span class="sxs-lookup"><span data-stu-id="1001f-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="1001f-107">Sådan opretter du standardsalgslinjer</span><span class="sxs-lookup"><span data-stu-id="1001f-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="1001f-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Standardsalgskoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1001f-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Sales Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1001f-109">Vælg handlingen **Ny** i vinduet **Standardsalgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1001f-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="1001f-110">Udfyld felterne efter behov i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1001f-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="1001f-111">I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1001f-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="1001f-112">Sådan indsættes standardsalgslinjer i en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="1001f-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="1001f-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Fakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1001f-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1001f-114">Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.</span><span class="sxs-lookup"><span data-stu-id="1001f-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="1001f-115">Vælg handlingen **Hent tilbagevendende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1001f-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="1001f-116">I vinduet **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.</span><span class="sxs-lookup"><span data-stu-id="1001f-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>
5. <span data-ttu-id="1001f-117">Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge eller redigere oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="1001f-117">Choose the **OK** button to insert the standard sales lines on the invoice, where you can reuse as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="1001f-118">Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer</span><span class="sxs-lookup"><span data-stu-id="1001f-118">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="1001f-119">Du kan bruge kørslen **Opret tilbagevendende salgsfaktura**</span><span class="sxs-lookup"><span data-stu-id="1001f-119">You can use the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1001f-120">til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgskoden.</span><span class="sxs-lookup"><span data-stu-id="1001f-120">batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales code.</span></span>

<span data-ttu-id="1001f-121">I vinduet **Tilbagevendende salgslinjer** kan du også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale.</span><span class="sxs-lookup"><span data-stu-id="1001f-121">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="1001f-122">De salgsfakturaer, der bliver oprettet med kørslen **Opret tilbagevendende salgsfaktura**,</span><span class="sxs-lookup"><span data-stu-id="1001f-122">The sales invoices that are created with the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1001f-123">vil derefter indeholde de oplysninger, der skal bruges til at opkræve betaling for salgsfakturaerne, med SEPA-Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="1001f-123">batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="1001f-124">Du kan finde flere oplysninger i Indhente betalinger med SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="1001f-124">For more information, see Collect Payments with SEPA Direct Debit.</span></span>

1. <span data-ttu-id="1001f-125">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1001f-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1001f-126">I vinduet **Opret tilbagevendende salgsfaktura**</span><span class="sxs-lookup"><span data-stu-id="1001f-126">In the **Create Recurring Sales Inv.**</span></span> <span data-ttu-id="1001f-127">skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="1001f-127">window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1001f-128">I feltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.</span><span class="sxs-lookup"><span data-stu-id="1001f-128">In the **Code** field, enter the code for standard sales lines assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="1001f-129">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="1001f-129">Choose the **OK** button.</span></span>

<span data-ttu-id="1001f-130">Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="1001f-130">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="1001f-131">Se også</span><span class="sxs-lookup"><span data-stu-id="1001f-131">See Also</span></span>  
[<span data-ttu-id="1001f-132">Salg</span><span class="sxs-lookup"><span data-stu-id="1001f-132">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="1001f-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1001f-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

