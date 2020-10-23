---
title: Definere en metode for igangværende arbejde og overvåge sagsstatus | Microsoft Docs
description: Beskriver, hvordan du kan oprette en metode for igangværende arbejde og beregne igangværende arbejde for at estimere den økonomiske værdi af sager, der er igangværende.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, KPI, work in process, work in progress
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: e46b9a11ce3a60711cfa6d01298cfd1aac13d4d6
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3921383"
---
# <a name="monitor-job-progress-and-performance"></a>Overvåge jobstatus og -udførelse
Efterhånden som status for en sag ændrer sig, forbruges der materialer, ressourcer og andre udgifter, og disse skal bogføres i sagen. Igangværende arbejde er en funktion, som giver dig mulighed for at estimere den økonomiske værdi af sager i finansregnskabet under udførelsen af sagen. Du kan i mange tilfælde bogføre udgifterne for en sag, før sagen faktureres. Hvis der kun er bogført udgifter, vil din regnskabsopgørelse ikke være helt korrekt. Du kan finde flere oplysninger i [Forstå metoder for igangværende arbejde](projects-understanding-wip.md).

Du kan beregne VIA og bogføre værdien i finansregnskabet for at spore værdien i finansregnskabet.

Du kan beregne VIA baseret på følgende:

* Kostværdi
* Salgsværdi
* Realiserede omkostninger
* Færdiggørelsesgrad
* Afsluttet kontrakt

Hvis du vil have vist resultatet ved hjælp af en anden metode, kan du skifte metode og beregne VIA igen. Der er ingen grænser for antallet af gange, du kan beregne VIA. VIA beregnes kun, det bogføres ikke i finansregnskabet. Når du har beregnet VIA, kan du foretage en bogføring i finansregnskabet.

## <a name="to-create-a-job-wip-method"></a>Sådan oprettes en sagsmetode for igangværende arbejde
Du kan oprette en sagsmetode for igangværende arbejde, der afspejler behovet i organisationen. Når du har oprettet den, kan du angive den som standardsagsberegningsmetoden for igangværende arbejde, der skal bruges i organisationen.  

> [!NOTE]
> Når du har brugt en ny metode til at oprette poster for igangværende arbejde, kan du ikke slette metoden eller ændre den.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sags-VIA-metoder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Luk siden.   
4. Hvis du gøre denne nye metode til standard, skal vælge ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angive **Sagsopsætning** og derefter vælge det relaterede link.  
5. I feltet **Standard-VIA-metode** skal du vælge metoden fra listen.

## <a name="to-define-a-wip-method-for-a-job"></a>Sådan definere en metode for igangværende arbejde for en sag
Når du opretter en ny sag, skal du angive, hvilken metode for igangværende arbejde der gælder. I nogle tilfælde er den sagsmetode for igangværende arbejde, der er oprettet for dig, oprettet som standard.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sager**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**. Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).  
3. På siden **Sagskort** i feltet **Metode for igangværende arbejde** skal du vælge en metode for igangværende arbejde. Hvis der er defineret en standardmetode, kan du vælge en anden indstilling, hvis det er nødvendigt.  

## <a name="to-calculate-wip"></a>Sådan beregnes VIA
Du kan fastlægge det beløb for igangværende arbejde, der skal bogføres til balancekonti ved periodeafslutningsrapporteringen. Det gør du ved at udføre kørslen **Beregn VIA for sag**.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Beregn VIA for sag**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Beregn igangværende arbejde**.
3. På siden **Beregn VIA for sag** skal du udfylde felterne efter behov.
4. Vælg knappen **OK**.  

> [!NOTE]  
>   Kørslen beregner kun igangværende arbejde. Det bogføres ikke i finansmodulet. Hvis du vil bogføre, skal du udføre kørslen **Bogfør igangværende arbejde - finansafstemning**, når du har beregnet igangværende arbejde. Du kan finde flere oplysninger i følgende procedure.

## <a name="to-post-wip"></a>Sådan bogføres igangværende arbejde
Når du har beregnet igangværende arbejde, kan du bogføre det til balancekontiene for periodeafslutningsrapporteringen. Det gør du ved at udføre kørslen **Bogfør VIA for sag**.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogfør VIA - finansafstemning**, og vælg derefter det relaterede link.  
2. På siden **Bogfør VIA - finansafstemning** skal du udfylde felterne efter behov.  
3. Vælg knappen **OK**.

## <a name="to-view-job-usage-estimates-and-post-updates"></a>Sådan vises sagsforbrugsestimater og bogføringsopdateringer
Du kan få vist sagsforbruget op til færdiggørelsen af et projekt i ét trin. Hvis du vil gøre det, skal du bruge kørslen **Beregn resterende forbrug for sag** for alle sagerne op til og inklusive afslutningen af en sag.  

På denne måde kan du holde styr på og sammenligne dine oprindelige estimater med de faktiske resultater og foretage ændringer eller oprette nye poster efter behov. Du kan f.eks. have anslået, at en sag krævede 10 timer, og at den frem til nu har taget 15 timer. Du kan føje de ekstra fem timer til den eksisterende kladdelinje eller oprette en ny kladdelinje for at rapportere disse fem timer som overtid, hvilket er en anden arbejdstype. Den korrekte omkostning og pris beregnes, og du kan derefter bogføre den til kladden.  

> [!NOTE]  
>   Vareposter opretter vareposter til finans og reducerer antallet af varer på lager. Kørslen **Bogfør lagerregulering** overfører omkostningen fra lager til finans. Ressourceposter opretter ressourceposter til finans.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagskladder**, og vælg derefter det relaterede link.  
2. Vælg en relevant sagskladde, og vælg derefter handlingen **Beregn resterede forbrug**.  
3. På siden **Beregn resterende forbrug for sag** skal du angive dokumentnummeret og bogføringsdatoen, der skal indsættes i kladden, og derefter vælge knappen **OK**.  
4. Opdater kladden med eventuelle nødvendige ændringer.  
5. Vælg **Bogfør**.

## <a name="to-view-job-ledger-entries"></a>Sådan får du vist sagsposter
Alle sagsrelaterede poster er registreret i sagsjournaler med fortløbende nummerering, hvor der startes med 1. Fra sagsjournalen kan du få et overblik over alle sagsposter.    

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Sagsjournaler**, og vælg derefter det relaterede link.
2. Vælg en relevant journal, og vælg derefter handlingen **Sagsposter**.

På siden **Sagsposter** kan du gennemse de poster, der er tilknyttet en sag.  

## <a name="see-also"></a>Se også
[Administrere projekter](projects-manage-projects.md)
[Administrere lageromkostninger](finance-manage-inventory-costs.md)   
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
