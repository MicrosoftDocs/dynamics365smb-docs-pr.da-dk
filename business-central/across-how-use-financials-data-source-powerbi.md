---
title: Brug Business Central i Power BI rapporter | Microsoft Docs
description: Gøre dine data tilgængelige som en datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 07/08/2019
ms.author: edupont
ms.openlocfilehash: c86f1c3c40f80ec993d0a3a89154047ddf9e8126
ms.sourcegitcommit: 519623f9a5134c9ffa97eeaed0841ae59835f453
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/16/2019
ms.locfileid: "1755237"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a><span data-ttu-id="d4375-103">Brug af [!INCLUDE [prodlong](includes/prodlong.md)] som Power BI-datakilde til oprettelse af rapporter</span><span class="sxs-lookup"><span data-stu-id="d4375-103">Using [!INCLUDE [prodlong](includes/prodlong.md)] as Power BI Data Source for Building Reports</span></span>

<span data-ttu-id="d4375-104">Du kan gøre dine [!INCLUDE[prodlong](includes/prodlong.md)]-data tilgængelige som datakilde i Power BI og opbygge nyttige rapporter over status for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="d4375-104">You can make your [!INCLUDE[prodlong](includes/prodlong.md)] data available as a data source in Power BI and build powerful reports of the state of your business.</span></span>  

<span data-ttu-id="d4375-105">Du skal have en gyldig konto til [!INCLUDE[prodshort](includes/prodshort.md)] og til Power BI.</span><span class="sxs-lookup"><span data-stu-id="d4375-105">You must have a valid account with [!INCLUDE[prodshort](includes/prodshort.md)] and with Power BI.</span></span> <span data-ttu-id="d4375-106">Desuden skal du hente [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span><span class="sxs-lookup"><span data-stu-id="d4375-106">Also, you must download [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/).</span></span> <span data-ttu-id="d4375-107">Du kan finde flere oplysninger under [Hurtig start: Opret forbindelse til data i Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span><span class="sxs-lookup"><span data-stu-id="d4375-107">For more information, see [Quickstart: Connect to data in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).</span></span>  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a><span data-ttu-id="d4375-108">Sådan tilføjes [!INCLUDE[prodshort](includes/prodshort.md)] som en datakilde i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d4375-108">To add [!INCLUDE[prodshort](includes/prodshort.md)] as a data source in Power BI Desktop</span></span>

1. <span data-ttu-id="d4375-109">I Power BI Desktop skal du i den venstre navigationsrude vælge **Hent data**.</span><span class="sxs-lookup"><span data-stu-id="d4375-109">In Power BI Desktop, in the left navigation pane, choose **Get Data**.</span></span>
2. <span data-ttu-id="d4375-110">På siden **Hent data** skal du vælge **Onlinetjenester**, vælge **Microsoft Dynamics 365 Business Central** og derefter vælge knappen **Opret forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="d4375-110">On the **Get Data** page, choose **Online Services**, choose **Microsoft Dynamics 365 Business Central**, and then choose the **Connect** button.</span></span>
3. <span data-ttu-id="d4375-111">Power BI viser en guide, der hjælper dig gennem forbindelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="d4375-111">Power BI displays a wizard that will guide you through the connection process.</span></span> <span data-ttu-id="d4375-112">Du bliver bedt om at logge på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d4375-112">You will be prompted to sign into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="d4375-113">Vælg **Log på**, og vælg den konto, du vil logge på som.</span><span class="sxs-lookup"><span data-stu-id="d4375-113">Select **Sign in** and choose the account you would like to sign in as.</span></span> <span data-ttu-id="d4375-114">Det skal være den samme konto, du bruger til at logge på [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d4375-114">This should be the same account you sign into [!INCLUDE [prodshort](includes/prodshort.md)] with.</span></span>
4. <span data-ttu-id="d4375-115">Vælg knappen **Opret forbindelse** for at forsætte.</span><span class="sxs-lookup"><span data-stu-id="d4375-115">Choose the **Connect** button to continue.</span></span> <span data-ttu-id="d4375-116">Guiden Power BI viser en liste over Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-regnskaber og -datakilder.</span><span class="sxs-lookup"><span data-stu-id="d4375-116">The Power BI wizard shows a list of Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)] companies and data sources.</span></span> <span data-ttu-id="d4375-117">Disse datakilder repræsenterer all de webtjenester, som du har publiceret fra hver virksomhed i [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="d4375-117">These data source represent all the web services that you have published from each company in [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>

  ![powerbi_webservices.png](media/across-how-use-financials-data-source-powerbi/powerbi_webservices.png)

5. <span data-ttu-id="d4375-119">Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE [prodshort](includes/prodshort.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.</span><span class="sxs-lookup"><span data-stu-id="d4375-119">Alternatively, create a new web service URL in [!INCLUDE [prodshort](includes/prodshort.md)] by using the **Create Data Set** action on the **Web Services** page, using the **Set Up Reporting** Assisted Setup guide, or by choosing the **Edit in Excel** action in any lists.</span></span>
6. <span data-ttu-id="d4375-120">Angiv de data, du vil føje til dine datamodel, og vælg derefter knappen **Indlæsning**.</span><span class="sxs-lookup"><span data-stu-id="d4375-120">Specify the data you want to add to your data model, and then choose the **Load** button.</span></span>
7. <span data-ttu-id="d4375-121">Gentag fremgangsmåden for at tilføje flere [!INCLUDE [prodshort](includes/prodshort.md)] eller andre data til din Power BI-datamodel.</span><span class="sxs-lookup"><span data-stu-id="d4375-121">Repeat the previous steps to add additional [!INCLUDE [prodshort](includes/prodshort.md)], or other data, to your Power BI data model.</span></span>

> [!NOTE]  
> <span data-ttu-id="d4375-122">Når du har oprettet forbindelse til [!INCLUDE [prodshort](includes/prodshort.md)], bliver du ikke bedt om at logge på igen.</span><span class="sxs-lookup"><span data-stu-id="d4375-122">Once you have successfully connected to [!INCLUDE [prodshort](includes/prodshort.md)], you will not be prompted again to sign in.</span></span>

<span data-ttu-id="d4375-123">Når dataene er indlæst, vises de i den rigtige navigation på siden.</span><span class="sxs-lookup"><span data-stu-id="d4375-123">Once the data is loaded it will appear in the right navigation on the page.</span></span> <span data-ttu-id="d4375-124">Nu har du oprettet forbindelse til dine [!INCLUDE [prodshort](includes/prodshort.md)]-data og er klar til at begynde at oprette din Power BI-rapport.</span><span class="sxs-lookup"><span data-stu-id="d4375-124">At this point, you have successfully connected to your [!INCLUDE [prodshort](includes/prodshort.md)] data and are ready to begin building your Power BI report.</span></span>  

<span data-ttu-id="d4375-125">Før du opretter rapporten, anbefales det, at du importerer [!INCLUDE [prodshort](includes/prodshort.md)]-temafilen.</span><span class="sxs-lookup"><span data-stu-id="d4375-125">Before building your report, we recommend that you import the [!INCLUDE [prodshort](includes/prodshort.md)] theme file.</span></span>  <span data-ttu-id="d4375-126">Temafilen opretter en farvepalet, så du kan oprette rapporter med de samme farvenuancer som [!INCLUDE [prodshort](includes/prodshort.md)]-apps, uden at du skal definere brugerdefinerede farver til hvert visuelle element.</span><span class="sxs-lookup"><span data-stu-id="d4375-126">The theme file will create a color palette so that you can build reports with the same color styling as the [!INCLUDE [prodshort](includes/prodshort.md)] apps without requiring you to define custom colors for each visual.</span></span>

<span data-ttu-id="d4375-127">Der er flere oplysninger i [Power BI-dokumentationen](/power-bi/consumer/power-bi-consumer-landing/).</span><span class="sxs-lookup"><span data-stu-id="d4375-127">For more information, see the [Power BI documentation](/power-bi/consumer/power-bi-consumer-landing/).</span></span>

## <a name="see-also"></a><span data-ttu-id="d4375-128">Se også</span><span class="sxs-lookup"><span data-stu-id="d4375-128">See Also</span></span>

[<span data-ttu-id="d4375-129">Aktivere virksomhedens data til Power BI</span><span class="sxs-lookup"><span data-stu-id="d4375-129">Enabling Your Business Data for Power BI</span></span>](admin-powerbi.md)  
[<span data-ttu-id="d4375-130">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="d4375-130">Business Intelligence</span></span>](bi.md)  
[<span data-ttu-id="d4375-131">Introduktion</span><span class="sxs-lookup"><span data-stu-id="d4375-131">Getting Started</span></span>](product-get-started.md)  
[<span data-ttu-id="d4375-132">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="d4375-132">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="d4375-133">[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span><span class="sxs-lookup"><span data-stu-id="d4375-133">[Setting Up [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)</span></span>  
[<span data-ttu-id="d4375-134">Finans</span><span class="sxs-lookup"><span data-stu-id="d4375-134">Finance</span></span>](finance.md)  
[<span data-ttu-id="d4375-135">Hurtig start: Opret forbindelse til data i Power BI Desktop</span><span class="sxs-lookup"><span data-stu-id="d4375-135">Quickstart: Connect to data in Power BI Desktop</span></span>](/power-bi/desktop-quickstart-connect-to-data)  
