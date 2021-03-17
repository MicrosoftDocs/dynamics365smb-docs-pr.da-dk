---
title: Udvidelsen Send remitteringsadvis | Microsoft Docs
description: Beskriver udvidelsen Send remitteringsadvis, der giver mulighed for at emaile og sende remitteringsadvis igen fra betalingskladden og kreditorposterne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e0868a5919f82af9d19dbd692c8d27577e64b6b0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5376958"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="2e466-103">Send remitteringsadvis</span><span class="sxs-lookup"><span data-stu-id="2e466-103">Send Remittance Advice</span></span>

<span data-ttu-id="2e466-104">Når der anvendes remitteringsadvis til at underrette kreditorerne om betalinger, kan du nu sende mails med flere remitteringsadviser fra udbetalingskladden og sende igen, når der er foretaget betalinger fra kreditorposter, ved hjælp af dokumentafsendelsesprofiler.</span><span class="sxs-lookup"><span data-stu-id="2e466-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="2e466-105">Denne funktionalitet understøttes kun i Business Central online og til det lokale miljø i følgende lande: Storbritannien, USA, Canada, Australien, New Zealand og Sydafrika.</span><span class="sxs-lookup"><span data-stu-id="2e466-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="2e466-106">Du kan sende remitteringsadvis på to forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="2e466-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="2e466-107">På siden **Udbetalingskladde** skal du vælge **Relaterede**, **Betalinger**, **Send remitteringsadvis** for at maile remitteringsadvis til en eller flere udbetalingskladdelinjer</span><span class="sxs-lookup"><span data-stu-id="2e466-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="2e466-108">På siden **Kreditorposter** skal du vælge **Handlinger**, **Funktioner** og **Send remitteringsadvis** for at sende mails med remitteringsadvis efter bogføring af kreditorbetalinger for én eller flere kreditorposter</span><span class="sxs-lookup"><span data-stu-id="2e466-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="2e466-109">Se også</span><span class="sxs-lookup"><span data-stu-id="2e466-109">See Also</span></span>

[<span data-ttu-id="2e466-110">Lav forslag</span><span class="sxs-lookup"><span data-stu-id="2e466-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="2e466-111">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="2e466-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="2e466-112">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e466-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2e466-113">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="2e466-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]