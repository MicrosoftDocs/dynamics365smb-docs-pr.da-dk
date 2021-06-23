---
title: Bruge Microsoft Word-skabeloner til massekommunikation | Microsoft Docs
description: Word-skabeloner kan gøre det nemmere at masseoprette dokumenter, der er tilpasset bestemte objekter.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110950"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="71dce-103">Bruge Word-skabeloner til massekommunikation</span><span class="sxs-lookup"><span data-stu-id="71dce-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="71dce-104">Microsoft Word-skabeloner kan gøre det nemmere at massekommunikere med objekter som f.eks. debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="71dce-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="71dce-105">Du kan f.eks. oprette brochurer, som giver debitorer besked om en salgskampagne, breve til kreditorer om en ny indkøbspolitik eller invitationer, der skal tiltrække kontakter til et kommende arrangement.</span><span class="sxs-lookup"><span data-stu-id="71dce-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="71dce-106">Du kan kun bruge Word-skabeloner på enheder med Microsoft Word 2019 og Windows-operativsystemet installeret.</span><span class="sxs-lookup"><span data-stu-id="71dce-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="71dce-107">Du kan bruge objekter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for skabelonen og til at tilføje fletfelter for at tilpasse dokumenter til de enkelte objekter.</span><span class="sxs-lookup"><span data-stu-id="71dce-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="71dce-108">Fletfelterne hentes fra objektet i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="71dce-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="71dce-109">Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="71dce-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="71dce-110">På siden **Word-skabeloner** kan du bruge en vejledning om assisteret opsætning for at hente en zip-fil, der indeholder filen DataSource.txt og en Word-skabelonfil til et objekt.</span><span class="sxs-lookup"><span data-stu-id="71dce-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="71dce-111">Når du har oprettet skabelonen og tilføjet fletfelter, bruger du den samme vejledning til at overføre skabelonen.</span><span class="sxs-lookup"><span data-stu-id="71dce-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="71dce-112">Du kan kun bruge den Word-skabelon og de datakildefiler, som du henter fra [!INCLUDE[prod_short](includes/prod_short.md)], og du skal gemme filerne på den samme placering.</span><span class="sxs-lookup"><span data-stu-id="71dce-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="71dce-113">Når du vælger et objekt, som du vil oprette en skabelon for, viser listen alle objekter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="71dce-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="71dce-114">Du kan dog ikke oprette skabeloner for alle objekter.</span><span class="sxs-lookup"><span data-stu-id="71dce-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="71dce-115">Hvis navnet på et objekt indeholder specialtegn som f.eks **/**, **.**, **_** eller **-**, kan du ikke oprette en skabelon for det.</span><span class="sxs-lookup"><span data-stu-id="71dce-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="71dce-116">Navnet på objektet vises i kolonnen **Objekttitel**.</span><span class="sxs-lookup"><span data-stu-id="71dce-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="71dce-117">Når du opretter skabelonen i Word, kan du tilføje fletfelter på fanen **Forsendelser** ved at vælge **Indsæt fletfelt**.</span><span class="sxs-lookup"><span data-stu-id="71dce-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="71dce-118">Du kan ikke bruge fletfelter, hvis navnet på feltet indeholder 40 tegn eller mere.</span><span class="sxs-lookup"><span data-stu-id="71dce-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="71dce-119">Du kan f.eks. ikke bruge feltet Toldregistreringsdato i virksomhedsoplysninger, da det indeholder 40 tegn.</span><span class="sxs-lookup"><span data-stu-id="71dce-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="71dce-120">Når du har klargjort din Word-skabelon, kan du vælge **Anvend** for at oprette dokumenterne på siden **Word-skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="71dce-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="71dce-121">Du kan enten oprette ét dokument, der indeholder sektioner for hvert objekt, eller opdele handlingen for at oprette et nyt dokument for hvert objekt.</span><span class="sxs-lookup"><span data-stu-id="71dce-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="71dce-122">Sådan oprettes en Word-skabelon</span><span class="sxs-lookup"><span data-stu-id="71dce-122">To create a Word template</span></span>
1. <span data-ttu-id="71dce-123">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Word-skabeloner**, og vælg derefter det tilknyttede link.</span><span class="sxs-lookup"><span data-stu-id="71dce-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="71dce-124">Følg trinnene i guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="71dce-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="71dce-125">Se også</span><span class="sxs-lookup"><span data-stu-id="71dce-125">See Also</span></span>
[<span data-ttu-id="71dce-126">Administrere rapport- og dokumentlayout</span><span class="sxs-lookup"><span data-stu-id="71dce-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
