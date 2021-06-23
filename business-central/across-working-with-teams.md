---
title: Dele Business Central-poster i Microsoft Teams
description: Sådan bruger du Business central-app til Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 8add662badbc0d791d6a37d0feb4e3a756519f00
ms.sourcegitcommit: 5a916b0aa0a2eef0c22b5722a0af041757e6d7c2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/19/2021
ms.locfileid: "6074583"
---
# <a name="sharing-business-central-records-in-microsoft-teams"></a><span data-ttu-id="1a4d7-103">Dele Business Central-poster i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1a4d7-103">Sharing Business Central Records in Microsoft Teams</span></span>

[!INCLUDE [online_only](includes/online_only.md)]

<span data-ttu-id="1a4d7-104">[!INCLUDE [prod_short](includes/prod_short.md)] tilbyder en app, der har forbindelse Microsoft Teams til dine forretningsdata [!INCLUDE [prod_short](includes/prod_short.md)], så du hurtigt kan dele detaljer på tværs af gruppemedlemmer og reagere hurtigere på forespørgsler.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-104">[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries.</span></span> <span data-ttu-id="1a4d7-105">I denne artikel lærer du, hvordan du kan bruge appen til at dele [!INCLUDE [prod_short](includes/prod_short.md)]-poster, f. eks. en kunde, en salgsordre eller en faktura, med kolleger i en gruppesamtale.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-105">In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.</span></span>

## <a name="overview"></a><span data-ttu-id="1a4d7-106">Oversigt</span><span class="sxs-lookup"><span data-stu-id="1a4d7-106">Overview</span></span>

<span data-ttu-id="1a4d7-107">Med [!INCLUDE [prod_short](includes/prod_short.md)]-appen kan du:</span><span class="sxs-lookup"><span data-stu-id="1a4d7-107">The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:</span></span>

- <span data-ttu-id="1a4d7-108">Kopiere et hyperlink til en hvilken som helst Business Central-post og sætte den ind i en Teams-samtale, som du kan dele med dine kolleger.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-108">Copy a link to any Business Central record and paste it into a Teams conversation to share with your coworkers.</span></span> <span data-ttu-id="1a4d7-109">Appen udvider derefter linket til et kompakt, interaktivt kort, der viser oplysninger om posten.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-109">The app will then expand the link into a compact, interactive card that displays information about the record.</span></span>
- <span data-ttu-id="1a4d7-110">Når du er i samtalen, kan du og dine kolleger få vist flere oplysninger om posten, redigere data og handle - uden at forlade&mdash;Teams.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-110">Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.</span></span>

<span data-ttu-id="1a4d7-111">[![Teams-integration med Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1a4d7-111">[![Teams integration with Business Central](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1a4d7-112">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="1a4d7-112">Prerequisites</span></span>

- <span data-ttu-id="1a4d7-113">Du har adgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-113">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="1a4d7-114">Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i grupper.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-114">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="1a4d7-115">Du kan finde flere oplysninger i [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="1a4d7-115">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>

> [!NOTE]
> <span data-ttu-id="1a4d7-116">Alle deltagerne i en samtale med Teams vil kunne få vist kort til Business Central-poster, som du sender til samtalen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-116">All participants in a Teams conversation will be able to view cards for Business Central records that you submit to the conversation.</span></span> <span data-ttu-id="1a4d7-117">Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1a4d7-117">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1a4d7-118">Du kan finde flere oplysninger i [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="1a4d7-118">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="include-a-business-central-card-in-a-teams-conversation"></a><span data-ttu-id="1a4d7-119">Medtage et Business Central-kort i en samtale med Teams</span><span class="sxs-lookup"><span data-stu-id="1a4d7-119">Include a Business Central card in a Teams conversation</span></span>

1. <span data-ttu-id="1a4d7-120">Log ind [!INCLUDE [prod_short](includes/prod_short.md)] for at bruge browseren.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-120">Sign in to [!INCLUDE [prod_short](includes/prod_short.md)] using your browser.</span></span>
2. <span data-ttu-id="1a4d7-121">Åbn den post, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-121">Open the record that you want to share.</span></span>

    <span data-ttu-id="1a4d7-122">Appen er designet til at vise sider med korttyper fra [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1a4d7-122">The app is designed to display card type pages from [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1a4d7-123">Åbne en side, hvor der vises en enkelt post, f.eks. en vare, kunde eller salgsordre.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-123">So open a page that displays a single record, like an item, customer, or sales order.</span></span> <span data-ttu-id="1a4d7-124">Du kan ikke bruge den til rollecentre eller sider, hvor der vises flere poster på en liste.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-124">You can't use it for role centers or pages that display several records in a list.</span></span>

3. <span data-ttu-id="1a4d7-125">Kopiere hele URL-adressen fra browserens adresselinje.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-125">Copy the entire URL from the browser's address bar.</span></span>

   ![Kopiere Business Central URL-adresse fra browser](media/teams-url-v2.png)
4. <span data-ttu-id="1a4d7-127">Gå til Teams, og start en samtale, som kan chatte med en person, en gruppe personer eller en team-kanal.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-127">Go to Teams and start a conversation, which can be chat with a person, group of persons, or a team channel.</span></span>

    <!--Teams imposes a few limitations here eg. you cannot unfurl a link during a Voice/Video call :/ We should probably only mention this in a Troubleshooting section (and i hope it will also be fixed soon)-->
5. <span data-ttu-id="1a4d7-128">Indsætte URL-adressen i den meddelelsesboks, hvor du samler en meddelelse.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-128">Paste the URL in the message box where you compose a message.</span></span>

   ![Indsætte Business Central URL-adresse i Teams](media/teams-paste-url-v2.png)
6. <span data-ttu-id="1a4d7-130">Første gang du indsætter et hyperlink til en samtale, bliver du bedt om at logge på [!INCLUDE [prod_short](includes/prod_short.md)] og give appen tilladelse til at hente data.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-130">The first time you paste a link into a conversation, you'll be asked to sign in to [!INCLUDE [prod_short](includes/prod_short.md)] and give consent for the app to retrieve data.</span></span> <span data-ttu-id="1a4d7-131">Du skal blot følge vejledningen på skærmen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-131">Just follow the on-screen instructions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1a4d7-132">Du behøver kun at udføre dette trin én gang.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-132">You'll only have to do this step once.</span></span>

7. <span data-ttu-id="1a4d7-133">Vent et øjeblik, mens der genereres et kort i meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-133">Wait a moment while a card is generated in the message box.</span></span>

8. <span data-ttu-id="1a4d7-134">Når kortet vises, skal kortets indhold gennemgås omhyggeligt for alle følsomme oplysninger, før du sender meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-134">When the card appears, review the contents of the card carefully for any sensitive information before sending the message.</span></span> <span data-ttu-id="1a4d7-135">Dette trin er vigtigt, fordi alle i samtalen kan se kortet, når du har sendt meddelelsen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-135">This step is important because once you send the message, everyone in the conversation can see the card.</span></span>

9. <span data-ttu-id="1a4d7-136">Hvis kortet ser flot ud, skal vælge **Send** for at sende det til samtalen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-136">If the card looks good, select **Send** to submit it to the conversation.</span></span>

    > [!TIP]
    > <span data-ttu-id="1a4d7-137">Når kortet vises, og før du vælger **Send**, kan du slette den indsatte URL-adresse, hvis du vil.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-137">After the card appears, and before you select **Send**, you can delete the pasted URL if you like.</span></span>

10. <span data-ttu-id="1a4d7-138">Hvis du vil have vist flere detaljer eller foretage ændringer i posten, skal du vælge **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-138">To view more details or make changes to the record shown in the card, select **Details**.</span></span> <span data-ttu-id="1a4d7-139">Der er flere oplysninger i næste sektion.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-139">For more information, see the next section.</span></span>

## <a name="view-card-details"></a><span data-ttu-id="1a4d7-140">Vis kortdetaljer</span><span class="sxs-lookup"><span data-stu-id="1a4d7-140">View card details</span></span>

<span data-ttu-id="1a4d7-141">Når et kort er sendt til en samtale, kan alle deltagere med de [rette tilladelser](admin-teams-integration.md#permissions) vælge **Detaljer** for at åbne et vindue, der indeholder flere oplysninger om posten&mdash;og muligvis foretage ændringer af posten.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-141">Once a card's been sent to a conversation, all participants with the [proper permissions](admin-teams-integration.md#permissions) can select **Details** to open a window that displays more information about the record&mdash;and possibly make changes to the record.</span></span> <span data-ttu-id="1a4d7-142">Det betyder ikke noget, hvis du er det, der afsender kortet, eller den, der modtagerkortet.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-142">It doesn't matter if you're the one sending the card or the one receiving the card.</span></span> <span data-ttu-id="1a4d7-143">Funktionen **Detaljer** er især nyttig for modtagere, da den hurtigt leverer præcise, målrettede oplysninger om posten i modsætning til at skulle scanne hele posten.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-143">The **Details** feature is especially useful to recipients, because it quickly provides them with concise, targeted information about the record, as opposed to having to scan the full record.</span></span>

<span data-ttu-id="1a4d7-144">Vinduet Detaljer svarer til det, du kan se i posten [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1a4d7-144">The details window is similar to what you'd see in [!INCLUDE [prod_short](includes/prod_short.md)] the record.</span></span> <span data-ttu-id="1a4d7-145">Men det er en smule beskåret for grupper.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-145">But it's slightly trimmed for Teams.</span></span> <span data-ttu-id="1a4d7-146">Når du er færdig med at gennemse og foretage ændringer, skal du lukke vinduet for at vende tilbage til samtalerne med team.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-146">When you're finished viewing and making changes, close the window to return to the Teams conversation.</span></span>

<span data-ttu-id="1a4d7-147">Her er et par ting, du skal være opmærksom på, når du arbejder med kort detaljer:</span><span class="sxs-lookup"><span data-stu-id="1a4d7-147">Here are a couple things to keep in mind when working with the card details:</span></span>

- <span data-ttu-id="1a4d7-148">Hvis du vil åbne kortoplysninger, skal brugere have tilladelse på siden og data i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1a4d7-148">To open the card details, users must have permission on the page and its data in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span>
- <span data-ttu-id="1a4d7-149">Kort i Teams-chats opdateres ikke automatisk til ændringer.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-149">Cards in Teams chats aren't automatically updated to changes.</span></span> <span data-ttu-id="1a4d7-150">Alle de ændringer, du gemmer i en post i vinduet detaljer, gemmes i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1a4d7-150">Any changes you save to a record in the details window are saved in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1a4d7-151">Men kortet i Teams viser ikke ændringerne i konverteringen, før du indsætter kæden igen.</span><span class="sxs-lookup"><span data-stu-id="1a4d7-151">But the card in Teams won't show the changes in the conversion, until you paste the link again.</span></span>

<span data-ttu-id="1a4d7-152">Du kan få mere at vide om, hvordan du arbejder med kort og kort detaljer, i [Teams, ofte stillede spørgsmål](teams-faq.md).</span><span class="sxs-lookup"><span data-stu-id="1a4d7-152">To learn more about working with cards and card details, see [Teams FAQ](teams-faq.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a4d7-153">Se også</span><span class="sxs-lookup"><span data-stu-id="1a4d7-153">See Also</span></span>

[<span data-ttu-id="1a4d7-154">Business Central og Microsoft Teams Oversigt over integration</span><span class="sxs-lookup"><span data-stu-id="1a4d7-154">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="1a4d7-155">[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="1a4d7-155">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="1a4d7-156">Teams, ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="1a4d7-156">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="1a4d7-157">Fejlfinding i Teams</span><span class="sxs-lookup"><span data-stu-id="1a4d7-157">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="1a4d7-158">Udvikling af Teams-integration</span><span class="sxs-lookup"><span data-stu-id="1a4d7-158">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]