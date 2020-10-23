---
title: Arbejde med Business Central-data i Microsoft Teams| Microsoft Docs
description: Sådan bruger du Business central-app til Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork
ms.date: 10/08/2020
ms.author: jswymer
ms.openlocfilehash: fbe024f724f018aae6d3aeb5251281bf4c3bfbde
ms.sourcegitcommit: 4bca699d2a5ce182eb5572d72fac4fb478c4f293
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989412"
---
# <a name="working-with-business-central-data-in-microsoft-teams"></a><span data-ttu-id="338b6-103">Arbejde med Business Central-data i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="338b6-103">Working with Business Central Data in Microsoft Teams</span></span>

[!INCLUDE [teams_preview.md](includes/teams_preview.md)]

<span data-ttu-id="338b6-104">[!INCLUDE [prodshort](includes/prodshort.md)] tilbyder en app, der har forbindelse Microsoft Teams til dine forretningsdata [!INCLUDE [prodshort](includes/prodshort.md)], så du hurtigt kan dele detaljer på tværs af gruppemedlemmer og reagere hurtigere på forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="338b6-104">[!INCLUDE [prodshort](includes/prodshort.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prodshort](includes/prodshort.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="338b6-105">I denne artikel lærer du, hvordan du kan bruge appen til at dele [!INCLUDE [prodshort](includes/prodshort.md)] data med kolleger i en samtale med grupper.</span><span class="sxs-lookup"><span data-stu-id="338b6-105">In this article, you'll learn how to use the app to share [!INCLUDE [prodshort](includes/prodshort.md)] data with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="338b6-106">Oversigt</span><span class="sxs-lookup"><span data-stu-id="338b6-106">Overview</span></span>

<span data-ttu-id="338b6-107">Med [!INCLUDE [prodshort](includes/prodshort.md)]-appen kan du:</span><span class="sxs-lookup"><span data-stu-id="338b6-107">The [!INCLUDE [prodshort](includes/prodshort.md)] app lets you:</span></span>

- <span data-ttu-id="338b6-108">Kopiere et hyperlink til en hvilken som helst Business Central-post og sætte den ind i en Teams-samtale, som du kan dele med dine kolleger.</span><span class="sxs-lookup"><span data-stu-id="338b6-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="338b6-109">Hyperlinket vil vise et kompakt, interaktivt kort, der viser oplysninger om posten.</span><span class="sxs-lookup"><span data-stu-id="338b6-109">The link will expand that into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="338b6-110">Når du er i samtalen, kan du og dine kolleger få vist flere oplysninger om posten, redigere data og handle uden at forlade Teams.</span><span class="sxs-lookup"><span data-stu-id="338b6-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action - without leaving Teams.</span></span>

<span data-ttu-id="338b6-111">[![Teams-integration med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="338b6-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="338b6-112">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="338b6-112">Prerequisites</span></span>

- <span data-ttu-id="338b6-113">Du har adgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="338b6-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="338b6-114">Du har installeret [!INCLUDE [prodshort](includes/prodshort.md)]-appen i grupper.</span><span class="sxs-lookup"><span data-stu-id="338b6-114">You've installed the [!INCLUDE [prodshort](includes/prodshort.md)] app in Teams.</span></span> <span data-ttu-id="338b6-115">Du kan finde flere oplysninger under [Installere [!INCLUDE [prodshort](includes/prodshort.md)]-app til Microsoft Teams](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="338b6-115">For more information, see [Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="338b6-116">Alle deltagerne i en samtale med Teams vil kunne få vist kort til Business Central-poster, som du sender til samtalen.</span><span class="sxs-lookup"><span data-stu-id="338b6-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="338b6-117">Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="338b6-117">But to view more details about records, by using the **Details** or **Pop-out** buttons on a card, they'll need access to [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="338b6-118">Du kan finde flere oplysninger under [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="338b6-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>
<!--
- People You and your coworkers have the following permissions in [!INCLUDE [prodshort](includes/prodshort.md)]
  - To paste a [!INCLUDE [prodshort](includes/prodshort.md)] link into a Teams conversation and have it expand into a card, you have to have at least permission to view the page and its data.
  - Once a card is submitted into a conversation, any user in that conversation can view that card without having permission to Business Central.
  - For other users to view more details from card, they must also have view permission, as a minimum, to the page and its data. If they want to change data, they'll need modify permissions.

  Setting up permissions is typically done by an administrator. For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md).-->

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="338b6-119">Medtage et Business Central-kort i en samtale med Teams</span><span class="sxs-lookup"><span data-stu-id="338b6-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="338b6-120">Log ind [!INCLUDE [prodshort](includes/prodshort.md)] for at bruge browseren.</span><span class="sxs-lookup"><span data-stu-id="338b6-120">Sign in to [!INCLUDE [prodshort](includes/prodshort.md)] using your browser.</span></span>
2. <span data-ttu-id="338b6-121">Åbn den post, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="338b6-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="338b6-122">Appen er designet til at vise sider med korttyper fra [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="338b6-122">The app is designed to display card type pages from [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="338b6-123">Åbne en side, hvor der vises en enkelt post, f. eks. en vare, kunde eller salgsordre.</span><span class="sxs-lookup"><span data-stu-id="338b6-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="338b6-124">Du kan ikke bruge den til rollecentre eller sider, hvor der vises flere poster på en liste.</span><span class="sxs-lookup"><span data-stu-id="338b6-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="338b6-125">Kopiere hele URL-adressen fra browserens adresselinje.</span><span class="sxs-lookup"><span data-stu-id="338b6-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopiere Business Central URL-adresse fra browser](media/teams-url.png)
4. <span data-ttu-id="338b6-127">Gå til Teams, og start en samtale, som kan chatte med en person, en gruppe personer eller en team-kanal.</span><span class="sxs-lookup"><span data-stu-id="338b6-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="338b6-128">Indsætte URL-adressen i den boks, hvor du tilføjer en meddelelse.</span><span class="sxs-lookup"><span data-stu-id="338b6-128">Paste the URL into the box where you add a message.</span></span>

   ![Indsætte Business Central URL-adresse i Teams](media/teams-paste-url.png)
6. <span data-ttu-id="338b6-130">Første gang du indsætter et hyperlink til en samtale, bliver du bedt om at logge på [!INCLUDE [prodshort](includes/prodshort.md)] og give appen tilladelse til at hente data.</span><span class="sxs-lookup"><span data-stu-id="338b6-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prodshort](includes/prodshort.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="338b6-131">Du skal blot følge vejledningen på skærmen.</span><span class="sxs-lookup"><span data-stu-id="338b6-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="338b6-132">Du behøver kun at udføre dette trin én gang.</span><span class="sxs-lookup"><span data-stu-id="338b6-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="338b6-133">Vent et øjeblik, mens der genereres et kort i meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="338b6-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="338b6-134">Når kortet vises, skal kortets indhold gennemgås omhyggeligt for alle følsomme oplysninger, før du sender meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="338b6-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="338b6-135">Dette trin er vigtigt, fordi alle i samtalen kan se kortet, når du har sendt meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="338b6-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="338b6-136">Hvis kortet ser flot ud, skal vælge **Send** for at sende det til samtalen.</span><span class="sxs-lookup"><span data-stu-id="338b6-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="338b6-137">Når kortet vises, og før du vælger **Send**, kan du slette den indsatte URL-adresse, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="338b6-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="338b6-138">Hvis du vil have vist flere detaljer eller foretage ændringer i posten, skal du vælge **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="338b6-138">To view more details or make changes to the record, select **Details**.</span></span>

    <span data-ttu-id="338b6-139">Siden detaljer svarer til det, du kan se i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="338b6-139">The details page is similar to what you'd see in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="338b6-140">Men det er en smule beskåret for grupper.</span><span class="sxs-lookup"><span data-stu-id="338b6-140">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="338b6-141">Når du er færdig med at gennemse og foretage ændringer, skal du lukke vinduet for at vende tilbage til samtalerne med team.</span><span class="sxs-lookup"><span data-stu-id="338b6-141">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="338b6-142">De ændringer, du foretager, afspejles ikke på kortet, før næste gang du indsætter et hyperlink til en samtale.</span><span class="sxs-lookup"><span data-stu-id="338b6-142">Any changes you make won't be reflected in the card until the next time you paste its link in a conversation.</span></span>

## <a name="see-also"></a><span data-ttu-id="338b6-143">Se også</span><span class="sxs-lookup"><span data-stu-id="338b6-143">See Also</span></span>

[<span data-ttu-id="338b6-144">Business Central og Microsoft Teams Oversigt over integration</span><span class="sxs-lookup"><span data-stu-id="338b6-144">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="338b6-145">[Installér appen [!INCLUDE [prodshort](includes/prodshort.md)] til Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="338b6-145">[Install the [!INCLUDE [prodshort](includes/prodshort.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="338b6-146">Udvikling af Teams-integration</span><span class="sxs-lookup"><span data-stu-id="338b6-146">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  
[<span data-ttu-id="338b6-147">Introduktion</span><span class="sxs-lookup"><span data-stu-id="338b6-147">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
