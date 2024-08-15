---
title: Forudsig forsinkede betalinger for salgsdokumenter
description: 'Dette element forklarer, hvordan du bruger vores forudsigelsesmodel til at forudsige, om en kunde vil betale en faktura til tiden.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'customer, payment, invoice, sales, invoice, quote'
ms.search.form: '1950, 1951,'
ms.date: 07/11/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="the-late-payment-prediction-extension"></a>Udvidelsen Forudsigelse af forsinket betaling

Det er vigtigt med effektiv styring af skyldige beløb for virksomhedens samlede finansielle tilstand. Hvis du vil reducere udestående tilgodehavender og have hjælp til at finde din indsamlingsstrategi, kan udvidelsen forudsige, om du kan forventeforsinkede betalinger. Hvis der f.eks. forudsiges en forsinkelse af en betaling, kan du vælge at justere betingelserne for betalingen eller betalingsmetoden for kunden.

## <a name="get-started"></a>Kom i gang

Når du åbner et bogført salgsdokument, vises en meddelelse øverst på siden. Når du vil bruge udvidelsen Forudsigelse af forsinket betaling, kan du tilvælge den ved at vælge **Aktiver** i meddelelsen. Du kan også konfigurere udvidelsen manuelt. Hvis du f.eks. fortryder at have afvist meddelelsen.

Du kan aktivere udvidelsen manuelt ved at gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af forudsigelse af forsinket betaling**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

> [!NOTE]
> Hvis du vælger at aktivere udvidelsen manuelt, skal du være opmærksom på, at [!INCLUDE[prod_short](includes/prod_short.md)] ikke tillader dette,, hvis modellens kvalitet er lav. Modelkvaliteten angiver, hvor nøjagtige modellens forudsigelser forventes at være. Flere faktorer kan have indflydelse på kvaliteten af en model. Det kan f.eks. være, at der ikke var nok data, eller at dataene ikke var tilstrækkeligt varierede. Du kan få vist kvaliteten af den model, du aktuelt bruger, på siden **Opsætning af forudsigelse af forsinket betaling**. Du kan også angive en mindstegrænse for modelkvaliteten.

## <a name="view-all-payment-predictions"></a>Få vist alle betalingsforudsigelser

Hvis du aktiverer udvidelsen, er feltet **Betalinger, der forventes at være forsinkede** tilgængeligt i **Virksomhedsleder** Rollecenter. Feltet viser antallet af betalinger, der forventes for at være forsinkede, og du kan åbne siden **Debitorposter**, hvor du kan få mere at vide om de bogførte fakturaer. Der er tre kolonner, du skal være opmærksom på:  

* **Forsinket betaling** - Angiver, om betalingen for fakturaen forventes at være forsinket.
* **Forudsigelseskonfidens** - Angiver, hvor pålidelig du kan betragte betalingen som. **Høj** betyder, at forudsigelsen er mindst 90 % sikker, **Mellem** ligger mellem 80 og 90 % og **Lav** er mindre end 80 %.
* **Forudsigelseskonfidens-%** - Viser den faktiske procent bag sikkerhedsvurderingen. Denne kolonne er skjult, men du kan tilføje den, hvis du vil. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

> [!TIP]
> Siden Debitorposter viser en faktaboks. Mens du gennemgår forudsigelserne, kan oplysningerne i sektionen **Debitoroplysninger** være nyttige. Når du vælger fakturaen på listen, viser sektionen oplysninger om kunden. Den gør dig også i stand til at udføre øjeblikkelige handlinger. Hvis en kunde f.eks. ofte ikke kan betale, kan du åbne debitorkortet fra faktaboksen og spærre for fremtidige salg til kunden.  

## <a name="design-details"></a>Designoplysninger

Microsoft udarbejder og anvender prognosewebtjenester i alle områder, hvor [!INCLUDE[prod_short](includes/prod_short.md)] er tilgængelig. Adgang til disse webtjenester er inkluderet i dit [!INCLUDE[prod_short](includes/prod_short.md)]-abonnement. Du kan få flere oplysninger i Licensvejledning til Microsoft Dynamics 365 Business Central. Denne vejledning kan hentes på webstedet for [Business Central](https://dynamics.microsoft.com/business-central/overview/).

Webtjenester fungerer i tre forskellige tilstande:

* Træning i model. Webtjenesten oplærer modellen med udgangspunkt i det angivne datasæt.
* Evaluering af model. Webtjenesten kontrollerer, om modellen returnerer pålidelige data for det angivne datasæt.
* Prognose. Webtjenesten anvender modellen på det angivne datasæt for at udføre en prognose.

Disse webtjenester har ingen status, hvilket betyder, at de kun bruger data til at beregne forudsigelser efter behov. De gemmer ikke data.

> [!NOTE]  
> Du kan bruge din egen prognosewebtjeneste. Du kan finde flere oplysninger i [Oprette og bruge din egen prognosewebtjeneste til forudsigelser af forsinkede betalinger](#AnchorText).

### <a name="data-required-to-train-and-evaluate-the-model"></a>Data, der kræves for at oplære og evaluere modellen

For hver **Debitorpost**, der har en relateret **Bogført salgsfaktura**:

* Beløb i lokal valuta, inkl. moms
* Betalingsbetingelser i dage beregnes som **Forfaldsdato** minus **Bogføringsdato**
* Om der er anvendt en kreditnota

Derudover er posten har aggregerede data fra andre fakturaer, der er relateret til den samme kunde.

- Samlet antal og beløb for betalte fakturaer
- Samlet antal og beløb for fakturaer, der blev betalt for sent
- Samlet antal og beløb for udestående fakturaer
- Samlet antal og beløb for udestående fakturaer, der allerede er forsinkede
- Gennemsnitlig forsinkelse i dage
- Forhold: Antal forsinket betalte/betalte fakturaer
- Forhold: Beløb på forsinket betalte/betalte fakturaer
- Nøgletal: Antal udestående forsinkede/udestående fakturaer
- Nøgletal: Beløb på udestående forsinkede/udestående fakturaer

> [!NOTE]
> Oplysningerne om debitoren medtages ikke i datasættet.

### <a name="standard-model-and-my-model"></a>Standardmodel og Min model

Udvidelsen Forudsigelse af forsinket betaling indeholder en prognosemodel, som vi har oplært ved hjælp af data, der repræsenterer en række små og mellemstore virksomheder. Når du starter bogføring af fakturaer og modtagelse af betalinger, evaluerer [!INCLUDE[prod_short](includes/prod_short.md)], om standardmodellen passer til din forretningsproces.

Hvis det viser sig, at processerne ikke svarer til standardmodellen, kan du stadig bruge udvidelsen, men du skal hente flere data. Bare fortsæt med at bruge [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Vi bruger lidt af din beregningstid hver uge, når vi vurderer og genoplærer modellen.

[!INCLUDE[prod_short](includes/prod_short.md)] kører træning og evaluering automatisk, når nok betalte og sene fakturaer er tilgængelige. Du kan dog køre det manuelt, når du vil.

#### <a name="to-train-and-use-your-model"></a>Sådan oplærer og bruger du din model

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af forudsigelse af forsinket betaling**, og vælg derefter det relaterede link.  
2. I feltet **Valgt model** skal du vælge **Min model**.
3. Vælg handlingen **Opret min model** for at oplære modellen på dine data.  

## <a name="a-nameanchortext-acreate-and-use-your-own-predictive-web-service-for-late-payment-prediction"></a><a name="AnchorText"> </a>Oprette og bruge din egen prognosewebtjeneste til forudsigelse af forsinket betaling

For [!INCLUDE[prod_short](includes/prod_short.md)] online udgives modellen af Microsoft og er forbundet med Microsoft-abonnementet. Hvis du vil have andre udrulningsmuligheder, skal du oprette Machine Learning-ressourcer i dit eget Azure-abonnement. Du kan finde eksempeltrin i [prøvelager](https://github.com/microsoft/BCTech/tree/master/samples/MachineLearning). Formålet med denne opgave er at hente API-URI'en og API-nøglen.

1. Vælg det ![lyspæreikon, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af forudsigelse af forsinket betaling**, og vælg derefter det relaterede link.  
2. Marker afkrydsningsfeltet **Brug mit Azure-abonnement**.
3. I oversigtspanelet **Brug mit Azure-abonnement** skal du angive API-URL-adressen og API-nøglen til din model.  

## <a name="see-also"></a>Se også

[Tilpasse Business Central ved hjælp af udvidelser](ui-extensions.md)    
[Velkommen til [!INCLUDE[prod_long](includes/prod_long.md)]](welcome.md)    
[Brug kunstig intelligens i Microsoft Dynamics 365 Business Central](/training/paths/use-artificial-intelligence/)    
[Forudsigelse for API-oversigt](/dynamics365/business-central/dev-itpro/developer/ml-prediction-api-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
