---
title: Opsætte merværdiafgift (moms)
description: 'Sørg for at beregne, bogføre og rapportere moms på køb og salg korrekt. Du anbefales at bruge den assisterede opsætningsvejledning, når du konfigurerer moms.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 08/12/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Opsætte beregnings- og bogføringsmetoder for moms

Forbrugere og virksomheder betaler moms, når de køber varer eller tjenesteydelser. Momsbeløbet, der skal betales, kan variere afhængigt af flere faktorer. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerer du moms til at angive de satser, der bruges til at beregne momsbeløb baseret på følgende parametre:

* Hvem du sælger til  
* Hvem du køber fra  
* Hvad du sælger  
* Hvad du køber.  

Du kan konfigurere momsberegninger manuelt, men der kan være svært og tidskrævende. Det er nemt at bruge forskellige momssatser utilsigtet og gøre rapporter vedrørende moms unøjagtige. Vi anbefaler at bruge den assisterede vejledning **Momsopsætning**, når du konfigurerer moms.

Hvis du selv vil konfigurere momsberegninger eller bare vil vide mere om de enkelte trin, indeholder i denne artikel beskrivelser af de enkelte trin.  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Konfigurer moms ved hjælp af den assisterede momsopsætningsvejledning (anbefales)

> [!NOTE]
> Du kan kun bruge **Momsopsætningsvejledning**, hvis du har oprettet *Min virksomhed* og endnu ikke har bogført transaktioner, der omfatter moms. Du kan få mere at vide Min virksomhed ved at gå til [Oprette nye virksomheder i [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).

For at starte vejledningen skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Assisteret opsætning**. 
2. Vælg **Konfigurer moms**, og fuldfør trinnene.
3. Når du har afsluttet den assisterede opsætning, skal du gå til siden **Momsbogf.opsætning** og kontrollere, om du er nødt til at udfylde flere felter i henhold til de landespecifikke krav for din version af [!INCLUDE [prod_short](includes/prod_short.md)]. Flere oplysninger i [Lokal funktionalitet i Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Kontrollere momsbogføringsopsætningen

For at understøtte dig i hurtig start viser [!INCLUDE [prod_short](includes/prod_short.md)] notifikationer, hvis du mangler finanskonti i bogføringsgrupper eller bogføringsopsætninger, f. eks siden **Momsbogføringsopsætning**. Du kan skifte denne type notifikation til eller fra ved hjælp af **finanskonti, der mangler i bogføringsgruppe eller installationsmeddelelse** på siden **Mine notifikationer**. Gå til siden **Mine indstillinger**, og vælg linket **Ændr, når jeg modtager notifikationer**.  

Hvis du vælger notifikationen, opretter [!INCLUDE [prod_short](includes/prod_short.md)] automatisk disse bogføringsopsætninger på basis af bogføringsgrupperne i det dokument eller den kladde, du arbejder på.  

På dette tidspunkt kan du nøjes med at udfylde de manglende finanskonti. Når du senere indsnævrer din installation yderligere, kan du muligvis se, at din første installation er forkert. [!INCLUDE [prod_short](includes/prod_short.md)] tillader ikke, at du sletter momsbogføringsopsætningen og bogføringsopsætningen, efter at de er brugt til at oprette poster. Hvis du vil forhindre, at brugere kommer til at følge med en opsætning, der ikke længere er relevant for nye posteringer, kan du bruge feltet **Spærret** på siden **Bogføringsopsætning**.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Oprette en standardmomsdato for dokumenter og kladder

Momsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] er baseret på **momsdatoen** for at medtage momsposter i momsrapporter i en momsperiode. Momsdatoen kan ændres på alle dokumenter og kladder, men du skal angive en standardværdi for momsdatoen.

> [!NOTE]
> Efter bogføring af dokumentet eller kladden, vises **momsdatoen** på **momsposter** og **finansposter** samt på det bogførte dokument, hvis det findes.

Benyt følgende fremgangsmåde for at angive en standardværdi for en momsdato:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Generelt** i feltet **Standardmomsdato** skal du vælge **Bogføringsdato** eller **Bilagsdato**.
3. Luk siden.  

> [!NOTE]
> Som standard er **standardmomsdatoen** **bogføringsdatoen**.

### <a name="enable-or-disable-the-vat-date-feature"></a>Aktivere eller deaktivere funktionen Momsdato

Nogle lande/områder kræver, at virksomheder bruger en bestemt momsdato, men andre lande/områder ikke. Nogle lande/områder kræver også, at virksomheder ændrer momsdatoen i bestemte situationer, efter at de bogfører bilag, men andre lande/områder tillader ikke ændringer af momsdatoer. Hvis du vil tillade forskellige kontekster, kan du vælge, om du vil bruge denne funktion, f. eks. i hvilken grad.

Benyt følgende fremgangsmåde for at angive niveauet for brug af momsdato:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Generelt** i feltet **momsdatoforbrug** skal du angive, i hvilket omfang funktionen momsdato skal anvendes. Du kan vælge en af disse indstillinger:

   | Type | Beskrivlse |
   |--------------------|-----------------------------------------|
   | **Brug funktionaliteten til momskorrektionsdato** | Alt, der er relateret til **momsdato** fungerer som standard med den maksimale **momsdato**-funktionalitet. Du kan angive datoen, ændre den i bilag, rapportere på grundlag af den og ændre datoen efter bogføringen, så længe perioden ikke er lukket eller beskyttet med tilladte datoer for bogføring. |
   | **Anvend men tillad ikke ændringer** | Alt, der er relateret til **momsdatoen** fungerer som standard med én undtagelse. Du kan ikke ændre **momsdatoen** i **momsposter**. |
   | **Brug ikke momsdatofunktionalitet** | [!INCLUDE [prod_short](includes/prod_short.md)] skjuler og gør **momsdato**-felterne ikke tilgængelige for dokumenter, kladder og poster. **Standard momsdato** vil blive konfigureret som **Bogføringsdato**. |

3. Luk siden.

> [!IMPORTANT]
> Selvom du vælger indstillingen **Brug ikke momsdatofunktionen**, bruger [!INCLUDE [prod_short](includes/prod_short.md)] **momsdatoen** i baggrunden. Når **Standardmomsdatoen** er konfigureret som **Bogføringsdato**, og du kan ikke ændre den i så fald får du samme oplevelse som uden denne funktion. **Momsdato** felter fjernes fra alle sider, men dette felt findes stadig i tabeller og rapporter fungerer på baggrund af det.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Begrænse perioder til bogføring og ændring af momsdatoen

Du kan forhindre, at personer bogfører eller ændrer momsposter inden for bestemte datointervaller. Du kan angive begrænsningen ved hjælp af to indstillinger:

* Baseret på lukket **moms-returperiode**
* Baseret på felterne **Tillad bogføring fra** og **Bogføring tilladt til**.

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Sådan begrænses bogføringen på basis af momsreturperiode

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Generelt** i feltet **Kontrol af momsperiode** skal du angive kontrol af momsreturperiode. Den følgende tabel beskriver indstillingerne.

| Type | Beskrivlse |
|--------------------|-----------------------------------------|
| **Spær bogføring i lukket periode, og advar om frigivet periode** | Forhindre, at personer bogfører et dokument eller en kladde eller ændrer momsposter, der har en moms dato inden for en afsluttet **momsreturperiode**. [!INCLUDE [prod_short](includes/prod_short.md)] viser også en advarsel, hvis **momsangivelsesperioden** er åben, men status for **momsretur** er **frigivet** eller **indsendt**. |
| **Spær bogføring i lukket periode** | Forhindre, at personer bogfører et dokument eller en kladde eller ændrer momsposter, der har en moms dato inden for en afsluttet **momsreturperiode**. |
| **Advar ved bogføring i lukket periode** | Vis en advarsel, men blokér ikke bogføring, hvis du vil bogføre et dokument eller en kladde, der har en moms dato inden for en afsluttet **momsreturperiode**. |
| **Deaktiveret** | Foretag ingen handlinger på basis af en afsluttet **momsreturperiode**. |

#### <a name="limit-posting-based-on-allow-fromto-period"></a>Begrænsning af bogføring baseret på Tillad fra/til periode

> [!NOTE]
> Fra og med Business Central version 23.1 ændres dette kontrolelement. I tidligere versioner var der kun ét kontrolelement på siden **Regnskabsopsætning** for både bogføringsdato og momsdato. Nu er disse kontrolelementer opdelt, så kontrolelementet på siden **Regnskabsopsætning** kun gælder **bogføringsdatoen**, og kontrolelementet **Momsopsætning** på siden kun er for **momsdatoen**. Der er også nye datokontroller på siden **Brugeropsætning**.  

##### <a name="version-231-or-newer"></a>Version 23.1 eller nyere

> [!IMPORTANT]
> Når du opgraderer til en ny version, skal du være opmærksom på, at værdierne opgraderes i den nye **Tillad momsdato fra/til** på siden **Momsopsætning** baseret på værdierne i **Tillad bogføring Fra/Til** i **Regnskabsopsætning**. Hvis du vil bruge forskellige datokontroller, skal du åbne siden **Momsopsætning** og foretage ændringer.  

Du kan angive begrænsning for firmaet eller bestemte brugerniveauer.

Sådan begrænses alle bogføringer for hele virksomheden:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Konfiguration af VAT** og vælg derefter det relaterede link.  
2. Angiv den momsdato, du tillader bogføring fra, i feltet **Tillad momsdato fra** i oversigtspanelet **Momsdato**. Bogføring af et dokument eller en kladde med en momsdato før denne dato er ikke tilladt.  
3. Angiv den momsdato, hvortil du tillader bogføring, i feltet **Tillad momsdato til** i oversigtspanelet **Momsdato**. Bogføring af et dokument eller en kladde med en momsdato efter denne dato er ikke tilladt. 

Sådan begrænses bogføring for en bestemt bruger:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. I feltet **bruger-id** skal du angive den bruger, der kan tillades i en bestemt periode.  
3. Angiv den momsdato, du tillader bogføring fra, i feltet **Tillad momsdato fra**. Bogføring af et dokument eller en kladde med en momsdato før denne dato er ikke tilladt. 
4. Angiv den momsdato, du tillader bogføring indtil, i feltet **Tillad momsdato til**. Bogføring af et dokument eller en kladde med en momsdato efter denne dato er ikke tilladt.  

##### <a name="versions-before-231"></a>Versioner før 23.1

Du kan angive begrænsning for firmaet eller bestemte brugerniveauer.

Sådan begrænses alle bogføringer for hele virksomheden:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. Angiv den momsdato, du tillader bogføring fra, i feltet **Tillad bogføring fra** i oversigtspanelet **Generelt**. Bogføring af et dokument eller en kladde med en momsdato før denne dato er ikke tilladt.  
3. Angiv den momsdato, du tillader bogføring indtil, i feltet **Tillad bogføring til** i oversigtspanelet **Generelt**. Bogføring af et dokument eller en kladde med en momsdato efter denne dato er ikke tilladt.

Sådan begrænses bogføring for en bestemt bruger:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Brugeropsætning**, og vælg derefter det relaterede link.  
2. I feltet **bruger-id** skal du angive den bruger, der kan tillades i en bestemt periode.  
3. Angiv den momsdato, du tillader bogføring fra, i feltet **Tillad bogføring fra**. Bogføring af et dokument eller en kladde med en momsdato før denne dato er ikke tilladt.
4. Angiv den momsdato, du tillader bogføring indtil, i feltet **Tillad bogføring til**. Bogføring af et dokument eller en kladde med en momsdato efter denne dato er ikke tilladt.

## <a name="set-up-vat-registration-numbers-for-your-countryregion"></a>Konfigurere momsregistreringsnumre for dit land/område

For at sikre, at brugere angiver gyldige momsregistreringsnumre, kan du definere formater til momsregistreringsnumre, som bruges i de lande/områder, hvor du handler. [!INCLUDE[prod_short](includes/prod_short.md)] viser en fejlmeddelelse, hvis en bruger laver en fejl eller bruger et format, der er forkert for land/område.

For at opsætte momsregistreringsnumre, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lande/områder**.
2. Vælg landet eller området, og vælg derefter handlingen **SE/CVR-nr.formater**.
3. I feltet **Formater** skal du angive formatet ved at angive et eller flere af følgende tegn:  

* **#** Kræver et etcifret tal.  
* **@** Kræver et bogstav. Dette format skelner ikke mellem store og små bogstaver.  
* **?** Tillader alle tegn.  

    > [!TIP]
    > Du kan bruge andre tegn, så længe de er altid findes i formatet for landet eller området. Hvis du f.eks. vil medtage et punktum eller en bindestreg mellem sæt af tal, kan du angive formatet som ##.####.### or @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Konfigurere momsvirksomhedsbogføringsgrupper

Formålet med momsvirksomhedsbogføringsgrupper er at repræsentere de markeder, hvor du handler med debitorer og kreditorer, og definere, hvordan moms beregnes og bogføres på hvert enkelt marked. Eksempler på momsvirksomhedsbogføringsgrupper er **Danmark** og **Den Europæiske Union (EU)**.  

Brug koder, der er lette at huske, og som beskriver virksomhedsbogføringsgruppen, f.eks. **EU**, **Ikke-EU** eller **Danmark**. Hver kode skal være unik, så du kan oprette lige så mange koder, som du har brug for, men du kan kun bruge den samme kode én gang i en tabel.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsvirksomhedsbogf.grupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

Du kan oprette standardmomsvirksomhedsbogføringsgrupper ved at linke dem til virksomhedsbogføringsgrupper. [!INCLUDE[prod_short](includes/prod_short.md)] tildeler automatisk momsvirksomhedsbogføringsgruppen, når du tildeler virksomhedsbogføringsgruppen til en debitor, kreditor eller finanskonto.

## <a name="set-up-vat-product-posting-groups"></a>Konfigurere momsproduktbogføringsgrupper

Momsproduktbogføringsgrupper repræsenterer de varer eller ressourcer, du køber eller sælger, og bestemmer, hvordan moms beregnes og bogføres i overensstemmelse med typen af vare eller ressource.

Det anbefales at bruge koder, der er lette at huske, og som beskriver satsen, som f.eks. **FRITAGET** eller **Nul**, **MOMS10** eller **Reduceret** for 10 procent moms og **MOMS25** eller **Standard** for 25 procent.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinere momsbogføringsgrupper i momsbogføringsopsætninger

[!INCLUDE[prod_short](includes/prod_short.md)] beregner momsbeløb af køb og salg baseret på momsbogføringsgrupper, der er kombinationer af momsvirksomheds- og -produktbogføringsgrupper. For hver kombination kan du angive momsprocenten, momsberegningstypen og finanskontonumre for bogføring af købs-, salgs- og modtagermoms. Du kan også angive, om moms skal genberegnes, når en kontantrabat anvendes eller modtages.  

Du kan definere et ubegrænset antal kombinationer. Hvis du vil gruppere kombinationer af momsbogføringsopsætninger med lignende attributter, kan du angive et **Moms-id** for hver enkelt gruppe og tildele id'et til gruppemedlemmerne.  

> [!NOTE]
> A **momsidentifikator** er en kode, du kan bruge til at gruppere lignende attributter. Vi anbefaler, at du bruger forskellige momskoder til forskellige momsprocenter.  

Hvis du vil kombinere momsbogføringsopsætninger, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 5.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tildele momsbogføringsgrupper til flere enheder som standard

Hvis du vil anvende de samme momsbogføringsgrupper på flere enheder, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at gøre det som standard.

* Du kan tildele momsvirksomhedsbogføringsgrupper til generelle virksomhedsbogføringsgrupper eller debitor- eller kreditorskabeloner.
* Du kan tildele momsproduktbogføringsgrupper til generelle produktbogføringsgrupper.  

Momsvirksomheds- eller produktbogføringsgruppen tildeles, når du vælger en virksomheds- eller produktbogføringsgruppe til en debitor, kreditor, vare eller ressource.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tildele momsbogføringsgrupper til konti, debitorer, kreditorer, varer og ressourcer

I følgende afsnit beskrives, hvordan du tildeler momsbogføringsgrupper til individuelle poster.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Sådan tildeles momsbogføringsgrupper til individuelle finanskonti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 6.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. Åbn kort for **kontoens finanskonto** .  
3. I oversigtspanelet **Bogføring** i feltet **Bogføringstype** skal du vælge enten **Salg** eller **Køb**.  
4. Vælg de momsbogføringsgrupper, du vil bruge til salgs- eller købskontoen.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Sådan tildeles momsvirksomhedsbogføringsgrupper til debitorer og kreditorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 7.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.  
2. Udvid oversigtspanelet **Fakturering** på **Debitor**- eller **Kreditor**-kortet.  
3. Vælg **momsvirksomhedsbogføringsgruppen**.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Sådan tildeles momsproduktbogføringsgrupper til individuelle varer og ressourcer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 8.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare** eller **Ressource**, og vælg derefter det relaterede link.  
2. Gør ét af følgende:  

    * Udvid oversigtspanelet **Pris og bogføring** på Vare **kort, og vælg** derefter Vis mere **for at få vist** feltet Momsproduktbogf.gruppe **.**   
    * Udvid oversigtspanelet **Fakturering** på **Ressource**-kortet.  
3. Vælg momsproduktbogføringsgruppen.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-nonstandard-vat-rates"></a>Konfigurere klausuler, der forklarer momsfritagelse eller ikke-standard-momssatser

Du konfigurerer en momsklausul til at beskrive oplysninger om den moms, der skal anvendes. Oplysningerne kan være påkrævet som påbudt af myndighederne. Når du har konfigureret en momsklausul og tilknyttet den til en momsbogføringsgruppe, vises momsklausulen på udskrevne salgsdokumenter, der bruger momsbogføringsopsætningsgruppen.

Hvis det er nødvendigt, kan du også angive, hvordan momsklausuler skal oversættes til andre sprog. Når du derefter opretter og udskriver et salgsdokument, der indeholder et moms-id, vil det udskrevne dokument indeholde den oversatte momsklausul. Den sprogkode, der er angivet på debitorkortet, bestemmer sproget.

Når du bruger ikke-standardiserede momssatser i forskellige typer dokumenter, f.eks. fakturaer eller kreditnotaer, skal du muligvis medtage en fritagelsestekst (momsklausul). Fritagelsesteksten angiver, hvorfor du beregnede en nedsat momssats eller nulmomssats. Du kan definere forskellige momsklausuler, der skal medtages i forretningsdokumenter for hver dokumenttype på siden **Momsklausuler efter bilagstype**.

Du kan redigere eller slette en momsklausul, og dine ændringer afspejles i en genereret rapport. Men [!INCLUDE[prod_short](includes/prod_short.md)] bevarer ikke en oversigt over ændringen. På rapporten udskrives og vises momsklausulbeskrivelserne for alle linjer i rapporten sammen med momsbeløbet og momsgrundbeløbet. Hvis en momsklausul ikke er defineret for alle linjer i salgsdokumentet, så udelades hele sektionen, når du udskriver rapporten.

### <a name="to-set-up-vat-clauses"></a>Sådan konfigureres momsklausuler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 9.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Oprette en ny linje på siden **Momsklausuler**.  
3. Angiv et id for klausulen i feltet **Kode**. Du bruger koden til at tildele klausulen til momsbogføringsgrupper.  
4. I feltet **Beskrivelse** skal du angive den momsfritagelse, du vil have vist i dokumenter, som kan inkludere moms. I feltet **Beskrivelse 2** skal du angive mere tekst, hvis det er nødvendigt. Teksten vises på nye dokumentlinjer.
5. Vælg handlingen **Beskrivelse efter dokumenttype**.
6. Udfyld felterne på siden **Momsklausuler efter dok.type** for at angive, hvilken momsfritagelsestekst der skal vises for hvilken dokumenttype.  
7. Valgfrit: Hvis du vil tildele momsklausulen til en momsbogføringsopsætning med det samme, skal du vælge **Opsætning** og derefter vælge klausulen. Hvis du vil vente, kan du tildele klausulen senere på siden **Momsbogf.opsætning**.  
8. Valgfrit: Hvis du vil angive, hvordan momsklausulen skal oversættes, skal du vælge handlingen **Oversættelser**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Sådan tildeles en momsklausul til en momsbogføringsopsætning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 10.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
2. Vælg den delsætning, der skal bruges til hver momsbogføringsopsætning, den gælder for, i kolonnen Momsbogføring Momsklausul **skode** .  

### <a name="to-specify-translations-for-vat-clauses"></a>Sådan angives oversættelser af momsklausuler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 11.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Oversættelser**.  
3. I feltet **Sprogkode** skal du vælge det sprog, du vil oversætte til.  
4. I felterne **Beskrivelse** og **Beskrivelse 2** skal du angive oversættelserne af beskrivelserne. Teksten vises i de oversatte momsrapportdokumenter.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>Sådan angives udvidet tekst til momsklausuler

> [!NOTE]  
> Hvis dit land eller område kræver længere tekst til momsklausuler end standardversionen, kan du angive en længere tekst for moms delsætningen som *udvidet tekst*, så den udskrives på salgs-og købsrapporterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 11.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Udvidede tekster**.  
3. Vælg handlingen **Ny**.  
4. Udfyld felterne **Sprogkode** og **Beskrivelse**.  
5. Alternativt kan du vælge feltet **Alle sprogkoder** eller angive det relevante sprog i feltet **Sprogkode**, hvis du bruger sprogkoder.  
6. Udfyld felterne **Startdato** og **Slutdato**, hvis du vil begrænse den tid, hvor den udvidede tekst bruges.  
7. Skriv den udvidede tekst til moms klausulerne på **Tekst**-linjerne.  
8. Markér de relevante felter for de dokumenttyper, hvor den udvidede tekst skal udskrives.  
9. Luk siden.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Oprette en momsbogføringsopsætning for at håndtere importmoms

Brug funktionen *Importmoms*, når du skal bogføre et dokument, hvor hele beløbet er moms. Du skal bruge funktionen, hvis du modtager en faktura fra skattemyndighederne for moms på importerede varer.  

Når du vil konfigurere koder for importmoms, skal du gøre følgende:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 12.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. På siden Momsproduktbogf.grupper. skal du oprette en ny momsproduktbogføringsgruppe for importmoms.  
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 13.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
4. På siden Opsætning af momsbogføring skal du oprette en ny linje eller bruge en eksisterende momsvirksomhedsbogføringsgruppe kombineret med den nye momsproduktbogføringsgruppe til importmoms.  
5. I feltet **Momsberegningstype** skal du vælge **Momskorrektion**.  
6. Angiv den finanskonto, der skal bruges til bogføring af importmoms, i feltet **Købsmomskonto**. Alle andre konti er valgfrie.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countriesregions"></a>Brug modtagermoms til handel mellem EU-lande/områder

Nogle virksomheder skal bruge modtagermoms, når de handler med andre virksomheder. Denne regel gælder f.eks. for køb fra EU-lande/områder og salg til EU-lande/områder.  

> [!NOTE]  
> Reglen gælder, når der handles med de virksomheder, som er registreret som momspligtige i et andet EU-land. Hvis du handler direkte med forbrugere i andre EU-lande/område, skal du kontakte skattemyndighederne for at få oplyst de gældende momsregler.  

> [!TIP]  
> Du kan kontrollere, at en virksomhed er registreret som momspligtig i et andet EU-land/område ved hjælp af tjenesten til kontrol af SE/CVR-nr. for EU. Tjenesten er tilgængelig og gratis i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Kontrollere CVR-numre](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countriesregions"></a>Salg til EU-lande/områder

Moms beregnes ikke på salg til momspligtige virksomheder i andre EU-lande/regioner. Du skal rapportere værdien af disse salg til EU-lande/områder separat på momsangivelsen.  

For at beregne moms på salg til EU-lande/områder korrekt, skal du:  

* Opret linjer for salg med de samme oplysninger for køb. Hvis du har oprettet linjer på siden **Momsbogf.opsætning** for køb fra EU-lande/områder, kan du også bruge disse linjer til salg.  
* Tildele momsvirksomhedsbogføringsgrupperne i feltet **Momsvirksomhedsbogf.gruppe** på oversigtspanelet **Fakturering** på kreditorkort for hver EU-kreditor. Du skal også angive debitorens CVR-nummer i feltet **SE/CVR-nr.** på oversigtspanelet **Udenrigshandel**.  

Når du bogfører salg til en debitor i et andet EU-land/område, beregner [!INCLUDE [prod_short](includes/prod_short.md)] momsbeløbet, og der oprettes en momspost baseret på oplysningerne om modtagermomsen og momsgrundbeløbet. Dette beløb bruges til at beregne momsbeløbet. Der bogføres ingen poster på momskontoen i finansposterne.

Hvis du vil bruge en kombination af momsvirksomheds- og momsproduktbogføringsgruppe til rapportering som tjenester i de periodiske momsrapporter, skal du markere feltet **EU-tjeneste**.

> [!NOTE]  
> Feltet **EU-tjeneste** gælder kun for momsrapporter. Feltet er ikke relateret til funktionerne **Servicedeklaration** eller **Intrastat for service** .

## <a name="vat-rounding-for-documents"></a>Momsafrunding for bilag

Beløb i de bilag, som endnu ikke er blevet bogført, afrundes og vises, så de svarer til de endelige afrundingsbeløb, som bogføres. [!INCLUDE [prod_short](includes/prod_short.md)] beregner moms for et fuldstændigt dokument. Momsberegningen er baseret på summen af alle linjerne i bilaget med det samme moms-id.  

## <a name="set-up-vat-reporting"></a>Konfigurer momsrapportering

Du skal angive oplysninger om, hvordan skattemyndighederne i dit land kræver, at du indsender momsrapporter. Følgende fremgangsmåde viser de mest almindeligt brugte oplysninger. Dit land/område kan dog kræve yderligere trin. Du kan finde flere oplysninger i den relevante artikel i afsnittet *lokal funktionalitet* i panelet til venstre.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Se også

[Oprette momsangivelsestyper og momsangivelsesnavne](finance-how-setup-vat-statement.md)    
[Oprette urealiseret moms](finance-setup-unrealized-vat.md)    
[Rapportere moms til en skattemyndighed](finance-how-report-vat.md)    
[Arbejde moms af salg og køb](finance-work-with-vat.md)    
[Arbejde med Momssatsændringsværktøj](finance-how-use-vat-rate-change-tool.md)    
[Kontrollere momsregistreringsnumre](finance-how-validate-vat-registration-number.md)    
[Lokal funktionalitet i Business Central](about-localization.md)    
[Momsindberetning i den tyske udgave](LocalFunctionality/Germany/vat-reporting.md)    
[Belgisk moms](LocalFunctionality/Belgium/belgian-vat.md)    
[Italiensk moms](LocalFunctionality/Italy/italian-vat.md)    
[Oprette elektroniske moms- og ICP-angivelser i den hollandske udgave](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)    
[Momsrapporter i den spanske udgave](LocalFunctionality/Spain/vat-reports.md)    
[Konfigurere bogføring af varer og tjenesteydelser i den australske version](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)    
[Moms i den tjekkiske udgave](LocalFunctionality/Czech/finance-vat.md)    
[Momsrapportering i den norske version](LocalFunctionality/Norway/norwegian-vat-reporting.md)    
[Rapportering af vare- og tjenestemoms og harmoniseret salgsmoms i Canada](LocalFunctionality/Canada/sales-tax-goods-services.md)    

[!INCLUDE[footer-include](includes/footer-banner.md)]
