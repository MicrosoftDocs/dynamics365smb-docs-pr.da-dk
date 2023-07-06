---
title: Opdatere valutakurser (indeholder video)
description: Hvis du sporer beløb i forskellige valutaer kan Business Central hjælpe med at regulere f.eks. valutakurser for bogførte poster med en ekstern service.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 03/15/2022
ms.author: edupont
---
# <a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a><a name="update-currency-exchange-rates"></a>Opdatere valutakurser

Du kan f. eks. definere forskellige valutaer i [!INCLUDE [prod_short](includes/prod_short.md)], hvis du f. eks. handler i andre valutaer end den lokale valuta. For at hjælpe dig med at holde styr på ændringer i valutakurserne kan du administrere valutaerne manuelt, eller du kan oprette en valutakurs service.

## <a name="currencies"></a><a name="currencies"></a><a name="currencies"></a>Valutaer

> [!TIP]  
> Hvis du leder efter realtidsoplysninger om valutakurser (fx) eller historiske kurser, omtales de som valuta i [!INCLUDE[prod_short](includes/prod_short.md)]. Udover denne artikel kan du også se [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du kan angive valutakoder i **valutaerne**, herunder yderligere oplysninger og indstillinger, der er nødvendige for hver valutakode. Der er flere oplysninger i [Valutaer](finance-set-up-currencies.md#curr)

### <a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a><a name="example-of-a-receivable-currency-transaction"></a>Eksempel på en valutapostering for tilgodehavender

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## <a name="exchange-rates"></a><a name="exchange-rates"></a><a name="exchange-rates"></a>Valutakurser

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

## <a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a><a name="adjusting-exchange-rates"></a>Regulering af valutakurser

Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives.

Kørslen **Juster valutakurser** bruges til at regulere valutakursen manuelt for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter.  

> [!TIP]
> Du kan bruge en service til automatisk at opdatere valutakurser i systemet. Du kan finde flere oplysninger i [Sådan konfigureres en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service). Dette regulerer imidlertid ikke valutakurser for allerede bogførte transaktioner. Hvis du vil opdatere valutakurser for bogførte poster, skal du bruge kørslen **Kursreguler valutabeholdninger**.

Du kan få vist den effekt, som en regulering har ved bogføring, inden du bogfører ved at vælge **Forhåndsversion** på siden **Kursreguler valutabeholdninger**. Du kan også vælge, om finansposteringen skal være detaljeret (pr. post) eller opsummeret (pr. valuta) ved at vælge **Opsummerede poster**. Du kan også angive, hvordan dimensioner for urealiserede gevinst-og tabs posteringer skal håndteres, ved at vælge en af følgende indstillinger i feltet **Overfør dimensionsværdier**:  

- **Kildepost**: Finansposter for urealiserede gevinster og tab får dimensionsværdier overført fra den justerede post.
- **Pr. finanskonto**: Finansposter for urealiserede gevinster og tab får dimensionsværdier overført fra den urealiserede gevinst-og tabs finanskontos kildepost.
- **Ingen overførsel**: Finansposter for urealiserede gevinster og tab har ikke dimensionsværdier.

### <a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a><a name="effect-on-customers-and-vendors"></a>Indflydelse på debitorer/kreditorer

Det gælder for debitor- og kreditorkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene i de enkelte valutaopgørelser og bogfører beløbene på den finanskonto, der er angivet i feltet **Urealiseret gevinstkonto** eller i feltet **Urealiseret tabskonto** på siden **Valutaer**. Modposteringer bogføres automatisk på samlekontoen i finansbogholderiet.

Kørslen gennemgår alle åbne debitor- og kreditorposter. Hvis der er en kursdifference for en post, oprettes der en ny detaljeret debitor- eller leverandørpost, der viser det justerede beløb i debitor- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a><a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner for debitor- og kreditorposter

Reguleringsposterne tildeles dimensionerne fra debitor-/kreditorposter, og reguleringerne bogføres pr. kombination af dimensionsværdier.

### <a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a><a name="effect-on-bank-accounts"></a>Indflydelse på bankkonti

Det gælder for bankkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene for hver bankkonto, der er blevet tildelt en valutakode, og bogfører beløbene på den finanskonto, der er angivet i feltet **Realiseret gevinstkonto** eller i feltet **Realiseret tabskonto** på siden **Valutaer**. Modposter bogføres automatisk på de finansbankkonti, der er angivet i bankbogføringsgrupperne. Kørslen beregner én post pr. valuta pr. bogføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a><a name="dimensions-on-bank-account-entries"></a>Dimensioner for bankkontoposter

Reguleringsposterne for bankkontoens finanskonto og for gevinst-/tabskontoen tildeles bankkontoens standarddimensioner.

### <a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a><a name="effect-on-gl-accounts"></a>Indflydelse på finanskonti
Hvis du bogfører i en ekstra rapporteringsvaluta, kan du bruge kørslen til at oprette nye finansposter for kursreguleringer mellem den relevante regnskabsvaluta og den ekstra rapporteringsvaluta. Kørslen beregner forskellene for hver finanspost og regulerer finansposterne, afhængigt af oplysningerne i feltet **Valutakursregulering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a><a name="dimensions-on-gl-account-entries"></a>Dimensioner for finanskontoposter
Reguleringsposterne tildeles standarddimensionerne fra de konti, de bogføres på.

> [!Important]
> Før du kan bruge kørslen, skal du indtaste de kursreguleringer, som den udenlandske valutabeholdning skal reguleres efter. Det kan du gøre på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## <a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a><a name="to-set-up-a-currency-exchange-rate-service"></a>Sådan konfigureres en valutakurstjeneste
Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdateret, f.eks. FloatRates. 

> [!NOTE]
> De fleste valutakurstjenester leverer data, der er kompatible med importprocessen i [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle gange bliver dataene formateret anderledes, og du skal tilpasse importprocessen. Du kan bruge dataudvekslingsstrukturen til at gøre det ved at tilføje din egen codeunit. Du har formentlig brug for hjælp fra en udvikler til at gøre det. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valutakurstjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Valutakurstjenester** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Aktiver tjenesten til ved at slå **Aktiveret** til.

> [!NOTE]
> Følgende video viser et eksempel på, hvordan du kan oprette forbindelse til en valutakursservice med brug af den europæiske Central Bank. I den målgruppe, der beskriver, hvordan du opretter felttilknytninger, returnerer indstillingen i kolonnen til den **Overordnede node for Valutakode** kun den første valuta, der er fundet i kolonnen **Kilde**. Indstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## <a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a><a name="to-update-currency-exchange-rates-through-a-service"></a>Sådan opdateres valutakurser fra en tjeneste
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **valutaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opdater valutakurser**.

Værdien i feltet **Valutakurs** på siden **Valutaer** opdateres med den seneste valutakurs.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Se også

[Valutaer i Business Central](finance-currencies.md)  
[Definere valutaer](finance-set-up-currencies.md)  
[Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
