---
title: Administrere Intercompany-transaktioner (IC)
description: Du kan forenkle forretningsgange og transaktioner mellem virksomheder i den samme organisation med Intercompany-funktionaliteten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: conceptual
ms.date: 02/06/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605,'
---
# <a name="managing-intercompany-transactions" />Administrere Intercompany-transaktioner (IC)

Virksomheder med mere end én juridisk enhed med separate regnskabsfunktioner kan drage fordel af IC-transaktioner. Det er f. eks. nyttigt for virksomheder med datterselskaber på flere internationale markeder eller områder. eller en organisation kan muligvis bestå af flere virksomheder, men har måske ikke det tilsvarende antal regnskabs- og administrationsgrupper. Med Intercompany-transaktioner kan du gøre forretningsgange og transaktioner mellem firmaer i koncernintern partnere.

Når du har angivet debitor-og kreditor relationerne for IC-transaktioner, skal partnere angive oplysningerne én gang i salgs- og købsdokumenter. Et tilsvarende dokument oprettes hos den anden partner, der er involveret i transaktionen. Tilknytningsfunktioner i kontoplanerne og dimensioner er med til at sikre, at oplysningerne vises de rigtige steder.  

Der er fire overordnede formål med intercompany-funktioner:  

* Øget produktivitet på grund af sparet tid og forenklede transaktioner  
* Færre fejl, fordi oplysninger kun skal angives én enkelt gang og automatiserede opdateringer på tværs af hele systemet  
* Komplet revisionssporing og fuld synlighed af forretningsaktiviteter og transaktionsoversigter  
* Effektive og besparende transaktioner med søster- og datterselskaber  

## <a name="streamline-the-flow-of-business-activities" />Strømlining flowet af forretningsaktiviteter

Med intercompany-transaktioner kan du distribuere salgs- og købsbilagene og finansposter til alle satellitkontorer, salgskontorer eller datterselskaber direkte i programmet. Distribuere transaktioner sparer tid og øger effektiviteten i hele virksomheden ved at reducere dataindtastning. Den nedskærer behovet for at sende, modtage, udskrive og arkivere salgs-og købsdokumenter.  

Du har den fulde kontrol over alle transaktionsbilag. Du kan f.eks. afvise et bilag, der er sendt til dig, og på denne måde **Tilbageføre kladdeposteringer** og **Annullere modtagelser/leverancer** for at foretage rettelser. Eller når du foretager et køb fra en partner eller et datterselskab, kan du opdatere købsordren, så længe den sælgende virksomhed ikke har afsendt nogen varer.  

Når du angiver en transaktion, behøver du ikke at angive, hvilke konti der skal bruges. Du skal blot vælge IC-partneren. Intercompany-funktionen opretter finanslinjer, som resulterer i afstemning af profilerne i de to virksomheder, der er involveret i en transaktion. I tilgodehavender og skyldige beløb tildeler du en koncernintern partnerkode til alle kunder og leverandører. Fra det tidspunkt, hvor alle ordrer og fakturaer til transaktioner mellem disse firmaer fremstiller tilsvarende dokumenter i partnervirksomheden. Resultatet er korrekt afstemt konto.  

Interne fokuseringer fokuserer på salgs-og købsdokumenter og generelle kladdelinjer og tillader transaktioner mellem flere [!INCLUDE [prod_short](includes/prod_short.md)]- databaser. Eksempler:

* I forskellige lande/områder
* Flere valutaer
* Forskellige kontoplaner
* Forskellige dimensioner
* Forskellige varenumre  

Intercompany-transaktioner bruger flere typer poster og dokumenter:  

* Finansposter
* Købs- og salgsordrer
* Købs- og salgsfakturaer
* Kreditnotaer
* Returvareordrer

Når du konfigurerer Intercompany-transaktioner, opretter du en liste over intercompany-partnere, kaldet IC-partnere, og en intercompany-kontoplan. Derefter kan du oprette transaktioner i IC-finanskladder.

> [!NOTE]
> Finanskladden indeholder heller ikke valutaer. Alle beløb omregnes til den lokale valuta ved den aktuelle valutakurs.

Når du har oprettet forretningspartnere som debitorer og kreditorer i systemet og tildelt dem Intercompany-partnerkoder, er det muligt at udveksle IC-købs- og salgsbilag, herunder varer og varegebyrer. 

> [!NOTE]
> Virksomheder kan ikke bruge intern til at udveksle alle typer data. Købsfakturaer sendes ikke til forretningspartnere via interne processer. Men salgsfakturaer, der sendes via interne processer, oprettes som købsfakturaer i modtagelsesfirmaet.

Konsolidering af finansielle oplysninger kan især være relevant i forbindelse med interne processer. Du kan finde flere oplysninger i [Konsolidering af finansielle oplysninger fra flere regnskaber](finance-consolidated-company-reporting.md).

Den følgende tabel indeholder en opgavesekvens med links til de artikler, der rummer beskrivelserne af opgaverne.

|Til |Skal du se|
|---|---|
|Opret koncerninterne kreditorer og debitorer som såkaldte koncerninterne partnere, og konfigurer en koncernintern (IC) kontoplan.|[Konfigurere mellemregning](intercompany-how-setup.md)|
|Bruge IC-dokumenter eller -kladder til at bogføre transaktioner med koncerninterne partnere.|[Arbejde med koncerninterne dokumenter og kladder](intercompany-how-work-documents-journals.md)|
|Organisere og behandle indgående og udgående transaktioner, som du udveksler med dine koncerninterne partnere.|[Administrere IC-indbakken og -udbakken](intercompany-how-manage-intercompany-inbox.md)|
|Brug IC-transaktioner til at fordele omkostninger mellem partnerfirmaer.|[Allokere omkostninger til IC-partnere](intercompany-allocate-costs.md)|

## <a name="see-also" />Se også

[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
