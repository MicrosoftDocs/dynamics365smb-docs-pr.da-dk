---
title: "Sådan defineres arbejdscentre og produktionsressourcer | Microsoft Docs"
description: "Et **arbejdscenterkort** organiserer produktionsressources faste værdier og krav og styrer på den måde den produktionsafgang, der udføres på arbejdscentret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8a7af6821affcef2c81499e904f2ed9520086323
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-work-centers-and-machine-centers"></a>Fremgangsmåde: Konfigurere arbejdscentre og produktionsressourcer
Programmet skelner mellem tre typer kapacitet. Disse er arrangeret hierarkisk. Hvert niveau indeholder underordnede niveauer.  

Det øverste niveau er arbejdscentergruppen. Arbejdscentre er knyttet til arbejdscentergrupper. Hvert arbejdscenter kan tilhøre en arbejdscentergruppe.

Du kan knytte forskellige produktionsressourcer til hvert arbejdscenter. En produktionsressource kan muligvis kun tilhøre et arbejdscenter.  

Den planlagte kapacitet for arbejdscentre består af disponeringen i de tilsvarende produktionsressourcer og den supplerende planlagte disponering i arbejdscentret. Den planlagte disponering i arbejdscentergruppen er derfor summen af alle tilsvarende produktionsressourcer og arbejdscentre.  

Tilgængeligheden er lagret i kalenderposter. Før du opretter arbejdscentre eller produktionsressourcer, skal du oprette produktionskalendere. Du kan finde flere oplysninger i [Fremgangsmåde: Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Sådan opsættes et arbejdscenter
Nedenstående beskrives primært, hvordan du opretter et arbejdscenter. Trinnene til at oprette en produktionsressourcekalender er identiske med undtagelse af oversigtspanelet **Ruteopsætning**.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Arbejdsskift**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Markér den højniveau ressourcegruppe, som arbejdscenteret er organiseret under, i feltet **Ressourcegruppe**, hvis det er relevant. Vælg handlingen **Ny** på rullemenuen.  
5.  Vælg feltet **Spærret**, hvis du vil forhindre, at arbejdscentret bruges i enhver behandling. Det betyder, at der ikke kan bogføres afgang for en vare, der produceres på arbejdscentret. Du kan finde flere oplysninger i [Fremgangsmåde: Bogføre produktionsafgang](production-how-to-post-output-quantity.md).
6.  Skriv omkostningen ved at producere en enhed på dette arbejdscenter, inklusive alle andre kostelementer, i feltet **Købspris**. Denne omkostning kaldes ofte *direkte arbejdsomkostning”*.  
7.  I feltet **Indir. omkost.pct** skal du angive de generelle driftsomkostninger ved at bruge arbejdscentret som en procentdel af købsprisen. Dette procenttal lægges til købsprisen ved beregningen af kostprisen.  
8.  I feltet **IPO-bidrag** skal du angive alle ikke-driftsmæssige omkostninger for arbejdscentret, f.eks. reparationsudgifter, som et direkte beløb.  

    Feltet **Kostpris** indeholder den beregnede kostpris ved produktion af en enhed på arbejdscentret, inklusive alle kostelementer, som følger:  

    Kostpris = Købspris + (Købspris x Indir. omkost.pct) + IPO-bidrag.  

9.  Angiv i feltet **Kostprisberegning**, om ovenstående beregning skal baseres på den forbrugte tid: **Tid** eller på antallet af producerede enheder: **Enheder**.  
10.  Vælg feltet **Specifik kostpris**, hvis du vil definere arbejdscentrets kostpris på den rutelinje, hvor det benyttes. Dette kan være relevant for operationer, hvor kapacitetsomkostningerne er væsentligt anderledes end for andre produktioner på arbejdscentret.  
11.  Vælg i feltet **Trækmetode**, om outputbogføring på dette arbejdscenter skal beregnes og bogføres manuelt eller automatisk med en af følgende metoder.  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Manuelt**|Forbrug bogføres manuelt i afgangskladden eller produktionskladden.|
    |**Forlæns**|Forbrug beregnes og bogføres automatisk, når produktionsordren frigives.|  
    |**Baglæns**|Forbrug beregnes og bogføres automatisk, når produktionsordren afsluttes.|  

    > [!NOTE]  
    >  Hvis det er nødvendigt, kan den trækmetode, der vælges her og på **Vare**-kortet, tilsidesættes for enkelte operationer ved at ændre indstillingen på rutelinjerne.

12.  Brug feltet **Enhedskode** til at angive den tidsenhed, som arbejdscentrets kostprisberegning og kapacitetsplanlægning udføres i.
    For konstant at kunne overvåge forbrug skal du først oprette en enhedsmetode. De enheder, du angiver, er basisenheder. F.eks. beregnes procestiderne i timer og minutter.

    > [!NOTE]  
    > Hvis du vælger at bruge Dage, skal du huske, at 1 dag = 24 timer - og ikke 8 (arbejdstimer).

13.  I feltet **Kapacitet** skal du angive, om arbejdscentret har mere end én maskine eller person, der arbejder samtidigt. Hvis din installation af **Produktnavn** ikke omfatter funktionaliteten Prod.ress., skal værdien i dette felt være **1**.  
14.  Angiv den procentdel af den forventede standardafgang, som arbejdscentret normalt producerer, i feltet **Effektivitet**. Hvis du angiver **100**, betyder det, at arbejdscentret har en faktisk afgang, der er den samme som standardafgangen.  
15. Markér afkrydsningsfeltet **Fælles kalender**, hvis du også bruger produktionsressourcer. Dette sikrer, at kalenderposter er akkumuleres fra produktionsressourcekalendere.  
16.  Vælg en produktionskalender i feltet **Produktionskalenderkode**. Du kan finde flere oplysninger i [Fremgangsmåde: Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md).  
17.  I feltet **Køtid** skal du angive et fast tidsrum, der skal forløbe, før det tildelte arbejde kan begynde på arbejdscentret. Bemærk, at køtiden lægges til andre ikke-produktive tidselementer, f.eks. ventetid og transporttid, som du kan definere på rutelinjer, der benytter dette arbejdscenter.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Eksempel - Du kan knytte forskellige produktionsressourcer til et arbejdscenter
Det er vigtigt at planlægge, hvilke kapaciteter der udgør den samlede kapacitet, når der angives produktionsressourcer og arbejdscentre.

Hvis forskellige produktionsressourcer, f.eks. 210 Pakkebord og 310 Malerkabine, knyttes til et arbejdscenter, er bedømmelsen af de enkelte kapaciteter i produktionsressourcerne vigtig, fordi fejl i en produktionsressource kan forstyrre hele processen. Produktionsressourcerne kan angives i overensstemmelse med deres kapacitet, men skal muligvis ikke medtages i planlægningen. Hvis feltet **Fælles kalender** deaktiveres, er det kun arbejdscentrets kapacitet, som knyttes til planlægningen, men ikke produktionsressourcerne.

Hvis identiske produktionsressourcer, f.eks. 210 Pakkebord 1 og 220 Pakkebord 2, kombineres i et arbejdscenter, kan arbejdscentret betragtes som summen af de tilknyttede produktionsressourcer. Derfor vises arbejdscentret med ingen kapacitet. Ved at aktivere feltet **Fælles kalender** knyttes den fælles kapacitet til arbejdscentret.

Hvis kapaciteter i arbejdscentre ikke skal bidrage til den samlede kapacitet, skal du angive effektivitet = 0.

## <a name="see-also"></a>Se også  
[Fremgangsmåde: Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

