---
title: Arbejde med regnskabsperioder og regnskabsår
description: 'Lær, hvordan du arbejder med regnskabsperioder, der kan definere, hvornår virksomheden rapporterer finansielle resultater.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.form: '100,'
ms.date: 08/05/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="work-with-accounting-periods-and-fiscal-years"></a>Arbejde med regnskabsperioder og regnskabsår

Regnskabsperioder, der kaldes også rapporteringsperioder, er tidsperioder, hvor en virksomhed eller organisation rapporterer finansielle resultater, f.eks. ved at generere deres resultatopgørelse eller balance. Typisk henviser regnskabsperioder til virksomhedens regnskabsår, der kan indeholde flere regnskabsperioder, f.eks. måneder eller kvartaler.

For mange virksomheder stemmer regnskabsåret ikke overens med kalenderåret, f.eks. når regnskabsåret slutter den 30. juni i stedet for den 31. december. For nyoprettede virksomheder kan regnskabsåret i realiteten være længere end 12 måneder.  

[!INCLUDE[prod_short](includes/prod_short.md)] kræver kun regnskabsperioder, hvis du vil lukke en resultatopgørelse eller udføre opgaver til komprimering af data.

Du kan f.eks. bruge regnskabsperioder i forbindelse med rapportering, når du gennemgår bogførte poster på siden **Saldo/Budget**, hvor du kan angive rapporteringsintervallet. En af de indstillinger, du kan angive, er at rapportere efter regnskabsperiode. Du kan også oprette en finansiel rapport, der sammenligner resultaterne for forskellige perioder.

## <a name="creating-a-new-fiscal-year"></a>Oprette et nyt regnskabsår

Du kan oprette flere regnskabsperioder ad gangen ved hjælp af **Opret regnskabsår** som batchjob eller manuelt.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Sådan oprettes flere regnskabsperioder ad gangen

Brug **Opret regnskabsår**-kørslen til at opdele et regnskabsår i perioder af samme varighed.  

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, angiv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Opret år**.
3. I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder.  
4. I feltet **Antal perioder** kan du angive det antal perioder, du vil opdele regnskabsåret i. Der kan være op til 365 perioder pr. år.  
5. I feltet **Periodelængde** skal du angive en varighed for hver periode. Varighed er f.eks. 1M for en måned, 1K for et kvartal og 1Å for et år.  
6. Vælg **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Sådan oprettes regnskabsperioder manuelt

Hvis regnskabsperioderne i regnskabsåret, der har forskellige varigheder som f.eks. 4-4-5-kalender, der anvendes i detail, kan du oprette det manuelt.  
  
1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, angiv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. I feltet **Startdato** kan du angive den dato, hvor regnskabsåret begynder. Feltet **Navn** viser navnet på måneden.  
3. Marker afkrydsningsfeltet **Nyt regnskabsår** for at angive, at dette er den første periode i året. [!INCLUDE[prod_short](includes/prod_short.md)] bruger denne periode til at bestemme, hvilke perioder der skal lukkes ved udgangen af året.
4. Gentag trin 2 og 3 for hver resterende periode.  

## <a name="closing-a-fiscal-year"></a>Afslutning af et regnskabsår

Lukning af regnskabsåret er en af opgaverne, når regnskaberne skal afsluttes. Når regnskabsåret er afsluttet, er felterne **Afsluttet** og **Dato låst** markeret for alle perioder i året. Du kan ikke genåbne et år eller fjerne markeringen i afkrydsningsfelterne.

> [!NOTE]  
> Du skal altid være mindst ét åbent regnskabsår. Når du lukker et år, skal du sikre dig, der er oprettet et nyt år. Bemærk også, at når du har afsluttet ét regnskabsår, er det ikke muligt at ændre startdatoen for det efterfølgende år.

1. Vælg ![Søg efter side eller rapport.](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport") ikon, skriv **Regnskabsperioder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Afslut år**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Bogføre poster til et afsluttet regnskabsår

Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det. Hvis du gør det, bliver posterne i forbindelse med bogføringen markeret som bogførte i et afsluttet regnskabsår, og afkrydsningsfeltet **Efterpost** bliver markeret. Afkrydsningsfeltet vises som standard ikke på siden, men du kan tilføje det. Som det næste skal du afslutte resultatopgørelsens konti og overføre årets resultater til en konto i balancen. Gentag disse trin, hver gang du bogfører poster i et afsluttet regnskabsår.

## <a name="see-also"></a>Se også

[Lukning af bøgerne](year-close-books.md)    
[Ultimoår og -perioder](year-close-years-periods.md)    
[Arbejde med finansielle rapporter](bi-how-work-account-schedule.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
