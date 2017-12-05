---
title: "Bruge udvidelsen C5-dataoverførsel | Microsoft Docs"
description: "Du kan bruge denne udvidelse til at overføre debitorer, kreditorer, varer og omkostninger på finanskonti fra Microsoft Dynamics C5 2012 til Financials."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 09/26/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 2d7d533662936116ffa40ded07b68e845fed810b
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="the-c5-data-migration-extension-for-dynamics-365-for-finance-and-operations-business-edition"></a><span data-ttu-id="edcd3-103">Udvidelsen C5-dataoverførsel til Dynamics 365 for Finance and Operations, Business Edition</span><span class="sxs-lookup"><span data-stu-id="edcd3-103">The C5 Data Migration Extension for Dynamics 365 for Finance and Operations, Business Edition</span></span>
<span data-ttu-id="edcd3-104">Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="edcd3-104">This extension makes it easy to migrate customers, vendors, items, and your general ledger accounts from Microsoft Dynamcis C5 2012 to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
  
> [!Note] 
> <span data-ttu-id="edcd3-105">Virksomheden i [!INCLUDE[d365fin](includes/d365fin_md.md)] må ikke indeholde data.</span><span class="sxs-lookup"><span data-stu-id="edcd3-105">The company in [!INCLUDE[d365fin](includes/d365fin_md.md)] must not contain any data.</span></span> <span data-ttu-id="edcd3-106">Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="edcd3-106">Additionally, after you start a migration, do not create customers, vendors, items, or accounts until the migration finishes.</span></span>

## <a name="to-migrate-data"></a><span data-ttu-id="edcd3-107">Sådan overføres data</span><span class="sxs-lookup"><span data-stu-id="edcd3-107">To migrate data</span></span>
<span data-ttu-id="edcd3-108">Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="edcd3-108">There are just a few steps to export data from C5, and import it in [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  
  
1. <span data-ttu-id="edcd3-109">I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="edcd3-109">In C5, use the **Export Database** feature to export the data.</span></span> <span data-ttu-id="edcd3-110">Send derefter eksportmappen til en komprimeret (zippet) mappe.</span><span class="sxs-lookup"><span data-stu-id="edcd3-110">Then send the export folder to a compressed (zipped) folder.</span></span>  
2. <span data-ttu-id="edcd3-111">I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Dataoverførsel** og derefter vælg **Dataoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="edcd3-111">In [!INCLUDE[d365fin](includes/d365fin_md.md)], choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Migration**, and then choose **Data Migration**.</span></span>  
3. <span data-ttu-id="edcd3-112">Udfør trinnene i guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="edcd3-112">Complete the steps in the assisted setup guide.</span></span> <span data-ttu-id="edcd3-113">Sørg for at vælge **Indlæs fra Microsoft Dynamcis C5 2012** som datakilde.</span><span class="sxs-lookup"><span data-stu-id="edcd3-113">Make sure to choose **Import from Microsoft Dynamcis C5 2012** as the data source.</span></span>  

> [!Note] 
> <span data-ttu-id="edcd3-114">Virksomheder tilføje ofte felter for at tilpasse C5 til deres specifikke branche.</span><span class="sxs-lookup"><span data-stu-id="edcd3-114">Companies often add fields to customize C5 for their specific line of business.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="edcd3-115"> overflytter ikke data fra brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="edcd3-115"> does not migrate data from custom fields.</span></span> <span data-ttu-id="edcd3-116">Overførslen mislykkes også, hvis du har mere end 10 brugerdefinerede felter.</span><span class="sxs-lookup"><span data-stu-id="edcd3-116">Also, migration will fail if you have more than 10 custom fields.</span></span> 

## <a name="viewing-the-status-of-the-migration"></a><span data-ttu-id="edcd3-117">Få vist status for overførslen</span><span class="sxs-lookup"><span data-stu-id="edcd3-117">Viewing the Status of the Migration</span></span>
<span data-ttu-id="edcd3-118">Brug siden **Dataoverførselsoversigt** til at overvåge status for overførslen.</span><span class="sxs-lookup"><span data-stu-id="edcd3-118">Use the **Data Migration Overview** page to monitor the success of the migration.</span></span> <span data-ttu-id="edcd3-119">Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket.</span><span class="sxs-lookup"><span data-stu-id="edcd3-119">The page shows information such as the number of entities that the migration will include, the status of the migration, and the number of items that have been migrated and whether they were successfull.</span></span> <span data-ttu-id="edcd3-120">Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne.</span><span class="sxs-lookup"><span data-stu-id="edcd3-120">It also shows the number of errors, lets you investigate what went wrong and, when possible, makes it easy to go to the entity to fix the issues.</span></span> <span data-ttu-id="edcd3-121">Du kan finde flere oplysninger i næste afsnit i dette emne.</span><span class="sxs-lookup"><span data-stu-id="edcd3-121">For more information, see the next section in this topic.</span></span> 

> [!Note] 
> <span data-ttu-id="edcd3-122">Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.</span><span class="sxs-lookup"><span data-stu-id="edcd3-122">While you are waiting for the results of the migration, you must refresh the page to display the results.</span></span>

## <a name="correcting-errors"></a><span data-ttu-id="edcd3-123">Rette fejl</span><span class="sxs-lookup"><span data-stu-id="edcd3-123">Correcting Errors</span></span>
<span data-ttu-id="edcd3-124">Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange.</span><span class="sxs-lookup"><span data-stu-id="edcd3-124">If something goes wrong and an error occurs, the **Status** field will show **Completed with Errors**, and the **Error Count** field will show how many.</span></span> <span data-ttu-id="edcd3-125">For at få vist en liste over fejlene, kan du åbne siden **Dataoverførselsfejl** side ved at vælge:</span><span class="sxs-lookup"><span data-stu-id="edcd3-125">To view a list of the errors, you can open the **Data Migration Errors** page by choosing:</span></span>

* <span data-ttu-id="edcd3-126">Nummeret i feltet **Antal fejl** for enheden.</span><span class="sxs-lookup"><span data-stu-id="edcd3-126">The number in the **Error Count** field for the entity.</span></span> 
* <span data-ttu-id="edcd3-127">Enheden og derefter handlingen **Vis fejl**.</span><span class="sxs-lookup"><span data-stu-id="edcd3-127">The entity, and then the **Show Errors** action.</span></span> 

<span data-ttu-id="edcd3-128">På siden **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse, og derefter vælge **Rediger post** for at åbne en side, der viser de overførte data for objektet.</span><span class="sxs-lookup"><span data-stu-id="edcd3-128">On the **Data Migration Errors** page, to fix an error you can choose an error message, then choose **Edit Record** to open a page that shows the migrated data for the entity.</span></span> <span data-ttu-id="edcd3-129">Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.</span><span class="sxs-lookup"><span data-stu-id="edcd3-129">After you fix one or more errors, you can choose **Migrate** to migrate only the entities you fixed, without having to completely restart the migration.</span></span>  

> [!Tip]
> <span data-ttu-id="edcd3-130">Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres.</span><span class="sxs-lookup"><span data-stu-id="edcd3-130">If you have fixed more than one error, you can use the **Select More** feature to select multiple lines to migrate.</span></span> <span data-ttu-id="edcd3-131">Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.</span><span class="sxs-lookup"><span data-stu-id="edcd3-131">Alternatively, if there are errors that are not important to fix, you can choose them and then choose **Skip Selections**.</span></span>

> [!Note]
> <span data-ttu-id="edcd3-132">Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den.</span><span class="sxs-lookup"><span data-stu-id="edcd3-132">If you have items that are included in a BOM, you might need to migrate more than once if the original item is not created before the variants that reference it.</span></span> <span data-ttu-id="edcd3-133">Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="edcd3-133">If an item variant is created first, the reference to the original item can cause an error message.</span></span>  

## <a name="verifying-data-after-migrating"></a><span data-ttu-id="edcd3-134">Kontrol af data efter overførsel</span><span class="sxs-lookup"><span data-stu-id="edcd3-134">Verifying Data After Migrating</span></span> 
<span data-ttu-id="edcd3-135">Hvis du vil kontrollere, at dine data overføres korrekt, kan du se de følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="edcd3-135">If you want to verify that your data migrated correctly, you can look at the following pages in C5 and [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

|<span data-ttu-id="edcd3-136">Microsoft Dynamics C5 2012</span><span class="sxs-lookup"><span data-stu-id="edcd3-136">Microsoft Dynamcis C5 2012</span></span> | [!INCLUDE[d365fin](includes/d365fin_md.md)]|
|-----|-----|
|<span data-ttu-id="edcd3-137">Debitorposter</span><span class="sxs-lookup"><span data-stu-id="edcd3-137">Customer Entries</span></span>| <span data-ttu-id="edcd3-138">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="edcd3-138">General Journals</span></span>|
|<span data-ttu-id="edcd3-139">Kreditorposter</span><span class="sxs-lookup"><span data-stu-id="edcd3-139">Vendor Entries</span></span>| <span data-ttu-id="edcd3-140">Finanskladder</span><span class="sxs-lookup"><span data-stu-id="edcd3-140">General Journals</span></span>|
|<span data-ttu-id="edcd3-141">Vareposter</span><span class="sxs-lookup"><span data-stu-id="edcd3-141">Item Entries</span></span>| <span data-ttu-id="edcd3-142">Varekladder</span><span class="sxs-lookup"><span data-stu-id="edcd3-142">Item Journals</span></span>|

<span data-ttu-id="edcd3-143">I [!INCLUDE[d365fin](includes/d365fin_md.md)] hedder batchen for de overførte data **C5MIGRATE**.</span><span class="sxs-lookup"><span data-stu-id="edcd3-143">In [!INCLUDE[d365fin](includes/d365fin_md.md)], the batch for the migrated data is named **C5MIGRATE**.</span></span> 

## <a name="stopping-data-migration"></a><span data-ttu-id="edcd3-144">Stoppe dataoverførslen</span><span class="sxs-lookup"><span data-stu-id="edcd3-144">Stopping Data Migration</span></span>
<span data-ttu-id="edcd3-145">Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**.</span><span class="sxs-lookup"><span data-stu-id="edcd3-145">You can stop migrating data by choosing **Stop All Migrations**.</span></span> <span data-ttu-id="edcd3-146">Hvis du gør det, stoppes alle ventende overførsler også.</span><span class="sxs-lookup"><span data-stu-id="edcd3-146">If you do, all pending migrations are also stopped.</span></span>

## <a name="see-also"></a><span data-ttu-id="edcd3-147">Se også</span><span class="sxs-lookup"><span data-stu-id="edcd3-147">See Also</span></span>
<span data-ttu-id="edcd3-148">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="edcd3-148">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="edcd3-149">[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="edcd3-149">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

