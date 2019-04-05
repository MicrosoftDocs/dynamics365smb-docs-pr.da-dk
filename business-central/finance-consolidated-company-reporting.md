---
title: Konsolidere data fra flere virksomheder | Microsoft Docs
description: Få vist en oversigt over den finansielle tilstand på tværs af din virksomhed.
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: consolidation, subsidiaries, consolidate
ms.date: 03/11/2019
ms.author: bholtorf
ms.openlocfilehash: feda9d1f681c40746db488027fdd8ae1d06a4d94
ms.sourcegitcommit: 2b2c3b488a610a5d3b51fc8218c40b0b732fddf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/11/2019
ms.locfileid: "832593"
---
# <a name="consolidating-financial-data-from-multiple-companies"></a>Konsolidering af finansielle oplysninger fra flere regnskaber
Hvis du har mere end én virksomhed i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan rapporten Konsolideret råbalance i Rollecenteret Regnskabsmedarbejder give dig et overblik over virksomheden samlede finansielle tilstand.  

Rapporten kombinerer finansposter fra alle dine regnskaber i et nyt virksomhed, som du opretter til at indeholder de konsoliderede data. Dette regnskab kaldes typisk det "konsoliderede regnskab". Det konsoliderede regnskab er kun en beholder til de konsoliderede data og har ingen direkte forretningsdata. De regnskaber, du inkluderer i det konsoliderede regnskab, bliver **koncernvirksomheder** i rapporten.

Konsolidering af finansielle oplysninger kan især være relevant i forbindelse med interne processer. Du kan finde flere oplysninger i [Administrere interne transaktioner](intercompany-manage.md).

Du kan konsolidere:  

* På tværs af regnskaber med forskellige kontoplaner.  
* Regnskaber med forskellige regnskabsår og forskellige valutaer.  
* Enten det fulde beløb eller en procentdel af et regnskabs finansielle oplysninger
* Ved brug af forskellige valutakurser i de enkelte finanskonti

Afhængigt af kompleksiteten af virksomhederne kan rapporten konfigureres på to måder:

* Hvis du ikke har brug for avancerede indstillinger, f.eks. inklusion af et regnskab, som du kun er en del af, kan du bruge den assisterede opsætningsvejledning **Virksomhedskonsolidering** til hurtigt at oprette en konsolidering. Guiden hjælper dig gennem de grundlæggende trin.
* Hvis du har brug for mere avancerede indstillinger, kan du oprette det konsoliderede regnskab og koncernvirksomhederne selv.

## <a name="to-do-a-simple-consolidation-setup"></a>Sådan udfører du en simpel konsolideringsopsætning
Hvis din konsolidering er enkel, f.eks. fordi du er eneejer af de koncernvirksomheder, der skal konsolideres, hjælper den assisterede opsætningsvejledning **Virksomhedskonsolidering** dig gennem følgende trin:

* Vælg, om du vil oprette et nyt konsolideret regnskab, eller om du vil konsolidere data i et regnskab, som du allerede har oprettet til konsolideringen. Regnskabet må ikke indeholde transaktioner.
* Få vist resultaterne. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, at masterdata og transaktioner kan overføres til det konsoliderede regnskab.

Hvis du vil bruge den assisterede opsætningsvejledning, skal du gøre følgende:

1. I Rollecenteret **Bogholder** skal du vælge handlingen **Assisteret opsætning**.
2. Vælg **Konfigurer konsolideringsrapportering**, og udfør derefter de enkelte trin i den assisterede opsætningsvejledning.

## <a name="to-do-an-advanced-consolidation-setup"></a>Sådan konfigurerer du en avanceret konsolidering
Hvis du har brug for mere avancerede indstillinger til din konsolidering, kan du oprette konsolideringen manuelt. Hvis du f.eks. har virksomheder, som du kun ejer delvist, eller virksomheder, som du ikke vil have med i konsolideringen. Du opretter det konsoliderede regnskab på samme måde, som du opretter andre regnskaber. Du kan finde flere oplysninger under [Blive klar til at handle](ui-get-ready-business.md).  

[!INCLUDE[d365fin](includes/d365fin_md.md)] giver dig mulighed for at oprette en liste over regnskaber, der skal konsolideres, kontrollere regnskabsdataene, før du konsoliderer dem, importere filer og oprette konsolideringsrapporter.  

1. Log på det konsoliderede regnskab.
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Vælg **Ny**, og udfyld de påkrævede felter. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!IMPORTANT]
> Når du udfylder felterne **Startdato** og **Slutdato**, skal du kontrollere, at du overholder GAAP-regler for regnskabsperioderne for koncernvirksomheden kontra moderselskabet.

Hvis koncernvirksomheden bruger en fremmed valuta, skal du angive kursen, der skal anvendes i konsolideringen. Du skal også angive konsolideringsoplysninger om koncernvirksomhedens finanskonti. Disse processer beskrives i de følgende afsnit.

### <a name="to-prepare-general-ledger-accounts-for-consolidation"></a>Sådan klargøres finanskonti til konsolidering
Hvis kontoplanen i koncernvirksomheden er anderledes end det konsoliderede regnskab, skal du forberede finanskonti til konsolidering. Du kan angive de konti, hvor debet og kredit skal posteres, og metoden, der skal bruges til at oversætte valutaer i det konsoliderede regnskab. Det er f.eks. nyttigt, hvis du ofte udfører rapporten.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. Åbn kortet for kontoen, og udfyld derefter felterne på oversigtspanelet **Konsolidering**.

### <a name="to-specify-exchange-rates-for-consolidations"></a>Sådan angives kurser for konsolideringer
Hvis en koncernvirksomhed bruger en anden valuta end det konsoliderede regnskab, skal du angive valutakursmetoder for hver konto, før du konsoliderer. For hver konto bestemmer indholdet af feltet **Konsol. oversættelsesmetode** valutakursen. På hvert koncernvirksomhedskort angiver du i feltet **Valutakurstabel**, om konsolideringen skal bruge valutakurser fra koncernvirksomhedens regnskab eller det konsoliderede regnskab. Hvis du bruger valutakurser fra det konsoliderede regnskab, kan du ændre kurserne for en koncernvirksomhed. For koncernvirksomheder gælder: Hvis der i feltet **Valutakurstabel** på koncernvirksomhedskortet står **Lokal**, kan du ændre valutakursen fra koncernvirksomhedskortet. Valutakurserne kopieres fra tabellen **Valutakurs**, men du kan ændre dem inden kosolideringen.

I følgende tabel beskrives de valutakursmetoder, du kan bruge til konti.

|Valutakurs | Typisk anvendelse |
|---|---|
|Gennemsnitskurs (manuel) | Du kan manuelt beregne den gennemsnitlige kurs for konsolideringsperioden. Beregn enten gennemsnittet som et aritmetisk gennemsnit eller som et kvalificeret estimat, og angiv resultatet for hver koncernvirksomhed. Bruges til resultatopgørelseskonti.|
|Ultimokurs | Bruges til konti på balancen.|
|Sidste ultimokurs | Den gældende kurs på valutamarkedet på den dato, hvor balancen eller resultatopgørelsen udarbejdes. Angiv denne kurs for hver koncernvirksomhed. Bruges til konti på balancen.|
|Historisk kurs | Den valutakurs, der var gældende, da transaktionen fandt sted.|
|Sammensat kurs | Beløbene i den aktuelle periode oversættes til gennemsnitskursen og føjes til den tidligere registrerede balance i det konsoliderede regnskab. Denne metode bruges typisk til resultatkonti, fordi disse omfatter beløb overført fra forskellige perioder og derfor er sammensat af beløb, der er oversat med forskellige valutakurser.|
|Aktiekurs | Dette svarer til **sammensat**. Differencerne bogføres på separate finanskonti.|   

Gør følgende for at angive valutakurser for koncernvirksomheder:

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsenheder**, og vælg derefter det relaterede link.  
2. Vælg koncernvirksomheden på siden **Koncernvirksomhedsoversigt**, og vælg derefter handlingen **Gennemsnitskurs (manuel)**.   
3. På siden **Ret valutakurs** er indholdet af feltet **Associeret valutakurs** blevet kopieret fra tabellen **Valutakurs**, men du kan ændre oplysningerne efter behov. Luk siden.  
4. Vælg handlingen **Ultimokurs**.  
5. I feltet **Associeret valutakursbeløb** skal du angive valutakursen.

<!-- ### To include or exclude dimensions

COMMENTING THIS OUT BECAUSE i CANNOT REPRODUCE THE SETTINGS. tHERE IS NO CONSOLIDATION CODE FIELD ON DIMENSIONS OR DIMENSIOIN VALUES.

You can consolidate dimension information and general ledger accounts, as follows:

* To exclude dimension information in the consolidation, leave the **Consolidation Code** field blank, and do not choose dimensions in the **Copy Dimensions** fields in any consolidation functions or reports described later in this topic.
* To include dimension information in the consolidation, leave the **Consolidation Code** field blank. However, the consolidation will only work if the dimension values in the business unit are the same as the consolidated company.
* To consolidate the dimension value code in the business unit with a different dimension value code in the consolidated company, fill in the **Consolidation Code**. -->

### <a name="to-exclude-a-company-from-consolidation"></a>Sådan udelukkes en virksomhed fra konsolideringen
Hvis du ikke vil medtage en koncernvirksomhed i konsolideringen, kan du udelukke den. Gå til koncernvirksomhedskortet for at gøre dette, og fjern markeringen af afkrydsningsfeltet **Konsolideres**.

### <a name="to-include-a-partially-owned-company-in-consolidation"></a>Sådan inkluderes en delvis ejet virksomhed i konsolideringen
Hvis du kun ejer en del af en virksomhed, kan du medtage en procentdel af hver transaktion, der svarer til den procentdel af virksomheden, du ejer. Hvis du f.eks. ejer 70 % af virksomheden, inkluderer konsolideringen $70 af en faktura på $100. Du angiver den procentdel af virksomheden, du ejer, ved at gå til koncernvirksomhedskortet og angive procentdelen i feltet **Konsolideringspct.**.  

### <a name="to-test-the-data-before-you-consolidate"></a>Sådan kontrolleres dataene, før du konsoliderer
Du kan teste dataene, inden du overfører dem til det konsoliderede regnskab. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, om der er forskelle mellem oplysningerne i koncernvirksomhederne og den konsoliderede virksomhed. F.eks., om kontonumre eller dimensionskoder er anderledes. Du skal rette fejlene, før du kan køre rapporten. Du kan teste databasen, eller hvis du importerer data fra en XML-fil, kan du teste filen.   

1. Åbn det konsoliderede regnskab.  
2. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Forretningsenheder**, og vælg derefter det relaterede link.  
3. Gør ét af følgende:  

    * For at teste en fil, skal du vælge handlingen **Kontroller fil**, angive navnet på filen, der skal kontrollere, og derefter vælge **Udskriv**.  
    * Du kan teste databasen ved at vælge **Test database**.  

## <a name="to-run-the-consolidation"></a>Så køres konsolideringen
Når du har testet dataene, kan du overføre dem til det konsoliderede regnskab.  

1. Log på det konsoliderede regnskab.  
2. I **Rollecenteret Bogholder** skal du vælge handlingen **Kør konsolidering**.  
3. Udfyld de påkrævede felter.  
4. I feltet **Hvor** skal du vælge **Virksomhedsnavn** og derefter vælge det konsoliderede regnskab i feltet **er**.

## <a name="to-eliminate-repeated-transactions"></a>Sådan fjernes gentagne transaktioner
Når du har konsolideret alle regnskaber, skal du finde de transaktioner, som er registreret mere end én gang på tværs af regnskaber, og derefter bogføre elimineringsposter for at fjerne dem.

Behandling af konsolideringselimineringer er en manuel proces. Du kan følge disse trin:
1. Find transaktioner, det kan være nødvendigt at regulere, og angiv finanskladdelinjer for at fjerne disse.
2. Kør **G/L konsolideringselimineringer**-rapporten for at få hjælp til at vurdere virkningen af finanskladdelinjerne inden bogføringen.
3. Bogfør tilpasningsposteringerne.

Rapporten **G/L konsolideringselimineringer** indeholder en foreløbig råbalance, hvor du kan simulere konsekvenserne af en eliminering af posterne, ved at sammenligne posterne i koncernregnskabet med de elimineringer, der er indtastet i den finanskladde.

Hvis et koncernvirksomhedsregnskab skal indgå i rapporten, skal det først være oprettet på siden **Konsolider** i feltet **Koncernvirksomhed**.

Hver konto vises på en separat linje, rapporten følger kontoplanens opbygning. En konto vises ikke, hvis alle beløb på linjen er nul. Følgende oplysninger vises om hver konto:

* Kontonummer
* Kontonavn.
* Hvis du har valgt en eller flere koncernvirksomhedskoder i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for koncernregnskabet ekskl. de valgte koncernvirksomheder og elimineringer. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for koncernregnskabet ekskl. elimineringer.
* Hvis du har valgt en koncernvirksomhedskode i feltet **Konc.virksomhedskode** på anmodningssiden, vises totalen for de indlæste poster fra koncernvirksomheden. Hvis du ikke har udfyldt feltet **Konc.virksomhedskode**, vises totalen for de bogførte elimineringer i koncernregnskabet.
* Totalen for koncernregnskabet med alle koncernvirksomheder og alle bogførte elimineringer.
* De elimineringer, der skal foretages i koncernregnskabet, dvs. poster i den finanskladde, der er valgt på anmodningssiden.
* Bogføringsteksten kopieret fra finanskladden.
* Koncernregnskabets total efter elimineringerne, hvis de bogføres.


## <a name="to-export-and-import-consolidated-data-between-databases"></a>Sådan eksporterer og importerer du konsoliderede data mellem databaser
Hvis data for en koncernvirksomhed er placeret i en anden database, skal du eksportere dataene til en fil, før de kan medtages i konsolideringen. Regnskaberne skal udlæses separat. Til det formål bruges kørslen **Udlæs konsolideringsposter**.  

Når du kører batchjobbet, behandles alle poster i finanskonti. Indhold i felterne **Beløb** sammentælles og udlæses for hver kombination af valgte dimensioner og dato. Den næste kombination af valgte dimensioner og dato med samme kontonummer behandles, og derefter behandles kombinationerne i næste kontonummer osv.  

De udlæste poster indeholder følgende felter: **Kontonr.**, **Bogføringsdato** og **Beløb**. Hvis dimensionsoplysningerne også blev eksporteret, medtages dimensionskoderne og dimensionsværdierne også.  

1. For hver eksporteret linje, hvis summen af **Beløb**-felterne er et debetbeløb, eksporteres det kontonummer , der er oprettet i koncernvirksomhedens felt **Kons.debetkonto** til linjen. Hvis summen er et kreditbeløb, eksporteres det tilsvarende tal i feltet **Kons.kreditkonto** til linjen.  
2. Den dato, der bruges til de udlæste linjer er enten periodens slutdato, eller også er det den nøjagtige dato for beregningen, hvis overførslen finder sted pr. dag.  
3. Den dimensionsværdi, der blev udlæst for posten, vil blive det konsoliderede regnskabs dimensionsværdi, som er oprettet i feltet **Konsolideringskode** for dimensionsværdien. Hvis der ikke er blevet oprettet en dimensionsværdi for det konsoliderede regnskab i feltet **Konsolideringskode** for dimensionsværdien, vil selve dimensionsværdien blive udlæst til linjen.   
4. XML-filerne indeholder også valutakurserne i konsolideringsperioden. Disse kurser er inkluderet i en separat sektion øverst i filen.

## <a name="see-also"></a>Se også
[Administrere Intercompany-transaktioner (IC)](intercompany-manage.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Eksportere forretningsdata til Excel](about-export-data.md)
