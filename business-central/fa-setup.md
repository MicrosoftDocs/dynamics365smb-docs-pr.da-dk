---
title: "Konfigurere anlægsaktiver | Microsoft Docs"
description: "Få mere at vide om den række af opgaver, du skal udføre for at oprette anlægsaktiver, f.eks. maskiner eller bygninger."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c20d4997e84db416e2103d2318533082adc04b49
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="f9b96-103">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="f9b96-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="f9b96-104">Før du kan arbejde med anlægsaktiver, skal du angive et par ting:</span><span class="sxs-lookup"><span data-stu-id="f9b96-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="f9b96-105">Hvordan du forsikrer, vedligeholder og afskriver anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="f9b96-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="f9b96-106">Hvordan du registrerer omkostninger og andre værdier i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="f9b96-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="f9b96-107">Tabellen nedenfor indeholder links til flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="f9b96-107">The table below has links to more information.</span></span> <span data-ttu-id="f9b96-108">Når du konfigureret disse ting, kan du begynde på forskellige aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="f9b96-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="f9b96-109">Du kan finde flere oplysninger under [Anlægsaktiver](fa-manage.md).</span><span class="sxs-lookup"><span data-stu-id="f9b96-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="f9b96-110">Du kan registrere anlægstransaktioner i vinduet **Anlægskassekladde** eller vinduet **Anlægskladde**, afhængigt af, om transaktionerne, der er til finansiel rapportering eller intern administration.</span><span class="sxs-lookup"><span data-stu-id="f9b96-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="f9b96-111">Hjælp for Anlæg beskriver kun, hvordan du bruger vinduet **Anlægskassekladde**.</span><span class="sxs-lookup"><span data-stu-id="f9b96-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="f9b96-112">Når du vælger en anlægsaktivitet i afsnittet **Finansintegration** i vinduet **Afskrivningsprofilkort**, bruges vinduet **Anlægsfinanskladde** til at bogføre transaktioner for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="f9b96-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

<span data-ttu-id="f9b96-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="f9b96-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="f9b96-114">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="f9b96-114">To</span></span> | <span data-ttu-id="f9b96-115">Se</span><span class="sxs-lookup"><span data-stu-id="f9b96-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="f9b96-116">Konfigurer standardfinanskonti, allokeringsnøgler, kladdetyper og -navne for bogføringen af anlægsaktiver og definere anlægsarter og -grupper, f.eks materielle og immaterielle.</span><span class="sxs-lookup"><span data-stu-id="f9b96-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="f9b96-117">Angive generelle oplysninger om anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="f9b96-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="f9b96-118">Oprette afskrivningsprofiler, definere forskellige afskrivningsmetoder, integrere med finansregnskabet og muliggøre kopiering af poster i flere afskrivningsprofiler.</span><span class="sxs-lookup"><span data-stu-id="f9b96-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="f9b96-119">Opsætte afskrivning af anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="f9b96-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="f9b96-120">Aktivere forsikring af anlæg, angive generelle forsikringsoplysninger, oprette forsikringskort pr. police, og klargøre kladder til at bogføre forsikringsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="f9b96-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="f9b96-121">Definere anlægsforsikring</span><span class="sxs-lookup"><span data-stu-id="f9b96-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="f9b96-122">Udføre reparation af anlægsaktiver, angive generelle reparationsoplysninger, oprette bogføringskonti for reparation og definere typer af vedligeholdelsesarbejde.</span><span class="sxs-lookup"><span data-stu-id="f9b96-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="f9b96-123">Definere anlægsreparation</span><span class="sxs-lookup"><span data-stu-id="f9b96-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="f9b96-124">Få mere at vide om forskellige afskrivningsmetoder for anlægsaktiver.</span><span class="sxs-lookup"><span data-stu-id="f9b96-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="f9b96-125">Afskrivningsmetoder</span><span class="sxs-lookup"><span data-stu-id="f9b96-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="f9b96-126">Se også</span><span class="sxs-lookup"><span data-stu-id="f9b96-126">See Also</span></span>
[<span data-ttu-id="f9b96-127">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="f9b96-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="f9b96-128">Finans</span><span class="sxs-lookup"><span data-stu-id="f9b96-128">Finance</span></span>](finance.md)  
<span data-ttu-id="f9b96-129">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="f9b96-129">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="f9b96-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f9b96-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

