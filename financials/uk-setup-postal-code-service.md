---
title: "Fremgangsmåde: Konfigurere udvidelsen Britiske GetAddress.io-postnumre | Microsoft Docs"
description: "Beskriver de overordnede funktioner, du bruger til at arbejde med data i Financials, som f.eks. at angive værdier, sortere data og ændre visninger."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="bead2-103">Fremgangsmåde: Konfigurere udvidelsen Britiske GetAddress.io-postnumre</span><span class="sxs-lookup"><span data-stu-id="bead2-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="bead2-104">Denne udvidelse gør det nemt at angive adresser i Storbritannien for enheder som kunder, kontaktpersoner, medarbejdere, leverandører, bankkonti og osv.</span><span class="sxs-lookup"><span data-stu-id="bead2-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="bead2-105">Dem britiske GetAddress.io-postnumerudvidelse bruger getAddress API'en til at finde adresser i postnumre i Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="bead2-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="bead2-106">Hvis du vil bruge udvidelsen, skal du hente en plan og en API-nøgle til getAddress-API'en.</span><span class="sxs-lookup"><span data-stu-id="bead2-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="bead2-107">Det er nemt, og vi hjælpe dig med at gøre det, når du opretter den britiske GetAddress.io-postnummerudvidelse.</span><span class="sxs-lookup"><span data-stu-id="bead2-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="bead2-108">Planer er baseret på brug, eller hvad der til tider omtales som kald.</span><span class="sxs-lookup"><span data-stu-id="bead2-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="bead2-109">I dette tilfælde er et kald, når [!INCLUDE[d365fin](includes/d365fin_md.md)] viser en liste over adresser i et postnummer.</span><span class="sxs-lookup"><span data-stu-id="bead2-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="bead2-110">Afhængigt af hvor ofte du tilføjer adresser skal du vælge den plan, der passer bedst til dig.</span><span class="sxs-lookup"><span data-stu-id="bead2-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="bead2-111">Hvis du vælger **Hent API nøgle** på siden, skal du bruge planen **Fri**, hvor du kan tilføje 20 adresser pr. dag, og som gælder for 30 dage.</span><span class="sxs-lookup"><span data-stu-id="bead2-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="bead2-112">Sådan konfigurerer du britiske GetAddress.io-postnummerudvidelser</span><span class="sxs-lookup"><span data-stu-id="bead2-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="bead2-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceforbindelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bead2-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bead2-114">I vinduet **Serviceforbindelser** skal du vælge **Britisk postnummertjeneste**.</span><span class="sxs-lookup"><span data-stu-id="bead2-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="bead2-115">På siden **Konfiguration af postnummerudbyder** skal du vælge **Deaktiveret**.</span><span class="sxs-lookup"><span data-stu-id="bead2-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="bead2-116">I vinduet **Valg af postnummertjeneste** skal vælge **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="bead2-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="bead2-117">I vinduet **GetAddress.io konfiguration** skal du vælge **Hent API nøgle** for at åbne siden **Planer** på webstedet for getAddress-API'en.</span><span class="sxs-lookup"><span data-stu-id="bead2-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="bead2-118">Du skal muligvis tillade pop op-vinduer i din webbrowser.</span><span class="sxs-lookup"><span data-stu-id="bead2-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="bead2-119">Køb en plan, eller vælg **Hent API nøgle**, og angiv derefter din mailadresse.</span><span class="sxs-lookup"><span data-stu-id="bead2-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="bead2-120">Åbn mailen fra getAddress.io, og kopier API-nøglen.</span><span class="sxs-lookup"><span data-stu-id="bead2-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="bead2-121">Nøglen findes under overskriften **Din API-nøgle**.</span><span class="sxs-lookup"><span data-stu-id="bead2-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="bead2-122">I vinduet **GetAddress.io konfiguration** skal du indsætte API-nøglen i feltet **API-nøgle** og derefter vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="bead2-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="bead2-123">På siden **Serviceforbindelser** skal du kontrollere, at feltet **Adresseudbyder** viser **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="bead2-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="bead2-124">Hvis det gør det, er tjenesten aktiveret.</span><span class="sxs-lookup"><span data-stu-id="bead2-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="bead2-125">Se også</span><span class="sxs-lookup"><span data-stu-id="bead2-125">See Also</span></span>
<span data-ttu-id="bead2-126">[Britiske GetAddress.io-postnumre](ui-extensions-getaddressio.md)
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="bead2-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="bead2-127">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="bead2-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
