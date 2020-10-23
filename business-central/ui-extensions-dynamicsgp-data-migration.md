---
title: Overføre data fra Dynamics GP før 15.3 | Microsoft Docs
description: Før opdatering 15.3 kunne du bruge udvidelsen Dataoverførsel i Dynamics GP til at overføre debitorer, kreditorer, lagervarer, finanskonti, åbne transaktioner for tilgodehavender og skyldige beløb fra Dynamics GP til Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ROBOTS: NOINDEX
ms.openlocfilehash: 7c17c5f54553e7960f4386918bda640fa2e0380e
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915181"
---
# <a name="the-dynamics-gp-data-migration-extension"></a><span data-ttu-id="e2f40-103">Udvidelsen Overførsel af data med Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="e2f40-103">The Dynamics GP Data Migration Extension</span></span>

> [!NOTE]
> <span data-ttu-id="e2f40-104">Udvidelsen er udfaset i 15.3-opdateringen.</span><span class="sxs-lookup"><span data-stu-id="e2f40-104">This extension is deprecated in the 15.3 update.</span></span> <span data-ttu-id="e2f40-105">Det anbefales, at brugere, der vil overflytte fra Dynamics GP, begynder at bruge guiden **Skymigrering** i stedet.</span><span class="sxs-lookup"><span data-stu-id="e2f40-105">We recommend that users who want to migrate from Dynamics GP start using the **Cloud Migration** wizard instead.</span></span> <span data-ttu-id="e2f40-106">**Skymigrering**-udvidelsen har mere robust funktionalitet og henter flere data til Business Central fra Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="e2f40-106">The **Cloud Migration** extension has more robust functionality and brings more data into Business Central from Dynamics GP.</span></span> <span data-ttu-id="e2f40-107">Du kan finde flere oplysninger i [Overføre til Business Central Online fra Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) i administrationsindholdet for [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="e2f40-107">For more information, see [Migrate to Business Central Online from Dynamics GP](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp) in the administration content for [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

## <a name="see-also"></a><span data-ttu-id="e2f40-108">Se også</span><span class="sxs-lookup"><span data-stu-id="e2f40-108">See Also</span></span>

[<span data-ttu-id="e2f40-109">Intelligente skyudvidelser til skymigrering</span><span class="sxs-lookup"><span data-stu-id="e2f40-109">Intelligent Cloud Extensions for Cloud Migration</span></span>](ui-extensions-data-replication.md)  
[<span data-ttu-id="e2f40-110">Importer virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="e2f40-110">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="e2f40-111">[Tilpasse [!INCLUDE[prodshort](includes/prodshort.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="e2f40-111">[Customizing [!INCLUDE[prodshort](includes/prodshort.md)] Using Extensions ](ui-extensions.md)</span></span>  
[<span data-ttu-id="e2f40-112">Overføre til Business Central Online fra Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="e2f40-112">Migrate to Business Central Online from Dynamics GP</span></span>](/dynamics365/business-central/dev-itpro/administration/migrate-dynamics-gp)  
