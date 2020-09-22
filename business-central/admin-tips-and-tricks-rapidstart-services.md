---
title: Tip - RapidStart Services | Microsoft Docs
description: Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/18/2020
ms.author: edupont
ms.openlocfilehash: e1c3dfe37e6288934d05c4e2d9294cf87da49537
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3786117"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="0048a-103">Tip: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0048a-103">Tips and Tricks: RapidStart Services</span></span>

<span data-ttu-id="0048a-104">Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.</span><span class="sxs-lookup"><span data-stu-id="0048a-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="0048a-105">Udnytte fordelen ved konfigurationsskabeloner</span><span class="sxs-lookup"><span data-stu-id="0048a-105">Take advantage of configuration templates</span></span>

<span data-ttu-id="0048a-106">Konfigurationsskabeloner kan hjælpe dig med at strømline implementeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="0048a-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="0048a-107">Ved hjælp af dem kan du inkludere lignende kunder i segmenter og derefter udarbejde en protokol til implementering, der behandler alle kunder i et segment på samme måde.</span><span class="sxs-lookup"><span data-stu-id="0048a-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="0048a-108">På denne måde kan du anvende et niveau af forudkonfiguration til hvert segment og fortsætte med en hurtig implementering.</span><span class="sxs-lookup"><span data-stu-id="0048a-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="0048a-109">Konfigurationsspørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="0048a-109">Configuration questionnaires</span></span>

<span data-ttu-id="0048a-110">Du skal overveje at definere standardsvar for at angive de bedste fremgangsmåder, som en støtte til processen med at udfylde et konfigurationsspørgeskema.</span><span class="sxs-lookup"><span data-stu-id="0048a-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="0048a-111">Batchoprettelse af kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="0048a-111">Batch creation of journal lines</span></span>

<span data-ttu-id="0048a-112">Vi anbefaler, at du bruger de leverede værktøjer til dataoverflytning til at overflytte journalposter.</span><span class="sxs-lookup"><span data-stu-id="0048a-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="0048a-113">Hvis du bruger et batchjob til at oprette kladdelinjer, har dette et begrænset omfang og opretter kun præ-standardfelter i en kladde.</span><span class="sxs-lookup"><span data-stu-id="0048a-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="0048a-114">Resten af kladden skal derefter udfyldes manuelt.</span><span class="sxs-lookup"><span data-stu-id="0048a-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="0048a-115">Overflytning af transaktioner</span><span class="sxs-lookup"><span data-stu-id="0048a-115">Migrating transactions</span></span>

<span data-ttu-id="0048a-116">Vi anbefaler, at du overflytter startsaldoer i følgende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0048a-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines-->

1. <span data-ttu-id="0048a-117">Overflytte startsaldoer for regnskab uden brug af underregnskaber i finans.</span><span class="sxs-lookup"><span data-stu-id="0048a-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="0048a-118">Brug af specifikke primosaldo modregningskonti, én opsat for hvert underregnskab.</span><span class="sxs-lookup"><span data-stu-id="0048a-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="0048a-119">Konfigurer modregningskontiene til at aktivere direkte bogføring.</span><span class="sxs-lookup"><span data-stu-id="0048a-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2. <span data-ttu-id="0048a-120">Overflyt åbne debitorposter.</span><span class="sxs-lookup"><span data-stu-id="0048a-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3. <span data-ttu-id="0048a-121">Overflyt åbne vareposter.</span><span class="sxs-lookup"><span data-stu-id="0048a-121">Migrate open item ledger entries.</span></span>  
4. <span data-ttu-id="0048a-122">Overflyt åbne anlægsposter.</span><span class="sxs-lookup"><span data-stu-id="0048a-122">Migrate open fixed asset entries.</span></span>  

## <a name="make-each-package-manageable"></a><span data-ttu-id="0048a-123">Gøre hver pakke håndterbar</span><span class="sxs-lookup"><span data-stu-id="0048a-123">Make each package manageable</span></span>

<span data-ttu-id="0048a-124">Når du bruger konfigurationspakker til at overføre data, skal du opdele dataene i separate pakker, så de er nemmere at overføre.</span><span class="sxs-lookup"><span data-stu-id="0048a-124">When you use configuration packages to migrate data, separate the data into separate packages for easier portability.</span></span> <span data-ttu-id="0048a-125">Hvis du f.eks. vil overføre 20 års finansposter, kan det tage mange timer og dage, før importen er udført.</span><span class="sxs-lookup"><span data-stu-id="0048a-125">For example, if you want to migrate 20 years of ledger entries, the import might take many hours and days.</span></span> <span data-ttu-id="0048a-126">I stedet skal du opdele dataene, så de enkelte pakker bliver nemmere at håndtere.</span><span class="sxs-lookup"><span data-stu-id="0048a-126">Instead, split the data up so that each package becomes more manageable.</span></span> <span data-ttu-id="0048a-127">I øjeblikket er der ingen faste regler for, hvad der gør en pakke håndterbar, men hvis du har problemer med at importere eller eksportere en pakke, skal du gøre den mindre og se, om det hjælper.</span><span class="sxs-lookup"><span data-stu-id="0048a-127">Currently, there are no firm rules for what makes a package performant, but if you see problems importing or exporting a package, try making it smaller and see if that helps.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0048a-128">Se også</span><span class="sxs-lookup"><span data-stu-id="0048a-128">See Also</span></span>

[<span data-ttu-id="0048a-129">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="0048a-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="0048a-130">Opsætning</span><span class="sxs-lookup"><span data-stu-id="0048a-130">Administration</span></span>](admin-setup-and-administration.md)  
