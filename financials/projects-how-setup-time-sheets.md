---
title: Konfigurere timesedler og godkendelse af dem | Microsoft Docs
description: "Du kan konfigurere timesedler for at registrere den tid, der bruges på sager og på anvendelse af ressourcer, der hjælper dig med projektstyring, personale og kapacitet"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff, resource
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 3e85168709eb8e96b2ee2aea516189c2cf88d426
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017


---
# <a name="how-to-set-up-time-sheets"></a><span data-ttu-id="eafb4-103">Sådan gør du: Konfigurere timesedler</span><span class="sxs-lookup"><span data-stu-id="eafb4-103">How to: Set Up Time Sheets</span></span>
<span data-ttu-id="eafb4-104">Timesedler i [!INCLUDE[d365fin](includes/d365fin_md.md)] håndterer tidsregistrering i ugentlige intervaller på syv dage.</span><span class="sxs-lookup"><span data-stu-id="eafb4-104">Time sheets in [!INCLUDE[d365fin](includes/d365fin_md.md)] handle time registration in weekly increments of seven days.</span></span> <span data-ttu-id="eafb4-105">Du kan bruge til at registrere den tid, der er brugt på sager, og du kan bruge dem til at registrere simpel ressourcetidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="eafb4-105">You use them to track the time used on jobs, and you can use them to record simple resource time registration.</span></span> <span data-ttu-id="eafb4-106">Før du kan bruge timesedler, skal du angive, hvordan du vil have dem oprettet og konfigureret.</span><span class="sxs-lookup"><span data-stu-id="eafb4-106">Before you can use time sheets, you must specify how you want them to be set up and configured.</span></span>

<span data-ttu-id="eafb4-107">Når du har konfigureret, hvordan organisationen skal bruge timesedler, kan du angive, om og hvordan timesedler godkendes.</span><span class="sxs-lookup"><span data-stu-id="eafb4-107">After you have set up how your organization will use time sheets, you can specify if and how time sheets are approved.</span></span> <span data-ttu-id="eafb4-108">Afhængigt af organisationens behov kan du angive:</span><span class="sxs-lookup"><span data-stu-id="eafb4-108">Depending on the needs of your organization, you can designate:</span></span>

* <span data-ttu-id="eafb4-109">En eller flere brugere som timeseddeladministrator og godkendere for alle timesedler.</span><span class="sxs-lookup"><span data-stu-id="eafb4-109">One or more users as the time sheet administrator and approver for all time sheets.</span></span>
* <span data-ttu-id="eafb4-110">En timeseddelgodkender for hver ressource.</span><span class="sxs-lookup"><span data-stu-id="eafb4-110">A time sheet approver for each resource.</span></span>

<span data-ttu-id="eafb4-111">Når du har oprettet timesedler, kan du oprette timesedler for ressourcer, tildele dem til planlægningslinjer og bogføre timeseddellinjer.</span><span class="sxs-lookup"><span data-stu-id="eafb4-111">When you have set up time sheets, you can create time sheets for resources, assign them to job planning lines, and post time sheet lines.</span></span> <span data-ttu-id="eafb4-112">Du kan finde flere oplysninger i [Fremgangsmåde: Bruge timesedler](projects-how-use-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="eafb4-112">For more information, see [How to: Use Time Sheets](projects-how-use-time-sheets.md).</span></span>

## <a name="to-set-up-general-information-for-time-sheets"></a><span data-ttu-id="eafb4-113">Sådan angives generelle oplysninger for timesedler</span><span class="sxs-lookup"><span data-stu-id="eafb4-113">To set up general information for time sheets</span></span>
1. <span data-ttu-id="eafb4-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="eafb4-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eafb4-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="eafb4-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="eafb4-116">For feltet **Timeseddel efter sagsgodkendelse** skal du vælge en af følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="eafb4-116">For the **Time Sheet by Job Approval** field, select one of the following options.</span></span>

| <span data-ttu-id="eafb4-117">Indstilling</span><span class="sxs-lookup"><span data-stu-id="eafb4-117">Option</span></span> | <span data-ttu-id="eafb4-118">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="eafb4-118">Description</span></span> |
| --- | --- |
| <span data-ttu-id="eafb4-119">**Aldrig**</span><span class="sxs-lookup"><span data-stu-id="eafb4-119">**Never**</span></span> |<span data-ttu-id="eafb4-120">Brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet godkender timesedlen.</span><span class="sxs-lookup"><span data-stu-id="eafb4-120">The user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |
| <span data-ttu-id="eafb4-121">**Altid**</span><span class="sxs-lookup"><span data-stu-id="eafb4-121">**Always**</span></span> |<span data-ttu-id="eafb4-122">Brugeren i feltet **Ansvarlig person** på sagskortet godkender timesedlen.</span><span class="sxs-lookup"><span data-stu-id="eafb4-122">The user in the **Person Responsible** field on the job card approves the time sheet.</span></span> |
| <span data-ttu-id="eafb4-123">**Kun maskine**</span><span class="sxs-lookup"><span data-stu-id="eafb4-123">**Machine Only**</span></span> |<span data-ttu-id="eafb4-124">Hvis maskintimesedlen er knyttet til en sag, godkendes timesedlen af brugeren i feltet **Ansvarlig person** på sagskortet.</span><span class="sxs-lookup"><span data-stu-id="eafb4-124">If the machine time sheet is linked with a job, then the user in the **Person Responsible** field on the job card approves the time sheet.</span></span> <span data-ttu-id="eafb4-125">Hvis maskintimesedlen er knyttet til en ressource, godkendes timesedlen af brugeren i feltet **Bruger-id for timeseddelgodkender** på ressourcekortet.</span><span class="sxs-lookup"><span data-stu-id="eafb4-125">If the machine time sheet is linked with a resource, then the user in the **Time Sheet Approver User ID** field on the resource card approves the time sheet.</span></span> |

## <a name="to-assign-a-time-sheet-administrator"></a><span data-ttu-id="eafb4-126">Sådan tildeles en timeseddeladministrator</span><span class="sxs-lookup"><span data-stu-id="eafb4-126">To assign a time sheet administrator</span></span>
1. <span data-ttu-id="eafb4-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourceopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="eafb4-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **User Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="eafb4-128">Tilføj en ny bruger, hvis brugerlisten ikke omfatter den person, som du ønsker, skal være timeseddeladministrator.</span><span class="sxs-lookup"><span data-stu-id="eafb4-128">Add a new user if the user list does not include the person who you want to be the time sheet administrator.</span></span> <span data-ttu-id="eafb4-129">Du kan finde flere oplysninger i [Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="eafb4-129">For more information, see [How to: Manage Users and Permissions](ui-how-users-permissions.md).</span></span>
3. <span data-ttu-id="eafb4-130">Vælg en bruger, der skal være timeseddeladministrator, og vælg derefter afkrydsningsfeltet **Timeseddeladm.**</span><span class="sxs-lookup"><span data-stu-id="eafb4-130">Select a user to be a time sheet administrator, and then select the **Time Sheet Admin.**</span></span> <span data-ttu-id="eafb4-131">.</span><span class="sxs-lookup"><span data-stu-id="eafb4-131">check box.</span></span>  

> [!TIP]  
>   <span data-ttu-id="eafb4-132">Det anbefales, at du kun udpeger én bruger til timeseddeladministrator for en virksomhed.</span><span class="sxs-lookup"><span data-stu-id="eafb4-132">It is recommended that you designate only one user to be the time sheet administrator for a company.</span></span> <span data-ttu-id="eafb4-133">I følgende procedure opretter du en timeseddelejer og -godkender, hvor timeseddelgodkenderen tildeles for hver ressource.</span><span class="sxs-lookup"><span data-stu-id="eafb4-133">In the following procedure, you set up a time sheet owner and approver where the time sheet approver is assigned for each resource.</span></span>  

## <a name="to-assign-a-time-sheets-owner-and-approver"></a><span data-ttu-id="eafb4-134">Sådan tildeles en timeseddelejer og -godkender</span><span class="sxs-lookup"><span data-stu-id="eafb4-134">To assign a time sheets owner and approver</span></span>
1. <span data-ttu-id="eafb4-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="eafb4-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="eafb4-136">Vælg den ressource, du vil konfigurere til at kunne bruge timesedler, og vælg derefter afkrydsningsfeltet **Brug timeseddel**.</span><span class="sxs-lookup"><span data-stu-id="eafb4-136">Select the resource for which you want to set up the ability to use time sheets, and then select the **Use Time Sheet** check box.</span></span>  
3. <span data-ttu-id="eafb4-137">I feltet **Bruger-id for timeseddelejer** skal du angive id'et for ejeren af timesedlen.</span><span class="sxs-lookup"><span data-stu-id="eafb4-137">In the **Time Sheet Owner User ID** field, enter the ID of the owner of the time sheet.</span></span> <span data-ttu-id="eafb4-138">Ejeren kan angive tidsforbrug på en timeseddel og sende den til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="eafb4-138">The owner can enter time usage on a time sheet and submit it for approval.</span></span> <span data-ttu-id="eafb4-139">Når ressourcen er en person, er denne person generelt også ejeren.</span><span class="sxs-lookup"><span data-stu-id="eafb4-139">In general, when the resource is a person, that person is also the owner.</span></span>  
4. <span data-ttu-id="eafb4-140">I feltet **Bruger-id for timeseddelgodkender** skal du angive id'et for godkenderen af timesedlen.</span><span class="sxs-lookup"><span data-stu-id="eafb4-140">In the **Time Sheet Approver User ID** field, enter the ID of the approver of the time sheet.</span></span> <span data-ttu-id="eafb4-141">Godkenderen kan godkende, afvise eller åbne en timeseddel igen.</span><span class="sxs-lookup"><span data-stu-id="eafb4-141">The approver can approve, reject, or reopen a time sheet.</span></span>  

> [!NOTE]  
>   <span data-ttu-id="eafb4-142">Du kan ikke ændre id'et på godkenderen af timesedler, hvis der er timesedler, der endnu ikke er behandlet, og som har statussen **Sendt** eller **Åben**.</span><span class="sxs-lookup"><span data-stu-id="eafb4-142">You cannot change the ID of the time sheet approver if there are time sheets that have not yet been processed and have the status of **Submitted** or **Open**.</span></span>

## <a name="see-also"></a><span data-ttu-id="eafb4-143">Se også</span><span class="sxs-lookup"><span data-stu-id="eafb4-143">See Also</span></span>
[<span data-ttu-id="eafb4-144">Konfigurere projektstyring</span><span class="sxs-lookup"><span data-stu-id="eafb4-144">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="eafb4-145">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="eafb4-145">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="eafb4-146">Finans</span><span class="sxs-lookup"><span data-stu-id="eafb4-146">Finance</span></span>](finance.md)  
<span data-ttu-id="eafb4-147">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="eafb4-147">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="eafb4-148">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="eafb4-148">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="eafb4-149">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="eafb4-149">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

