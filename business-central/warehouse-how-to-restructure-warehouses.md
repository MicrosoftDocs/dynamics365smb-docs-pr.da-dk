---
title: Omstrukturere lagre
description: 'Få mere at vide om, hvordan du omstrukturerer lagerstedet med nye placeringskoder og nye placeringskarakteristika for at opnå eller opretholde en mere effektiv operation.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9813, 9814'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="restructure-warehouses"></a>Omstrukturere lagre
Det kan eventuelt blive nødvendigt at omstrukturere lagerstedet med nye placeringskoder og nye karakteristika for placeringer. Sådanne omstruktureringer foretages som regel sjældent, men der kan opstå situationer, hvor det er nødvendigt med en omklassificering for at opnå en mere effektiv forretningsgang. Eksempler:  

- Lageret går over til at bruge et ADCS-system (Automatic Data Capture System), hvor der skal benyttes nye placeringskoder, som kan registreres med håndholdt udstyr.  
- Der indføres et nyt hyldesystem på lagerstedet, som giver nye muligheder for opbevaring.  
- Virksomheden indfører et nyt varesortiment og flytter lageret til en ny mere velegnet lokation.  

Hvis lagerstedet er sat op til at benytte placeringer, men ikke styret læg-på-lager og pluk, skal du omstrukturere lagerstedet ved at oprette nye placeringer, som du vil benytte fremover.  

## <a name="to-restructure-a-basic-warehouse-that-uses-bins-only"></a>Sådan omstruktureres et grundlæggende lager, der kun bruger placeringer
1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  På oversigtspanelet **Lagersted** skal du angive feltet **Standardplacering** til **Sidst anv. placering**.  
3.  Flyt alt indhold fra de nuværende placeringer til de nye placeringer, du lige har oprettet.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vareomposteringskladde**, og vælg derefter det relaterede link.  
    2.  Vælg en kladdelinje, og vælg derefter handlingen **Hent placeringsindh**.  
    3.  I oversigtspanelet **Placeringsindhold** skal du angive filtre i felterne **Lokationskode**, **Placeringskode** og **Varenr.** for at angive det indhold, du vil flytte.  
    4.  Vælg knappen **OK** for at udfylde en kladdelinje.  
    5.  Vælg den placering, som varen skal flyttes til, i feltet **Ny placeringskode**.  
    6.  Gentag trin b til e for alt placeringsindhold, du vil flytte.  
    7.  Vælg handlingen **Bogfør**.  

Du har nu tømt de placeringer, hvor varerne plejede at være. Standardplaceringerne for varerne er nu ændret til de nye placeringer.  

## <a name="to-restructure-an-advanced-warehouse-that-uses-directed-put-away-and-pick"></a>Sådan omstruktureres et avanceret lager, hvor der bruges styret læg-på-lager og pluk

1.  Opret de nye placeringer, der skal benyttes fremover. Du kan finde flere oplysninger i [Oprette placeringer](warehouse-how-to-create-individual-bins.md).  
2.  Flyt alt indhold fra de nuværende placeringer til de nye placeringer, som du lige har oprettet.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lageromposteringskladde**, og vælg derefter det relaterede link.  
    2.  Opret en linje for hver af de nuværende placeringer, for hvilke der ikke er tale om egentlig flytning af varer, i **Lageromposteringskladde** med den gamle placeringskode, **Fra placeringskode**, og den nye placeringskode, **Til placeringskode**.  
    3.  Hvis der er bevægelser, der omfatter fysisk flytning af varer, skal du bruge **Bevægelseskladder** til at oprette bevægelsesinstruktioner i stedet for at bruge omposteringskladden. Du kan finde flere oplysninger i [Flytte varer i avancerede lageropsætninger](warehouse-how-to-move-items-in-advanced-warehousing.md).  

3.  Når gamle placeringer er tømt, skal du genklassificere dem som type **KK**-placeringer for at sikre, at de ikke er inkluderet i vareforløb.  

    1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
    2.  Marker linjen med placeringen, og vælg derefter handlingen **Placeringer**.  
    3.  På siden **Placeringer** i feltet **Placeringstypekode** skal du angive **KK** for hver af gamle placeringer, som du slettede indholdet af i trin 3 i den foregående fremgangsmåde.  

Du har nu fjernet placeringerne fra lagerstedet og omposteret dem som KK-placeringer. KK-placeringer har ingen af aktivitetsfelterne på siden **Placeringstyper** valgt og tages derfor ikke i betragtning af varestrømmen. Der er flere oplysninger i [Konfigurere placeringer](warehouse-how-to-set-up-bin-types.md).  

## <a name="to-delete-a-bin"></a>Sådan slettes en placering

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  Vælg den lokation, hvor der skal slettes placeringer. Vælg handlingen **Placeringer**.  
3.  Marker linjerne for de placeringer, du vil slette.  
4.  Vælg handlingen **Slet**.  

Hvis du klikker på knappen **Ja**, slettes placeringen og kan ikke længere bruges, men placeringskoden står stadig på alle lagerposterne.  

Hvis du vil omdøbe en placering, så alle de tildelte poster også omdøbes, bl.a. placeringsindhold, lageraktivitetslinjer, registrerede lageraktivitetslinjer, lagerkladdelinjer, lagermodtagelseslinjer, bogførte lagermodtagelseslinjer, lagerleverancelinjer, bogførte lagerleverancelinjer og lagerposter, kan du gøre det på siden **Placeringer**.  

## <a name="to-rename-a-bin-and-change-the-bin-code-in-all-records"></a>Sådan omdøbes en placering, og sådan ændres placeringskoden i alle poster

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lokationer**, og vælg derefter det relaterede link.  
2.  Vælg den lokation, hvor du vil omdøbe en placering eller ændre placeringskoden, og vælg derefter handlingen **Placeringer**.  
3.  Vælg den placering, du vil ændre, og angiv en nye placeringskode i feltet **Kode**.  
4.  Vælg knappen **Ja**.  

> [!NOTE]  
>  Hvis du vælger **Ja**, og der er mange poster knyttet til placeringen, hvis du f.eks. ikke har slettet lagerdokumenter i lang tid, kan det tage nogen tid inden ændringen er gennemført. Derfor, hvis du bruger denne metode, kan du overveje at køre batchjobbet **Slet registrerede lagerdokumenter**, før du starter omdøbningsprocessen. Bemærk, at de dokumenter, der slettes i kørslen, kun omfatter læg-på-lager-aktiviteter, pluk og bevægelser.  
>   
>  Hvis du omdøber en modtagelses- eller en leveranceplacering, omdøbes alle de bogførte modtagelser eller leverancer, der henviser til den pågældende placering.  

## <a name="see-also"></a>Se også
[Warehouse Management-oversigt](design-details-warehouse-management.md)
[Lager](inventory-manage-inventory.md)  
[Sådan konfigureres Warehouse Management](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
