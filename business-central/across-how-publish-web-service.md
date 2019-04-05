---
title: Vise objekter som webtjenester | Microsoft Docs
description: Publicerer objekter som webtjenester for at gøre dem tilgængelige på netværket med det samme.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: bb9623c00aa038b387179d46e6eb8a869552569e
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792160"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="ef1cf-103">Udgive en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="ef1cf-103">Publish a Web Service</span></span>

<span data-ttu-id="ef1cf-104">Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for en række eksterne systemer og brugere.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ef1cf-105">indeholder en lang række objekter, der vises som webtjenester som standard, på grund af integration med andre Microsoft-tjenester, men du kan også tilføje andre webtjenester.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="ef1cf-106">Du kan oprette en webtjeneste i Windows-klienten eller i webklienten.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="ef1cf-107">Du skal derefter publicere webtjenesten, så den er tilgængelig for serviceanmodninger via netværket.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="ef1cf-108">Brugere kan se webtjenester ved at pege på en browser på serverplaceringen og anmode om en oversigt over tilgængelige tjenester.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="ef1cf-109">Når du publicerer en webtjeneste, bliver den straks tilgængelig over netværket for godkendte brugere.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="ef1cf-110">Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="ef1cf-111">Oprettelse og publicering af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="ef1cf-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="ef1cf-112">Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="ef1cf-113">Sådan oprettes og publiceres en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="ef1cf-113">To create and publish a web service</span></span>  

1.  <span data-ttu-id="ef1cf-114">Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Webtjeneste**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="ef1cf-115">På siden **Webtjeneste** skal du vælge **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  <span data-ttu-id="ef1cf-116">**Codeunit** og **Side** er gyldige typer for SOAP-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="ef1cf-117">**Side** og **Forespørgsel** er gyldige typer for OData-webtjenester.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    <span data-ttu-id="ef1cf-118">Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    <span data-ttu-id="ef1cf-119">Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3.  <span data-ttu-id="ef1cf-120">Marker afkrydsningsfeltet i kolonnen **Udgivet**.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="ef1cf-121">Når du publicerer en webtjeneste, kan du i felterne **URL-adresse til OData** og **URL-adresse til SOAP** se de URL'er, der er genereret for webtjenesten.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="ef1cf-122">Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="ef1cf-123">Du kan vælge at kopiere værdien af feltet og gemme det til senere brug.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

<span data-ttu-id="ef1cf-124">Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-124">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="ef1cf-125">Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket på siden **URL-adresse til OData** og **URL-adresse til SOAP** på siden **Webtjenester**.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-125">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="ef1cf-126">Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-126">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="ef1cf-127">Sådan kontrolleres tilgængeligheden af en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="ef1cf-127">To verify the availability of a web service</span></span>  

1.  <span data-ttu-id="ef1cf-128">Indtast den relevante URL-adresse i din browser</span><span class="sxs-lookup"><span data-stu-id="ef1cf-128">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="ef1cf-129">Følgende tabel viser de typer URL'er, som du kan angive for forskellige typer webtjenester.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-129">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  
> [!div class="mx-tdBreakAll"]
> |<span data-ttu-id="ef1cf-130">Enhedstype</span><span class="sxs-lookup"><span data-stu-id="ef1cf-130">Type</span></span>|<span data-ttu-id="ef1cf-131">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ef1cf-131">Syntax</span></span>|<span data-ttu-id="ef1cf-132">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ef1cf-132">Example</span></span>|
> |----------------|------|-------|
> |<span data-ttu-id="ef1cf-133">SOAP</span><span class="sxs-lookup"><span data-stu-id="ef1cf-133">SOAP</span></span> |<span data-ttu-id="ef1cf-134">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span><span class="sxs-lookup"><span data-stu-id="ef1cf-134">https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/</span></span> |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |
> |<span data-ttu-id="ef1cf-135">OData</span><span class="sxs-lookup"><span data-stu-id="ef1cf-135">OData</span></span> |<span data-ttu-id="ef1cf-136">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span><span class="sxs-lookup"><span data-stu-id="ef1cf-136">https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')</span></span>|<span data-ttu-id="ef1cf-137">[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="ef1cf-137">[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com)</span></span> <br />    <span data-ttu-id="ef1cf-138">Der skelnes mellem små og store bogstaver i firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-138">The company name is case-sensitive.</span></span>|

2.  <span data-ttu-id="ef1cf-139">Gennemse de oplysninger, der vises i browseren.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="ef1cf-140">Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="ef1cf-141">Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive firmanavnet.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-141">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="ef1cf-142">Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-142">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="ef1cf-143">F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.</span><span class="sxs-lookup"><span data-stu-id="ef1cf-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a><span data-ttu-id="ef1cf-144">Se også</span><span class="sxs-lookup"><span data-stu-id="ef1cf-144">See Also</span></span>  
[<span data-ttu-id="ef1cf-145">Opsætning</span><span class="sxs-lookup"><span data-stu-id="ef1cf-145">Administration</span></span>](admin-setup-and-administration.md)  
