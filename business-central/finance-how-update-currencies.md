---
title: Opdatere valutakurser
description: 'Få mere at vide om, hvordan du kan bruge Business Central til at justere valutakurser i forskellige valutaer.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'multiple currencies, adjust exchange rates, FX rates'
ms.search.form: '5, 118'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Opdatere valutakurser

Hvis du handler i forskellige valutaer, skal du holde styr på ændringerne i valutakurserne. [!INCLUDE [prod_short](includes/prod_short.md)] hjælper dig med at holde styr på og opdatere valutakurserne manuelt eller automatisk og med at oprette en valutakurstjeneste.

## Valutaer

> [!TIP]  
> Du kan finde realtidsoplysninger om valutakurser (fx) eller historiske kurser under termen valuta i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md).

[!INCLUDE [finance-currencies-def](includes/finance-currencies-def.md)]

Du kan angive valutakoder i **valutaerne**, herunder yderligere oplysninger og indstillinger, der er nødvendige for hver valutakode. Der er flere oplysninger i [Valutaer](finance-set-up-currencies.md#curr)

### Eksempel på en valutapostering for tilgodehavender

[!INCLUDE [finance-currencies-example](includes/finance-currencies-example.md)]

## Valutakurser

Valutakurserne er værktøjet til beregning af den lokale valutaværdi (RV) for hver valuta transaktion. Siden **Valutakurser** indeholder følgende felter:

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Startdato**|Den dato, hvor valuta kursen blev gældende.|  
|**Valutakode**|Den valutakode, der er knyttet til denne valutakurs.|  
|**Associeret valutakode**|Hvis valutaen er en del af en trekants beregning, kan den relaterede valutakode oprettes her.|  
|**Valutakursbeløb**|Valutakursbeløbet er den kurs, der skal bruges til den valutakode, der er valgt på linjen. Normalt 1 eller 100.|  
|**Associeret valutakursbeløb**|Det forholdsmæssige valutakursbeløb er den kurs, der skal bruges til den forholdsmæssige valutakode.|  
|**Regul. valutakursbeløb**|Den valutakode, der er valgt på linjen til brug af kørslen **Kursregulering af valutabeholdninger**.|  
|**Ass. regul. valutakursbeløb**|Den valutakode, der er valgt på linjen til brug af kørslen **Kursregulering af valutabeholdninger**.|  
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

## Regulere valutakurser

Fordi valutakurser svinger hele tiden, skal andre valutaer i systemet reguleres med jævne mellemrum. Hvis du ikke gør det, kan beløb, som du har omregnet fra udenlandske (eller andre) valutaer og bogført i finansregnskabet i lokal valuta, være forkerte. Du skal desuden opdatere daglige poster, der er bogført, før du angiver en daglig valutakurs.

Du kan bruge **Juster valutakurser** til at regulere valutakursen manuelt for bogførte kunde-, leverandør- og bankkontoposter. Kørslen opdaterer også opdatere andre rapporteringsvalutabeløb i finansposter.  

> [!TIP]
> Du kan bruge en service til automatisk at opdatere valutakurser i systemet. Du kan finde flere oplysninger i [Sådan konfigureres en valutakurstjeneste](finance-how-update-currencies.md#set-up-a-currency-exchange-rate-service). Dette regulerer imidlertid ikke valutakurser for allerede bogførte transaktioner. Hvis du vil opdatere valutakurser for bogførte poster, skal du bruge kørslen **Kursreguler valutabeholdninger**.

Du kan også angive, hvordan dimensioner for justeringerne håndteres for gevinst-og tabs posteringer ved at vælge en af følgende indstillinger i feltet **Overfør bogføring**:  

* **Kildepostdimensioner**: Overfør dimensionsværdier for finansposter for urealiserede gevinster og tab fra den justerede post.  
* **Ingen dimensioner**: Undlad at overføre dimensionsværdier for urealiserede gevinster og tab til Finansposter. [!INCLUDE [prod_short](includes/prod_short.md)] vil stadig bruge standarddimensionsindstillinger, f.eks. **Kode obligatorisk**, **Samme kode** eller **Ingen kode**. Hvis kildetransaktionsposterne har dimensionsværdier, oprettes der poster uden dimensionsværdier.  
* **Finanskontodimensioner**: Overfør dimensionsværdier fra urealiserede gevinster og tab på finanskontoens dimensionsindstillinger fra kildeposten til finanskontoposter.

> [!NOTE]
> Hvis du vil bruge prøveversionen, skal du aktivere funktionen **Funktionsopdatering: Aktivér brug af ny valutakursregulering, der kan udvides, herunder funktionen til gennemgang af bogføring** for siden **[Funktionsstyring](https://businesscentral.dynamics.com/?page=2610)**.

> [!IMPORTANT]
> På grund af lokale krav i Schweiz anbefaler vi ikke, at du aktiverer **Funktionsopdatering: Aktivér brug af ny valutakursregulering, der kan udvides, herunder bogføringsgennemgang** i den schweiziske (CH) landeversion.

## Få vist effekten af en justering

Du kan få vist den effekt, som en justering af en valutakurs har ved bogføring, inden du bogfører ved at vælge **Forhåndsversion** på siden **Justering af kursvalutaer** (Report 596). På anmodningssiden kan du angive, hvad der skal medtages i eksemplet:

* Hent en detaljeret bogføring på en finanspost efter bogføring.
* Få en opsummeret bogføring efter valuta. Du skal blot vælge feltet **Reguler pr. post** i rapporten **Regulering af valutakurser**.

### Indflydelse på debitorer og kreditorer

Det gælder for debitor- og kreditorkonti, at kørslen bruger den valuta, der er gældende på den bogføringsdato, der er angivet i kørslen, for at justere valutaen. Kørslen beregner forskellene i de enkelte valutaopgørelser og bogfører beløbene på den finanskonto, der er angivet i feltet **Urealiseret gevinstkonto** eller i feltet **Urealiseret tabskonto** på siden **Valutaer**. Modposteringer bogføres automatisk på samlekontoen i finansbogholderiet.

Kørslen gennemgår alle åbne debitor- og kreditorposter. Hvis der er en kursdifference for en post, oprettes der en ny detaljeret debitor- eller leverandørpost. Den nye post afspejler det justerede beløb i debitor- eller kreditorposten.

#### Dimensioner for debitor- og kreditorposter

[!INCLUDE [prod_short](includes/prod_short.md)] tildeler dimensionerne fra debitor-/kreditorposter, og reguleringerne bogføres pr. kombination af dimensionsværdier.

### Indflydelse på bankkonti

Det gælder for bankkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene for hver bankkonto, der er blevet tildelt en valutakode, og bogfører beløbene på den finanskonto, der er angivet i feltet **Realiseret gevinstkonto** eller i feltet **Realiseret tabskonto** på siden **Valutaer**. Modposter bogføres automatisk på de finansbankkonti, der er angivet i bankbogføringsgrupperne. Kørslen beregner én post pr. valuta pr. bogføringsgruppe.

#### Dimensioner for bankkontoposter

Reguleringsposterne for bankkontoens finanskonto og for gevinst-/tabskontoen tildeles bankkontoens standarddimensioner.

### Indflydelse på finanskonti

Hvis du bogfører i en anden rapporteringsvaluta, kan kørslen oprette nye finansposter for kursreguleringer mellem den lokale valutaer og andre rapporteringsvalutaer. Batchjobbet beregner forskellene for hver hovedbogspost. Det beregner kladdeposten på finansbogholderiet, afhængigt af oplysningerne i feltet **Valutakursregulering** for hver finanskonto.

#### Dimensioner for finanskontoposter

Reguleringsposterne tildeles standarddimensionerne fra de konti, de bogføres på.

> [!Important]
> Før du kan bruge kørslen, skal du indtaste de kursreguleringer, som den udenlandske valutabeholdning skal reguleres efter. Det kan du gøre på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

## Konfigurere en valutakurstjeneste

Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdaterede.

> [!NOTE]
> De fleste valutakurstjenester leverer data, der er kompatible med importprocessen i [!INCLUDE[prod_short](includes/prod_short.md)]. Nogle gange bliver dataene formateret anderledes, og du skal tilpasse importprocessen. Du kan bruge dataudvekslingsstrukturen til at gøre det ved at tilføje din egen codeunit. Du har formentlig brug for hjælp fra en udvikler til at gøre det. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Valutakurstjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Valutakurstjenester** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Knyt felterne fra XML-filen til valutakurstabellen i kildefeltet.
5. Anvend alle nødvendige transformationsregler.
6. Aktiver tjenesten til ved at slå **Aktiveret** til.

> [!NOTE]
> Følgende video viser et eksempel på, hvordan du kan oprette forbindelse til en valutakursservice med brug af den europæiske Central Bank. I den målgruppe, der beskriver, hvordan du opretter felttilknytninger, returnerer indstillingen i kolonnen til den **Overordnede node for Valutakode** kun den første valuta, der er fundet i kolonnen **Kilde**. Indstillingen skal være `/gesmes:Envelope/Code/Code/Code`.

<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4A1jy?rel=0]

## Opdater valutakurser fra en tjeneste

Følg trinene for at opdatere valutakurserne gennem en tjeneste:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **valutaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opdater valutakurser**.

## Ret fejl

Nu og da skal du muligvis rette en fejl i en betalingstransaktion, der er forbundet med justeringer af gevinster og tab i udenlandsk valuta. Du kan bruge handlingen **Tilbagefør transaktion** på siderne **Bankposter**, **Debitorposter** og **Kreditorposter** til at fortryde og tilbageføre betalingstransaktionen.

> [!NOTE]
> Når du annullerer og tilbagefører en betaling for en post, der var genstand for valutakursreguleringer, bogføres tilbageførselsposter for reguleringerne. Du skal muligvis køre valutakursreguleringen igen for at få den korrekte aktuelle saldo.

## Se også

[valutaer i Business Central](finance-currencies.md)  
[Definere valutaer](finance-set-up-currencies.md)  
[Konfigurere en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
