---
title: Hvorfor kan jeg ikke tilpasse en side | Microsoft Docs
description: Forklarer, hvorfor du ikke kan tilpasse en side, og hvad du kan gøre for at låse den op, så du kan tilpasse den.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c77664a1013804de13303c8e1d162c437cf5d6e7
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315128"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="ddb63-103">Hvorfor er en side låst mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="ddb63-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="ddb63-104">Der er to forhold, der forhindrer dig i at tilpasse en side.</span><span class="sxs-lookup"><span data-stu-id="ddb63-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="ddb63-105">Enten er siden låst (som angivet af ikonet ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst")), eller den er spærret (som angivet af ikonet ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret")).</span><span class="sxs-lookup"><span data-stu-id="ddb63-105">Either the page is locked (as indicated by the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) icon or it is blocked (as indicated by the ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="ddb63-106">Låst mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="ddb63-106">Locked from Personalizing</span></span>

<span data-ttu-id="ddb63-107">Hvis ikonet ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") findes i banneret **Tilpasning**, når du åbner en side, betyder det, at du i øjeblikket er forhindret i at foretage flere tilpasningsændringer af siden.</span><span class="sxs-lookup"><span data-stu-id="ddb63-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page, this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="ddb63-108">Der kan være to grunde til dette:</span><span class="sxs-lookup"><span data-stu-id="ddb63-108">There can be two reasons for this:</span></span>

1. <span data-ttu-id="ddb63-109">Du har tilpasset siden før, men det er gjort ved hjælp af en tidligere version af produktet.</span><span class="sxs-lookup"><span data-stu-id="ddb63-109">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="ddb63-110">Vi har ændret den måde, hvorpå tilpasning fungerer i baggrunden, siden sidste gang du har tilpasset siden.</span><span class="sxs-lookup"><span data-stu-id="ddb63-110">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="ddb63-111">Desværre arbejder den gamle måde og den nye måde at gøre tingene på ikke sammen.</span><span class="sxs-lookup"><span data-stu-id="ddb63-111">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="ddb63-112">Indtil nu har du kun brugt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til at tilpasse siden.</span><span class="sxs-lookup"><span data-stu-id="ddb63-112">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="ddb63-113">Oplåsning af siden</span><span class="sxs-lookup"><span data-stu-id="ddb63-113">Unlocking the Page</span></span>

<span data-ttu-id="ddb63-114">Hvis du vil låse en side op og fortsætte med at tilpasse den, skal du vælge ikonet ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") og derefter vælge handlingen **Lås op**.</span><span class="sxs-lookup"><span data-stu-id="ddb63-114">If you want to unlock a page and continue personalizing it, choose the ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon, and then choose the **Unlock** action.</span></span>  

<span data-ttu-id="ddb63-115">Før du låser siden op, skal du være opmærksom på følgende:</span><span class="sxs-lookup"><span data-stu-id="ddb63-115">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="ddb63-116">Den aktuelle tilpasning af siden fjernes.</span><span class="sxs-lookup"><span data-stu-id="ddb63-116">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="ddb63-117">Siden vender tilbage til sit oprindelige format, og du skal starte forfra.</span><span class="sxs-lookup"><span data-stu-id="ddb63-117">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="ddb63-118">I feltet [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] forbliver siden, som den er, og bliver ikke påvirket af nye tilpasningsændringer i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="ddb63-118">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="ddb63-119">Fremover vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt adskilt fra hinanden.</span><span class="sxs-lookup"><span data-stu-id="ddb63-119">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="ddb63-120">Spærret mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="ddb63-120">Blocked from Personalizing</span></span>

<span data-ttu-id="ddb63-121">Hvis ikonet ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret") i banneret **Tilpasning**, betyder det, at du er afskåret fra at foretage nogen form for tilpasning af siden.</span><span class="sxs-lookup"><span data-stu-id="ddb63-121">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the **Personalizing** banner, this means that you are blocked from doing any personalization to the page.</span></span>

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked](media/personalization-blocked.png "Personalize lock") -->

<span data-ttu-id="ddb63-122">Det skyldes, at det rollecenter eller den rolle, der aktuelt er knyttet til brugerkontoen, ændrer denne side specifikt til din rolle.</span><span class="sxs-lookup"><span data-stu-id="ddb63-122">The reason for this is that the Role Center or role that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="ddb63-123">Kontakt din administrator for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="ddb63-123">Contact your administrator for assistance.</span></span> <span data-ttu-id="ddb63-124">Du kan også prøve at skifte til et rollecenter, der omfatter rolletilpasning for denne side.</span><span class="sxs-lookup"><span data-stu-id="ddb63-124">Alternatively, try switching to a Role Center that does include role-tailoring for this page.</span></span> <span data-ttu-id="ddb63-125">Du kan finde flere oplysninger under [Ændre grundlæggende indstillinger](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="ddb63-125">For more information, see [Change Basic Settings](ui-change-basic-settings.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ddb63-126">Se også</span><span class="sxs-lookup"><span data-stu-id="ddb63-126">See Also</span></span>
[<span data-ttu-id="ddb63-127">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="ddb63-127">Personalize Your Workspace</span></span>](ui-personalization-user.md)  
[<span data-ttu-id="ddb63-128">Tilpasse sider til profiler</span><span class="sxs-lookup"><span data-stu-id="ddb63-128">Customize Pages for Profiles</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="ddb63-129">Ændre grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="ddb63-129">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="ddb63-130">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="ddb63-130">Change Which Features are Displayed</span></span>](ui-experiences.md)  
