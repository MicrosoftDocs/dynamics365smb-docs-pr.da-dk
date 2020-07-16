---
title: Konfigurer maillogføring | Microsoft Docs
description: Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 07/01/2020
ms.author: bholtorf
ms.openlocfilehash: 9ca381bfebcd6db8e67d8153d4d2bc17eeffad81
ms.sourcegitcommit: f9aec4a72172d9270e14e2938c5550d69508f1aa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/02/2020
ms.locfileid: "3532665"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="1a405-103">Spore udveksling af mails mellem sælgere og kontakter</span><span class="sxs-lookup"><span data-stu-id="1a405-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>

<span data-ttu-id="1a405-104">Få mere ud af kommunikationen mellem sælgerne og dine eksisterende eller potentielle kunder ved at spore udveksling af mails og derefter ændre dem til handlingsrettede leads.</span><span class="sxs-lookup"><span data-stu-id="1a405-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1a405-105">kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser.</span><span class="sxs-lookup"><span data-stu-id="1a405-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="1a405-106">Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.</span><span class="sxs-lookup"><span data-stu-id="1a405-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

## <a name="set-up-public-folders-and-rules-for-email-logging-in-exchange-online"></a><span data-ttu-id="1a405-107">Konfigurere offentlige mapper og regler maillogføring i Exchange Online</span><span class="sxs-lookup"><span data-stu-id="1a405-107">Set up Public Folders and Rules for Email Logging in Exchange Online</span></span>

[!INCLUDE[admin-setup-email-public-folder](includes/admin-setup-email-public-folder.md)]

<span data-ttu-id="1a405-108">Derefter opretter du forbindelse mellem [!INCLUDE[prodshort](includes/prodshort.md)] og Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="1a405-108">Next, you connect [!INCLUDE[prodshort](includes/prodshort.md)] with Exchange Online.</span></span>

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="1a405-109">Oprette [!INCLUDE[d365fin](includes/d365fin_md.md)] til logføring af mails</span><span class="sxs-lookup"><span data-stu-id="1a405-109">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>

<span data-ttu-id="1a405-110">Introduktion til maillogføring i to lette trin:</span><span class="sxs-lookup"><span data-stu-id="1a405-110">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="1a405-111">Opret forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Exchange Online for dit Office 365-abonnement.</span><span class="sxs-lookup"><span data-stu-id="1a405-111">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="1a405-112">Exchange Online håndterer dine mails.</span><span class="sxs-lookup"><span data-stu-id="1a405-112">Exchange Online handles your email messages.</span></span> <span data-ttu-id="1a405-113">Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="1a405-113">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="1a405-114">Du skal blot bruge dine administratorrettigheder til din administratorkonto i Office 365.</span><span class="sxs-lookup"><span data-stu-id="1a405-114">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="1a405-115">Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter **Konfigurer maillogføring**.</span><span class="sxs-lookup"><span data-stu-id="1a405-115">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span>  

2. <span data-ttu-id="1a405-116">Kontrollér, at der er angivet gyldige mailadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] for dine sælgere og kontakter, afhængigt af om de er potentielle eller eksisterende kunder.</span><span class="sxs-lookup"><span data-stu-id="1a405-116">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="1a405-117">Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="1a405-117">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="1a405-118">Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="1a405-118">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="1a405-119">Søg efter **Marketingopsætning**, vælg **Proces**, derefter **Funktioner** og derefter **Valider opsætning af maillogføring**.</span><span class="sxs-lookup"><span data-stu-id="1a405-119">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="1a405-120">Få vist udveksling af mails i interaktionslogposten</span><span class="sxs-lookup"><span data-stu-id="1a405-120">Viewing Email Message Exchanges in the Interaction Log</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="1a405-121">opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail.</span><span class="sxs-lookup"><span data-stu-id="1a405-121">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="1a405-122">Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** eller **Sælger/indkøber** for personen, vælge **Naviger**, **Oversigt** og derefter vælge **Interaktionslogposter**.</span><span class="sxs-lookup"><span data-stu-id="1a405-122">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="1a405-123">Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f. eks.:</span><span class="sxs-lookup"><span data-stu-id="1a405-123">There are a few things we can do with each entry in the log, for example:</span></span>

- <span data-ttu-id="1a405-124">Få vist indholdet af den mail, der blev udvekslet, ved at klikke på handlingen **Vis vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="1a405-124">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
- <span data-ttu-id="1a405-125">Omdanne en mailudveksling til et salgs-lead – hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg.</span><span class="sxs-lookup"><span data-stu-id="1a405-125">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="1a405-126">Det gør du ved at vælge posten og derefter vælge handlingen **Opret lead**.</span><span class="sxs-lookup"><span data-stu-id="1a405-126">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="1a405-127">Du kan finde flere oplysninger under [Administrere salgsleads](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="1a405-127">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1a405-128">Se også</span><span class="sxs-lookup"><span data-stu-id="1a405-128">See Also</span></span>
[<span data-ttu-id="1a405-129">Styre relationer</span><span class="sxs-lookup"><span data-stu-id="1a405-129">Managing Relationships</span></span>](marketing-relationship-management.md)

