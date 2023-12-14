---
title: Konfigurere valutaer
description: 'Du skal konfigurere valutaer, hvis du køber eller sælger i andre valutaer end din lokale valuta eller registrerer finanstransaktioner i forskellige valutaer.'
author: brentholtorf
ms.topic: conceptual
ms.search.keywords: multiple currencies
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: bholtorf
---
# Konfigurere valutaer

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Brug en ekstern tjeneste til at få de seneste valutakurser i vinduet **Valutaer**. Du kan finde flere oplysninger i [Sådan konfigureres en valutakurstjeneste](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service).  

[!INCLUDE [finance-currencies-lcy](includes/finance-currencies-lcy-note.md)]

## <a name="curr"></a>Valutaer

I følgende tabel beskrives de felterne i listen **Valutaer**.

|Felt|Beskrivlse|  
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
|**Maks. momsdifference tilladt**|Det maksimalt tilladte beløb for momsdifferencer i denne valuta. Flere oplysninger i [Manuel korrektion af momsbeløb i salgs- og købsdokumenter](finance-work-with-vat.md#correcting-vat-amounts-manually-on-sales-and-purchase-documents). Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|
|**Momsafrundingstype**|Angiver afrundingsmetoden for korrigering af momsbeløb manuelt i salgs-og købsdokumenter. Dette felt er muligvis ikke synligt som standard. Den kan hentes ved at tilpasse siden.|

### Tilgængelige valutafunktioner

I følgende tabel beskrives nøgle handlinger på siden **Valutaer**.  

|Menu|Handling|Beskrivlse|
|-------------|--------------|------------------------------|
|**Behandle**|**Foreslå konti**|Bruge konti fra andre valutaer. De mest almindeligt brugte konti indsættes.|
||**Skift betalingstolerance**|Rediger den maksimale betalingstolerance og/eller betalingstoleranceprocenten og filtrere efter valuta. Du kan finde flere oplysninger i [Betalingstolerance og kontantrabattolerance](finance-payment-tolerance-and-payment-discount-tolerance.md)|
||**Valutakurser**|Vis opdaterede kurser for de valutaer, som du vil bruge.|
||**Kursreguler valutabeholdninger**|Reguler finans-, debitor-, kreditor- og bankkontoposter, så de svarer til den opdaterede saldo i situationer, hvor kursen har ændret sig siden bogføringen.|
||**Valutakursreguleringsjournal**|Få vist resultaterne af kørslen **Kursreguler valutabeholdninger**. Der oprettes én linje for hver valuta eller valutakombination og bogføringsgruppe, der indgår i reguleringen.|
|**Valutakurstjeneste**|**Valutakurstjenester**|Vis eller rediger konfigurationen af de tjenester, der er konfigureret til at hente opdaterede valutakurser, når du vælger handlingen **Opdater valutakurser**.|
||**Opdater valutakurser**|Brug de seneste valutakurser fra en tjenesteudbyder.|
|**Rapporter**|**Valutaopgørelse**|Vis saldi for alle debitorer og kreditorer i såvel udenlandsk valuta som i den lokale valuta. Rapporten indeholder 2 LV-saldi. Det ene er saldoen for udenlandsk valuta omregnet til RV ved hjælp af valutakurs på tidspunktet for transaktion. Det andet er saldoen for udenlandsk valuta omregnet til RV ved hjælp af valutakurs på arbejdsdatoen.|

## RV og andre valutaer

[!INCLUDE [finance-currencies-lcy-def](includes/finance-currencies-lcy-def.md)]

## Afrundingsvalutaer

Hvis du vil styre valutaer, hvor der ikke anvendes decimaler, og du vil undgå unødvendige decimaler i udenlandsk valuta, kan du benytte to forskellige afrundingsfunktioner:

- Pris-afrunding  

- Afrunding  

Disse funktioner kan anvendes uafhængigt eller kombineret. Derudover kan funktioner anvendes sammen med fakturaafrunding.

I modsætning til fakturaafrundingsfunktionen påvirker funktionerne til afrunding og pris-afrunding kun beløb i udenlandsk valuta - ikke de tilsvarende beløb i den lokale valuta. Disse to funktioner resulterer ikke i bogføring til finanskonti. Det er derfor ikke nødvendigt at specificere en finanskonto til bogføringsgrupper eller andet.

### Pris-afrunding

Pris-afrundingsfunktionen styrer den måde, salgspriser for varer og ressourcer i udenlandsk valuta afrundes på salgs- og købslinjer. Du skal angive reglerne for hver valuta separat i feltet **Pris-afrundingspræcision** i listen **Valutaer**.

Pris-afrundingsfunktionen bruges automatisk, hver gang du angiver et vare- eller ressourcenummer på en salgslinje. Hvis fakturaen er til en kunde, som har en fakturakode, omregnes varens eller ressourcens pris til kundens valuta. Prisen afrundes i overensstemmelse med pris-afrundingspræcisionen for valutaen.

### Afrunding

Afrundingsfunktionen styrer den måde, beløb i udenlandske valutaer afrundes på finanskladdelinjer, salgslinjer og købslinjer. Du skal angive reglerne for hver valuta separat i feltet **Afrundingspræcision** i listen **Valutaer**.

Beløb i udenlandske valutaer afrundes, når du udfylder og bogfører finanskladdelinjer, salgslinjer og købslinjer.

## Valutakurser

Du kan registrere valutakurser for hver udenlandsk valuta og angive, hvilke datoer valutakurserne gælder fra. Du kan f.eks. angive daglige, månedlige eller kvartalsvise valutakurser for hver udenlandsk valuta.

Du kan bevare valutakurser på siden **Valutakurs** til referenceformål. Når du har brug for at opdatere valutakurserne, kan du bruge knappen **Opdater valutakurser** for at få de seneste valutakurser fra en ekstern tjenesteudbyder.

## Finanskonti

Du kan ikke sammenkæde valutakoder til finanskonti, fordi beløb på regnskab føres i RV. Hvis du har et banklån i DKK og placerer indskud på en bankkonto i SEK, kan du holde styr på disse konti ved at oprette bankkonti i USD og SEK. Med bogføringsgrupper kan du sammenkæde kontiene til relevante finanskonti. I regnskabet vises værdien af beløbene i RV.

Du kan angive en valutakode på en finanskladdelinje og bogføre linjen til en finanskonto. Den relevante valutakurs bruges til at omregne beløbet til lokal valuta, før det bogføres til finanskontoen.  

## Eksempel på en valutapostering for tilgodehavender

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Se også

[Opdatere valutakurser](finance-how-update-currencies.md)  
[Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
