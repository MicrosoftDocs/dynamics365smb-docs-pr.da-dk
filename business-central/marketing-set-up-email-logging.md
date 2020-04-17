---
title: Konfigurer maillogføring | Microsoft Docs
description: Få at vide, hvordan du ændrer mailinteraktioner mellem sælgere og kunder til reelle salgs-leads.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect, opportunity, email
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: 13699c002402b6b6d32edc13dca3710fefff2129
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3181251"
---
# <a name="track-email-message-exchanges-between-salespeople-and-contacts"></a><span data-ttu-id="96fde-103">Spore udveksling af mails mellem sælgere og kontakter</span><span class="sxs-lookup"><span data-stu-id="96fde-103">Track Email Message Exchanges Between Salespeople and Contacts</span></span>
<span data-ttu-id="96fde-104">Få mere ud af kommunikationen mellem sælgerne og dine eksisterende eller potentielle kunder ved at spore udveksling af mails og derefter ændre dem til handlingsrettede leads.</span><span class="sxs-lookup"><span data-stu-id="96fde-104">Get more out of the communications between salespeople and your existing or potential customers by tracking email exchanges, and then turning them into actionable opportunities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="96fde-105">kan bruges sammen med Exchange Online til at føre en log over indgående og udgående meddelelser.</span><span class="sxs-lookup"><span data-stu-id="96fde-105">can work with Exchange Online to keep a log of the inbound and outbound messages.</span></span> <span data-ttu-id="96fde-106">Du kan få vist og analysere indholdet af hver meddelelse på siden **Interaktionslogposter**.</span><span class="sxs-lookup"><span data-stu-id="96fde-106">You can view and analyze the contents of each message on the **Interaction Log Entries** page.</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085401]

## <a name="setting-up-d365fin-to-log-email-messages"></a><span data-ttu-id="96fde-107">Oprette [!INCLUDE[d365fin](includes/d365fin_md.md)] til logføring af mails</span><span class="sxs-lookup"><span data-stu-id="96fde-107">Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)] to Log Email Messages</span></span>
<span data-ttu-id="96fde-108">Introduktion til maillogføring i to lette trin:</span><span class="sxs-lookup"><span data-stu-id="96fde-108">Get started with email logging in two easy steps:</span></span>

1. <span data-ttu-id="96fde-109">Opret forbindelse mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Exchange Online for dit Office 365-abonnement.</span><span class="sxs-lookup"><span data-stu-id="96fde-109">Connect [!INCLUDE[d365fin](includes/d365fin_md.md)] with Exchange Online for your Office 365 subscription.</span></span> <span data-ttu-id="96fde-110">Exchange Online håndterer dine mails.</span><span class="sxs-lookup"><span data-stu-id="96fde-110">Exchange Online handles your email messages.</span></span> <span data-ttu-id="96fde-111">Vi har gjort dette trin lettilgængeligt med en vejledning til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="96fde-111">We've made this step easy by providing an assisted setup guide.</span></span> <span data-ttu-id="96fde-112">Du skal blot bruge dine administratorrettigheder til din administratorkonto i Office 365.</span><span class="sxs-lookup"><span data-stu-id="96fde-112">You just need your administrator credentials for your administrator account in Office 365.</span></span> <span data-ttu-id="96fde-113">Start vejledningen ved at gå til **Assisteret opsætning**, og vælg derefter **Konfigurer maillogføring**.</span><span class="sxs-lookup"><span data-stu-id="96fde-113">To start the guide, go to **Assisted Setup**, and then choose **Set up email logging**.</span></span> 
2. <span data-ttu-id="96fde-114">Kontrollér, at der er angivet gyldige mailadresser i [!INCLUDE[d365fin](includes/d365fin_md.md)] for dine sælgere og kontakter, afhængigt af om de er potentielle eller eksisterende kunder.</span><span class="sxs-lookup"><span data-stu-id="96fde-114">Make sure that valid email addresses have been entered in [!INCLUDE[d365fin](includes/d365fin_md.md)] for your sales people and contacts, depending on whether they are potential or existing customers.</span></span> <span data-ttu-id="96fde-115">Hvis du vil gøre det, skal du for hver debitor eller sælger åbne kortet **Kontakt** eller **Sælger/indkøber** og se feltet **Mailadresse**.</span><span class="sxs-lookup"><span data-stu-id="96fde-115">To do that, for each customer or salesperson, open the **Contact** or **Salesperson/Purchaser** card and have a look in the **Email** field.</span></span>

> [!Tip]
> <span data-ttu-id="96fde-116">Når du har udført trinnene i programguiden, kan du kontrollere, om forbindelsen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="96fde-116">After you complete the steps in the guide you can check whether the connection was successful.</span></span> <span data-ttu-id="96fde-117">Søg efter **Marketingopsætning**, vælg **Proces**, derefter **Funktioner** og derefter **Valider opsætning af maillogføring**.</span><span class="sxs-lookup"><span data-stu-id="96fde-117">Search for **Marketing Setup**, choose **Process**, then **Functions**, and then **Validate Email Logging Setup**.</span></span>

## <a name="viewing-email-message-exchanges-in-the-interaction-log"></a><span data-ttu-id="96fde-118">Få vist udveksling af mails i interaktionslogposten</span><span class="sxs-lookup"><span data-stu-id="96fde-118">Viewing Email Message Exchanges in the Interaction Log</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="96fde-119">opretter en post på siden **Interaktionslog**, hver gang en sælger og en kontakt udveksler en mail.</span><span class="sxs-lookup"><span data-stu-id="96fde-119">creates an entry on the **Interaction Log** page each time a salesperson and a contact exchange an email message.</span></span> <span data-ttu-id="96fde-120">Du kan få vist interaktionsloggen ved at åbne kortet **Kontakt** eller **Sælger/indkøber** for personen, vælge **Naviger**, **Oversigt** og derefter vælge **Interaktionslogposter**.</span><span class="sxs-lookup"><span data-stu-id="96fde-120">To view the interaction log, open the **Contact** or **Salesperson\*Purchaser** card for the person, and then choose **Navigate**, **History**, and then choose **Interaction Log Entries**.</span></span> <span data-ttu-id="96fde-121">Der er nogle få ting, der kan udføres for hver indtastning i logfilen, f. eks.:</span><span class="sxs-lookup"><span data-stu-id="96fde-121">There are a few things we can do with each entry in the log, for example:</span></span>

* <span data-ttu-id="96fde-122">Få vist indholdet af den mail, der blev udvekslet, ved at klikke på handlingen **Vis vedhæftede filer**.</span><span class="sxs-lookup"><span data-stu-id="96fde-122">View the content of the email message that was exchanged by clicking the **Show Attachments** action.</span></span>
* <span data-ttu-id="96fde-123">Omdanne en mailudveksling til et salgs-lead – hvis en post ser lovende ud, kan du gøre den til en lead og derefter styre forløbet hen imod et salg.</span><span class="sxs-lookup"><span data-stu-id="96fde-123">Turn an email exchange into a sales opportunity - If an entry looks promising, you can turn it into an opportunity and then manage its progress toward a sale.</span></span> <span data-ttu-id="96fde-124">Det gør du ved at vælge posten og derefter vælge handlingen **Opret lead**.</span><span class="sxs-lookup"><span data-stu-id="96fde-124">To do that, choose the entry, and then choose the **Create Opportunity** action.</span></span> <span data-ttu-id="96fde-125">Du kan finde flere oplysninger under [Administrere salgsleads](marketing-manage-sales-opportunities.md).</span><span class="sxs-lookup"><span data-stu-id="96fde-125">For more information, see [Managing Sales Opportunities](marketing-manage-sales-opportunities.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="96fde-126">Se også</span><span class="sxs-lookup"><span data-stu-id="96fde-126">See Also</span></span>
[<span data-ttu-id="96fde-127">Styre relationer</span><span class="sxs-lookup"><span data-stu-id="96fde-127">Managing Relationships</span></span>](marketing-relationship-management.md)

