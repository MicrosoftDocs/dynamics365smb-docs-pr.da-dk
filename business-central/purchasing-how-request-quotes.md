---
title: Oprette en købsrekvisition for at få et tilbud | Microsoft Docs
description: Beskriver, hvordan du opretter et salgstilbuds- eller tilbudsanmodningsdokument for at registrere dit tilbud til en kunde om at sælge produkter i henhold til bestemte betingelser.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 01f0f607faab45b07a85fe4cd13327b02ae14f1e
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5387745"
---
# <a name="request-quotes"></a><span data-ttu-id="9d9cf-103">Anmode om tilbud</span><span class="sxs-lookup"><span data-stu-id="9d9cf-103">Request Quotes</span></span>
<span data-ttu-id="9d9cf-104">Du kan bruge en købsrekvisition som foreløbig kladde til en købsordre for senere at konvertere ordren til en købsfaktura eller en ordre.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-104">A purchase quote can be used as a preliminary draft for a purchase order, and the order can then be converted to a purchase invoice or an order.</span></span>


## <a name="to-create-a-purchase-quote"></a><span data-ttu-id="9d9cf-105">Sådan oprettes en købsrekvisition</span><span class="sxs-lookup"><span data-stu-id="9d9cf-105">To create a purchase quote</span></span>
1. <span data-ttu-id="9d9cf-106">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsrekvisitioner**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Quotes**, and then choose the related link.</span></span>
2. <span data-ttu-id="9d9cf-107">Opret et nyt dokument på samme måde, som du opretter en købsordre.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-107">Create a new document, in the same way as you make a purchase order.</span></span> <span data-ttu-id="9d9cf-108">Du kan finde flere oplysninger under [Registrere køb](purchasing-how-record-purchases.md).</span><span class="sxs-lookup"><span data-stu-id="9d9cf-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md).</span></span>

## <a name="to-convert-a-purchase-quote-to-a-purchase-order"></a><span data-ttu-id="9d9cf-109">Sådan konverteres en rekvisition til en købsordre</span><span class="sxs-lookup"><span data-stu-id="9d9cf-109">To convert a purchase quote to a purchase order</span></span>
<span data-ttu-id="9d9cf-110">Når du har accepteret leverandørtilbuddet, kan du konvertere det til en købsfaktura eller ordre for at behandle den.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-110">When you have accepted the vendor's quote, you can convert it to a purchase invoice or order to process the purchase.</span></span>

1. <span data-ttu-id="9d9cf-111">Åbn en købsrekvisition, der er klar til at konvertere, og vælg derefter handlingen **Lav ordre**.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-111">Open a purchase quote that is ready to convert, and then choose the **Make Order** action.</span></span>

<span data-ttu-id="9d9cf-112">Købsrekvisitionen fjernes fra databasen.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-112">The purchase quote is removed from the database.</span></span> <span data-ttu-id="9d9cf-113">En købsfaktura eller indkøbsordre oprettes på grundlag af oplysningerne i købsrekvisitionen, hvor du kan behandle købet.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-113">A purchase invoice or a purchase order is created based on the information in the purchase quote in which you can process the purchase.</span></span> <span data-ttu-id="9d9cf-114">I feltet **Tilbudsnr.** på købsfakturaen eller købsordren kan du se nummeret på den købsrekvisition, den blev oprettet ud fra.</span><span class="sxs-lookup"><span data-stu-id="9d9cf-114">In the **Quote No.** field on the purchase invoice or purchase order, you can see the number of the purchase quote that it was made from.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d9cf-115">Se også</span><span class="sxs-lookup"><span data-stu-id="9d9cf-115">See Also</span></span>
[<span data-ttu-id="9d9cf-116">Køb</span><span class="sxs-lookup"><span data-stu-id="9d9cf-116">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="9d9cf-117">Opsætning af indkøb</span><span class="sxs-lookup"><span data-stu-id="9d9cf-117">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="9d9cf-118">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="9d9cf-118">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="9d9cf-119">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="9d9cf-119">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]