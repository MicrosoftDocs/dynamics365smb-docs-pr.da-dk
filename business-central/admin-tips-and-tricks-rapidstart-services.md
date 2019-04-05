---
title: Tip - RapidStart Service | Microsoft Docs
description: Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 875ab6f5875a842fb4c2ab906f39ae95607f6ba8
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "793321"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="8607f-103">Tip: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8607f-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="8607f-104">Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.</span><span class="sxs-lookup"><span data-stu-id="8607f-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="8607f-105">Udnytte fordelen ved konfigurationsskabeloner</span><span class="sxs-lookup"><span data-stu-id="8607f-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="8607f-106">Konfigurationsskabeloner kan hjælpe dig med at strømline implementeringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="8607f-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="8607f-107">Ved hjælp af dem kan du inkludere lignende kunder i segmenter og derefter udarbejde en protokol til implementering, der behandler alle kunder i et segment på samme måde.</span><span class="sxs-lookup"><span data-stu-id="8607f-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="8607f-108">På denne måde kan du anvende et niveau af forudkonfiguration til hvert segment og fortsætte med en hurtig implementering.</span><span class="sxs-lookup"><span data-stu-id="8607f-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="8607f-109">Konfigurationsspørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="8607f-109">Configuration questionnaires</span></span>  
<span data-ttu-id="8607f-110">Du skal overveje at definere standardsvar for at angive de bedste fremgangsmåder, som en støtte til processen med at udfylde et konfigurationsspørgeskema.</span><span class="sxs-lookup"><span data-stu-id="8607f-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="8607f-111">Batchoprettelse af kladdelinjer</span><span class="sxs-lookup"><span data-stu-id="8607f-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="8607f-112">Vi anbefaler, at du bruger de leverede værktøjer til dataoverflytning til at overflytte journalposter.</span><span class="sxs-lookup"><span data-stu-id="8607f-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="8607f-113">Hvis du bruger et batchjob til at oprette kladdelinjer, har dette et begrænset omfang og opretter kun præ-standardfelter i en kladde.</span><span class="sxs-lookup"><span data-stu-id="8607f-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="8607f-114">Resten af kladden skal derefter udfyldes manuelt.</span><span class="sxs-lookup"><span data-stu-id="8607f-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="8607f-115">Overflytning af transaktioner</span><span class="sxs-lookup"><span data-stu-id="8607f-115">Migrating transactions</span></span>  
<span data-ttu-id="8607f-116">Vi anbefaler, at du overflytter startsaldoer i følgende rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="8607f-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="8607f-117">Overflytte startsaldoer for regnskab uden brug af underregnskaber i finans.</span><span class="sxs-lookup"><span data-stu-id="8607f-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="8607f-118">Brug af specifikke primosaldo modregningskonti, én opsat for hvert underregnskab.</span><span class="sxs-lookup"><span data-stu-id="8607f-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="8607f-119">Konfigurer modregningskontiene til at aktivere direkte bogføring.</span><span class="sxs-lookup"><span data-stu-id="8607f-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="8607f-120">Overflyt åbne debitorposter.</span><span class="sxs-lookup"><span data-stu-id="8607f-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="8607f-121">Overflyt åbne vareposter.</span><span class="sxs-lookup"><span data-stu-id="8607f-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="8607f-122">Overflyt åbne anlægsposter.</span><span class="sxs-lookup"><span data-stu-id="8607f-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8607f-123">Se også</span><span class="sxs-lookup"><span data-stu-id="8607f-123">See Also</span></span>  
[<span data-ttu-id="8607f-124">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="8607f-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="8607f-125">Opsætning</span><span class="sxs-lookup"><span data-stu-id="8607f-125">Administration</span></span>](admin-setup-and-administration.md)
