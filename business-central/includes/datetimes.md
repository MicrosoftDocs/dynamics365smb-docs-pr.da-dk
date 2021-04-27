---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 7ead218d289668d893a659f730a4c64e31195f10
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788515"
---
<span data-ttu-id="3ac72-101">Når du angiver dato/klokkeslæt, som en dato og klokkeslæt kombineret i ét felt, skal du angive et mellemrum mellem datoen og klokkeslættet.</span><span class="sxs-lookup"><span data-stu-id="3ac72-101">When you enter datetimes, which are a date and time combined into one field, you must enter a space between the date and the time.</span></span> <span data-ttu-id="3ac72-102">Datodelen kan kun indeholde mellemrum i form af officielle datoseparatorer af indstillingerne for land/område.</span><span class="sxs-lookup"><span data-stu-id="3ac72-102">The date part can only contain spaces in the form of the official date separator of your region settings.</span></span> <span data-ttu-id="3ac72-103">Tidsangivelsen, der kan indeholde mellemrum omkring AM/PM-symbolet i de relevante indstillinger for området.</span><span class="sxs-lookup"><span data-stu-id="3ac72-103">The time can contain spaces around the AM/PM indicator in relevant regional settings.</span></span>

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

<span data-ttu-id="3ac72-104">I den følgende tabel kan du se, hvordan du kan skrive dato og klokkeslæt, og hvordan de fortolkes.</span><span class="sxs-lookup"><span data-stu-id="3ac72-104">The following table lists the various ways in which you can enter datetimes and how they're interpreted.</span></span>  

|<span data-ttu-id="3ac72-105">Post</span><span class="sxs-lookup"><span data-stu-id="3ac72-105">Entry</span></span>|<span data-ttu-id="3ac72-106">Fortolkning</span><span class="sxs-lookup"><span data-stu-id="3ac72-106">Interpretation</span></span>|
|---------------|------------------------|
|<span data-ttu-id="3ac72-107">08-01-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="3ac72-107">08-01-2022 05:48:12 PM</span></span>|<span data-ttu-id="3ac72-108">08\-01\-2022 05:48:12 PM</span><span class="sxs-lookup"><span data-stu-id="3ac72-108">08\-01\-2022 05:48:12 PM</span></span>|
|<span data-ttu-id="3ac72-109">131222 132455</span><span class="sxs-lookup"><span data-stu-id="3ac72-109">131222 132455</span></span>|<span data-ttu-id="3ac72-110">13-12-22 13:24:55</span><span class="sxs-lookup"><span data-stu-id="3ac72-110">13-12-22 13:24:55</span></span>|
|<span data-ttu-id="3ac72-111">1-12-22 10</span><span class="sxs-lookup"><span data-stu-id="3ac72-111">1-12-22 10</span></span>|<span data-ttu-id="3ac72-112">01-12-22 10:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-112">01-12-22 10:00:00</span></span>|
|<span data-ttu-id="3ac72-113">1.12.22 5</span><span class="sxs-lookup"><span data-stu-id="3ac72-113">1.12.22 5</span></span>|<span data-ttu-id="3ac72-114">01-12-22 05:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-114">01-12-22 05:00:00</span></span>|
|<span data-ttu-id="3ac72-115">1.12.22</span><span class="sxs-lookup"><span data-stu-id="3ac72-115">1.12.22</span></span>|<span data-ttu-id="3ac72-116">01-12-22 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-116">01-12-22 00:00:00</span></span>|
|<span data-ttu-id="3ac72-117">11 12</span><span class="sxs-lookup"><span data-stu-id="3ac72-117">11 12</span></span>|<span data-ttu-id="3ac72-118">11-løbende måned-løbende år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-118">11-current month-current year 12:00:00</span></span>|
|<span data-ttu-id="3ac72-119">1112 12</span><span class="sxs-lookup"><span data-stu-id="3ac72-119">1112 12</span></span>|<span data-ttu-id="3ac72-120">11-12-aktuelt år 12:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-120">11-12-current year 12:00:00</span></span>|
|<span data-ttu-id="3ac72-121">d eller dags dato</span><span class="sxs-lookup"><span data-stu-id="3ac72-121">t or today</span></span>|<span data-ttu-id="3ac72-122">dags dato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-122">today's date 00:00:00</span></span>|
|<span data-ttu-id="3ac72-123">d tid</span><span class="sxs-lookup"><span data-stu-id="3ac72-123">t time</span></span>|<span data-ttu-id="3ac72-124">dags dato aktuelt klokkeslæt</span><span class="sxs-lookup"><span data-stu-id="3ac72-124">today's date actual time</span></span>|
|<span data-ttu-id="3ac72-125">d 10:30</span><span class="sxs-lookup"><span data-stu-id="3ac72-125">t 10:30</span></span>|<span data-ttu-id="3ac72-126">dags dato 10:30:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-126">today's date 10:30:00</span></span>|
|<span data-ttu-id="3ac72-127">d 3:3:3</span><span class="sxs-lookup"><span data-stu-id="3ac72-127">t 3:3:3</span></span>|<span data-ttu-id="3ac72-128">dags dato 03:03:03</span><span class="sxs-lookup"><span data-stu-id="3ac72-128">today's date 03:03:03</span></span>|
|<span data-ttu-id="3ac72-129">a eller arbejdsdato</span><span class="sxs-lookup"><span data-stu-id="3ac72-129">w or workdate</span></span>|<span data-ttu-id="3ac72-130">arbejdsdato 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-130">the working date 00:00:00</span></span>|
|<span data-ttu-id="3ac72-131">m eller mandag</span><span class="sxs-lookup"><span data-stu-id="3ac72-131">m or Monday</span></span>|<span data-ttu-id="3ac72-132">Mandag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-132">Monday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-133">ti eller tirsdag</span><span class="sxs-lookup"><span data-stu-id="3ac72-133">tu or Tuesday</span></span>|<span data-ttu-id="3ac72-134">Tirsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-134">Tuesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-135">on eller onsdag</span><span class="sxs-lookup"><span data-stu-id="3ac72-135">we or Wednesday</span></span>|<span data-ttu-id="3ac72-136">Onsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-136">Wednesday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-137">to eller torsdag</span><span class="sxs-lookup"><span data-stu-id="3ac72-137">th or Thursday</span></span>|<span data-ttu-id="3ac72-138">Torsdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-138">Thursday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-139">f eller fredag</span><span class="sxs-lookup"><span data-stu-id="3ac72-139">f or Friday</span></span>|<span data-ttu-id="3ac72-140">Fredag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-140">Friday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-141">l eller lørdag</span><span class="sxs-lookup"><span data-stu-id="3ac72-141">s or Saturday</span></span>|<span data-ttu-id="3ac72-142">Lørdag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-142">Saturday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-143">s eller søndag</span><span class="sxs-lookup"><span data-stu-id="3ac72-143">su or Sunday</span></span>|<span data-ttu-id="3ac72-144">Søndag i den aktuelle uge 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-144">Sunday of the current week 00:00:00</span></span>|
|<span data-ttu-id="3ac72-145">ti 10:30</span><span class="sxs-lookup"><span data-stu-id="3ac72-145">tu 10:30</span></span>|<span data-ttu-id="3ac72-146">Tirsdag i den aktuelle uge 10:30:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-146">Tuesday of the current week 10:30:00</span></span>|
|<span data-ttu-id="3ac72-147">ti 3:3:3</span><span class="sxs-lookup"><span data-stu-id="3ac72-147">tu 3:3:3</span></span>|<span data-ttu-id="3ac72-148">Tirsdag i den aktuelle uge 03:03:03</span><span class="sxs-lookup"><span data-stu-id="3ac72-148">Tuesday of the current week 03:03:03</span></span>|
|<span data-ttu-id="3ac72-149">ti23 t</span><span class="sxs-lookup"><span data-stu-id="3ac72-149">t23 t</span></span>|<span data-ttu-id="3ac72-150">Tirsdag i uge 23 i året for arbejdsdatoen, det aktuelle tidspunkt på dagen</span><span class="sxs-lookup"><span data-stu-id="3ac72-150">Tuesday of week 23 of the work date year, current time of day</span></span>|
|<span data-ttu-id="3ac72-151">ti23</span><span class="sxs-lookup"><span data-stu-id="3ac72-151">t23</span></span>|<span data-ttu-id="3ac72-152">Tirsdag i uge 23 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="3ac72-152">Tuesday of week 23 of the work date year</span></span>|
|<span data-ttu-id="3ac72-153">ti 23</span><span class="sxs-lookup"><span data-stu-id="3ac72-153">t 23</span></span>|<span data-ttu-id="3ac72-154">Dags dato 23:00:00</span><span class="sxs-lookup"><span data-stu-id="3ac72-154">Today 23:00:00</span></span>|
|<span data-ttu-id="3ac72-155">ti-1</span><span class="sxs-lookup"><span data-stu-id="3ac72-155">t-1</span></span>|<span data-ttu-id="3ac72-156">Tirsdag i uge 1 i året for arbejdsdatoen</span><span class="sxs-lookup"><span data-stu-id="3ac72-156">Tuesday of week 1 of the work date year</span></span>|


