---
title: Udvidelser af skymigrering
description: Brug skymigreringsudvidelserne til at flytte lokale data til Business Central online. Disse udvidelser flytter data, der findes i den lokale sky, til skyen, så du kan bruge Business Central online med dine eksisterende data.
author: jenolson
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.reviewer: edupont
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f02face497affd1fd1467c118e10e69f2be39b85
ms.sourcegitcommit: 951d3c9d541f0b1d26712d37e253c2958dae3321
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889120"
---
# <a name="cloud-migration-extensions-for-migrating-to-business-central-online"></a><span data-ttu-id="1c0d4-104">Udvidelser af skymigrering for migrering til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="1c0d4-104">Cloud Migration Extensions for Migrating to Business Central Online</span></span>

<span data-ttu-id="1c0d4-105">Afhængigt af løsningen i det lokale miljø, skal du bruge forskellige filtypenavne til at oprette forbindelse til dine data med [!INCLUDE[prod_short](includes/prod_short.md)] online for at kunne overflytte løsningen til skyen.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-105">Depending on your on-premises solution, you must use different extensions to connect your data with [!INCLUDE[prod_short](includes/prod_short.md)] online for purposes of migrating your solution to the cloud.</span></span>  

<span data-ttu-id="1c0d4-106">Hvis du bruger et af de understøttede lokale produkter, kan du konfigurere dit skymiljø baseret på en produktspecifik udvidelse.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-106">If you are using one of the supported on-premises products, you can configure your cloud environment based on a product-specific extension.</span></span> <span data-ttu-id="1c0d4-107">Når dit skymiljø er konfigureret, kan du flytte data fra din lokale løsning til [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1c0d4-107">Once your cloud environment is configured, you will be able to migrate data from your on-premises solution to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="1c0d4-108">Dette gør det muligt for dig at få fuldt udbytte af, hvad skyen kan tilbyde din virksomhed f.eks. udvidet indsigt i din virksomhed, kunstig intelligens, adgang til flere enheder og adgang overalt og til enhver tid.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-108">This will enable you to take full advantage of what the cloud has to offer your business such as, enhanced insights into your business, artificial intelligence, multiple device access, and anytime, anywhere access.</span></span>  

<span data-ttu-id="1c0d4-109">Du kan finde flere oplysninger i [Overførsel af lokale data til Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) i administrationsindholdet for [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="1c0d4-109">For more information, see [Migrating On-Premises Data to Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) in the administration content for [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  

## <a name="business-central-on-premises"></a><span data-ttu-id="1c0d4-110">Business Central til det lokale miljø</span><span class="sxs-lookup"><span data-stu-id="1c0d4-110">Business Central on-premises</span></span>

<span data-ttu-id="1c0d4-111">Hvis du bruger en lokal installation af [!INCLUDE[prod_short](includes/prod_short.md)], skal du hente **Intelligent sky basis**-udvidelsen og **Intelligent sky i Business Central**-udvidelsen og derefter køre den assisterede opsætningsvejledning **Konfiguration af skymigrering**.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-111">If you are using an on-premises deployment of [!INCLUDE[prod_short](includes/prod_short.md)], get the **Intelligent Cloud Base** extension and the **Business Central Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="dynamics-gp"></a><span data-ttu-id="1c0d4-112">Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="1c0d4-112">Dynamics GP</span></span>

<span data-ttu-id="1c0d4-113">Hvis du bruger Dynamics GP, skal du hente **Intelligent sky basisudvidelsen** og  **Dynamics GP Intelligent sky**-udvidelsen og derefter køre den assisterede opsætningsvejledning **Konfiguration af skymigrering**.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-113">If you are using Dynamics GP,  get the **Intelligent Cloud Base Extension** extension and the **Dynamics GP Intelligent Cloud** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="1c0d4-114">Overførsel fra Dynamics GP ved hjælp af vejledningen **Konfigurer skymigrering** som assisteret opsætning understøttes i øjeblikket kun på følgende markeder: USA, Canada, Storbritannien.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-114">Migrating from Dynamics GP using the **Cloud Migration Setup** assisted setup guide is currently only supported for the following markets: United States, Canada, United Kingdom.</span></span>

## <a name="dynamics-sl"></a><span data-ttu-id="1c0d4-115">Dynamics SL</span><span class="sxs-lookup"><span data-stu-id="1c0d4-115">Dynamics SL</span></span>

<span data-ttu-id="1c0d4-116">Hvis du bruger Dynamics SL, skal du hente udvidelsen **Intelligent cloudbase**, udvidelsen **Intelligent sky i Microsoft Dynamics SL** og udvidelsen **SmartLists for Microsoft Dynamics SL-historik** og derefter køre den assisterede opsætningsvejledning **Konfiguration af cloudmigrering**.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-116">If you are using Dynamics SL, get the **Intelligent Cloud Base** extension, the **Microsoft Dynamics SL Intelligent Cloud** extension and the **Microsoft Dynamics SL History SmartLists** extension, and then run the **Cloud Migration Setup** assisted setup guide.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1c0d4-117">Se også</span><span class="sxs-lookup"><span data-stu-id="1c0d4-117">See Also</span></span>

[<span data-ttu-id="1c0d4-118">Udvidelser af skymigreringsbase</span><span class="sxs-lookup"><span data-stu-id="1c0d4-118">Cloud Migration Base Extension</span></span>](ui-extensions-intelligent-cloud.md)  
[<span data-ttu-id="1c0d4-119">Overførsel af lokale data til Business Central Online</span><span class="sxs-lookup"><span data-stu-id="1c0d4-119">Migrating On-Premises Data to Business Central Online</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-data)  

[!INCLUDE[footer-include](includes/footer-banner.md)]