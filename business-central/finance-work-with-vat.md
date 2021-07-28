---
title: 'Fremgangsmåde: Arbejde moms af salg og køb'
description: I dette emne beskrives de forskellige metoder til at arbejde med moms både manuelt og med automatisk opsætning, så du kan overholde landespecifikke regler.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 06/16/2021
ms.author: bholtorf
ms.openlocfilehash: 5c4efb0be09769770fdaf8ec0e503018119ce081
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6439431"
---
# <a name="work-with-vat-on-sales-and-purchases"></a>Arbejde moms af salg og køb
Hvis dit land eller område kræver, at du beregner moms af salgs- og købstransaktioner, så du kan indberette beløbene til skattemyndighederne, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til automatisk at beregne moms på salgs- og købsdokumenter. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Der er dog nogle opgaver i forbindelse med moms, der kan udføres manuelt. Du kan f.eks. rette et bogførte beløb, hvis du opdager, at en leverandør anvender en anden afrundingsmetode.  

> [!TIP]
> Du kan lade [!INCLUDE[prod_short](includes/prod_short.md)] kontrollere momsregistreringsnummeret og andre virksomhedsoplysninger, når du opretter eller opdaterer dokumenter. Du kan finde flere oplysninger i [Validate CVR-numre](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Beregne og vise momsbeløb i salg- og købsdokumenter  
Du kan beregne og vise momsbeløb i salgs- og købsdokumenter forskelligt, afhængigt af den type debitor eller kreditor, du handler med. Du kan også tilsidesætte det beregnede momsbeløb for at have det samme momsbeløb som det, der er beregnet af kreditoren i en given transaktion.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Salgspris og linjebeløb inkl./ekskl. moms i salgsdokumenter  
Når du vælger et varenummer i feltet **Nummer** i et salgsdokument, udfylder [!INCLUDE[prod_short](includes/prod_short.md)] også feltet **Salgspris**. Salgsprisen stammer fra enten **Vare**-kortet eller fra de varesalgspriser, der er tilladt for varen og debitoren. [!INCLUDE[prod_short](includes/prod_short.md)] beregner kun **Linjebeløb**, når du angiver et antal for linjen.  

Hvis du sælger til detailhandelsvirksomheder, skal priserne på salgsdokumenterne evt. være inkl. moms. For at gøre dette skal du markere afkrydsningsfeltet **Priser inkl. moms** på dokumentet.  

### <a name="including-or-excluding-vat-on-prices"></a>Priser med eller uden moms
Hvis afkrydsningsfeltet **Priser inkl. moms** er markeret på et salgsdokument, vil felterne **Salgspris** og **Linjebeløb** være inkl. moms. Feltnavnene vil også afspejle dette. Som standard er moms ikke inkluderet i disse felter.  

Hvis afkrydsningsfeltet ikke er markeret, vil felterne **Salgspris** og **Linjebeløb** udfyldes ekskl. moms, og feltnavnene vil afspejle dette.  

Du kan oprette standardindstillinger for **Priser inkl. moms** for alle salgsdokumenterne for en kunde i feltet **Priser inkl. moms** på kortet **Debitor**. Du kan også oprette varesalgspriser, så de er inkl. eller ekskl. moms. Sædvanligvis vil varesalgsprisen på varekortet være prisen ekskl. moms. Det er oplysningerne i feltet **Salgspris inkl. moms** på **Vare**-kortet, der bruges til at bestemme salgsprisbeløbet for salgsdokumenter.  

Følgende tabel indeholder en oversigt over, hvordan salgsprisbeløbene for et salgsdokument beregnes, når du har oprettet priser på siden **Salgspriser**:  

|**Feltet Salgspris inkl. moms på varekortet**|**Feltet Priser inkl. moms i salgshovedet**|**Handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ingen markering|Ingen markering|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen ekskl. moms** i salgslinjerne.|  
|Ingen markering|Markering|Momsbeløbet pr. salgsenhed beregnes og lægges til **salgsprisen** på varekortet. Den samlede salgspris indsættes derefter i feltet **med salgsprisen inkl. moms** på salgslinjerne.|  
|Markering|Ingen markering|Programmer beregner momsbeløbet, der er medtaget i **Salgsprisen** på varekortet ved hjælp af momsprocenten relateret til kombinationen af Momsvirks.bogf.gruppe (pris) og Momsproduktbogf.gruppe. **Salgsprisen** på varekortet, reduceret med momsbeløbet, angives derefter i feltet **Enhed pris ekskl. MOMS** i salgslinjerne.|  
|Markering|Markering|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen inkl. moms** i salgslinjerne.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Manuel korrektion af momsbeløb i salgs- og købsdokumenter  
Du kan korrigere bogførte momsposter. Det giver mulighed for at ændre de samlede salgs- eller købsmomsbeløb uden at ændre momsgrundlaget. Det kan være nødvendigt, hvis du f.eks. modtager en faktura fra en leverandør, der har beregnet momsen forkert.  

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
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgskvitteringer**, og vælg derefter det relaterede link.  
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
    >  Du kan ikke oprette et nyt leveringscertifikat på siden **Leveringscertifikat**, når du navigerer til det ved hjælp af denne procedure. Hvis du vil oprette et certifikat til en forsendelse, der ikke var sat op til at kræve ét, skal du åbne den bogførte salgsleverance og bruge den ene af de to fremgangsmåder, der er beskrevet ovenfor:  
    >
    > * Sådan opretter du manuelt et leveringscertifikat  
    > * Sådan udskriver du et leveringscertifikat.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Valider et SE/CVR-nr.](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
