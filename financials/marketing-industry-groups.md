---
title: Konfigurere brancher for kontaktvirksomheder | Microsoft Docs
description: Beskriver, hvordan du definerer en branche og knytter den til en kontaktvirksomhed, for eksempel detailbranchen eller automobilbranchen.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c7a8549a5c6528cafb5e2959a3391fb323fe92ca
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-industry-groups-for-contact-companies"></a><span data-ttu-id="7d1d5-103">Angive brancher for kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="7d1d5-103">Set Up Industry Groups for Contact Companies</span></span>
<span data-ttu-id="7d1d5-104">Du bruger brancher til at angive, hvilken branchetype dine kontakter tilhører, f.eks. detailbranchen eller automobilbranchen.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-104">You use industry groups to indicate the type of industry to which your contacts belong, for example, the retail industry or the automobile industry.</span></span>

<span data-ttu-id="7d1d5-105">Brug af brancher i kontakter er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-105">Using industry groups on contacts is a two-step process.</span></span> <span data-ttu-id="7d1d5-106">Først skal du definere branchekoden.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-106">First, you define the industry group code.</span></span> <span data-ttu-id="7d1d5-107">Du behøver kun at udføre dette trin én gang for hver branche.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-107">You only have to perform this step one time for each industry group.</span></span> <span data-ttu-id="7d1d5-108">Når du har en branchekode, kan du begynde at tildele koden til kontaktvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-108">Once you have an industry group code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7d1d5-109">Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-an-industry-group-code"></a><span data-ttu-id="7d1d5-110">Sådan defineres en branchekode</span><span class="sxs-lookup"><span data-stu-id="7d1d5-110">To define an industry group code</span></span>
<span data-ttu-id="7d1d5-111">Koden for branchen definerer type eller kategori for gruppen, f.eks REKLAME for reklame, eller PRESSE for tv og radio.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-111">The industry group code defines the type or category of the group, such as ADVERT for advertising, or PRESS, for TV and radio.</span></span> <span data-ttu-id="7d1d5-112">Du kan have flere branchekoder.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-112">You can have several industry group codes.</span></span> <span data-ttu-id="7d1d5-113">Du definerer brancherne fra vinduet **Brancher**.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-113">To define the industry groups, you use the **Industry Groups** window.</span></span>

1. <span data-ttu-id="7d1d5-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Brancher**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Industry Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d1d5-115">Vælg handlingen **Ny**, og indtast en kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="7d1d5-116">Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignIndustryGroupContact"></a> <span data-ttu-id="7d1d5-117">Sådan tildeles brancher til en kontakt</span><span class="sxs-lookup"><span data-stu-id="7d1d5-117">To assign industry groups to a contact</span></span>
<span data-ttu-id="7d1d5-118">Du kan ikke tildele brancher til en kontaktperson – kun til virksomheder.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-118">You cannot assign industry groups to a contact person - only companies.</span></span>

1. <span data-ttu-id="7d1d5-119">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-119">Open the contact.</span></span>
2. <span data-ttu-id="7d1d5-120">Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Brancher**.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-120">Choose the **Company** action, and then the **Industry Groups** action.</span></span> <span data-ttu-id="7d1d5-121">Vinduet **Branchegrupper** åbnes.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-121">The **Contact Industry Groups** window opens.</span></span>
3. <span data-ttu-id="7d1d5-122">I feltet **Branchekode** skal du vælge den branche, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-122">In the **Industry Groups Code** field, select the industry groups you want to assign.</span></span>

<span data-ttu-id="7d1d5-123">Gentag disse trin for hver branche, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-123">Repeat these steps to assign as many industry groups as you want.</span></span> <span data-ttu-id="7d1d5-124">Du kan også tildele brancher fra kontaktoversigten ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-124">You can also assign industry groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="7d1d5-125">Det antal brancher, du har tildelt til kontakten, vises i feltet **Antal brancher** i sektionen **Segmentering** i vinduet **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-125">The number of industry groups that you have assigned to the contact is displayed in the **No. of Industry Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="7d1d5-126">Når du har tildelt brancher til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper.</span><span class="sxs-lookup"><span data-stu-id="7d1d5-126">After you have assigned industry groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="7d1d5-127">Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="7d1d5-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7d1d5-128">Se også</span><span class="sxs-lookup"><span data-stu-id="7d1d5-128">See Also</span></span>
[<span data-ttu-id="7d1d5-129">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="7d1d5-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="7d1d5-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d1d5-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

