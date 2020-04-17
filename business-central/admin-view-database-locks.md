---
title: Se databaselåse
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196372"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="6c525-102">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6c525-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="6c525-103">Om låse</span><span class="sxs-lookup"><span data-stu-id="6c525-103">About Locks</span></span>

<span data-ttu-id="6c525-104">Låsning af databaser styrer adgangen for flere brugere til de samme data på samme tid.</span><span class="sxs-lookup"><span data-stu-id="6c525-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="6c525-105">Hvis du vil beskytte en transaktion mod andre transaktioner, der ændrer de samme data, medfører den første transaktion en låsning af dataene.</span><span class="sxs-lookup"><span data-stu-id="6c525-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="6c525-106">Låsen forbliver aktiv, indtil transaktionen er udført.</span><span class="sxs-lookup"><span data-stu-id="6c525-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="6c525-107">Brugere kan forhindres i at fuldføre transaktioner på de låste data.</span><span class="sxs-lookup"><span data-stu-id="6c525-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="6c525-108">De vil typisk se en meddelelse, der angiver låsetilstanden.</span><span class="sxs-lookup"><span data-stu-id="6c525-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="6c525-109">Sådan ser du databaselåse</span><span class="sxs-lookup"><span data-stu-id="6c525-109">To view database locks</span></span>

<span data-ttu-id="6c525-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Databaselåse**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="6c525-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="6c525-111">Siden **Databaselåse** viser et øjebliksbillede af alle aktuelle databaselåse.</span><span class="sxs-lookup"><span data-stu-id="6c525-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="6c525-112">Få flere oplysninger om låsning af databaser i [Overvågning af databaselåsninger](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) i hjælp til Business Central-udviklere og it-eksperter.</span><span class="sxs-lookup"><span data-stu-id="6c525-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c525-113">Se også</span><span class="sxs-lookup"><span data-stu-id="6c525-113">See Also</span></span>

[<span data-ttu-id="6c525-114">Overvåg låsninger af databaser</span><span class="sxs-lookup"><span data-stu-id="6c525-114">Monitor Database Locks</span></span>](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
