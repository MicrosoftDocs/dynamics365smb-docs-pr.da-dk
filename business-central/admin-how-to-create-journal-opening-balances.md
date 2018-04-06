---
title: "Sådan oprettes kladden Primosaldi | Microsoft Docs"
description: "Business Central indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data med posteringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fc8e8f34220643b7cd3fd357aea3807641cee911
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a><span data-ttu-id="89424-104">Oprette kladden Primosaldi</span><span class="sxs-lookup"><span data-stu-id="89424-104">Create Journal Opening Balances</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="89424-105"> indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed.</span><span class="sxs-lookup"><span data-stu-id="89424-105"> includes several batch jobs that are provided to help in the transfer of legacy account balances to a newly configured company.</span></span> <span data-ttu-id="89424-106">Du kan nemt overføre disse data til debitorkladden, kreditorkladden, varekladden og finanskladden.</span><span class="sxs-lookup"><span data-stu-id="89424-106">You can easily transfer this data with the customer journal, the vendor journal, the item journal, or the G/L journal.</span></span>

<span data-ttu-id="89424-107">Det første trin er at oprette en konfigurationspakke, der omfatter konfigurationstabellerne for disse kladder.</span><span class="sxs-lookup"><span data-stu-id="89424-107">The first step is to create a configuration package that includes the setup tables for those journals.</span></span> <span data-ttu-id="89424-108">I følgende procedure antages det, at dette trin er udført.</span><span class="sxs-lookup"><span data-stu-id="89424-108">The following procedure assumes that this step is completed.</span></span> <span data-ttu-id="89424-109">Du kan finde flere oplysninger i [Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="89424-109">For more information, see [Set Up Company Configuration](admin-set-up-company-configuration.md).</span></span> <span data-ttu-id="89424-110">Proceduren beskriver de efterfølgende trin, som omfatter anvendelse af den pakke, der leveres af en partner.</span><span class="sxs-lookup"><span data-stu-id="89424-110">This procedure describes the subsequent steps, which include applying the package that is provided by a partner.</span></span>  

<span data-ttu-id="89424-111">Før du starter, skal du kontrollere, at du er på rollecentersiden RapidStart Services-implementering, som indeholder den korrekte kontekst til dit konfigurationsarbejde.</span><span class="sxs-lookup"><span data-stu-id="89424-111">Before you start, make sure that you are on the RapidStart Services Implementer Role Center page as it provides the correct context for your configuration work.</span></span> <span data-ttu-id="89424-112">Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="89424-112">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a><span data-ttu-id="89424-113">Udligne posterne i en kladde til en ny virksomhed</span><span class="sxs-lookup"><span data-stu-id="89424-113">To apply the entries in a journal to a new company</span></span>  
1. <span data-ttu-id="89424-114">Konfigurer en ny virksomhed, og anvend en konfigurationspakke på den.</span><span class="sxs-lookup"><span data-stu-id="89424-114">Configure a new company and apply a configuration package to it.</span></span> <span data-ttu-id="89424-115">Du kan finde flere oplysninger i [Konfigurere en virksomhed med guiden RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="89424-115">For more information, see [Configure a Company with the RapidStart Wizard](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).</span></span>  

    <span data-ttu-id="89424-116">Den nye virksomhed indeholder ikke oplysninger om kladdeprimosaldi.</span><span class="sxs-lookup"><span data-stu-id="89424-116">The new company does not contain information about journal opening balances.</span></span>  

2. <span data-ttu-id="89424-117">Åbn konfigurationsregnearket, og importér eksisterende data om debitorer, varer, kreditorer og regnskabet.</span><span class="sxs-lookup"><span data-stu-id="89424-117">Open the configuration worksheet and import existing data about customers, items, vendors, and the general ledger.</span></span> <span data-ttu-id="89424-118">Du kan finde flere oplysninger i [Overflytte debitordata](admin-migrate-customer-data.md).</span><span class="sxs-lookup"><span data-stu-id="89424-118">For more information, see [Migrate Customer Data](admin-migrate-customer-data.md).</span></span>  
3. <span data-ttu-id="89424-119">Vælg f.eks. handlingen **Opret sagskladdelinjer**.</span><span class="sxs-lookup"><span data-stu-id="89424-119">Choose, for example, the **Create G/L Journal Lines** action.</span></span>  
4. <span data-ttu-id="89424-120">Udfyld oversigtspanelet **Indstillinger**, og angiv filtre efter behov.</span><span class="sxs-lookup"><span data-stu-id="89424-120">Fill in the **Options** FastTab as appropriate, and set filters as needed.</span></span> <span data-ttu-id="89424-121">Skriv f.eks. et navn i feltet **Kladdetype**.</span><span class="sxs-lookup"><span data-stu-id="89424-121">For example, in the **Journal Template** field, enter a name.</span></span>  
5. <span data-ttu-id="89424-122">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="89424-122">Choose the **OK** button.</span></span> <span data-ttu-id="89424-123">Posterne er nu i kladden, men beløbene er tomme.</span><span class="sxs-lookup"><span data-stu-id="89424-123">The records are now in the journal, but the amounts are empty.</span></span>  
6. <span data-ttu-id="89424-124">Eksportér kladdetabellen til Excel, og angiv manuelt bogførings- og modkontooplysninger fra ældre data.</span><span class="sxs-lookup"><span data-stu-id="89424-124">Export the journal table to Excel and manually enter the posting and balancing account information from the legacy data.</span></span>
7. <span data-ttu-id="89424-125">Importér og anvend tabeloplysningerne i den nye virksomhed.</span><span class="sxs-lookup"><span data-stu-id="89424-125">Import and apply the table information into the new company.</span></span> <span data-ttu-id="89424-126">Kladdelinjerne er klar til bogføring.</span><span class="sxs-lookup"><span data-stu-id="89424-126">The journal lines are ready for posting.</span></span>  
8. <span data-ttu-id="89424-127">I konfigurationsregnearket skal du vælge kladdelinjetabellen og derefter vælge handlingen **Databasedata**.</span><span class="sxs-lookup"><span data-stu-id="89424-127">In the configuration worksheet, select the journal line table, and then choose the **Database Data** action.</span></span>  
9. <span data-ttu-id="89424-128">Gennemgå oplysningerne, og vælg derefter handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="89424-128">Review the information, and then choose the **Post** action.</span></span>  
10. <span data-ttu-id="89424-129">Gentag trinene for at importere og bogføre eventuelle andre primosaldi.</span><span class="sxs-lookup"><span data-stu-id="89424-129">Repeat the steps to import and post any other opening balances.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89424-130">Se også</span><span class="sxs-lookup"><span data-stu-id="89424-130">See Also</span></span>  
[<span data-ttu-id="89424-131">Anvende konfigurationer på nye virksomheder</span><span class="sxs-lookup"><span data-stu-id="89424-131">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="89424-132">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="89424-132">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="89424-133">Opsætning</span><span class="sxs-lookup"><span data-stu-id="89424-133">Administration</span></span>](admin-setup-and-administration.md)

