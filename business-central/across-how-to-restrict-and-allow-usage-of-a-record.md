---
title: Sådan begrænses og tillades brug af en post
description: Hvis du vil begrænse brugen af en post, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2021
ms.author: edupont
ms.openlocfilehash: 7873091d64e55460986437cf255d98cd0d00b6d3
ms.sourcegitcommit: f1e272485a0e675d337a694aba3e35a5daf43920
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130141"
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrænse og tillade brugen af en record

Hvis du vil begrænse brugen af en record, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten. Et arbejdsgangsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne. Et andet arbejdsgangsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne. Der er to svar i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] til dette formål: **Tilføj postbegrænsning** og **Fjern postbegrænsning**.

> [!NOTE]  
> Standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check. For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.  

> [!NOTE]  
> Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.

Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt. Den nye arbejdsgang baseres på den eksisterende skabelon Godkendelsesworkflow for købsfaktura.  

## <a name="to-create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Sådan opretter du et trin i en arbejdsgang, som begrænser bogføring af ikke-godkendte købsordrer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. På siden **Workflows** skal du vælge handlingen **Nyt workflow fra skabelon**. Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).
3. På siden **Workflowskabeloner** skal du vælge skabelonen *Godkendelsesworkflow for købsfaktura*.  

   Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer. Fortsæt for at ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.  
4. I oversigtspanelet **Workflowtrin** skal du vælge feltet **På betingelse** for det første trin, og derefter skal du vælge **Ordre** for filteret **Dokumenttype**.  
5. Fortsæt med at redigere, slette eller tilføje andre trin i arbejdsgangen for at tilpasse til en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.  

## <a name="see-also"></a>Se også

[Oprette arbejdsgange](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]