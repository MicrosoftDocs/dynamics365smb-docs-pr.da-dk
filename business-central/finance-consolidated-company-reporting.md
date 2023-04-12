---
title: Konsolidere data fra flere virksomheder
description: 'Denne artikel beskriver, hvordan du kan konsolidere finansposterne fra to eller flere separate regnskaber (datterselskaber) til et konsolideret regnskab.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.date: 09/29/2022
ms.author: bholtorf
---

# Konsolidering af finansielle oplysninger fra flere regnskaber

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der skal rapportere til overordnede organisationer. I begge tilfælde bruger bogholderen indbyggede værktøjer til at konsolidere de finansielle data.  

Du kan konsolidere finansposterne fra to eller flere separate regnskaber (datterselskaber) til et konsolideret regnskab. Hvert enkelt regnskab, der er involveret i en konsolidering, kaldes en koncernvirksomhed. Det kombinerede regnskab kaldes det konsoliderede regnskab.  

Du kan indlæse data til det konsoliderede regnskab fra andre regnskaber i samme [!INCLUDE [prod_short](includes/prod_short.md)]-lejer fra lejere eller fra filer.  

Hvis en koncernvirksomheds resultatopgørelse er i en anden valuta end den valuta, der er anvendt i det konsoliderede regnskab, skal du oprette valutakurser for konsolideringen.  

Du kan konsolidere:  

* På tværs af regnskaber med forskellige kontoplaner.  
* Regnskaber med forskellige regnskabsår og forskellige valutaer.  
* Enten det fulde beløb eller en procentdel af et regnskabs finansielle oplysninger
* Ved brug af forskellige valutakurser i de enkelte finanskonti
* Virksomheder i andre regnskabs-og virksomhedsstyringsprogrammer

Du opretter det konsoliderede regnskab på samme måde, som du opretter andre regnskaber. Kontoplanerne er uafhængige af kontoplanerne i virksomhedsenheder. Kontoplanen i virksomhedsenhederne kan afvige fra hinanden. Du opretter en liste over regnskaber, der skal konsolideres, kontrollere regnskabsdataene, før du konsoliderer dem, importere filer og oprette konsolideringsrapporter. Du kan finde flere oplysninger i [Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Konsolidering af finansielle oplysninger kan især være relevant i forbindelse med interne processer. Du kan finde flere oplysninger i [Administrere interne transaktioner](intercompany-manage.md).

## Bruge rapporten Konsolideret råbalance

Rapporten **Konsolideret råbalance** kan give dig et overblik over virksomheden samlede finansielle tilstand. Rapporten kombinerer finansposter fra alle dine regnskaber i et nyt virksomhed, som du har oprettet til de konsoliderede data. Dette regnskab kaldes typisk det *konsoliderede regnskab*. Det konsoliderede regnskab er kun en beholder til de konsoliderede data og har ingen direkte forretningsdata. De regnskaber, du inkluderer i det konsoliderede regnskab, bliver **koncernvirksomheder** i rapporten. Du kan finde flere oplysninger i [Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md). Hvis der er fire eller færre koncernvirksomheder, kan du også bruge rapporten **Kons. råbal. - 4 virksomheder**.  

Rapporten viser en linje for hver konto og følger kontoplanens opbygning. En konto vises ikke, hvis alle beløb på linjen er 0. Rapporten viser følgende oplysninger om hver konto:

* Kontonummeret og -navnet, der hører til kontoen.
* Totalerne for koncernregnskabet og for hver koncernvirksomhed. Totaler kan vises som bevægelse eller saldo til dato.
* Elimineringer foretaget i koncernregnskabet. Elimineringerne vil altid blive vist i en periode, der svarer til koncernregnskabets regnskabsår.
* Totalen for koncernregnskabet efter elimineringerne, vist som bevægelse eller saldo til dato.

## Konsolidere data

Den faktiske *konsolidering* er at overføre tallene fra koncernvirksomhederne til det konsoliderede regnskab. Før du gør det, er det en god ide at kontrollere, om der er forskelle mellem de grundlæggende oplysninger i koncernvirksomhederne og det konsoliderede regnskab. Der er to rapporter, du kan bruge til at teste databasen og filen.

### Sådan kontrolleres dataene, før du konsoliderer

Du kan teste dataene, inden du overfører dem til det konsoliderede regnskab. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om der er forskelle mellem oplysningerne i koncernvirksomhederne og den konsoliderede virksomhed. F.eks., om kontonumre eller dimensionskoder er anderledes. Du skal rette fejlene, før du kan køre rapporten. Du kan teste databasen, eller hvis du importerer data fra en XML-fil, kan du teste filen.  

1. Åbn det konsoliderede regnskab.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Test filen og databasen på følgende måde:  

    * For at teste en fil, skal du vælge handlingen **Kontroller fil**, angive navnet på filen, der skal kontrollere, og derefter vælge **Udskriv**.  
    * Du kan teste databasen ved at vælge **Test database**.  

### Kør konsolideringen

Når du har testet dataene, kan du overføre dem til det konsoliderede regnskab.  

1. Log på det konsoliderede regnskab.  
2. I **Rollecenteret Bogholder** skal du vælge handlingen **Kør konsolidering**.  
3. Udfyld de påkrævede felter.  
4. I afsnittet filter skal du angive et filter for den relevante afdeling eller det relevante firmanavn.  
5. Alternativt kan du planlægge en rapport til at køre på et passende klokkeslæt.  

## Fjerne gentagne transaktioner

Når du har konsolideret alle regnskaber, skal du finde de transaktioner, som er registreret mere end én gang på tværs af regnskaber. Behandling af konsolideringselimineringer er en manuel proces.  

Sådan fjernes gentagne transaktioner:

1. Find transaktioner, det kan være nødvendigt at regulere, og angiv finanskladdelinjer for at fjerne disse.
2. Kør **G/L konsolideringselimineringer**-rapporten for at få hjælp til at vurdere virkningen af finanskladdelinjerne inden bogføringen.
3. Bogfør tilpasningsposteringerne.

Rapporten **G/L konsolideringselimineringer** viser en foreløbig råbalance, hvor du kan simulere konsekvenserne af eliminering af poster. Rapporten sammenligner posterne i det konsoliderede regnskab med de elimineringer, der er angivet i finanskladden.

Hvis et koncernvirksomhedsregnskab skal indgå i rapporten, skal det først være oprettet på siden **Virksomheden**. Feltet **Konsolidere** skal markeres.

Hver konto vises på en separat linje, rapporten følger kontoplanens opbygning. En konto vises ikke, hvis alle beløb på linjen er 0. Følgende oplysninger vises om hver konto:

* Kontonummer
* Kontonavn.
* Hvis du har valgt en eller flere koncernvirksomhedskoder i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for koncernregnskabet ekskl. de valgte koncernvirksomheder og elimineringer. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for koncernregnskabet ekskl. elimineringer.
* Hvis du har valgt en koncernvirksomhedskode i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for de indlæste poster fra koncernvirksomheden. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for de bogførte elimineringer i koncernregnskabet.
* Totalen for koncernregnskabet med alle koncernvirksomheder og alle bogførte elimineringer.
* Elimineringer foretaget i koncernregnskabet. Det vil sige posterne i den finanskladde, der er valgt på siden anmodning.
* Bogføringsteksten kopieret fra finanskladden.
* Koncernregnskabets total efter elimineringerne, hvis de bogføres.

## Eksportere og importere konsoliderede data mellem databaser

Hvis data for en koncernvirksomhed er placeret i en anden database, skal du eksportere dataene til en fil, før de kan medtages i konsolideringen. Regnskaberne skal udlæses separat. Til det formål bruges kørslen **Udlæs konsolideringsposter**.  

> [!TIP]
> Brug den samme proces til at eksportere konsoliderede data, der skal sendes til Dynamics 365 Finance, f.eks. Hvis den aktuelle afdeling er et datterselskab, og moderselskabet bruger Dynamics 365 Finance.

Når du kører batchjobbet, behandles alle poster i finanskonti. Indhold i felterne **Beløb** sammentælles og udlæses for hver kombination af valgte dimensioner og dato. Den næste kombination af valgte dimensioner og dato med samme kontonummer behandles. Derefter behandles kombinationerne i det næste kontonummer osv.  

De udlæste poster indeholder følgende felter: **Kontonr.**, **Bogføringsdato** og **Beløb**. Hvis dimensionsoplysningerne også blev eksporteret, medtages dimensionskoderne og dimensionsværdierne også.  

1. For hver eksporteret linje, hvis summen af **Beløb**-felterne er et debetbeløb, eksporteres det kontonummer , der er oprettet i koncernvirksomhedens felt **Kons.debetkonto** til linjen. Hvis summen er et kreditbeløb, eksporteres det tilsvarende tal i feltet **Kons.kreditkonto** til linjen.  
2. Den dato, der bruges til de udlæste linjer er enten periodens slutdato, eller også er det den nøjagtige dato for beregningen, hvis overførslen finder sted pr. dag.  
3. Den dimensionsværdi, der blev udlæst for posten, vil blive det konsoliderede regnskabs dimensionsværdi, som er oprettet i feltet **Konsolideringskode** for dimensionsværdien. Hvis der ikke er blevet oprettet en dimensionsværdi for det konsoliderede regnskab i feltet **Konsolideringskode** for dimensionsværdien, vil selve dimensionsværdien blive udlæst til linjen.  
4. XML-filerne indeholder også valutakurserne i konsolideringsperioden. Disse kurser er inkluderet i en separat sektion øverst i filen.  

## Se også

[Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]