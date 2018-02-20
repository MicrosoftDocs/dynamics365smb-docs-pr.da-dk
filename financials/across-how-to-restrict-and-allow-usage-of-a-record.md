---
title: "Fremgangsmåde: Begrænse og tillade brug af en post | Microsoft Docs"
description: "Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 4636cdedc2c99d1aa7cfc2dc361f7135aa3c4199
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrænse og tillade brugen af en record
Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten. Et arbejdsgangsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne. Et andet arbejdsgangsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne. Der findes to svar i den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] til dette formål: **Begræns brugen af en record.** og **Tillad brugen af en record**.

> [!NOTE]  
>  Den generelle version af [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check. For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.  

> [!NOTE]  
>  Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.

Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt. Den nye arbejdsgang baseres på den eksisterende arbejdsgangskabelon Arbejdsgang for godkendelse af købsfaktura.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Sådan opretter du et trin i en arbejdsgang, som begrænser bogføring af ikke-godkendte købsordrer  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2. I vinduet **Workflows** skal du oprette et nyt workflow med navnet Godkendelsesworkflow for købsordre. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  
3. Vælg handlingen **Kopiér fra arbejdsgangsskabelon**.  
4. Vælg feltet **Kildearbejdsgangskode**, og vælg derefter i vinduet **Workflowskabeloner** workflowskabelonen Godkendelsesworkflow for købsfaktura.  

     Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer. Fortsæt for at ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.  
5. I oversigtspanelet **Workflowtrin** skal du vælge feltet **Hændelsesbetingelser** og derefter vælge **Ordre** for filteret **Dokumenttype**.  
6. Fortsæt med at redigere, slette eller tilføje andre trin i arbejdsgangen for at tilpasse til en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.  

## <a name="see-also"></a>Se også  
[Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Workflow](across-workflow.md)   

