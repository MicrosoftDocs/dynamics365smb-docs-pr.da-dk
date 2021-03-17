---
title: Konfiguration af Rentebetingelser
description: Se her, hvordan du konfigurerer Business Central, så du kan underrette debitorerne om tilføjede gebyrer ved at sende rentenotaer.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: dad02adfb6cc0a0ebb6d950b67f2e092b3313c59
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5377083"
---
# <a name="set-up-finance-charge-terms"></a><span data-ttu-id="bd3f0-103">Konfiguration af Rentebetingelser</span><span class="sxs-lookup"><span data-stu-id="bd3f0-103">Set Up Finance Charge Terms</span></span>

<span data-ttu-id="bd3f0-104">Når en debitor ikke betaler til forfaldsdatoen, kan du automatisk få en rentenota beregnet og føje den til de forfaldne beløb på debitorens konto.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-104">When a customer does not pay by the due date, you can have finance charges calculated automatically and add them to the overdue amounts on the customer's account.</span></span> <span data-ttu-id="bd3f0-105">Du kan underrette debitor om de tilføjede gebyrer ved at sende rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-105">You can inform customers of the added charges by sending finance charge memos.</span></span> <span data-ttu-id="bd3f0-106">Først skal du definere en kode, der repræsenterer for hver renteberegningsmetode.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-106">But first, you must set up a code that represents each finance charge calculation.</span></span> <span data-ttu-id="bd3f0-107">Du kan så angive denne kode i feltet Rentebetingelseskode på debitorkortene.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-107">Then you can enter this code in the Fin. Charge Terms Code field on customer cards.</span></span>  

## <a name="finance-charge-terms"></a><span data-ttu-id="bd3f0-108">Rentebetingelser</span><span class="sxs-lookup"><span data-stu-id="bd3f0-108">Finance charge terms</span></span>

<span data-ttu-id="bd3f0-109">Du skal definere rentebetingelser for hver renteberegning og derefter knytte betingelserne til debitoren i feltet **Rentebetingelseskode** på siden **Debitor**.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-109">You must set up finance charge terms for each finance charge calculation, and then assign the terms to the customer in the **Fin. Charge Terms Code** field on the **Customer** page.</span></span>

<span data-ttu-id="bd3f0-110">Rentenotaer kan beregnes efter kreditkronedage- eller saldorentemetoder.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-110">Finance charges can be calculated using either the average daily balance or the balance due methods.</span></span>

* <span data-ttu-id="bd3f0-111">Gennemsnitlig daglig saldo</span><span class="sxs-lookup"><span data-stu-id="bd3f0-111">Average daily balance</span></span>  
  
  <span data-ttu-id="bd3f0-112">Der tages hensyn til det antal dage, betalingsfristen er overskredet med:</span><span class="sxs-lookup"><span data-stu-id="bd3f0-112">The number of days the payment is overdue is taken into account:</span></span>  
  <span data-ttu-id="bd3f0-113">*Metoden Kreditkronedage* - *Rente* = *Forfalden saldo* x *(Kreditdage/Renteperiode)* x *(Rentesats/100)*</span><span class="sxs-lookup"><span data-stu-id="bd3f0-113">*Average Daily Balance method* - *Finance Charge* = *Overdue Amount* x *(Days Overdue / Interest Period)* x *(Interest Rate/100)*</span></span>

* <span data-ttu-id="bd3f0-114">Forf. beløb</span><span class="sxs-lookup"><span data-stu-id="bd3f0-114">Balance due</span></span>  
  
  <span data-ttu-id="bd3f0-115">Rentegebyret er blot en procentdel af den forfaldne saldo:</span><span class="sxs-lookup"><span data-stu-id="bd3f0-115">The finance charge is a percentage of the overdue amount:</span></span>  
  <span data-ttu-id="bd3f0-116">*Saldorenteprincippet* - *Rente* = *Forfalden saldo* x *(Rentesats/100)*</span><span class="sxs-lookup"><span data-stu-id="bd3f0-116">*Balance Due method* - *Finance Charge* = *Overdue Amount* x *(Interest Rate / 100)*</span></span>

<span data-ttu-id="bd3f0-117">Hver kode i tabellen Rentebetingelser er desuden kædet sammen med en undertabel, nemlig tabellen Rentenotatekst.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-117">Additionally, each term in the Finance Charge Terms table is linked to a subtable, the Finance Charge Text table.</span></span> <span data-ttu-id="bd3f0-118">Til hver rentebetingelse kan du definere en starttekst og/eller en sluttekst, som skal vises på rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-118">For each set of finance charge terms, you can define a beginning and/or an ending text to include on the finance charge memo.</span></span>

### <a name="to-set-up-finance-charge-terms"></a><span data-ttu-id="bd3f0-119">Sådan konfigurerer du rentebetingelser</span><span class="sxs-lookup"><span data-stu-id="bd3f0-119">To set up finance charge terms</span></span>

1. <span data-ttu-id="bd3f0-120">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentebetingelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-120">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2. <span data-ttu-id="bd3f0-121">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-121">Fill in the fields as necessary.</span></span>
3. <span data-ttu-id="bd3f0-122">Hvis du vil bruge mere end én kombination af rentebetingelser, kan du angive en kode for hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-122">To use more than one combination of finance charge terms, set up a code for each one.</span></span>

    <span data-ttu-id="bd3f0-123">For hver rentebetingelse kan du angive individuelle betingelser, som kan omfatte ekstra gebyrer i både lokal og udenlandsk valuta.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-123">For each finance charge term, you can specify individual conditions that can include additional fees in both LCY and in foreign currency.</span></span> <span data-ttu-id="bd3f0-124">Du kan definere adskillige opkrævningsgebyrer i udenlandsk valuta for hver kode på siden **Rentebetingelser**.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-124">You can define additional fees in foreign currencies for each term on the **Finance Charge Terms** page.</span></span>
4. <span data-ttu-id="bd3f0-125">Vælg handlingen **Valutaer**.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-125">Choose the **Currencies** action.</span></span>
5. <span data-ttu-id="bd3f0-126">På siden **Valutaer til rentebetingelser** skal du for hver periode angive en valutakode og et opkrævningsgebyr.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-126">On the **Currencies for Fin. Chrg. Terms** page, define for each term a currency code and an additional fee.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="bd3f0-127">Når du beregner renter i en udenlandsk valuta, bruges de betingelser for udenlandsk valuta, som du angiver her, til at oprette rentenotaer.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-127">When you create finance charges in a foreign currency, the foreign currency conditions that you set up here will be used to create finance charge memos.</span></span> <span data-ttu-id="bd3f0-128">Hvis der ikke er defineret rentebetingelser i udenlandske valutaer, bruges rentebetingelserne i den regnskabsvaluta, der er angivet på siden **Rentebetingelser**, og de konverteres derefter til den relevante valuta.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-128">If there are no foreign currency finance charge conditions set up, the LCY finance charge conditions specified on the **Finance Charge Terms** page will be used and then converted to the relevant currency.</span></span>

    <span data-ttu-id="bd3f0-129">For hver rentebetingelse kan du angive tekst, der udskrives før (**Starttekst**) eller efter (**Sluttekst**) på posterne i rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-129">For each finance charge term, you can specify text that will be printed before (**Beginning Text**) or after (**Ending Text**) on the entries on the finance charge memo.</span></span>  
6. <span data-ttu-id="bd3f0-130">Vælg henholdsvis handlingen **Starttekst** eller **Sluttekst**, og udfyld siden **Rentenotatekst**.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-130">Choose the **Beginning Text** or **Ending Text** actions respectively, and fill on the **Finance Charge Text** page.</span></span>
7. <span data-ttu-id="bd3f0-131">Hvis du vil indsætte relaterede værdier i den resulterende rentenotatekst automatisk, skal du angive følgende pladsholdere i feltet **Tekst**.</span><span class="sxs-lookup"><span data-stu-id="bd3f0-131">To automatically insert related values in the resulting finance charge text, enter the following placeholders in the **Text** field.</span></span>

|<span data-ttu-id="bd3f0-132">Pladsholder</span><span class="sxs-lookup"><span data-stu-id="bd3f0-132">Placeholder</span></span>|<span data-ttu-id="bd3f0-133">Værdi</span><span class="sxs-lookup"><span data-stu-id="bd3f0-133">Value</span></span>|  
|-----------------|-----------|  
|<span data-ttu-id="bd3f0-134">%1</span><span class="sxs-lookup"><span data-stu-id="bd3f0-134">%1</span></span>|<span data-ttu-id="bd3f0-135">Indholdet af feltet **Bilagsdato** på rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-135">Content of the **Document Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-136">%2</span><span class="sxs-lookup"><span data-stu-id="bd3f0-136">%2</span></span>|<span data-ttu-id="bd3f0-137">Indholdet af feltet **Forfaldsdato** på rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-137">Content of the **Due Date** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-138">%3</span><span class="sxs-lookup"><span data-stu-id="bd3f0-138">%3</span></span>|<span data-ttu-id="bd3f0-139">Indholdet af feltet **Rentesats** på de relaterede rentebetingelser</span><span class="sxs-lookup"><span data-stu-id="bd3f0-139">Content of the **Interest Rate** field on the related finance charge terms</span></span>|  
|<span data-ttu-id="bd3f0-140">%4</span><span class="sxs-lookup"><span data-stu-id="bd3f0-140">%4</span></span>|<span data-ttu-id="bd3f0-141">Indholdet af feltet **Restbeløb** i rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-141">Content of the **Remaining Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-142">%5</span><span class="sxs-lookup"><span data-stu-id="bd3f0-142">%5</span></span>|<span data-ttu-id="bd3f0-143">Indholdet af feltet **Rentebeløb** i rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-143">Content of the **Interest Amount** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-144">%6</span><span class="sxs-lookup"><span data-stu-id="bd3f0-144">%6</span></span>|<span data-ttu-id="bd3f0-145">Indholdet af feltet **Opkrævningsgebyr** i rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-145">Content of the **Additional Fee** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-146">%7</span><span class="sxs-lookup"><span data-stu-id="bd3f0-146">%7</span></span>|<span data-ttu-id="bd3f0-147">Rykkerens totalbeløb</span><span class="sxs-lookup"><span data-stu-id="bd3f0-147">The total amount of the reminder</span></span>|  
|<span data-ttu-id="bd3f0-148">%8</span><span class="sxs-lookup"><span data-stu-id="bd3f0-148">%8</span></span>|<span data-ttu-id="bd3f0-149">Indholdet af feltet **Valutadato** på rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-149">Content of the **Currency Code** field on the finance charge memo header</span></span>|  
|<span data-ttu-id="bd3f0-150">%9</span><span class="sxs-lookup"><span data-stu-id="bd3f0-150">%9</span></span>|<span data-ttu-id="bd3f0-151">Indholdet af feltet **Bogføringsdato** i rentenotahovedet</span><span class="sxs-lookup"><span data-stu-id="bd3f0-151">Content of the **Posting Date** field on the finance charge memo header</span></span>|  

## <a name="see-also"></a><span data-ttu-id="bd3f0-152">Se også</span><span class="sxs-lookup"><span data-stu-id="bd3f0-152">See also</span></span>

[<span data-ttu-id="bd3f0-153">Indhente udestående beløb</span><span class="sxs-lookup"><span data-stu-id="bd3f0-153">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="bd3f0-154">Konfiguration af rykkerbetingelser og -niveauer</span><span class="sxs-lookup"><span data-stu-id="bd3f0-154">Set Up Reminder Terms and Levels</span></span>](finance-setup-reminders.md)  
[<span data-ttu-id="bd3f0-155">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="bd3f0-155">Setting Up Finance</span></span>](finance-setup-finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]