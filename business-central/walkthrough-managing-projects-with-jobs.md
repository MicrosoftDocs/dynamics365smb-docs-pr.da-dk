---
title: Gennemgang - Administration af projekter med sager
description: Denne gennemgang introducerer funktionerne til projektstyring i opgaver, som giver dig mulighed for at planlægge brugen af virksomhedens ressourcer og meget mere.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/24/2021
ms.author: edupont
ms.openlocfilehash: a4be92935903c1572e43af0f035e101fe0567772
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8513415"
---
# <a name="walkthrough-managing-projects-with-jobs"></a>Gennemgang: Administration af projekter med sager

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Denne gennemgang giver dig en introduktion til projektstyringsfunktioner i sager. Du kan bruge modulet Sager til at planlægge brugen af virksomhedens ressourcer og holde styr på de forskellige omkostninger, der er forbundet med ressourcerne på et bestemt projekt. Sager inkluderer forbruget af medarbejdertimer, maskintimer, lagervarer og andre brugstyper, du ønsker at spore, efterhånden som en sag skrider frem.  

 Denne gennemgang beskriver opsætningen af et nyt job samt nogle af de almindelige opgaver, som f.eks. fastprishåndtering, betaling af afdrag, bogføring af fakturaer fra sager og kopiering af sager.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
 Denne gennemgang viser følgende opgaver:  

### <a name="setting-up-a-job"></a>Oprettelse af en sag  
 Med den budgetstruktur, der oprettet for sager, er oprettelse af en sag ligetil. Denne gennemgang omfatter følgende procedurer:  

- Hvordan du opretter sagsopgavelinjer og planlægningslinjer.  
- Hvordan du opretter sags-specifikke priser på varer, ressourcer og finanskonti.  
- Fakturering fra en sag.  

### <a name="handling-fixed-prices"></a>Håndtere faste priser  
 I Sager kan du håndtere faste priser og priser på tjenester eller varer, der er aftalt med kunder i forvejen. I denne gennemgang kan du gøre følgende:  

- Se, hvordan leverandør- og fakturaværdier bestemmes.  
- Gøre plads til ekstraarbejde i planen, der ikke er faktureret.  

### <a name="copying-a-job"></a>Kopiering af en sag  
 Denne gennemgang fokuserer på, hvordan du kan kopiere en del af eller en komplet sag for at reducere behovet for manuel indtastning af data og forbedre nøjagtigheden. Dette omfatter følgende:  

- Kopiering af en del af en sag til en ny sag.  
- Kopiering af sags-specifikke priser.  
- Kopiering af planlægningslinjer.  

### <a name="making-payment-by-installment"></a>Betaling af afdrag  
 Når et stort, dyrt projekt varer længere tid, laver kunden ofte en aftale med virksomheden om at betale afdrag. Dette scenarie viser, hvordan du opretter betaling af afdrag håndteres og dækker følgende:  

- Hvordan betaling af afdrag for en sag oprettes.  
- Fakturering af betalinger til debitorer.  
- Kontering af forbrug i en sag opsat til betaling af afdrag.  

## <a name="roles"></a>Roller  
 Denne gennemgang indeholder opgaver for følgende roller:  

- Projektleder  
- Projektteammedlem  

## <a name="prerequisites"></a>Forudsætninger  
 Før du kan udføre opgaverne i denne gennemgang, skal du gøre følgende:  

- Installer CRONUS-demonstrationsdatabasen.
- Opret eksempeldata ved at bruge trinnene i følgende afsnit.  

## <a name="story"></a>Historie  
Denne gennemgang fokuserer på CRONUS, et design- og konsulentfirma, der designer og tilpasser nye infrastrukturer, f.eks. konferencerum og kontorer, med møbler, tilbehør og lagerenheder. Det meste af firmaets arbejde er projektorienteret. Per er projektleder hos CRONUS. Han bruger sager til at give ham et overblik over igangværende sager, som CRONUS har startet, samt de sager, der er afsluttet. Det er som regel ham, der indgår aftaler med kunderne og indtaster sagens hovedkomponenter, hvilket er opgave- og planlægningslinjer i [!INCLUDE[prod_short](includes/prod_short.md)]. Han konstaterer, at oprettelse, vedligeholdelse og gennemgang af oplysninger er ligetil. Per kan også lide, den måde [!INCLUDE[prod_short](includes/prod_short.md)] aktiverer kopiering af sager og betaling af afdrag.

 Tina, der er medlem af projekttemaet og rapporterer til Per, er ansvarlig for overvågning af sagen dag for dag. Hun indtaster sit eget arbejde i tillæg til det arbejde, der udføres af teknikere på hver opgave. Hun registrerer de varer, som de har brugt, og de omkostninger, som de har afholdt.  

## <a name="preparing-sample-data"></a>Klargøre eksempeldata  
 Forbered denne gennemgang ved at tilføje Tina som en ny ressource.  

### <a name="to-prepare-the-sample-data"></a>Sådan klargøres eksempeldataene  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ressourcer**, og vælg derefter det relaterede link.  
2.  Klik på handlingen **Ny** for at oprette et nyt ressourcekort.  
3.  Indtast følgende oplysninger i oversigtspanelet **Generelt**:  

    - **Nr.**: **Tina**  
    - **Navn**: **Tina**  
    - **Type**: **Person**  

4.  Vælg feltet **Basisenhed**, og vælg derefter handlingen **Ny** for at åbne siden **Ressourceenhed**. Vælg **Time** i feltet **Kode**.  
5.  Indtast følgende oplysninger i oversigtspanelet **Fakturering**:  

    - **Købspris**: **5**  
    - **Indir. omk.pct**: **4**  
    - **Kostpris**: **10**  
    - **Produktbogføringsgruppe**: **Tjenester**  
    - **Moms-produkt-bogf.gruppe**: **MOMS 25**  

6. Luk siden.

I den næste procedure opretter du en sagskladde for Tina for at bogføre hendes forbrug.  

### <a name="to-create-a-job-journal-batch"></a>Sådan oprettes et sagskladdenavn  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2.  Vælg feltet **Kladdenavn** på siden **Sagskladde**. Siden **Kladdenavn** åbnes.  
3.  Vælg handlingen **Ny** for at oprette en ny linje med følgende oplysninger:  

    - **Navn**: **Tina**  
    - **Beskrivelse**: **Tina**  
    - **Nummerserie**: **JJNL-GEN**  

4.  Vælg knappen **OK** for at gemme ændringerne.

## <a name="setting-up-a-job"></a>Oprettelse af en sag  
 I dette scenarie, har CRONUS vundet en kontrakt med en kunde, Progressive Home Furnishings, om at designe en konference- og spisesal. Kunden har base i USA, og projektet kræver specialsoftware. Projektlederen når frem til en aftale med kunden og opretter en sag, der dækker aftalen.  

### <a name="to-set-up-a-job"></a>Sådan oprettes en sag  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2.  Klik på handlingen **Ny** for at oprette et nyt kort.  
3.  Indtast følgende oplysninger i oversigtspanelet **Generelt**:  

    - **Beskrivelse**: **Rådgivning om montering af konferencesal**  
    - **Faktureres til kundenr.**: **01445544**  

4.  Indtast følgende oplysninger i oversigtspanelet **Bogføring**:  

    - **Status**: **Planlægning**  
    - **Sagsbogføringsgruppe**: **Opsætning**  
    - **VIA-metode**: **Kostværdi**  

5.  Gå til oversigtspanelet **Varighed**, angiv dags dato i felterne **Startdato** og **Slutdato**. Disse datoer hjælper med at anvende valutakonvertering, når sagen faktureres.  
6.  Gå til oversigtspanelet **Udenrigshandel**, indstil valutakoden til **USD**. Hvis du vælger USD i feltet **Faktureringsvalutakode**, faktureres sagen i US dollar og planlægges kun i den lokale valuta for CRONUS.  

 Du kan tilpasse priser til kunder pr. sagsbasis, afhængigt af de aftaler, du har indgået. I den næste procedure angiver projektlederen en pris for Tinas tid, angiver prisen for den nødvendige software og tilføjer rejseudgifter, som debitor har accepteret at betale.  

### <a name="to-customize-pricing"></a>Tilpasse priser  

1.  Gå til sagskortet, vælg handlingen **Ressource**.  
2.  Indtast følgende oplysninger på siden **Sagsressourcepriser**:  

    - **Kode**: **Tina**  
    - **Salgspris**: **20**  

3.  Luk siden.  
4.  Vælg handlingen **Vare**.  
5.  Indtast følgende oplysninger og tilpasset pris på siden **Sagsvarepriser**:  

    1.  **Varenr.**: **80201 (grafikprogram)**  
    2.  **Salgspris**: **200**  

6.  Luk siden.  
7.  Vælg handlingen **Finanskonto**.  
8.  På siden **Sagsfinanskontopriser** skal du angive følgende oplysninger og prisen for rejsen, som debitor har accepteret at betale pris plus 25 procent:  

    1.  **Finanskonto**: **8430 (rejse)**  
    2.  **Kostprisfaktor**: **1,25**  

9. Luk siden.  

 De sidste trin i opsætning af en sag tilføjer sagsopgaver og de planlægningslinjer, der indgår i hver opgave. Planlægningslinjerne bestemmer, hvad kunden faktureres for.  

### <a name="to-add-job-tasks"></a>Sådan tilføjes sagsopgaver  

1.  På kortet **Sag** for den nye sag skal du vælge handlingen **Sagsopgavelinjer**.  
2.  I følgende tabel beskrives de oplysninger, du skal angive i felterne.  

    |Sagsopgavenr.|Beskrivelse|Sagsopgavetype|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Konsulentydelse for montering af sal|Fra-sum|  
    |1010|Konsulentmøde med kunde|Konto|  
    |1020|Udvikling|Konto|  
    |1090|Konsulentydelse i alt|Til-sum|  

3.  Vælg handlingen **Indryk sagsopgaver** for at vise, at nogle opgaver er underkategorier til andre opgaver.  

 En planlægningslinje være en af følgende typer:  

- **Budget**: Føjet til skemaet, men ikke faktureret.  
- **Fakturerbar**: Faktureret, men ikke føjet til skemaet.  
- **Både budget og fakturerbar**: faktureret og føjet til budgettet.  

 I denne gennemgang bruger projektleder **Både budget og fakturerbar**. Han oprettes de tre planlægningslinjer for opgaven 1010 og to planlægningslinjer for opgave 1020.  

### <a name="to-create-planning-lines"></a>Sådan oprettes planlægningslinjer  

1. Vælg linje 1010, og vælg derefter handlingen **Sagsplanlægningslinjer**.  

2. Opret planlægningslinjer med følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både budget og fakturerbar | (dags dato) | Ressource | Tina | 40        |     |
    | 2    | Både budget og fakturerbar | (dags dato) | Ressource | Thomas | 40        |     |
    | 3    | Både budget og fakturerbar | (dags dato) | Finanskonto | 8430 (Rejse) | 2 | 400    |

     Luk siden. Totalerne opdateres på siden **Sagsopgavelinjer**.  
3. Vælg linje 1020, og vælg derefter handlingen **Sagsplanlægningslinjer**. Angiv følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Både budget og fakturerbar | (dags dato) | Ressource | Tina | 80        |     |
    | 2    | Både budget og fakturerbar | (dags dato) | Vare | 80201 (Grafikprogram) | 1 |     |

4. Luk siden. Totaler opdateres på siden **Sagsopgavelinjer**.  

## <a name="calculating-remaining-usage"></a>Beregne resterede forbrug  
 Tina, der er medlem af projektteamet, har arbejdet på sagen i et stykke tid og ønsker at registrere sine timer og forbrug på sagen. Hun har ikke arbejdet mere end aftalt med kunden i forvejen. Hun bruger kørslen **Beregn resterede forbrug** til at beregne det resterende forbrug for sagen i sagskladden. For hver opgave beregner kørslen forskellen mellem planlagt forbrug af varer, ressourcer og finansudgifter og det faktiske forbrug, der er bogført i finansposterne. Det resterende forbrug vises derefter i sagskladden, hvor hun kan bogføre det.  

### <a name="to-calculate-remaining-usage"></a>Sådan beregnes resterede forbrug  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2.  På siden **Sagskladde** og feltet **Kladdenavn**, skal du åbne listen **Job Journals Batch**. Vælg sagskladden **Tina**.  
3.  Vælg handlingen **Beregn resterende forbrug**.  
4.  Vælg **Sagsnr.** i oversigtspanelet **Sagsopgaver** på siden **Beregn resterende forbrug for sag**, og vælg det relevante sagsnummer, typisk job J00010.  
5.  Gå til oversigtspanelet **Indstillinger**, indtast **J00001** i feltet **Bilagsnr.**. Dette gør fremtidig sporing af bogføringer nemmere.  
6.  Angiv dags dato som bogføringsdatoen.  
7.  Vælg knappen **OK**. Dermed oprettes der opgavekladdelinjer, der kommer fra de planlægningslinjer, som Per oprettede for sagen.  
8.  Vælg knappen **OK** på bekræftelsessiden. Genererede linjer føjes til sagskladde.  
9. Kontroller, at alle bilagsnumre er J00001, og vælg derefter handlingen **Bogfør**. Vælg **Ja** for at bekræfte bogføringen.  

Linjerne er nu bogført.  

## <a name="creating-and-posting-a-job-sales-invoice"></a>Oprette og bogføre en sagssalgsfaktura  
 Derefter kan Tina oprette en ny faktura for hele sagen eller for en del af en sag. Hun kan også tilknytte fakturaen til en anden faktura til samme kunde for samme sag. I dette tilfælde fakturerer hun hele sagen, da projektet nu er færdigt.  

### <a name="to-create-a-job-sales-invoice"></a>Sådan oprettes en sagssalgsfaktura  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2.  Vælg den sag, du oprettede tidligere, og vælg derefter handlingen **Opret salgsfaktura**.  
3.  Fjern alle filtre på **Sagsopgavenr.** i oversigtspanelet **Sagsopgave** for at fakturere sagen. Vælg det relevante job i feltet **Sagsnr.**.  
4.  Udfyld bogføringsdatoen, og angiv, om du vil oprette én faktura pr. opgave eller kun én enkelt faktura for alle opgaver, i oversigtspanelet **Indstillinger**.  
5.  Vælg knappen **OK** for at oprette fakturaen, og vælg knappen **OK** på bekræftelsessiden.  

 Når Tina opretter fakturaen, kan hun f.eks. få adgang til den fra rollecenteret **Salgsordrebehandler**. 

### <a name="to-post-a-new-sales-invoice"></a>Sådan bogføres en ny salgsfaktura  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn fakturaen til kunde nr. 01445544. Du kan se de oplysninger, der er indtastet fra planlægningslinjerne.  
3.  Vælg handlingen **Bogfør**. Vælg **Ja** for at bekræfte bogføringen.  

### <a name="to-view-the-posted-invoice"></a>Sådan vises den bogførte faktura  

1.  Åbn sagen, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
2.  Markér en hvilken som helst faktureret planlægningslinje, og vælg derefter handlingen **Salgsfaktura/Kreditnota**.
3. På siden **Sagsfakturaer** skal du vælge handlingen **Åbn salgsfaktura/kreditnota**.  

 Tina har et spørgsmål ang. priser, omkostninger og indtjening, der er relevant for denne bestemte sag, så hun får adgang til disse oplysninger på den nye side **Statistik**.  

### <a name="to-open-the-statistics-page"></a>Sådan åbner du siden Statistik  

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Statistik**. Du kan gennemgå detaljerede oplysninger om sagspriser, omkostninger og avancer i både lokale og udenlandske valutaer.  
3.  Vælg knappen **Luk** for at lukke siden **Sagsstatistik**.  

## <a name="handling-fixed-prices"></a>Håndtere faste priser  
 CRONUS er blevet bestilt til at oprette konferencerum. Som projektleder ønsker Per at have et godt overblik over de opgaver, der er påkrævet for sagen med de tilhørende budgetterede og realiserede omkostninger for hver sag. Derudover vil han gerne kende den samlede kontraktpris for sagen og det beløb, der er faktureret indtil nu. Han er nået frem til en aftale med kunden om faste priser for denne sag.  

### <a name="to-manage-fixed-pricing-in-jobs"></a>Sådan håndteres faste priser i sager  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Vælg sagsnummeret **Svend Hansen Møbler**, og vælg derefter handlingen **Sagsopgavelinjer**.  
3. Vælg linje 1120, og højreklik på beløbet i feltet **Budget (kostpris)**, og vælg **Specificer**.  

     Ved at gennemse sagsplanlægningslinjerne, kan Per se, at han får brug for Tina i 30 timer i denne fase af projektet. Han aftaler en fast pris med kunden.  

4. På siden **Sagsopgavelinjer** skal du markere linje 1120, og derefter vælge handlingen **Sagsplanlægningslinjer**. Opret en planlægningslinje med følgende oplysninger:  

    | Linje | Linjetype | Type        | Nummer   | Antal |
    |------|-----------|-------------|-------|----------|
    | 1    | Både budget og fakturerbar  | Ressource | Tina | 30 |

     Luk siden.  
5. Højreklik på feltet i feltet **Budget (kostbeløb)**, og vælg **Specificer** igen på siden **Sagsopgavelinjer**. Få vist ændringerne i tidsplanen. Du kan se, at de 30 timer er føjet til budgettet.  
6. Luk siderne.  

Når Tina har føjet budgettet til denne opgavelinje, arbejder hun 25 timer på sagen. Hun angiver disse timer i sagskladden.  

### <a name="to-enter-hours-in-the-job-journal"></a>Sådan angives timer i sagskladden  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sagskladder**, og vælg derefter det relaterede link.  
2. Angiv følgende oplysninger på en ny linje:  

    - **Linjetype**: **(tom)**  
    - **Bogføringsdato**: **(dags dato)**  
    - **Bilagsnr.**: **J00002**  
    - **Sagsnr.**: **Svend Hansen Møbler**  
    - **Sagsopgavenr.**: **1120**  
    - **Type**: **Ressource**  
    - **Nr.**: **Tina**  
    - **Antal**: **25**  

3. Vælg handlingen **Bogfør**.  

     Nogle få dage senere, arbejder Tina ti timer til på sagen. Hun har nu arbejdet 35 timer alt i alt. Da aftalen med kunden lyder på 30 timer, er det kun fem af disse timer, der vil blive faktureret kunden. Tina vil føje de ekstra fem timer, som hun har arbejdet, manuelt til tidsplanen.  

4. På siden **Sagskladde** skal du vælge handlingen **Beregn resterende forbrug**.  
5. På siden **Beregn resterende forbrug for sag** skal du angive følgende oplysninger i oversigtspanelet **Indstillinger**:  

    - **Bilagsnr.**: **J00003**  
    - **Bogføringsdato**: **(dags dato)**  

6. Angiv følgende oplysninger i oversigtspanelet **Sagsopgave**:  

    - **Sagsnr.**: **Svend Hansen Møbler**  
    - **Sagsopgavenr.**: **1120**  

7. Vælg knappen **OK** for at køre beregningen.

    Der mangler fem timers arbejde for Tina. Feltet **Linjetype** er tomt, hvilket indikerer, at det kun er forbruget, der mangler at blive bogført, da arbejdet allerede er budgetteret.  

8. Opret en ny linje med følgende oplysninger i **Sagskladde**. Kontroller, at både sagsnumre er i fortløbende i forhold til dem, du allerede har brugt:  

    - **Linjetype**: **Budget**  
    - **Sagsnr.**: **Svend Hansen Møbler**  
    - **Sagsopgavenr.**: **1120**  
    - **Type**: **Ressource**  
    - **Nr.**: **Tina**  
    - **Antal**: **5**  

     Ved at bruge linjetypen **Budget** opdateres de budgetterede omkostninger og priser uden at opdatere de kontraktomkostninger og priser, der faktureres til kunden.  

9. Vælg handlingen **Bogfør**. Vælg knappen **OK** for at lukke siden.  
10. Åbn listen **Sager**.  
11. Vælg sagen Svend Hansen Møbler, og vælg derefter linje 1120 i sektionen **Sagsopgavelinjer**, og højreklik på beløbet i feltet **Budget (kostbeløb)**. Vælg **Specificer** for at få vist oplysningerne.  

     Ændringerne angives automatisk på linjen for Sagsopgavenr. 1120. I de samlede omkostninger for budgetteret arbejde føjes fem ekstra timers arbejde for Tina til budgettet.  

12. Vælg knappen **Luk** for at lukke siden.  
13. Højreklik nu på beløbet i feltet **Kontrakt (kostbeløb)**, og vælg **Specificer** for at få vist oplysningerne.  

Når du gennemser tabellen for den samlede kontraktpris, er det kun de oprindeligt kontraktaftalte 30 timer, der er inkluderet, da dette er det, der er aftalt med kunden.  

## <a name="copying-jobs"></a>Kopiere sager

Per er nået frem til en aftale med en kunder, Ravel Møbler, om at opsætte ti konferencerum. Aftalen ligner en tidligere sag. Derfor vil det spare tid at kopiere den tidligere sag.  

På siden **Kopier sag** kan du vælge sagen og de opgavelinjer, du vil kopiere. Du kan også vælge at kopiere kildesagsposterne, der opretter planlægningslinjer baseret på det faktiske forbrug, eller du kan kopiere kildesagsplanlægningslinjerne, der kopierer de oprindelige planlægningslinjer til den nye sag. Du kan derefter vælge den planlægningslinje eller finanspostlinjetype, du vil inkludere, ved kun at vælge det, der er relevant for den nye sag. Til sidst kan du vælge den sag, som du vil kopiere til, og definere, om priser og antal også skal kopieres.  

### <a name="to-copy-a-job"></a>Sådan kopieres en sag  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Sager**, og vælg derefter det relaterede link.  
2. Klik på handlingen **Ny** for at oprette en ny sag. Angiv følgende oplysninger:  

    - **Beskrivelse**: **Opsætning til 10 konferencerum**  
    - **Faktureres til kundenr.**: **20000**  

3. Vælg handlingen **Kopier sagsopgaver fra**.  
4. Indtast følgende på siden **Kopier sagsopgaver**:  

    - **Sagsnr.**: **Svend Hansen Møbler**  
    - **Sagsopgavenr. fra**: **1000**  
    - **Kilde**: **Sagsplanlægningslinjer**  
    - **Inkl. planlægningslinjetype**: **Budget + fakturerbar**  
    - **Til sagsnr.**: **Svend Hansen Møbler Opsætning af 10 konferencerum**  
    - Vælg felterne **Kopier dimensioner** og **Kopier antal**.  

5. Vælg knappen **OK** for at kopiere sagen, og vælg derefter knappen **OK** for at lukke bekræftelsessiden.  

Ved at sammenligne priser, sagsopgavelinjer og sagsplanlægningslinjer for de to job, kan du se, at oplysninger er blevet kopieret.  

## <a name="making-payments-by-installments"></a>Foretage betaling af afdrag

CRONUS har lige fået et stort projekt hjem, der vil tage mere end et år at gennemføre. Da det kræver tildeling af en lang række ressourcer, opsætter projektlederen kontrakten på en sådan måde, at kunden betaler en del af prisen med det samme, en del, når projektet er halvvejs færdigt, og den sidste betaling ved færdiggørelsen.  

### <a name="to-set-up-a-new-account"></a>Sådan oprettes et nyt konto  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. På siden **Kontoplan** skal du vælge handlingen **Ny** for at oprette et nyt kort.  
3. Indtast følgende oplysninger på kortet **Ny finanskonto**:  

    - **Nr.**: **40255**  
    - **Navn**: **Sagsbetaling**  

4. Vælg **Tjenester** i feltet **Produktbogføringsgruppe** i oversigtspanelet **Bogføring**. Luk siden.  
5. På siden **Kontoplan** skal du markere **Sagsbetaling nr 40255** og derefter vælge handlingen **Indryk kontoplan**. Vælg **Ja** for at bekræfte.  

Følgende procedurer viser, hvordan du opretter et nyt job, angiver priser og derefter oprette betaling af afdrag. På sagsopgavelinjerne kan du oprette specifikke linjer, der er dedikeret til betaling af afdrag. Alt det færdiggjorte arbejde, der føjes til budgettet, angives på forbrugslinjerne. For hver betalingsopgavelinje på planlægningslinjerne er linjetypen **Fakturerbar**, hvilket betyder, at debitoren faktureres. Angiv en ny linje for Udbetalingen. På forbrugsopgavelinjen kan du indtaste oplysningerne for de varer og ressourcer, der er brugt i dette projekt, hvilket vil øge budgettet for f.eks. medarbejdertimer og varer, der er anvendt i sagen.  

### <a name="to-make-a-payment-by-installment"></a>Sådan foretages betaling af afdrag  

1. Opret en ny sag.  
2. Udfyld følgende oplysninger på det nye **Job**-kort:  

    - **Beskrivelse**: **Omdekoration af receptionsområde**  
    - **Faktureres til kundenr.**: **30000**  
    - **Sagsbogføringsgruppe**: **Opsætning**  
    - **VIA-metode**: **Kostværdi**  

3. På jobkortet skal du vælge handlingen **Priser** og derefter vælge handlingen **Ressource**. Angiv følgende oplysninger:  

    - **Kode**: **Tina**  
    - **Salgspris**: **10**  

     Luk siden.  

4. Tilføj sagsopgavelinjer på kortet **Sag** i sektionen **Opgaver**, som beskrevet i følgende tabel:  

    | Linje | Sagsopgavenr. | Beskrivelse          | Sagsopgavetype |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Betaling - afdragsbetaling | Bogføring       |
    | 2    | 2000         | Forbrug                | Konto       |
    | 3    | 3000         | Betaling - midtvejs     | Konto       |
    | 4    | 4000         | Betaling - afslutning | Konto       |

5. Vælg opgave 1000, og vælg derefter handlingen **Sagsplanlægningslinjer**.  

6. Opret en planlægningslinje med følgende oplysninger:  

    | Linje | Linjetype | Planlægningsdato  | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (dags dato) | Finanskonto | 40255 | 1        | 5000       |

     Luk siden.  

7. Vælg opgave 2000, og vælg derefter handlingen **Sagsplanlægningslinjer**.  

8. Opret en planlægningslinje med følgende oplysninger:

    | Linje | Linjetype | Planlægningsdato  | Type     | Nummer    | Antal |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (dags dato) | Ressource | Tina | 120      |
    | 2    | Budget    | (dags dato) | Vare     | 70104  | 10       |

     Luk siden. Du kan se de budgetbeløb, der er opdateret, på siden **Sagsopgavelinjer**.  

9. Vælg opgave 32000, og vælg derefter handlingen **Sagsplanlægningslinjer**.  

10. Opret en planlægningslinje med følgende oplysninger:

    | Linje | Linjetype | Planlægningsdato   | Type        | Nummer   | Antal | Enhedspris |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Fakturerbar  | (en fremtidig dato) | Finanskonto | 40255 | 1        | 5000       |

     Luk siden.  

11. Opret en tilsvarende planlægningslinjepost for sagsopgave 4000.  

 Nu, hvor opgave- og planlægningslinjerne er angivet, kan Per oprette en faktura for første betaling. Han gør dette fra sagsopgavelinjerne for at sikre, at fakturaen kun indeholder linjer for den første betaling. Du kan åbne salgsorden fra planlægningslinjerne eller opgavelinjerne.  

### <a name="to-create-an-invoice"></a>Sådan oprettes en faktura  

1.  På siden **Sagsopgavelinjer** skal du markere linje 1000, og derefter vælge handlingen **Opret salgsfaktura**.  
2.  Angiv dags dato som bogføringsdatoen på siden **Opret salgsfaktura**, angiv **Pr. opgave**, og vælg knappen **OK** for at oprette en faktura med standardoplysningerne. Vælg knappen **OK** for at gemme og lukke bekræftelsessiden.  
3.  Vælg handlingen **Opret salgsfaktura/kreditnota**. På salgsfakturaen kan du se, at det kun er udbetalingen, der er inkluderet på fakturaen. Du kan nu sende den til kunden som aftalt.  

## <a name="next-steps"></a>Efterfølgende trin  
 Denne gennemgang har taget dig gennem nogle af de grundlæggende trin til at arbejde med sager i [!INCLUDE[prod_short](includes/prod_short.md)]. Du har lært, hvordan du opretter en ny sag, kopierer en sag og hvordan du håndterer betalinger. Du har også fået vist en demonstration af, hvordan du kan registrere timer og oprette fakturaer.  

## <a name="see-also"></a>Se også

 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)   
 [Konfigurere projektstyring](projects-setup-projects.md)   
 [Bruge ressourcer](projects-how-use-resources.md)   
 [Overvåge status og udførelse](projects-how-monitor-progress-performance.md)   
 [Fakturere sager](projects-how-invoice-jobs.md)  
 [Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]