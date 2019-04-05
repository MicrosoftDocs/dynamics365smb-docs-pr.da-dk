---
title: Holde styr på målgrupper og de tilhørende interaktioner | Microsoft Docs
description: Få mere at vide om at oprette målgrupper for at definere grupper af kontaktpersoner og angive interaktioner for målgrupper.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 10/01/2018
ms.author: jswymer
ms.openlocfilehash: 1fcec3051fdabae818528742fba5d9ca57a721c8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793389"
---
# <a name="managing-interactions-for-segments"></a><span data-ttu-id="d848d-103">Administrere interaktioner for målgrupper</span><span class="sxs-lookup"><span data-stu-id="d848d-103">Managing Interactions for Segments</span></span>
<span data-ttu-id="d848d-104">Siden **Målgruppe** er en slags kladde, hvor du kan:</span><span class="sxs-lookup"><span data-stu-id="d848d-104">The **Segment** page is a type of worksheet where you can:</span></span>

* <span data-ttu-id="d848d-105">Oprette målgrupper.</span><span class="sxs-lookup"><span data-stu-id="d848d-105">Create segments.</span></span>
* <span data-ttu-id="d848d-106">Gemme de målgruppekriterier, som du har anvendt til at vælge kontakter.</span><span class="sxs-lookup"><span data-stu-id="d848d-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="d848d-107">Logge målgruppen og registrere interaktioner, som vedrører kontakterne i målgruppen.</span><span class="sxs-lookup"><span data-stu-id="d848d-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="d848d-108">Segmentering</span><span class="sxs-lookup"><span data-stu-id="d848d-108">Segmenting</span></span>
<span data-ttu-id="d848d-109">Du kan oprette målgrupper på flere forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="d848d-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="d848d-110">Du kan manuelt angive de kontakter, som du vil medtage i målgruppen på linjerne.</span><span class="sxs-lookup"><span data-stu-id="d848d-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="d848d-111">Du kan vælge kontakter.</span><span class="sxs-lookup"><span data-stu-id="d848d-111">You can select contacts.</span></span>
* <span data-ttu-id="d848d-112">Du kan genbruge en gemt målgruppe som grundlag for oprettelse af en ny.</span><span class="sxs-lookup"><span data-stu-id="d848d-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="d848d-113">Du kan genbruge gemte målgruppekriterier.</span><span class="sxs-lookup"><span data-stu-id="d848d-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="d848d-114">Interaktioner</span><span class="sxs-lookup"><span data-stu-id="d848d-114">Interactions</span></span>
<span data-ttu-id="d848d-115">På siden **Målgruppe** kan du oprette interaktioner for flere kontakter samtidigt.</span><span class="sxs-lookup"><span data-stu-id="d848d-115">On the **Segment** page, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="d848d-116">Du kan f.eks. flette en målgruppe sammen med et Microsoft Word-dokument, så du kan sende et brev til alle kontakterne i målgruppen.</span><span class="sxs-lookup"><span data-stu-id="d848d-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="d848d-117">Du kan angive oplysninger om interaktion for målgruppen på **Målgruppe** hovedet.</span><span class="sxs-lookup"><span data-stu-id="d848d-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="d848d-118">Du kan f.eks. bestemme, hvilken interaktionsskabelon du ønsker at bruge for alle kontakter, angive en beskrivelse, en korrespondancetype osv.</span><span class="sxs-lookup"><span data-stu-id="d848d-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="d848d-119">Du kan dog ændre disse oplysninger i målgruppelinjen for hver enkelt kontakt ved f.eks. at angive en anden beskrivelse for en kontakt.</span><span class="sxs-lookup"><span data-stu-id="d848d-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="d848d-120">Hvis du fletter en målgruppe med et Microsoft Word-dokument, kan du tilpasse dokumentet, der skal sendes til en eller flere af kontakterne i målgruppen, f.eks. ved tilføjelse af individuelle kommentarer i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="d848d-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="d848d-121">Logføring</span><span class="sxs-lookup"><span data-stu-id="d848d-121">Logging</span></span>
<span data-ttu-id="d848d-122">Når du vælger **Log** på siden **Målgruppe**, registrerer programmet interaktioner på siden **Interaktionslogpost**, og målgruppen registreres i loggen.</span><span class="sxs-lookup"><span data-stu-id="d848d-122">On the **Segment** page, when you choose **Log**, the application records the interactions on the **Interaction Log Entry** page, and logs the segment.</span></span> <span data-ttu-id="d848d-123">Når du har registreret målgruppen i loggen, kan du kun finde den på siden **Gemte målgrupper**.</span><span class="sxs-lookup"><span data-stu-id="d848d-123">After you have logged the segment, you can only find it on the **Logged Segments** page.</span></span>

<span data-ttu-id="d848d-124">På siden **Logførte målgrupper**, kan du vælge at oprette en opfølgende målgruppe, der indeholder de samme kontaktpersoner som den målgruppe, du har logget.</span><span class="sxs-lookup"><span data-stu-id="d848d-124">On the **Logged Segments** page, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="d848d-125">Se også</span><span class="sxs-lookup"><span data-stu-id="d848d-125">See Also</span></span>
[<span data-ttu-id="d848d-126">Oprette målgrupper</span><span class="sxs-lookup"><span data-stu-id="d848d-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="d848d-127">Oprette interaktioner til målgrupper</span><span class="sxs-lookup"><span data-stu-id="d848d-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="d848d-128">Administrere målgrupper</span><span class="sxs-lookup"><span data-stu-id="d848d-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="d848d-129">Registrering af interaktioner med kontakter</span><span class="sxs-lookup"><span data-stu-id="d848d-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="d848d-130">Administrere salgsleads</span><span class="sxs-lookup"><span data-stu-id="d848d-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="d848d-131">Oprette og administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="d848d-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="d848d-132">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="d848d-132">Working with Business Central</span></span>](ui-work-product.md)
