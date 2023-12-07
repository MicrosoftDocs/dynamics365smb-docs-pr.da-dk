---
title: Sådan konfigureres brugerdefinerede afskrivningsmetoder
description: I Business central kan du anvende en brugerdefineret afskrivningsmetode til at definere afskrivningsmetoden for aktivet på anlægskortsiden.
author: jill-kotel-andersson
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: user-depreciation
ms.date: 07/05/2021
ms.author: bholtorf
---

# Oprette anlægsaktiver med brugerdefinerede afskrivningsmetoder

Du kan bruge [!INCLUDE[prod_short](includes/prod_short.md)] til at definere de brugerdefinerede afskrivningsmetoder, som beskrevet her.

For hver brugerdefineret metode skal du bruge siden **Afskrivningstabeller**, hvor du skal angive en afskrivningsprocent for hver periode (måned, kvartal, år eller regnskabsperiode). Når du derefter tildeler en afskrivningsprofil med en brugerdefineret metode til et anlægsaktiv, skal du angive feltet **Første brugerdefinerede dato** og **Afskriv fra den relevante anlægsdato** på siden **Anlægsafskrivningsprofiler**.  

Formlen for beregning af afskrivningsbeløbet er:  

*Afskrivningsbeløb = (Afskrivningsprocent x Antal afskrivningsdage x Afskrivningsgrundlag) / (100 x 360)*


> [!NOTE]  
> Mens datoen i feltet **Første brugerdef. dato**bruges til at bestemme tidsintervallerne er det den **startdato for afskrivningen**, der bruges til at bestemme antallet af afskrivningsdage. Hvis **Første brugerdef. afskr.dato** ligger tidligere end datoen i feltet **Afskriv fra den**, vil procenten i den første periode i afskrivningstabellen kun blive delvist brugt i forbindelse med den automatiske beregning af første afskrivning. Det betyder, at anlægget ikke er helt afskrevet ved slutningen af den sidste periode.

## Sådan knyttes en afskrivningsprofil til et anlægsaktiv med en brugerdefineret afskrivningsmetode

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, som du vil konfigurere en anlægsafskrivningsprofil for.
3. Vælg den **relaterede** handling, og vælg derefter **anlægsaktiver** og derefter **Afskrivningsprofiler**. Derved åbnes siden **Anlægsafskrivningsprofiler**.

   Som standard er nogle af de felter, der skal udfyldes, på basis af nedenstående instruktioner skjult, så de skal vises. Hvis du vil gøre dette, skal du tilpasse siden. Du kan finde flere oplysninger i [Start af tilpasning af en side gennem det personlige banner](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).
4. Du skal vælge **Brugerdefineret** i feltet **Afskrivningsmetode**.
5. Vælg den **afskrivningstabel**, du vil bruge, i feltet **Afskrivningstabelkode**.
6. Vælg startdatoen for afskrivningsberegningen i feltet **Afskriv fra den**.
7. Når du bruger en brugerdefineret metode, angives feltet **Første brugerdef. dato** skal være angivet til en dato, der er identisk med eller tidligere end feltet **Afskriv fra den**. Hvis du har valgt en værdi i feltet **Periodelængde** i afskrivningstabellen, skal datoen i feltet **Første brugerdef. afskr.dato** være startdatoen i en regnskabsperiode.
8. Udfyld feltet **Antal afskrivningsår** eller feltets **Afskriv til den**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 

## Sådan konfigureres brugerdefinerede afskrivningsmetoder

På siden **Afskrivningstabel** kan du oprette brugerdefinerede afskrivningsmetoder. For eksempel kan du konfigurere afskrivning baseret på antal enheder.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Afskrivningstabeller**, og vælg derefter det relaterede link.  
2. På siden **Afskrivningstabeloversigt** skal du vælge handlingen **Ny**.  
3. På siden **Afskrivningstabelkort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

> [!TIP]
> Brug **Tabelfunktionen Opret sum af cifre** til at definere en afskrivningstabel baseret på metode *Sum af cifre*.

Med metoden *Sum af cifre* afskrives et anlæg over fire år, og afskrivningen beregnes for hvert år på følgende måde:

Sum af cifre = 1 + 2 + 3 + 4 = 10 Afskrivning:

* År 1 = 4/10  
* År 2 = 3/10  
* År 3 = 2/10  
* År 4 = 1/10  

### Afskrivning baseret på antal enheder

Denne brugerdefinerede metode kan også bruges til afskrivning baseret på antal enheder, f.eks. i forbindelse med produktionsmaskiner med fastlagt levetidskapacitet. På siden **Afskrivningstabeller** kan du angive antallet af enheder, der kan produceres i hver enkelt periode (måned, kvartal, år eller regnskabsperiode).  

### Eksempel - Brugerdefineret afskrivning

Du bruger en afskrivningsmetode, der gør det muligt at afskrive aktiver hurtigere af skattemæssige årsager.  

Til et anlægsaktiv med en levetid på tre år ville du af skattemæssige årsager anvende følgende afskrivningssatser:  

* År 1: 25 %  
* År 2: 38 %  
* År 3: 37 %  

Anskaffelsesprisen er RV 100.000, og afskrivningslevetiden er fem år. Afskrivningen beregnes en gang om året.  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelse |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 31-12-20 |Afskrivninger |360 |-25.000,00 |75,000.00 |
| 31-12-21 |Afskrivninger |360 |-38.000,00 |37,000.00 |
| 31-12-22 |Afskrivninger |360 |-37.000,00 |0 |
| 31-12-23 |Afskrivninger |Ingen |Ingen |0 |
| 31-12-24 |Afskrivninger |Ingen |Ingen |0 |

I det foregående eksempel er begge felter **Første brugerdef. dato** og **Afskriv. startdato** indstilles til 01/01/20 på siden **Anlægsafskrivningsprofiler** for det specifikke anlægsaktiv. Hvis feltet **Første brugerdef. afskr.dato** imidlertid indeholdte 01/01/20, og feltet **Afskriv fra den** indeholdte 04/01/20, ville resultatet være:  

| Dato | Anlægsbogføringstype | Dage | Beløb | Bogført værdi |
| --- | --- | --- | --- | --- |
| 01-01-20 |Anskaffelse |(Afskrivningens startdato) |100,000.00 |100,000.00 |
| 31-12-20 |Afskrivninger |270 |-18.750,00 |81,250.00 |
| 31-12-21 |Afskrivninger |360 |-38.000,00 |42,250.00 |
| 31-12-22 |Afskrivninger |360 |-37.000,00 |6,250.00 |
| 31-12-23 |Afskrivninger |90 |-6.250,00 |0 |
| 31-12-24 |Afskrivninger |Ingen |Ingen |0 |


## Se også
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Opsætte afskrivning af anlægsaktiv](fa-how-setup-depreciation.md)  
[Metoder til afskrivning af anlægsaktiver](fa-depreciation-methods.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
