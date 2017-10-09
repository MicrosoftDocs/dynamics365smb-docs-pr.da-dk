---
title: "Fremgangsmåde: Kontrollere SE/CVR-numre | Microsoft Docs"
description: "Du kan bruge en EU-webtjeneste til at kontrollere, om de momsregistreringsnumre, du angiver på debitor-, kreditor- eller kontaktkort, er gyldige."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="6ad00-103">Fremgangsmåde: Kontrollere SE/CVR-numre</span><span class="sxs-lookup"><span data-stu-id="6ad00-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="6ad00-104">Du kan bruge en EU-webtjeneste til at kontrollere, om de momsregistreringsnumre, du angiver på debitor-, kreditor- eller kontaktkort, er gyldige.</span><span class="sxs-lookup"><span data-stu-id="6ad00-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="6ad00-105">Når du ændrer værdien i feltet **SE/CVR-nr.** på et kort, hvor værdien i feltet **Lande-områdekode** er et EU-landområde, bliver det nye momsregistreringsnummer og dit bruger-id logført i vinduet **Log over SE/CVR-nr.**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="6ad00-106">Du kan kontrollere et CVR-nummer ved at vælge knappen **Bekræft SE/CVR-nr.** i vinduet **Log over SE/CVR-nr.**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="6ad00-107">Der oprettes en ny linje, hver gang du bruger kontrolfunktionen.</span><span class="sxs-lookup"><span data-stu-id="6ad00-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="6ad00-108">Hvis nummeret kunne bekræftes, indeholder feltet **Status** værdien **Gyldig**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="6ad00-109">Hvis nummeret ikke kunne bekræftes, vil feltet **Status** indeholde **Ugyldig**, og du skal derefter ændre tallet i feltet **SE/CVR-nr.** på kortet og starte kontrolfunktionen igen.</span><span class="sxs-lookup"><span data-stu-id="6ad00-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="6ad00-110">URL-adressen for standard-webtjenesten er angivet i feltet **URL-adresse til validering af SE/CVR-nr.** i vinduet **Regnskabsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="6ad00-111">I tabellen **SE/CVR-nr.format** kan du for hvert land/område ændre de forskellige formater af CVR-nummer, som brugere har tilladelse til at skrive i feltet **SE/CVR-nr.**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="6ad00-112">Denne webtjeneste bruger HTTP-protokollen, hvilket betyder, at data, der overføres via tjenesten, ikke er krypteret.</span><span class="sxs-lookup"><span data-stu-id="6ad00-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="6ad00-113">Du kan opleve nedetid for denne tjeneste, som Microsoft ikke er ansvarlig for, da tjenesten er en del af et bredt EU-netværk af nationale momsregistre.</span><span class="sxs-lookup"><span data-stu-id="6ad00-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="6ad00-114">Sådan bekræftes et CVR-nummer fra et debitorkort</span><span class="sxs-lookup"><span data-stu-id="6ad00-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="6ad00-115">Benyt følgende fremgangsmåde til at kontrollere momsregistreringsnummeret for en debitor.</span><span class="sxs-lookup"><span data-stu-id="6ad00-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="6ad00-116">Trinene er de samme for en leverandør og en kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="6ad00-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="6ad00-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6ad00-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="6ad00-118">Åbn et debitorkort, hvor du vil kontrollere momsregistreringsnummeret.</span><span class="sxs-lookup"><span data-stu-id="6ad00-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="6ad00-119">Feltet **Lande/områdekode** på debitorkortet skal indeholde et EU-land/område.</span><span class="sxs-lookup"><span data-stu-id="6ad00-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="6ad00-120">Brug oversigtspanelet **Fakturering** til at vælge Specificer-knappen ud for feltet **SE/CVR-nr.**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="6ad00-121">Vinduet **Log over SE/CVR-nr.** åbnes og viser én linje, hvor feltet **Status** indeholder **Ikke bekræftet**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="6ad00-122">Vælg handlingen **Bekræft SE/CVR-nr.**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="6ad00-123">Der oprettes en ny linje, hvor feltet **Status** indeholder enten **Gyldig** eller **Ugyldig**.</span><span class="sxs-lookup"><span data-stu-id="6ad00-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="6ad00-124">Hvis feltet **Status** indeholder **Ugyldig**, skal du ændre nummeret i feltet **SE/CVR-nr.** på kortet og derefter gentage trin 3 og 4.</span><span class="sxs-lookup"><span data-stu-id="6ad00-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6ad00-125">Se også</span><span class="sxs-lookup"><span data-stu-id="6ad00-125">See Also</span></span>  
[<span data-ttu-id="6ad00-126">Finans</span><span class="sxs-lookup"><span data-stu-id="6ad00-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="6ad00-127">Fremgangsmåde: Registrere nye debitorer</span><span class="sxs-lookup"><span data-stu-id="6ad00-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="6ad00-128">Fremgangsmåde: Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="6ad00-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="6ad00-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="6ad00-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

