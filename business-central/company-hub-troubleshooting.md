---
title: Fejlfinding i virksomhedens hub
description: Få at vide, hvordan du kan løse eventuelle problemer med virksomhedshubben i Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3f348de3e8116efd789f85f1b011ecc7013bf2b1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3927629"
---
# <a name="troubleshooting-your-company-hub"></a><span data-ttu-id="91091-103">Fejlfinding i virksomhedens hub</span><span class="sxs-lookup"><span data-stu-id="91091-103">Troubleshooting Your Company Hub</span></span>

<span data-ttu-id="91091-104">Det er nemt at føje virksomheder til virksomhedshubben, og denne artikel vedrører problemer, der eventuelt opstår undervejs.</span><span class="sxs-lookup"><span data-stu-id="91091-104">Adding companies to the company hub dashboard is easy enough, but this article addresses issues that you may have on the way.</span></span>  

## <a name="check-errors"></a><span data-ttu-id="91091-105">Kontrollér fejl</span><span class="sxs-lookup"><span data-stu-id="91091-105">Check errors</span></span>

<span data-ttu-id="91091-106">Brug handlingen **Kontroller fejl** til at få vist en liste over de seneste fejl.</span><span class="sxs-lookup"><span data-stu-id="91091-106">Use the **Check Errors** action to view a list of recent errors.</span></span> <span data-ttu-id="91091-107">Du kan få vist flere oplysninger om hver fejl, og du kan rydde op i loggen ved at slette gamle poster.</span><span class="sxs-lookup"><span data-stu-id="91091-107">You can see additional details for each error, and you can clean up the log by deleting older entries.</span></span>  

## <a name="connection-failed"></a><span data-ttu-id="91091-108">Der kunne ikke oprettes forbindelse</span><span class="sxs-lookup"><span data-stu-id="91091-108">Connection failed</span></span>

<span data-ttu-id="91091-109">Der kan være nogle årsager til, at du ikke kan oprette forbindelse til en virksomhed, herunder følgende:</span><span class="sxs-lookup"><span data-stu-id="91091-109">There can be a couple of reasons why you cannot connect to a company, including the following:</span></span>

- <span data-ttu-id="91091-110">URL-adressen i feltet **Miljølink** er ikke gyldig</span><span class="sxs-lookup"><span data-stu-id="91091-110">The URL in the **Environment Link** field is not valid</span></span>  

  <span data-ttu-id="91091-111">Gå til siden **Miljølinks**, åbn det miljø, du ikke kan oprette forbindelse til, og vælg derefter handlingen **Test forbindelse**.</span><span class="sxs-lookup"><span data-stu-id="91091-111">Go to the **Environment Links** page, open the environment that you cannot connect to, and then choose the **Test the connection** action.</span></span>  
- <span data-ttu-id="91091-112">Kundens virksomhed er offline, f.eks. hvis den er ved at blive opgraderet</span><span class="sxs-lookup"><span data-stu-id="91091-112">The client's company is currently offline, for example if it being upgraded</span></span>

  <span data-ttu-id="91091-113">På dashboardet skal du vælge menupunktet **Værktøjer** og derefter vælge **Kontroller fejl**.</span><span class="sxs-lookup"><span data-stu-id="91091-113">In your dashboard, choose the **Tools** menu item, and then choose **Check Errors**.</span></span> <span data-ttu-id="91091-114">Dermed åbnes en liste med tekniske oplysninger, så du skal måske kontakte systemadministratoren, hvis du får vist fejl.</span><span class="sxs-lookup"><span data-stu-id="91091-114">This opens a list with technical details, so you might want to contact your administrator if you're seeing errors.</span></span> <span data-ttu-id="91091-115">Meddelelsen "*Serveren har afvist kundens legitimationsoplysninger*" angiver f.eks., at du ikke har adgang.</span><span class="sxs-lookup"><span data-stu-id="91091-115">For example, the error message "*The server has rejected the client credentials*" suggests that you do not have access.</span></span>  
- <span data-ttu-id="91091-116">Du har ikke adgang til alle regnskaber i miljøet, som du forsøger at oprette forbindelse til.</span><span class="sxs-lookup"><span data-stu-id="91091-116">You do not have access to all companies in the environment that you are trying to connect to</span></span>

  <span data-ttu-id="91091-117">I [!INCLUDE [prodshort](includes/prodshort.md)] kan en organisation have flere forretningsenheder kaldet virksomheder, og du har muligvis ikke adgang til alle virksomheder.</span><span class="sxs-lookup"><span data-stu-id="91091-117">In [!INCLUDE [prodshort](includes/prodshort.md)], an organization can have multiple business units called companies, and you might not have access to all companies.</span></span> <span data-ttu-id="91091-118">Arbejd sammen med administratoren for at sikre, at du har adgang til de virksomheder, som du ønsker at arbejde i.</span><span class="sxs-lookup"><span data-stu-id="91091-118">Work with your administrator or client to make sure that you have access to the companies that you have to work in.</span></span>  

## <a name="data-does-not-refresh"></a><span data-ttu-id="91091-119">Data opdateres ikke</span><span class="sxs-lookup"><span data-stu-id="91091-119">Data does not refresh</span></span>

<span data-ttu-id="91091-120">Når du tilføjer en virksomhed eller anmoder om en opdatering af dataene, henter [!INCLUDE [prodshort](includes/prodshort.md)] dataene.</span><span class="sxs-lookup"><span data-stu-id="91091-120">When you add a company or request a refresh of the data, [!INCLUDE [prodshort](includes/prodshort.md)] fetches the data.</span></span> <span data-ttu-id="91091-121">Men du skal selv opdatere siden, f.eks. ved at vælge handlingen **Genindlæs alle virksomheder**, opdatere browsersiden, navigere væk fra dashboardet og derefter tilbage igen eller noget lignende.</span><span class="sxs-lookup"><span data-stu-id="91091-121">But you must refresh the page yourself, such as choosing the **Reload all companies** action, refresh the browser page, navigate away from the dashboard and then back again, or similar.</span></span>  

<span data-ttu-id="91091-122">Hvis du har tilføjet et regnskab, men det ikke vises på listen, kan du også bruge handlingen **Genindlæs alle virksomheder** for at opdatere listen.</span><span class="sxs-lookup"><span data-stu-id="91091-122">If you've added a company but it is not displaying in the list, you can also use the **Reload all companies** action to update the list.</span></span>

## <a name="see-also"></a><span data-ttu-id="91091-123">Se også</span><span class="sxs-lookup"><span data-stu-id="91091-123">See also</span></span>

[<span data-ttu-id="91091-124">Administrere arbejde på tværs af flere regnskaber i virksomhedshub</span><span class="sxs-lookup"><span data-stu-id="91091-124">Manage Work across Multiple Companies in the Company Hub</span></span>](company-hub.md)  
[<span data-ttu-id="91091-125">Tilføj firmaer til virksomhedens hub</span><span class="sxs-lookup"><span data-stu-id="91091-125">Add companies to your company hub</span></span>](company-hub-add-company.md)  
[<span data-ttu-id="91091-126">Revisoroplevelser i Business Central</span><span class="sxs-lookup"><span data-stu-id="91091-126">Accountant Experiences in Business Central</span></span>](finance-accounting.md)  