---
title: Konfigurere servicekontrakter | Microsoft Docs
description: "Få at vide, hvordan du definerer servicekontrakter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: b221b125a65dbad46b56172bc267a5da382dc765
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---

# <a name="set-up-service-contracts"></a><span data-ttu-id="f3fda-103">Opsætte servicekontrakter</span><span class="sxs-lookup"><span data-stu-id="f3fda-103">Set Up Service Contracts</span></span>
<span data-ttu-id="f3fda-104">Før du kan arbejde med kontrakter, skal du angive følgende:</span><span class="sxs-lookup"><span data-stu-id="f3fda-104">Before you can work with contracts, you must set up the following:</span></span> 

* <span data-ttu-id="f3fda-105">**Servicekontraktgrupper**, som samler servicekontrakter, der på en eller anden måde er indbyrdes relateret.</span><span class="sxs-lookup"><span data-stu-id="f3fda-105">**Service contract groups**, which gather service contracts that are related in some way.</span></span>
* <span data-ttu-id="f3fda-106">**Servicekontraktkontogrupper**, der bruges til at gruppere servicekontraktkonti for servicefakturaer, der er oprettet til servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="f3fda-106">**Service contract account groups**, which are used to group the service contract accounts together for service invoices created for service contracts.</span></span> <span data-ttu-id="f3fda-107">Du tildeler disse grupper til servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="f3fda-107">You assign these groups to service contracts.</span></span>  
* <span data-ttu-id="f3fda-108">**Kontraktskabeloner**, som definerer kontraktlayout for kontrakter, der indeholder de mest almindeligt anvendte detaljer i servicekontrakter.</span><span class="sxs-lookup"><span data-stu-id="f3fda-108">**Contract templates** that define contract layouts of contracts that include the most commonly used service contract details.</span></span> <span data-ttu-id="f3fda-109">Når du opretter servicekontrakttilbud, kan du gøre det ved at bruge skabeloner.</span><span class="sxs-lookup"><span data-stu-id="f3fda-109">When you create service contract quotes, you can create them by using templates.</span></span> <span data-ttu-id="f3fda-110">Når du opretter et kontrakttilbud, indeholder felterne automatisk indholdet af skabelonfelterne.</span><span class="sxs-lookup"><span data-stu-id="f3fda-110">When you create a contract quote, the fields automatically contain the contents of the template fields.</span></span>
* <span data-ttu-id="f3fda-111">**Debitorskabeloner**, så du kan oprette tilbud til kontakter eller potentielle kunder, der ikke er registreret som debitorer i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f3fda-111">**Customer templates** that let you create quotes for contacts or potential customers who are not registered as customers in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="to-set-up-a-service-contract-group"></a><span data-ttu-id="f3fda-112">Sådan defineres servicekontraktgrupper</span><span class="sxs-lookup"><span data-stu-id="f3fda-112">To set up a service contract group</span></span>  
1. <span data-ttu-id="f3fda-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Servicekontraktgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3fda-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3fda-114">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3fda-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="f3fda-115">Marker afkrydsningsfeltet **Kun rabat på kontraktordrer**, hvis kontrakt- eller servicerabatter kun skal være gyldige for kontraktserviceordrer, f.eks. vedligeholdelse.</span><span class="sxs-lookup"><span data-stu-id="f3fda-115">Choose the **Disc. on Contr. Orders Only** check box if you want contract or service discounts to be valid only for contract service orders, such as maintenance.</span></span>  

## <a name="to-set-up-a-service-contract-account-group"></a><span data-ttu-id="f3fda-116">Sådan oprettes servicekontraktkontogrupper</span><span class="sxs-lookup"><span data-stu-id="f3fda-116">To set up a service contract account group</span></span>  
1. <span data-ttu-id="f3fda-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Servicekontraktkontogrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3fda-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Serv. Contract Account Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3fda-118">Opret en ny servicekontraktkontogruppe.</span><span class="sxs-lookup"><span data-stu-id="f3fda-118">Create a new service contract account group.</span></span>   
3. <span data-ttu-id="f3fda-119">Udfyld felterne **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-119">Fill in the **Code** and **Description** fields.</span></span> <span data-ttu-id="f3fda-120">Disse felter beskriver servicekontogruppen.</span><span class="sxs-lookup"><span data-stu-id="f3fda-120">These fields describe the service account group.</span></span>  
4. <span data-ttu-id="f3fda-121">Udfyld feltet **Ikkeforudbet. kontraktkonto**, og vælg finanskontonummeret for den ikke forudbetalte konto.</span><span class="sxs-lookup"><span data-stu-id="f3fda-121">Fill in the **Non-Prepaid Contract Acc.** field, choose general ledger account number for the non-prepaid account.</span></span>  
5. <span data-ttu-id="f3fda-122">I feltet **Forudbet. kontraktkonto** skal du vælge finanskontonummeret for den forudbetalte konto.</span><span class="sxs-lookup"><span data-stu-id="f3fda-122">In the **Prepaid Contract Acc.** field, choose the general ledger account number for the prepaid account.</span></span>  

## <a name="to-set-up-a-contract-template"></a><span data-ttu-id="f3fda-123">Sådan oprettes kontraktskabeloner</span><span class="sxs-lookup"><span data-stu-id="f3fda-123">To set up a contract template</span></span>  
1. <span data-ttu-id="f3fda-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Skabelon til servicekontrakt**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3fda-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Contract Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3fda-125">Opret en ny servicekontraktskabelon.</span><span class="sxs-lookup"><span data-stu-id="f3fda-125">Create a new service contract template.</span></span>  
3. <span data-ttu-id="f3fda-126">I feltet **Nummer**</span><span class="sxs-lookup"><span data-stu-id="f3fda-126">In the **No.**</span></span> <span data-ttu-id="f3fda-127">skal du skrive et nummer til kontraktskabelonen.</span><span class="sxs-lookup"><span data-stu-id="f3fda-127">field, enter a number for the contract template.</span></span>  
  
     <span data-ttu-id="f3fda-128">Hvis du har defineret en nummerserie for kontraktskabeloner i vinduet **Serviceopsætning**, kan du trykke på Enter og få indsat det næste ledige kontraktskabelonnummer automatisk.</span><span class="sxs-lookup"><span data-stu-id="f3fda-128">Alternatively, if you have set up number series for contract templates in the **Service Mgt. Setup** window, you can press the Enter key to enter the next available contract template number.</span></span> <span data-ttu-id="f3fda-129">Udfyld de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3fda-129">Fill in the other fields if appropriate.</span></span>  
  
4. <span data-ttu-id="f3fda-130">I oversigtspanelet **Faktura** skal du udfylde feltet **Servicekontraktkto.grp.kode**, **Faktureringsperiode** osv.</span><span class="sxs-lookup"><span data-stu-id="f3fda-130">On the **Invoice** FastTab, fill in the **Serv. Contract Acc. Group Code** field, the **Invoice Period**, and so on.</span></span> <span data-ttu-id="f3fda-131">Udfyld de andre felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="f3fda-131">Fill in the other fields if appropriate.</span></span>  
5. <span data-ttu-id="f3fda-132">Vælg handlingen **Servicerabatter** for at tilføje kontraktrabatter.</span><span class="sxs-lookup"><span data-stu-id="f3fda-132">Choose the **Service Discounts** action to add contract discounts.</span></span>  

## <a name="to-set-up-a-customer-template"></a><span data-ttu-id="f3fda-133">Sådan oprettes debitorskabeloner</span><span class="sxs-lookup"><span data-stu-id="f3fda-133">To set up a customer template</span></span>  
1. <span data-ttu-id="f3fda-134">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorskabeloner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f3fda-134">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Templates**, and then choose the related link.</span></span>  
2. <span data-ttu-id="f3fda-135">Opret et nyt debitorskabelonkort.</span><span class="sxs-lookup"><span data-stu-id="f3fda-135">Create a new customer template card.</span></span>  
3. <span data-ttu-id="f3fda-136">I oversigtspanelet **Generelt** skal du skrive en kode og en beskrivelse til debitorskabelonen i henholdsvis feltet **Kode** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-136">On the **General** FastTab, enter a code and a description for the customer template in the **Code** and **Description** fields respectively.</span></span> 
4. <span data-ttu-id="f3fda-137">Du kan definere søgekriterier ved at udfylde de øvrige felter, f.eks. **Lande-/områdekode**, **Distriktskode** og **Sprogkode**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-137">To define search criteria, fill in the other fields, such as **Country/Region Code**, **Territory Code**, and **Language Code**.</span></span>  
5. <span data-ttu-id="f3fda-138">Udfyld felterne **Virksomhedsbogføringsgruppe** og **Debitorbogføringsgruppe**.</span><span class="sxs-lookup"><span data-stu-id="f3fda-138">Fill in the **Gen. Bus. Posting Group** and **Customer Posting Group** fields.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f3fda-139">Se også</span><span class="sxs-lookup"><span data-stu-id="f3fda-139">See Also</span></span>
[<span data-ttu-id="f3fda-140">Konfigurere Service</span><span class="sxs-lookup"><span data-stu-id="f3fda-140">Setting Up Service Management</span></span>](service-setup-service.md)
