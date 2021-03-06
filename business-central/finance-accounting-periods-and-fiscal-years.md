---
title: Arbejde med regnskabsperioder og regnskabsår | Microsoft Docs
description: Lær, hvordan du arbejder med regnskabsperioder, der kan definere, hvornår virksomheden rapporterer finansielle resultater.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: ae13b3c24e73f9b73335291b2911f16d6acf29d0
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4751101"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Arbejde med regnskabsperioder og regnskabsår

Regnskabsperioder, der kaldes også rapporteringsperioder, er tidsperioder, hvor en virksomhed eller organisation rapporterer finansielle resultater, f.eks. ved at generere deres resultatopgørelse eller balance. Typisk henviser regnskabsperioder til virksomhedens regnskabsår, der kan indeholde flere regnskabsperioder, f.eks. måneder eller kvartaler.

For mange virksomheder falder regnskabsåret ikke sammen med kalenderåret. For eksempel kan regnskabsåret slutte den 30 juni i stedet for 31. december. For nyoprettede virksomheder kan regnskabsåret i realiteten være længere end 12 måneder.  

[!INCLUDE[prod_short](includes/prod_short.md)] kræver kun regnskabsperioder, hvis du vil lukke en resultatopgørelse eller udføre opgaver til komprimering af data. 

Du kan bruge regnskabsperioder i forbindelse med rapportering. F.eks. når du gennemgår bogførte poster på siden **Saldo/Budget**, hvor du kan angive rapporteringsintervallet. En af de indstillinger kan du angive for at rapportere regnskabsperiode. Du kan også oprette et kontoskema, der sammenligner resultaterne for forskellige perioder.

## <a name="creating-a-new-fiscal-year"></a>Oprette et nyt regnskabsår

Du kan oprette flere regnskabsperioder ad gangen ved hjælp af **Opret regnskabsår**-kørslen eller manuelt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Sådan oprettes flere regnskabsperioder ad gangen

Brug **Opret regnskabsår**-kørslen til at opdele et regnskabsår i perioder af samme varighed.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Opret år**.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder.  
4. I feltet **Antal perioder** kan du angive det antal perioder, du vil opdele regnskabsåret i. Der kan være op til 365 perioder pr. år.  
5. I feltet **Periodelængde** skal du angive en varighed for hver periode. F.eks. 1M for én måned, 1K for et kvartal og 1Å for et år.  
6. Vælg **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Sådan oprettes regnskabsperioder manuelt

Hvis regnskabsperioderne i regnskabsåret, der har forskellig varigheder som 4-4-5-kalender, der anvendes i detail, du kan oprette det manuelt.  
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder. Feltet **Navn** viser navnet på måneden.  
3. Marker afkrydsningsfeltet **Nyt regnskabsår** for at angive, at dette er den første periode i året. [!INCLUDE[prod_short](includes/prod_short.md)] bruger denne periode til at bestemme, hvilke perioder der skal lukkes ved udgangen af året.
4. Gentag trin 2 og 3 for hver resterende periode.  

## <a name="closing-a-fiscal-year"></a>Afslutning af regnskabsår

Lukning af regnskabsåret er en af opgaverne, når regnskaberne skal afsluttes. Når regnskabsåret er afsluttet, er felterne **Afsluttet** og **Dato låst** markeret for alle perioder i året. Du kan ikke genåbne et år eller fjerne markeringen i felterne.

> [!NOTE]  
> Du skal altid være mindst ét åbent regnskabsår. Når du lukker et år, skal du sikre dig, der er oprettet et nyt år. Bemærk også, at når du har afsluttet ét regnskabsår, er det ikke muligt at ændre startdatoen for det efterfølgende år.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Afslut år**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bogføre poster til et afsluttet regnskabsår

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** bliver markeret. Afkrydsningsfeltet vises ikke på siden som standard, men du kan tilføje det. Som det næste skal du afslutte resultatopgørelsens konti og overføre årets resultater til en konto i balancen. Gentag disse trin, hver gang du bogfører poster i et afsluttet regnskabsår.

## <a name="see-also"></a>Se også

[Afslutte regnskaberne](year-close-books.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Sådan arbejder du med kontoskemaer](bi-how-work-account-schedule.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]