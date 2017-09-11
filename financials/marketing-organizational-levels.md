---
title: Konfigurere kompetenceniveauer for kontaktpersoner | Microsoft Docs
description: Du kan definere et kompetenceniveau og tildele det til din kontakt for at angive vedkommendes stilling i hans eller hendes virksomhed, f.eks. ledelse.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, client, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 927c27998bfaeb8d7247158cde1d1eb958a6911f
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-organizational-levels-for-contact-persons"></a><span data-ttu-id="6e475-103">Fremgangsmåde: Oprette kompetenceniveauer for kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="6e475-103">How to: Set Up Organizational Levels for Contact Persons</span></span>
<span data-ttu-id="6e475-104">Du kan bruge kompetenceniveauer til kontakter, så de selv kan angive den stilling, som de har i virksomheden, f.eks. ledelse.</span><span class="sxs-lookup"><span data-stu-id="6e475-104">You can use organizational levels on your contacts to specify which position they have in the company, for example, top management.</span></span> <span data-ttu-id="6e475-105">Du kan bruge disse oplysninger, når du angiver oplysninger om dine kontakter.</span><span class="sxs-lookup"><span data-stu-id="6e475-105">You can use this information when entering information about your contacts.</span></span>

<span data-ttu-id="6e475-106">Brug af kompetenceniveauer til kontakter er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="6e475-106">Using organizational levels on contacts is a two-step process.</span></span> <span data-ttu-id="6e475-107">Først skal du definere koden for kompetenceniveauet.</span><span class="sxs-lookup"><span data-stu-id="6e475-107">First, you define the organizational level code.</span></span> <span data-ttu-id="6e475-108">Du behøver kun at udføre dette trin én gang for hvert kompetenceniveau.</span><span class="sxs-lookup"><span data-stu-id="6e475-108">You only have to perform this step one time for each organizational level.</span></span> <span data-ttu-id="6e475-109">Når du har et kompetenceniveau, kan du begynde at tildele koden til kontakter.</span><span class="sxs-lookup"><span data-stu-id="6e475-109">Once you have an organizational level code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-an-organizational-level-code"></a><span data-ttu-id="6e475-110">for at definere en kompetenceniveaukode</span><span class="sxs-lookup"><span data-stu-id="6e475-110">to define an organizational level code</span></span>
<span data-ttu-id="6e475-111">Kompetenceniveaukoden definerer kompetenceniveautypen eller -kategorien, f.eks. ADMINDIR eller ØKODIR.</span><span class="sxs-lookup"><span data-stu-id="6e475-111">The organizational level code defines the type or category of the organizational level, such a CEO  or CFO.</span></span> <span data-ttu-id="6e475-112">Du kan have flere kompetenceniveaukoder.</span><span class="sxs-lookup"><span data-stu-id="6e475-112">You can have several organizational level codes.</span></span> <span data-ttu-id="6e475-113">Du definerer kompetenceniveauet fra vinduet **Kompetenceniveauer**.</span><span class="sxs-lookup"><span data-stu-id="6e475-113">To define the organizational level, you use the **Organizational Levels** window.</span></span>

1. <span data-ttu-id="6e475-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kompetenceniveauer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6e475-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Organizational Levels**, and then choose the related link.</span></span>
2. <span data-ttu-id="6e475-115">Vælg handlingen **Ny**, og indtast en kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="6e475-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="6e475-116">Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.</span><span class="sxs-lookup"><span data-stu-id="6e475-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="to-assign-organizational-levels-to-a-contact-person"></a><span data-ttu-id="6e475-117">for at tildele kompetenceniveauer til en kontaktperson</span><span class="sxs-lookup"><span data-stu-id="6e475-117">to assign organizational levels to a contact person</span></span>
<span data-ttu-id="6e475-118">Du kan kun tilknytte organisationsniveau til kontaktpersoner, ikke kontaktvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="6e475-118">You can assign organizational levels to contact persons only, not contact companies.</span></span> <span data-ttu-id="6e475-119">Du kan kun tildele ét kompetenceniveau pr. kontakt.</span><span class="sxs-lookup"><span data-stu-id="6e475-119">You can only assign one organizational level to each contact.</span></span>

1. <span data-ttu-id="6e475-120">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="6e475-120">Open the contact.</span></span>
2. <span data-ttu-id="6e475-121">I feltet **Kompetenceniveauer** skal du vælge den kode, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="6e475-121">In the **Organizational Levels** field, select the code you want to assign.</span></span>

<span data-ttu-id="6e475-122">Når du har tildelt kompetenceniveauer til dine kontakter, kan du bruge oplysningerne til at oprette målgrupper.</span><span class="sxs-lookup"><span data-stu-id="6e475-122">After you have assigned organizational levels to your contacts, you can use this information to create segments.</span></span>

<span data-ttu-id="6e475-123">Når du har tildelt ansvarsområder til kontaktpersoner, kan du bruge oplysningerne til at udvælge kontakter til målgrupper.</span><span class="sxs-lookup"><span data-stu-id="6e475-123">After you have assigned job responsibilities to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="6e475-124">Du kan finde flere oplysninger i [Fremgangsmåde: Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="6e475-124">For more information, see [How to: Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="6e475-125">Se også</span><span class="sxs-lookup"><span data-stu-id="6e475-125">See Also</span></span>
[<span data-ttu-id="6e475-126">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="6e475-126">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
[<span data-ttu-id="6e475-127">Oprette kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="6e475-127">Creating Contact Persons</span></span>](marketing-create-contact-persons.md)  
<span data-ttu-id="6e475-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6e475-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

