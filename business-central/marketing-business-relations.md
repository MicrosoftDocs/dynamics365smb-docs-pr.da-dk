---
title: Definere forretningsrelationskode for kontakter | Microsoft Docs
description: "Brug forretningsrelationer i Business Central til at hjælpe med marketing og til at angive det forretningsforhold, som findes mellem din virksomhed og dine kundeemner og kunder, f.eks. en bank eller serviceleverandør."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 8a950b87b7e7947de1602db76805a0b1f41d8274
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="c8fba-103">Opsætning af forretningsrelationer i kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="c8fba-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="c8fba-104">Du kan bruge forretningsrelationer til at angive det forretningsforhold, som findes mellem din virksomhed og dine kontakter, f.eks. et kundeemne, bank, konsulent, serviceleverandør osv.</span><span class="sxs-lookup"><span data-stu-id="c8fba-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="c8fba-105">Brug af forretningsrelationer i kontakter er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="c8fba-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="c8fba-106">Først skal du definere koden for forretningsrelationen.</span><span class="sxs-lookup"><span data-stu-id="c8fba-106">First, you define the business relation code.</span></span> <span data-ttu-id="c8fba-107">Du behøver kun at udføre dette trin én gang for hver forretningsrelation.</span><span class="sxs-lookup"><span data-stu-id="c8fba-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="c8fba-108">Når du har en forretningsrelationskode, kan du begynde at tildele koden til kontaktvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="c8fba-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c8fba-109">Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.</span><span class="sxs-lookup"><span data-stu-id="c8fba-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="c8fba-110">Sådan defineres en forretningsrelationskode</span><span class="sxs-lookup"><span data-stu-id="c8fba-110">To define a business relation code</span></span>
<span data-ttu-id="c8fba-111">Forretningsrelationskoden definerer en kategori eller type af forretningsrelation, f.eks BANK eller Law.</span><span class="sxs-lookup"><span data-stu-id="c8fba-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="c8fba-112">Du kan have flere forretningsrelationskoder.</span><span class="sxs-lookup"><span data-stu-id="c8fba-112">You can have several business relation codes.</span></span> <span data-ttu-id="c8fba-113">Du kan definere forretningsrelationen fra vinduet **Forretningsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="c8fba-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="c8fba-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsrelationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c8fba-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="c8fba-115">Vælg handlingen **Ny**, og indtast en kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c8fba-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="c8fba-116">Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.</span><span class="sxs-lookup"><span data-stu-id="c8fba-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="c8fba-117">Sådan tildeles forretningsrelationer til en kontakt</span><span class="sxs-lookup"><span data-stu-id="c8fba-117">To assign business relations to a contact</span></span>
<span data-ttu-id="c8fba-118">Du kan ikke tildele forretningsrelationer til en kontaktperson – kun til virksomheder.</span><span class="sxs-lookup"><span data-stu-id="c8fba-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="c8fba-119">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="c8fba-119">Open the contact.</span></span>
2. <span data-ttu-id="c8fba-120">Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Forretningsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="c8fba-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="c8fba-121">Vinduet **Kontakt til forretningsrelation** åbnes.</span><span class="sxs-lookup"><span data-stu-id="c8fba-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="c8fba-122">I feltet **Forretningsrelationskode** skal du vælge den forretningsrelation, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="c8fba-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="c8fba-123">Gentag disse trin for hver forretningsrelation, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="c8fba-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="c8fba-124">Du kan også tildele forretningsrelationer fra kontaktoversigten ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="c8fba-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="c8fba-125">Det antal relationer, du har tildelt kontakten, vises i feltet **Antal forretningsrelationer** i sektionen **Segmentering** i vinduet **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="c8fba-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="c8fba-126">Når du har tildelt forretningsrelationer til kontakter, kan du bruge oplysningerne til at udvælge kontakter til dine målgrupper.</span><span class="sxs-lookup"><span data-stu-id="c8fba-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="c8fba-127">Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="c8fba-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c8fba-128">Se også</span><span class="sxs-lookup"><span data-stu-id="c8fba-128">See Also</span></span>
[<span data-ttu-id="c8fba-129">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="c8fba-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="c8fba-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c8fba-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

