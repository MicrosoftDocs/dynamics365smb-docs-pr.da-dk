---
title: Hvorfor kan jeg ikke tilpasse en side | Microsoft Docs
description: Forklarer, hvorfor du ikke kan tilpasse en side, og hvad du kan gøre for at låse den op, så du kan tilpasse den.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 64995372f68ed2804bc165823dacc34ad6a3194d
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2019
ms.locfileid: "911692"
---
# <a name="why-a-page-is-locked-from-personalization"></a><span data-ttu-id="d7b6e-103">Hvorfor er en side låst mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="d7b6e-103">Why a Page is Locked from Personalization</span></span>

<span data-ttu-id="d7b6e-104">Der er to forhold, der forhindrer dig i at tilpasse en side.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-104">There are two conditions that prevent you from personalizing a page.</span></span> <span data-ttu-id="d7b6e-105">Enten er siden låst (som angivet af ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst")), eller den er spærret (som angivet af ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret")).</span><span class="sxs-lookup"><span data-stu-id="d7b6e-105">Either the page is locked (as indicated by ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock")) or it is blocked (as indicated by ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked")).</span></span>

## <a name="locked-from-personalizing"></a><span data-ttu-id="d7b6e-106">Låst mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="d7b6e-106">Locked from Personalizing</span></span>

<span data-ttu-id="d7b6e-107">Hvis der er et ikon![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") i banneret **Tilpasning**, når du åbner en side (som vist), betyder det, at du i øjeblikket er forhindret i at foretage flere tilpasningsændringer af siden.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-107">If there is a ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock") icon in the **Personalizing** banner when you open a page (as shown), this means that you are currently prevented from making any more personalization changes to the page.</span></span>

<span data-ttu-id="d7b6e-108">![Tilpasning låst](media/personalization-locked.png "Tilpasning låst")</span><span class="sxs-lookup"><span data-stu-id="d7b6e-108">![Personalize Lock](media/personalization-locked.png "Personalize lock")</span></span>


<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

<span data-ttu-id="d7b6e-109">Der kan være to grunde til dette:</span><span class="sxs-lookup"><span data-stu-id="d7b6e-109">There can be two reasons for this:</span></span>

1. <span data-ttu-id="d7b6e-110">Du har tilpasset siden før, men det er gjort ved hjælp af en tidligere version af produktet.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-110">You have personalized the page before, but it was done using an earlier version of the product.</span></span> <span data-ttu-id="d7b6e-111">Vi har ændret den måde, hvorpå tilpasning fungerer i baggrunden, siden sidste gang du har tilpasset siden.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-111">We changed the way personalization works behind the scenes since the last time that you personalized the page.</span></span> <span data-ttu-id="d7b6e-112">Desværre arbejder den gamle måde og den nye måde at gøre tingene på ikke sammen.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-112">Unfortunately, the old way and new way of doing things do not work together.</span></span>

2. <span data-ttu-id="d7b6e-113">Indtil nu har du kun brugt [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til at tilpasse siden.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-113">Until now, you have only used the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] to personalize the page.</span></span>

### <a name="unlocking-the-page"></a><span data-ttu-id="d7b6e-114">Oplåsning af siden</span><span class="sxs-lookup"><span data-stu-id="d7b6e-114">Unlocking the Page</span></span>

<span data-ttu-id="d7b6e-115">Hvis du vil låse en side op og fortsætte med at tilpasse den, skal du vælge ![Tilpasning låst](media/personalization-lock-icon.png "Tilpasning låst") og derefter **Lås op**.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-115">If you want to unlock a page and continue personalizing it, choose ![Personalize Lock](media/personalization-lock-icon.png "Personalize lock"), and then **Unlock**.</span></span>  

<span data-ttu-id="d7b6e-116">Før du låser siden op, skal du være opmærksom på følgende:</span><span class="sxs-lookup"><span data-stu-id="d7b6e-116">Before you unlock the page, be aware of the following:</span></span>

- <span data-ttu-id="d7b6e-117">Den aktuelle tilpasning af siden fjernes.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-117">The current personalization of the page will be cleared.</span></span> <span data-ttu-id="d7b6e-118">Siden vender tilbage til sit oprindelige format, og du skal starte forfra.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-118">The page will go back to its original layout, and you will have to start from scratch.</span></span>

- <span data-ttu-id="d7b6e-119">I feltet [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] forbliver siden, som den er, og bliver ikke påvirket af nye tilpasningsændringer i Business Central-klienten.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-119">In the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)], the page will remain as-is and will not be affected by the new personalization changes made in the Business Central client.</span></span> <span data-ttu-id="d7b6e-120">Fremover vil tilpasningen i [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] og Business Central-klienten være helt adskilt fra hinanden.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-120">Going forward, the personalization in the [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] and Business Central client will be completely separate from each other.</span></span>

## <a name="blocked-from-personalizing"></a><span data-ttu-id="d7b6e-121">Spærret mod tilpasning</span><span class="sxs-lookup"><span data-stu-id="d7b6e-121">Blocked from Personalizing</span></span>

<span data-ttu-id="d7b6e-122">Hvis der er et ikon ![Tilpasning spærret](media/personalization-blocked-icon.png "Tilpasning spærret") i banneret Tilpasning, betyder det, at du er spærret mod at foretage nogen form for tilpasning af siden.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-122">If there is a ![Personalization blocked](media/personalization-blocked-icon.png "Personalization blocked") icon in the Personalizing banner, this means that you are blocked from doing any personalization to the page.</span></span>

<span data-ttu-id="d7b6e-123">![Tilpasning spærret](media/personalization-blocked.png "Tilpasning låst")</span><span class="sxs-lookup"><span data-stu-id="d7b6e-123">![Personalize blocked](media/personalization-blocked.png "Personalize lock")</span></span>

<span data-ttu-id="d7b6e-124">Det skyldes, at det rollecenter eller den profil, der aktuelt er knyttet til brugerkontoen, ændrer denne side specifikt til din rolle.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-124">The reason for this is that the Role Center or profile that is currently associated with your user account modifies this page specifically for your role.</span></span> <span data-ttu-id="d7b6e-125">Du kan kontakte systemadministratoren for at få hjælp, eller også kan du, hvis det giver mening, forsøge at skifte til et Rollecenter (fra [**Mine indstillinger**](https://businesscentral.dynamics.com?page=9176 "Gå direkte til siden med dine brugerindstillinger i Business Central")), der inkluderer specifik tilpasning til rollen for denne side.</span><span class="sxs-lookup"><span data-stu-id="d7b6e-125">Please contact your administrator for assistance or, if it makes sense, try switching to a Role Center (from  [**My Settings**](https://businesscentral.dynamics.com?page=9176 "Go directly to your user settings page in Business Central")) that does include role-tailoring for this page.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7b6e-126">Se også</span><span class="sxs-lookup"><span data-stu-id="d7b6e-126">See Also</span></span>
[<span data-ttu-id="d7b6e-127">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="d7b6e-127">Personalizing Your Workspace</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="d7b6e-128">Administration af tilpasning</span><span class="sxs-lookup"><span data-stu-id="d7b6e-128">Managing Personalization</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="d7b6e-129">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="d7b6e-129">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="d7b6e-130">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="d7b6e-130">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
