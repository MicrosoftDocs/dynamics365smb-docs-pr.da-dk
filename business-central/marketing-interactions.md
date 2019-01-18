---
title: Administrere interaktioner med dine kontakter | Microsoft Docs
description: "Du kan administrere alle typer kommunikation eller interaktioner mellem din virksomhed og dine kontakter, f.eks. kommunikation via brev, telefon, møder osv."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 6fa95883e30b7912ed2b6b22f40cbcd5af339f31
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="managing-interactions-with-contacts"></a><span data-ttu-id="e6fa2-103">Administration af interaktioner med kontakter</span><span class="sxs-lookup"><span data-stu-id="e6fa2-103">Managing Interactions With Contacts</span></span>
<span data-ttu-id="e6fa2-104">I [!INCLUDE[d365fin](includes/d365fin_md.md)] er interaktioner alle typer kommunikation mellem din virksomhed og dine kontakter.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-104">In [!INCLUDE[d365fin](includes/d365fin_md.md)], interactions are all types of communications between your company and your contacts.</span></span> <span data-ttu-id="e6fa2-105">F.eks. kan kommunikation foregå via brev, fax, mail, telefon, møder osv.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-105">For example, communications can be by letter, fax, email, telephone, meetings, and so on.</span></span>

<span data-ttu-id="e6fa2-106">I relationsstyringsområdet kan du registrere alle de interaktioner, du har med kontakter. Det sætter dig i stand til at holde styr på de salgs- og marketingstiltag, du har iværksat i forbindelse med kontakterne, og til at forbedre de fremtidige forretningsinteraktioner med dem.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-106">The relationship management area enables you to record all the interactions you have with your contacts in order to keep track of the sales and marketing efforts you have directed at your contacts and to improve your future business interactions with them.</span></span> <span data-ttu-id="e6fa2-107">Konfiguration af programmet til at registrere interaktioner består af disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="e6fa2-107">Setting up your application to record interactions consists of these tasks:</span></span>

* <span data-ttu-id="e6fa2-108">Konfiguration af interaktionsskabeloner</span><span class="sxs-lookup"><span data-stu-id="e6fa2-108">Setting up interaction templates</span></span>  
* <span data-ttu-id="e6fa2-109">Oprettelse af interaktioner i kontakter eller målgrupper</span><span class="sxs-lookup"><span data-stu-id="e6fa2-109">Creating interactions on contacts or segments</span></span>  
* <span data-ttu-id="e6fa2-110">Få vist og administrere registrerede interaktioner</span><span class="sxs-lookup"><span data-stu-id="e6fa2-110">View and manage recorded interactions</span></span>  

##  <a name="setting-up-interaction-templates"></a><span data-ttu-id="e6fa2-111">Konfiguration af interaktionsskabeloner</span><span class="sxs-lookup"><span data-stu-id="e6fa2-111">Setting up Interaction Templates</span></span>
<span data-ttu-id="e6fa2-112">Du skal konfigurere interaktionsskabeloner, før du kan oprette og registrere interaktioner.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-112">Before you can create and record interactions, you must set up interaction templates.</span></span> <span data-ttu-id="e6fa2-113">Når du skal oprette interaktioner, skal du angive de skabeloner, som interaktionerne er baseret på.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-113">When creating interactions, you must specify the interaction templates they are based on.</span></span> <span data-ttu-id="e6fa2-114">En interaktionsskabelon en model, der definerer grundlæggende karakteristika for en interaktion.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-114">An interaction template is a model that defines the basic characteristics of an interaction.</span></span>
<span data-ttu-id="e6fa2-115">Du konfigurerer en interaktionsskabelon på siden **Interaktionsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-115">You set up an interaction template on the **Interaction Templates** page.</span></span>

<span data-ttu-id="e6fa2-116">Når du er færdig med at indtaste oplysninger om interaktionsskabelonen, kan du oprette en vedhæftet fil, f.eks. et Microsoft Word-dokument.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-116">After you have entered information about the interaction template, you can create an attachment, for example, a Microsoft Word document.</span></span> <span data-ttu-id="e6fa2-117">Gentag trinnene for hver interaktionsskabelon, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-117">Repeat the steps to set up as many interaction templates as you want.</span></span>  

## <a name="creating-interactions"></a><span data-ttu-id="e6fa2-118">Oprette interaktioner</span><span class="sxs-lookup"><span data-stu-id="e6fa2-118">Creating Interactions</span></span>
<span data-ttu-id="e6fa2-119">Interaktioner kan registreres på to måder:</span><span class="sxs-lookup"><span data-stu-id="e6fa2-119">There are two ways of recording interactions:</span></span>

* <span data-ttu-id="e6fa2-120">Du kan oprette interaktioner manuelt, der er knyttet til en enkelt kontakt eller en målgruppe.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-120">You can manually create interactions that are linked to a single contact or to a segment.</span></span> <span data-ttu-id="e6fa2-121">Du kan finde flere oplysninger i [Oprette interaktioner for kontakter og målgrupper](marketing-how-create-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="e6fa2-121">For more information, see [Create Interactions on Contacts and Segments](marketing-how-create-interactions.md).</span></span>  
* <span data-ttu-id="e6fa2-122">Du kan automatisk registrere interaktioner, når du udfører handlinger i programmet, f.eks. når du udskriver en faktura eller et tilbud.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-122">You can automatically record interactions when you perform actions in the application, for example, when you print an invoice, or quote.</span></span> <span data-ttu-id="e6fa2-123">Du kan finde flere oplysninger i [Automatisk registrere interaktioner med kontakter](marketing-auto-record-interactions.md).</span><span class="sxs-lookup"><span data-stu-id="e6fa2-123">For more information, see [Automatically Record Interactions with Contacts](marketing-auto-record-interactions.md).</span></span>

## <a name="viewing-and-managing-recorded-interactions"></a><span data-ttu-id="e6fa2-124">Visning og administration af registrerede interaktioner</span><span class="sxs-lookup"><span data-stu-id="e6fa2-124">Viewing and Managing Recorded Interactions</span></span>
<span data-ttu-id="e6fa2-125">Brug siden **Interaktionslogposter** til at se alle de registrerede interaktioner, som ikke er blevet slettet.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-125">You can view all the recorded interactions that have not been deleted on the **Interaction Log Entries** page.</span></span> <span data-ttu-id="e6fa2-126">Du kan åbne siden ved at:</span><span class="sxs-lookup"><span data-stu-id="e6fa2-126">You can open this page by:</span></span>

* <span data-ttu-id="e6fa2-127">Bruge ikonet **Søg efter side eller rapport** til at søge på **Interaktionslogposter**.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-127">Using the **Search for Page or Report** icon to search on **Interaction Log Entries**.</span></span>
* <span data-ttu-id="e6fa2-128">Vælge handlingen **Interaktionslogposter** i en kontakt eller en målgruppe.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-128">Choosing the **Interaction Log Entries** action on a contact or segment.</span></span>
  <span data-ttu-id="e6fa2-129">Siden **Interaktionslogpost** indeholder både de interaktioner, du opretter manuelt, og dem, som registreres automatisk af programmet.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-129">The **Interaction Log Entry** page contains the interactions you create manually and the interactions that the application records automatically.</span></span>

<span data-ttu-id="e6fa2-130">På denne side kan du:</span><span class="sxs-lookup"><span data-stu-id="e6fa2-130">In this page, you can:</span></span>

* <span data-ttu-id="e6fa2-131">Få vist status for interaktioner.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-131">View the status of interactions.</span></span>
* <span data-ttu-id="e6fa2-132">Markere interaktioner som annulleret.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-132">Mark interactions as canceled.</span></span>

<span data-ttu-id="e6fa2-133">Du kan slette interaktionslogposter, der er blevet annulleret.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-133">You can delete interaction log entries that have been canceled.</span></span> <span data-ttu-id="e6fa2-134">For at slette interaktionslogposter skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Slet annullerede interaktionslogposter** og derefter vælge det relaterede link og angive oplysningerne.</span><span class="sxs-lookup"><span data-stu-id="e6fa2-134">To delete interaction log entries, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Canceled Interaction Log Entries**, and then choose the related link, and then fill in the information.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6fa2-135">Se også</span><span class="sxs-lookup"><span data-stu-id="e6fa2-135">See Also</span></span>
[<span data-ttu-id="e6fa2-136">Administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="e6fa2-136">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="e6fa2-137">Administrere salgsleads</span><span class="sxs-lookup"><span data-stu-id="e6fa2-137">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="e6fa2-138">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="e6fa2-138">Working with Business Central</span></span>](ui-work-product.md)  

