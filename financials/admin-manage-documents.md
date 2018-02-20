---
title: Administrere, slette eller komprimere dokumenter | Microsoft Docs
description: Beholde dine historiske data eller slette dem.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 60438f0b6f0d5da60925b5b9c309cc359a8422e3
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="manage-documents"></a><span data-ttu-id="9aee0-103">Administrere dokumenter</span><span class="sxs-lookup"><span data-stu-id="9aee0-103">Manage Documents</span></span>
<span data-ttu-id="9aee0-104">En central rolle, f.eks. som programadministrator, skal regelmæssigt håndtere store mængder akkumulerede oversigtsdokumenter, der skal slettes eller komprimeres.</span><span class="sxs-lookup"><span data-stu-id="9aee0-104">A central role, such as the application administrator, must regularly deal with accumulating historic documents by deleting or compressing them.</span></span>  

## <a name="delete-documents"></a><span data-ttu-id="9aee0-105">Slet dokumenter</span><span class="sxs-lookup"><span data-stu-id="9aee0-105">Delete Documents</span></span>
<span data-ttu-id="9aee0-106">Du kan i visse situationer have behov for at slette fakturaer.</span><span class="sxs-lookup"><span data-stu-id="9aee0-106">In certain situations, you may need to delete invoiced purchase orders that have not been deleted.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="9aee0-107"> kontrollerer, om de slettede købsordrer er fuldt faktureret.</span><span class="sxs-lookup"><span data-stu-id="9aee0-107"> checks that you have fully invoiced the deleted purchase orders.</span></span> <span data-ttu-id="9aee0-108">Du kan kun slette ordrer, hvis de er blevet fuldt faktureret og modtaget.</span><span class="sxs-lookup"><span data-stu-id="9aee0-108">You cannot delete orders that you have not fully invoiced and received.</span></span>  

<span data-ttu-id="9aee0-109">Returvareordrer slettes normalt, når de er faktureret.</span><span class="sxs-lookup"><span data-stu-id="9aee0-109">Return orders are usually deleted after they are invoiced.</span></span> <span data-ttu-id="9aee0-110">Når en faktura bogføres, overføres den til vinduet **Bogført købskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-110">When you post an invoice, it is transferred to the **Posted Purchase Credit Memo** window.</span></span> <span data-ttu-id="9aee0-111">Hvis afkrydsningsfeltet **Returvarekvit. på kreditnota** er markeret i vinduet **Købsopsætning**, overføres fakturaen til vinduet **Bogført returvareleverance**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-111">If you selected the **Return Shipment on Credit Memo** check box in the **Purchases & Payable Setup** window, then the invoice is transferred to the **Posted Return Shipment** window.</span></span> <span data-ttu-id="9aee0-112">Du kan slette dokumenter ved hjælp af kørslen **Slet fakt. købsreturvareordrer**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-112">You can delete the documents using the **Delete Invd Purch. Ret. Orders** batch job.</span></span> <span data-ttu-id="9aee0-113">Før du sletter, kontrollerer kørslen, om købsreturvareordreordrer er fuldt leveret og faktureret.</span><span class="sxs-lookup"><span data-stu-id="9aee0-113">Before deleting, the batch job checks if the purchase return orders are fully shipped and invoiced.</span></span>  

<span data-ttu-id="9aee0-114">Rammekøbsordrer slettes ikke, når du har behandlet og faktureret alle relaterede købsordrer.</span><span class="sxs-lookup"><span data-stu-id="9aee0-114">Blanket purchase orders are not deleted after you have processed and invoiced all the related purchase orders.</span></span> <span data-ttu-id="9aee0-115">Du kan slette rammeordrer med kørslen **Slet fak. rammekøbsordrer**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-115">You can delete blanket orders with the **Delete Invoiced Blanket Purchase Orders** batch job.</span></span>  

<span data-ttu-id="9aee0-116">Fakturerede serviceordrer slettes som regel automatisk, når de er faktureret fuldt ud.</span><span class="sxs-lookup"><span data-stu-id="9aee0-116">Invoiced service orders are usually deleted automatically after having been fully invoiced.</span></span> <span data-ttu-id="9aee0-117">Når en faktura bogføres, oprettes der en tilsvarende post i vinduet **Bogførte servicefakturaer**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-117">When an invoice is posted, a corresponding entry is created in the **Posted Service Invoices** window.</span></span> <span data-ttu-id="9aee0-118">Det bogførte dokument kan ses i vinduet **Bogført servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-118">The posted document can be viewed in the **Posted Service Invoice** window.</span></span>  

<span data-ttu-id="9aee0-119">Serviceordrer slettes ikke automatisk i programmet, men hvis det samlede antal i ordren er bogført, ikke fra selve serviceordren, men fra vinduet **Servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-119">Service orders are not deleted automatically, however, if the total quantity on the order has been posted not from the service order itself, but from the **Service Invoice** window.</span></span> <span data-ttu-id="9aee0-120">Det kan i så fald være nødvendigt at slette fakturerede ordrer, der ikke er slettet.</span><span class="sxs-lookup"><span data-stu-id="9aee0-120">Then you may need to delete invoiced orders that were not deleted.</span></span> <span data-ttu-id="9aee0-121">Det kan du gøre ved at aktivere kørslen **Slet fakturerede serviceordrer**.</span><span class="sxs-lookup"><span data-stu-id="9aee0-121">You can do this by running the **Delete Invoiced Service Orders** batch job.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9aee0-122">Se også</span><span class="sxs-lookup"><span data-stu-id="9aee0-122">See Also</span></span>  
[<span data-ttu-id="9aee0-123">Opsætning og administration i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="9aee0-123">Setup and Administration in Finance and Operations, Business edition</span></span>](admin-setup-and-administration.md)  

