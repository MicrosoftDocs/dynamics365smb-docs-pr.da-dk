---
title: Gennemgang - Manuel planlægning af forsyninger
description: 'Denne gennemgang viser, hvordan du planlægger forsyningsordrer for at opfylde nyt behov, herunder planlægning af en købs-, overflytnings-og produktionsordre.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-planning-supplies-manually"></a><a name="walkthrough-planning-supplies-manually"></a><a name="walkthrough-planning-supplies-manually"></a>Gennemgang: Manuel planlægning af forsyninger

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Denne gennemgang viser processen med at planlægge forsyningsordrer til opfyldning af nye behov. Du kan starte forsyningsplanlægningen med faste intervaller, f.eks. hver morgen eller hver mandag, eller når du får besked om det af salg eller produktion, afhængigt af behovstypen. I denne gennemgang kommer du til at bruge siden **Ordreplanlægning**, der er et simpelt forsyningsplanlægningsværktøj, der er baseret på manuel beslutningstagning i stedet for en parameterbaseret automatisk planlægning.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Om denne gennemgang
 Denne gennemgang illustrerer følgende opgaver:  

-   Planlægning af en købsordre for produktionskomponenter.  
-   Planlægning af en overflytningsordre til opfyldning af et salgsbehov.  
-   Planlægning af en produktionsordre for en vare med flere niveauer.  

## <a name="roles"></a><a name="roles"></a><a name="roles"></a>Roller
 Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Produktionsplanlægger  
-   Indkøbsagent  
-   Salgsordrebehandler  

## <a name="prerequisites"></a><a name="prerequisites"></a><a name="prerequisites"></a>Forudsætninger
 Inden du begynder denne gennemgang, skal du installere [!INCLUDE[prod_short](includes/prod_short.md)]. Der skal foretages følgende ændringer i databasen:  

-   Slet alle eksisterende salgsordrer på cykler.  
-   Opret én salgsordre på ti cykler på lokationen EAST.  
-   Slet alle planlagte og fastlagte produktionsordrer. Slet ikke startede ordrer med poster, der allerede er bogførte.  

 Du skal som hovedregel bruge de foreslåede data i denne gennemgang, da disse data indeholder de nødvendige poster.  

## <a name="story"></a><a name="story"></a><a name="story"></a>Historie
 Erik, der er produktionsplanlægger i en mindre produktionsvirksomhed, er ved at planlægge produktions og købsordrer til opfyldning af nye salgsbehov.  

 Da der er få styklisteniveauer i produkterne, og ordrestrømmen er relativ beskeden, anvender Erik siden **Ordreplanlægning** til manuelt at oprette forsyningsordrer – ét produktniveau ad gangen.  

 Ved mere komplekse produktionsmiljøer, bruges planlægningskladden til at planlægge forsyningen baseret på vareparametre, som f.eks. ændringsperiode, sikkerhedstid, genbestillingspunkt og batchberegninger af den samlede efterspørgsel fra alle produktniveauer.  

## <a name="setting-up-the-sample-data"></a><a name="setting-up-the-sample-data"></a><a name="setting-up-the-sample-data"></a>Oprette eksempeldata
 Standarddemoregnskabet CRONUS har p.t. en stor mængde ikke-planlagte behov. Under de forskellige planlægningsopgaver i denne gennemgang vil du få brug for at afvige fra den realistiske forretningsgang ved at ignorere behov med tætte forfaldsdatoer og i stedet bruge behov med senere forfaldsdatoer.  

## <a name="use-the-order-planning-page"></a><a name="use-the-order-planning-page"></a><a name="use-the-order-planning-page"></a>Bruge siden Ordreplanlægning

Du kan få adgang til siden **Ordreplanlægning** fra flere forskellige lokationer:  

-   Produktion, Planlægning  
-   Salg & Marketing, Ordrebehandling  
-   Køb, Planlægning  
-   Derudover kan du åbne siden for en bestemt produktionsordre ved at vælge handlingen **Planlægning**.

### <a name="to-use-the-order-planning-page"></a><a name="to-use-the-order-planning-page"></a><a name="to-use-the-order-planning-page"></a>Sådan bruges siden Ordreplanlægning

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreplanlægning**, og vælg derefter det relaterede link.  

     Når siden **Ordreplanlægning** først åbnes, skal der beregnes en plan for at få vist det nye behov, siden det sidst blev beregnet.  

2.  Vælg handlingen **Beregn plan**.  

     Planlægningssystemet analyserer et eventuelt nyt behov, der er kommet til, som f.eks. nye salg, ændrede salg eller produktionsordrer.  

     Det nødvendige antal for hvert behovslinje beregnes baseret på den samlede tilgængelighed. Denne beregning udføres ordre-for-ordre. Dette betyder, at den ordre, der indeholder behovslinjen med den tidligste forfaldsdato eller afsendelsesdato, beregnes først. Derefter vil de andre behovslinjer blive beregnet i samme ordre, uanset forfaldsdato eller afsendelsesdato.  

3.  Sørg for, at siden **Ordreplanlægning** er maksimeret, og at kolonnefelterne er tilpasset, så de viser alle standardfeltnavnene.  

     Når beregningen er færdig, viser siden alle ikke-opfyldte behov som ikke-udvidede ordrehovedlinjer sorteret efter tidligste behovsdato.  

     Bemærk, at CRONUS har flere ordrer med ikke-opfyldte behov. Hver planlægningslinje, der står med fed skrift, repræsenterer en ordre, salgsordre eller produktionsordre, inklusive mindst én ordrelinje med utilstrækkelig disponering.  

4.  Gå til feltet **Vis behov som**, og vælg filteret **Alle behov**.  

     I feltet **Behovstype** kan du vælge, hvilke ordretyper der skal vises.  

     Ordrer, der ikke har disponeringsproblemer, vises ikke. Hvis der ikke findes nogle ordrer, når en plan beregnes, vil der blive vist en meddelelse, og der vil ikke blive vist nogen planlægningslinjer.  

## <a name="planning-a-purchase-order-to-fulfill-component-demand"></a><a name="planning-a-purchase-order-to-fulfill-component-demand"></a><a name="planning-a-purchase-order-to-fulfill-component-demand"></a>Planlægge en købsordre for at opfylde et komponentbehov
 I denne procedure opretter du en købsordre til manglende produktionskomponenter.  

### <a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a><a name="to-plan-a-purchase-order-to-fulfill-component-need-in-production"></a>Sådan planlægges en købsordre for at opfylde et komponentbehov i produktionen

1.  Udvid den første linje (vælg symbolet +).  
2.  Vælg den første behovslinje med varen **LSU-15**, og vælg derefter handlingen **Vis dokument**.  
3.  Luk den åbnede produktionsordre for at vende tilbage til siden **Ordreplanlægning**.  
4.  Gå til feltet **Genbestillingssystem**, og vælg **Køb**.  

     Standardværdien er fra vare- eller lagerkortet, men du kan ændre det til et af følgende muligheder:  

    -   **Køb** – for at oprette en købsordre.  
    -   **Overførsel** – for at oprette en overflytningsordre.  
    -   **Produktionsordre** – for at oprette en produktionsordre.  

5.  Vælg en af følgende indstillinger, der svarer til det valgte genbestillingssystem i feltet **Forsyning fra**:  

    -   **Kreditor** – For køb  
    -   **Lokation** – til overførsler  

     Hvis feltet ikke er udfyldt, vises der en fejlmeddelelse, når du prøver at oprette forsyningsordren.  

    > [!NOTE]  
    >  Hvis der er oprettet et standardleverandørnummer på varekortene for komponenterne, vil linjerne være forudindstillet.  

6.  Markér feltet **Forsyning fra**.  
7.  På siden **Vare/leverandører** skal du vælge handlingen **Ny** og derefter vælge leverandør **30000**.  
8.  Vælg knappen **OK** for at gå tilbage til siden **Ordreplanlægning**.  
9. Kopier leverandør **30000** for til andre linjer for højttalerkomponenterne på denne produktionsordre.  

     Du er nu klar til at oprette en købsordre.  

10. Vælg handlingen **Lav ordrer**. Siden **Opret forsyningsordrer** åbnes.  
11. På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Aktiv ordre**.  
12. Gå til oversigtspanelet **indstillinger** og feltet **Opret købsordre**, og vælg indstillingen **Opret købsordrer**.  
13. Vælg **OK**-knappen for at oprette købsordrer for alle komponenterne i ordren.  

     Købsordrerne er nu oprettet og gemt som de sidste ordrer på listen over købsordrer.  

## <a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><a name="planning-a-transfer-order-to-fulfill-sales-demand"></a><a name="planning-a-transfer-order-to-fulfill-sales-demand"></a>Planlægge en overflytningsordre for at opfylde et salgsbehov
 I denne procedure kommer du til at planlægge ud fra et behov fra en salgsordre. Behovslinjerne repræsenterer salgslinjer og ikke komponentlinjer som ved produktionsbehov.  

### <a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a><a name="to-plan-a-transfer-order-to-fulfill-sales-demand"></a>Sådan planlægges en overflytningsordre til opfyldning af et salgsbehov.

1.  Flyt markøren til planlægningslinjen for ordre **2008**.  
2.  Udvid linjen, og flyt markøren til behovslinjen.  

     Salgsordre **2008** er på ti højttalere, vare **LS-120**, der er bestilt af Lauritzen Kontormøbler A/S.  

     Varens definerede genbestillingssystem og standardleverandør vises.  

    > [!NOTE]  
    >  Nederst på siden er der fire oplysningsfelter. I feltet **Tidligste disponible dato** vil de ti stykker, der er behov for, være til disposition på en indgående forsyningsordre ni dage senere end den aktuelle forfaldsdato. Hvis dette er for sent for kunden, viser feltet **Disponibel til overflytning** 13 stykker af varen på en anden lokation. Du vil skulle planlægge denne lagerbeholdning.  

3.  Vælg feltet **Disponibel til overflytning** for at åbne siden **Hent alternativ forsyning**.  
4.  Vælg **OK**-knappen for at registrere de ti varer, der er til disposition.  

    > [!NOTE]  
    >  Det foreslåede køb i behovslinjen er erstattet med en overførsel fra lokationen MAIN. Funktionen **Lav ordrer** opretter en overflytningsordre fra MAIN til den påkrævede lokation. Feltet **Erstatning findes** fungerer på samme måde.  

5.  Vælg handlingen **Lav ordrer**. Siden **Opret forsyningsordrer** åbnes.  
6.  På oversigtspanelet **Ordreplanlægning**, i feltet **Lav ordrer for**, skal du vælge muligheden **Den aktive ordre**.  
7.  Gå til oversigtspanelet **indstillinger** og feltet **Opret overflytningsordre**, og vælg indstillingen **Opret overførselsordrer**.  
8.  Vælg knappen **OK** for at oprette overførselsordren til forsyning af salgsordren.  

     Overførselsordren er nu oprettet og gemt som den sidste ordre på listen over åbne overførselsordrer.  

## <a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a><a name="planning-a-multilevel-production-order-to-fulfill-sales-demand"></a>Planlægge en Produktionsordre med flere niveauer for at opfylde et salgsbehov
 I denne procedure kommer du til at planlægge en opfyldning af et salgsbehov for en produceret vare med flere produktniveauer, der hver opretter afhængige produktionsbehov.  

### <a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a><a name="to-plan-multilevel-production-to-fulfill-sales-demand"></a>Sådan planlægges en produktion med flere niveauer for at opfylde et salgsbehov

1.  Vælg planlægningslinjen med salgsbehovet for ordre **1001**, oprettet tidligere som forudsætningsdata.  

     Behovet er en salgslinje, men varen har et defineret genbestillingssystem for **Prod.ordre**. Fortsæt med at tilføje en ekstra ringeklokke til komponentbehovet for hver cykel.  

2.  Vælg handlingen **Komponenter** for at åbne siden **Planlægning - komponenter**.  
3.  På linjen for Ringeklokke skal du ændre feltet **Antal pr.** fra **1** til **2**.  
4.  Overvej dine planlægningsalternativer på siden **Ordreplanlægning**. I dette tilfælde har du ingen alternative forsyningsmuligheder, ingen overførsel, erstatning eller senere levering. Du skal oprette den foreslåede forsyningsordre, en produktionsordre.  
5.  Vælg handlingen knappen **Lav ordrer** for at oprette produktionsordren.  

     På siden **Ordreplanlægning** kan du se, at planlægningslinjen for salgsordre **1001** ikke længere findes, og at det første salgsbehov er dækket.  

6.  Luk siden **Ordreplanlægning**.  

     Nu kunne du vælge at blive i denne visning og færdiggøre planlægningsopgaverne. I stedet vil du dog nu antage rollen som produktionsplanlægger ved at gå til den produktionsordre, som du lige har oprettet, og åbne siden **Ordreplanlægning**.  

 Som produktionsplanlægger skal du planlægge en specifik produktionsordre.  

### <a name="to-plan-a-specific-production-order"></a><a name="to-plan-a-specific-production-order"></a><a name="to-plan-a-specific-production-order"></a>Sådan planlægges en specifik produktionsordre

1.  Åbn produktionsordren **101001**, på ti cykler, som du oprettede ved at bruge funktionen **Lav ordrer**.  
2.  Åbn siden **Prod.ordrekomponenter** for at kontrollere, at de ekstra ringeklokker afspejles på produktionsordren.  
3.  Vælg handlingen **Planlægning**.  

     Siden **Ordreplanlægning** åbnes i en visning, der altid er filtreret ud fra det specifikke produktionsbehov. Salgsbehovet vises ikke. Du skal beregne en plan, før du kan se et eventuelt ekstra behov.  

4.  Vælg handlingen **Beregn plan**.  

     Bemærk, at de nye produktionsordrer vises som ikke-planlagt produktionsbehov, der er afledt af ordren **101001**. De nye linjer repræsenterer et nyt produktionsbehov fra de underordnede samlinger, der skal oprettes for at producere ordren.  

5.  Vælg handlingen **Udvid alle** for at få vist en oversigt over alle produktionsbehov for produktionsordrerne.  

     Hvis du vil angive yderligere oplysninger om behovslinjerne, kan du tilføjefelterne **Behovsmængde** og **Tilgængelig behovsmængde** til visningen.  

     Nu skal du levere ti af hver komponent.  

     Bemærk, at fire af behovslinjerne har angivet genbestillingssystemet Prod.ordre. Disse fire halvfabrikata repræsenterer det andet produktniveau af cyklen.  

     Standardindstillingerne for genbestilling er allerede udfyldt, og du kan fortsætte til at lave ordrer.  

6.  Vælg handlingen **Lav ordrer**.  

     Før du klikker på **OK**, skal du bemærke teksten i oversigtspanelet **Ordreplanlægning**. Denne tekst er vigtig, fordi du ved, at cyklen har adskillige producerede komponenter, halvfabrikata, i produktstrukturen, som der kan være behov for, når du opretter denne produktionsordre.  

7.  Vælg indstillingen **Alle linjer**, og derefter knappen **OK** i feltet **Lav ordrer for** på siden **Opret forsyningsordre for** for at oprette produktionsordrer for det andet ordreproduktniveau.  

     Bemærk, at det øverste niveau i produktionsbehovet for produktionsordre 101001 ikke længere findes. Dette betyder, at der er foretage planlægning for det første produktionsbehov for de underordnede samlinger.  

     På siden **Ordreplanlægning** beregner du igen en plan for at planlægge cykelstrukturen.  

8.  Vælg handlingen **Beregn plan** for at genberegne planen som angivet i den integrerede hjælpetekst.  

     De to nye linjer repræsenterer et yderligere produktionsbehov fra de underordnede samlinger, der er planlagt i de forrige trin. Det foreslås, at du opretter to produktionsordrer til forsyning af hjulnav, én til 10 nav fortil og én til 10 nav bagtil.  

9. Vælg handlingen **Udvid alle** for at få vist en oversigt over alle behov for de to produktionsordrer.  

     Den foreslåede forsyningsplan indikerer, at der i alt oprettes fire købsordrer for komponenterne. Du beslutter dig for at lave de foreslåede ordrer.  

10. Vælg handlingen **Lav ordrer**.  
11. Vælg indstillinger **Alle linjer** og derefter knappen **OK** i feltet **Lav ordrer for**. Kontroller, om der stadig findes et behov for produktionen af den overordnede vare, cyklen, der sælges på salgsordren 1001.  
12. Vælg handlingen **Beregn plan**.  

     Meddelelsen angiver, at alle påkrævede varer nu er leveret. Kontrollér de fastlagte produktionsordrer, der er oprettet.  

13. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagt produktionsordrer**, og vælg derefter det relaterede link.  

     Se, hvordan start- og sluttiderne for de enkelte ordrer er planlagt i overensstemmelse med produktstrukturen på siden **Fastlagte prod.ordrer**. Komponenterne til de laveste niveauer i strukturen produceres først. Derfor skal du planlægge ordrer med flere niveauer som vist i denne planlægningsprocedure.  

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også
 [Gennemgang af forretningsproces](walkthrough-business-process-walkthroughs.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
