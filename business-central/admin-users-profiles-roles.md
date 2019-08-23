---
title: Administrere brugere og roller | Microsoft Docs
description: Lære at administrere brugere og rollecentre i Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 08/02/2019
ms.author: edupont
ms.openlocfilehash: 27a57490101195f8dc05cc39538260e7db5e46af
ms.sourcegitcommit: 5bcc5f95e450ee9a3d9f7a380e592a5e75c4185b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2019
ms.locfileid: "1858216"
---
# <a name="understanding-users-roles-and-profiles"></a><span data-ttu-id="f8886-103">Forstå brugere, roller og profiler</span><span class="sxs-lookup"><span data-stu-id="f8886-103">Understanding Users, Roles, and Profiles</span></span>

<span data-ttu-id="f8886-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] tilføjes brugerne af en administrator, der giver også brugerne adgang til de områder i [!INCLUDE[d365fin](includes/d365fin_md.md)], de skal bruge i deres arbejde.</span><span class="sxs-lookup"><span data-stu-id="f8886-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], users are added by an administrator who also gives users access to the areas of [!INCLUDE[d365fin](includes/d365fin_md.md)] that they need in their work.</span></span>  

<span data-ttu-id="f8886-105">Adgangen til funktionen styres via *brugergrupper* og *profiler (roller)*.</span><span class="sxs-lookup"><span data-stu-id="f8886-105">Access to functionality is managed through *user groups* and *profiles (roles)*.</span></span> <span data-ttu-id="f8886-106">Som administrator, kan du tilføje og fjerne brugere som en del af dit [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement, og du kan tildele brugertilladelser gennem brugergrupper.</span><span class="sxs-lookup"><span data-stu-id="f8886-106">As an administrator, you can add and remove users as part of your [!INCLUDE[d365fin](includes/d365fin_md.md)] subscription, and you can assign users permissions through user groups.</span></span>  

## <a name="adding-users"></a><span data-ttu-id="f8886-107">Tilføje brugere</span><span class="sxs-lookup"><span data-stu-id="f8886-107">Adding Users</span></span>

<span data-ttu-id="f8886-108">Når du vil tilføje brugere i [!INCLUDE[d365fin](includes/d365fin_md.md)] online, skal din virksomheds Office 365-administrator først oprette brugerne i Office 365 Administration.</span><span class="sxs-lookup"><span data-stu-id="f8886-108">To add users in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, your company's Office 365 administrator must first create the users in the Office 365 Admin Center.</span></span> <span data-ttu-id="f8886-109">Du kan finde flere oplysninger under [Føje brugere til Office 365 til virksomheder](https://aka.ms/CreateOffice365Users).</span><span class="sxs-lookup"><span data-stu-id="f8886-109">For more information, see [Add Users to Office 365 for business](https://aka.ms/CreateOffice365Users).</span></span>

<span data-ttu-id="f8886-110">Administratoren kan derefter tildele tilladelser til hver bruger og grupper af brugere.</span><span class="sxs-lookup"><span data-stu-id="f8886-110">Then, the administrator can assign permissions to each user and groups of users.</span></span> <span data-ttu-id="f8886-111">Du kan finde flere oplysninger i [Administrere brugere og rettigheder](ui-how-users-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f8886-111">For more information, see [Managing Users and Permissions](ui-how-users-permissions.md).</span></span>  

<span data-ttu-id="f8886-112">De mest effektive rettigheder, en bruger kan have, er rettighedssættet SUPER.</span><span class="sxs-lookup"><span data-stu-id="f8886-112">The most powerful permissions that a user can have is the SUPER permission set.</span></span> <span data-ttu-id="f8886-113">Hver virksomhed skal have mindst én bruger med dette rettighedssæt, men det er bedst at give hver bruger rettigheder, der passer til deres arbejdsbehov i [!INCLUDE[prodshort](includes/prodshort.md)] og ikke mere end det.</span><span class="sxs-lookup"><span data-stu-id="f8886-113">Each company must have at least one user with this permission set, but it is a best practice to give each user permissions that match their work needs in [!INCLUDE[prodshort](includes/prodshort.md)] and not more than that.</span></span> <span data-ttu-id="f8886-114">Dette sikrer f.eks, at brugerne kun har adgang til data, der er relevante for deres arbejde.</span><span class="sxs-lookup"><span data-stu-id="f8886-114">This helps ensure that users only have access to data that is relevant to their work, for example.</span></span>  

> [!TIP]
> <span data-ttu-id="f8886-115">Det anbefales at sikre, at Office 365-administratoren også har rettigheden SUPER indstillet i [!INCLUDE[prodshort](includes/prodshort.md)], fordi der letter mange administrative opgaver, herunder konfiguration af integration med andre programmer.</span><span class="sxs-lookup"><span data-stu-id="f8886-115">It's a best practice to make sure that the Office 365 administrator also has the SUPER permission set in [!INCLUDE[prodshort](includes/prodshort.md)] because that makes many administrative tasks easier, including setting up integration with other apps.</span></span>

### <a name="users-of-on-premises-deployments"></a><span data-ttu-id="f8886-116">Brugere af lokale installationer</span><span class="sxs-lookup"><span data-stu-id="f8886-116">Users of on-premises deployments</span></span>

<span data-ttu-id="f8886-117">Ved lokale installationer af [!INCLUDE[d365fin](includes/d365fin_md.md)] kan administratoren vælge mellem forskellige godkendelse af legitimationsoplysninger for brugere.</span><span class="sxs-lookup"><span data-stu-id="f8886-117">For on-premises deployments of [!INCLUDE[d365fin](includes/d365fin_md.md)], the administrator can choose between different credential authorization mechanisms for users.</span></span> <span data-ttu-id="f8886-118">Når du derefter opretter en bruger, angiver du forskellige oplysninger, afhængigt af den type legitimationsoplysninger, du bruger i den specifikke [!INCLUDE[server](includes/server.md)]-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f8886-118">Then, when you create a user, you provide different information depending on the credential type that you are using in the specific [!INCLUDE[server](includes/server.md)] instance.</span></span> <span data-ttu-id="f8886-119">Du kan finde flere oplysninger i [Godkendelse og typer af legitimationsoplysninger](/dynamics365/business-central/dev-itpro/administration/users-credential-types) i sektionen Administration af udvikler- og ITPro-indholdet til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="f8886-119">For more information, see the [Authentication and Credential Types](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in the Administration section of the developer and ITPro content for [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

## <a name="profiles-roles"></a><span data-ttu-id="f8886-120">Profiler (Roller)</span><span class="sxs-lookup"><span data-stu-id="f8886-120">Profiles (Roles)</span></span>

<span data-ttu-id="f8886-121">Personer i virksomheden, der har adgang til [!INCLUDE[d365fin](includes/d365fin_md.md)], tildeles alle en rolle, som giver dem adgang til et *Rollecenter*.</span><span class="sxs-lookup"><span data-stu-id="f8886-121">The people in your company who have access to [!INCLUDE[d365fin](includes/d365fin_md.md)] are all assigned a role that gives them access to a *Role Center*.</span></span>

<span data-ttu-id="f8886-122">Profiler er samlinger af [!INCLUDE[d365fin](includes/d365fin_md.md)]-brugere, der deler den samme rolle.</span><span class="sxs-lookup"><span data-stu-id="f8886-122">Profiles are collections of [!INCLUDE[d365fin](includes/d365fin_md.md)] users who share the same role.</span></span> <span data-ttu-id="f8886-123">Et rollecenter er indgangspunktet og startsiden til [!INCLUDE[d365fin](includes/d365fin_md.md)], der giver dig hurtig adgang til dine vigtigste opgaver og viser forskellig indsigt og nøgletal (KPI'er) om dit arbejde.</span><span class="sxs-lookup"><span data-stu-id="f8886-123">A Role Center is the entry point and home page for [!INCLUDE[d365fin](includes/d365fin_md.md)] that gives you quick access to your most important tasks and displays various insights and key performance indicators (KPIs) about your work.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="f8886-124">I den aktuelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] online kan du ikke tilføje, redigere eller slette profiler.</span><span class="sxs-lookup"><span data-stu-id="f8886-124">In the current version of [!INCLUDE[d365fin](includes/d365fin_md.md)] online, you cannot add, edit, or delete profiles.</span></span>  

### <a name="CreateProfile"></a><span data-ttu-id="f8886-125">Sådan oprettes en profil</span><span class="sxs-lookup"><span data-stu-id="f8886-125">To create a profile</span></span>

1.  <span data-ttu-id="f8886-126">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "ikonet Søg efter side eller rapport"), angiv **Profiler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f8886-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Profiles**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="f8886-127">På siden **Profiler** skal du vælge handlingen **Ny** for at åbne siden **Nyt profilkort**.</span><span class="sxs-lookup"><span data-stu-id="f8886-127">On the **Profiles** page, choose the **New** action to open the **New Profile Card** page.</span></span>  

3.  <span data-ttu-id="f8886-128">I feltet **Profil-id** skal du angive et navn, der beskriver den tiltænkte rolle for brugerne.</span><span class="sxs-lookup"><span data-stu-id="f8886-128">In the **Profile ID** field, enter a name that describes the intended role of the users.</span></span>  

4.  <span data-ttu-id="f8886-129">Gå til feltet **Beskrivelse** , og angiv en beskrivelse af profil-id'et, f.eks. **Ordrebehandler**.</span><span class="sxs-lookup"><span data-stu-id="f8886-129">In the **Description** field, enter a description of the Profile ID, for example, **Order Processor**.</span></span>  

5.  <span data-ttu-id="f8886-130">Angiv feltet **Rollecenter-id** for det rollecenter, der skal tildeles til profilen.</span><span class="sxs-lookup"><span data-stu-id="f8886-130">Set the **Role Center ID** field to the Role Center that you want to assign to the profile.</span></span>  

<span data-ttu-id="f8886-131">Proceduren for ændring af en eksisterende profil er den samme, bortset fra, at du kan vælge en eksisterende profil på siden **Profiler** i stedet for at vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f8886-131">The procedure for modifying an existing profile is the same, except you select an existing profile on the **Profiles** page instead of choosing the **New** action.</span></span>  


### <a name="copy-a-profile"></a><span data-ttu-id="f8886-132">Kopiere en profil</span><span class="sxs-lookup"><span data-stu-id="f8886-132">Copy a profile</span></span>
<span data-ttu-id="f8886-133">Kopiering af en profil kan spare tid, hvis du vil bruge samme indstillinger på en profil, og du kun vil ændre nogle få indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f8886-133">Copying a profile can save you time if you want to use similar settings on a profile and you only want to change a few settings.</span></span>

1.  <span data-ttu-id="f8886-134">Åbn den profil, du vil kopiere, og vælg derefter handlingen **Kopier profil**.</span><span class="sxs-lookup"><span data-stu-id="f8886-134">Open the profile that you want to copy, and then choose the **Copy Profile** action.</span></span>

2.  <span data-ttu-id="f8886-135">I feltet **Nyt profil-id** skal du indtaste et navn på den profil, du vil kopiere.</span><span class="sxs-lookup"><span data-stu-id="f8886-135">In **New Profile ID** field, enter a name for the profile that you want to copy.</span></span>

3.  <span data-ttu-id="f8886-136">Angiv feltet **Ny profils område** til et af følgende:</span><span class="sxs-lookup"><span data-stu-id="f8886-136">Set the **New Profile Scope** field to one of the following:</span></span>

    - <span data-ttu-id="f8886-137">**System** for at gøre den nye profil tilgængelig for alle lejerdatabaser, der bruger programmet.</span><span class="sxs-lookup"><span data-stu-id="f8886-137">**System** to make the new profile available to all tenant databases that use the application.</span></span>
    - <span data-ttu-id="f8886-138">**Lejer** for at gøre den nye profil tilgængelig for kun den aktuelle lejerdatabase.</span><span class="sxs-lookup"><span data-stu-id="f8886-138">**Tenant** to make the new profile available to just the current tenant database.</span></span>
4. <span data-ttu-id="f8886-139">Tryk på knappen **OK**, når du er færdig.</span><span class="sxs-lookup"><span data-stu-id="f8886-139">Choose the **OK** button when done.</span></span>

### <a name="ExportImportProfile"></a><span data-ttu-id="f8886-140">Eksportere og importere profiler</span><span class="sxs-lookup"><span data-stu-id="f8886-140">Export and import profiles</span></span>

<span data-ttu-id="f8886-141">Du kan eksportere og importere profiler som XML-filer til og fra den en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database.</span><span class="sxs-lookup"><span data-stu-id="f8886-141">You can export and import profiles as XML files to and from the a [!INCLUDE[d365fin](includes/d365fin_md.md)] database.</span></span> <span data-ttu-id="f8886-142">Eksport og import af en profil kan spare dig tid, når du konfigurerer brugergrænsefladen, fordi du kan genbruge en eksisterende profil i stedet at konfigurere en profil forfra.</span><span class="sxs-lookup"><span data-stu-id="f8886-142">Exporting and importing a profile can save you time when configuring the user interface because you reuse an existing profile configuration instead of having to configure a profile from scratch.</span></span> <span data-ttu-id="f8886-143">Hvis du har en profil, der er konfigureret i en [!INCLUDE[d365fin](includes/d365fin_md.md)]-database, og du vil genbruge alle eller nogle af de samme profilkonfigurationer i en anden database, kan du eksportere profilen til en XML-fil.</span><span class="sxs-lookup"><span data-stu-id="f8886-143">If you have a profile that is configured in a [!INCLUDE[d365fin](includes/d365fin_md.md)] database and you would like to reuse all or some of the same profile configurations in another database, you can export the profile to an XML file.</span></span> <span data-ttu-id="f8886-144">Du kan derefter importere XML-filen med profilen til anden databasen.</span><span class="sxs-lookup"><span data-stu-id="f8886-144">Then, you can import the profile XML file into the other database.</span></span>

-   <span data-ttu-id="f8886-145">For at eksportere en profil kan du enten vælge handlingen **Udlæs profiler** fra siden **Profilliste** eller siden **Profilkort**, eller du kan søge efter og åbne siden **Udlæs profiler**.</span><span class="sxs-lookup"><span data-stu-id="f8886-145">To export a profile, you can either choose the **Export Profiles** action from the **Profile List** or **Profile Card** page or you can search for and open the **Export Profiles** page.</span></span> <span data-ttu-id="f8886-146">Gem XML-filen på en placering på computeren eller netværket.</span><span class="sxs-lookup"><span data-stu-id="f8886-146">Save the XML file to a location on your computer or network.</span></span>

-   <span data-ttu-id="f8886-147">For at importere en profil kan du enten vælge handlingen **Indlæs profiler** fra siden **Profilliste**, eller du kan søge efter og åbne siden **Indlæs profiler**.</span><span class="sxs-lookup"><span data-stu-id="f8886-147">To import a profile, you can either choose the **Import Profile** action from the **Profile List** page, or you can search for and open the **Import Profiles** page.</span></span>

    > [!NOTE]  
    >  <span data-ttu-id="f8886-148">Du kan ikke importere en profil, der allerede findes i databasen, selvom XML-filen har et andet navn eller har et andet indhold.</span><span class="sxs-lookup"><span data-stu-id="f8886-148">You cannot import a profile that already exists in the database, even though the XML file is named differently or has different content.</span></span> <span data-ttu-id="f8886-149">Før du kan importere den nye profil, skal du slette den eksisterende profil.</span><span class="sxs-lookup"><span data-stu-id="f8886-149">You must delete the existing profile before you can import the new profile.</span></span>


## <a name="configuration-and-personalization"></a><span data-ttu-id="f8886-150">Konfiguration og brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="f8886-150">Configuration and Personalization</span></span>
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

<span data-ttu-id="f8886-151">Brugene tilpasser brugergrænsefladen i deres personlige version ved at tilpasse brugergrænsefladen under deres egne brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="f8886-151">Users personalize the user interface of their personal version by customizing the user interface under their own user logon.</span></span> <span data-ttu-id="f8886-152">Denne tilpasning kan slettes af administratoren.</span><span class="sxs-lookup"><span data-stu-id="f8886-152">This personalization can be deleted by the administrator.</span></span> <span data-ttu-id="f8886-153">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="f8886-153">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="f8886-154">Se også</span><span class="sxs-lookup"><span data-stu-id="f8886-154">See Also</span></span>  
[<span data-ttu-id="f8886-155">Administrere brugere og deres rettigheder</span><span class="sxs-lookup"><span data-stu-id="f8886-155">Managing Users and Permissions</span></span>](ui-how-users-permissions.md)  
[<span data-ttu-id="f8886-156">Administrere tilpasning som administrator</span><span class="sxs-lookup"><span data-stu-id="f8886-156">Managing Personalization as an Administrator</span></span>](ui-personalization-manage.md)  
[<span data-ttu-id="f8886-157">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="f8886-157">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
