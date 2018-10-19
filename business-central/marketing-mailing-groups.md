---
title: "Opsætning af mailgrupper for kontakter | Microsoft Docs"
description: "Du kan bruge mailgrupper til at identificere grupper af kontakter, som skal modtage de samme oplysninger, f.eks. til en marketingkampagne eller et fremstød."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: a7b9c39b1f213bf2b09ee24e3e6172df027e042c
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="set-up-mailing-groups-for-contacts"></a><span data-ttu-id="e6efe-103">Oprette mailgrupper til kontakter</span><span class="sxs-lookup"><span data-stu-id="e6efe-103">Set Up Mailing Groups for Contacts</span></span>
<span data-ttu-id="e6efe-104">Du kan bruge mailgrupper til at angive grupper af kontakter, som skal modtage de samme oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e6efe-104">You can use mailing groups to identify groups of contacts that you want to receive the same information.</span></span> <span data-ttu-id="e6efe-105">F.eks. kan du oprette en mailgruppe til de kontakter, du vil sende en meddelelse til om at skifte kontor, og en anden gruppe om at sende gaver til andre kontakter.</span><span class="sxs-lookup"><span data-stu-id="e6efe-105">For example, you can set up a mailing group for the contacts that you want to send a notification of an office move, or another group for sending holiday gifts.</span></span>

<span data-ttu-id="e6efe-106">Brug af mailgrupper til kontakter er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="e6efe-106">Using mailing groups on contacts is a two-step process.</span></span> <span data-ttu-id="e6efe-107">Først skal du definere mailgruppekoden.</span><span class="sxs-lookup"><span data-stu-id="e6efe-107">First, you define the mailing group code.</span></span> <span data-ttu-id="e6efe-108">Du behøver kun at udføre dette trin én gang for hver mailgruppe.</span><span class="sxs-lookup"><span data-stu-id="e6efe-108">You only have to perform this step one time for each mailing group.</span></span> <span data-ttu-id="e6efe-109">Når du har en mailgruppekode, kan du begynde at tildele koden til kontaktvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="e6efe-109">Once you have a mailing group code, you can start to assign the code to contact companies.</span></span>

## <a name="to-define-mailing-group-codes"></a><span data-ttu-id="e6efe-110">Sådan defineres mailgruppekoder</span><span class="sxs-lookup"><span data-stu-id="e6efe-110">To define mailing group codes</span></span>
<span data-ttu-id="e6efe-111">Feltet Mailgruppekode definerer type eller kategori af gruppen, f.eks SKIFT i forbindelse med skift af kontor eller GAVE i forbindelse med barsel.</span><span class="sxs-lookup"><span data-stu-id="e6efe-111">The mailing group code defines the type or category of the group, such as MOVE for office move, or GIFT for holiday gift.</span></span> <span data-ttu-id="e6efe-112">Du kan have flere branchekoder.</span><span class="sxs-lookup"><span data-stu-id="e6efe-112">You can have several industry group codes.</span></span> <span data-ttu-id="e6efe-113">Du definerer brancherne fra vinduet **Mailgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e6efe-113">To define the industry groups, you use the **Mailing Groups** window.</span></span>

1. <span data-ttu-id="e6efe-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Mailgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="e6efe-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Mailing Groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="e6efe-115">Vælg handlingen **Ny**, og indtast en kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e6efe-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="e6efe-116">Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.</span><span class="sxs-lookup"><span data-stu-id="e6efe-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignMailGroupContact"></a> <span data-ttu-id="e6efe-117">Sådan tildeles mailgrupper til en kontakt</span><span class="sxs-lookup"><span data-stu-id="e6efe-117">To assign mailing groups to a contact</span></span>
1. <span data-ttu-id="e6efe-118">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="e6efe-118">Open the contact.</span></span>
2. <span data-ttu-id="e6efe-119">Vælg handlingen **Mailgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e6efe-119">Choose the **Mailing Groups** action.</span></span> <span data-ttu-id="e6efe-120">Vinduet **Mailgrupper for kontakt** åbnes.</span><span class="sxs-lookup"><span data-stu-id="e6efe-120">The **Contact Mailing Groups** window opens.</span></span>
3. <span data-ttu-id="e6efe-121">I feltet **Mailgruppekode** skal du vælge den mailgruppe, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="e6efe-121">In the **Mailing Groups Code** field, select the mailing group that you want to assign.</span></span>

<span data-ttu-id="e6efe-122">Gentag disse trin for hver mailgruppe, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="e6efe-122">Repeat these steps to assign as many mailing groups as you want.</span></span> <span data-ttu-id="e6efe-123">Du kan også tildele mailgrupper fra kontaktoversigten ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="e6efe-123">You can also assign mailing groups from the contact list by following the same procedure.</span></span>

<span data-ttu-id="e6efe-124">Det antal mailgrupper, du har tildelt kontakten, vises i feltet **Antal mailgrupper** i sektionen **Segmentering** i vinduet **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e6efe-124">The number of mailing groups you have assigned to the contact is displayed in the **No. of Mailing Groups** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="e6efe-125">Når du har tildelt mailgrupper til kontakter, kan du bruge oplysningerne til at udvælge kontakter til målgrupper.</span><span class="sxs-lookup"><span data-stu-id="e6efe-125">After you have assigned mailing groups to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="e6efe-126">Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="e6efe-126">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e6efe-127">Se også</span><span class="sxs-lookup"><span data-stu-id="e6efe-127">See Also</span></span>
[<span data-ttu-id="e6efe-128">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="e6efe-128">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="e6efe-129">Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e6efe-129">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
[<span data-ttu-id="e6efe-130">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="e6efe-130">Working with Business Central</span></span>](ui-work-product.md)

