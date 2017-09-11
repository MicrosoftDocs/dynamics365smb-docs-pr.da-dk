---
title: "Spore brugeraktivitet i en ændringslog | Microsoft Docs"
Description: "Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c27c63ae26f2f97dd15d31978b967f6a08dd55b7
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2017


---
# <a name="logging-changes-in-dynamics-365-for-financials"></a><span data-ttu-id="b8084-103">Logføring af ændringer i Dynamics 365 for Financials</span><span class="sxs-lookup"><span data-stu-id="b8084-103">Logging Changes in Dynamics 365 for Financials</span></span>
<span data-ttu-id="b8084-104">Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b8084-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="b8084-105">Loggen er baseret på ændringer, der foretages i data i de tabeller, du sporer.</span><span class="sxs-lookup"><span data-stu-id="b8084-105">The log is based on changes that are made to data in the tables that you track.</span></span> <span data-ttu-id="b8084-106">I ændringsloggen står posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller.</span><span class="sxs-lookup"><span data-stu-id="b8084-106">In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="b8084-107">Ændringsloggen indsamler alle ændringer, der foretages i tabellen.</span><span class="sxs-lookup"><span data-stu-id="b8084-107">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="b8084-108">Arbejde med ændringsloggen</span><span class="sxs-lookup"><span data-stu-id="b8084-108">Working with the change log</span></span>
<span data-ttu-id="b8084-109">Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data.</span><span class="sxs-lookup"><span data-stu-id="b8084-109">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="b8084-110">Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="b8084-110">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="b8084-111">Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen.</span><span class="sxs-lookup"><span data-stu-id="b8084-111">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="b8084-112">Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="b8084-112">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="b8084-113">Du aktiverer og deaktiverer ændringsloggen i vinduet **Opsætning af ændringslog**.</span><span class="sxs-lookup"><span data-stu-id="b8084-113">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="b8084-114">Når du aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="b8084-114">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="b8084-115">Denne funktion kan ikke deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="b8084-115">This cannot be turned off.</span></span>  

<span data-ttu-id="b8084-116">Hvis du i vinduet **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore.</span><span class="sxs-lookup"><span data-stu-id="b8084-116">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="b8084-117"> registrerer også en række systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="b8084-117"> also tracks a number of system tables.</span></span>

<span data-ttu-id="b8084-118">Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne i vinduet **Ændringslogposter**.</span><span class="sxs-lookup"><span data-stu-id="b8084-118">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="b8084-119">Hvis du vil slette poster, kan du gøre det i vinduet **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="b8084-119">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b8084-120">Se også</span><span class="sxs-lookup"><span data-stu-id="b8084-120">See Also</span></span>
[<span data-ttu-id="b8084-121">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="b8084-121">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="b8084-122">Sortering</span><span class="sxs-lookup"><span data-stu-id="b8084-122">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="b8084-123">Brug af Søg efter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="b8084-123">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="b8084-124">[Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="b8084-124">[How to: Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="b8084-125">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b8084-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

