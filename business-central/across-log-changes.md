---
title: "Spore brugeraktivitet i en ændringslog | Microsoft Docs"
description: "Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 59afb06e9d43bdadc5ceacf563a9e6faf7439b7b
ms.openlocfilehash: bc56e07a540c24f53b88651ad2b2ff5e1e56a571
ms.contentlocale: da-dk
ms.lasthandoff: 12/05/2018

---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="f089e-103">Ændringer af revision i Business Central</span><span class="sxs-lookup"><span data-stu-id="f089e-103">Auditing Changes in Business Central</span></span>

<span data-ttu-id="f089e-104">Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f089e-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="f089e-105">Loggen er baseret på ændringer, der er foretaget i de tabeller, som du sporer. På siden **Ændringslogposter** registreres posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller.</span><span class="sxs-lookup"><span data-stu-id="f089e-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="f089e-106">Ændringsloggen indsamler alle ændringer, der foretages i tabellen.</span><span class="sxs-lookup"><span data-stu-id="f089e-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="f089e-107">En brugers ændringer vises ikke i **Ændringslogposter**, før brugerens session startes igen, hvilket sker i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="f089e-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="f089e-108">Sessionen er udløbet og er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="f089e-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="f089e-109">Brugeren har valgt et andet regnskab eller Rollecenter.</span><span class="sxs-lookup"><span data-stu-id="f089e-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="f089e-110">Bruger har logget af og på igen.</span><span class="sxs-lookup"><span data-stu-id="f089e-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="f089e-111">Arbejde med ændringsloggen</span><span class="sxs-lookup"><span data-stu-id="f089e-111">Working with the Change Log</span></span>

<span data-ttu-id="f089e-112">Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data.</span><span class="sxs-lookup"><span data-stu-id="f089e-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="f089e-113">Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="f089e-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="f089e-114">Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen.</span><span class="sxs-lookup"><span data-stu-id="f089e-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="f089e-115">Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="f089e-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="f089e-116">Du aktiverer og deaktiverer ændringsloggen på siden **Opsætning af ændringslog**.</span><span class="sxs-lookup"><span data-stu-id="f089e-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="f089e-117">Når en bruger aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="f089e-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="f089e-118">Hvis du på siden **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også en række systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="f089e-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="f089e-119">Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne på siden **Ændringslogposter**.</span><span class="sxs-lookup"><span data-stu-id="f089e-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="f089e-120">Hvis du vil slette poster, kan du gøre det på siden **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="f089e-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f089e-121">Se også</span><span class="sxs-lookup"><span data-stu-id="f089e-121">See Also</span></span>
[<span data-ttu-id="f089e-122">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="f089e-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="f089e-123">Sortering</span><span class="sxs-lookup"><span data-stu-id="f089e-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="f089e-124">Brug af Søg efter side eller rapport</span><span class="sxs-lookup"><span data-stu-id="f089e-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="f089e-125">[Administrere brugere og deres rettigheder](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="f089e-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="f089e-126">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f089e-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

