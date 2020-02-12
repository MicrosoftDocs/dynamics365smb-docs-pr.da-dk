---
title: Overvågning af ændringer | Microsoft Docs
description: Du kan aktivere en brugerlog for at få en oversigt over ændringer af data i registrerede tabeller. Du kan også spore aktiviteter med bestemte typer aktivitetslogge.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cffa7d23b7c09561914cc00a8a4b9820ed743c29
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775351"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="16d54-104">Ændringer af revision i Business Central</span><span class="sxs-lookup"><span data-stu-id="16d54-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="16d54-105">Du kan aktivere ændringsloggen i [!INCLUDE[d365fin](includes/d365fin_md.md)], så du har en oversigt over aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="16d54-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="16d54-106">Loggen er baseret på ændringer, der er foretaget i de tabeller, som du sporer. På siden **Ændringslogposter** registreres posterne i kronologisk rækkefølge og viser de ændringer, der er foretaget i felterne på de angivne tabeller.</span><span class="sxs-lookup"><span data-stu-id="16d54-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="16d54-107">Ændringsloggen indsamler alle ændringer, der foretages i tabellen.</span><span class="sxs-lookup"><span data-stu-id="16d54-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="16d54-108">En brugers ændringer vises ikke i **Ændringslogposter**, før brugerens session startes igen, hvilket sker i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="16d54-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="16d54-109">Sessionen er udløbet og er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="16d54-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="16d54-110">Brugeren har valgt et andet regnskab eller Rollecenter.</span><span class="sxs-lookup"><span data-stu-id="16d54-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="16d54-111">Bruger har logget af og på igen.</span><span class="sxs-lookup"><span data-stu-id="16d54-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="16d54-112">Arbejde med ændringsloggen</span><span class="sxs-lookup"><span data-stu-id="16d54-112">Working with the Change Log</span></span>

<span data-ttu-id="16d54-113">Et almindeligt problem i mange økonomisystemer er at finde årsagen til fejl og ændringer i data.</span><span class="sxs-lookup"><span data-stu-id="16d54-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="16d54-114">Det kan være alt fra et forkert kundetelefonnummer til en forkert postering i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="16d54-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="16d54-115">Du kan bruge funktionaliteten i ændringsloggen til at spore alle direkte modifikationer, som en bruger foretager af data i databasen.</span><span class="sxs-lookup"><span data-stu-id="16d54-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="16d54-116">Du skal for hver tabel og hvert felt angive, hvad der skal registreres i loggen. Derefter skal du aktivere ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="16d54-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="16d54-117">Du aktiverer og deaktiverer ændringsloggen på siden **Opsætning af ændringslog**.</span><span class="sxs-lookup"><span data-stu-id="16d54-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="16d54-118">Når en bruger aktiverer eller deaktiverer ændringsloggen, logføres denne aktivitet, så du altid kan se, hvilken bruger der har deaktiveret eller aktiveret ændringsloggen.</span><span class="sxs-lookup"><span data-stu-id="16d54-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="16d54-119">Hvis du på siden **Opsætning af ændringslog** vælger handlingen **Tabeller**, kan du angive, hvilke tabeller du vil spore ændringer for, og hvilke ændringer du vil spore. [!INCLUDE[d365fin](includes/d365fin_md.md)] sporer også en række systemtabeller.</span><span class="sxs-lookup"><span data-stu-id="16d54-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="16d54-120">Når du har konfigureret ændringsloggen, aktiveret den og ændret data, kan du få vist og filtrere ændringerne på siden **Ændringslogposter**.</span><span class="sxs-lookup"><span data-stu-id="16d54-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="16d54-121">Hvis du vil slette poster, kan du gøre det på siden **Slet ændringslogposter**, hvor du kan angive filtre baseret på datoer og tidspunkter.</span><span class="sxs-lookup"><span data-stu-id="16d54-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="16d54-122">Arbejde med aktivitetslogge</span><span class="sxs-lookup"><span data-stu-id="16d54-122">Working with Activity Logs</span></span>

<span data-ttu-id="16d54-123">Fra nogle sider i [!INCLUDE [prodshort](includes/prodshort.md)] kan du få vist en aktivitetslog, der viser status og eventuelle fejl i filer, som du eksporterer fra eller importerer til [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="16d54-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="16d54-124">Oplysningerne vises på siden **Aktivitetslog** i overensstemmelse med den kontekst, de åbnes fra.</span><span class="sxs-lookup"><span data-stu-id="16d54-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="16d54-125">Du kan åbne vinduet fra siderne **Opsætning af dokumentudvekslingstjeneste**, **Indgående bilag**, **Bogført salgsfaktura** og **Bogført salgskreditnota**.</span><span class="sxs-lookup"><span data-stu-id="16d54-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="16d54-126">Du kan tømme listen med logposter eller blot rydde oversigten over poster, der er ældre end 7 dage.</span><span class="sxs-lookup"><span data-stu-id="16d54-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="16d54-127">Se også</span><span class="sxs-lookup"><span data-stu-id="16d54-127">See Also</span></span>
[<span data-ttu-id="16d54-128">Ændre grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="16d54-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="16d54-129">Sortering</span><span class="sxs-lookup"><span data-stu-id="16d54-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="16d54-130">Søge efter sider og oplysninger med Fortæl mig</span><span class="sxs-lookup"><span data-stu-id="16d54-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="16d54-131">[Tildele tilladelser til brugere og grupper](ui-define-granular-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="16d54-131">[Assign Permissions to Users and Groups](ui-define-granular-permissions.md)  </span></span>  
<span data-ttu-id="16d54-132">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="16d54-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
