---
title: "Bedste fremgangsmåder for opsætning af global planlægning | Microsoft Docs"
description: "Oversigtpanelet **Planlægning** i vinduet **Produktionsopsætning** indeholder flere felter, der definerer globale regler for forsyningsplanlægning."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1201f7d7abf5d85e17a60b9663a479b7ec12f70a
ms.contentlocale: da-dk
ms.lasthandoff: 09/28/2018

---
# <a name="setup-best-practices-global-planning-setup"></a><span data-ttu-id="a0643-103">Konfigurere bedste fremgangsmåder: Global planlægningsopsætning</span><span class="sxs-lookup"><span data-stu-id="a0643-103">Setup Best Practices: Global Planning Setup</span></span>
<span data-ttu-id="a0643-104">Oversigtpanelet **Planlægning** i vinduet **Produktionsopsætning** indeholder flere felter, der definerer globale regler for forsyningsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="a0643-104">The **Planning** FastTab in the **Manufacturing Setup** window contains several fields that define global rules for supply planning.</span></span>  

 <span data-ttu-id="a0643-105">Følgende tabel viser de bedste fremgangsmåder til konfiguration af udvalgte globale felter med planlægningsparametre.</span><span class="sxs-lookup"><span data-stu-id="a0643-105">The following table provides best practices on how to set up selected global planning parameter fields.</span></span> <span data-ttu-id="a0643-106">Du kan få yderligere oplysninger om et felt ved at vælge linket i kolonnen **Opsætningsfelt**.</span><span class="sxs-lookup"><span data-stu-id="a0643-106">For more information about a field, choose the link in the **Setup field** column.</span></span>  

|<span data-ttu-id="a0643-107">Angive indstillinger for felt</span><span class="sxs-lookup"><span data-stu-id="a0643-107">Setup field</span></span>|<span data-ttu-id="a0643-108">Bedste fremgangsmåde</span><span class="sxs-lookup"><span data-stu-id="a0643-108">Best practice</span></span>|<span data-ttu-id="a0643-109">Bemærkning</span><span class="sxs-lookup"><span data-stu-id="a0643-109">Comment</span></span>|  
|-----------------|-------------------|-------------|  
|<span data-ttu-id="a0643-110">Forecast på lokationer</span><span class="sxs-lookup"><span data-stu-id="a0643-110">Use Forecast on Locations</span></span>|<span data-ttu-id="a0643-111">Vælg denne indstilling, hvis du har prognoser for bestemte lokationer.</span><span class="sxs-lookup"><span data-stu-id="a0643-111">Select if you have forecasts for specific locations.</span></span>||  
|<span data-ttu-id="a0643-112">Komponenter på lokation</span><span class="sxs-lookup"><span data-stu-id="a0643-112">Components at Location</span></span>|<span data-ttu-id="a0643-113">Hvis varerne ikke er defineret som lagervarer, skal du vælge lokationskoden til hovedlageret.</span><span class="sxs-lookup"><span data-stu-id="a0643-113">If items are not defined as SKUs, select the location code of your main warehouse.</span></span>|<span data-ttu-id="a0643-114">Dette gælder også, hvis du kun bruger indkøbskladden.</span><span class="sxs-lookup"><span data-stu-id="a0643-114">This also applies if you only use the requisition worksheet.</span></span>|  
|<span data-ttu-id="a0643-115">Tomt overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="a0643-115">Blank Overflow Level</span></span>|<span data-ttu-id="a0643-116">Vælg **Tillad standardberegning** Hvis du overfører fra Microsoft Dynamics NAV 5.0 eller tidligere.</span><span class="sxs-lookup"><span data-stu-id="a0643-116">Select **Allow Default Calculation** if you are migrating from Microsoft Dynamics NAV 5.0 or earlier.</span></span>|<span data-ttu-id="a0643-117">Skal kun bruges, hvis du vil tillade alle eller nogle af varerne at løbe over genbestillingspunktet.</span><span class="sxs-lookup"><span data-stu-id="a0643-117">Use only if you want to allow all or some of your items to overflow the reorder point.</span></span>|  
|<span data-ttu-id="a0643-118">Standardbufferperiode</span><span class="sxs-lookup"><span data-stu-id="a0643-118">Default Dampener Period</span></span>|<span data-ttu-id="a0643-119">Indstillingen skal ligge mellem 1D og 5D.</span><span class="sxs-lookup"><span data-stu-id="a0643-119">Set between 1D and 5D.</span></span><br /><br /> <span data-ttu-id="a0643-120">Hvis du er nybegynder i planlægning i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive en længere periode.</span><span class="sxs-lookup"><span data-stu-id="a0643-120">If new to planning in [!INCLUDE[d365fin](includes/d365fin_md.md)], then set a longer period.</span></span>|<span data-ttu-id="a0643-121">Når brugerne er mere fortrolige med de forskellige årsager til aktionsmeddelelser, kan du afkorte bufferperioden for at tillade flere ændringsforslag.</span><span class="sxs-lookup"><span data-stu-id="a0643-121">When users are more familiar with the different reasons for action messages, then shorten the dampener period to allow more change suggestions.</span></span>|  
|<span data-ttu-id="a0643-122">Standardbufferantal</span><span class="sxs-lookup"><span data-stu-id="a0643-122">Default Dampener Quantity</span></span>|<span data-ttu-id="a0643-123">Indstilles til mellem 5 og 20 % af varens lotstørrelse.</span><span class="sxs-lookup"><span data-stu-id="a0643-123">Set between 5 and 20 percent of the item’s lot size.</span></span>||  

## <a name="see-also"></a><span data-ttu-id="a0643-124">Se også</span><span class="sxs-lookup"><span data-stu-id="a0643-124">See Also</span></span>  
 <span data-ttu-id="a0643-125">[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a0643-125">[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md) </span></span>  
 <span data-ttu-id="a0643-126">[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="a0643-126">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
 [<span data-ttu-id="a0643-127">Opret komplekse moduler ved hjælp af bedste praksis</span><span class="sxs-lookup"><span data-stu-id="a0643-127">Set Up Complex Application Areas Using Best Practices</span></span>](set-up-complex-application-areas-using-best-practices.md)  
 <span data-ttu-id="a0643-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a0643-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

