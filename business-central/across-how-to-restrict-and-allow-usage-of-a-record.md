---
title: Sådan begrænses og tillades brug af en post
description: Hvis du vil begrænse brugen af en post, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: bd7382730a70295693a9feb70ff67d9fb6344717
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6438303"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrænse og tillade brugen af en record
Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten. Et arbejdsgangsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne. Et andet arbejdsgangsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne. Der findes to svar i den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] til dette formål: **Begræns brugen af en record.** og **Tillad brugen af en record**.

> [!NOTE]  
>  Den generelle version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check. For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.  

> [!NOTE]  
>  Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.

Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt. Den nye arbejdsgang baseres på den eksisterende arbejdsgangskabelon Arbejdsgang for godkendelse af købsfaktura.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Sådan opretter du et trin i en arbejdsgang, som begrænser bogføring af ikke-godkendte købsordrer  
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Arbejdsflow**, og vælg derefter det relaterede link.  
2. På siden **Workflows** skal du oprette et nyt workflow med navnet Godkendelsesworkflow for købsordre. Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).  
3. Vælg handlingen **Kopiér fra arbejdsgangsskabelon**.  
4. Vælg feltet **Kildearbejdsgangskode**, og vælg derefter på siden **Workflowskabeloner** workflowskabelonen Godkendelsesworkflow for købsfaktura.  

     Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer. Fortsæt for at ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.  
5. I oversigtspanelet **Workflowtrin** skal du vælge feltet **Hændelsesbetingelser** og derefter vælge **Ordre** for filteret **Dokumenttype**.  
6. Fortsæt med at redigere, slette eller tilføje andre trin i arbejdsgangen for at tilpasse til en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.  

## <a name="see-also"></a>Se også  
[Oprette arbejdsgange](across-how-to-create-workflows.md)   
[Workflow](across-workflow.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]