---
title: Konfigurere webkilder for kontaktvirksomheder | Microsoft Docs
description: Du kan definere internet- eller webkilder og tildele dem til en kontaktvirksomhed for at identificere, hvordan du vil søge efter oplysninger om dine kontakter.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: internet
ms.date: 10/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 8e9defda4f5ff25d5ac90a308549880e454bc637
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308664"
---
# <a name="set-up-web-sources-for-contact-companies"></a><span data-ttu-id="62c95-103">Angive webkilder for kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="62c95-103">Set Up Web Sources for Contact Companies</span></span>
<span data-ttu-id="62c95-104">Du kan bruge webkilder til dine kontaktvirksomheder for at identificere f.eks. søgemaskiner og websteder på internettet, som du vil bruge til at søge efter oplysninger om kontakterne.</span><span class="sxs-lookup"><span data-stu-id="62c95-104">You can use web sources with your contact companies to identify, for example, search engines and web sites, on the Internet that you want to use to search for information about the contacts.</span></span> <span data-ttu-id="62c95-105">Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="62c95-105">When assigning web sources, you specify which search engine and search word the application will use to find the requested information.</span></span>

<span data-ttu-id="62c95-106">Brug af webkilder for kontakter er totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="62c95-106">Using web sources on contacts is a two-step process.</span></span> <span data-ttu-id="62c95-107">Først skal du angive webkildekoden.</span><span class="sxs-lookup"><span data-stu-id="62c95-107">First, you define the web source code.</span></span> <span data-ttu-id="62c95-108">Du behøver kun at udføre dette trin én gang for hver webkilde.</span><span class="sxs-lookup"><span data-stu-id="62c95-108">You only have to perform this step one time for each web source.</span></span> <span data-ttu-id="62c95-109">Når du har en webkildekode, kan du begynde at tildele koden til kontakter.</span><span class="sxs-lookup"><span data-stu-id="62c95-109">Once you have a web source code, you can start to assign the code to contact persons.</span></span>

## <a name="to-define-a-web-source-code"></a><span data-ttu-id="62c95-110">Sådan defineres en webkildekode</span><span class="sxs-lookup"><span data-stu-id="62c95-110">To define a web source code</span></span>
1. <span data-ttu-id="62c95-111">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webkilder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="62c95-111">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Sources**, and then choose the related link.</span></span>
2. <span data-ttu-id="62c95-112">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="62c95-112">Choose the **New** actions.</span></span>
3. <span data-ttu-id="62c95-113">Udfyld felterne **Kode**, **Beskrivelse** og **URL**.</span><span class="sxs-lookup"><span data-stu-id="62c95-113">Fill in the **Code**, **Description**, and **URL** fields.</span></span>

    <span data-ttu-id="62c95-114">Indtast %1 i feltet **URL** for at indsætte en pladsholder for et søgeord i URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="62c95-114">Type %1 in the **URL** field to insert a placeholder for a search word in the URL.</span></span> <span data-ttu-id="62c95-115">Når du starter webkilden fra en kontakt, erstattes %1 med det søgeord, du har indtastet på siden **Webkilder for kontakter**, f.eks. navnet på virksomheden.</span><span class="sxs-lookup"><span data-stu-id="62c95-115">When you launch the web source from a contact, the %1 is replaced with the search word, for example, the name of the company that you have entered on the **Contact Web Sources** page.</span></span>

<span data-ttu-id="62c95-116">Gentag disse trin for hver webkilde, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="62c95-116">Repeat these steps to set up as many web sources as you want.</span></span>

## <a name="to-assign-web-sources-to-a-contact-company"></a><span data-ttu-id="62c95-117">Sådan tildeles webkilder til en kontaktvirksomhed</span><span class="sxs-lookup"><span data-stu-id="62c95-117">To assign web sources to a contact company</span></span>
<span data-ttu-id="62c95-118">Når du tildeler websteder skal du angive den søgemaskine og det søgeord, som skal bruges til at finde de ønskede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="62c95-118">When assigning web sources, you specify which search engine and search word that the application will use to find the requested information.</span></span>

1. <span data-ttu-id="62c95-119">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="62c95-119">Open the contact.</span></span>
2. <span data-ttu-id="62c95-120">Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Webkilder**.</span><span class="sxs-lookup"><span data-stu-id="62c95-120">Choose the **Company** action, and then choose the **Web Sources** action.</span></span> <span data-ttu-id="62c95-121">Siden **Webkilder for kontakt** åbnes.</span><span class="sxs-lookup"><span data-stu-id="62c95-121">The **Contact Web Sources** page opens.</span></span>
3. <span data-ttu-id="62c95-122">I feltet **Webkildekode** skal du vælge den webkilde , du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="62c95-122">In the **Web Source Code** field, choose the web source you want to assign.</span></span>
4. <span data-ttu-id="62c95-123">Brug feltet **Søgeord** til at indtaste det søgeord, som du vil bruge til at finde oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="62c95-123">In the **Search Word** field, enter the search word that you want to use to find the information.</span></span>

<span data-ttu-id="62c95-124">Gentag disse trin for hver webkilde, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="62c95-124">Repeat these steps to assign as many web sources as you want.</span></span>

<span data-ttu-id="62c95-125">Du kan også tildele webkilder fra siden **Kontaktoversigt** ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="62c95-125">You can also assign web sources from the **Contact List** page by following the same procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="62c95-126">Se også</span><span class="sxs-lookup"><span data-stu-id="62c95-126">See Also</span></span>
[<span data-ttu-id="62c95-127">Oprettelse af kontakter</span><span class="sxs-lookup"><span data-stu-id="62c95-127">Creating Contacts</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="62c95-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="62c95-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
