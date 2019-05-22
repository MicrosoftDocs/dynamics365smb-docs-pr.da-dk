---
title: Styre tilpasningen som en administrator i Business Central | Microsoft Docs
description: Få at vide, hvordan du kan tilpasse brugergrænsefladen, så den passer til din måde at arbejde på.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250591"
---
# <a name="managing-personalization-as-an-administrator"></a><span data-ttu-id="54c18-103">Administrere tilpasning som administrator</span><span class="sxs-lookup"><span data-stu-id="54c18-103">Managing Personalization as an Administrator</span></span>

<span data-ttu-id="54c18-104"> Brugere kan tilpasse deres arbejdsområde, så det passer til deres egne præferencer.</span><span class="sxs-lookup"><span data-stu-id="54c18-104">Users can personalize their workspace to suit their own preferences.</span></span> <span data-ttu-id="54c18-105">Som administrator kan du styre og administrere tilpasning ved at:</span><span class="sxs-lookup"><span data-stu-id="54c18-105">As an administrator, you control and manage personalization by:</span></span>

-   <span data-ttu-id="54c18-106">Aktivere eller deaktivere tilpasningsfunktionen for hele programmet (kun for lokal installation).</span><span class="sxs-lookup"><span data-stu-id="54c18-106">Enabling or disabling the personalization feature for the entire the application (on-premises installation only).</span></span>
-   <span data-ttu-id="54c18-107">Aktivere eller deaktivere tilpasningsfunktionen for brugere med en bestemt profil.</span><span class="sxs-lookup"><span data-stu-id="54c18-107">Enabling or disabling the personalization feature for users of a specific profile.</span></span>
-   <span data-ttu-id="54c18-108">Fjerne eventuelle sidetilpasninger, som brugere har foretaget.</span><span class="sxs-lookup"><span data-stu-id="54c18-108">Clearing any page personalizations that users have made.</span></span>

## <a name="EnablePersonalization"></a><span data-ttu-id="54c18-109">Sådan aktiveres eller deaktiveres tilpasning (kun lokalt)</span><span class="sxs-lookup"><span data-stu-id="54c18-109">To enable or disable personalization (On-Premises Only)</span></span>

<span data-ttu-id="54c18-110">Tilpasning er som standard ikke aktiveret på klienten.</span><span class="sxs-lookup"><span data-stu-id="54c18-110">By default, personalization is not enabled in the client.</span></span> <span data-ttu-id="54c18-111">Du kan aktivere eller deaktivere tilpasning ved at ændre konfigurationsfilen (navsettings.json) på den Business Central Web Server-forekomst, der betjener klienterne.</span><span class="sxs-lookup"><span data-stu-id="54c18-111">You enable or disable personalization by modifying the configuration file (navsettings.json) of the Business Central Web Server instance that serves the clients.</span></span>

1. <span data-ttu-id="54c18-112">Hvis du vil aktivere tilpasning, skal du tilføje følgende linje i filen navsettings.json:</span><span class="sxs-lookup"><span data-stu-id="54c18-112">To enable personalization, add the following line in the navsettings.json file:</span></span>

    ```
    "PersonalizationEnabled": "true"
    ```

    <span data-ttu-id="54c18-113">Hvis du vil deaktivere tilpasning, skal du fjerne linjen eller ændre den til:</span><span class="sxs-lookup"><span data-stu-id="54c18-113">To disable personalization, remove this line or change it to:</span></span>

    ```
    "PersonalizationEnabled": "false"
    ```

    <span data-ttu-id="54c18-114">Du kan finde flere oplysninger om, hvordan du kan ændre filen navsettings.json, i [Redigere navsettings.json-filen direkte](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span><span class="sxs-lookup"><span data-stu-id="54c18-114">For more information about how to modify the navsettings.json file, see [Modify the navsettings.json file directly](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings).</span></span>

2. <span data-ttu-id="54c18-115">Oprette og hente programsymboler.</span><span class="sxs-lookup"><span data-stu-id="54c18-115">Generate and download the application symbols.</span></span>

    <span data-ttu-id="54c18-116">Dette trin er valgfrit og er ikke påkrævet for at aktivere brugertilpasning.</span><span class="sxs-lookup"><span data-stu-id="54c18-116">This step is optional, and not required to enable personalization.</span></span> <span data-ttu-id="54c18-117">Men det sikrer, at nye sider, der er oprettet af udviklere, kan tilpasses.</span><span class="sxs-lookup"><span data-stu-id="54c18-117">However, it ensures that new pages that are created by developers can be personalized.</span></span>

    1. <span data-ttu-id="54c18-118">Først skal du oprette symbolerne ved at køre finsql.exe med kommandoen `generatesymbolreference`.</span><span class="sxs-lookup"><span data-stu-id="54c18-118">First, you generate the symbols by running finsql.exe with `generatesymbolreference` command.</span></span> <span data-ttu-id="54c18-119">Filen finsql.exe er placeret i installationsmappen til [!INCLUDE[server](includes/server.md)] og Dynamics NAV-udviklingsmiljøet (CSIDE).</span><span class="sxs-lookup"><span data-stu-id="54c18-119">The finsql.exe file is located in the installation folder for the [!INCLUDE[server](includes/server.md)] and Dynamics NAV Development Environment (CSIDE).</span></span> <span data-ttu-id="54c18-120">Opret symbolerne ved at åbne en kommandoprompt, skift til den mappe, hvor filen er gemt, og kør følgende kommando:</span><span class="sxs-lookup"><span data-stu-id="54c18-120">To generate the symbols, open a command prompt, change to the directory where the file is store, and the run the following command:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    <span data-ttu-id="54c18-121">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="54c18-121">For example:</span></span>

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    <span data-ttu-id="54c18-122">Du kan finde flere oplysninger i [Kørsel af C/SIDE og AL Side om side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span><span class="sxs-lookup"><span data-stu-id="54c18-122">For more information, see [Running C/SIDE and AL Side-by-Side](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).</span></span>

    2. <span data-ttu-id="54c18-123">Konfigurer [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-forekomsten til **Aktivér indlæsning af programsymbolreferencer ved serverstart** (EnableSymbolLoadingAtServerStartup).</span><span class="sxs-lookup"><span data-stu-id="54c18-123">Configure [!INCLUDE[nav_server_md](includes/nav_server_md.md)] instance to **Enable loading application symbol references at server startup** (EnableSymbolLoadingAtServerStartup).</span></span> <span data-ttu-id="54c18-124">Du kan finde flere oplysninger under [Konfiguration af Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span><span class="sxs-lookup"><span data-stu-id="54c18-124">For more information, see [Configuring Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings).</span></span>

## <a name="to-disable-personalization-for-a-profile"></a><span data-ttu-id="54c18-125">Sådan deaktiveres tilpasning for en profil</span><span class="sxs-lookup"><span data-stu-id="54c18-125">To disable personalization for a profile</span></span>

<span data-ttu-id="54c18-126">Du kan forhindre alle brugere, der tilhører en bestemt profil, i at tilpasse deres sider.</span><span class="sxs-lookup"><span data-stu-id="54c18-126">You can prevent all users that belong to a specific profile from being able to personalize their pages.</span></span>

1. <span data-ttu-id="54c18-127">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Profiler**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54c18-127">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="54c18-128">Vælg den profil på listen, der skal ændres.</span><span class="sxs-lookup"><span data-stu-id="54c18-128">Select the profile in the list that you want to modify.</span></span>
3. <span data-ttu-id="54c18-129">Markér afkrydsningsfeltet **Deaktiver tilpasning**, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="54c18-129">Select the **Disable personalization** check box, and then choose the **OK** button.</span></span>

## <a name="to-clear-user-personalizations"></a><span data-ttu-id="54c18-130">Sådan fjernes brugertilpasninger</span><span class="sxs-lookup"><span data-stu-id="54c18-130">To clear user personalizations</span></span>

<span data-ttu-id="54c18-131">Når sidetilpasninger fjernes, går siden tilbage til det oprindelige layout, før der blev foretaget nogen tilpasning.</span><span class="sxs-lookup"><span data-stu-id="54c18-131">Clearing page personalization changes the page back to its original layout before any personalization was made.</span></span> <span data-ttu-id="54c18-132">Tilpasninger, som brugere har foretaget af sider, kan fjernes på to måder: ved brug af siden **Slet brugertilpasning** side og ved brug af siden **Brugertilpasningskort**.</span><span class="sxs-lookup"><span data-stu-id="54c18-132">There are two ways to clear the personalizations that users have made to pages: using the **Delete User Personalization** page and using the **User Personalization Card** page.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a><span data-ttu-id="54c18-133">Sådan fjernes brugertilpasninger ved brug af siden Slet brugertilpasning</span><span class="sxs-lookup"><span data-stu-id="54c18-133">To clear user personalizations by using the Delete User Personalization page</span></span>

<span data-ttu-id="54c18-134">Siden **Slet brugertilpasning** giver dig mulighed for at slette tilpasning på sidebasis for hver enkelt bruger.</span><span class="sxs-lookup"><span data-stu-id="54c18-134">The **Delete User Personalization** page enables you to clear personalizations on a per-page basis for each user individually.</span></span>

1. <span data-ttu-id="54c18-135">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet brugertilpasning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54c18-135">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="54c18-136">Siden viser alle de sider, der er blevet tilpasset, og den bruger, de tilhører.</span><span class="sxs-lookup"><span data-stu-id="54c18-136">The page lists all the pages that have been personalized and the user it belongs to.</span></span>

    >[!NOTE]
    > <span data-ttu-id="54c18-137">En markering i kolonnerne **Ældre tilpasning** angiver, at tilpasningen blev udført i en ældre version af [!INCLUDE[d365fin](includes/d365fin_md.md)], som håndterede tilpasning anderledes end nu.</span><span class="sxs-lookup"><span data-stu-id="54c18-137">A check mark in the **Legacy Personalization** columns indicates that the personalization was done in an older version of [!INCLUDE[d365fin](includes/d365fin_md.md)], which handled personalization different than it does now.</span></span> <span data-ttu-id="54c18-138">Brugere, som forsøger at tilpasse siderne, er blokeret fra at gøre det, medmindre de vælger at låse siden op.</span><span class="sxs-lookup"><span data-stu-id="54c18-138">Users who try to personalize these pages are locked from doing so unless they choose to unlock the page.</span></span> <span data-ttu-id="54c18-139">Du kan finde flere oplysninger i [Derfor er en side spærret for tilpasning](ui-personalization-locked.md).</span><span class="sxs-lookup"><span data-stu-id="54c18-139">For more information, see [Why a page is locked from personalizing](ui-personalization-locked.md).</span></span>

2. <span data-ttu-id="54c18-140">Marker den post, du vil slette, og vælg derefter handlingen **Slet**.</span><span class="sxs-lookup"><span data-stu-id="54c18-140">Select the entry that you want to delete, and then choose the **Delete** action.</span></span>

    <span data-ttu-id="54c18-141">Brugerne vil se ændringerne, næste gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="54c18-141">The user will see the changes the next time they sign-in.</span></span>

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a><span data-ttu-id="54c18-142">Sådan fjernes brugertilpasninger ved brug af siden Brugertilpasningskort</span><span class="sxs-lookup"><span data-stu-id="54c18-142">To clear user personalizations by using the User Personalization Card page</span></span>

<span data-ttu-id="54c18-143">Siden **Brugertilpasningskort** giver dig mulighed for at slette tilpasningen på alle sider for en specifik bruger.</span><span class="sxs-lookup"><span data-stu-id="54c18-143">The **User Personalization Card** page enables you to clear the personalization on all pages for specific user.</span></span> <span data-ttu-id="54c18-144">Det kræver skrivetilladelse til tabel 2000000072 **Profil**.</span><span class="sxs-lookup"><span data-stu-id="54c18-144">This requires write permission to Table 2000000072 **Profile**.</span></span>

1. <span data-ttu-id="54c18-145">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Brugertilpasning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="54c18-145">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Personalization**, and then choose the related link.</span></span>

    <span data-ttu-id="54c18-146">Siden **Brugertilpasning** viser alle brugere, der muligvis kan have personlige sider.</span><span class="sxs-lookup"><span data-stu-id="54c18-146">The **User Personalization** page lists all users who potentially have personalized pages.</span></span> <span data-ttu-id="54c18-147">Hvis du ikke kan finde en bruger på listen, betyder det, at vedkommende ikke har nogen tilpassede sider.</span><span class="sxs-lookup"><span data-stu-id="54c18-147">If you cannot find a user in the list, this means that they do not have any personalized pages.</span></span>

2. <span data-ttu-id="54c18-148">Vælg brugeren på listen, og vælg derefter handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="54c18-148">Select the user from the list, and then choose the **Edit** action.</span></span>

3. <span data-ttu-id="54c18-149">Under fanen **Handlinger** skal du vælge **Fjern tilpassede sider**.</span><span class="sxs-lookup"><span data-stu-id="54c18-149">On the **Actions** tab, choose **Clear Personalized Pages**.</span></span>

    <span data-ttu-id="54c18-150">Brugerne vil se ændringerne, næste gang de logger på.</span><span class="sxs-lookup"><span data-stu-id="54c18-150">The user will see the changes the next time they sign-in.</span></span>

## <a name="see-also"></a><span data-ttu-id="54c18-151">Se også</span><span class="sxs-lookup"><span data-stu-id="54c18-151">See Also</span></span>
[<span data-ttu-id="54c18-152">Tilpasse dit arbejdsområde</span><span class="sxs-lookup"><span data-stu-id="54c18-152">Personalizing Your Workspace</span></span>](ui-personalization-user.md)  
<span data-ttu-id="54c18-153">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="54c18-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="54c18-154">Ændring af grundlæggende indstillinger</span><span class="sxs-lookup"><span data-stu-id="54c18-154">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="54c18-155">Ændre, hvilke funktioner der vises</span><span class="sxs-lookup"><span data-stu-id="54c18-155">Changing Which Features are Displayed</span></span>](ui-experiences.md)  
