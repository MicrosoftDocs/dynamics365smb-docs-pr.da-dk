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
ms.openlocfilehash: 118d8db1266bb7150965ec4d1ce44ece77638764
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788516"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="7bb13-103">Bruge Word-skabeloner til massekommunikation</span><span class="sxs-lookup"><span data-stu-id="7bb13-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="7bb13-104">Microsoft Word-skabeloner kan gøre det nemmere at massekommunikere med objekter som f.eks. debitorer og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="7bb13-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="7bb13-105">Du kan f.eks. oprette brochurer, som giver debitorer besked om en salgskampagne, breve til kreditorer om en ny indkøbspolitik eller invitationer, der skal tiltrække kontakter til et kommende arrangement.</span><span class="sxs-lookup"><span data-stu-id="7bb13-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

<span data-ttu-id="7bb13-106">Du kan bruge objekter i [!INCLUDE[prod_short](includes/prod_short.md)] som datakilde for skabelonen og til at tilføje fletfelter for at tilpasse dokumenter til de enkelte objekter.</span><span class="sxs-lookup"><span data-stu-id="7bb13-106">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="7bb13-107">Fletfelterne hentes fra objektet i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="7bb13-107">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="7bb13-108">Når du anvender en Word-skabelon til et objekt, indsættes data fra fletfelterne i dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7bb13-108">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="7bb13-109">På siden **Word-skabeloner** kan du bruge en vejledning om assisteret opsætning for at hente en zip-fil, der indeholder filen DataSource.txt og en Word-skabelonfil til et objekt.</span><span class="sxs-lookup"><span data-stu-id="7bb13-109">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="7bb13-110">Når du har oprettet skabelonen og tilføjet fletfelter, bruger du den samme vejledning til at overføre skabelonen.</span><span class="sxs-lookup"><span data-stu-id="7bb13-110">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="7bb13-111">Du kan kun bruge den Word-skabelon og de datakildefiler, som du henter fra [!INCLUDE[prod_short](includes/prod_short.md)], og du skal gemme filerne på den samme placering.</span><span class="sxs-lookup"><span data-stu-id="7bb13-111">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="7bb13-112">Når du vælger et objekt, som du vil oprette en skabelon for, viser listen alle objekter i [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="7bb13-112">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="7bb13-113">Du kan dog ikke oprette skabeloner for alle objekter.</span><span class="sxs-lookup"><span data-stu-id="7bb13-113">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="7bb13-114">Hvis navnet på et objekt indeholder specialtegn som f.eks **/**, **.**, **_** eller **-**, kan du ikke oprette en skabelon for det.</span><span class="sxs-lookup"><span data-stu-id="7bb13-114">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="7bb13-115">Navnet på objektet vises i kolonnen **Objekttitel**.</span><span class="sxs-lookup"><span data-stu-id="7bb13-115">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="7bb13-116">Når du opretter skabelonen i Word, kan du tilføje fletfelter på fanen **Forsendelser** ved at vælge **Indsæt fletfelt**.</span><span class="sxs-lookup"><span data-stu-id="7bb13-116">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="7bb13-117">Du kan ikke bruge fletfelter, hvis navnet på feltet indeholder 40 tegn eller mere.</span><span class="sxs-lookup"><span data-stu-id="7bb13-117">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="7bb13-118">Du kan f.eks. ikke bruge feltet Toldregistreringsdato i virksomhedsoplysninger, da det indeholder 40 tegn.</span><span class="sxs-lookup"><span data-stu-id="7bb13-118">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="7bb13-119">Når du har klargjort din Word-skabelon, kan du vælge **Anvend** for at oprette dokumenterne på siden **Word-skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="7bb13-119">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="7bb13-120">Du kan enten oprette ét dokument, der indeholder sektioner for hvert objekt, eller opdele handlingen for at oprette et nyt dokument for hvert objekt.</span><span class="sxs-lookup"><span data-stu-id="7bb13-120">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="7bb13-121">Sådan oprettes en Word-skabelon</span><span class="sxs-lookup"><span data-stu-id="7bb13-121">To create a Word template</span></span>
1. <span data-ttu-id="7bb13-122">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Word-skabeloner**, og vælg derefter det tilknyttede link.</span><span class="sxs-lookup"><span data-stu-id="7bb13-122">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="7bb13-123">Følg trinnene i guiden til assisteret opsætning.</span><span class="sxs-lookup"><span data-stu-id="7bb13-123">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="7bb13-124">Se også</span><span class="sxs-lookup"><span data-stu-id="7bb13-124">See Also</span></span>
[<span data-ttu-id="7bb13-125">Administrere rapport- og dokumentlayout</span><span class="sxs-lookup"><span data-stu-id="7bb13-125">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
