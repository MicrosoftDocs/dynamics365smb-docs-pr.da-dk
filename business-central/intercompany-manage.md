---
title: Administrere Intercompany-transaktioner (IC)
description: Du kan forenkle forretningsgange og transaktioner mellem virksomheder i den samme organisation med Intercompany-funktionaliteten.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: 605
ms.date: 08/11/2021
ms.author: edupont
---
# Administrere Intercompany-transaktioner (IC)

IC-transaktioner er udviklet til de brugere, som styrer mere end én juridisk forretningsenhed, og som har oprettet flere virksomheder for at adskille regnskabsfunktionerne for hver af disse enheder. Denne brede beskrivelse gælder for mange brugere, især dem, som opererer på internationale markeder eller områder med meget forskelligartede forretningskulturer og regler og love.

Organisationen består muligvis af flere virksomheder, men har måske ikke det tilsvarende antal regnskabs- og administrationsgrupper. Med Intercompany-transaktioner kan du gøre forretningsgange og transaktioner mellem alle disse enheder lettere og mere strømlinede.

Når du er startet med at bruge Intercompany-transaktioner, vil det være lige så nemt at handle med datterselskaber og interne partnerorganisationer som med de eksterne leverandører og kunder. Du angiver kun oplysninger om intercompany-transaktioner én gang i de relevante bilag. Du kan bruge de funktioner, du allerede kender, f.eks. likviditetsstyring. Tilknytningsfunktioner i kontoplanerne og dimensioner er med til at sikre, at oplysningerne vises de rigtige steder.  

Der er fire overordnede formål med Intercompany-funktioner:  

- Øget produktivitet på grund af sparet tid og forenklede transaktioner  
- Mindsket risiko for fejl, fordi oplysninger kun skal angives én enkelt gang og automatiserede opdateringer på tværs af hele systemet  
- Komplet revisionssporing og fuld synlighed af forretningsaktiviteter og transaktionsoversigter  
- Effektive og besparende transaktioner med søster- og datterselskaber  

## Strømlining af afviklingen af forretningsaktiviteter  

Med Intercompany-transaktioner kan du distribuere salgs- og købsbilagene og finansposter til alle satellitkontorer, salgskontorer eller datterselskaber direkte i programmet. Du sparer tid og øger effektiviteten i hele organisationen, idet du fjerner overflødig dataangivelse og afsendelse, modtagelse, udskrivning og arkivering af salgs- og købsbilagene på papir.  

Du har den fulde kontrol over alle transaktionsbilag. Du kan f.eks. afvise et bilag, der er sendt til dig, og på denne måde tilbageføre kladdeposteringer og annullere forkerte modtagelser/leverancer. Eller når du foretager et køb fra en partner eller et datterselskab, kan du opdatere købsordren, så længe den sælgende virksomhed ikke har afsendt nogen varer.  

Når du angiver en transaktion, skal du ikke angive kontiene for et individuelt sæt af profiler, men blot oplyse partnervirksomhedens id. Intercompany-funktionen opretter finanslinjer, som resulterer i afstemning af profilerne i de to virksomheder, der er involveret i en transaktion. I tilgodehavender og skyldige beløb tildeler du en koncernintern partnerkode til alle kunder og leverandører. Fra det øjeblik af vil alle de ordrer og fakturaer, der oprettes på baggrund af transaktioner med disse virksomheder, resultere i tilsvarende bilag i partnervirksomheden, som igen resulterer i korrekt afstemning af kontiene.  

Funktionen Intercompany-transaktioner fokuserer på understøttelse af intercompany-transaktioner med salgs- og købsbilag og med finanslinjer. I dette modul gør Intercompany-transaktioner det muligt med intercompany-transaktioner mellem flere [!INCLUDE [prod_short](includes/prod_short.md)]-databaser. f.eks. i forskellige lande såvel som flere valutaer, forskellige kontoplaner, forskellige dimensioner og forskellige varenumre.  

I Intercompany-transaktioner bruges der en række poster og bilag ved intercompany-transaktioner:  

- Finansposter
- Købs- og salgsordrer
- Købs- og salgsfakturaer
- Kreditnotaer
- Returvareordrer

Når du konfigurerer Intercompany-transaktioner, opretter du en liste over intercompany-partnere, kaldet IC-partnere, og en intercompany-kontoplan. Hvis du følger disse trin, kan du udføre intercompany-finanskladdetransaktioner. Du opretter dimensioner separat, hvis der er behov for det.  

> [!NOTE]
> Bemærk, at finanskladden alene ikke omfatter valutafunktioner, men konverterer alle beløb med den gældende kurs til lokal valuta.

Når du har oprettet forretningspartnere som debitorer og kreditorer i systemet og tildelt dem Intercompany-partnerkoder, er det muligt at udveksle IC-købs- og salgsbilag, herunder varer og varegebyrer. [!INCLUDE [prod_short](includes/prod_short.md)] understøtter intercompany-transaktioner mellem flere databaser, f.eks. i forskellige lande/områder såvel som flere valutaer, forskellige kontoplaner, forskellige dimensioner og forskellige varenumre.  

> [!NOTE]
> Ikke alle typer data kan udveksles mellem virksomheder på denne måde. Købsfakturaer sendes ikke til forretningspartnere via interne processer. Men salgsfakturaer, der sendes via interne processer, oprettes som købsfakturaer i modtagelsesfirmaet.

Konsolidering af finansielle oplysninger kan især være relevant i forbindelse med interne processer. Du kan finde flere oplysninger i [Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|Hvis du vil |Skal du se|
|---|---|
|Opret koncerninterne kreditorer og debitorer som såkaldte koncerninterne partnere, og konfigurer en koncernintern (IC) kontoplan.|[Konfigurere mellemregning](intercompany-how-setup.md)|
|Bruge IC-dokumenter eller -kladder til at bogføre transaktioner med koncerninterne partnere.|[Arbejde med koncerninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)|
|Organisere og behandle indgående og udgående transaktioner, som du udveksler med dine koncerninterne partnere.|[Administrere IC-indbakken og -udbakken](intercompany-how-manage-intercompany-inbox.md)|
|Brug IC-transaktioner til at fordele omkostninger mellem partnerfirmaer.|[Allokere omkostninger til IC-partnere](intercompany-allocate-costs.md)|

## Se også

[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
