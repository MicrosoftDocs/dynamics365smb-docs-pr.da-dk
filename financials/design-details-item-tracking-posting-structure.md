---
title: "Designdetaljer – Bogføringsstruktur for varesporing | Microsoft Docs"
description: "Få at vide, hvordan du bruger vareposter som den primære bærer af varesporingsnumre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item tracking, posting, inventory
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 72de5863bf2e7c64078a9ca5421202f00f439250
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-item-tracking-posting-structure"></a><span data-ttu-id="912a6-103">Designdetaljer: Bogføringsstruktur for varesporing</span><span class="sxs-lookup"><span data-stu-id="912a6-103">Design Details: Item Tracking Posting Structure</span></span>
<span data-ttu-id="912a6-104">Med henblik på at tilpasse lageromkostningsfunktionalitet og for at opnå en enklere og mere stabil løsning bruges vareposter som den primære bærer af varesporingsnumre.</span><span class="sxs-lookup"><span data-stu-id="912a6-104">To align with inventory costing functionality and to obtain a simpler and more robust solution, item ledger entries are used as the primary carrier of item tracking numbers.</span></span>  
  
<span data-ttu-id="912a6-105">Varesporingsnumre på ordrenetværksenheder og netværksenheder, der ikke er ordrer, er angivet i tabellen **Reservationspost** (T337).</span><span class="sxs-lookup"><span data-stu-id="912a6-105">Item tracking numbers on order network entities and non-order network entities are specified in the **Reservation Entry** table (T337).</span></span> <span data-ttu-id="912a6-106">Varesporingsnumre, der vedrører historiske oplysninger, er hentet direkte fra de vareposter, der vedrører den pågældende transaktion.</span><span class="sxs-lookup"><span data-stu-id="912a6-106">Item tracking numbers that are related to historical information are retrieved directly from the item ledger entries that are related to the transaction in question.</span></span> <span data-ttu-id="912a6-107">Det betyder, at vareposter afspejler varesporingsspecifikation af den bogførte ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="912a6-107">This means that item ledger entries reflect the item tracking specification of the posted order line.</span></span>  
  
<span data-ttu-id="912a6-108">Vinduet **Varesporingslinjer** henter oplysningerne fra T337 og vareposterne og viser dem igennem den midlertidige tabel, **Sporingsspecifikation** (T336).</span><span class="sxs-lookup"><span data-stu-id="912a6-108">The **Item Tracking Lines** window retrieves the information from T337 and the item ledger entries and shows it through the temporary table, **Tracking Specification** (T336).</span></span> <span data-ttu-id="912a6-109">T336 indeholder også midlertidige data i **vinduet Varesporingslinjer** for varesporingsantal, der mangler at blive faktureret.</span><span class="sxs-lookup"><span data-stu-id="912a6-109">T336 also hold the temporary data in the **Item Tracking Lines window** for item tracking quantities that remain to be invoiced.</span></span>  
  
## <a name="one-to-many-relation"></a><span data-ttu-id="912a6-110">En til mange-relation</span><span class="sxs-lookup"><span data-stu-id="912a6-110">One-to-Many Relation</span></span>  
<span data-ttu-id="912a6-111">Tabellen **Varepostrelation**, som bruges til at knytte en bogført dokumentlinje til de relaterede vareposter, består af to primære dele:</span><span class="sxs-lookup"><span data-stu-id="912a6-111">The **Item Entry Relation** table, which is used to link a posted document line with its related item ledger entries, consists of two main parts:</span></span>  
  
* <span data-ttu-id="912a6-112">En henvisning til den bogførte dokumentlinje, feltet **Ordrelinjenr.**.</span><span class="sxs-lookup"><span data-stu-id="912a6-112">A pointer to the posted document line, the **Order Line No.**</span></span> <span data-ttu-id="912a6-113">.</span><span class="sxs-lookup"><span data-stu-id="912a6-113">field.</span></span>  
* <span data-ttu-id="912a6-114">Et løbenummer, der peger på en varepost, feltet **Vareløbenr.**.</span><span class="sxs-lookup"><span data-stu-id="912a6-114">An entry number pointing to an item ledger entry, the **Item Entry No.** field.</span></span>  
  
<span data-ttu-id="912a6-115">Funktionaliteten af det eksisterende **Løbenr.**-felt, som vedrører en varepost til en bogført dokumentlinje, håndterer den typiske én til én-relation, når der ikke findes nogen varesporingsnumre på den bogførte bilagslinje.</span><span class="sxs-lookup"><span data-stu-id="912a6-115">The functionality of the existing **Entry No.** field, which relates an item ledger entry to a posted document line, handles the typical one-to-one relation when no item tracking numbers exist on the posted document line.</span></span> <span data-ttu-id="912a6-116">Hvis der findes varesporingsnumre, så er feltet **Løbenr.** tomt, og en-til-mange-relationen håndteres af tabellen **Varepostrelation**.</span><span class="sxs-lookup"><span data-stu-id="912a6-116">If item tracking numbers exist, then the **Entry No.** field is left blank, and the one-to-many relation is handled by the **Item Entry Relation** table.</span></span> <span data-ttu-id="912a6-117">Hvis den bogførte bilagslinje indeholder varesporingsnumre, men kun vedrører en enkelt varepost, vil feltet **Løbenr.** håndtere relationen, og der oprettes ingen post i tabellen **Varepostrelation**.</span><span class="sxs-lookup"><span data-stu-id="912a6-117">If the posted document line carries item tracking numbers but only relates to a single item ledger entry, then the **Entry No.** field handles the relation, and the no record is created in the **Item Entry Relation** table.</span></span>  
  
## <a name="codeunits-80-and-90"></a><span data-ttu-id="912a6-118">Kodeenheder 80 og 90</span><span class="sxs-lookup"><span data-stu-id="912a6-118">Codeunits 80 and 90</span></span>  
<span data-ttu-id="912a6-119">Med henblik på at opdele vareposter ved bogføring indsættes koden i kodeenhed 80 og kodeenhed 90 i løkker, der kører gennem globale, midlertidige postvariabler.</span><span class="sxs-lookup"><span data-stu-id="912a6-119">To split the item ledger entries during posting, the code in codeunit 80 and codeunit 90, is encircled by loops that run through global temporary record variables.</span></span> <span data-ttu-id="912a6-120">Denne kode kalder kodeenhed 22 med en varekladdelinje.</span><span class="sxs-lookup"><span data-stu-id="912a6-120">This code calls codeunit 22 with an item journal line.</span></span> <span data-ttu-id="912a6-121">Disse variabler er initialiseret, når der findes varesporingsnumre for dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="912a6-121">These variables are initialized when item tracking numbers exist for the document line.</span></span> <span data-ttu-id="912a6-122">Denne løkkestruktur bruges altid for at bevare koden enkel.</span><span class="sxs-lookup"><span data-stu-id="912a6-122">To keep the code simple, this looping structure is always used.</span></span> <span data-ttu-id="912a6-123">Hvis der ikke findes varesporingsnumre til bilagslinjen, vil en enkelt post indsættes, og løkken køres kun en gang.</span><span class="sxs-lookup"><span data-stu-id="912a6-123">If no item tracking numbers exist for the document line, then a single record is inserted, and the loop runs only once.</span></span>  
  
## <a name="posting-the-item-journal"></a><span data-ttu-id="912a6-124">Bogføring af varekladden</span><span class="sxs-lookup"><span data-stu-id="912a6-124">Posting the Item Journal</span></span>  
<span data-ttu-id="912a6-125">Varesporingsnumre overføres via reservationsposter, der vedrører en bestemt varepost, og gennemløbet af varesporingsnumre sker i codeunit 22.</span><span class="sxs-lookup"><span data-stu-id="912a6-125">Item tracking numbers are transferred via the reservation entries that relate to the item ledger entry, and the looping through item tracking numbers occurs in codeunit 22.</span></span> <span data-ttu-id="912a6-126">Dette begreb fungerer på samme måde, når en varekladdelinje indirekte bruges til at bogføre et salg eller en indkøbsordre, ligesom når en varekladdelinje bruges direkte.</span><span class="sxs-lookup"><span data-stu-id="912a6-126">This concept works in the same way when an item journal line is used indirectly to post a sale or purchase order as when an item journal line is used directly.</span></span> <span data-ttu-id="912a6-127">Når varekladden bruges direkte, peger feltet **Kilderække-id** på selve varekladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="912a6-127">When the item journal is used directly, the **Source Row ID** field points to the item journal line itself.</span></span>  
  
## <a name="code-unit-22"></a><span data-ttu-id="912a6-128">Kodeenhed 22</span><span class="sxs-lookup"><span data-stu-id="912a6-128">Code Unit 22</span></span>  
<span data-ttu-id="912a6-129">Kodeenheder 80 og 90 gentager kaldet fra kodenhed 22 under fakturabogføring af varesporingsnumre og under fakturering af eksisterende leverancer eller modtagelser.</span><span class="sxs-lookup"><span data-stu-id="912a6-129">Codeunits 80 and 90 loop the call of codeunit 22 during the invoice posting of item tracking numbers and during the invoicing of existing shipments or receipts.</span></span>  
  
<span data-ttu-id="912a6-130">Under antalsbogføring af varesporingsnumre, henter kodeenhed 22 varesporingsnumre fra posterne i T337, der vedrører bogføringen.</span><span class="sxs-lookup"><span data-stu-id="912a6-130">During quantity posting of item tracking numbers, codeunit 22 retrieves item tracking numbers from the entries in T337 that relate to the posting.</span></span> <span data-ttu-id="912a6-131">Disse poster placeres direkte på varekladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="912a6-131">These entries are placed directly on the item journal line.</span></span>  
  
<span data-ttu-id="912a6-132">Kodeenhed 22 gentages via varesporingsnumrene og opdeler bogføringen i de respektive vareposter, der har varesporingsnumrene.</span><span class="sxs-lookup"><span data-stu-id="912a6-132">Codeunit 22 loops through the item tracking numbers and splits the posting into the respective item ledger entries that carry the item tracking numbers.</span></span> <span data-ttu-id="912a6-133">Oplysninger om, hvilke vareposter der oprettes returneres til T337 ved hjælp af en midlertidig T336 post, der kaldes af en procedure i codeunit 22.</span><span class="sxs-lookup"><span data-stu-id="912a6-133">Information about which item ledger entries are created is returned to T337 by using a temporary T336 record, which is called by a procedure in codeunit 22.</span></span> <span data-ttu-id="912a6-134">Denne procedure udløses, når kodeenhed 22 har afsluttet kørslen, da kodeenhed 22-objektet på dette tidspunkt indeholder oplysninger.</span><span class="sxs-lookup"><span data-stu-id="912a6-134">This procedure is triggered when codeunit 22 has finished its run because at that point, the codeunit 22 object contains the information.</span></span> <span data-ttu-id="912a6-135">Når den midlertidige T336-post er hentet, opretter kodeenhederne 80 og 90 poster i tabellen **Varepostrelation** for at knytte de oprettede vareposter til den oprettede leverance- eller modtagelseslinje.</span><span class="sxs-lookup"><span data-stu-id="912a6-135">When the temporary T336 record is retrieved, codeunits 80 and 90 create records in the **Item Entry Relation** table to link the created item ledger entries to the created shipment or receipt line.</span></span> <span data-ttu-id="912a6-136">Kodeenhed 80 eller kodeenhed 90 konverterer derefter de midlertidige T336-poster til reelle T336-poster, der er relateret til den pågældende linje.</span><span class="sxs-lookup"><span data-stu-id="912a6-136">Codeunits 80 or codeunit 90 then converts the temporary T336 records to real T336 records that are related to the line in question.</span></span> <span data-ttu-id="912a6-137">Men konverteringen sker kun, hvis den bogførte bilagslinje ikke er slettet, fordi den er kun delvist bogført.</span><span class="sxs-lookup"><span data-stu-id="912a6-137">However, this conversion occurs only if the posted document line is not deleted, because it is only partially posted.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="912a6-138">Se også</span><span class="sxs-lookup"><span data-stu-id="912a6-138">See Also</span></span>  
<span data-ttu-id="912a6-139">[Designoplysninger: Varesporing](design-details-item-tracking.md) </span><span class="sxs-lookup"><span data-stu-id="912a6-139">[Design Details: Item Tracking](design-details-item-tracking.md) </span></span>  
[<span data-ttu-id="912a6-140">Designoplysninger: Design af varesporing</span><span class="sxs-lookup"><span data-stu-id="912a6-140">Design Details: Item Tracking Design</span></span>](design-details-item-tracking-design.md)