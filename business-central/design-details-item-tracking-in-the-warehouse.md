---
title: "Designoplysninger – Tilgængelighed af varesporing | Microsoft Docs"
description: "Dette emne beskriver, hvordan du sikrer dig, at de personer, der behandler ordrer, kan stole på tilgængeligheden af serie- eller lotnumre."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, serial number, lot number, outbound documents
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: fcdfc219f94462048474acdef259f671e1c8a402
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="design-details-item-tracking-availability"></a><span data-ttu-id="220f9-103">Designoplysninger: Tilgængelighed af varesporing</span><span class="sxs-lookup"><span data-stu-id="220f9-103">Design Details: Item Tracking Availability</span></span>
<span data-ttu-id="220f9-104">Siderne **Varesporingslinjer** og **Varesporingsoversigt** indeholder dynamiske disponeringsoplysninger for serie- eller lotnumre.</span><span class="sxs-lookup"><span data-stu-id="220f9-104">The **Item Tracking Lines** and **Item Tracking Summary** pages provide dynamic availability information for serial or lot numbers.</span></span> <span data-ttu-id="220f9-105">Formålet med dette er at øge gennemsigtigheden for brugere på udgående dokumenter, f.eks. salgsordrer, ved at vise dem, hvilke serienumre eller hvor mange enheder af et lotnummer, der aktuelt er tildelt på andre åbne dokumenter.</span><span class="sxs-lookup"><span data-stu-id="220f9-105">The purpose of this is to increase transparency for users on outbound documents, such as sales orders, by showing them which serial numbers or how many units of a lot number are currently assigned on other open documents.</span></span> <span data-ttu-id="220f9-106">Dette mindsker usikkerhed, der er forårsaget af dobbelt allokering, og giver ordrebehandlere tillid til, at varesporingsnumre og datoer, som de lover på ikke-bogførte salgsordre, kan opfyldes.</span><span class="sxs-lookup"><span data-stu-id="220f9-106">This reduces uncertainty that is caused by double allocation and instills confidence in order processors that the item tracking numbers and dates that they are promising on unposted sales orders can be fulfilled.</span></span> <span data-ttu-id="220f9-107">Du kan finde flere oplysninger i [Designoplysninger: Siden Varesporingslinjer](design-details-item-tracking-lines-window.md).</span><span class="sxs-lookup"><span data-stu-id="220f9-107">For more information, see [Design Details: Item Tracking Lines Page](design-details-item-tracking-lines-window.md).</span></span>  

<span data-ttu-id="220f9-108">Når du åbner siden **Varesporingslinjer**, hentes der tilgængelighedsdata fra tabellen **Varepost** og tabellen **Reservationspost** uden datofilter.</span><span class="sxs-lookup"><span data-stu-id="220f9-108">When you open the **Item Tracking Lines** page, availability data is retrieved from the **Item Ledger Entry** table and the **Reservation Entry** table, with no date filter.</span></span> <span data-ttu-id="220f9-109">Når du vælger feltet **Serienr.** eller feltet **Lotnr.**, åbnes siden **Varesporingsoversigt** og viser en oversigt over varesporingsoplysninger i tabellen **Reservationspost**.</span><span class="sxs-lookup"><span data-stu-id="220f9-109">When you choose the **Serial No.** field or the **Lot No.** field, the **Item Tracking Summary** page opens and shows a summary of the item tracking information in the **Reservation Entry** table.</span></span> <span data-ttu-id="220f9-110">Oversigten indeholder følgende oplysninger om hvert serie- eller lotnummer på varesporingslinjen:</span><span class="sxs-lookup"><span data-stu-id="220f9-110">The summary contains the following information about each serial or lot number on the item tracking line:</span></span>  

|<span data-ttu-id="220f9-111">Felt</span><span class="sxs-lookup"><span data-stu-id="220f9-111">Field</span></span>|<span data-ttu-id="220f9-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="220f9-112">Description</span></span>|  
|---------------------------------|---------------------------------------|  
|<span data-ttu-id="220f9-113">**I alt**</span><span class="sxs-lookup"><span data-stu-id="220f9-113">**Total Quantity**</span></span>|<span data-ttu-id="220f9-114">Det samlede antal af serie- eller lotnumre, der aktuelt er på lager.</span><span class="sxs-lookup"><span data-stu-id="220f9-114">The total quantity of the serial or lot number that is currently in inventory.</span></span>|  
|<span data-ttu-id="220f9-115">**Ønsket antal i alt**</span><span class="sxs-lookup"><span data-stu-id="220f9-115">**Total Requested Quantity**</span></span>|<span data-ttu-id="220f9-116">Det samlede antal af serie- og lotnumre, der aktuelt er anmodet om i alle dokumenter.</span><span class="sxs-lookup"><span data-stu-id="220f9-116">The total quantity of the serial or lot number that is currently requested in all documents.</span></span>|  
|<span data-ttu-id="220f9-117">**Aktuelt ventende antal**</span><span class="sxs-lookup"><span data-stu-id="220f9-117">**Current Pending Quantity**</span></span>|<span data-ttu-id="220f9-118">Det antal, der angives i den aktuelle forekomst af siden **Varesporingslinjer**, men som endnu ikke er overført til databasen.</span><span class="sxs-lookup"><span data-stu-id="220f9-118">The quantity that is entered in the current instance of the **Item Tracking Lines** page but is not yet committed to the database.</span></span>|  
|<span data-ttu-id="220f9-119">**Beholdning i alt**</span><span class="sxs-lookup"><span data-stu-id="220f9-119">**Total Available Quantity**</span></span>|<span data-ttu-id="220f9-120">Antallet af serie- eller lotnumre, som brugeren kan anmode om.</span><span class="sxs-lookup"><span data-stu-id="220f9-120">The quantity of the serial or lot number that is available for the user to request.</span></span><br /><br /> <span data-ttu-id="220f9-121">Dette antal beregnes ud fra andre felter på siden på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="220f9-121">This quantity is calculated from other fields on the page as follows:</span></span><br /><br /> <span data-ttu-id="220f9-122">aktuelt antal – (anmodet antal i alt + aktuelt ventende antal).</span><span class="sxs-lookup"><span data-stu-id="220f9-122">total quantity – (total requested quantity + current pending quantity).</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="220f9-123">Du kan også se oplysningerne i den foregående tabel ved hjælp af funktionen **Marker poster** på siden **Varesporingslinjer**.</span><span class="sxs-lookup"><span data-stu-id="220f9-123">You can also see the information in the preceding table by using the **Select Entries** function on the **Item Tracking Lines** page.</span></span>  

<span data-ttu-id="220f9-124">Hvis du vil bevare databasens ydeevne, hentes tilgængelighedsdata kun én gang fra databasen, når du åbner siden **Varesporingslinjer** og bruger funktionen **Opdater disponering** på siden.</span><span class="sxs-lookup"><span data-stu-id="220f9-124">To preserve database performance, availability data is only retrieved once from the database when you open the **Item Tracking Lines** page and use the **Refresh Availability** function on the page.</span></span>  

## <a name="calculation-formula"></a><span data-ttu-id="220f9-125">Beregningsformel</span><span class="sxs-lookup"><span data-stu-id="220f9-125">Calculation Formula</span></span>  
<span data-ttu-id="220f9-126">Som beskrevet i foregående tabel beregnes tilgængeligheden af et bestemt serienummer eller lotnummer på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="220f9-126">As described in the preceding table, the availability of a given serial or lot number is calculated as follows:</span></span>  

* <span data-ttu-id="220f9-127">beholdning i alt = antal på lager – (alle behov + antal, der endnu ikke er disponeret i databasen)</span><span class="sxs-lookup"><span data-stu-id="220f9-127">total available quantity = quantity in inventory – (all demands + quantity not yet committed to the database)</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="220f9-128">Denne formel angiver, at disponeringsberegningen for serie- eller lotnummer kun tager lagerbeholdningen i betragtning og ignorerer forventede modtagelser.</span><span class="sxs-lookup"><span data-stu-id="220f9-128">This formula implies that the serial or lot number availability calculation considers only inventory and ignores projected receipts.</span></span> <span data-ttu-id="220f9-129">Forsyning, der endnu ikke er bogført til lageret, påvirker derfor ikke tilgængelighed i forbindelse med varesporing, i modsætning til almindelig varedisponering, hvor forventede tilgange er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="220f9-129">Accordingly, supply that is not yet posted to inventory does not affect item tracking availability, as opposed to regular item availability where projected receipts are included.</span></span>  

## <a name="see-also"></a><span data-ttu-id="220f9-130">Se også</span><span class="sxs-lookup"><span data-stu-id="220f9-130">See Also</span></span>  
[<span data-ttu-id="220f9-131">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="220f9-131">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)

