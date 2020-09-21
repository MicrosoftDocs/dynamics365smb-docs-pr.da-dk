---
title: Vise objekter som webtjenester | Microsoft Docs
description: Publicer objekter som webtjenester for at gøre dem umiddelbart tilgængelige for din Business Central-løsning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 05/19/2020
ms.author: edupont
ms.openlocfilehash: 230f3a7fc11e19813d77da2ff15388433642c744
ms.sourcegitcommit: aeaa0dc64e54432a70c4b0e1faf325cd17d01389
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/17/2020
ms.locfileid: "3697643"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="59599-103">Udgive en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="59599-103">Publish a Web Service</span></span>

<span data-ttu-id="59599-104">Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for en række eksterne systemer og brugere.</span><span class="sxs-lookup"><span data-stu-id="59599-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="59599-105">indeholder en lang række objekter, der vises som webtjenester som standard, på grund af integration med andre Microsoft-tjenester, men du kan også tilføje andre webtjenester.</span><span class="sxs-lookup"><span data-stu-id="59599-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="59599-106">Du kan oprette en webtjeneste i [!INCLUDE[d365fin](includes/d365fin_md.md)]-klienten.</span><span class="sxs-lookup"><span data-stu-id="59599-106">You set up a web service in the [!INCLUDE[d365fin](includes/d365fin_md.md)] client.</span></span> <span data-ttu-id="59599-107">Du skal derefter publicere webtjenesten, så den er tilgængelig for serviceanmodninger via netværket.</span><span class="sxs-lookup"><span data-stu-id="59599-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="59599-108">Brugere kan se webtjenester ved at pege på en browser på serverplaceringen og anmode om en oversigt over tilgængelige tjenester.</span><span class="sxs-lookup"><span data-stu-id="59599-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="59599-109">Når du publicerer en webtjeneste, bliver den straks tilgængelig over netværket for godkendte brugere.</span><span class="sxs-lookup"><span data-stu-id="59599-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="59599-110">Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.</span><span class="sxs-lookup"><span data-stu-id="59599-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="59599-111">Oprettelse og publicering af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="59599-111">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="59599-112">Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="59599-112">The following steps explain how to create and publish a web service.</span></span>  

<!--
    You can also create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] instead. Choose one of the following methods:

      - Use the **Create Data Set** action on the **Web Services** page
      - Use the **Set Up Reporting** Assisted Setup guide
      - Choose the **Edit in Excel** action in any lists
    -->

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="59599-113">Sådan oprettes og publiceres en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="59599-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="59599-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="59599-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="59599-115">På siden **Webtjeneste** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="59599-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="59599-116">**Codeunit** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="59599-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="59599-117">**Side** og **Forespørgsel** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="59599-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="59599-118">Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.</span><span class="sxs-lookup"><span data-stu-id="59599-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="59599-119">Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.</span><span class="sxs-lookup"><span data-stu-id="59599-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="59599-120">Marker afkrydsningsfeltet i kolonnen **Udgivet**.</span><span class="sxs-lookup"><span data-stu-id="59599-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="59599-121">Når du publicerer en webtjeneste, kan du i felterne **URL-adresse til OData** og **URL-adresse til SOAP** se de URL'er, der er genereret for webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="59599-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="59599-122">Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**.</span><span class="sxs-lookup"><span data-stu-id="59599-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="59599-123">Du kan vælge at kopiere værdien af feltet og gemme det til senere brug.</span><span class="sxs-lookup"><span data-stu-id="59599-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!NOTE]
> <span data-ttu-id="59599-124">Hvis du ikke kan få adgang til de objekter, du fremviser som webtjenester, i [!INCLUDE[prodshort](includes/prodshort.md)] online, skal du markere de metoder, der vises i koden, som `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="59599-124">If the objects that you expose as web services must not be accessible from [!INCLUDE[prodshort](includes/prodshort.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="59599-125">Du kan finde flere oplysninger i [Områdeattribut](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="59599-125">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="59599-126">Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="59599-126">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="59599-127">Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket på siden **URL-adresse til OData** og **URL-adresse til SOAP** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="59599-127">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="59599-128">Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.</span><span class="sxs-lookup"><span data-stu-id="59599-128">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="59599-129">Sådan kontrolleres tilgængeligheden af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="59599-129">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="59599-130">Indtast den relevante URL-adresse i din browser</span><span class="sxs-lookup"><span data-stu-id="59599-130">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="59599-131">Følgende tabel viser de typer URL'er, som du kan angive for forskellige typer webtjenester.</span><span class="sxs-lookup"><span data-stu-id="59599-131">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="59599-132">Type</span><span class="sxs-lookup"><span data-stu-id="59599-132">Type</span></span>|<span data-ttu-id="59599-133">Syntaks</span><span class="sxs-lookup"><span data-stu-id="59599-133">Syntax</span></span>|<span data-ttu-id="59599-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="59599-134">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="59599-135">SOAP</span><span class="sxs-lookup"><span data-stu-id="59599-135">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="59599-136">V4-adresse til OData</span><span class="sxs-lookup"><span data-stu-id="59599-136">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="59599-137">Der skelnes mellem små og store bogstaver i firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="59599-137">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="59599-138">Gennemse de oplysninger, der vises i browseren.</span><span class="sxs-lookup"><span data-stu-id="59599-138">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="59599-139">Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="59599-139">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="59599-140">Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="59599-140">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="59599-141">Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene.</span><span class="sxs-lookup"><span data-stu-id="59599-141">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="59599-142">F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.</span><span class="sxs-lookup"><span data-stu-id="59599-142">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="59599-143">Se også</span><span class="sxs-lookup"><span data-stu-id="59599-143">See Also</span></span>

[<span data-ttu-id="59599-144">Opsætning</span><span class="sxs-lookup"><span data-stu-id="59599-144">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="59599-145">Business Centrale-webtjenester til udviklere</span><span class="sxs-lookup"><span data-stu-id="59599-145">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="59599-146">Anmodningsgrænser for OData</span><span class="sxs-lookup"><span data-stu-id="59599-146">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  
