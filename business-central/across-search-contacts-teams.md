---
title: Søgning efter kontakter fra Microsoft Teams
description: Få mere at vide om, hvordan du kan søge efter Business Central-debitorer, -kreditorer og andre kontakter fra Microsoft Teams.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, contacts, search, messaging extensions
ms.date: 04/12/2021
ms.author: jswymer
ms.openlocfilehash: 6d094e365ad0c7da73467e5a3160d926902c45d9
ms.sourcegitcommit: c11ad91a389ed72532f5513654fdc7909b20aed9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/22/2021
ms.locfileid: "5935157"
---
# <a name="searching-for-customers-vendors-and-other-contacts-from-microsoft-teams"></a><span data-ttu-id="6c08c-103">Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6c08c-103">Searching for Customers, Vendors, and Other Contacts from Microsoft Teams</span></span>

<span data-ttu-id="6c08c-104">[!INCLUDE [online_only](includes/online_only.md)].</span><span class="sxs-lookup"><span data-stu-id="6c08c-104">[!INCLUDE [online_only](includes/online_only.md)].</span></span> <span data-ttu-id="6c08c-105">Introduceret i 2021 udgivelsesbølge 1.</span><span class="sxs-lookup"><span data-stu-id="6c08c-105">Introduced in 2021 release wave 1.</span></span>

<span data-ttu-id="6c08c-106">[!INCLUDE [prod_short](includes/prod_short.md)] har et omfattende system til styring af virksomhedskontakter, som er afgørende for brugere inden for salg, drift eller andre afdelinger.</span><span class="sxs-lookup"><span data-stu-id="6c08c-106">[!INCLUDE [prod_short](includes/prod_short.md)] has a comprehensive business contact management system that is essential for users in sales, operations, or other departmental roles.</span></span> <span data-ttu-id="6c08c-107">Hvis du bruger en af disse roller, er du ofte nødt til at søge efter, mødes med eller starte en samtale med dine kreditorer, debitorer og andre kontakter.</span><span class="sxs-lookup"><span data-stu-id="6c08c-107">If you're a user in one of these roles, you'll often need to look up, meet, or start a conversation with your vendors, customers, and other contacts.</span></span> <span data-ttu-id="6c08c-108">Med appen [!INCLUDE [prod_short](includes/prod_short.md)] til Teams kan du udføre disse opgaver direkte fra Teams uden at skulle skifte til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c08c-108">With the [!INCLUDE [prod_short](includes/prod_short.md)] app for Teams, you can do these tasks directly from Teams, without having to switch to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c08c-109">I Teams kan du:</span><span class="sxs-lookup"><span data-stu-id="6c08c-109">From within Teams, you can:</span></span>

- <span data-ttu-id="6c08c-110">Søge efter [!INCLUDE [prod_short](includes/prod_short.md)]-kontakter fra Teams-kommandoboksen eller meddelelsesområdet.</span><span class="sxs-lookup"><span data-stu-id="6c08c-110">Look up [!INCLUDE [prod_short](includes/prod_short.md)] contacts from the Teams command box or from the message compose area.</span></span> <span data-ttu-id="6c08c-111">Kontakter kan omfatte kundeemner, kreditorer, debitorer eller andre virksomhedsrelationer.</span><span class="sxs-lookup"><span data-stu-id="6c08c-111">Contacts can include prospects, vendors, customers, or other business relationships.</span></span>
- <span data-ttu-id="6c08c-112">Dele en kontaktperson som et kort i en Teaks-samtale.</span><span class="sxs-lookup"><span data-stu-id="6c08c-112">Share a contact as a card in a Teams conversation.</span></span>
- <span data-ttu-id="6c08c-113">Få vist detaljer om kontakt, interaktionshistorik og anden indsigt som f.eks. udestående betalinger eller åbne dokumenter.</span><span class="sxs-lookup"><span data-stu-id="6c08c-113">View details about the contact, interaction history, and other insights like outstanding payments or open documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6c08c-114">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="6c08c-114">Prerequisites</span></span>

- <span data-ttu-id="6c08c-115">Du har adgang til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6c08c-115">You have access to Microsoft Teams.</span></span>
- <span data-ttu-id="6c08c-116">Du har installeret [!INCLUDE [prod_short](includes/prod_short.md)]-appen i Teams.</span><span class="sxs-lookup"><span data-stu-id="6c08c-116">You've installed the [!INCLUDE [prod_short](includes/prod_short.md)] app in Teams.</span></span> <span data-ttu-id="6c08c-117">Du kan finde flere oplysninger i [Installere [!INCLUDE [prod_short](includes/prod_short.md)]-app til Microsoft Teams](across-install-app-for-teams.md).</span><span class="sxs-lookup"><span data-stu-id="6c08c-117">For more information, see [Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>
- <span data-ttu-id="6c08c-118">Du har en [!INCLUDE [prod_short](includes/prod_short.md)]-konto med adgang til kontakter i mindst én virksomhed.</span><span class="sxs-lookup"><span data-stu-id="6c08c-118">You've got a [!INCLUDE [prod_short](includes/prod_short.md)] account with access to contacts in at least one company.</span></span>

> [!NOTE]
> <span data-ttu-id="6c08c-119">Hvis du søger fra kommandoboksen eller meddelelsesboksen, kan du blive bedt om at logge på eller konfigurere appen første gang.</span><span class="sxs-lookup"><span data-stu-id="6c08c-119">Whether you searching from the command box or message compose box, you may be asked to sign in or set up the app the first time.</span></span> <span data-ttu-id="6c08c-120">Dette trin er nødvendigt, hvis du vil søge efter kontakter i den rette Business Central-virksomhed.</span><span class="sxs-lookup"><span data-stu-id="6c08c-120">This step is necessary to search for contacts in the right Business Central company.</span></span> <span data-ttu-id="6c08c-121">Du kan finde oplysninger om, hvordan du konfigurerer appen til at vælge virksomheden, i [Skift af regnskab og andre indstillinger i Teams](across-teams-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6c08c-121">For information about setting up the app to choose your company, see [Changing Company and Other Settings in Teams](across-teams-settings.md).</span></span>

## <a name="look-up-contacts-from-the-command-box"></a><span data-ttu-id="6c08c-122">Søge efter kontakter fra kommandoboksen</span><span class="sxs-lookup"><span data-stu-id="6c08c-122">Look up contacts from the command box</span></span>

<span data-ttu-id="6c08c-123">Kommandoboksen er placeret øverst i alle skærmbilleder i Teams.</span><span class="sxs-lookup"><span data-stu-id="6c08c-123">The command box is at the top of every screen in Teams.</span></span> <span data-ttu-id="6c08c-124">Det gør det muligt at søge efter, udføre hurtige handlinger eller starte apps som f.eks. appen [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c08c-124">It lets you search, take quick actions, or launch apps, like the [!INCLUDE [prod_short](includes/prod_short.md)] app.</span></span> <span data-ttu-id="6c08c-125">Søgning fra kommandoboksen er perfekt til hurtig søgning efter kontakter og deres relaterede data til egen brug.</span><span class="sxs-lookup"><span data-stu-id="6c08c-125">Searching from the command box is great for quickly looking up contacts and their related data for your own use.</span></span> <span data-ttu-id="6c08c-126">Antag f.eks., at du vil søge efter en mailadresse for en leverandør for at oprette et kalendermøde.</span><span class="sxs-lookup"><span data-stu-id="6c08c-126">For example, suppose you want to look up an email address of a vendor to set up a calendar meeting.</span></span> <span data-ttu-id="6c08c-127">Eller måske vil du søge efter interaktionshistorikken under et møde med en kunde.</span><span class="sxs-lookup"><span data-stu-id="6c08c-127">Or maybe you want to look up interaction history during a meeting with a customer.</span></span>

1. <span data-ttu-id="6c08c-128">Skriv **@Business Central** i kommandoboksen, og vælg derefter Business Central-appen fra resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6c08c-128">In the command box, type **@Business Central**, then select the Business Central app from the results.</span></span>

    ![Åbn Business Central-appen for at søge efter kontakter fra kommandoboksen](media/teams-contacts-command-1.png)

2. <span data-ttu-id="6c08c-130">Begynd at indtaste søgetekst som f.eks. et navn, en adresse eller et telefonnummer i boksen **Business Central**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-130">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="6c08c-131">Mens du indtaster, vises matchende resultater.</span><span class="sxs-lookup"><span data-stu-id="6c08c-131">As you type, matching results will appear.</span></span>

    ![Søge efter Business Central-kontakter fra kommandoboksen i Teams](media/teams-contacts-command-2.png)
3. <span data-ttu-id="6c08c-133">Vælg en kontakt fra resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6c08c-133">Select a contact from the results.</span></span>

    <span data-ttu-id="6c08c-134">Kontaktkortet vises under kommandoboksen.</span><span class="sxs-lookup"><span data-stu-id="6c08c-134">The contact card appears beneath the command box.</span></span>

4. <span data-ttu-id="6c08c-135">Hvis du vil føje et kontaktkort til en samtale, skal du gå til øverste højre hjørne af kortet og vælge **... (Flere indstillinger)** > **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-135">If you want to add the contact card into a conversation, go to the upper right corner of the card, select **... (More options)** > **Copy**.</span></span> <span data-ttu-id="6c08c-136">Indsæt derefter kopien i meddelelsesboksen til en samtale.</span><span class="sxs-lookup"><span data-stu-id="6c08c-136">Then, paste the copy in the message compose box of a conversation.</span></span>  

<span data-ttu-id="6c08c-137">Du kan finde generelle oplysninger om kommandoboksen i Teams i [Teams - Bruge kommandoboksen](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span><span class="sxs-lookup"><span data-stu-id="6c08c-137">For more general information about the command box in Teams, see [Teams - Use the command box](https://support.microsoft.com/en-us/office/use-the-command-box-13c4e429-7324-4886-b377-5dbed539193b).</span></span>

## <a name="look-up-contacts-from-the-message-compose-box"></a><span data-ttu-id="6c08c-138">Søge efter kontakter fra meddelelsesboksen</span><span class="sxs-lookup"><span data-stu-id="6c08c-138">Look up contacts from the message compose box</span></span>

<span data-ttu-id="6c08c-139">Fordelen ved at bruge meddelelsesboksen er, at du kan tilføje et kontaktkort direkte til en samtale, så andre kan se det.</span><span class="sxs-lookup"><span data-stu-id="6c08c-139">The advantage of using the message compose box is that you can add a contact card directly to a conversation, for others to see.</span></span>

1. <span data-ttu-id="6c08c-140">Vælg ikonet for **Business Central** for at starte appen under meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="6c08c-140">Beneath to message compose box, select the **Business Central** icon to launch the app.</span></span>

    <span data-ttu-id="6c08c-141">Hvis du ikke kan se ikonet for **Business Central**, skal du vælge **... (Meddelelsesudvidelser)**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-141">If you don't see the **Business Central** icon, select **... (Messaging extensions)**.</span></span>

    ![Åbn Business Central-appen for at søge efter kontakter fra meddelelsesboksen](media/teams-contacts-message-box.png)

2. <span data-ttu-id="6c08c-143">Begynd at indtaste søgetekst som f.eks. et navn, en adresse eller et telefonnummer i boksen **Business Central**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-143">In the **Business Central** box, start typing search text, like a name, address, or phone number.</span></span>

    <span data-ttu-id="6c08c-144">Mens du indtaster, vises matchende resultater.</span><span class="sxs-lookup"><span data-stu-id="6c08c-144">As you type, matching results will appear.</span></span>

    ![Søge efter Business Central-kontakter fra meddelelsesboksen](media/teams-contacts-5.png)
3. <span data-ttu-id="6c08c-146">Vælg en kontakt fra resultaterne.</span><span class="sxs-lookup"><span data-stu-id="6c08c-146">Select a contact from the results.</span></span>

    <span data-ttu-id="6c08c-147">Kontaktkortet vises i meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="6c08c-147">The contact card appears in the message compose box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c08c-148">Kontaktkortet sendes ikke med det samme til samtalen, hvor andre kan se det.</span><span class="sxs-lookup"><span data-stu-id="6c08c-148">The contact card isn't sent to the conversation right away for others to see.</span></span> <span data-ttu-id="6c08c-149">Du har mulighed for at gennemgå indholdet af kortet og tilføje tekst efter ønske før og efter det er sendt.</span><span class="sxs-lookup"><span data-stu-id="6c08c-149">You have the opportunity to review the contents of the card, and add text before or after it as you like.</span></span> <span data-ttu-id="6c08c-150">Send derefter meddelelsen til chatten, når du er klar.</span><span class="sxs-lookup"><span data-stu-id="6c08c-150">Then, send your message to the chat when ready.</span></span>

### <a name="heres-another-way"></a><span data-ttu-id="6c08c-151">En anden metode</span><span class="sxs-lookup"><span data-stu-id="6c08c-151">Here's another way</span></span>

1. <span data-ttu-id="6c08c-152">I stedet for at bruge ikonet for **Business Central** skal du skrive **@Business Central** direkte i meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="6c08c-152">Instead of using the **Business Central** icon, type **@Business Central** directly in the message compose box.</span></span>
2. <span data-ttu-id="6c08c-153">Indtast dine søgeord i feltet.</span><span class="sxs-lookup"><span data-stu-id="6c08c-153">Enter your search terms in the box.</span></span>
3. <span data-ttu-id="6c08c-154">Brug piletasterne Op og Ned på tastaturet til at vælge en kontakt, og tryk derefter på Enter for at vælge kontakten.</span><span class="sxs-lookup"><span data-stu-id="6c08c-154">Use the up and down arrow keys on the keyboard to choose a contact, then press Enter to select it.</span></span>

## <a name="viewing-contact-card-details"></a><span data-ttu-id="6c08c-155">Visning af oplysninger fra visitkort</span><span class="sxs-lookup"><span data-stu-id="6c08c-155">Viewing contact card details</span></span>

<span data-ttu-id="6c08c-156">Kontaktkortet i Teams giver dig et hurtigt overblik over debitoren, kreditoren eller kontaktpersonen.</span><span class="sxs-lookup"><span data-stu-id="6c08c-156">The contact card in Teams gives you a quick overview of the customer, vendor, or contact.</span></span> <span data-ttu-id="6c08c-157">Kortet er interaktivt&mdash;hvilket betyder, at du kan få vist flere oplysninger eller ændre en kontakt ved hjælp af knapperne **Detaljer** eller **Pop-op**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-157">The card is interactive&mdash;meaning you can view more information or even modify a contact by using the **Details** or **Pop-out** buttons.</span></span>

<span data-ttu-id="6c08c-158">Knappen **Detaljer** åbner et vindue i Teams med flere oplysninger om kontakten, men ikke så mange oplysninger som i [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c08c-158">The **Details** button opens a window within Teams that displays more information about the contact, but not as much as you'd see in [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c08c-159">Hvis du vil se alle oplysninger om en kontakt i [!INCLUDE [prod_short](includes/prod_short.md)], skal du vælge **Pop-op**.</span><span class="sxs-lookup"><span data-stu-id="6c08c-159">To see all the information about a contact in [!INCLUDE [prod_short](includes/prod_short.md)], select **Pop-out**.</span></span>

<span data-ttu-id="6c08c-160">Kontaktkortet fungerer på samme måde som kort for poster, f.eks. varer, debitorer eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="6c08c-160">The contact card works just like cards for records, like items, customers, or sales orders.</span></span> <span data-ttu-id="6c08c-161">Du kan finde flere oplysninger om kort i [Vise kortoplysninger](across-working-with-teams.md#view-card-details).</span><span class="sxs-lookup"><span data-stu-id="6c08c-161">For more information about cards, see [View card details](across-working-with-teams.md#view-card-details).</span></span>

> [!NOTE]
> <span data-ttu-id="6c08c-162">Alle deltagerne i en Teams-samtale kan få vist kort for den Business Central-kontakt, som du sender til en samtale.</span><span class="sxs-lookup"><span data-stu-id="6c08c-162">All participants in a Teams conversation will be able to view cards for Business Central contact that you submit to a conversation.</span></span> <span data-ttu-id="6c08c-163">Men hvis du vil have vist flere detaljer om poster, bruge **Detaljer** eller **Pop-op**-knapper på et kort, skal de have adgang til [!INCLUDE [prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6c08c-163">But to view more details about records, by using the **Details** or **Pop out** buttons on a card, they'll need access to [!INCLUDE [prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6c08c-164">Du kan finde flere oplysninger i [Administrere Microsoft Teams-integration](admin-teams-integration.md#minimum-requirements-1).</span><span class="sxs-lookup"><span data-stu-id="6c08c-164">For more information, see [Managing Microsoft Teams Integration](admin-teams-integration.md#minimum-requirements-1).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c08c-165">Se også</span><span class="sxs-lookup"><span data-stu-id="6c08c-165">See Also</span></span>

[<span data-ttu-id="6c08c-166">Business Central og Microsoft Teams Oversigt over integration</span><span class="sxs-lookup"><span data-stu-id="6c08c-166">Business Central and Microsoft Teams Integration Overview</span></span>](across-teams-overview.md)  
<span data-ttu-id="6c08c-167">[Installér appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)</span><span class="sxs-lookup"><span data-stu-id="6c08c-167">[Install the [!INCLUDE [prod_short](includes/prod_short.md)] App for Microsoft Teams](across-install-app-for-teams.md)</span></span>  
[<span data-ttu-id="6c08c-168">Teams, ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="6c08c-168">Teams FAQ</span></span>](teams-faq.md)  
[<span data-ttu-id="6c08c-169">Fejlfinding i Teams</span><span class="sxs-lookup"><span data-stu-id="6c08c-169">Troubleshooting Teams</span></span>](admin-teams-troubleshooting.md)  
[<span data-ttu-id="6c08c-170">Udvikling af Teams-integration</span><span class="sxs-lookup"><span data-stu-id="6c08c-170">Developing for Teams Integration</span></span>](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]