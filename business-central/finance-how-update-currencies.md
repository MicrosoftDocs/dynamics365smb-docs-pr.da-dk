---
title: Opdatere valutakurser
description: Spore beløb i forskellige valutaer ved hjælp af valutakoder, og lad Business Central hjælpe dig med at regulere valutakursen for bogførte poster med en ekstern service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 06/03/2021
ms.author: edupont
ms.openlocfilehash: 0baa12a7f63e67184a00dab893c8222facfe269d
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/08/2021
ms.locfileid: "6441618"
---
# <a name="update-currency-exchange-rates"></a>Opdatere valutakurser

Da virksomheder handler i flere lande/områder, bliver det mere vigtigt, at de kan gennemgå eller rapportere finansielle oplysninger i mere end én valuta. Den lokale valuta (RV) er defineret på siden **Regnskabsopsætning**, som beskrevet i artiklen [opsætning af Finans](finance-setup-finance.md). Når den lokale valuta (RV) er blevet defineret, vises den som en tom valuta, så hvis feltet **Valuta** er tomt, betyder det, at valutaen er RV.  

Derefter skal du oprette valutakoder for hver valuta, du bruger, hvis du køber eller sælger i andre valutaer end den lokale valuta (RV). Du kan også oprette bankkonti ved hjælp af valutaer. Det er muligt at bogføre finanstransaktioner i forskellige valutaer, men finanstransaktionen bogføres altid i lokal valuta (RV).

> [!Important]
> Du skal ikke oprette den lokale valutakode både i **regnskabsopsætningen** og på **valuta**-siden. Dette vil skabe forvirring mellem den tomme valuta og koden for RV i valutatabellen, og bankkonti, debitorer og kreditorer kan ved et uheld blive oprettet, nogle med den tomme valuta og nogle med RV-koden.

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Ved at angive en anden valuta som en såkaldt ekstra rapporteringsvaluta vil [!INCLUDE[prod_short](includes/prod_short.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md). Den ekstra rapporteringsvaluta bruges ofte til at lette finansiel rapportering til ejere, som er placeret i lande/områder, som bruger forskellige valutaer end den lokale valuta (RV).  

> [!IMPORTANT]
> Hvis du vil bruge en ekstra rapporteringsvaluta til finansiel rapportering, skal du have kendskab til begrænsningerne. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="currencies"></a>Valutaer

Du kan angive valutakoder i **valutaerne**, herunder yderligere oplysninger og indstillinger, der er nødvendige for hver valutakode.

> [!TIP]
> Opret valutaerne med den internationale ISO-kode som kode for at forenkle arbejdet med valutaen i fremtiden.

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Kode**|Id for valutaen.|
|**Beskrivelse**|En fritekstbeskrivelse af valutaen.|
|**ISO-kode**|Den internationale 3-bogstavkode til den valuta, der er defineret i ISO 4217.|
|**Numerisk ISO-kode**|Den internationale numeriske reference til den valuta, der er defineret i ISO 4217.|
|**Valutakursdato**|Den seneste faktiske valutakurs.|
|**ØMU-valuta**|Angiver, om valutaen er en ØMU-valuta (Economic and Monetary Union) - f.eks. EUR.|
|**Realiseret finansgevinstkonto**|Den konto, hvor den faktiske gevinst bogføres, når du modtager betalinger til tilgodehavender eller registrerer den faktiske valutakurs på betalinger til kreditorer. Du kan se et eksempel på en valutapostering i eksemplet nedenfor i denne tabel. |
|**Realiseret finanstabskonto**|Den konto, hvor det faktiske tab bogføres, når du modtager betalinger til tilgodehavender eller registrerer den faktiske valutakurs på betalinger til kreditorer. Du kan se et eksempel på en valutapostering i eksemplet nedenfor i denne tabel. |
|**Ikke-realiseret finansgevinstkonto**|Den konto, hvor den teoretiske gevinst bogføres, når du foretager en kursregulering.|
|**Ikke-realiseret finanstabskonto**|Den konto, hvor det teoretiske tab bogføres, når du foretager en kursregulering.|
|**Afrundingspræcision**|Nogle valutaer har andre formater til fakturabeløb, end det er defineret på siden **Regnskabsopsætning**. Hvis du ændrer afrundingspræcisionen for en valuta, vil alle fakturabeløb i den pågældende valuta afrundet med den opdaterede præcision.|
|**Decimaler for beløb**|Nogle valutaer har andre formater til fakturabeløb, end det er defineret på siden **Regnskabsopsætning**. Hvis du ændrer afrundingsdecimalen for en valuta, vil alle fakturabeløb i den pågældende valuta afrundet med den opdaterede decimaler.|
|**Afrundingstype på fakturaer**|Angiver den metode, der skal bruges, hvis beløbene skal afrundes. Indstillingerne er **nærmest**, **op** og **ned**.|
|**Præcision ved afrunding af enheder eller beløb**|Nogle valutaer har andre formater til enhedsbeløb, end det er defineret på siden **Regnskabsopsætning**. Hvis du ændrer enhedspræcisionen for en valuta, vil alle enhedsbeløb i den pågældende valuta afrundet med den opdaterede præcision.|
|**Decimalplaceringer for enheder eller beløb**|Nogle valutaer har andre formater til enhedsbeløb, end det er defineret på siden **Regnskabsopsætning**. Hvis du ændrer enhedsafrundingsdecimalen for en valuta, vil alle enhedsbeløb i den pågældende valuta afrundet med den opdaterede decimaler.|
|**Udlign. afrundingspræcision**|Angiver det interval, der skal gælde som afrundingsdifference, når du udligner poster i forskellige valutaer.|
|**Konverterings RV afrundet. Debetkonto**|Angiver konverteringsoplysninger, der også skal indeholde en debetkonto, hvis du vil indsætte rettelseslinjer til afrundingsdifferencer i finanskladden vha. funktionen **Indsæt konv. RV-afrund.linjer**.|
|**Konverterings RV afrundet. Kreditkonto**|Angiver konverteringsoplysninger, der også skal indeholde en kreditkonto, hvis du vil indsætte rettelseslinjer til afrundingsdifferencer i finanskladden vha. funktionen **Indsæt konv. RV-afrund.linjer**.|
|**Reguleret den**|Datoen for den sidste kursregulering.|
|**Rettet den**|Datoen for ændringen af valuta opsætningen.|
|**Betalingstolerance %**|Den maksimale betalingstolerance %, der er angivet for denne valuta. Du kan finde flere oplysninger i [Betalingstolerance og kontantrabattolerance](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Maks. betalingstolerancebeløb**|Det maksimale betalingstolerancebeløb, der er angivet for denne valuta. Du kan finde flere oplysninger i [Betalingstolerance og kontantrabattolerance](finance-payment-tolerance-and-payment-discount-tolerance.md). |
|**Valutafaktor**|Angiver forholdet mellem den valutaen og den lokale valuta ved hjælp af den aktuelle valutasats.|
|**Realiseret finansgevinstkonto**|Angiver den finanskonto, hvor kursgevinster skal bogføres for kursreguleringer mellem den lokale valuta (RV) og den ekstra rapporteringsvaluta. Kursgevinster beregnes, når kørslen Kursreguler valutabeholdninger udføres for at regulere finanskonti. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Realiseret finanstabskonto**|Angiver den finanskonto, hvor kurstab skal bogføres for kursreguleringer mellem den lokale valuta (RV) og den ekstra rapporteringsvaluta. Kursgevinster beregnes, når kørslen Kursreguler valutabeholdninger udføres for at regulere finanskonti. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Afrundingskonto (gevinst)**|Angiver den finanskonto, der bruges til at bogføre afrundingsbeløb (afrundingsdifferencer), når der bruges en ekstra rapporteringsvaluta i finansmodulet. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Afrundingskonto (tab)**|Angiver den finanskonto, der bruges til at bogføre afrundingsbeløb (afrundingsdifferencer), når der bruges en ekstra rapporteringsvaluta i finansmodulet. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Maks. momsdifference tilladt**|Det maksimalt tilladte beløb for momsdifferencer i denne valuta. Flere oplysninger i [Manuel korrektion af momsbeløb i salgs- og købsdokumenter](finance-work-with-vat.md#correcting-vat-amounts-manually-in-sales-and-purchase-documents). Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Momsafrundingstype**|Angiver afrundingsmetoden for korrigering af momsbeløb manuelt i salgs-og købsdokumenter. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|

### <a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en valutapostering for tilgodehavender

Når du modtager en faktura fra en virksomhed i en udenlandsk valuta, er det forholdsvis nemt at beregne fakturaens lokale valuta (RV) på basis af den aktuelle valutakurs. Fakturaen leveres imidlertid ofte med betalingsbetingelser, så du kan udskyde betalingen til en senere dato, hvilket indebærer en anden valutakurs. Dette problem kombineret med, at valutakurser altid er forskellige fra de officielle valutakurser gør, at det ikke er muligt at forudsige det nøjagtige beløb i den lokale valuta (RV), der er nødvendig for at dække fakturaen. Hvis fakturaens forfaldsdato går til næste måned, skal du muligvis også revaluate det lokale valuta beløb i slutningen af måneden. Kursreguleringen er nødvendig, fordi den nye RV-værdi, der skal dække fakturabeløbet, kan være anderledes, og firmaets gæld til leverandøren er potentielt ændret. Det nye RV-beløb kan være højere eller lavere end det forrige beløb og vil derfor være et tab eller et tab. Men da fakturaen endnu ikke er betalt, anses gevinsten eller tabet for at være *Urealiseret*. Senere betales fakturaen, og banken har returneret den faktiske valutakurs for betalingen. Det antages ikke, at det *realiserede* gevinst-eller tabsbeløb beregnes. Denne urealiserede gevinst eller gevinst tilbageføres derefter, og realiseringen af gevinsten eller tabet bogføres i stedet.

I følgende eksempel modtages en faktura den 1. januar med Valutabeløbet på 1000. På det tidspunkt er valutakursen 1.123.

|Dato|Handling|Valutabeløb|Bilagskurs|RV-beløb på dokument|Justeringskurs|Ikke-realiseret finansgevinstbeløb|Betalingssats|Realiseret finansbeløb|  
|-----|----------|------------|-----------|---------|-----------|-------------|---------|---------|
|1/1|**Faktura**|1000|1.123|1123|||||
|1/31|**Regulering**|1000||1125|1.125|2|||
|2/15|**Tilbagebetaling af betalingsregulering**|1000||||-2|||
|2/15|**Betaling**|1000||1120|||1.120|-3|

Ved udgangen af måneden udføres der en kursregulering, hvor kursreguleringen er angivet til 1,125, hvilket udløser en Urealiseret gevinst på 2.

På betalingstidspunktet viser den faktiske valutakurs, der er registreret for bank transaktionen, en valutakurs på 1,120.

Der er en urealiseret transaktion, som derfor bliver tilbageført sammen med betalingen.

Endelig registreres betalingen, og det faktiske tab bogføres på den realiserede tabskonto.

## <a name="available-currency-functions"></a>Tilgængelige Valutafunktioner

I følgende tabel beskrives nøgle handlinger på siden **Valutaer**. Nogle af handlingerne er forklaret i de næste afsnit.  

|Menu|Handling|Beskrivelse|
|-------------|--------------|------------------------------|
|**Behandle**|**Foreslå konti**|Bruge konti fra andre valutaer. De mest almindeligt brugte konti indsættes.|
||Skift betalingstolerance|Rediger den maksimale betalingstolerance og/eller betalingstoleranceprocenten og filtrere efter valuta. Du kan finde flere oplysninger i [Betalingstolerance og kontantrabattolerance](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**valutakurser**|Vis opdaterede kurser for de valutaer, som du vil bruge.|
||**Kursreguler valutabeholdninger**|Reguler finans-, debitor-, kreditor- og bankkontoposter, så de svarer til den opdaterede saldo i situationer, hvor kursen har ændret sig siden bogføringen.|
||**Valutakursreguleringsjournal**|Få vist resultaterne af kørslen **Kursreguler valutabeholdninger**. Der oprettes én linje for hver valuta eller valutakombination og bogføringsgruppe, der indgår i reguleringen.|
|**Valutakurstjeneste**|**Valutakurstjenester**|Vis eller rediger konfigurationen af de tjenester, der er konfigureret til at hente opdaterede valutakurser, når du vælger handlingen **Opdater valutakurser**.|
||**Opdater valutakurser**|Brug de seneste valutakurser fra en tjenesteudbyder.|
|**Rapporter**|**Valutaopgørelse**|Vis saldi for alle debitorer og kreditorer i såvel udenlandsk valuta som i den lokale valuta. Rapporten indeholder 2 LV-saldi. Det ene er saldoen for udenlandsk valuta omregnet til RV ved hjælp af valutakurs på tidspunktet for transaktion. Det andet er saldoen for udenlandsk valuta omregnet til RV ved hjælp af valutakurs på arbejdsdatoen.|

## <a name="exchange-rates"></a>Valutakurser

Valutakurserne er værktøjet til beregning af den lokale valutaværdi (RV) for hver valuta transaktion. Siden **Valutakurser** indeholder følgende felter:

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Startdata**|Den dato, hvor valuta kursen blev effektueret|  
|**Valutakode**|Den valutakode, der er knyttet til denne valutakurs|  
|**Associeret valutakode**|Hvis valutaen er en del af en trekants beregning, kan den relaterede valutakode oprettes her|  
|**Valutakursbeløb**|Valutakursbeløbet er den kurs, der skal bruges til den valutakode, der er valgt på linjen. Normalt 1 eller 100|  
|**Associeret valutakursbeløb**|Det forholdsmæssige valutakursbeløb er den kurs, der skal bruges til den forholdsmæssige valutakode.|  
|**Regul. valutakursbeløb**|Det regulerede valutakursbeløb er den kurs, der skal bruges til den valutakode, der er valgt på linjen til brug af kørslen **Kursreguler. valutabeholdninger**.|  
|**Ass. regul. valutakursbeløb**|Det forholdsmæssige regulerede valutakursbeløb er den kurs, der skal bruges til den valutakode, der er valgt på linjen til brug af kørslen **Kursreguler. valutabeholdninger**.|  
|**Fastsæt valutakursbeløb**|Angiver, om valutaens kurs kan ændres på fakturaer og kladdelinjer.|  

Generelt bruges værdierne i felterne **Valutakursbeløb** og **Associeret valutakursbeløb** som standardvaluta kurs på alle nye tilgodehavender og skyldige dokumenter, der er oprettet frem. Dokumentet tildeles valutakurserne i overensstemmelse med den aktuelle arbejdsdato.  

> [!Note]
> Den faktiske valutakurs beregnes vha. følgende formel:
>
> `Currency Amount = Amount / Exchange Rate Amount * Relational Exch. Rate Amount`

Reguleringsvalutakursbeløbet for reguleringsvalutakursen eller relations-reguleringen bruges til at opdatere alle åbne bank-, debitor-eller købstransaktioner.  

> [!Note]
> Den faktiske valutakurs beregnes vha. følgende formel:
>
> `Currency Amount = Amount / Adjustment Exch. Rate Amount * Relational Adjmt Exch. Rate Amt`

## <a name="adjusting-exchange-rates"></a>Regulering af valutakurser

Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives.

Kørslen **Juster valutakurser** bruges til at regulere valutakursen manuelt for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter.  

> [!TIP]
> Du kan bruge en service til automatisk at opdatere valutakurser i systemet. Du kan finde flere oplysninger i [Sådan konfigureres en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Dette regulerer imidlertid ikke valutakurser for allerede bogførte transaktioner. Hvis du vil opdatere valutakurser for bogførte poster, skal du bruge kørslen **Kursreguler valutabeholdninger**.

### <a name="effect-on-customers-and-vendors"></a>Indflydelse på debitorer/kreditorer

Det gælder for debitor- og kreditorkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene i de enkelte valutaopgørelser og bogfører beløbene på den finanskonto, der er angivet i feltet **Urealiseret gevinstkonto** eller i feltet **Urealiseret tabskonto** på siden **Valutaer**. Modposteringer bogføres automatisk på samlekontoen i finansbogholderiet.

Kørslen gennemgår alle åbne debitor- og kreditorposter. Hvis der er en kursdifference for en post, oprettes der en ny detaljeret debitor- eller leverandørpost, der viser det justerede beløb i debitor- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner for debitor- og kreditorposter

Reguleringsposterne tildeles dimensionerne fra debitor-/kreditorposter, og reguleringerne bogføres pr. kombination af dimensionsværdier.

### <a name="effect-on-bank-accounts"></a>Indflydelse på bankkonti

Det gælder for bankkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene for hver bankkonto, der er blevet tildelt en valutakode, og bogfører beløbene på den finanskonto, der er angivet i feltet **Realiseret gevinstkonto** eller i feltet **Realiseret tabskonto** på siden **Valutaer**. Modposter bogføres automatisk på de finansbankkonti, der er angivet i bankbogføringsgrupperne. Kørslen beregner én post pr. valuta pr. bogføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioner for bankkontoposter

Reguleringsposterne for bankkontoens finanskonto og for gevinst-/tabskontoen tildeles bankkontoens standarddimensioner.

### <a name="effect-on-gl-accounts"></a>Indflydelse på finanskonti
Hvis du bogfører i en ekstra rapporteringsvaluta, kan du bruge kørslen til at oprette nye finansposter for kursreguleringer mellem den relevante regnskabsvaluta og den ekstra rapporteringsvaluta. Kørslen beregner forskellene for hver finanspost og regulerer finansposterne, afhængigt af oplysningerne i feltet **Valutakursregulering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioner for finanskontoposter
Reguleringsposterne tildeles standarddimensionerne fra de konti, de bogføres på.

> [!Important]
> Før du kan bruge kørslen, skal du indtaste de kursreguleringer, som den udenlandske valutabeholdning skal reguleres efter. Det kan du gøre på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Sådan konfigureres en valutakurstjeneste
Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdateret, f.eks. FloatRates.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valutakurstjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Valutakurstjenester** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktiver tjenesten til ved at slå **Aktiveret** til.

> [!NOTE]
> Følgende video viser et eksempel på, hvordan du kan oprette forbindelse til en valutakursservice med brug af den europæiske Central Bank. I den målgruppe, der beskriver, hvordan du opretter felttilknytninger, returnerer indstillingen i kolonnen til den **Overordnede node for Valutakode** kun den første valuta, der er fundet i kolonnen **Kilde**. Indstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Sådan opdateres valutakurser fra en tjeneste
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **valutaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opdater valutakurser**.

Værdien i feltet **Valutakurs** på siden **Valutaer** opdateres med den seneste valutakurs.

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
