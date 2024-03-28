---
title: 'Fremgangsmåde: Arbejde moms af salg og køb'
description: 'I dette emne beskrives de forskellige metoder til at arbejde med moms både manuelt og med automatisk opsætning, så du kan overholde lande/områdespecifikke regler.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbejde med moms af salg og køb

Hvis dit land eller område kræver, at du beregner moms på salgs-og købstransaktioner, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at beregne moms. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Der er dog nogle opgaver i forbindelse med moms, der kan udføres manuelt. Du kan f.eks. rette et bogførte beløb, hvis du opdager, at en leverandør anvender en anden afrundingsmetode.  

> [!TIP]
> Du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] kontrollere momsregistreringsnummeret og andre virksomhedsoplysninger, når du opretter eller opdaterer dokumenter. Du kan finde flere oplysninger i [Validate CVR-numre](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents"></a>Beregne og vise momsbeløb i salg- og købsdokumenter

Når du vælger et varenummer i feltet **Nummer** felt på salgs-eller købsdokumenter, [!INCLUDE[prod_short](includes/prod_short.md)] udfylder felterne **Enhedspris** og **Linjebeløb**. Salgsprisen stammer fra enten **Vare**-kortet eller fra de varesalgspriser, der er tilladt for varen og debitoren. [!INCLUDE[prod_short](includes/prod_short.md)] beregner kun linjebeløb, når du angiver et antal for linjen.  

Hvis salgsprisen og linjebeløbene skal være inklusive moms, f. eks. Hvis du sælger til detailkunder, skal du markere afkrydsningsfeltet **priser inkl. moms** i dokumentet. Du kan finde flere oplysninger i [nkl./ekskl. moms i salgsdokumenter](#including-or-excluding-vat-in-prices-and-line-amounts). 

Du kan beregne og vise momsbeløb i salgs- og købsdokumenter forskelligt, afhængigt af den type debitor eller kreditor, du handler med. Du kan også ændre det beregnede momsbeløb manuelt for at have det samme momsbeløb som det, der er beregnet af kreditoren i en given transaktion.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts"></a>Inklusive eller eksklusive moms i priser og linjebeløb

Hvis afkrydsningsfeltet **Priser inkl. moms** er markeret på et salgsdokument, vil felterne **Enhedspris** og **Linjebeløb** være inkl. moms. Som standard er moms ikke inkluderet i disse felter. Navnene på felterne afspejler, om priserne er inkl. moms.  

Du kan oprette standardindstillinger for **Priser inkl. moms** for alle salgsdokumenterne for en kunde i feltet **Priser inkl. moms** på kortet **Debitor**. Du kan også oprette varesalgspriser, så de er inkl. eller ekskl. moms. Salgsprisen på varekortet udelukker typisk moms. 

Følgende tabel indeholder en oversigt over, hvordan salgsprisbeløbene for et salgsdokument beregnes, når du har oprettet priser på siden **Salgspriser**:  

|**Feltet Salgspris inkl. moms på varekortet**|**Priser inkl. moms-felt**|**Handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ikke aktiveret|Ikke aktiveret|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen ekskl. moms** i salgslinjerne.|  
|Ikke aktiveret|Aktiveret|Momsbeløbet pr. salgsenhed beregnes og lægges til **salgsprisen** på varekortet. Den samlede salgspris indsættes derefter i feltet **salgsprisen inkl. moms** på salgslinjerne.|  
|Aktiveret|Ikke aktiveret|Programmer beregner momsbeløbet, der er medtaget i **Salgsprisen** på **varekortet** ved hjælp af momsprocenten relateret til kombinationen af Momsvirks.bogf.gruppe (pris) og Momsproduktbogf.gruppe. **Salgsprisen** på varekortet, reduceret med momsbeløbet, angives derefter i feltet **Enhed pris ekskl. MOMS** i salgslinjerne. Du kan finde flere oplysninger i [Bruge momsvirksomhedsbogføringsgrupper og debitorprisgrupper](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups).|  
|Aktiveret|Aktiveret|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen inkl. moms** i salgslinjerne.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups"></a>Bruge momsvirksomhedsbogføringsgrupper og debitorprisgrupper

Hvis du vil have priser til at omfatte moms, kan du bruge momsvirksomhedsbogføringsgrupper til at beregne beløbet på grundlag af momsbogføringsopsætningen for gruppen. Du kan finde flere oplysninger i [Konfigurere momsvirksomhedsbogføringsgrupper](finance-setup-vat.md#set-up-vat-business-posting-groups).

Afhængigt af hvad du vil gøre, kan du knytte en momsvirksomhedsbogføringsgruppe til debitorer eller salgsdokumenter på følgende måder:

* Hvis du vil bruge samme momssats for alle debitorer, kan du vælge en gruppe i feltet **momsvirksomhedsbogføringsgruppe (salgsbeløb)** på siden **Salgsopsætning**.
* Hvis du vil bruge en momssats for en bestemt debitor, kan du vælge en gruppe i feltet **momsvirksomhedsbogføringsgruppe (salgsbeløb)** på siden **Debitorkort**. 
* Hvis du vil bruge en momssats for bestemte debitorer, kan du vælge en gruppe i feltet **momsvirksomhedsbogføringsgruppe (salgsbeløb)** på siden **Debitorprisgruppe**. Dette er f. eks. nyttigt, når du vil have en pris, der gælder for alle debitorer i bestemte geografiske områder eller for en bestemt branche.
* På alle salgsdokumenter i feltet **momsvirksomhedsbogføringsgruppe**. Det momsbeløb, der er angivet for gruppen, bruges kun for det dokument, du arbejder på i øjeblikket.

> [!NOTE]
> Hvis du ikke angiver en gruppe i feltet **momsvirksomhedsbogføringsgruppe (pris)**, medtages de ikke i priserne.

#### <a name="examples"></a>Eksempler

Faktorer som det land eller område, du sælger i, eller den type brancher, du sælger til, kan påvirke det momsbeløb, du skal redegøre for. F. eks. kan en restaurant opkræve 6 % moms af måltider, der er Eaten internt og 17 % for takeaway. For at opnå dette skal du oprette en momsvirksomhedsbogføringsgruppe (salgspris) for internt og en til takeaway.

## <a name="working-with-vat-date"></a>Arbejde med momsdato

### <a name="vat-date-in-documents"></a>Momsdato i dokumenter

Når du opretter nye salgs-eller købsdokumenter, bliver **momsdatoen** baseret på indstillingen i feltet **standardmomsdato** på siden **Regnskabsopsætning**. Denne standardværdi kan være den samme som **Bogføringsdato** eller **Bilagsdato**. Hvis du har brug for en anden moms dato, kan du ændre værdien i feltet **momsdato** manuelt. Når du bogfører dokumentet, vises **momsdatoen** på bogførings dokumentet og på moms-og finansposterne.

> [!NOTE]
> Hvis feltet **Momsdato** ikke er tilgængeligt i dokumenter eller kladder, betyder det, at **Brug ikke momsdatofunktionen** er valgt i feltet **Forbrug af momsdato** på **Regnskabsopsætning**-siden .  

> [!IMPORTANT]
> Hvis du konfigurerer **Kontrol af momsperiode** i **Regnskabsopsætningen** som **Blokér bogføring inden for den lukkede periode** eller **Blokér bogføring inden for lukket periode**, kan du kun bogføre et dokument eller en kladde, hvis datoen i feltet **Momsdato** ikke er i en lukket periode i **Momsangivelsesperioder**. Selvom perioden i **Momsangivelsesperioder** er åben, får du måske en advarsel baseret på **Momsangivelsesstatus** og konfiguration i **Kontrol af momsperioden**.

> [!IMPORTANT]
> Med start i version 23.1 kan du forhindre eller tillade bogføring af **Momsdatoen** for et bestemt dataområde ved hjælp af felterne **Tillad bogføring fra** og **Tillad bogføring til** i **Regnskabsopsætningen** og **Brugeropsætningen**. Hvis du bruger ældre versioner kan du forhindre eller tillade bogføring af **Momsdatoen** for et bestemt dataområde ved hjælp af felterne **Tillad bogføring fra** og **Tillad bogføring til** i **Regnskabsopsætningen** og **Brugeropsætningen**.  

> [!NOTE]
> Hvis du lader **Momsdatoen** være tom, vil [!INCLUDE [prod_short](includes/prod_short.md)] bruge standardopsætningen fra **Standardmomsdatoen** i **Regnskabsopsætningen** som en **Momsdato** i den bogførte transaktion.  

### <a name="modifying-the-vat-date-in-posted-entries"></a>Tilpasse momsdato i bogførte poster

Hvis det er nødvendigt, kan du ændre momsdatoen ved bogføring af dokumenter. Hvis du vil ændre **momsdatoen** for bogførte bilag, skal du følge disse trin:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **VAT-poster**, og vælg derefter det relaterede link. 
2. Find posten med en forkert momsdato.  
3. Klik på **Rediger liste**-handling, og indtast den korrekte dato i feltet **momsdato**.  
4. Den nye momsdato bliver ændret i relaterede **finansposter**, og i det bogførte dokument.  

> [!NOTE]
> Du kan kun ændre feltet **Momsdato** i **Momsposter**, hvis den aktuelle dato ikke er i en afsluttet momsreturperiode. Selvom perioden i **Momsangivelsesperioder** er åben, får du måske en advarsel baseret på **Momsangivelsesstatus**.  

> [!NOTE]
> Hvis dokumentet indeholder mere end én **Momspost**, skal du kun ændre værdien i feltet **Momsdato** i en post, der er relateret til dokumentet. For at sikre, at poster er vedvarende, ændrer [!INCLUDE[prod_short](includes/prod_short.md)] automatisk momsdatoen i momsposter, der vedrører denne transaktion. [!INCLUDE [prod_short](includes/prod_short.md)] vil opdatere **momsdatoen** i andre tabeller (finansposter og-bilag), men kun med relation til denne transaktion.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents"></a>Manuel korrektion af momsbeløb i salgs- og købsdokumenter

Du kan foretage rettelser i bogførte momsposter, så du kan ændre beløbene for den samlede salgs- eller købsmoms uden at ændre momsbasen. Hvis du f. eks. modtager en faktura fra en kreditor med et forkert momsbeløb.  

Selvom du måske har oprettet en eller flere kombinationer til håndtering af importmoms, skal du angive mindst én momsproduktbogføringsgruppe. For eksempel kan du navngive den **RETTELSER** med henblik på korrektion, medmindre du kan bruge den samme finanskonto i feltet **Købsmomskonto** på momsbogføringslinjen. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Hvis en kontantrabat er beregnet på basis af et fakturabeløb, der er inkl. moms, tilbagefører du momsen af kontantrabatten, når rabatten er tildelt. Bemærk, at du skal aktivere feltet **Reguler moms ved kontantrabat** for både opsætning af finanskontiene generelt og momsbogføringsopsætning for en bestemt kombination af en momsvirksomhedsbogføringsgruppe og en momsproduktbogføringsgruppe.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents"></a>Sådan indstilles systemet for manuel momspostering i salgsdokumenter
I det følgende beskrives, hvordan du aktiverer manuelle momsændringer i salgsdokumenter. Trinnene er de samme på siden **Købsopsætning**.

1. På siden **Opsætning af Finans** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Salgsopsætning** skal du markere afkrydsningsfeltet **Tillad momsdifference**.  

### <a name="to-adjust-vat-for-a-sales-document"></a>Sådan reguleres moms for et salgsdokument

1. Åbn den relevante Salgsordre.  
2. Vælg handlingen **Statistik**.  
3. I oversigtspanelet **Fakturering** skal du vælge værdien i feltet **Antal skattelinjer**.
4. Rediger feltet **Momsbeløb**.   

> [!NOTE]  
> Det samlede momsbeløb på fakturaen, grupperet efter moms-id, vises på linjerne. Du kan justere beløbet manuelt i feltet **Momsbeløb** på linjerne for hvert moms-id. Når du retter i feltet **Momsbeløb**, kontrolleres det, at du ikke har ændret momsen med mere end det beløb, du har angivet som den maksimalt tilladte difference. Hvis beløbet er uden for **den maksimalt tilladte momsdifference**, vises der en advarsel, hvor den maksimalt tilladte difference vises. Du vil ikke kunne fortsætte, før beløbet ændres, så det ligger inden for de acceptable parametre. Klik på **OK** , og angiv et andet **momsbeløb**, som ligger inden for det tilladte. Hvis momsdifferencen er lig med eller lavere end den maksimalt tilladte, deles momsen proportionalt mellem de dokumentlinjer, der har det samme moms-id.  

## <a name="calculating-vat-manually-using-journals"></a>Manuel momsberegning ved hjælp af kladder
Du kan også justere momsbeløb i finans-, salgs- og købskladder. Det kan f.eks. være nødvendigt, når du angiver en kreditorfaktura i kladden, og der er en forskel mellem det momsbeløb, som [!INCLUDE[prod_short](includes/prod_short.md)] har beregnet, og momsbeløbet på kreditorfakturaen.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals"></a>Sådan indstilles systemet til manuel momspostering i finanskladder
Du skal udføre følgende trin, før du manuelt indtaster moms i en finanskladde.  

1. På siden **Opsætning af Finans** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Finanskladdetyper** skal du markere afkrydsningsfeltet **Tillad momsdifference** for den relevante kladde.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals"></a>Sådan indstilles systemet til manuel momspostering i salgs- og købskladder

Du skal udføre følgende trin, før du manuelt indtaster moms i en salgs- eller købskladde.

1. På siden **Købsopsætning** skal du markere afkrydsningsfeltet **Tillad momsdifference**.  
2. Gentag trin 1 for siden **Salgsopsætning**.
3. Når du har fuldført konfigurationen som beskrevet ovenfor, kan du justere værdien i feltet **Momsbeløb** på finanskladdelinjen eller værdien i feltet **Modkontos momsbeløb** på salgs- eller købskladdelinjen. [!INCLUDE[prod_short](includes/prod_short.md)] kontrollerer, at differencen ikke er større end det angivne maksimum.  

> [!NOTE]  
> Hvis differencen er større, bliver der vist en advarsel med den maksimalt tilladte difference. Hvis du vil fortsætte, skal du justere beløbet. Vælg **OK**, og angiv derefter et beløb, som ligger inden for det tilladte. Hvis momsforskellen er lig med eller lavere end det maksimalt tilladte, viser [!INCLUDE[prod_short](includes/prod_short.md)] differencen i feltet **Momsdifference**.  

## <a name="posting-import-vat-with-purchase-invoices"></a>Sådan bogføres importmoms på købsfakturaer
I stedet for at bruge kladder, når du bogfører en faktura med importmoms, kan du bruge en købsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Konfigurere Indkøb til at bogføre fakturaer med importmoms

1. Opret et kreditorkort for den importmyndighed, der sender dig fakturaen med importmoms. Du skal vælge de samme indstillinger til **Virksomhedsbogføringsgruppe** og **Momsvirksomhedsbogf.gruppe** som til den finanskonto, der bruges til importmoms.  
2. Opret en **Produktbogføringsgruppe** til importmomsen, og opret en **Momsproduktbogf.gruppe**, der skal bruges som standard til den tilhørende **Produktbogføringsgruppe**.  
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
4. Vælg finanskontoen til importmoms, og vælg derefter handlingen **Rediger**.  
5. På oversigtspanelet **Bogføring** skal du vælge opsætningen **Produktbogføringsgruppe** for at importere moms. [!INCLUDE[prod_short](includes/prod_short.md)] udfylder automatisk feltet **Momsproduktbogf.gruppe**.  
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
7. Opret en kombination af **Virksomhedsbogføringsgruppe** til momsmyndighederne og **Produktbogføringsgruppe** til importmoms. Til denne nye kombination skal du i feltet **Købskonto** vælge finanskontoen for importmoms.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Sådan oprettes en ny faktura til importmyndigheden (leverandører), når du har foretaget opsætningen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Opret en ny købsfaktura.  
3. I feltet **Leverandørnr.** skal du vælge importmyndigheden (leverandøren), og derefter vælge knappen **OK**.  
4. På købslinjen i feltet **Type** skal du vælge **Finanskonto** og i feltet **Nummer** og vælge finanskontoen til importmoms.  
5. I feltet **Antal** skal du skrive **1**.  
6. Angiv momsbeløbet i feltet **Købspris Ekskl. moms**.  
7. Bogfør fakturaen.  

## <a name="processing-certificates-of-supply"></a>Behandling af leveringscertifikater

Når du sælger varer til en kunde i et andet EU-land/-område, skal du tilsende kunden et leveringscertifikat, som kunden skal underskrive og returnere til dig. Der er følgende procedurer for behandling af leveringscertifikater for salgsleverancer, men de samme trin gælder for serviceleverancer af varer og returvareleverancer til kreditorer.  

### <a name="to-view-certificate-of-supply-details"></a>Sådan får du vist leveringscertifikatdetaljer
1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg **Leveringscertifikatdetaljer**.  
4. Som standard, hvis afkrydsningsfeltet **Leveringscertifikat påkrævet** er markeret for opsætningen af momsbogføringsgruppen for kunden, er feltet **Status** indstillet til **Påkrævet**. Du kan opdatere feltet for at angive, om kunden har returneret certifikatet.  

> [!Note]  
>  Hvis opsætningen af momsbogføringsgruppe ikke har afkrydsningsfeltet **Leveringscertifikat påkrævet** markeret, oprettes der en post, og feltet **Status** indstilles til **Ikke tilgængelig**. Du kan opdatere feltet for at afspejle de korrekte statusoplysninger. Du kan manuelt ændre status fra **Ikke tilgængelig** til **Påkrævet** og fra **Påkrævet** til **Ikke tilgængelig** efter behov.  

   Når du opdaterer feltet **Status** til **Påkrævet**, **Modtaget** eller **Ikke modtaget**, oprettes der et certifikat.  

> [!TIP]  
>  Du kan bruge siden **Leveringscertifikater** til at få et overblik over status for alle bogførte leverancer, der er blevet oprettet et leveringscertifikat for.  

5. Vælg **Udskriv leveringscertifikat**.  

> [!Note]  
>  Du kan se eller udskrive dokumentet. Når du vælger **Udskriv leveringscertifikat** og udskriver dokumentet, bliver afkrydsningsfeltet **Udskrevet** automatisk markeret. Desuden, hvis det ikke allerede er angivet, opdateres status for certifikatet til **Påkrævet**. Du kan evt. også medtage det udskrevne certifikat i leverancen.  

### <a name="to-print-a-certificate-of-supply"></a>Sådan udskriver du et leveringscertifikat

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg handlingen **Udskriv leveringscertifikat**.  

> [!NOTE]  
>  Alternativt kan du udskrive et certifikat fra siden **Leveringscertifikat**.  

4. Markér afkrydsningsfeltet **Udskriv linjedetaljer** for at medtage oplysninger fra linjerne på leverancedokumentet i certifikatet.  
5. Markér afkrydsningsfeltet **Opret leveringscertifikater, hvis de ikke allerede er oprettet** for at få [!INCLUDE[prod_short](includes/prod_short.md)] til at oprette certifikater til bogførte leverancer, der ikke har ét på tidspunktet for udførelsen. Når du markerer afkrydsningsfeltet, oprettes nye certifikater for alle bogførte leverancer, der ikke har certifikater i det valgte område.  
6. Som standard er filterindstillingerne for det leverancedokument, du har valgt. Udfyld filtreringsoplysningerne for at vælge et bestemt certifikat for levering, som du vil udskrive.  
7. På siden **Leveringscertifikat** skal du vælge knappen **Udskriv** for at udskrive rapporten eller vælge handlingen **Vis udskrift** for at se den på skærmen.  

> [!Note]  
> Feltet **Status for leveringscertifikat** og feltet **Udskrevet** opdateres med leveringen på siden **Leveringscertifikater**.  

8. Send det trykte leveringscertifikat til underskrift hos kunden.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Sådan opdaterer du status for et leveringscertifikat til en leverance

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke har returneret det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog kundens signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[prod_short](includes/prod_short.md)]-sammenkædning.  

   Hvis kunden ikke returnerer det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Du skal derefter tilsende kunden en ny faktura, der inkluderer moms, fordi den oprindelige faktura ikke vil blive accepteret af skattemyndighederne.  

Hvis du vil se en gruppe af certifikater, skal du starte fra siden **Leveringscertifikater** og derefter opdatere oplysninger om status for udestående certifikater, når du får dem tilbage fra dine kunder. Dette kan være nyttigt, når du vil søge efter alle de certifikater, der har en bestemt status, for eksempel **Påkrævet**, hvis status du vil opdatere til **Ikke modtaget**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Sådan opdaterer du status for en gruppe af leveringscertifikater

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Leveringscertifikater**, og derefter vælge det relaterede link.  
2. Filtrer feltet **Status** til den værdi, du ønsker, for at oprette en liste over certifikater, som du vil administrere.  
3. For at opdatere statusoplysningerne skal du vælge **Rediger liste**.  
4. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke har returneret det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog det signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[prod_short](includes/prod_short.md)]-dokumentsammenkædning.  

> [!NOTE]
> Du kan ikke oprette et nyt leveringscertifikat på siden **Leveringscertifikat**, når du navigerer til det ved hjælp af denne procedure. Hvis du vil oprette et certifikat til en forsendelse, der ikke var sat op til at kræve ét, skal du åbne den bogførte salgsleverance og bruge den ene af de to fremgangsmåder, der er beskrevet ovenfor:  
>
> * Sådan opretter du manuelt et leveringscertifikat  
> * Sådan udskriver du et leveringscertifikat.

## <a name="see-also"></a>Se også

[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Valider et SE/CVR-nr.](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
