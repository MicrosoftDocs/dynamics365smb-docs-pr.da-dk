---
title: Opsætte e-dokumenter
description: 'Få mere at vide om, hvordan du konfigurerer funktionaliteten for e-dokumenter.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, electronic invoice, e-document, e-invoice'
ms.search.form: '359, 360, 6103, 6133'
ms.date: 10/05/2023
ms.author: altotovi
---

# Opsætte e-dokumenter

> [!IMPORTANT]
> E-dokumenters kernemodul er en ramme. Der er som standard ikke noget felt til **Tjenesteintegration**. Hvis du finder **Dokumentformat** indstillingerne som standard, skal du være opmærksom på, at de tilbydes som et eksempel, og at lokalisering skal give et detaljeret format. Disse oplysninger er en del af lokaliseringsapps, fordi de er specifikke for lokale krav.

> [!NOTE]
> Fra version 23.2 tilføjes et PEPPOL-standarddokumentformat som et globalt format i feltet **Dokumentformat**. Husk, at du sandsynligvis ikke kan bruge dette format, som det er. Det er et W1-format, der leveres for at vise, hvordan man bruger denne funktion. Vi anbefaler, at du tester det eksisterende PEPPOL-format, før du begynder at bruge dette format.

Det første trin i konfigurationen af elektroniske dokumenter (e-dokumenter) er at konfigurere tjenesten E-dokumenter, hvor du konfigurerer hele systemets funktionsmåde i forbindelse med e-dokumentkommunikation.

## Konfigurere tjenesten til e-dokument

Følg disse trin for at konfigurere e-dokumenttjenesten.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **e-dokumenttjeneste**, og vælg derefter det relaterede link.
2. Vælg **Ny**, og konfigurer derefter felterne i oversigtspanelet **Generelt** på siden **E-dokumenttjeneste** som beskrevet i følgende tabel.

    | Felt | Beskrivelse |
    |-------|-------------|
    | Kode | Vælg opsætningskoden for elektronisk eksport. |
    | Beskrivelse | Angiv en kort beskrivelse af opsætningen af den elektroniske eksport. |
    | Dokumentformat | <p>Eksportformatet for opsætningen af den elektroniske eksport.</p><p>Der er som standard to indstillinger i dette felt. Du kan vælge **PEPPOL BIS 3** som et generisk kodebaseret format eller **Data Exchange** når du skal konfigurere pre-dokumenter af specifikke formater på oversigtspanelet **Data Exchange Definition**.</p> |
    | Serviceintegration | Vælg integrationskode for opsætningen af elektronisk eksport. I bølge 1 er den eneste mulighed **Ingen integration**. |
    | Brug batchbehandling | Angiv, om tjenesten bruger batchbehandling til eksport. |

3. På oversigtspanelet **Importerede parametre** skal du udfylde felterne som beskrevet i følgende tabel.

    | Felt | Beskrivelse |
    |-------|-------------|
    | Valider modtagende virksomhed | Angiv, om modtagende virksomhedsoplysninger skal valideres under indlæsning. |
    | Løs enhed | Angiv, om enheden skal løses under indlæsning. |
    | Opslagsvarereference | Angiv, om der skal søges efter en vare efter varereferencen under indlæsning. |
    | Slå GTIN for vare op | Angiv, om der skal søges efter en vare efter GTIN (Global Trade Item Number) under indlæsning. |
    | Slå kontotilknytning op | Angiv, om der skal søges i en konto i **kontotilknytning** efter den indgående tekst under indlæsning. |
    | Godkend linjerabat | Angiv, om en linjerabat skal valideres under indlæsning. |
    | Anvend fakturarabat | Angiv, om der skal anvendes en fakturarabat under indlæsning. |
    | Bekræft totaler | Angiv, om der skal anvendes en fakturarabat under indlæsning. |
    | Opdater ordre | Angiv, om den tilsvarende købsordre skal opdateres. |
    | Opret kladdelinjer | Angiv, om der skal oprettes kladdelinje i stedet for købsdokument. Vælg denne indstilling, hvis du vil bruge kladder som destination for dine fakturaer. |
    | Finanskladdetypenavn | Angiv navnet på finanskladdeskabelonen, der bruges til oprettelse af kladdelinjer. Feltet kan anvendes, hvis du vil bruge kladder som destination for dine fakturaer. |
    | Finanskladdenavn | Angiv navnet på den finanskladdebatch, der bruges til oprettelse af kladdelinjer. Feltet kan anvendes, hvis du vil bruge kladder som destination for dine fakturaer. |
    | Automatisk indlæsning | Angiv, om dokumenter skal indlæses automatisk fra tjenesten. |
    | Batchens starttidspunkt | Angiv starttidspunktet for importsager. |
    | Minutter mellem kørsler | Angiv antallet af minutter mellem kørsel af indlæsningsjobs. |

4. Hvis du valgte **Dataudveksling** i feltet **Dokumentformat** på oversigtspanelet **Generelt**, brug **Dataudvekslingsdefinitionen**-oversigtspanelet til at indstille følgende felter.

    | Felt | Beskrivelse |
    |-------|-------------|
    | Dokumenttype | Angiv den dokumenttype, der bruger dataudveksling til import og eksport af dataene. Eksempler omfatter **salgsfaktura**, **salgskreditnota** og **Købsfaktura**. |
    | Definitionskode for indlæsning af dataudveksling | Angiv den dataudvekslingskode, der bruges til import af dataene. Brug kun dette felt til at modtage et dokument i købsprocessen. |
    | Definitionskode for udlæsning af dataudveksling | Angiv den dataudvekslingskode, der bruges til eksport af dataene. Brug kun dette felt til at levere dokumenter i salgsprocessen. |

> [!NOTE]
> Der er udarbejdet dataudvekslingsdefinitioner for PEPPOL-formatet, der er relateret til standard salgs- og købsdokumentet. Du kan dog sandsynligvis ikke bruge disse definitioner, som de er. De er alle W1-formater, der leveres for at vise, hvordan man bruger denne funktion. Vi anbefaler, at du tester det eksisterende PEPPOL-format, før du begynder at bruge dem.

Hvis du har konfigureret formatet **Data Exchange Definition** i lokaliseringen, kan du tilføje en linje for hver dokumenttype, du har brug for. Tilføj linjer, der matcher standarddataudvekslingseksemplet for W1 PEPPOL-formatet. Du skal først vælge indstillingen **Dokumenttype** for hver linje, du har brug for. For hver datatype skal du vælge værdien **Import Data Exchange Def. Code** eller **Export Data Exchange Def. Code**, som du vil bruge.

Hvis du ikke bruger **Data Exchange Definition**-formatet, kan du oprette og konfigurere formater ved at bruge [grænsefladen](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments). Juster oplysningerne på linjerne **Eksportér kortlægning** og **Importér kortlægning**, hvor du kan finde de tabeller og felter, der skal konfigureres transformationsregler. I dette tilfælde skal du tilføje en ny mulighed i feltet **Dokumentformat**, der er relateret til dit format.  

### Understøttede dokumenttyper 

Understøttede dokumenttyper er baseret på det valgte **dokumentformat**. For at kontrollere, hvilke dokumenttyper der understøttes, skal du på **E-Document Service** siden køre handlingen **Understøttede dokumenttyper** . **E-Document Service Understøttede kildedokumenttyper** åbner, og i kolonnen **Kildedokumenttype** kan du finde alle de understøttede dokumenttyper.  

## Konfigurere dokumentafsendelsesprofil

Du kan konfigurere en foretrukken metode til afsendelse af salgsdokumenter for hver debitor. På denne måde behøver du ikke at vælge en afsendelsesindstilling, hver gang du vælger handlingen **Bogfør og send**. På siden **Profiler for afsendelse af dokumenter** kan du oprette forskellige afsendelsesprofiler, som du kan vælge i feltet **Dokumentafsendelsesprofil** på et debitorkort. Du kan markere afkrydsningsfeltet **Standard** for at angive, at dokumentafsendelsesprofilen er standardprofilen for alle debitorer, bortset fra debitorer, hvor feltet **Dokumentafsendelsesprofil** er udfyldt med en anden afsendelsesprofil.

Denne funktion bruges til at konfigurere automatisering af elektronisk fakturering. Når du vælger **Bogfør og send** i et salgsdokument, viser dialogboksen **Bekræftelse af bogfør og send** den afsendelsesprofil, der bruges, enten den, der er konfigureret for kunden, eller standard for alle debitorer.

Følg disse trin for at oprette en dokumentafsendelsesprofil.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Dokumentafsendelsesprofil**, og vælg derefter det relaterede link.
2. På siden **Dokumentafsendelsesprofil** skal du vælge **Ny**.
3. I oversigtspanelet **Generelt** skal du vælge eller angive feltoplysninger efter behov.
4. I oversigtspanelet **Sendeindstillinger** skal du konfigurere felterne som beskrevet i følgende tabel.

    | Felt | Beskrivelse |
    |-------|-------------|
    | Elektronisk dokument | Angiv, om dokumentet sendes som et e-dokument, som kunden kan importere i sit system, når du vælger **Bogfør og send**. Hvis du vil bruge denne indstilling, skal du også angive feltet **Format** eller **Elektronisk serviceflowkode for elektroniske dokumenter**. Du kan også gemme filen på harddisken. |
    | Format | Angiv det format, der skal bruges til at sende et e-dokument. Dette felt skal bruges, hvis du vælger **Via dokumentudveksling** i feltet **Elektronisk dokument**. |
    | Flowkode for elektronisk dokumenttjeneste | Angiv det elektroniske tjenesteflow, der bruges til afsendelse af dokumenter. Dette felt skal bruges, hvis du vælger **Udvidet e-dokumenttjenesteflow** i feltet **Elektronisk dokument**. |

    > [!NOTE]
    > Hvis du vælger **Udvidet e-dokumentserviceflow i** feltet **Elektronisk dokument** , skal arbejdsprocessen allerede være konfigureret for dine e-dokumenter.

## Konfigurere workflowet

Følg disse trin for at konfigurere det workflow, der bruges i e-dokumentfunktionalitet.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Word-skabeloner**, og vælg derefter det relaterede link.
2. Hvis du ikke kan finde **Skabeloner til e-dokumentworkflow** på siden **Arbejdsprocesskabeloner**, skal du vælge **Nulstil Microsoft-skabeloner**. Derefter vises **skabeloner til e-dokumentarbejdsgange**. Luk siden.
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Workflows**, og vælg derefter det relaterede link.
4. Kør handlingen **Nyt workflow fra skabelon** for at vælge en skabelon til e-dokumentprocessen. De tilgængelige skabeloner er **Send til én tjeneste** og **Send til flere tjenester**.
5. Vælg **OK** for at fuldføre opsætningen af workflowet.
6. I feltet **Derefter svar** skal du vælge **Send e-dokument ved hjælp af opsætning** for at konfigurere arbejdsgangssvarene.
7. Vælg den E-dokumenttjeneste, du har oprettet, som en indstilling, vælg **OK,** og aktivér derefter arbejdsgangen.

> [!NOTE]
> Du kan oprette din egen arbejdsgang til e-dokumenter uden at bruge foruddefinerede arbejdsgangsskabeloner. Hvis du har flere tjenester, kan du bruge forskellige arbejdsgange.

For at bruge flere arbejdsgange skal du konfigurere dem gennem dokumentafsendelsesprofilerne for forskellige kunder. Når du konfigurerer arbejdsgangen, skal du angive dokumentafsendelsesprofilen i kolonnen **On Condition** på oversigtspanelet **Workflow Steps**, fordi du ikke kan have to tjenester, der bruger den samme dokumentafsendelsesprofil i arbejdsgange.

Når du konfigurerer dit workflow på **Workflow** siden, skal du pege på feltet **On Condition** på oversigtspanelet **Workflow-trin**. På siden **Begivenhedsbetingelser** i feltet **Filter** skal du vælge den dokumentafsendelsesprofil, du vil bruge.

## Oprette en opbevaringspolitik for e-dokumenter

E-dokumenter kan være omfattet af forskellige lokale lovgivninger, der er relateret til den periode, hvor e-dokumenterne opbevares. Derfor har vi tilføjet en opsætning af opbevaringspolitik for alle vigtige oplysninger, der er relateret til e-dokumenter. Administratorer kan definere opbevaringspolitikker, der angiver, hvor ofte Dynamics 365 Business Central forældede poster, der er relateret til e-dokumenter, slettes. Du kan få mere at vide om opbevaringspolitikker i [Definere opbevaringspolitikker](admin-data-retention-policies.md).

Følg disse trin for at konfigurere opbevaringspolitikker relateret til e-dokumenter.

1. På siden **E-dokumenttjenester** skal du køre handlingen **Opbevaringspolitik**.
2. Når handlingen er fuldført, skal du vælge en af følgende opbevaringspolitikker, der skal konfigureres:

    - Log over e-dokument
    - Log over integration af e-dokumenter
    - Log over tilknytning af e-dokument
    - Lagring af e-dokumentdata

## Se også

[Sådan bruges e-dokumenter i Business Central](finance-how-use-edocuments.md)  
[Sådan udvides e-dokumenter i Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-extend-edocuments)  
[Økonomistyring](finance.md)  
[Fakturasalg](sales-how-invoice-sales.md)  
[Registrere køb med købsfakturaer og ordrer](purchasing-how-record-purchases.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
