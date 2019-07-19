---
title: Fejlfinding i forbindelse med synkroniseringsfejl | Microsoft Docs
description: I denne artikel gives vejledning til identifikation og løsning af synkroniseringsfejl.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726786"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="833c9-103">Fejlfinding i forbindelse med synkroniseringsfejl</span><span class="sxs-lookup"><span data-stu-id="833c9-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="833c9-104">Der skal flyttes mange forskellige dele, når [!INCLUDE[d365fin](includes/d365fin_md.md)] skal integreres med [!INCLUDE[crm_md](includes/crm_md.md)], og nogle gange går tingene forkert.</span><span class="sxs-lookup"><span data-stu-id="833c9-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="833c9-105">I dette emne beskrives nogle af de mest almindelige fejl, der opstår, og der angives oplysninger om, hvordan de kan løses.</span><span class="sxs-lookup"><span data-stu-id="833c9-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="833c9-106">Fejl opstår ofte, fordi en bruger har udført handlinger på sammenkædede poster, eller fordi, der er noget galt med den måde, integrationen er konfigureret på.</span><span class="sxs-lookup"><span data-stu-id="833c9-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="833c9-107">Fejl, der vedrører sammenkædede poster, kan brugerne selv løse.</span><span class="sxs-lookup"><span data-stu-id="833c9-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="833c9-108">Disse fejl skyldes handlinger som f.eks. sletning af en post i en, men ikke begge forretningsapps med efterfølgende synkronisering.</span><span class="sxs-lookup"><span data-stu-id="833c9-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="833c9-109">Du kan finde flere oplysninger under [Se status på en synkronisering](admin-how-to-view-synchronization-status.md).</span><span class="sxs-lookup"><span data-stu-id="833c9-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="833c9-110">Fejl, der er relateret til, hvordan integrationen er konfigureret, kræver typisk handlinger udført af en administrator.</span><span class="sxs-lookup"><span data-stu-id="833c9-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="833c9-111">Du kan få vist fejlene på siden **Integrationssynkroniseringsfejl**.</span><span class="sxs-lookup"><span data-stu-id="833c9-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="833c9-112">Eksempler på typiske problemer omfatter:</span><span class="sxs-lookup"><span data-stu-id="833c9-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="833c9-113">De tilladelser og roller, der er tildelt til brugere, er ikke korrekte.</span><span class="sxs-lookup"><span data-stu-id="833c9-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="833c9-114">Administratorkontoen blev angivet som integrationsbrugeren.</span><span class="sxs-lookup"><span data-stu-id="833c9-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="833c9-115">Integrationsbrugerens adgangskode er indstillet til at kræve en ændring, når brugeren logger på.</span><span class="sxs-lookup"><span data-stu-id="833c9-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="833c9-116">Valutakurserne er ikke angivet i den ene eller den anden app.</span><span class="sxs-lookup"><span data-stu-id="833c9-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="833c9-117">Du skal rette fejlene manuelt, men du kan få visse former for hjælp på siden.</span><span class="sxs-lookup"><span data-stu-id="833c9-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="833c9-118">Eksempler:</span><span class="sxs-lookup"><span data-stu-id="833c9-118">For example:</span></span>  

* <span data-ttu-id="833c9-119">Felterne **Kilde** og **Destination** kan indeholde links til den post, hvor fejlen blev fundet.</span><span class="sxs-lookup"><span data-stu-id="833c9-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="833c9-120">Klik på linket for at åbne posten og undersøge fejlen.</span><span class="sxs-lookup"><span data-stu-id="833c9-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="833c9-121">Handlingerne **Slet poster, der er ældre end syv dage** og **Slet alle poster** rydder op på listen.</span><span class="sxs-lookup"><span data-stu-id="833c9-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="833c9-122">Du bruger typisk disse handlinger, når du har fundet årsagen til en fejl, der påvirker mange poster.</span><span class="sxs-lookup"><span data-stu-id="833c9-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="833c9-123">Men gå forsigtigt frem.</span><span class="sxs-lookup"><span data-stu-id="833c9-123">Use caution, however.</span></span> <span data-ttu-id="833c9-124">Disse handlinger kan muligvis slette fejl, der stadig er relevante.</span><span class="sxs-lookup"><span data-stu-id="833c9-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="833c9-125">Se også</span><span class="sxs-lookup"><span data-stu-id="833c9-125">See Also</span></span>
<span data-ttu-id="833c9-126">[Integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="833c9-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="833c9-127">[Konfigurere brugerkonti til integration med [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="833c9-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="833c9-128">[Oprette en forbindelse til [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="833c9-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="833c9-129">Sammenkæde og synkronisere poster manuelt</span><span class="sxs-lookup"><span data-stu-id="833c9-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="833c9-130">Se status på en synkronisering</span><span class="sxs-lookup"><span data-stu-id="833c9-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  