---
title: Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter
description: Bruges til at udligne debitorindbetalinger eller refusioner til en eller flere åbne debitorposter. Dette er en del af afstemning af debitorbetalinger.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 04/01/2021
ms.author: edupont
---
# Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter

Når du modtager en kontantbetaling fra en debitor, eller du foretager en kontantrefusion, skal du vælge, om betalingen skal lukke en eller flere åbne debet- eller kreditposter. Du kan angive det beløb, du vil udligne. Du kan f.eks. udligne delbetalinger til debitorposter. Når du lukker debitorposter, sikrer du, at oplysninger som debitorstatistik, kontoudtog og rentenotaer er opdaterede.

> [!TIP]  
>   På siden **Debitorposter** betyder rød skrift, at den tilhørende betaling har overskredet forfaldsdatoen. Hvis forfaldne beløb bliver et problem, kan vi hjælpe dig med at reducere hyppigheden af dem. Du kan aktivere udvidelsen **Forudsigelser af forsinkede betalinger**, som bruger en forudsigelsesmodel, der blev udviklet i Azure Machine Learning til at forudsige tidspunktet for betalinger. Disse forudsigelser hjælper dig med at reducere udestående tilgodehavender og finjustere din indsamlingsstrategi. Hvis der f.eks. forudsiges en forsinkelse af en betaling, kan du vælge at justere betingelserne for betalingen eller betalingsmetoden for kunden. Du kan finde flere oplysninger i [Forudsigelser af forsinkede betalinger](ui-extensions-late-payment-prediction.md).  

Du kan udligne debitorposter på forskellige måder:

* Når du angiver oplysninger på dedikerede sider:
    * Siden **Betalingsudligningskladde**. Du kan finde flere oplysninger i [Udligne betalinger automatisk og afstemme bankkonti](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * Siden **Betalingsregistrering**. Du kan finde flere oplysninger i [Afstemme debitorbetalinger på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).
    * **Indbetalingskladde**. Denne indstilling beskrives nedenfor.
* Ved at udfylde feltet **Udligningsbilagsnr.** på salgskreditnotadokumenter. Denne indstilling beskrives nedenfor.
* Ved hjælp af handlingen **Sæt udlignings-id** på en debitorpost. Denne indstilling beskrives nedenfor.
* Ved at bruge handlingen **Udlign poster** på siden **Bankindbetalinger** og derefter angive fakturanummeret i feltet **Udlignings-id**. Du kan finde flere oplysninger i [Oprette bankindskud](bank-create-bank-deposits.md).

> [!NOTE]  
>   Hvis feltet **Udligningsmetode** på debitorkortet indeholder **Saldo**, bliver betalinger automatisk udlignet til den ældste åbne kreditpost, medmindre du foretager en manuel angivelse. Hvis udligningsmetoden er **Manuel**, skal du altid udligne posterne manuelt.

## Sådan udfyldes og bogføres en indbetalingskladde
Indbetalingskladden er en type finanskladde. Du kan bruge det til at bogføre på finanskonti, bankkonti, debitor- og kreditorkonti og anlægskonti. Du kan anvende betalingen på en eller flere debetposteringer, når du bogfører betalingen. Du kan også udligne fra de bogførte posteringer senere.
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger kladde**.
3. Vælg den ønskede kladde i feltet **Kladdenavn**.
4. Udfyld feltet **Bogføringsdato**.  
5. I feltet **Bilagstype** skal du vælge **Betaling**.

    Der indsættes et nummer i feltet **Bilagsnr.**, som hentes fra den Nummerserie, der er tildelt kladden.  
6. Brug feltet **Eksternt bilagsnr.** til at lagre et id, som f.eks. debitorens checknummer.
7. I feltet **Kontotype** skal du vælge **Debitor**.
8. Vælg den relevante bankkonto i feltet **Kontonr.**.
9. Hvis du vil foretage efterudligningen på samme tid, som du bogfører kladden, skal du gøre et af følgende.
10. I feltet **Modkontotype** skal du vælge **Finanskonto** til kontantindbetalinger og **Bankkonto** til andre betalinger.
11. Vælg kontantkontoen til kontantindbetalinger eller bankkontoen til andre betalinger i feltet **Modkonto**.
12. Bogfør journalen.

## Sådan udlignes en betaling med en enkelt debitorpost
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger kladde**.
3. Angiv de relevante oplysninger om den post, der skal udlignes, i den første indkøbskladdelinje.
4. I feltet **Bilagstype** skal du angive **Betaling**.
5. I feltet **Kontotype** skal du angive **Debitor**.
6. I feltet **Modkontotype** skal du angive **Bankkonto**.
7. I feltet **Udligningsbilagsnr.** skal du vælge feltet for at åbne siden **Udlign debitorposter**.
8. Vælg den post, som betalingen skal udlignes med, på siden **Udlign debitorposter**.
9. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.

    Nederst på siden **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
10. Vælg knappen **OK**. Siden **Indbetalingskladde** viser nu posten i felterne **Udligningsbilagstype** og **Udligningsbilagsnr.**.
11. Bogfør indbetalingskladden.

## Sådan udlignes en betaling med flere debitorposter:
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger kladde**.
3. Angiv de relevante oplysninger om den post, der skal udlignes, i den første indkøbskladdelinje.
4. I feltet **Bilagstype** skal du angive **Betaling**.
5. I feltet **Kontotype** skal du angive **Debitor**.
6. I feltet **Modkontotype** skal du angive **Bankkonto**.
7. I feltet **Beløb** skal du angive den fulde betaling som et negativt beløb.
8. Hvis du vil udligne betalingen med flere debitorposter, når du bogfører, skal du vælge handlingen **Udlign poster**.  
9. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id**.  
10. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.

    Nederst på siden **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
11. Vælg knappen **OK**.
12. Bogfør indbetalingskladden.

## Sådan udlignes en kreditnota på en enkelt debitorpost
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Åbn den relevante salgskreditnota.
3. Hvis du vil udligne kreditnotaen med en enkelt debitorpost i forbindelse med bogføringen, skal du i feltet **Udligningsbilagsnr.** vælge den post, som du vil udligne betalingen med.
4. På linjen i feltet **Beløb, der skal udlignes** skal du og indtaste beløbet, som du vil udligne posten med.  

    Hvis du ikke indtaster et beløb, udligner programmet automatisk det maksimale beløb. Nederst på siden **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.    
5. Vælg knappen **OK**. Siden **Salgskreditnota** viser nu posten, som du valgte, i felterne **Udligningsbilagstype** og **Udligningsbilagsnr.**. Og beløbet på kreditnotaen, som skal bogføres, reguleres i forhold til mulige kontantrabatter.
6. Bogfør kreditnotaen.

## Sådan udlignes en kreditnota med flere debitorposter
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Åbn den relevante salgskreditnota.
3. Hvis du vil udligne kreditnotaen med flere debitorposter, når du bogfører, skal du vælge handlingen **Udlign poster**.
4. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id**.
5. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.  

    Nederst på siden **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
6. Vælg knappen **OK**. Siden viser nu **Salgskreditnota** beløbet på kreditnotaen, som skal bogføres, justeret i forhold til eventuelle kontantrabatter.
7. Bogfør kreditnotaen.

## Sådan udlignes bogførte debitorposter
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn debitorkortet for debitoren med de poster, du vil udligne.
3. Vælg handlingen **Poster**, og vælg derefter linjen med den post, som betalingen skal udlignes med.
4. Vælg handlingen **Udlign**. Siden **Udlign debitorposter** åbnes, så du kan se debitorens åbne poster.
5. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id** .
6. På hver linje i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.  

    Nederst på siden **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**.  
7. Vælg handlingen **Efterudlign**. Siden **Efterudlign** vises med dokumentnummeret på udligningsposten og bogføringsdatoen for posten med den nyeste bogføringsdato.  
8. Vælg **OK** for at bogføre udligningen.

    Hvis den bogførte udligning har resulteret i lukkede debitorposter, vil der ikke længere være en markering for disse poster i feltet **Åbn**.    
9. Du kan se sagsposter ved at vælge den ![lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link. Find kortet for den relevante debitor for at få vist posterne.  

På oversigten over poster kan du se, at afkrydsningsfeltet **Åben** ikke er markeret på den linje, der indeholder finansposten, der blev fuldt udlignet.  

> [!NOTE]  
>   Når du har valgt en post på siden **Udlign debitorposter** eller flere poster ved at indstille feltet **Udlignings-id**, indeholder feltet **Udlignet beløb** på kladdelinjen summen af de resterende beløb for de bogførte poster, som du valgte - medmindre feltet allerede indeholder noget. Hvis du markerer **Saldo** i feltet **Udligningsmetode** på debitorkortet, sker udligningen automatisk.

## Sådan udlignes debitorposter i andre valutaer med hinanden
Hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du stadig knytte fakturaen til betalingen.  

Her er et eksempel. Du udligner post 1 i én valuta til post 2 i en anden valuta. Bogføringsdatoen i post 1 bruges til at finde den valutakurs, der skal bruges til omregning af beløb i post 2. Den relevante valutakurs findes på siden **Valutakurser**.  

Udligning af debitorposter i andre valutaer skal være aktiveret. Du kan finde flere oplysninger i [Aktivere anvendelsen af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Åbn den ønskede kladde, og udfyld den første tomme kladdelinje ved hjælp af en valutakode.
3. Vælg handlingen **Udlign**.
4. Marker linjen med den post, du vil udligne posten i indbetalingskladden med, vælg handlingen **Sæt udlignings-id**, og vælg derefter den post, du vil udligne posten med.
5. Vælg knappen **OK** for at vende tilbage til indbetalingskladde.
6. Bogfør salgskladden.  

> [!IMPORTANT]  
>   Når du udligner poster i forskellige valutaer, konverteres posterne til RV. Selvom valutakursen for de to valutaer er fast, f.eks. mellem USD og EUR, kan der være et lille restbeløb, når de konverteres til RV. Disse små restbeløb bogføres som gevinst og tab på den konto, der er angivet i feltet **Realiseret gevinstkonto** eller feltet **Realiseret tabskonto** på siden **Valutaer**. Feltet **Beløb (RV)** tilpasses også på kreditorposter.  

## Sådan rettes en udligning af debitorposter
Når du retter en udligning, oprettes der korrigerende poster, som bogføres for alle poster. De korrigerende poster er de samme som originalerne, men har en modsat log i feltet **Beløb**. De korrigerende poster omfatter alle finansposter, der er afledt af udligningen. F.eks. kontantrabatten og tab/gevinst. Alle poster, der blev lukket af programmet, genåbnes.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort.
3. Vælg handlingen **Poster**.
4. Vælg den relevante finanspost, og vælg derefter handlingen **Annuller udligning**.
5. Du kan også vælge handlingen **Detaljerede poster**.
6. Vælg udligningsposten, og vælg derefter handlingen **Annuller udligning**.
7. Udfyld felterne i hovedet, og vælg derefter handlingen **Annuller udligning**.  

> [!IMPORTANT]  
>   Hvis en post er udlignet med mere end en udligningspost, skal du fjerne udligningen af den sidste udligningspost først.  

## Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]