---
title: "Oprette standardlinjer til tilbagevendende salg og køb | Microsoft Docs"
description: "Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: df4f093ded0a55d45c40be15c5888035d6e3b2df
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="create-recurring-sales-and-purchase-lines"></a><span data-ttu-id="1a0f5-103">Oprette gentagne salgs- og købslinjer</span><span class="sxs-lookup"><span data-stu-id="1a0f5-103">Create Recurring Sales and Purchase Lines</span></span>
<span data-ttu-id="1a0f5-104">Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-104">If you often need to create sales and purchase lines with similar information, you can set up standard lines that you can then insert on recurring sales and purchase documents, for example, for recurring replenishment orders.</span></span>  

<span data-ttu-id="1a0f5-105">Følgende procedure viser, hvordan du arbejder med standardsalgslinjer.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-105">The following procedure shows how to work with standard sales lines.</span></span> <span data-ttu-id="1a0f5-106">Det fungerer på samme måde for standardkøbslinjer.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-106">It works in a similar way for standard purchase lines.</span></span>  

## <a name="to-set-up-standard-sales-lines"></a><span data-ttu-id="1a0f5-107">Sådan opretter du standardsalgslinjer</span><span class="sxs-lookup"><span data-stu-id="1a0f5-107">To set up standard sales lines</span></span>  
1. <span data-ttu-id="1a0f5-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Standardsalgslinjer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Standard Sales Lines**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1a0f5-109">Vælg handlingen **Ny** i vinduet **Standardsalgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-109">In the **Standard Sales Lines** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="1a0f5-110">Udfyld felterne efter behov i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-110">On the **General** FastTab, fill the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="1a0f5-111">I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-111">On the **Lines** FastTab, enter information in the fields to prepare sales lines that reflect the standard lines that you expect to use as recurring lines on sales documents.</span></span>  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a><span data-ttu-id="1a0f5-112">Sådan indsættes standardsalgslinjer i en salgsfaktura</span><span class="sxs-lookup"><span data-stu-id="1a0f5-112">To insert standard sales lines on a sales invoice</span></span>
1. <span data-ttu-id="1a0f5-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Fakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a0f5-114">Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-114">Open the sales invoice that you want to insert one or more standard sales lines on.</span></span>
3. <span data-ttu-id="1a0f5-115">Vælg handlingen **Hent tilbagevendende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-115">Choose the **Get Recurring Sales Lines** action.</span></span>
4. <span data-ttu-id="1a0f5-116">I vinduet **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-116">In the **Recurring Sales Lines** window, choose the lookup button in the **Code** field, and then select a set of standard sales lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a0f5-117">For at bruge de tilbagevendende salgslinjer, der er indstillet, sammen med kørslen **Opret tilbagevendende salgsfakturaer**, skal du også udfylde felterne **Datoen Gyldig fra** og **Datoen Gyldig til** i vinduet **Tilbagevendende salgslinjer**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-117">To use the recurring sales lines set together with the **Create Recurring Sales Invoices** batch job, you must also fill in the **Valid From Date** and **Valid To Date** fields in the **Recurring Sales Lines** window.</span></span> <span data-ttu-id="1a0f5-118">Du kan finde flere oplysninger i "Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer".</span><span class="sxs-lookup"><span data-stu-id="1a0f5-118">For more information, see the "To create multiple sales invoices based on standard sales lines" section.</span></span>

5. <span data-ttu-id="1a0f5-119">Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge dem eller redigere oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-119">Choose the **OK** button to insert the standard sales lines on the invoice where you can reuse them as is or edit the information.</span></span>

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a><span data-ttu-id="1a0f5-120">Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer</span><span class="sxs-lookup"><span data-stu-id="1a0f5-120">To create multiple sales invoices based on standard sales lines</span></span>
<span data-ttu-id="1a0f5-121">Du kan bruge kørslen **Opret tilbagevendende salgsfakturaer** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgslinjerne.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-121">You can use the **Create Recurring Sales Invoices** batch job to create sales invoices according to standard sales lines that are assigned to the customers and with posting dates within the valid-from and valid-to dates that you specify on the standard sales lines.</span></span>

> [!NOTE]
> <span data-ttu-id="1a0f5-122">I vinduet **Tilbagevendende salgslinjer** kan du også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-122">In the **Recurring Sales Lines** window, you can also specify a direct-debit payment method and a direct-debit mandate.</span></span> <span data-ttu-id="1a0f5-123">Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfaktura**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-123">The sales invoices that are created with the **Create Recurring Sales Inv.** batch job will then include information required to collect payment for the sales invoices with SEPA direct debit.</span></span> <span data-ttu-id="1a0f5-124">Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span><span class="sxs-lookup"><span data-stu-id="1a0f5-124">For more information, see [Collecting Payments with SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).</span></span>

1. <span data-ttu-id="1a0f5-125">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-125">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Create Recurring Sales Invoices**, and then choose the related link.</span></span>
2. <span data-ttu-id="1a0f5-126">Udfyld felterne efter behov i vinduet **Opret tilbagevendende salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-126">In the **Create Recurring Sales Invoices** window, fill in the fields as necessary.</span></span>
3. <span data-ttu-id="1a0f5-127">I filterfeltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-127">In the **Code** filter field, enter the code for standard sales lines that are assigned to a customer that you want to create sales invoices for.</span></span>
4. <span data-ttu-id="1a0f5-128">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-128">Choose the **OK** button.</span></span>

<span data-ttu-id="1a0f5-129">Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.</span><span class="sxs-lookup"><span data-stu-id="1a0f5-129">Sales invoices are created for the customers with the specified standard customer sales code, and any specified direct-debit information, for posting on the specified date.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a0f5-130">Se også</span><span class="sxs-lookup"><span data-stu-id="1a0f5-130">See Also</span></span>  
[<span data-ttu-id="1a0f5-131">Salg</span><span class="sxs-lookup"><span data-stu-id="1a0f5-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="1a0f5-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1a0f5-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

