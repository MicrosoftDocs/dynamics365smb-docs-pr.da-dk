---
title: Sådan angives flere rentesatser
description: Du kan beregne renter med flere rentesatser for en bestemt periode. Renteberegningen sker på samme måde for alle finansielle udgifter , der er kun ændring i rentesatsen for en bestemt periode.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: e6312b1e00b3267c582dac50da616bdccd2a75b7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305976"
---
# <a name="set-up-multiple-interest-rates"></a><span data-ttu-id="27fc4-104">Angive flere rentesatser</span><span class="sxs-lookup"><span data-stu-id="27fc4-104">Set Up Multiple Interest Rates</span></span>
<span data-ttu-id="27fc4-105">Flere rentesatser bruges til forskellige perioder for forsinkede betalinger i handelstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="27fc4-105">Multiple interest rates are used for different periods for delayed payments in trade transactions.</span></span> <span data-ttu-id="27fc4-106">F.eks. angiver det offentlige den maksimale rente, der kan opkræves for en bruger.</span><span class="sxs-lookup"><span data-stu-id="27fc4-106">For example, a government specifies the maximum interest to be levied for a consumer.</span></span> <span data-ttu-id="27fc4-107">Denne rentesats kan ændres to gange om året på 1. januar og 1. juli.</span><span class="sxs-lookup"><span data-stu-id="27fc4-107">This interest rate can be changed twice a year on 01 January and 01 July.</span></span> <span data-ttu-id="27fc4-108">Rentesatsen mellem virksomheder (B2B) aftales af parterne, og der er ingen grænser for denne kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="27fc4-108">The interest rate between businesses (B2B) is agreed by the parties and there is no limit to that customer group.</span></span> <span data-ttu-id="27fc4-109">Den annoncerece rente er som regel fire procent højere end den normale bankrente.</span><span class="sxs-lookup"><span data-stu-id="27fc4-109">The announced rate is usually four percent more than the normal bank interest.</span></span>

<span data-ttu-id="27fc4-110">Når du opretter rentebetingelser og rykkerbetingelser for forsinket betaling, kan du angive flere rentesatser, så strafgebyret beregnes ud fra forskellige rentesatser i forskellige perioder.</span><span class="sxs-lookup"><span data-stu-id="27fc4-110">When you create finance charge terms and reminder terms, for delayed payment penalty, you can specify multiple interest rates so that the penalty fee is calculated from different interest rates in different periods.</span></span> <span data-ttu-id="27fc4-111">Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="27fc4-111">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>

## <a name="to-set-up-multiple-interest-rates"></a><span data-ttu-id="27fc4-112">Sådan angives flere rentesatser</span><span class="sxs-lookup"><span data-stu-id="27fc4-112">To set up multiple interest rates</span></span>  
1.  <span data-ttu-id="27fc4-113">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rentebetingelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27fc4-113">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Finance Charge Terms**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="27fc4-114">På siden **Rentebetingelser** skal du vælge de krævede økonomiske betingelser og derefter vælge handlingen **Rentesatser**.</span><span class="sxs-lookup"><span data-stu-id="27fc4-114">On the **Finance Charge Terms** page, select the required finance term, and then choose the **Interest Rates** action.</span></span>  
3.  <span data-ttu-id="27fc4-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="27fc4-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  <span data-ttu-id="27fc4-116">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="27fc4-116">Choose the **OK** button.</span></span>  
5.  <span data-ttu-id="27fc4-117">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Rykkerbetingelser**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="27fc4-117">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Reminder Terms**, and then choose the related link.</span></span>  
6.  <span data-ttu-id="27fc4-118">På siden **Rentebetingelser** skal du vælge de krævede rykkerbetingelser og derefter vælge handlingen **Niveauer**.</span><span class="sxs-lookup"><span data-stu-id="27fc4-118">On the **Reminder Terms** page, select the required reminder term, and then choose the **Levels** action.</span></span>  
7.  <span data-ttu-id="27fc4-119">På siden **Rykkerniveauer** skal du markere feltet **Beregn rente**.</span><span class="sxs-lookup"><span data-stu-id="27fc4-119">On the **Reminder Levels** page, select the **Calculate Interest** field.</span></span>  

<span data-ttu-id="27fc4-120">Når du udsteder en rentenota, viser notaen renterne med flere rentesatser for en bestemt tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="27fc4-120">When you issue a finance charge memo, the memo shows the finance charges with multiple interest rates for a specific time period.</span></span> <span data-ttu-id="27fc4-121">Rentenotaen indeholder også kontaktoplysningerne for kunden, virksomheden, der udsteder rentenotaen, et ekstra beløb og det samlede beløb.</span><span class="sxs-lookup"><span data-stu-id="27fc4-121">The memo also contains the contact details of the customer, the company issuing the memo, the additional amount, and the total amount.</span></span> <span data-ttu-id="27fc4-122">Åbningsposten på rentenotaen vises med fed skrift.</span><span class="sxs-lookup"><span data-stu-id="27fc4-122">The opening entry on the memo is displayed in bold.</span></span> <span data-ttu-id="27fc4-123">Renteberegningen beregnes ved brug af flere rentesatser for en bestemt tidsperiode og udskrives efter åbningsposten på rentenotaen.</span><span class="sxs-lookup"><span data-stu-id="27fc4-123">The finance charges are calculated with multiple interest rates for a specific time period and are printed after the opening entry of the memo.</span></span>  

## <a name="see-also"></a><span data-ttu-id="27fc4-124">Se også</span><span class="sxs-lookup"><span data-stu-id="27fc4-124">See Also</span></span>  
[<span data-ttu-id="27fc4-125">Indhente udestående beløb</span><span class="sxs-lookup"><span data-stu-id="27fc4-125">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md)  
[<span data-ttu-id="27fc4-126">Konfigurere Finans</span><span class="sxs-lookup"><span data-stu-id="27fc4-126">Setting Up Finance</span></span>](finance-setup-finance.md)
