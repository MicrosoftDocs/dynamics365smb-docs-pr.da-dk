---
title: Bruge funktionen Overfør difference til konto til at afstemme betalinger
description: 'Bruges til at behandle betalinger, der ikke kan udlignes til et dokument, f.eks. når en valutakurs medfører forskellige beløb.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="reconcile-payments-that-cannot-be-applied-automatically"></a>Afstemme betalinger, der ikke kan udlignes automatisk
Det kan være nødvendigt at håndtere betalinger til din bankkonto, der ikke kan udlignes på en relateret åben debitor-, kreditor eller bankkontopost. Det kan skyldes, at der ikke findes noget dokument i [!INCLUDE[prod_short](includes/prod_short.md)], som betalingen kan udlignes til, eller at det relaterede dokument i [!INCLUDE[prod_short](includes/prod_short.md)] har et andet beløb end f.eks. transaktionsbeløbet på grund af valutakurser. På siden **Betalingsudligningskladde** vises alle transaktionsbeløb for betalinger, som endnu ikke er udlignet, i feltet **Difference**, herunder beløb, der ikke kan udlignes af årsager som f.eks. dem ovenfor.

Metoderne til løsning af disse typer ikke-udlignede betalinger:
* Udligne manuelt
* Anvende tekst-til-kontotilknytning
* Overfør et overskydende beløb til en kladdelinje for at oprette og bogføre den påkrævede post, f.eks. en refusion af en overbetaling.

Betalinger, der ikke kan udlignes, kan blive vist på betalingsudligningskladdelinjer på følgende måder:

* Værdien i feltet **Difference** er lig med værdien i feltet **Transaktionsbeløb**, hvilket angiver, at ingen del af betalingen kan udlignes til en relateret åben debitor-, kreditor- eller bankkontopost.
* Værdien i feltet **Difference** er lavere end værdien i feltet **Transaktionsbeløb**, hvilket angiver, at en del af betalingen kan udlignes til en relateret åben debitor-, kreditor- eller bankkontopost. Den resterende del af betalingen kan ikke udlignes og skal afstemmes manuelt eller ved bogføring direkte på en konto.

Når du vil afstemme sådanne betalinger, kan du vælge handlingen **Overfør difference til konto** og derefter angive, hvilken konto beløbet i feltet **Difference** skal bogføres på, når du bogfører betalingsudligningskladden. Du kan enten gøre det fra siden **Betaling af afstemningskladde** eller fra siden **Anmeldelse af betalingsansøgning**, som du åbner ved at vælge værdien i feltet **Match tillid** eller ved at vælge feltet **Difference**.

> [!TIP]  
>   Der findes lignende funktioner, som bruges til at konfigurere automatisk afstemning af tilbagevendende betalinger, der kan udlignes på relaterede åbne debitor-, kreditor- eller bankkontoposter. Du kan finde flere oplysninger i [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## <a name="to-reconcile-payments-that-cannot-be-applied-automatically"></a>Sådan afstemmes betalinger, der ikke kan udlignes automatisk
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsudligningskladder**, og vælg derefter det relaterede link.
2. Åbne en kladde til betalingsafstemning. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. Vælg **Overfør difference til konto**. Siden **Overfør difference til konto** åbnes.
4. I feltet **Kontotype** skal du angive den kontotype, som betalingsbeløbet vil blive bogført til.
5. I feltet **Kontonr.** skal du angive den kontotype, som betalingsbeløbet vil blive bogført til.
6. I feltet **Beskrivelse** skal du angive tekst, der beskriver denne direkte betalingsbogføring. Som standard indsættes teksten i feltet **Transaktionstekst** på betalingsudligningskladdelinjen.
7. Vælg knappen **OK**.

Hvis værdien i feltet **Difference** er lig med værdien i feltet **Transaktionsbeløb**, når du har bogført betalingsudligningskladden, bliver hele betalingen på kladdelinjen bogført direkte på den angivne modkonto.

Hvis værdien i feltet **Difference** er lavere end værdien i feltet **Transaktionsbeløb**, oprettes der en ekstra kladdelinje med den samme tekst og dato og differencen indsættes i feltet **Transaktionsbeløb**. På den oprindelige kladdelinje fratrækkes differencen fra værdien i feltet **Transaktionsbeløb**, og betalingen vil forsat blive udlignet på den relaterede debitor-, kreditor- eller bankkontopost. Når du bogfører betalingsudligningskladden, bliver en del af betalingen bogført som en udlignet betaling. Den anden del af betalingen vil blive bogført direkte på den angivne konto.

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
