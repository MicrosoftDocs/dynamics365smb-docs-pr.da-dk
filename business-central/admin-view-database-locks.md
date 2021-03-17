---
title: Se databaselåse
description: Få mere at vide om, hvordan du kan få vist oplysninger om databaselåse direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 640608b810f3ad9812decc493ad4e35bcc316f98
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388145"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="6d4cd-103">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6d4cd-103">Viewing Database Locks</span></span>

<span data-ttu-id="6d4cd-104">Låsning af databaser styrer adgangen for flere brugere til de samme data på samme tid.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="6d4cd-105">Hvis du vil beskytte en transaktion mod andre transaktioner, der ændrer de samme data, medfører den første transaktion en låsning af dataene.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="6d4cd-106">Låsen forbliver aktiv, indtil transaktionen er udført.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="6d4cd-107">Brugere kan forhindres i at fuldføre transaktioner på de låste data.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="6d4cd-108">De vil typisk se en meddelelse, der angiver låsetilstanden.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="6d4cd-109">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6d4cd-109">To view database locks</span></span>

<span data-ttu-id="6d4cd-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Databaselåse**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="6d4cd-111">Siden **Databaselåse** viser et øjebliksbillede af alle aktuelle databaselåse.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="6d4cd-112">Få flere oplysninger om låsning af databaser i [Overvågning af databaselåsninger](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjælp til Business Central-udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="6d4cd-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d4cd-113">Se også</span><span class="sxs-lookup"><span data-stu-id="6d4cd-113">See Also</span></span>

[<span data-ttu-id="6d4cd-114">Overvåg låsninger af databaser</span><span class="sxs-lookup"><span data-stu-id="6d4cd-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 


[!INCLUDE[footer-include](includes/footer-banner.md)]