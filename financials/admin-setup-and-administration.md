---
title: Administrative opgaver i Finance and Operations, Business edition | Microsoft Docs
description: "Nogle opgaver i Finance and Operations, Business edition kræver central administration og installation. Se, hvilke opgaver det er, og få at vide, hvad du skal gøre."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: c64bc883031be28aa6634bdcf48f00c7ca77567d
ms.contentlocale: da-dk
ms.lasthandoff: 02/02/2018

---
# <a name="setup-and-administration-in-finance-and-operations-business-edition"></a><span data-ttu-id="79336-104">Opsætning og administration i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="79336-104">Setup and Administration in Finance and Operations, Business edition</span></span>
<span data-ttu-id="79336-105">Centrale administrationsopgaver udføres som regel af én rolle i firmaet.</span><span class="sxs-lookup"><span data-stu-id="79336-105">Central administration tasks are usually performed by one role in the company.</span></span> <span data-ttu-id="79336-106">Omfanget af disse opgaver kan afhænge af firmaets størrelse og administratorens jobansvar.</span><span class="sxs-lookup"><span data-stu-id="79336-106">The scope of these tasks can depend on the company's size and the administrator's job responsibilities.</span></span> <span data-ttu-id="79336-107">Disse opgaver kan omfatte styring af databasesynkronisering af job og e-mail-køer, oprette brugere, tilpasse brugergrænsefladen og administration af krypteringsnøgler.</span><span class="sxs-lookup"><span data-stu-id="79336-107">These tasks can include managing database synchronization of job and email queues, setting up users, customizing the user interface, and managing encryption keys.</span></span>  

<span data-ttu-id="79336-108">Det er vigtigt, at der indtastes korrekte opsætningsværdier fra starten, for at ny forretningssoftware kan fungere effektivt.</span><span class="sxs-lookup"><span data-stu-id="79336-108">Entering the correct setup values from the start is important to the success of any new business software.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="79336-109"> indeholder en række opsætningsvejledninger, som hjælper dig med opsætningen af basisoplysninger.</span><span class="sxs-lookup"><span data-stu-id="79336-109"> includes a number of setup guides that help you set up core data.</span></span> <span data-ttu-id="79336-110">Du kan finde flere oplysninger under [Konfigurere Finance and Operations, Business edition](setup.md).</span><span class="sxs-lookup"><span data-stu-id="79336-110">For more information, see [Setting Up Finance and Operations, Business edition](setup.md).</span></span>

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

<span data-ttu-id="79336-111">Superbruger eller administrator kan konfigurere Data Exchange Framework så brugere kan eksportere og importere data i bank og løn filer, f.eks. til forskellige likviditetsstyringsprocesser.</span><span class="sxs-lookup"><span data-stu-id="79336-111">A super user or an administrator can set up the Data Exchange Framework to enable users to export and import data in bank and payroll files, for example for various cash management processes.</span></span>  

<span data-ttu-id="79336-112">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="79336-112">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="79336-113">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="79336-113">**To**</span></span>|<span data-ttu-id="79336-114">**Se**</span><span class="sxs-lookup"><span data-stu-id="79336-114">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="79336-115">Tilføj brugere, administrer tilladelser og få adgang til data og tildel roller.</span><span class="sxs-lookup"><span data-stu-id="79336-115">Add users, manage permissions and access to data, assign roles.</span></span>|[<span data-ttu-id="79336-116">Brugere, profiler og rollecentre i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="79336-116">Users, Profiles, and Role Centers in Finance and Operations, Business edition</span></span>](admin-users-profiles-roles.md)|  
|<span data-ttu-id="79336-117">Spore alle de direkte modifikationer, som brugere foretager af data i databasen for at identificere oprindelsen til fejl og dataændringer.</span><span class="sxs-lookup"><span data-stu-id="79336-117">Track all direct modifications that users make to data in the database to identify the origin of errors and data changes.</span></span>|[<span data-ttu-id="79336-118">Logføring af ændringer i Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="79336-118">Logging Changes in Finance and Operations, Business edition</span></span>](across-log-changes.md)|  
|<span data-ttu-id="79336-119">Understøt dine opsætningsbeslutninger med anbefalinger for udvalgte felter, der er kendt for potentielt at gøre løsning ineffektiv, hvis de opsættes forkert</span><span class="sxs-lookup"><span data-stu-id="79336-119">Support your setup decisions with recommendations for selected fields that are known to potentially cause the solution to be inefficient if set up incorrectly</span></span>|[<span data-ttu-id="79336-120">Opret komplekse moduler ved hjælp af bedste praksis</span><span class="sxs-lookup"><span data-stu-id="79336-120">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)|  
|<span data-ttu-id="79336-121">Vis sider, kodeenheder og forespørgsler som webtjenester.</span><span class="sxs-lookup"><span data-stu-id="79336-121">Expose pages, codeunits, and queries as web services.</span></span>|[<span data-ttu-id="79336-122">Udgive en webtjeneste</span><span class="sxs-lookup"><span data-stu-id="79336-122">Publish a Web Service</span></span>](across-how-publish-web-service.md)|  
|<span data-ttu-id="79336-123">Konfigurere en SMTP-server til at aktivere mailkommunikation til og fra Finance and Operations, Business edition.</span><span class="sxs-lookup"><span data-stu-id="79336-123">Set up an SMTP server to enable e-mail communication in and out of Finance and Operations, Business edition</span></span>| [<span data-ttu-id="79336-124">Konfigurere mail manuelt eller ved hjælp af den assisterede opsætning</span><span class="sxs-lookup"><span data-stu-id="79336-124">Set Up Email Manually or Using the Assisted Setup</span></span>](madeira-how-setup-email.md)|  
|<span data-ttu-id="79336-125">Angive engangsanmodninger eller gentagne anmodninger om at køre rapporter eller kodeenheder.</span><span class="sxs-lookup"><span data-stu-id="79336-125">Enter single or recurring requests to run reports or codeunits.</span></span>|[<span data-ttu-id="79336-126">Du kan bruge opgavekøer til at planlægge opgaver</span><span class="sxs-lookup"><span data-stu-id="79336-126">Use Job Queues to Schedule Tasks</span></span>](admin-job-queues-schedule-tasks.md)|  
|<span data-ttu-id="79336-127">Administrere, slette eller komprimere dokumenter</span><span class="sxs-lookup"><span data-stu-id="79336-127">Manage, delete, or compress documents</span></span>|[<span data-ttu-id="79336-128">Administrere dokumenter</span><span class="sxs-lookup"><span data-stu-id="79336-128">Manage Documents</span></span>](admin-manage-documents.md)|  
|<span data-ttu-id="79336-129">Oprette en ny koncernvirksomhed ved hjælp af skabeloner</span><span class="sxs-lookup"><span data-stu-id="79336-129">Set up a new business unit using templates</span></span>|<span data-ttu-id="79336-130">[Oprettelse af nye virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span><span class="sxs-lookup"><span data-stu-id="79336-130">[Creating New Companies in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)</span></span>|  

## <a name="see-also"></a><span data-ttu-id="79336-131">Se også</span><span class="sxs-lookup"><span data-stu-id="79336-131">See Also</span></span>
[<span data-ttu-id="79336-132">Forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="79336-132">Business Functionality</span></span>](madeira-business-functionality.md)  
[<span data-ttu-id="79336-133">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="79336-133">General Business Functionality</span></span>](ui-across-business-areas.md)  
<span data-ttu-id="79336-134">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="79336-134">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
<span data-ttu-id="79336-135">[Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="79336-135">[Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)</span></span>  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

