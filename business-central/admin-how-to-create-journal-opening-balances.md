---
title: Sådan oprettes kladden Primosaldi | Microsoft Docs
description: Business Central indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data med posteringer.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 07/14/2020
ms.author: sgroespe
ms.openlocfilehash: 5360b3a8a72387cda8d0e640562a118ca1f20ff4
ms.sourcegitcommit: 89d0ea903f61ab0628f99329c762d9f1619c49a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2020
ms.locfileid: "3577122"
---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="23da0-104">Oprette kladden Primosaldi</span><span class="sxs-lookup"><span data-stu-id="23da0-104">Create Journal Opening Balances</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="23da0-105">indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed.</span><span class="sxs-lookup"><span data-stu-id="23da0-105">includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="23da0-106">Du kan nemt overføre disse data til debitorkladden, kreditorkladden, varekladden og finanskladden.</span><span class="sxs-lookup"><span data-stu-id="23da0-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="23da0-107">Det første trin er at oprette en konfigurationspakke, der omfatter konfigurationstabellerne for disse kladder.</span><span class="sxs-lookup"><span data-stu-id="23da0-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="23da0-108">I følgende procedure antages det, at dette trin er udført.</span><span class="sxs-lookup"><span data-stu-id="23da0-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="23da0-109">Du kan finde flere oplysninger i [Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="23da0-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="23da0-110">Proceduren beskriver de efterfølgende trin, som omfatter anvendelse af den pakke, der leveres af en partner.</span><span class="sxs-lookup"><span data-stu-id="23da0-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="23da0-111">Før du starter, skal du kontrollere, at du du bruger rollecentersiden Administration, fordi den indeholder den korrekte kontekst til dit konfigurationsarbejde.</span><span class="sxs-lookup"><span data-stu-id="23da0-111">Before you start, make sure that you are using the Administration Role Center page because it provides the correct context for your configuration work.</span></span> <span data-ttu-id="23da0-112">Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="23da0-112">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="23da0-113">Udligne posterne i en kladde til en ny virksomhed</span><span class="sxs-lookup"><span data-stu-id="23da0-113">To apply the entries in a journal to a new company</span></span>

1. <span data-ttu-id="23da0-114">Konfigurer en ny virksomhed, og anvend en konfigurationspakke på den.</span><span class="sxs-lookup"><span data-stu-id="23da0-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="23da0-115">Du kan finde flere oplysninger i [Konfigurere en virksomhed med guiden RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="23da0-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="23da0-116">Den nye virksomhed indeholder ikke oplysninger om kladdeprimosaldi.</span><span class="sxs-lookup"><span data-stu-id="23da0-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="23da0-117">Åbn konfigurationsregnearket, og importér eksisterende data om debitorer, varer, kreditorer og regnskabet.</span><span class="sxs-lookup"><span data-stu-id="23da0-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="23da0-118">Du kan finde flere oplysninger i [Overflytte debitordata](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="23da0-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  

    <span data-ttu-id="23da0-119">Nu er stamdataene på plads.</span><span class="sxs-lookup"><span data-stu-id="23da0-119">Now you have master data in place.</span></span> <span data-ttu-id="23da0-120">Derefter skal du tilføje primosaldi.</span><span class="sxs-lookup"><span data-stu-id="23da0-120">Next, you add the opening balances.</span></span> <span data-ttu-id="23da0-121">Følgende fremgangsmåde beskriver, hvordan du opretter kladdelinjer til finanskonti, men gælder også for oprettelse af kladdelinjer til debitorer, kreditorer og varer.</span><span class="sxs-lookup"><span data-stu-id="23da0-121">The following steps describe how to create journal lines for G/L accounts, but the same apply to creating journal lines for customers, vendors, and items.</span></span>  
3. <span data-ttu-id="23da0-122">Vælg handlingen **Opret kladdelinjer for finanskonto**.</span><span class="sxs-lookup"><span data-stu-id="23da0-122">Choose the **Create G/L Acct. Journal Lines** action.</span></span>  
4. <span data-ttu-id="23da0-123">Udfyld oversigtspanelet **Indstillinger**, og angiv filtre efter behov.</span><span class="sxs-lookup"><span data-stu-id="23da0-123">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="23da0-124">Skriv f.eks. et navn i feltet **Kladdetype**.</span><span class="sxs-lookup"><span data-stu-id="23da0-124">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="23da0-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="23da0-125">Choose the **OK** button.</span></span> <span data-ttu-id="23da0-126">Posterne er nu i kladden, men beløbene er tomme.</span><span class="sxs-lookup"><span data-stu-id="23da0-126">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="23da0-127">Eksportér kladdetabellen til Excel, og angiv manuelt bogførings- og modkontooplysninger fra ældre data.</span><span class="sxs-lookup"><span data-stu-id="23da0-127">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="23da0-128">Importér og anvend tabeloplysningerne i den nye virksomhed.</span><span class="sxs-lookup"><span data-stu-id="23da0-128">Import and apply the table information into the new company.</span></span> <span data-ttu-id="23da0-129">Kladdelinjerne er klar til bogføring.</span><span class="sxs-lookup"><span data-stu-id="23da0-129">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="23da0-130">I konfigurationsregnearket skal du vælge kladdelinjetabellen og derefter vælge handlingen **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="23da0-130">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="23da0-131">Gennemgå oplysningerne, og vælg derefter handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="23da0-131">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="23da0-132">Gentag trinene for at importere og bogføre eventuelle andre primosaldi.</span><span class="sxs-lookup"><span data-stu-id="23da0-132">Repeat the steps to import and post any other opening balances.</span></span>  

> [!TIP]
> <span data-ttu-id="23da0-133">Du kan bruge de samme kørsler til at tilføje primosaldi, hver gang du registrerer en ny debitor eller kreditor, som du har handlet med, men som ikke er registreret i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="23da0-133">You can use the same batch jobs to add opening balances whenever you register a new customer or vendor that you have done business with before but not registered in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="23da0-134">Du skal blot søge efter den relevante opgave og derefter vælge det relevante link.</span><span class="sxs-lookup"><span data-stu-id="23da0-134">Just search for the relevant task, and then choose the relevant link.</span></span>

## <a name="see-also"></a><span data-ttu-id="23da0-135">Se også</span><span class="sxs-lookup"><span data-stu-id="23da0-135">See Also</span></span>

[<span data-ttu-id="23da0-136">Anvende konfigurationer på nye virksomheder</span><span class="sxs-lookup"><span data-stu-id="23da0-136">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="23da0-137">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="23da0-137">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="23da0-138">Opsætning</span><span class="sxs-lookup"><span data-stu-id="23da0-138">Administration</span></span>](admin-setup-and-administration.md)  
