---
title: "Spore brugeraktivitet i en ændringslog | Microsoft Docs"
Description: You can activate a user log so that you have a history of any changes made to data in tracked tables.
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
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f49e3722f95d4e5a2c8eea83d77175581d93277
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="logging-changes-in-finance-and-operations-business-edition"></a><span data-ttu-id="7eaba-102">Logføring af ændringer i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="7eaba-102">Logging Changes in Finance and Operations, Business edition</span></span> 
<span data-ttu-id="7eaba-103">Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="7eaba-103">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="7eaba-104">Loggen er baseret på ændringer, der er foretaget i de tabeller, som du sporer. I ændringsloggen registreres posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller.</span><span class="sxs-lookup"><span data-stu-id="7eaba-104">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="7eaba-105">Ændringsloggen indsamler alle ændringer, der foretages i tabellen.</span><span class="sxs-lookup"><span data-stu-id="7eaba-105">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="7eaba-106">Arbejde med ændringsloggen</span><span class="sxs-lookup"><span data-stu-id="7eaba-106">Working with the Change Log</span></span>
<span data-ttu-id="7eaba-107">Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data.</span><span class="sxs-lookup"><span data-stu-id="7eaba-107">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="7eaba-108">Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="7eaba-108">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="7eaba-109">Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen.</span><span class="sxs-lookup"><span data-stu-id="7eaba-109">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="7eaba-110">Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="7eaba-110">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="7eaba-111">Du aktiverer og deaktiverer ændringsloggen i vinduet **Opsætning af ændringslog**.</span><span class="sxs-lookup"><span data-stu-id="7eaba-111">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="7eaba-112">Når du aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="7eaba-112">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="7eaba-113">Denne funktion kan ikke deaktiveres.</span><span class="sxs-lookup"><span data-stu-id="7eaba-113">This cannot be turned off.</span></span>  

<span data-ttu-id="7eaba-114">Hvis du i vinduet **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også en række systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="7eaba-114">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="7eaba-115">Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne i vinduet **Ændringslogposter**.</span><span class="sxs-lookup"><span data-stu-id="7eaba-115">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="7eaba-116">Hvis du vil slette poster, kan du gøre det i vinduet **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="7eaba-116">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7eaba-117">Se også</span><span class="sxs-lookup"><span data-stu-id="7eaba-117">See Also</span></span>
[<span data-ttu-id="7eaba-118">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="7eaba-118">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="7eaba-119">Sortering</span><span class="sxs-lookup"><span data-stu-id="7eaba-119">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="7eaba-120">Brug af Søg efter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="7eaba-120">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="7eaba-121">[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="7eaba-121">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="7eaba-122">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7eaba-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

