---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115926"
---
<span data-ttu-id="56424-101">På købsdokumenter og kladder kan du angive et bilagsnummer, der henviser til kreditorens nummereringssystem.</span><span class="sxs-lookup"><span data-stu-id="56424-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="56424-102">Du kan bruge dette felt til at registrere det nummer, som kreditoren har tildelt ordren, fakturaen eller kreditnotaen.</span><span class="sxs-lookup"><span data-stu-id="56424-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="56424-103">Du kan derefter bruge nummeret, hvis du har brug for at søge efter den bogførte kladdelinje ved hjælp af det eksterne bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="56424-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="56424-104">Feltet **udv. doc. Obligatorisk** på opsætningssiden **Køb og kreditorstyring** angiver, om der skal angives et eksternt bilagsnummer i følgende situationer:</span><span class="sxs-lookup"><span data-stu-id="56424-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="56424-105">I feltet **Kreditors fakturanr.**, **Kreditors ordrenr.**</span><span class="sxs-lookup"><span data-stu-id="56424-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="56424-106">I feltet eller **Kreditors kr.notanr.**</span><span class="sxs-lookup"><span data-stu-id="56424-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="56424-107">Feltet på et købshoved.</span><span class="sxs-lookup"><span data-stu-id="56424-107">field on a purchase header</span></span>

* <span data-ttu-id="56424-108">I feltet **Eksternt bilagsnr.** på en finanskladdelinje, hvor oplysningerne i feltet **Bilagstype** er angivet til *Faktura*, *Kreditnota* eller *Rentenota*, og **Kontotype** er angivet til *Kreditor*.</span><span class="sxs-lookup"><span data-stu-id="56424-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="56424-109">Hvis du markerer afkrydsningsfeltet, vil det ikke være muligt at bogføre en faktura, en kreditnota eller den type finanskladdelinje, der er beskrevet ovenfor, uden et eksternt bilagsnummer.</span><span class="sxs-lookup"><span data-stu-id="56424-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="56424-110">Det eksterne bilagsnummer indgår i bogførte dokumenter, hvor du kan søge efter det relevante nummer.</span><span class="sxs-lookup"><span data-stu-id="56424-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="56424-111">Du kan også bruge det eksterne bilagsnummer, når du navigerer på kreditorposter.</span><span class="sxs-lookup"><span data-stu-id="56424-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="56424-112">Du kan håndtere eksterne bilagsnumre på en anden måde ved at bruge feltet **Reference**.</span><span class="sxs-lookup"><span data-stu-id="56424-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="56424-113">Hvis du bruger feltet **Reference**, medtages nummeret i bogførte bilag, og du kan søge på den samme måde som for værdier fra feltet **Eksternt bilagsnr.**.</span><span class="sxs-lookup"><span data-stu-id="56424-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="56424-114">Men feltet er ikke tilgængeligt på kladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="56424-114">But the field is not available on journal lines.</span></span>
