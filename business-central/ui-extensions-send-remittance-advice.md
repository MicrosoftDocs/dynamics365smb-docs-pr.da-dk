---
title: Udvidelsen Send remitteringsadvis | Microsoft Docs
description: Beskriver udvidelsen Send remitteringsadvis, der giver mulighed for at emaile og sende remitteringsadvis igen fra betalingskladden og kreditorposterne.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757063"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="ac524-103">Send remitteringsadvis</span><span class="sxs-lookup"><span data-stu-id="ac524-103">Send Remittance Advice</span></span>

<span data-ttu-id="ac524-104">Når der anvendes remitteringsadvis til at underrette kreditorerne om betalinger, kan du nu sende mails med flere remitteringsadviser fra udbetalingskladden og sende igen, når der er foretaget betalinger fra kreditorposter, ved hjælp af dokumentafsendelsesprofiler.</span><span class="sxs-lookup"><span data-stu-id="ac524-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="ac524-105">Denne funktionalitet understøttes kun i Business Central online og til det lokale miljø i følgende lande: Storbritannien, USA, Canada, Australien, New Zealand og Sydafrika.</span><span class="sxs-lookup"><span data-stu-id="ac524-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="ac524-106">Du kan sende remitteringsadvis på to forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="ac524-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="ac524-107">På siden **Udbetalingskladde** skal du vælge **Relaterede**, **Betalinger**, **Send remitteringsadvis** for at maile remitteringsadvis til en eller flere udbetalingskladdelinjer</span><span class="sxs-lookup"><span data-stu-id="ac524-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="ac524-108">På siden **Kreditorposter** skal du vælge **Handlinger**, **Funktioner** og **Send remitteringsadvis** for at sende mails med remitteringsadvis efter bogføring af kreditorbetalinger for én eller flere kreditorposter</span><span class="sxs-lookup"><span data-stu-id="ac524-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="ac524-109">Se også</span><span class="sxs-lookup"><span data-stu-id="ac524-109">See Also</span></span>

[<span data-ttu-id="ac524-110">Lav forslag</span><span class="sxs-lookup"><span data-stu-id="ac524-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="ac524-111">[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ac524-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="ac524-112">[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ac524-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ac524-113">Sende dokumenter som mail</span><span class="sxs-lookup"><span data-stu-id="ac524-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
