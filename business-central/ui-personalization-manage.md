---
title: Styre tilpasningen som en administrator i Business Central | Microsoft Docs
description: "Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 15d7e4aac7989f95f7becc8aa8ed96381a7dc2de
ms.contentlocale: da-dk
ms.lasthandoff: 11/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="2ef73-103">Administrere tilpasning som administrator</span><span class="sxs-lookup"><span data-stu-id="2ef73-103">Managing Personalization as an Administrator</span></span>
<span data-ttu-id="2ef73-104"><!--NAV in the Web client--> Brugere kan tilpasse deres arbejdsområde, så det passer til deres egne præferencer.</span><span class="sxs-lookup"><span data-stu-id="2ef73-104"><!--NAV in the Web client--> Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="2ef73-105">Som administrator kan du kan styre og administrere tilpasning ved at deaktivere brugernes mulighed for at tilpasse sider og ved at fjerne alle sidetilpasninger, som brugere har foretaget.</span><span class="sxs-lookup"><span data-stu-id="2ef73-105">As an administrator, you can control and manage personalization by disabling the ability for users to personalize pages and clearing any page personalizations that users have made.</span></span>

## <a name="disable-personalization-for-a-profile"></a><span data-ttu-id="2ef73-106">Deaktivere tilpasning for en profil</span><span class="sxs-lookup"><span data-stu-id="2ef73-106">Disable personalization for a profile</span></span>
<span data-ttu-id="2ef73-107">Du kan forhindre alle brugere, der tilhører en bestemt profil, i at tilpasse deres sider.</span><span class="sxs-lookup"><span data-stu-id="2ef73-107">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>
1.  <span data-ttu-id="2ef73-108">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Profiler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2ef73-108">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2.  <span data-ttu-id="2ef73-109">Vælg den profil på listen, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="2ef73-109">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="2ef73-110">Markér afkrydsningsfeltet **Deaktiver tilpasning**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-110">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="clear-user-personalizations"></a><span data-ttu-id="2ef73-111">Fjern brugertilpasninger</span><span class="sxs-lookup"><span data-stu-id="2ef73-111">Clear user personalizations</span></span>

<span data-ttu-id="2ef73-112">Når sidetilpasninger fjernes, går siden tilbage til det oprindelige layout, før der blev foretaget nogen tilpasning.</span><span class="sxs-lookup"><span data-stu-id="2ef73-112">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="2ef73-113">Tilpasninger, som brugere har foretaget af sider, kan fjernes på to måder: ved brug af siden **Slet brugertilpasning** side og ved brug af siden **Brugertilpasningskort**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-113">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="2ef73-114">Slette brugertilpasninger ved brug af siden Slet brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="2ef73-114">Clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="2ef73-115">Siden **Slet brugertilpasning** giver dig mulighed for at slette tilpasning på sidebasis for hver enkelt bruger.</span><span class="sxs-lookup"><span data-stu-id="2ef73-115">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1.  <span data-ttu-id="2ef73-116">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet brugertilpasning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2ef73-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="2ef73-117">Siden viser alle de sider, der er blevet tilpasset, og den bruger, de tilhører.</span><span class="sxs-lookup"><span data-stu-id="2ef73-117">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="2ef73-118">En markering i kolonnerne **Ældre tilpasning** angiver, at tilpasningen blev udført i en ældre version af [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterede tilpasning anderledes end nu.</span><span class="sxs-lookup"><span data-stu-id="2ef73-118">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="2ef73-119">Brugere, som forsøger at tilpasse siderne, er blokeret fra at gøre det, medmindre de vælger at låse siden op.</span><span class="sxs-lookup"><span data-stu-id="2ef73-119">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="2ef73-120">Du kan finde flere oplysninger i [Derfor er en side spærret for tilpasning](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="2ef73-120">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="2ef73-121">Marker den post, du vil slette, og vælg derefter handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-121">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="2ef73-122">Brugerne vil se ændringerne, næste gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="2ef73-122">The user will see the changes the next time they sign-in.</span></span>

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="2ef73-123">Slette brugertilpasninger ved brug af siden Brugertilpasningskort</span><span class="sxs-lookup"><span data-stu-id="2ef73-123">Clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="2ef73-124">Siden **Brugertilpasningskort** giver dig mulighed for at slette tilpasningen på alle sider for en specifik bruger.</span><span class="sxs-lookup"><span data-stu-id="2ef73-124">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="2ef73-125">Det kræver skrivetilladelse til tabel 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-125">This requires write permission to Table 2000000072 **Profile**.</span></span>

1.  <span data-ttu-id="2ef73-126">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugertilpasning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="2ef73-126">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="2ef73-127">Siden **Brugertilpasning** viser alle brugere, der muligvis kan have personlige sider.</span><span class="sxs-lookup"><span data-stu-id="2ef73-127">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="2ef73-128">Hvis du ikke kan finde en bruger på listen, betyder det, at vedkommende ikke har nogen tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="2ef73-128">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="2ef73-129">Vælg brugeren på listen, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-129">Select the user from the list, and then choose the **Edit** action.</span></span>

3.  <span data-ttu-id="2ef73-130">Under fanen **Handlinger** skal du vælge **Fjern tilpassede sider**.</span><span class="sxs-lookup"><span data-stu-id="2ef73-130">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="2ef73-131">Brugerne vil se ændringerne, næste gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="2ef73-131">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="2ef73-132">Se også</span><span class="sxs-lookup"><span data-stu-id="2ef73-132">See Also</span></span>
[<span data-ttu-id="2ef73-133">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="2ef73-133">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="2ef73-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2ef73-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="2ef73-135">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="2ef73-135">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="2ef73-136">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="2ef73-136">Changing Which Features are Displayed</span></span>](ui-experiences.md)  

