---
title: Sådan begrænses og tillades brug af en post
description: 'Hvis du vil begrænse brugen af en post, kan du integrere to arbejdsgangssvar i en arbejdsgang, der styrer forbruget af posten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/08/2022
ms.author: edupont
---
# <a name="restrict-and-allow-usage-of-a-record"></a>Begrænse og tillade brugen af en record

Hvis du vil begrænse brugen af en post, f.eks. i bestemte aktiviteter, kan du integrere to arbejdsgangssvar i workflowet, der styrer forbruget af posten. Et workflowsvar begrænser brugen af posten, som defineret i arbejdsganghændelsen og -betingelserne. Det andet workflowsvar tillader brug af posten, som defineret i arbejdsganghændelsen og -betingelserne. Der er to svar i standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] til dette formål: **Tilføj postbegrænsning** og **Fjern postbegrænsning**.

> [!NOTE]  
> Standardversionen af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter begrænsning af bogføring af en post, eksport af en post som en betaling og udskrivning af en post som en check. For at understøtte andre begrænsninger skal en Microsoft-partner tilpasse programkoden.  

> [!NOTE]  
> Arbejdsgangfunktionen, som begrænser og tillader brug af poster, er ikke relateret til funktioner, der blokerer bogføring af vare-, debitor- og kreditorposter.

Følgende fremgangsmåde beskriver, hvordan du kan begrænse bogføring af købsordrer, indtil de er godkendt. Den nye arbejdsgang baseres på den eksisterende skabelon *Godkendelsesworkflow for købsfaktura*.  

## <a name="create-a-workflow-step-that-restricts-posting-of-unapproved-purchase-orders"></a>Oprette et trin i et workflow, som begrænser bogføring af ikke-godkendte købsordrer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.  
2. På siden **Workflows** skal du vælge handlingen **Nyt workflow fra skabelon**. Flere oplysninger [Oprette workflows fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).
3. På siden **Workflowskabeloner** skal du vælge skabelonen *Godkendelsesworkflow for købsfaktura*.  

   Bemærk, at de to første trin i arbejdsgangen drejer sig om at begrænse og derefter tillade brug af købsfakturaer. Ændre hændelsesbetingelsen i det første trin af den nye arbejdsgang for at angive, at den gælder for købsordrer.  
4. I oversigtspanelet **Workflowtrin** skal du vælge feltet **På betingelse** for det første trin og **Ordre** for filteret **Dokumenttype**.  
5. Fortsæt med at redigere, slette eller tilføje andre workflowtrin for at reflektere en forretningsproces, der begynder med at begrænse bogføring af ikke-godkendte købsordrer.  

## <a name="see-also"></a>Se også

[Bruge godkendelsesworkflows](across-use-workflows.md)  
[Opret godkendelsesworkflows](across-how-to-create-workflows.md)  
[Workflow](across-workflow.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
