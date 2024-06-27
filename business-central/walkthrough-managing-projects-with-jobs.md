---
title: Gennemgang – Administrere projekter med projekter
description: 'Denne gennemgang introducerer funktionerne til projektstyring, som giver dig mulighed for at planlægge brugen af virksomhedens ressourcer.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 05/30/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Gennemgang: administration af projekter

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Denne gennemgang giver dig en introduktion til projektstyringsfunktioner. Du kan bruge modulet Projekter til at planlægge brugen af virksomhedens ressourcer og holde styr på de forskellige omkostninger, der er forbundet med ressourcerne på et bestemt projekt. Projekter involverer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, du måske vil spore, efterhånden som et projekt skrider frem.  

Denne gennemgang beskriver opsætningen af et nyt projekt og relaterede opgaver:

- Håndting af faste priser
- Foretage betalinger af afdrag
- Bogføre fakturaer fra projekter
- Kopiere projekter

## Om denne gennemgang

 Denne gennemgang viser følgende opgaver:  

### Opsætte et projekt

Med den budgetstruktur, der er oprettet for projekter, er oprettelse af et projekt ligetil. Denne gennemgang omfatter følgende procedurer:  

- Opsætte projektopgavelinjer og planlægningslinjer.  
- Oprette projektspecifikke priser på varer, ressourcer og finanskonti.  
- Fakturere kunder for et projekt  

### Håndtere faste priser

 Du kan håndtere faste priser og priser på tjenester eller varer, der er aftalt med kunder i forvejen. I denne gennemgang lærer du, hvordan du kan:  

- Se, hvordan leverandør- og fakturaværdier bestemmes.  
- Gøre plads til ekstraarbejde i planen, der ikke er faktureret.  

### Kopiere et projekt

 Denne gennemgang fokuserer på, hvordan du kan kopiere en del af eller et komplet projekt for at reducere behovet for manuel indtastning af data og forbedre nøjagtigheden.

- Kopiere en del af et projekt til et nyt projekt.  
- Kopiere projektspecifikke priser.  
- Kopiere planlægningslinjer  

### Betaling af afdrag

 Når et stort, dyrt projekt varer længere tid, laver kunden ofte en aftale med virksomheden om at betale afdrag. Dette scenarie viser, hvordan du opretter betaling af afdrag håndteres og dækker følgende:  

- Oprette betaling af afdrag for et projekt.  
- Fakturere betalinger til kunder.  
- Gøre rede for forbrug i et projekt konfigureret til betaling af afdrag.  

## Roller

 Denne gennemgang indeholder opgaver for følgende roller:  

- Projektleder  
- Projektteammedlem  

## Forudsætninger

 Før du kan udføre opgaverne i denne gennemgang, skal du:  

- Installer CRONUS-demonstrationsdatabasen.
- Opret eksempeldata ved at bruge trinnene i følgende afsnit.  

## Historie

Denne gennemgang fokuserer på CRONUS, som er et fiktivt design- og konsulentfirma, der designer og tilpasser nye infrastrukturer. For eksempel konferencerum og kontorer med møbler, tilbehør og lagerenheder. Det meste af firmaets arbejde er projektorienteret. Prakash, en projektleder hos CRONUS, bruger projekter til at få et overblik over igangværende projekter, som CRONUS har startet og afsluttet. Det er som regel Prakash, der indgår aftaler med kunderne og indtaster projektets hovedkomponenter, hvilket er opgave- og planlægningslinjer i [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash konstaterer, at oprettelse, vedligeholdelse og gennemgang af oplysninger er ligetil. Prakash kan også lide, den måde [!INCLUDE[prod_short](includes/prod_short.md)] aktiverer kopiering af projekter og betaling af afdrag.

 Tricia, der er medlem af projekttemaet og rapporterer til Prakash, er ansvarlig for overvågning af projektet dag for dag. Tricia angiver det arbejde, der udføres af teknikerne på hver opgave, herunder de varer, som de har brugt, og de omkostninger, som der er påløbet.  

## Klargøre eksempeldata

Forbered denne gennemgang ved at tilføje Tricia som en ressource.  

### Sådan klargøres eksempeldataene  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.  
2. Klik på handlingen **Ny** for at oprette et nyt ressourcekort.  
3. Indtast følgende oplysninger i oversigtspanelet **Generelt**:  

    - **Nr.**: **Tina**  
    - **Navn**: **Tina**  
    - **Type**: **Person**  

4. Vælg feltet **Basisenhed**, og vælg derefter handlingen **Ny** for at åbne siden **Ressourceenhed**. Vælg **Time** i feltet **Kode**.  
5. Indtast følgende oplysninger i oversigtspanelet **Fakturering**:  

    - **Købspris**: **5**  
    - **Indir. omk.pct**: **4**  
    - **Kostpris**: **10**  
    - **Produktbogføringsgruppe**: **Tjenester**  
    - **Moms-produkt-bogf.gruppe**: **MOMS 25**  

6. Luk siden.

I den næste procedure opretter du en projektkladde for Tricia for at bogføre forbruget.  

### Sådan oprettes et projektkladdenavn  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. Vælg feltet **Kladdenavn** på siden **Projektkladde**. Siden **Projektkladdenavn** åbnes.  
3. Vælg handlingen **Ny** for at oprette en ny linje med følgende oplysninger:  

    - **Navn**: **Tina**  
    - **Beskrivelse**: **Tina**  
    - **Nummerserie**: **JJNL-GEN**  

4. Vælg knappen **OK** for at gemme ændringerne.

## Opsætte et projekt

I dette scenarie vandt CRONUS en kontrakt med en kunde, Progressive Home Furnishings, om at designe en konference- og spisesal. Kunden har base i USA, og projektet kræver specialsoftware. Projektlederen når frem til en aftale med kunden og opretter et projekt, der dækker aftalen.  

### Sådan konfigurerer du et projekt  

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Klik på handlingen **Ny** for at oprette et nyt kort.  
3. Indtast følgende oplysninger i oversigtspanelet **Generelt**:  

    - **Beskrivelse**: **Rådgivning om montering af konferencesal**  
    - **Faktureres til kundenr.**: **01445544**  

4. Indtast følgende oplysninger i oversigtspanelet **Bogføring**:  

    - **Status**: **Planlægning**  
    - **Projektbogføringsgruppe**: **Opsætning**  
    - **VIA-metode**: **Kostværdi**  

5. Gå til oversigtspanelet **Varighed**, angiv dags dato i felterne **Startdato** og **Slutdato**. Disse datoer hjælper med at anvende valutakonvertering, når projektet faktureres.  
6. Gå til oversigtspanelet **Udenrigshandel**, indstil valutakoden til **USD**. Hvis du vælger USD i feltet **Faktureringsvalutakode**, faktureres projektet i US dollar og planlægges kun i den lokale valuta for CRONUS.  

 Du kan tilpasse priser for kunder for de enkelte projekter, afhængigt af de aftaler du har indgået. I den næste procedure angiver projektlederen en pris for Tricias tid, angiver prisen for den nødvendige software og tilføjer rejseudgifter, som kunden accepterer at betale.  

### Tilpasse priser  

1. Gå til **Projektkort**, og vælg handlingen **Ressource**.  
2. Indtast følgende oplysninger på siden **Projektressourcepriser**:  

    - **Kode**: **Tina**  
    - **Salgspris**: **20**  

3. Luk siden.  
4. Vælg handlingen **Vare**.  
5. Indtast følgende oplysninger og tilpasset pris på siden **Projektvarepriser**:  

    1. **Varenr.**: **80201 (grafikprogram)**  
    2. **Salgspris**: **200**  

6. Luk siden.  
7. Vælg handlingen **Finanskonto**.  
8. På siden **Projektfinanskontopriser** skal du angive følgende oplysninger og prisen for rejsen, som kunden accepterede at betale pris plus 25 procent:  

    1. **Finanskonto**: **8430 (rejse)**  
    2. **Kostprisfaktor**: **1,25**  

9. Luk siden.  

 De sidste trin i opsætning af et projekt tilføjer projektopgaver og de planlægningslinjer, der indgår i hver opgave. Planlægningslinjerne bestemmer, hvad kunden faktureres for.  

### Sådan tilføjes projektopgaver  

1. På kortet **Projekt** for det nye projekt skal du vælge handlingen **Projektopgavelinjer**.  
2. I følgende tabel beskrives de oplysninger, du skal angive i felterne.  

    |Projektopgavenr.|Beskrivelse|Projektopgavetype|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Konsulentydelse for montering af sal|Fra-sum|  
    |1010|Konsulentmøde med kunde|Konto|  
    |1020|Udvikling|Konto|  
    |1090|Konsulentydelse i alt|Til-sum|  

3. Vælg handlingen **Indryk projektopgaver** for at vise, at nogle opgaver er underkategorier til andre opgaver.  

En planlægningslinje være en af følgende typer:  

- **Budget**: Føjet til skemaet, men ikke faktureret.  
- **Fakturerbar**: Faktureret, men ikke føjet til skemaet.  
- **Både budget og fakturerbar**: faktureret og føjet til budgettet.  

I denne gennemgang bruger projektleder **Både budget og fakturerbar**. De opretter tre planlægningslinjer for opgaven 1010 og to planlægningslinjer for opgave 1020.  

### Sådan oprettes planlægningslinjer  

1. Vælg linje 1010, og vælg derefter handlingen **Projektplanlægningslinjer**.  
2. Opret planlægningslinjer med følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både budget og fakturerbar | (dags dato) | Ressource | Tina | 40        |     |
    | 2    | Både budget og fakturerbar | (dags dato) | Ressource | Thomas | 40        |     |
    | 3    | Både budget og fakturerbar | (dags dato) | Finanskonto | 8430 (Rejse) | 2 | 400    |

     Luk siden. Totalerne opdateres på siden **Projektopgavelinjer**.  
3. Vælg linje 1020, og vælg derefter handlingen **Projektplanlægningslinjer**. Angiv følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både budget og fakturerbar | (dags dato) | Ressource | Tina | 80        |     |
    | 2    | Både budget og fakturerbar | (dags dato) | Vare | 80201 (Grafikprogram) | 1 |     |

4. Luk siden. Totaler opdateres på siden **Projektopgavelinjer**.  

## Beregne resterede forbrug

Tricia, der er medlem af projektteamet, har arbejdet på projektet i et stykke tid og ønsker at registrere deres timer og forbrug. Tricia arbejdede ikke flere timer end aftalt med kunden i forvejen. Tricia bruger kørslen **Beregn resterede forbrug** til at beregne det resterende forbrug i en projektkladde. For hver opgave beregner kørslen forskellen mellem planlagt forbrug af varer, ressourcer og finansudgifter og det faktiske forbrug, der er bogført i finansposterne for projektet. Det resterende forbrug vises derefter i projektkladden, og Tricia kan bogføre det.  

### Sådan beregnes resterede forbrug  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. På siden **Projektkladde** og i feltet **Kladdenavn** skal du åbne listen **Projektkladdenavne**. Vælg projektkladdenavnet **Tricia**.  
3. Vælg handlingen **Beregn resterende forbrug**.  
4. På siden **Beregn resterende forbrug for projekt** i oversigtspanelet **Projektopgave** skal du vælge feltet **Projektnr.** og vælge det relevante projektnummer, typisk projekt J00010.  
5. Gå til oversigtspanelet **Indstillinger**, indtast **J00001** i feltet **Bilagsnr.**. Disse oplysninger gør fremtidig sporing af bogføringer nemmere.  
6. Angiv dags dato som bogføringsdatoen.  
7. Vælg knappen **OK**. Denne handling opretter projektkladdelinjer baseret på de planlægningslinjer, som Prakash har oprettet.  
8. Vælg knappen **OK** på bekræftelsessiden. Genererede linjer føjes til projektkladden.  
9. Kontroller, at alle bilagsnumre er J00001, og vælg derefter handlingen **Bogfør**. Vælg **Ja** for at bekræfte bogføringen.  

Linjerne er nu bogført.  

## Oprette og bogføre en projektsalgsfaktura

Derefter kan Tricia oprette en ny faktura for hele projektet eller for en del af et projekt. Tricia kan også tilknytte fakturaen til en anden faktura til samme kunde for samme projekt. I dette tilfælde fakturerer Tricia hele projektet, da projektet nu er færdigt.  

### Sådan opretter du en projektsalgsfaktura  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg det projekt, du oprettede tidligere, og vælg derefter handlingen **Opret projektsalgsfaktura**.  
3. Ryd alle filtre på **Projektopgavenr.** i oversigtspanelet **Projektopgave** for at fakturere projektet. I feltet **Projektnr.** skal du vælge det relevante projekt.  
4. Udfyld bogføringsdatoen, og angiv, om du vil oprette én faktura pr. opgave eller kun én enkelt faktura for alle opgaver, i oversigtspanelet **Indstillinger**.  
5. Vælg knappen **OK** for at oprette fakturaen, og vælg knappen **OK** på bekræftelsessiden.  

Når Tricia opretter fakturaen, er den f.eks. tilgængelig fra rollecenteret **Salgsordrebehandler**.

### Sådan bogføres en ny salgsfaktura  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. Åbn fakturaen til kunde nr. 01445544. Du kan se de oplysninger, der er indtastet fra planlægningslinjerne.  
3. Vælg handlingen **Bogfør**. Vælg **Ja** for at bekræfte bogføringen.  

### Sådan vises den bogførte faktura  

1. Åbn det relevante projekt, og vælg derefter handlingen **Projektplanlægningslinjer**.  
2. Markér en hvilken som helst planlægningslinje, der blev faktureret, og vælg derefter handlingen **Salgsfaktura/Kreditnota**.
3. På siden **Projektfakturaer** skal du vælge handlingen **Åbn salgsfaktura/kreditnota**.  

Tricia har et spørgsmål ang. priser, omkostninger og indtjening, der er relevant for dette bestemte projekt, så hun får adgang til disse oplysninger på den nye side **Statistik**.  

### Sådan åbner du siden Statistik  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Statistik**. Du kan gennemgå detaljerede oplysninger om projektpriser, omkostninger og avancer i både lokale og udenlandske valutaer.  
3. Vælg knappen **Luk** for at lukke siden **Projektstatistik**.  

## Håndtere faste priser

CRONUS er bestilt til at oprette konferencerum. Som projektleder vil Prakash gerne have et godt overblik over de opgaver, der er påkrævet for projektet med de tilhørende budgetterede og realiserede omkostninger for hver sag. Derudover vil Prakash gerne kende den samlede kontraktpris for projektet og det beløb, der blev faktureret indtil nu. De har er nået frem til en aftale med kunden om faste priser for dette projekt.  

### Sådan håndteres faste priser i projekter  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg projektnummeret **Guildford**, og vælg derefter handlingen **Projektopgavelinjer**.  
3. Vælg linje 1120, og højreklik på beløbet i feltet **Budget (kostpris)**, og vælg **Specificer**.  

     Ved at gennemse projektplanlægningslinjerne kan Prakash se, at han får brug for Tricia i 30 timer i denne fase af projektet. Prakash aftaler en fast pris med kunden.  

4. På siden **Projektopgavelinjer** skal du markere linje 1120, og derefter vælge handlingen **Projektplanlægningslinjer**. Opret en planlægningslinje med følgende oplysninger:  

    | Linje | Linjetype | Type        | Nummer   | Antal |
    |------|-----------|-------------|-------|----------|
    | 1    | Både budget og fakturerbar  | Ressource | Tina | 30 |

     Luk siden.  
5. Højreklik i feltet **Budget (kostbeløb)**, og vælg **Specificer** igen på siden **Projektopgavelinjer**. Få vist ændringerne i tidsplanen. Du kan se, at de 30 timer er føjet til budgettet.  
6. Luk siderne.  

Når Tricia har føjet budgettet til denne opgavelinje, arbejder hun 25 timer på projektet. Disse timer kan angives i projektkladden.  

### Sådan angives timer i en projektkladde  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") , skriv **Projektkladder**, og vælg derefter det relaterede link.  
2. Angiv følgende oplysninger på en ny linje:  

    - **Linjetype**: **(tom)**  
    - **Bogføringsdato**: **(dags dato)**  
    - **Bilagsnr.**: **J00002**  
    - **Projektnr.**: **Svend Hansen Møbler**  
    - **Projektopgavenr.**: **1120**  
    - **Type**: **Ressource**  
    - **Nr.**: **Tina**  
    - **Antal**: **25**  

3. Vælg handlingen **Bogfør**.  

     Nogle få dage senere, arbejder Tricia for at finde flere 10 timer på projektet, og har arbejdet 35 timer i alt. Da aftalen med kunden lyder på 30 timer, er det kun fem af disse timer, der vil blive faktureret kunden. Tricia føjer manuelt de andre fem timer til budgettet.  

4. På siden **Projektkladde** skal du vælge handlingen **Beregn resterende forbrug**.  
5. På siden **Beregn resterende forbrug for projekt** skal du angive følgende oplysninger i oversigtspanelet **Indstillinger**:  

    - **Bilagsnr.**: **J00003**  
    - **Bogføringsdato**: **(dags dato)**  

6. Angiv følgende oplysninger i oversigtspanelet **Projektopgave**:  

    - **Projektnr.**: **Svend Hansen Møbler**  
    - **Projektopgavenr.**: **1120**  

7. Vælg knappen **OK** for at køre beregningen.

    Der mangler fem timers arbejde for Tina. Feltet **Linjetype** er tomt, hvilket indikerer, at det kun er forbruget, der mangler at blive bogført, da arbejdet allerede blev budgetteret.  

8. Opret en ny linje med følgende oplysninger i **Projektkladde**. Kontroller, at begge projektnumre er i fortløbende i forhold til de numre, du allerede har brugt:  

    - **Linjetype**: **Budget**  
    - **Projektnr.**: **Svend Hansen Møbler**  
    - **Projektopgavenr.**: **1120**  
    - **Type**: **Ressource**  
    - **Nr.**: **Tina**  
    - **Antal**: **5**  

     Hvis du bruger linjetypen **Budget** opdateres de budgetterede omkostninger og priser uden at opdatere de kontraktomkostninger og priser, der faktureres til kunden.  

9. Vælg handlingen **Bogfør**. Vælg knappen **OK** for at lukke siden.  
10. Åbn listen **Projekter**.  
11. Vælg projektet GUILDFORD, og vælg derefter linje 1120 i sektionen **Projektopgavelinjer**, og højreklik på beløbet i feltet **Budget (kostbeløb)**. Vælg **Specificer** for at få vist oplysningerne.  

     Ændringerne angives automatisk på linjen for Projektopgavenr. 1120. I de samlede omkostninger for budgetteret arbejde føjes fem ekstra timers arbejde for Tricia til budgettet.  

12. Vælg knappen **Luk** for at lukke siden.  
13. Højreklik nu på beløbet i feltet **Kontrakt (kostbeløb)**, og vælg **Specificer** for at få vist oplysningerne.  

I den samlede kontraktpris er det kun de oprindeligt kontraktaftalte 30 timer, der er inkluderet, som aftalt med kunde.  

## Kopiere projekter

Prakash er nået frem til en aftale med en kunder, Selagorian Ltd,, om at opsætte 10 konferencerum. Aftalen ligner et tidligere projekt. Det sparer derfor tid at kopiere det tidligere projekt.  

På siden **Kopier projekt** kan du vælge projektet og de opgavelinjer, du vil kopiere.

- Kopier kildeprojektposterne for at oprette planlægningslinjer baseret på det faktiske forbrug.
- Kopier kildeprojektplanlægningslinjerne for at kopiere de oprindelige planlægningslinjer til det nye projekt.

Du kan derefter vælge den planlægningslinje eller finanspostlinjetype, du vil inkludere, ved kun at vælge det, der er relevant for det nye projekt. Til sidst kan du vælge det projekt, som du vil kopiere til, og definere, om priser og antal også skal kopieres.  

### Sådan kopieres et projekt  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Projekter**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** for at oprette et nyt projekt. Angiv følgende oplysninger:  

    - **Beskrivelse**: **Opsætning til 10 konferencerum**  
    - **Faktureres til kundenr.**: **20000**  

3. Vælg handlingen **Kopier projektopgaver fra**.  
4. Indtast følgende på siden **Kopier projektopgaver**:  

    - **Projektnr.**: **Svend Hansen Møbler**  
    - **Projektopgavenr. fra**: **1000**  
    - **Kilde**: **Projektplanlægningslinjer**  
    - **Inkl. planlægningslinjetype**: **Budget + fakturerbar**  
    - **Til projektnr.**: **Svend Hansen Møbler Opsætning af 10 konferencerum**  
    - Vælg felterne **Kopier dimensioner** og **Kopier antal**.  

5. Vælg knappen **OK** for at kopiere projektet, og vælg derefter knappen **OK** for at lukke bekræftelsessiden.  

Ved at sammenligne priser, projektopgavelinjer og projektplanlægningslinjer for de to projekter kan du se, at oplysninger er blevet kopieret.  

## Foretage betalinger af afdrag

CRONUS har lige fået et stort projekt hjem, der vil tage et år at gennemføre. Da det kræver mange ressourcer, opsætter projektlederen kontrakten på en sådan måde, at kunden betaler en del af prisen med det samme, en del, når projektet er halvvejs færdigt, og den sidste betaling ved færdiggørelsen.  

### Sådan oprettes et nyt konto  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. På siden **Kontoplan** skal du vælge handlingen **Ny** for at oprette et nyt kort.  
3. Indtast følgende oplysninger på kortet **Ny finanskonto**:  

    - **Nr.**: **40255**  
    - **Navn**: **Projektbetaling**  

4. Vælg **Tjenester** i feltet **Produktbogføringsgruppe** i oversigtspanelet **Bogføring**. Luk siden.  
5. På siden **Kontoplan** skal du markere **Sagsbetaling nr 40255** og derefter vælge handlingen **Indryk kontoplan**. Vælg **Ja** for at bekræfte.  

Følgende procedurer viser, hvordan du opretter et nyt projekt, angiver priser og derefter oprette betaling af afdrag. På projektopgavelinjerne kan du oprette specifikke linjer, der er dedikeret til betaling af afdrag. Alt det færdiggjorte arbejde på projektet, der føjes til budgettet, angives på forbrugslinjerne. For hver betalingsopgavelinje på planlægningslinjerne er linjetypen **Fakturerbar**, hvilket betyder, at debitoren faktureres. Angiv en ny linje for Udbetalingen. På forbrugsopgavelinjen kan du indtaste oplysningerne for de varer og ressourcer, der er brugt i dette projekt, hvilket vil øge budgettet for f.eks. medarbejdertimer og varer, der er anvendt i projektet.  

### Sådan foretages betaling af afdrag  

1. Opret et nyt projekt.  
2. Udfyld følgende oplysninger på det nye **Projekt**-kort:  

    - **Beskrivelse**: **Omdekoration af receptionsområde**  
    - **Faktureres til kundenr.**: **30000**  
    - **Projektbogføringsgruppe**: **Opsætning**  
    - **VIA-metode**: **Kostværdi**  

3. På projektkortet skal du vælge handlingen **Priser** og derefter vælge handlingen **Ressource**. Angiv følgende oplysninger:  

    - **Kode**: **Tina**  
    - **Salgspris**: **10**  

     Luk siden.  

4. Tilføj projektopgavelinjer på kortet **Projekt** i sektionen **Opgaver**, som beskrevet i følgende tabel:  

    | Linje | Projektopgavenr. | Beskrivelse          | Projektopgavetype |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Betaling - afdragsbetaling | Bogfører       |
    | 2    | 2000         | Brug                | Bogfører       |
    | 3    | 3000         | Betaling - midtvejs     | Konto       |
    | 4    | 4000         | Betaling - afslutning | Bogfører       |

5. Vælg opgave 1000, og vælg derefter handlingen **Projektplanlægningslinjer**.  

6. Opret en planlægningslinje med følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (dags dato) | Finanskonto | 40255 | 1        | 5000       |

     Luk siden.  

7. Vælg opgave 2000, og vælg derefter handlingen **Projektplanlægningslinjer**.  

8. Opret en planlægningslinje med følgende oplysninger:

    | Linje | Linjetype | Planlægningsdato  | Type     | Nummer    | Antal |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (dags dato) | Ressource | Tina | 120      |
    | 2    | Budget    | (dags dato) | Artikel     | 70104  | 10       |

     Luk siden. Du kan se de budgetbeløb, der er opdateret, på siden **Projektopgavelinjer**.  

9. Vælg opgave 32000, og vælg derefter handlingen **Projektplanlægningslinjer**.  

10. Opret en planlægningslinje med følgende oplysninger:

    | Linje | Linjetype | Planlægningsdato   | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (en fremtidig dato) | Finanskonto | 40255 | 1        | 5000       |

     Luk siden.  

11. Opret en tilsvarende planlægningslinjepost for projektopgave 4000.  

 Nu, hvor opgave- og planlægningslinjerne er angivet, kan Per oprette en faktura for første betaling. Prakash gør dette fra projektopgavelinjerne for at sikre, at fakturaen kun indeholder linjer for den første betaling. Du kan åbne salgsorden fra planlægningslinjerne eller opgavelinjerne.  

### Sådan oprettes en faktura  

1. På siden **Projektopgavelinjer** skal du markere linje 1000, og derefter vælge handlingen **Opret salgsfaktura**.  
2. Angiv dags dato som bogføringsdatoen på siden **Opret salgsfaktura**, angiv **Pr. opgave**, og vælg knappen **OK** for at oprette en faktura med standardoplysningerne. Vælg knappen **OK** for at gemme og lukke bekræftelsessiden.  
3. Vælg handlingen **Opret salgsfaktura/kreditnota**. På salgsfakturaen kan du se, at det kun er udbetalingen, der er inkluderet på fakturaen. Du kan nu sende den til kunden som aftalt.  

## Oversigt

Denne gennemgang har taget dig gennem nogle af de grundlæggende trin til at arbejde med projekter i [!INCLUDE[prod_short](includes/prod_short.md)]. Du har lært, hvordan du opretter et nyt projekt, kopierer et projekt, og hvordan du håndterer betalinger. Du har også fået vist en demonstration af, hvordan du kan registrere timer og oprette fakturaer.  

## Se også

 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Konfigurere projektstyring](projects-setup-projects.md)  
 [Bruge ressourcer](projects-how-use-resources.md)  
 [Overvåge status og udførelse](projects-how-monitor-progress-performance.md)  
 [Fakturere projekter](projects-how-invoice-jobs.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
