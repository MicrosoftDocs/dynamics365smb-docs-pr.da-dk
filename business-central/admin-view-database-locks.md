---
title: Se databaselåse
description: Få mere at vide om, hvordan du kan få vist oplysninger om databaselåse direkte fra klientgrænsefladen i Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922313"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="6d1f4-103">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6d1f4-103">Viewing Database Locks</span></span>

<span data-ttu-id="6d1f4-104">Låsning af databaser styrer adgangen for flere brugere til de samme data på samme tid.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="6d1f4-105">Hvis du vil beskytte en transaktion mod andre transaktioner, der ændrer de samme data, medfører den første transaktion en låsning af dataene.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="6d1f4-106">Låsen forbliver aktiv, indtil transaktionen er udført.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="6d1f4-107">Brugere kan forhindres i at fuldføre transaktioner på de låste data.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="6d1f4-108">De vil typisk se en meddelelse, der angiver låsetilstanden.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="6d1f4-109">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6d1f4-109">To view database locks</span></span>

<span data-ttu-id="6d1f4-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Databaselåse**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="6d1f4-111">Siden **Databaselåse** viser et øjebliksbillede af alle aktuelle databaselåse.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="6d1f4-112">Få flere oplysninger om låsning af databaser i [Overvågning af databaselåsninger](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) i hjælp til Business Central-udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="6d1f4-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="6d1f4-113">Se også</span><span class="sxs-lookup"><span data-stu-id="6d1f4-113">See Also</span></span>

[<span data-ttu-id="6d1f4-114">Overvåg låsninger af databaser</span><span class="sxs-lookup"><span data-stu-id="6d1f4-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
