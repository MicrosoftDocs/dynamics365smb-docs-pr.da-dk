---
title: Vise objekter som webtjenester
description: Publicer objekter som webtjenester for at gøre dem umiddelbart tilgængelige for din Business Central-løsning.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 59b6febc147687e88f11423b4ad317ab6ee5a408
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5775943"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="add52-103">Udgive en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="add52-103">Publish a Web Service</span></span>

<span data-ttu-id="add52-104">Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for forskellige eksterne systemer og brugere.</span><span class="sxs-lookup"><span data-stu-id="add52-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="add52-105">Som standard viser [!INCLUDE[prod_short](includes/prod_short.md)] en række objekter som webtjenester, hvilket giver en bedre integration med andre Microsoft-tjenester.</span><span class="sxs-lookup"><span data-stu-id="add52-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="add52-106">Du kan tilføje andre webtjenester, efterhånden som virksomheden kræver det.</span><span class="sxs-lookup"><span data-stu-id="add52-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="add52-107">Opret en webtjeneste i [!INCLUDE[prod_short](includes/prod_short.md)], og udgiv derefter webtjenesten, så den er tilgængelig for godkendte brugere.</span><span class="sxs-lookup"><span data-stu-id="add52-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="add52-108">Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.</span><span class="sxs-lookup"><span data-stu-id="add52-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="add52-109">Oprettelse og publicering af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="add52-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="add52-110">Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="add52-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="add52-111">Sådan oprettes og publiceres en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="add52-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="add52-112">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjenester**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="add52-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="add52-113">På siden **Webtjeneste** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="add52-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="add52-114">**Codeunit** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="add52-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="add52-115">**Side** og **Forespørgsel** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="add52-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="add52-116">Fra og med version 16.3 **Codeunit**, som også er en gyldig type til OData v4-webtjenester, men derefter vises der ikke nogen URL-adresse i brugergrænsefladen.</span><span class="sxs-lookup"><span data-stu-id="add52-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="add52-117">Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.</span><span class="sxs-lookup"><span data-stu-id="add52-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="add52-118">Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.</span><span class="sxs-lookup"><span data-stu-id="add52-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="add52-119">Marker afkrydsningsfeltet i kolonnen **Udgivet**.</span><span class="sxs-lookup"><span data-stu-id="add52-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="add52-120">Når du udgiver webtjenesten, viser felterne **OData URL** og **SOAP-URL** nye URL-adresser.</span><span class="sxs-lookup"><span data-stu-id="add52-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="add52-121">For de kodeenheder, der eksponeres som Odata v4-ubundne handlinger, vises URL-felterne imidlertid ikke.</span><span class="sxs-lookup"><span data-stu-id="add52-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="add52-122">Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**.</span><span class="sxs-lookup"><span data-stu-id="add52-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="add52-123">Du kan vælge at kopiere værdien af feltet og gemme det til senere brug.</span><span class="sxs-lookup"><span data-stu-id="add52-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="add52-124">Hvis du vil teste kodeenheder, som er eksponerede som OData v4-ubundne handlinger, skal du følge instruktionerne i afsnittet [Kontroller webtjenestetilgængelighed](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) i udviklerindholdet.</span><span class="sxs-lookup"><span data-stu-id="add52-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="add52-125">Hvis du ikke kan få adgang til de objekter, du fremviser som webtjenester, i [!INCLUDE[prod_short](includes/prod_short.md)] online, skal du markere de metoder, der vises i koden, som `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="add52-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="add52-126">Du kan finde flere oplysninger i [Områdeattribut](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="add52-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="add52-127">Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="add52-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="add52-128">Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket på siden **URL-adresse til OData** og **URL-adresse til SOAP** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="add52-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="add52-129">Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.</span><span class="sxs-lookup"><span data-stu-id="add52-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="add52-130">Sådan kontrolleres tilgængeligheden af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="add52-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="add52-131">Indtast den relevante URL-adresse i din browser</span><span class="sxs-lookup"><span data-stu-id="add52-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="add52-132">Følgende tabel viser de typer URL'er, som du kan angive for forskellige typer webtjenester.</span><span class="sxs-lookup"><span data-stu-id="add52-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="add52-133">Type</span><span class="sxs-lookup"><span data-stu-id="add52-133">Type</span></span>|<span data-ttu-id="add52-134">Syntaks</span><span class="sxs-lookup"><span data-stu-id="add52-134">Syntax</span></span>|<span data-ttu-id="add52-135">Eksempel</span><span class="sxs-lookup"><span data-stu-id="add52-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="add52-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="add52-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="add52-137">V4-adresse til OData</span><span class="sxs-lookup"><span data-stu-id="add52-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="add52-138">Der skelnes mellem små og store bogstaver i firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="add52-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="add52-139">Gennemse de oplysninger, der vises i browseren.</span><span class="sxs-lookup"><span data-stu-id="add52-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="add52-140">Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="add52-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="add52-141">Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[prod_short](includes/prod_short.md)], skal du angive firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="add52-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="add52-142">Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene.</span><span class="sxs-lookup"><span data-stu-id="add52-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="add52-143">F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.</span><span class="sxs-lookup"><span data-stu-id="add52-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="add52-144">Se også</span><span class="sxs-lookup"><span data-stu-id="add52-144">See Also</span></span>

[<span data-ttu-id="add52-145">Opsætning</span><span class="sxs-lookup"><span data-stu-id="add52-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="add52-146">Business Centrale-webtjenester til udviklere</span><span class="sxs-lookup"><span data-stu-id="add52-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="add52-147">Anmodningsgrænser for OData</span><span class="sxs-lookup"><span data-stu-id="add52-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]