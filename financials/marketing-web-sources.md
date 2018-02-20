---
title: Konfigurere webkilder for kontaktvirksomheder | Microsoft Docs
description: "Du kan definere internet- eller webkilder og tildele dem til en kontaktvirksomhed for at identificere, hvordan du vil søge efter oplysninger om dine kontakter."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b80edfbbad575cfcaa15b2c1b79a4feacb077371
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="14425-103">Angive webkilder for kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="14425-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="14425-104">Du kan bruge webkilder til dine kontaktvirksomheder for at identificere f.eks. søgemaskiner og websteder på internettet, som du vil bruge til at søge efter oplysninger om kontakterne.</span><span class="sxs-lookup"><span data-stu-id="14425-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="14425-105">Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="14425-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="14425-106">Brug af webkilder for kontakter er totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="14425-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="14425-107">Først skal du angive webkildekoden.</span><span class="sxs-lookup"><span data-stu-id="14425-107">First, you define the web source code.</span></span> <span data-ttu-id="14425-108">Du behøver kun at udføre dette trin én gang for hver webkilde.</span><span class="sxs-lookup"><span data-stu-id="14425-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="14425-109">Når du har en webkildekode, kan du begynde at tildele koden til kontakter.</span><span class="sxs-lookup"><span data-stu-id="14425-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="14425-110">Sådan defineres en webkildekode</span><span class="sxs-lookup"><span data-stu-id="14425-110">To define a web source code</span></span>
1. <span data-ttu-id="14425-111">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Webkilder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="14425-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="14425-112">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="14425-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="14425-113">Udfyld felterne **Kode**, **Beskrivelse** og **URL**.</span><span class="sxs-lookup"><span data-stu-id="14425-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="14425-114">Indtast %1 i feltet **URL** for at indsætte en pladsholder for et søgeord i URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="14425-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="14425-115">Når du starter webkilden fra en kontakt, erstattes %1 med det søgeord, du har indtastet i vinduet **Webkilder for kontakter**, f.eks. navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="14425-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered in the **Contact Web Sources** window.</span></span>

<span data-ttu-id="14425-116">Gentag disse trin for hver webkilde, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="14425-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="14425-117">Sådan tildeles webkilder til en kontaktvirksomhed</span><span class="sxs-lookup"><span data-stu-id="14425-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="14425-118">Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="14425-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="14425-119">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="14425-119">Open the contact.</span></span>
2. <span data-ttu-id="14425-120">Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Webkilder**.</span><span class="sxs-lookup"><span data-stu-id="14425-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="14425-121">Vinduet **Webkilder for kontakt** åbnes.</span><span class="sxs-lookup"><span data-stu-id="14425-121">The **Contact Web Sources** window opens.</span></span>
3. <span data-ttu-id="14425-122">I feltet **Webkildekode** skal du vælge den webkilde , du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="14425-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="14425-123">Brug feltet **Søgeord** til at indtaste det søgeord, som du vil bruge til at finde oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="14425-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="14425-124">Gentag disse trin for hver webkilde, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="14425-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="14425-125">Du kan også tildele webkilder fra vinduet **Kontaktoversigt** ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="14425-125">You can also assign web sources from the **Contact List** window by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="14425-126">Se også</span><span class="sxs-lookup"><span data-stu-id="14425-126">See Also</span></span>
[<span data-ttu-id="14425-127">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="14425-127">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="14425-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14425-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

