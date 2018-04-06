---
title: "Overførsel af data fra Dynamics GP med udvidelsen Dataoverførsel | Microsoft Docs"
description: "Du kan bruge udvidelsen Dataoverførsel i Dynamics GP til at overføre debitorer, kreditorer, lagervarer og konti fra Dynamics GP til Business Central."
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 5d689a43e3debe51cfbb9306252d0c9f75e7bb70
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a><span data-ttu-id="8be82-103">Udvidelsen Overførsel af Dynamics GP-data til Business Central</span><span class="sxs-lookup"><span data-stu-id="8be82-103">The Dynamics GP Data Migration Extension for Business Central</span></span> 
<span data-ttu-id="8be82-104">Denne udvidelse gør det nemt at overføre debitorer, kreditorer, lagervarer og konti fra Dynamics GP til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8be82-104">This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8be82-105">Hvis din virksomhed bruger Dynamics GP i dag, kan du eksportere de relevante stamdataposter og derefter åbne en assisteret opsætningsvejledning for at tilføje dataene i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8be82-105">If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="8be82-106">Du kan finde flere oplysninger under [Overføre virksomhedsdata fra andre økonomisystemer](upload-data.md).</span><span class="sxs-lookup"><span data-stu-id="8be82-106">For more information, see [Migrate Business Data from Other Finance Systems](upload-data.md).</span></span>

## <a name="exporting-data-from-dynamics-gp"></a><span data-ttu-id="8be82-107">Eksportere data fra Dynamics GP</span><span class="sxs-lookup"><span data-stu-id="8be82-107">Exporting Data from Dynamics GP</span></span>
<span data-ttu-id="8be82-108">Du skal have eksporteret nogle af eller alle dine eksisterende debitorer, kreditorer, lagervarer og konti til en fil ved hjælp af funktionen til dataeksport i Dynamics GP.</span><span class="sxs-lookup"><span data-stu-id="8be82-108">You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export.</span></span> <span data-ttu-id="8be82-109">I forbindelse med [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du eksportere følgende datatyper:</span><span class="sxs-lookup"><span data-stu-id="8be82-109">For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:</span></span>

* <span data-ttu-id="8be82-110">Konto</span><span class="sxs-lookup"><span data-stu-id="8be82-110">Account</span></span>  
* <span data-ttu-id="8be82-111">Kunde</span><span class="sxs-lookup"><span data-stu-id="8be82-111">Customer</span></span>  
* <span data-ttu-id="8be82-112">Vare</span><span class="sxs-lookup"><span data-stu-id="8be82-112">Item</span></span>  
* <span data-ttu-id="8be82-113">Kreditor</span><span class="sxs-lookup"><span data-stu-id="8be82-113">Vendor</span></span>  

<span data-ttu-id="8be82-114">Udvidelsen til overførsel af data til Dynamics GP tilknyttes automatisk de udlæste data, så dataene hurtigt er tilgængelige i det nye regnskab i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="8be82-114">The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company.</span></span> <span data-ttu-id="8be82-115">Under processen oprettes understøttende opsætningsoplysninger som f.eks. bogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="8be82-115">During the process, supporting setup information is created, such as posting groups.</span></span> <span data-ttu-id="8be82-116">Lagervarer overføres til systemet med FIFO som omkostningsevalueringsmetoden.</span><span class="sxs-lookup"><span data-stu-id="8be82-116">Inventory items will be brought into the system with FIFO as the cost valuation method.</span></span> <span data-ttu-id="8be82-117">Konti oprettes som hovedkontosegmentet fra Dynamics GP med dimensioner, fordi [!INCLUDE[d365fin](includes/d365fin_long_md.md)] ikke har kontosegmenter.</span><span class="sxs-lookup"><span data-stu-id="8be82-117">Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.</span></span>

## <a name="see-also"></a><span data-ttu-id="8be82-118">Se også</span><span class="sxs-lookup"><span data-stu-id="8be82-118">See Also</span></span>
[<span data-ttu-id="8be82-119">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="8be82-119">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="8be82-120">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="8be82-120">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  

