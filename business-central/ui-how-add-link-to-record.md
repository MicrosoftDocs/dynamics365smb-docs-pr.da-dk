---
title: Sådan sammenkædes poster med eksterne oplysninger eller programmer | Microsoft Docs
description: Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/12/2019
ms.author: jswymer
ms.openlocfilehash: 602d520043c5192109ccc4e2605ae0e231dafc1e
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/29/2019
ms.locfileid: "1250338"
---
# <a name="add-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="a2b9a-103">Føje links til websteder, dokumenter eller programmer på poster</span><span class="sxs-lookup"><span data-stu-id="a2b9a-103">Add Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="a2b9a-104">På en bestemt post, f.eks. en debitor, et dokument eller en salgsordre, kan du tilføje et link til et eksternt dokument, websted eller program.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="a2b9a-105">Det kan også være, at du ønsker et link, der åbner en ny tom mail til en bestemt modtager, når du vælger det.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="a2b9a-106">På kortsiden på nogle poster, f.eks. debitor- og kreditorkort, er der et felt **Hjemmeside**, hvor du kan angive en URL-adresse (internetadresse).</span><span class="sxs-lookup"><span data-stu-id="a2b9a-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="a2b9a-107">Hvis du vil medtage andre links, kan du bruge den metode, der er beskrevet i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-107">To include other links, you can use the method described in this article.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a2b9a-108">I øjeblikket er denne funktion kun tilgængelig på [!INCLUDE [prodshort](includes/prodshort.md)] i lokale installationer med den ældre Dynamics NAV Windows-klient.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-108">Currently, this capability is available only in [!INCLUDE [prodshort](includes/prodshort.md)] on-premises deployments with the legacy Dynamics NAV Windows client.</span></span>  

<span data-ttu-id="a2b9a-109">Et andet eksempel kan være, når du modtager en trykt faktura fra kreditorer.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-109">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="a2b9a-110">Du kan scanne den og gemme den som en .pdf-fil på et SharePoint-websted.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-110">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="a2b9a-111">Derefter kan du oprette et link fra en købsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende faktura i SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-111">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="a2b9a-112">Eller du kan oprette et link fra et varekort til den tilsvarende side i kreditorens onlinekatalog.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-112">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="a2b9a-113">Sådan tilføjes et link til en post</span><span class="sxs-lookup"><span data-stu-id="a2b9a-113">To add a link on a record</span></span>   

1.  <span data-ttu-id="a2b9a-114">Åbn den post, du vil oprette linket til, f.eks. et debitorkort eller en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-114">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="a2b9a-115">Hvis linket skal knyttes til en bestemt linje, f.eks. en kladdelinje, skal du placere markøren på linjen.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-115">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="a2b9a-116">Vælg handlingen **Links** for at åbne siderne **Links**, der viser de aktuelle kæder, der føjes til posten.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-116">Choose the **Links** action to open the **Links** pages that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="a2b9a-117">Hvis du vil tilføje et nyt link, skal du vælge **+ny**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-117">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="a2b9a-118">I feltet **Hyperlinkadresse** skal du angive</span><span class="sxs-lookup"><span data-stu-id="a2b9a-118">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="a2b9a-119">Hvis du vil sammenkæde med en fil på din computer eller dit netværk, skal du angive den fulde sti og filnavn, f.eks. **C: Min dokumentfaktura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-119">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="a2b9a-120">Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="a2b9a-121">Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-121">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="a2b9a-122">Hvis du vil sammenkæde med et program, skal du angive en bestemt streng for at åbne programmet.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-122">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="a2b9a-123">Hvis du f.eks. vil åbne OneNote med en bestemt side, skal du angive **OneNote:///C:Min dokumenttest.one**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-123">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="a2b9a-124">Eller hvis du vil åbne Outlook med en ny tom mail til et bestemt alias, skal du angive **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-124">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="a2b9a-125">Angiv oplysninger om linket i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-125">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="a2b9a-126">Vælg knappen **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-126">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="a2b9a-127">Sådan slettes et link fra en post</span><span class="sxs-lookup"><span data-stu-id="a2b9a-127">To delete a link from a record</span></span>  

<span data-ttu-id="a2b9a-128">Hvis du vil slette et link, kan du på siden **Links** vælge **...** og derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-128">To delete a link, on the **Links** page, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="a2b9a-129">Hvis du sletter en enkelt post, f.eks. en salgsordrelinje, en salgsordre eller en debitor, så slettes alle links med tilknytning til denne post.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-129">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="a2b9a-130">Men hvis du sletter poster med en kørsel, f.eks. kørslen **Slet fakturerede salgsordrer**, så lagres linksene stadig i databasen.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-130">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="a2b9a-131">Hvis du vil slette linkene fra databasen, skal du køre codeunit **Slet underordnede postlinks**.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-131">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="a2b9a-132">For at gøre dette skal du vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Slet uafhængige posttilknytninger**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a2b9a-132">To do this, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="a2b9a-133">Se også</span><span class="sxs-lookup"><span data-stu-id="a2b9a-133">See Also</span></span>  
<span data-ttu-id="a2b9a-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2b9a-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
