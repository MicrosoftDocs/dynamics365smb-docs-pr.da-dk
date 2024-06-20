---
title: Konsolidere data fra flere virksomheder
description: 'Denne artikel beskriver, hvordan du kan konsolidere finansposterne fra to eller flere separate regnskaber (datterselskaber) til et konsolideret regnskab.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 06/27/2023
ms.custom: bap-template
ms.search.keywords: 'consolidation, subsidiaries, consolidate'
ms.search.form: '1826, 1827'
ms.service: dynamics-365-business-central
---

# Konsolidering af finansielle oplysninger fra flere regnskaber

Nogle organisationer bruger [!INCLUDE [prod_short](includes/prod_short.md)] i flere afdelinger eller juridiske enheder. Andre bruger [!INCLUDE [prod_short](includes/prod_short.md)] i datterselskaber, der skal rapportere til overordnede organisationer. [!INCLUDE [prod_short](includes/prod_short.md)] giver bogholdere værktøjer, der kan hjælpe dem med at overføre finansposter fra to eller flere regnskaber (datterselskaber) til et konsolideret regnskab.  

Hvert regnskab, der er involveret i en konsolidering, kaldes en koncernvirksomhed. Det regnskab, hvor du kombinerer data, kaldes det konsoliderede regnskab.  

Du kan overføre finansielle data fra datterselskaber til det konsoliderede regnskab, selvom datterselskaberne bruger [!INCLUDE [prod_short](includes/prod_short.md)] i forskellige miljøer. Du kan få mere at vide om, hvordan du opretter forbindelse til andre miljøer, ved at gå til [Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

Hvis en koncernvirksomheds resultatopgørelse er i en anden valuta end de øvrige i det konsoliderede regnskab, skal du oprette valutakurser for konsolideringen. Du kan få mere at vide om valutakurser for konsolideringer ved at gå til [Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md#exchrates).  

Du kan konsolidere:  

* På tværs af regnskaber med forskellige kontoplaner.  
* Regnskaber med forskellige regnskabsår og forskellige valutaer.  
* Enten det fulde beløb eller en procentdel af et regnskabs finansielle oplysninger.
* Ved brug af forskellige valutakurser i de enkelte finanskonti.
* Virksomheder i andre regnskabs-og virksomhedsstyringsprogrammer.
* Virksomheder i forskellige [!INCLUDE [prod_short](includes/prod_short.md)]-miljøer.

Du opretter det konsoliderede regnskab på samme måde, som du opretter andre regnskaber. Kontoplanerne er uafhængige af kontoplanerne i virksomhedsenheder. Kontoplanen i virksomhedsenhederne kan afvige fra hinanden. Du kan få mere at vide om opsætning af en konsolidering ved at gå til [Opsætning af firmakonsolidering](finance-consolidated-company-reporting-setup.md).  

> [!TIP]
> Konsolidering af finansielle data kan især være relevant i forbindelse med interne processer. Du kan få mere at vide om Intercompany-funktioner ved at gå til [Administrere interne transaktioner](intercompany-manage.md).

## Konsolidere data

Før du konsoliderer, er det en god ide at teste dine data, før du overfører dem til det konsoliderede regnskab. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, om der er forskelle mellem oplysningerne i koncernvirksomhederne og den konsoliderede virksomhed. F.eks., om kontonumre eller dimensionskoder er anderledes. Ret eventuelle fejl, før du kan køre rapporten. Du kan teste databasen, eller hvis du importerer data fra en XML-fil.

### Test dataene, før du konsoliderer

1. Åbn det konsoliderede regnskab.  
2. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Test filen og databasen på følgende måde:  

    * For at teste en fil, skal du vælge handlingen **Kontroller fil**, angive navnet på filen, der skal kontrollere, og derefter vælge **Udskriv**.  
    * Du kan teste databasen ved at vælge **Test database**.  

### Kør konsolideringen

Når du har testet dataene, kan du overføre dem til det konsoliderede regnskab. En assisteret opsætningsvejledning hjælper dig gennem processen.

> [!NOTE]
> Når du udfører konsolideringen, kan du vælge, hvilke regnskaber der skal medtages. Hvis dit konsoliderede regnskab ikke har adgang til et eller flere datterselskaber, giver vejledningen dig mulighed for at give adgang til dem.

1. Log på det konsoliderede regnskab.  
2. På siden **Virksomhedsenheder** skal du vælge handlingen **Konsolider**.  
3. Udfyld de påkrævede felter.  

## Bruge rapporten Konsolideret råbalance

Rapporten **Konsolideret råbalance** kan give dig et overblik over virksomheden samlede finansielle tilstand. Rapporten kombinerer finansposter fra alle dine regnskaber i et nyt virksomhed, som du har oprettet til de konsoliderede data. Det konsoliderede regnskab er kun en beholder til de konsoliderede data og har ingen direkte forretningsdata. De regnskaber, du inkluderer i det konsoliderede regnskab, bliver **koncernvirksomheder** i rapporten. Hvis der er fire eller færre koncernvirksomheder, kan du også bruge rapporten **Kons. råbal. - 4 virksomheder**.  

Rapporten viser en linje for hver konto og følger kontoplanens opbygning. En konto vises ikke, hvis alle beløb på linjen er 0. Rapporten viser følgende oplysninger om hver konto:

* Kontonummeret og -navnet, der hører til kontoen.
* Totalerne for koncernregnskabet og for hver koncernvirksomhed. Totaler kan vises som bevægelse eller saldo til dato.
* Elimineringer foretaget i koncernregnskabet. Elimineringerne vil altid blive vist i en periode, der svarer til koncernregnskabets regnskabsår.
* Totalen for koncernregnskabet efter elimineringerne, vist som bevægelse eller saldo til dato.

## Fjerne gentagne transaktioner

Når du har konsolideret alle regnskaber, skal du finde de transaktioner, som er registreret mere end én gang på tværs af regnskaber. Behandling af konsolideringselimineringer er en manuel proces.  

Sådan fjernes gentagne transaktioner:

1. Find transaktioner, det kan være nødvendigt at regulere, og angiv finanskladdelinjer for at fjerne disse.
2. Kør **G/L konsolideringselimineringer**-rapporten for at få hjælp til at vurdere virkningen af finanskladdelinjerne inden bogføringen.
3. Bogfør tilpasningsposteringerne.

Rapporten **G/L konsolideringselimineringer** viser en foreløbig råbalance, hvor du kan simulere konsekvenserne af eliminering af poster. Rapporten sammenligner posterne i det konsoliderede regnskab med de elimineringer, der er angivet i finanskladden.

Hvis en afdeling skal indgå i rapporten, skal det først være oprettet på siden **Afdelinger**. Sørg for at aktivere til/fra-knappen **Konsolider**.

Hver konto vises på en separat linje, rapporten følger kontoplanens opbygning. En konto vises ikke, hvis alle beløb på linjen er 0. Rapporten viser følgende oplysninger om hver konto:

* Kontonummer
* Kontonavn.
* Hvis du har valgt en eller flere koncernvirksomhedskoder i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for koncernregnskabet ekskl. de valgte koncernvirksomheder og elimineringer. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for koncernregnskabet ekskl. elimineringer.
* Hvis du har valgt en koncernvirksomhedskode i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for de indlæste poster fra koncernvirksomheden. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for de bogførte elimineringer i koncernregnskabet.
* Totalen for koncernregnskabet med alle koncernvirksomheder og alle bogførte elimineringer.
* Elimineringer foretaget i koncernregnskabet. Det vil sige posterne i den finanskladde, der er valgt på siden anmodning.
* Bogføringsteksten kopieret fra finanskladden.
* Koncernregnskabets total efter elimineringerne, hvis de bogføres.

## Eksportere og importere konsoliderede data mellem databaser

Hvis data for en afdeling findes i en anden database, kan du foretage en manuel filbaseret overførsel eller automatisere processen ved hjælp af en API. Du kan få mere at vide om API'en ved at gå til [Brug vores API til automatisk at dele data på tværs af miljøer](#use-our-api-to-automatically-share-data-across-environments).

I dette afsnit beskrives den manuelle, filbaserede proces.

Du eksporterer dataene til en fil, før du medtager dem i konsolideringen. Eksportere hvert regnskab separat ved hjælp af kørslen **Eksporter konsolidering**.  

> [!TIP]
> Brug den samme proces til at eksportere konsoliderede data, som du skal sende til Dynamics 365 Finance. Hvis afdelingen f.eks. er et datterselskab, og moderselskabet bruger Dynamics 365 Finance.

Når du kører batchjobbet, behandles alle poster i finanskonti. Indhold i felterne **Beløb** sammentælles og udlæses for hver kombination af valgte dimensioner og dato. Den næste kombination af valgte dimensioner og dato med samme kontonummer behandles. Derefter behandles kombinationerne i det næste kontonummer osv.  

De udlæste poster indeholder følgende felter: **Kontonr.**, **Bogføringsdato** og **Beløb**. Hvis dimensionsoplysningerne også blev eksporteret, medtages dimensionskoderne og dimensionsværdierne også.  

1. For hver eksporteret linje, hvis summen af **Beløb**-felterne er et debetbeløb, eksporteres det kontonummer , der er oprettet i koncernvirksomhedens felt **Kons.debetkonto** til linjen. Hvis summen er et kreditbeløb, eksporteres det tilsvarende tal i feltet **Kons.kreditkonto** til linjen.  
2. Den dato, der bruges til de udlæste linjer er enten periodens slutdato, eller også er det den nøjagtige dato for beregningen, hvis overførslen finder sted pr. dag.  
3. Den dimensionsværdi, der blev udlæst for posten, vil blive det konsoliderede regnskabs dimensionsværdi, som er oprettet i feltet **Konsolideringskode** for dimensionsværdien. Hvis der ikke er blevet oprettet en dimensionsværdi for det konsoliderede regnskab i feltet **Konsolideringskode** for dimensionsværdien, vil selve dimensionsværdien blive udlæst til linjen.  
4. XML-filerne indeholder også valutakurserne i konsolideringsperioden. Disse kurser er inkluderet i en separat sektion øverst i filen.  

## Brug vores API til automatisk at dele data på tværs af miljøer

[!INCLUDE [prod_short](includes/prod_short.md)] indeholder en API, som du kan bruge til at automatisere processen med at dele økonomiske data fra afdelinger til det konsoliderede regnskab. API'en er gratis at bruge og nem at konfigurere. Det giver dig endda mulighed for at dele data på tværs af [!INCLUDE [prod_short](includes/prod_short.md)] miljøer. Det kan f.eks. være nødvendigt at dele på tværs af miljøer, når afdelingerne ikke er i de samme geografiske Azure-områder. Du kan få mere at vide om, hvordan du bruger API'en til at automatisere konsolideringsprocessen, ved at gå til [Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md#busunit).

## Se også

[Konfigurere virksomhedskonsolidering](finance-consolidated-company-reporting-setup.md)  
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]