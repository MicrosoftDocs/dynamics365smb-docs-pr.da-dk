---
title: Sådan arbejder du med moms af salg og køb
description: 'I denne artikel beskrives de forskellige metoder til at arbejde med moms både manuelt og med automatisk opsætning, så du kan overholde lande/områdespecifikke regler.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 05/29/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Arbejde med moms af salg og køb

Hvis dit land eller område kræver, at du beregner moms på salgs-og købstransaktioner, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at beregne moms. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Der er dog nogle opgaver i forbindelse med moms, der kan udføres manuelt. Du kan f.eks. rette et bogførte beløb, hvis du opdager, at en leverandør anvender en anden afrundingsmetode.  

> [!TIP]
> Du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] kontrollere momsregistreringsnummeret og andre virksomhedsoplysninger, når du opretter eller opdaterer dokumenter. Du kan finde flere oplysninger i [Validate CVR-numre](finance-how-validate-vat-registration-number.md).

## Beregne og vise momsbeløb i salg- og købsdokumenter  

Når du vælger et varenummer i feltet **Nummer** felt på salgs-eller købsdokumenter, [!INCLUDE[prod_short](includes/prod_short.md)] udfylder felterne **Enhedspris** og **Linjebeløb**. Salgsprisen stammer fra enten **Vare**-kortet eller fra de varesalgspriser, der er tilladt for varen og debitoren. [!INCLUDE[prod_short](includes/prod_short.md)] beregner kun linjebeløb, når du angiver et antal for linjen.  

Hvis salgsprisen og linjebeløbene skal være inklusive moms, hvis du f.eks. sælger til detailkunder, skal du markere afkrydsningsfeltet **Priser inkl. moms** i dokumentet. Du kan finde flere oplysninger i [nkl./ekskl. moms i salgsdokumenter](#including-or-excluding-vat-in-prices-and-line-amounts). 

Du kan beregne og vise momsbeløb på forskellige måder i salg- og købsdokumenter Forskellen afhænger af den type debitor eller kreditor, du har med at gøre. Du kan også ændre det beregnede momsbeløb manuelt for at have det samme momsbeløb som det, der er beregnet af kreditoren i en given transaktion.

### Inklusive eller eksklusive moms i priser og linjebeløb

Hvis afkrydsningsfeltet **Priser inkl. moms** er markeret på et salgsdokument, vil felterne **Enhedspris** og **Linjebeløb** være inkl. moms. Som standard er moms ikke inkluderet i disse felter. Navnene på felterne afspejler, om priserne er inkl. moms.  

Du kan oprette standardindstillinger for **Priser inkl. moms** for alle salgsdokumenterne for en kunde i feltet **Priser inkl. moms** på kortet **Debitor**. Du kan også oprette varesalgspriser, så de er inkl. eller ekskl. moms. Salgsprisen på varekortet udelukker typisk moms.

Følgende tabel indeholder en oversigt over, hvordan applikationen beregner salgsprisbeløbene for et salgsdokument, når priserne er opsat på siden **Salgspriser**:  

|**Feltet Salgspris inkl. moms på varekortet**|**Priser inkl. moms-felt**|**Handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ikke aktiveret|Ikke aktiveret|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen ekskl. moms** i salgslinjerne.|  
|Ikke aktiveret|Aktiveret|Momsbeløbet pr. salgsenhed beregnes og lægges til **salgsprisen** på varekortet. Den samlede salgspris indsættes derefter i feltet **salgsprisen inkl. moms** på salgslinjerne.|  
|Aktiveret|Ikke aktiveret|Programmer beregner momsbeløbet, der er medtaget i **Salgsprisen** på **varekortet** ved hjælp af momsprocenten relateret til kombinationen af Momsvirks.bogf.gruppe (pris) og Momsproduktbogf.gruppe. **Salgsprisen** på varekortet, reduceret med momsbeløbet, angives derefter i feltet **Enhed pris ekskl. MOMS** i salgslinjerne. Du kan finde flere oplysninger i [Bruge momsvirksomhedsbogføringsgrupper og debitorprisgrupper](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktiveret|Aktiveret|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen inkl. moms** i salgslinjerne.|

#### Bruge momsvirksomhedsbogføringsgrupper og debitorprisgrupper 

Hvis du vil have priser til at omfatte moms, kan du bruge momsvirksomhedsbogføringsgrupper til at beregne beløbet på grundlag af momsbogføringsopsætningen for gruppen. Du kan finde flere oplysninger i [Konfigurere momsvirksomhedsbogføringsgrupper](finance-setup-vat.md#set-up-vat-business-posting-groups).

Afhængigt af hvad du vil gøre, kan du knytte en momsvirksomhedsbogføringsgruppe til debitorer eller salgsdokumenter på følgende måder:

* Hvis du vil bruge samme momssats for alle debitorer, kan du vælge en gruppe i feltet **momsvirksomhedsbogføringsgruppe (salgsbeløb)** på siden **Salgsopsætning**.
* Hvis du vil bruge en momssats for en bestemt debitor, kan du vælge en gruppe i feltet **momsvirksomhedsbogføringsgruppe (salgsbeløb)** på siden **Debitorkort**. 
* Hvis du vil bruge en momssats for bestemte debitorer, kan du vælge en gruppe i feltet **Momsvirksomhedsbogføringsgruppe (pris)** på siden **Debitorprisgruppe**. Denne indstilling er f.eks. nyttig, når du vil have en pris, der gælder for alle debitorer i bestemte geografiske områder eller for en bestemt branche.
* På alle salgsdokumenter i feltet **Momsvirksomhedsbogføringsgruppe**. Det momsbeløb, der er angivet for gruppen, bruges kun for det dokument, du arbejder på i øjeblikket.

> [!NOTE]
> Hvis du ikke angiver en gruppe i feltet **momsvirksomhedsbogføringsgruppe (pris)**, medtages de ikke i priserne.

#### Eksempler

Faktorer som det land/område, du sælger i, eller den type brancher, du sælger til, kan påvirke det momsbeløb, du skal redegøre for. F. eks. kan en restaurant opkræve 6 % moms af måltider, der er Eaten internt og 17 % for takeaway. For at opnå dette skal du oprette en momsvirksomhedsbogføringsgruppe (salgspris) for internt og en til takeaway.

## Arbejde med momsdato

### Momsdato i dokumenter

Når du opretter nye salgs-eller købsdokumenter, er **Momsdato** baseret på indstillingen i feltet **Standardmomsdato** på siden **Opsætning af Finans**. Denne standardværdi kan være den samme som **Bogføringsdato** eller **Bilagsdato**. Hvis du har brug for en anden moms dato, kan du ændre værdien i feltet **momsdato** manuelt. Når du bogfører dokumentet, vises **Momsdato** på bogføringsdokumentet og på moms-og finansposterne.

> [!NOTE]
> Hvis feltet **Momsdato** ikke er tilgængeligt i dokumenter eller kladder, betyder det, at **Brug ikke momsdatofunktionen** er valgt i feltet **Forbrug af momsdato** på **Regnskabsopsætning**-siden .  

> [!IMPORTANT]
> Hvis du konfigurerer **Kontrol af momsperiode** i **Regnskabsopsætningen** som **Blokér bogføring inden for den lukkede periode** eller **Blokér bogføring inden for lukket periode**, kan du kun bogføre et dokument eller en kladde, hvis datoen i feltet **Momsdato** ikke er i en lukket periode i **Momsangivelsesperioder**. Selvom perioden i **Momsangivelsesperioder** er åben, får du måske en advarsel baseret på **Momsangivelsesstatus** og konfiguration i **Kontrol af momsperioden**.

> [!IMPORTANT]
> Med start i version 23.1 kan du forhindre eller tillade bogføring af **Momsdatoen** for et bestemt dataområde ved hjælp af felterne **Tillad bogføring fra** og **Tillad bogføring til** i **Regnskabsopsætningen** og **Brugeropsætningen**. Hvis du bruger ældre versioner kan du forhindre eller tillade bogføring af **Momsdatoen** for et bestemt dataområde ved hjælp af felterne **Tillad bogføring fra** og **Tillad bogføring til** i **Regnskabsopsætningen** og **Brugeropsætningen**.  

> [!NOTE]
> Hvis du lader **Momsdatoen** være tom, vil [!INCLUDE [prod_short](includes/prod_short.md)] bruge standardopsætningen fra **Standardmomsdatoen** i **Regnskabsopsætningen** som en **Momsdato** i den bogførte transaktion.  

### Tilpasse momsdato i bogførte poster

Hvis det er nødvendigt, kan du ændre momsdatoen ved bogføring af dokumenter. Hvis du vil ændre **momsdatoen** for bogførte bilag, skal du følge disse trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **VAT-poster**, og vælg derefter det relaterede link. 
2. Find posten med en forkert momsdato.  
3. Klik på **Rediger liste**-handling, og indtast den korrekte dato i feltet **momsdato**.  
4. Den nye momsdato ændres i relaterede **Finansposter** og i det bogførte dokument.  

> [!NOTE]
> Du kan kun ændre feltet **Momsdato** i **Momsposter**, hvis den aktuelle dato ikke er i en afsluttet momsreturperiode. Selvom perioden i **Momsangivelsesperioder** er åben, får du måske en advarsel baseret på **Momsangivelsesstatus**.  

> [!NOTE]
> Hvis dokumentet indeholder mere end én **Momspost**, skal du kun ændre værdien i feltet **Momsdato** i en post, der er relateret til dokumentet. For at sikre, at poster er vedvarende, ændrer [!INCLUDE[prod_short](includes/prod_short.md)] automatisk momsdatoen i momsposter, der vedrører denne transaktion. [!INCLUDE [prod_short](includes/prod_short.md)] vil opdatere **momsdatoen** i andre tabeller (finansposter og-bilag), men kun med relation til denne transaktion.  

## Manuel korrektion af momsbeløb i salgs- og købsdokumenter  

Du kan foretage rettelser i bogførte momsposter, så du kan ændre beløbene for den samlede salgs- eller købsmoms uden at ændre momsbasen. Hvis du f. eks. modtager en faktura fra en kreditor med et forkert momsbeløb.  

Selvom du måske har oprettet en eller flere kombinationer til håndtering af importmoms, skal du angive mindst én momsproduktbogføringsgruppe. For eksempel kan du navngive den **RETTELSER** med henblik på korrektion, medmindre du kan bruge den samme finanskonto i feltet **Købsmomskonto** på momsbogføringslinjen. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Hvis en kontantrabat var beregnet på basis af et fakturabeløb, der er inkl. moms, tilbagefører du momsen af kontantrabatten, når du tildeler rabatten. Du skal aktivere feltet **Reguler moms ved kontantrabat** for både opsætning af finanskontiene generelt og momsbogføringsopsætning for en bestemt kombination af en momsvirksomhedsbogføringsgruppe og en momsproduktbogføringsgruppe.  

### Sådan indstilles systemet for manuel momspostering i salgsdokumenter

Følg disse trin for at aktivere manuelle momsændringer i salgsdokumenter. Trinnene er de samme på siden **Købsopsætning**.

1. På siden **Opsætning af Finans** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Salgsopsætning** skal du slå til/fra-kontakten **Tillad momsdifference** til.  

### Sådan reguleres moms for et salgsdokument

1. Åbn den relevante Salgsordre.  
2. Vælg handlingen **Statistik**.  
3. I oversigtspanelet **Fakturering** skal du vælge værdien i feltet **Antal skattelinjer**.
4. Rediger feltet **Momsbeløb**.   

> [!NOTE]  
> Det samlede momsbeløb på fakturaen, grupperet efter moms-id, vises på linjerne. Du kan justere beløbet manuelt i feltet **Momsbeløb** på linjerne for hvert moms-id. Når du retter i feltet **Momsbeløb**, kontrolleres det, at du ikke har ændret momsen med mere end det beløb, du har angivet som den maksimalt tilladte difference. Hvis beløbet er uden for **den maksimalt tilladte momsdifference**, vises der en advarsel, hvor den maksimalt tilladte difference vises. Du vil ikke kunne fortsætte, før beløbet ændres, så det ligger inden for de acceptable parametre. Klik på **OK** , og angiv et andet **momsbeløb**, som ligger inden for det tilladte. Hvis momsdifferencen er lig med eller lavere end den maksimalt tilladte, deles momsen proportionalt mellem de dokumentlinjer, der har det samme moms-id.  

## Manuel momsberegning ved hjælp af kladder  

Du kan også justere momsbeløb i finans-, salgs- og købskladder. Du skal måske bruge en regulering, hvis du f.eks. angiver en kreditorfaktura i kladden, og der er en forskel mellem det momsbeløb, som [!INCLUDE[prod_short](includes/prod_short.md)] har beregnet, og momsbeløbet på kreditorfakturaen.  

### Sådan indstilles systemet til manuel momspostering i finanskladder

Du skal udføre følgende trin, før du manuelt indtaster moms i en finanskladde.  

1. På siden **Opsætning af Finans** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Finanskladdetyper** skal du markere afkrydsningsfeltet **Tillad momsdifference** for den relevante kladde.  

### Sådan indstilles systemet til manuel momspostering i salgs- og købskladder

Du skal udføre følgende trin, før du manuelt indtaster moms i en salgs- eller købskladde.

1. På siden **Købsopsætning** skal du markere afkrydsningsfeltet **Tillad momsdifference**.  
2. Gentag trin 1 for siden **Salgsopsætning**.
3. Når du har fuldført konfigurationen, kan du justere værdien i feltet **Momsbeløb** på finanskladdelinjen eller værdien i feltet **Modkontos momsbeløb** på salgs- eller købskladdelinjen. [!INCLUDE[prod_short](includes/prod_short.md)] bekræfter, at differencen ikke er større end det angivne maksimum.  

> [!NOTE]  
> Hvis differencen er større, bliver der vist en advarsel med den maksimalt tilladte difference. Hvis du vil fortsætte, skal du justere beløbet. Vælg **OK**, og angiv derefter et beløb, som ligger inden for det tilladte. Hvis momsforskellen er lig med eller lavere end det maksimalt tilladte, viser [!INCLUDE[prod_short](includes/prod_short.md)] differencen i feltet **Momsdifference**.  

## Sådan bogføres importmoms på købsfakturaer
I stedet for at bruge kladder, når du bogfører en faktura med importmoms, kan du bruge en købsfaktura.  

### Konfigurere Indkøb til at bogføre fakturaer med importmoms

1. Opret et kreditorkort for den importmyndighed, der sender dig fakturaen med importmoms. Du skal vælge de samme indstillinger til **Virksomhedsbogføringsgruppe** og **Momsvirksomhedsbogf.gruppe** som til den finanskonto, der bruges til importmoms.  
2. Opret en **Produktbogføringsgruppe** til importmomsen, og opret en **Momsproduktbogf.gruppe**, der skal bruges som standard til den tilhørende **Produktbogføringsgruppe**.  
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
4. Vælg finanskontoen til importmoms, og vælg derefter handlingen **Rediger**.  
5. På oversigtspanelet **Bogføring** skal du vælge opsætningen **Produktbogføringsgruppe** for at importere moms. [!INCLUDE[prod_short](includes/prod_short.md)] udfylder automatisk feltet **Momsproduktbogf.gruppe**.  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
7. Opret en kombination af **Virksomhedsbogføringsgruppe** til momsmyndighederne og **Produktbogføringsgruppe** til importmoms. Til denne kombination skal du vælge finanskontoen for importmoms i feltet **Købskonto**.  

### Sådan oprettes en ny faktura til importmyndigheden (leverandører), når du har afsluttet opsætningen  

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Opret en ny købsfaktura.  
3. I feltet **Leverandørnr.** skal du vælge importmyndigheden (leverandøren), og derefter vælge knappen **OK**.  
4. På købslinjen i feltet **Type** skal du vælge **Finanskonto** og i feltet **Nummer** og vælge finanskontoen til importmoms.  
5. I feltet **Antal** skal du skrive **1**.  
6. Angiv momsbeløbet i feltet **Købspris Ekskl. moms**.  
7. Bogfør fakturaen.  

## Behandling af leveringscertifikater

Når du sælger varer til en kunde i et andet EU-land/-område, skal du tilsende kunden et leveringscertifikat, som kunden skal underskrive og returnere til dig. Der er følgende procedurer for behandling af leveringscertifikater for salgsleverancer, men de samme trin gælder for serviceleverancer af varer og returvareleverancer til kreditorer.  

### Sådan får du vist leveringscertifikatdetaljer  
1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg **Leveringscertifikatdetaljer**.  
4. Som standard, hvis afkrydsningsfeltet **Leveringscertifikat påkrævet** er markeret for opsætningen af momsbogføringsgruppen for kunden, er feltet **Status** indstillet til **Påkrævet**. Du kan opdatere feltet for at angive, om kunden returnerede certifikatet.  

> [!Note]  
>  Hvis opsætningen af momsbogføringsgruppe ikke har afkrydsningsfeltet **Leveringscertifikat påkrævet** markeret, oprettes der en post, og feltet **Status** indstilles til **Ikke tilgængelig**. Du kan opdatere feltet for at afspejle de korrekte statusoplysninger. Du kan manuelt ændre status fra **Ikke tilgængelig** til **Påkrævet** og fra **Påkrævet** til **Ikke tilgængelig** efter behov.  

   Når du opdaterer feltet **Status** til **Påkrævet**, **Modtaget** eller **Ikke modtaget**, oprettes der et certifikat.  

> [!TIP]  
>  Du kan bruge siden **Leveringscertifikater** til at få et overblik over status for alle bogførte leverancer, der er blevet oprettet et leveringscertifikat for.  

5. Vælg **Udskriv leveringscertifikat**.  

> [!Note]  
> Du kan se eller udskrive dokumentet. Når du vælger **Udskriv leveringscertifikat** og udskriver dokumentet, bliver afkrydsningsfeltet **Udskrevet** automatisk markeret. Desuden, hvis det ikke allerede er angivet, opdateres status for certifikatet til **Påkrævet**. Du kan evt. også medtage det udskrevne certifikat i leverancen.  

### Sådan udskriver du et leveringscertifikat

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg handlingen **Udskriv leveringscertifikat**.  

> [!NOTE]  
> Alternativt kan du udskrive et certifikat fra siden **Leveringscertifikat**.  

4. Slå til/fra-kontakten **Udskriv linjedetaljer** til for at medtage oplysninger fra linjerne på leverancedokumentet i certifikatet.  
5. Hvis [!INCLUDE[prod_short](includes/prod_short.md)] skal oprette certifikater til bogføre leverancer, der ikke har en, skal du slå til/fra-kontakten **Opret leveringscertifikater, hvis de ikke allerede er oprettet** til. Når du slår til/fra-kontakten til, oprettes nye certifikater for alle bogførte leverancer, der ikke har certifikater i det valgte område.  
6. Som standard er filterindstillingerne for det leverancedokument, du valgte. Udfyld filtreringsoplysningerne for at vælge et bestemt certifikat for levering, som du vil udskrive.  
7. På siden **Leveringscertifikat** skal du vælge knappen **Udskriv** for at udskrive rapporten eller vælge handlingen **Vis udskrift** for at se den på skærmen.  

   > [!Note]  
   > Feltet **Status for leveringscertifikat** og feltet **Udskrevet** opdateres med leveringen på siden **Leveringscertifikater**.  

8. Send det trykte leveringscertifikat til underskrift hos kunden.  

### Sådan opdaterer du status for et leveringscertifikat til en leverance  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke returnerede det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog kundens signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[prod_short](includes/prod_short.md)]-sammenkædning.  

   Hvis kunden ikke returnerer det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Du skal derefter tilsende kunden en ny faktura, der inkluderer moms, fordi skattemyndighederne ikke vil acceptere den oprindelige faktura.  

Hvis du vil have vist en gruppe af certifikater, skal du starte fra siden **Leveringscertifikater** og derefter opdatere oplysninger om status for udestående certifikater, når du får dem tilbage fra dine kunder. De opdaterede oplysninger kan være nyttige, når du vil søge efter alle de certifikater, der har en bestemt status, f.eks. **Påkrævet**, hvis status du vil opdatere til **Ikke modtaget**.  

### Sådan opdaterer du status for en gruppe af leveringscertifikater  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leveringscertifikater**, og derefter vælge det relaterede link.  
2. Filtrer feltet **Status** til den værdi, du ønsker, for at oprette en liste over certifikater, som du vil administrere.  
3. For at opdatere statusoplysningerne skal du vælge **Rediger liste**.  
4. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke returnerede det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog det signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentsammenkædning.  

> [!NOTE]
> Du kan ikke oprette et nyt leveringscertifikat på siden **Leveringscertifikat**, når du navigerer til det ved hjælp af denne procedure. Hvis du vil oprette et certifikat til en forsendelse, der ikke var sat op til at kræve ét, skal du åbne den bogførte salgsleverance og bruge den ene af de to fremgangsmåder, der er beskrevet tidligere:  
>
> * Sådan opretter du manuelt et leveringscertifikat  
> * Sådan udskriver du et leveringscertifikat.

## Se også

[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Valider et SE/CVR-nr.](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
