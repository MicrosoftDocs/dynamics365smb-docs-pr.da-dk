---
title: "Oprette en købsrekvisition for at få et tilbud fra din leverandør | Microsoft Docs"
description: "Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 08/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: fe51ade7a46ab7a8fdf77419a0098ac47fe2e5d1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-request-quotes"></a><span data-ttu-id="cbcbc-103">Fremgangsmåde: Anmode om tilbud</span><span class="sxs-lookup"><span data-stu-id="cbcbc-103">How to: Request Quotes</span></span>
<span data-ttu-id="cbcbc-104">Du kan bruge en købsrekvisition som foreløbig kladde til en købsordre for senere at konvertere ordren til en købsfaktura eller en ordre.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or a order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="cbcbc-105">Sådan oprettes en købsrekvisition</span><span class="sxs-lookup"><span data-stu-id="cbcbc-105">To create a purchase quote</span></span>
1. <span data-ttu-id="cbcbc-106">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsrekvisitioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-106">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="cbcbc-107">Opret et nyt dokument på samme måde, som du opretter en købsordre.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="cbcbc-108">Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="cbcbc-108">For more information, see [How to: Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="cbcbc-109">Sådan konverteres en rekvisition til en købsordre</span><span class="sxs-lookup"><span data-stu-id="cbcbc-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="cbcbc-110">Når du har accepteret leverandørtilbuddet, kan du konvertere det til en købsfaktura eller ordre for at behandle den.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-110">When you have accepted the vendors quote, you can convert it to a purchase invoice or ordfer to process the purchase.</span></span>

1. <span data-ttu-id="cbcbc-111">Åbn en købsrekvisition, der er klar til at konvertere, og vælg derefter handlingen **Lav ordre**.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="cbcbc-112">Købsrekvisitionen fjernes fra databasen.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="cbcbc-113">En købsfaktura eller salgsordre oprettes på grundlag af oplysningerne i købsrekvisitionen, hvor du kan behandle købet.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-113">A purchase invoice or a sales order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="cbcbc-114">I feltet **Tilbudsnr.** på købsfakturaen eller købsordren kan du se nummeret på den købsrekvisition, den blev oprettet ud fra.</span><span class="sxs-lookup"><span data-stu-id="cbcbc-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbcbc-115">Se også</span><span class="sxs-lookup"><span data-stu-id="cbcbc-115">See Also</span></span>
[<span data-ttu-id="cbcbc-116">Køb</span><span class="sxs-lookup"><span data-stu-id="cbcbc-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="cbcbc-117">Opsætning af indkøb</span><span class="sxs-lookup"><span data-stu-id="cbcbc-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="cbcbc-118">Fremgangsmåde: Sende dokumenter via mail</span><span class="sxs-lookup"><span data-stu-id="cbcbc-118">How to: Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="cbcbc-119">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="cbcbc-119">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
