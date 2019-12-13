---
title: Sådan defineres arbejdscentre og produktionsressourcer | Microsoft Docs
description: Et **arbejdscenterkort** organiserer produktionsressources faste værdier og krav og styrer på den måde den produktionsafgang, der udføres på arbejdscentret.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 1d8b24df628cbb41449e37b31cbf1082d434bb81
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877827"
---
# <a name="set-up-work-centers-and-machine-centers"></a>Konfigurere arbejdscentre og produktionsressourcer
Programmet skelner mellem tre typer kapacitet. Disse er arrangeret hierarkisk. Hvert niveau indeholder underordnede niveauer.  

Det øverste niveau er arbejdscentergruppen. Arbejdscentre er knyttet til arbejdscentergrupper. Hvert arbejdscenter kan tilhøre en arbejdscentergruppe.

Du kan knytte forskellige produktionsressourcer til hvert arbejdscenter. En produktionsressource kan muligvis kun tilhøre et arbejdscenter.  

Den planlagte kapacitet for arbejdscentre består af disponeringen i de tilsvarende produktionsressourcer og den supplerende planlagte disponering i arbejdscentret. Den planlagte disponering i arbejdscentergruppen er derfor summen af alle tilsvarende produktionsressourcer og arbejdscentre.  

Tilgængeligheden er lagret i kalenderposter. Før du opretter arbejdscentre eller produktionsressourcer, skal du oprette produktionskalendere. Du kan finde flere oplysninger i [Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md).  

## <a name="to-set-up-a-work-center"></a>Sådan opsættes et arbejdscenter
Nedenstående beskrives primært, hvordan du opretter et arbejdscenter. Trinnene til at oprette en produktionsressourcekalender er identiske med undtagelse af oversigtspanelet **Ruteopsætning**.  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Arbejdscentre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4.  Markér den højniveau ressourcegruppe, som arbejdscenteret er organiseret under, i feltet **Ressourcegruppe**, hvis det er relevant. Vælg handlingen **Ny** på rullemenuen.  
5.  Vælg feltet **Spærret**, hvis du vil forhindre, at arbejdscentret bruges i enhver behandling. Det betyder, at der ikke kan bogføres afgang for en vare, der produceres på arbejdscentret. Du kan finde flere oplysninger i [Bogføre produktionsafgang](production-how-to-post-output-quantity.md).
6.  Skriv omkostningen ved at producere en enhed på dette arbejdscenter, inklusive alle andre kostelementer, i feltet **Købspris**. Denne omkostning kaldes ofte *direkte arbejdsomkostning”*.  
7.  I feltet **Indir. omkost.pct** skal du angive de generelle driftsomkostninger ved at bruge arbejdscentret som en procentdel af købsprisen. Dette procenttal lægges til købsprisen ved beregningen af kostprisen.  
8.  I feltet **IPO-bidrag** skal du angive alle ikke-driftsmæssige omkostninger for arbejdscentret, f.eks. reparationsudgifter, som et direkte beløb.  

    Feltet **Kostpris** indeholder den beregnede kostpris ved produktion af en enhed på arbejdscentret, inklusive alle kostelementer, som følger:  

    Kostpris = Købspris + (Købspris x Indir. omkost.pct) + IPO-bidrag.  

9.  Angiv i feltet **Kostprisberegning**, om ovenstående beregning skal baseres på den forbrugte tid: **Tid** eller på antallet af producerede enheder: **Enheder**.  
10.  Vælg feltet **Specifik kostpris**, hvis du vil definere arbejdscentrets kostpris på den rutelinje, hvor det benyttes. Dette kan være relevant for operationer, hvor kapacitetsomkostningerne er væsentligt anderledes end for andre produktioner på arbejdscentret.  
11.  Vælg i feltet **Trækmetode**, om outputbogføring på dette arbejdscenter skal beregnes og bogføres manuelt eller automatisk med en af følgende metoder.

|Indstilling|Beskrivelse|
|------|-----------|
|**Manuelt**|Forbrug bogføres manuelt i afgangskladden eller produktionskladden.|
|**Forlæns**|Forbrug beregnes og bogføres automatisk, når produktionsordren frigives.|
|**Baglæns**|Forbrug beregnes og bogføres automatisk, når produktionsordren afsluttes.|

> [!NOTE]
> Hvis det er nødvendigt, kan den trækmetode, der vælges her og på **Vare**-kortet, tilsidesættes for enkelte operationer ved at ændre indstillingen på rutelinjerne

12.  Brug feltet **Enhedskode** til at angive den tidsenhed, som arbejdscentrets kostprisberegning og kapacitetsplanlægning udføres i.
    For konstant at kunne overvåge forbrug skal du først oprette en enhedsmetode. De enheder, du angiver, er basisenheder. F.eks. beregnes procestiderne i timer og minutter.

> [!NOTE]  
> Hvis du vælger at bruge Dage, skal du huske, at 1 dag = 24 timer - og ikke 8 (arbejdstimer).

13.  I feltet **Kapacitet** skal du angive, om arbejdscentret har mere end én maskine eller person, der arbejder samtidigt. Hvis din [!INCLUDE[d365fin](includes/d365fin_md.md)]-installation ikke omfatter funktionaliteten Produktionsressource, skal værdien i dette felt være **1**.  
14.  Angiv den procentdel af den forventede standardafgang, som arbejdscentret normalt producerer, i feltet **Effektivitet**. Hvis du angiver **100**, betyder det, at arbejdscentret har en faktisk afgang, der er den samme som standardafgangen.  
15. Markér afkrydsningsfeltet **Fælles kalender**, hvis du også bruger produktionsressourcer. Dette sikrer, at kalenderposter er akkumuleres fra produktionsressourcekalendere.  
16.  Vælg en produktionskalender i feltet **Produktionskalenderkode**. Du kan finde flere oplysninger i [Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md).  
17.  I feltet **Køtid** skal du angive et fast tidsrum, der skal forløbe, før det tildelte arbejde kan begynde på arbejdscentret. Bemærk, at køtiden lægges til andre ikke-produktive tidselementer, f.eks. ventetid og transporttid, som du kan definere på rutelinjer, der benytter dette arbejdscenter.  

## <a name="example---different-machine-centers-assigned-to-a-work-center"></a>Eksempel - Du kan knytte forskellige produktionsressourcer til et arbejdscenter
Det er vigtigt at planlægge, hvilke kapaciteter der udgør den samlede kapacitet, når der angives produktionsressourcer og arbejdscentre.

Hvis forskellige produktionsressourcer, f.eks. 210 Pakkebord og 310 Malerkabine, knyttes til et arbejdscenter, er bedømmelsen af de enkelte kapaciteter i produktionsressourcerne vigtig, fordi fejl i en produktionsressource kan forstyrre hele processen. Produktionsressourcerne kan angives i overensstemmelse med deres kapacitet, men skal muligvis ikke medtages i planlægningen. Hvis feltet **Fælles kalender** deaktiveres, er det kun arbejdscentrets kapacitet, som knyttes til planlægningen, men ikke produktionsressourcerne.

Hvis identiske produktionsressourcer, f.eks. 210 Pakkebord 1 og 220 Pakkebord 2, kombineres i et arbejdscenter, kan arbejdscentret betragtes som summen af de tilknyttede produktionsressourcer. Derfor vises arbejdscentret med ingen kapacitet. Ved at aktivere feltet **Fælles kalender** knyttes den fælles kapacitet til arbejdscentret.

Hvis kapaciteter i arbejdscentre ikke skal bidrage til den samlede kapacitet, skal du angive effektivitet = 0.

## <a name="to-set-up-a-capacity-constrained-machine-or-work-center"></a>Hvis du vil oprette en produktionsressource eller et arbejdscenter med kapacitetsbegrænsning
Du skal oprette produktionsressourcer, som du betragter som kritiske, og udpege dem som i stand til at håndtere en begrænset belastning i stedet for den ubegrænsede belastning, som andre ressourcer kan håndtere. En kapacitetsbegrænset ressource kan f.eks. være et arbejdscenter eller en produktionsressource, der er identificeret som flaskehals, og som du derfor vil tildele en begrænset (endelig) belastning for.

[!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter ikke detaljeret produktionskontrol. Det planlægger en mulig udnyttelse af ressourcer ved at tilbyde en grov plan, men det opretter og vedligeholder ikke automatisk detaljerede planer, der er baseret på prioriteter eller optimeringsregler.

På siden **Kapacitetsbegrænsede ressourcer** kan du foretage en opsætning, der undgår overbelastning af bestemte ressourcer og sikrer, at ingen kapacitet er ikke-allokeret, hvis det kan forbedre gennemløbstiden for en produktionsordre. I feltet **Aktionsgrænse (% af den samlede kapacitet)** kan du tilføje aktionsgrænsetid for ressourcer for at begrænse tab på opdeling af operationer. Dette gør det muligt for systemet at planlægge belastning på den sidst mulige dag ved at overskride den kritiske belastningsprocent en smule, hvis dette kan reducere antallet af operationer, der er opdelt.

Ved planlægning med kapacitetsbegrænsede ressourcer sikrer systemet, at der ikke indlæses nogen ressource over dens definerede kapacitet (kritisk belastning). Dette gøres ved at tildele hver operation til det nærmeste tilgængelige tidsrum. Hvis tidsrummet ikke er stort nok til at fuldføre hele handlingen, bliver handlingen opdelt i to eller flere dele, der er placeret i de nærmeste ledige tidsrum.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kapacitetsbegrænsede ressourcer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov.

> [!NOTE]
> Operationer i arbejdscentre eller produktionsressourcer, der er opsat som begrænsede ressourcer planlægges altid serielt. Det betyder, at hvis en begrænset ressource har flere kapaciteter, kan disse kapaciteter kun planlægges i sekvenser, ikke parallelt, som det ville være tilfældet, hvis arbejds- eller produktionscenteret ikke var sat op som begrænset ressource. I en begrænset ressource vil feltet Kapacitet på arbejdscenteret eller produktionsressource være større end 1.

> I tilfælde af opdeling af operationen er opstillingstiden kun tildelt én gang, da det antages, at nogen manuel regulering er udført for at optimere planen.

## <a name="see-also"></a>Se også  
[Opsætte produktionskalendere](production-how-to-create-work-center-calendars.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
