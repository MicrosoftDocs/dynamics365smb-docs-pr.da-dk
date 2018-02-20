---
title: Udligne debitorposter for manuelt at afstemme debitorbetalinger | Microsoft Docs
description: "Bruges til at udligne debitorindbetalinger eller refusioner til en eller flere åbne debitorposter og afstemme betalinger fra debitorer."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6e00e9cbc1b1dc8674ccf83876809496a563b0be
ms.contentlocale: da-dk
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-customer-payments-manually"></a>Afstemme debitorbetalinger manuelt
Når du modtager en kontaktrefusion fra en debitor, eller du foretager en kontantrefusion, skal du vælge, om betalingen skal udlignes eller refunderes for at lukke en eller flere åbne debet- eller kreditposter. Du kan angive det beløb, du vil udligne. Du kan f.eks. udligne delbetalinger til debitorposter. Når du lukker debitorposter, sikrer du, at oplysninger som debitorstatistik, kontoudtog og rentenotaer er korrekte.

> [!NOTE]  
>   I vinduet **Debitorposter** betyder rød skrift, at den tilhørende betaling har overskredet forfaldsdatoen.

Du kan udligne debitorposter på forskellige måder:

* Ved at indtaste oplysninger i dedikerede vinduer, f.eks. vinduerne **Indbetalingskladde** og **Betalingsudligningskladde**.
* Fra salgskreditnotadokumenter.
* Fra debitorposter efter at salgsdokumenter er bogført, men ikke udlignet.

> [!NOTE]  
>   Hvis feltet **Udligningsmetode** på debitorkortet indeholder **Saldo**, bliver betalinger automatisk udlignet til den ældste åbne kreditpost, medmindre du foretager en manuel angivelse. Hvis udligningsmetoden er **Manuel**, skal du altid udligne posterne manuelt.

Du kan anvende debitorbetalinger manuelt i vinduet **Indbetalingskladde**. Indbetalingskladden er en form for finanskladde, og derfor kan den bruges, når der bogføres transaktioner til finans-, bank-, debitor-, kreditor- og anlægskonti. Du kan anvende betalingen på en eller flere debetposteringer, når du bogfører betalingen, eller du kan anvende fra de bogførte posteringer senere.

Du kan også anvende debitor- og kreditorbetalinger i vinduet **Betalingsudligningskladde** ved hjælp af funktioner til import af bankkontoudtog, automatisk udligning og bankkontoudligning. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md). Du kan også afstemme debitorbetalinger, der er baseret på en liste over ubetalte salgsdokumenter i vinduet **Betalingsregistrering**. Du kan finde flere oplysninger under [Afstemme debitorbetalinger på en liste over ubetalte salgsdokumenter](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md).

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Sådan udfyldes og bogføres en indbetalingskladde
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indbetalingskladde**, og vælg derefter det relaterede link.
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

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Sådan udlignes en betaling med en enkelt debitorpost
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indbetalingskladde**, og vælg det relaterede link.
2. Vælg handlingen **Rediger kladde**.
3. Angiv de relevante oplysninger om den post, der skal udlignes, i den første indkøbskladdelinje.
4. I feltet **Bilagstype** skal du angive **Betaling**.
5. I feltet **Kontotype** skal du angive **Debitor**.
6. I feltet **Modkontotype** skal du angive **Bankkonto**.
7. I feltet **Udligningsbilagsnr.** skal du vælge feltet for at åbne vinduet **Udlign debitorposter**.
8. Vælg den post, som betalingen skal udlignes med, i vinduet **Udlign debitorposter**.
9. I feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.

    Nederst i vinduet **Udlign debitorposter**, kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
10. Vælg knappen **OK**. Vinduet **Indbetalingskladde** viser nu posten, som du valgte, i felterne **Udligningsbilagstype** og **Udligningsbilagsnr.**.
11. Bogfør indbetalingskladden.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Sådan udlignes en betaling med flere debitorposter:
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Vælg handlingen **Rediger kladde**.
3. Angiv de relevante oplysninger om den post, der skal udlignes, i den første indkøbskladdelinje.
4. I feltet **Bilagstype** skal du angive **Betaling**.
5. I feltet **Kontotype** skal du angive **Debitor**.
6. I feltet **Modkontotype** skal du angive **Bankkonto**.
7. I feltet **Beløb** skal du angive den fulde betaling som et negativt beløb.
8. Hvis du vil udligne betalingen med flere debitorposter, når du bogfører, skal du vælge handlingen **Udlign poster**.  
9. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id**.  
10. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.

    Nederst i vinduet **Udlign debitorposter**, kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
11. Vælg knappen **OK**.
12. Bogfør indbetalingskladden.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Sådan udlignes en kreditnota på en enkelt debitorpost
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Åbn den relevante salgskreditnota.
3. Hvis du vil udligne kreditnotaen med en enkelt debitorpost i forbindelse med bogføringen, skal du i feltet **Udligningsbilagsnr.** vælge den post, som du vil udligne betalingen med.
4. På linjen i feltet **Beløb, der skal udlignes** skal du og indtaste beløbet, som du vil udligne posten med.  

    Hvis du ikke indtaster et beløb, udligner programmet automatisk det maksimale beløb. Nederst i vinduet **Udlign debitorposter**, kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.    
5. Vælg knappen **OK**. Vinduet **Salgskreditnota** viser nu posten, som du valgte, i felterne **Udligningsbilagstype** og **Udligningsbilagsnr.**. Og beløbet på kreditnotaen, som skal bogføres, reguleres i forhold til mulige kontantrabatter.
6. Bogfør kreditnotaen.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Sådan udlignes en kreditnota med flere debitorposter
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgskreditnotaer**, og vælg derefter det relaterede link.
2. Åbn den relevante salgskreditnota.
3. Hvis du vil udligne kreditnotaen med flere debitorposter, når du bogfører, skal du vælge handlingen **Udlign poster**.
4. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id**.
5. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.  

    Nederst i vinduet **Udlign debitorposter**, kan du se det specifikke beløb i feltet **Udligningsbeløb**, og også om udligningen balancerer.  
6. Vælg knappen **OK**. Vinduet viser nu **Salgskreditnota** beløbet på kreditnotaen, som skal bogføres, justeret i forhold til eventuelle kontantrabatter.
7. Bogfør kreditnotaen.

## <a name="to-apply-posted-customer-ledger-entries"></a>Sådan udlignes bogførte debitorposter
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn debitorkortet for debitoren med de poster, du vil udligne.
3. Vælg handlingen **Poster**, og vælg derefter linjen med den post, som betalingen skal udlignes med.
4. Vælg handlingen **Udlign**. Vinduet **Udlign debitorposter** åbnes, så du kan se debitorens åbne poster.
5. Vælg linjer med poster, som du ønsker, at udligningsposten skal udlignes med, og derefter vælge handlingen **Sæt udlignings-id** .
6. På hver linje i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som du vil udligne med posten. Hvis du ikke indtaster et beløb, udlignes der med det maksimale beløb.  

    Nederst i vinduet **Udlign debitorposter** kan du se det specifikke beløb i feltet **Udligningsbeløb**.  
7. Vælg handlingen **Efterudlign**. Vinduet **Efterudlign** med dokumentnummeret på udligningsposten vises, og bogføringsdatoen på posten med den nyeste bogføringsdato.  
8. Vælg **OK** for at bogføre udligningen.

    Hvis den bogførte udligning har resulteret i lukkede debitorposter, vil der ikke længere være en markering for disse poster i feltet **Åbn**.    
9. Hvis du vil se posterne skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Debitorer** og derefter vælge det relaterede link. Find kortet for den relevante debitor for at få vist posterne.  

På oversigten over poster kan du se, at afkrydsningsfeltet **Åben** ikke er markeret på den linje, der indeholder finansposten, der blev fuldt udlignet.  

> [!NOTE]  
>   Når du har valgt en post i vinduet **Udlign debitorposter** eller flere poster ved at indstille feltet **Udlignings-id**, indeholder feltet **Udlignet beløb** på kladdelinjen summen af de resterende beløb for de bogførte poster, som du valgte - medmindre feltet allerede indeholder noget. Hvis du markerer **Saldo** i feltet **Udligningsmetode** på debitorkortet, sker udligningen automatisk.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Sådan udlignes debitorposter i andre valutaer med hinanden
Hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du stadig knytte fakturaen til betalingen.  

Hvis du udligner en post (post 1) i en valuta med en post (post 2) i en anden valuta, anvendes bogføringsdatoen i post 1 til at finde relevante valutakurser til at konvertere beløb i post 2. Den relevante valutakurs findes i vinduet **Valutakurser**.  

Udligning af debitorposter i andre valutaer skal være aktiveret. Du kan finde flere oplysninger under [Aktivere anvendelsen af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indbetalingskladde**, og vælg derefter det relaterede link.
2. Åbn den ønskede kladde, og udfyld den første tomme kladdelinje ved hjælp af en valutakode.
3. Vælg handlingen **Udlign**.
4. Marker linjen med den post, du vil udligne posten i indbetalingskladden med, vælg handlingen **Sæt udlignings-id**, og vælg derefter den post, du vil udligne posten med.
5. Vælg knappen **OK** for at vende tilbage til indbetalingskladde.
6. Bogfør salgskladden.  

> [!IMPORTANT]  
>   Når du udligner poster i forskellige valutaer, konverteres posterne til RV. Selvom valutakursen for de to valutaer er fast, f.eks. mellem USD og EUR, kan der være et lille restbeløb, når de konverteres til RV. Disse små restbeløb bogføres som gevinst og tab på den konto, der er angivet i feltet **Realiseret gevinstkonto** eller feltet **Realiseret tabskonto** i vinduet **Valutaer**. Feltet **Beløb (RV)** tilpasses også på kreditorposter.  

## <a name="to-correct-an-application-of-customer-entries"></a>Sådan rettes en udligning af debitorposter
Hvis du retter en udligning, oprettes og bogføres der automatisk korrigerende poster, der er identiske med den oprindelige post, men med modsat fortegn i beløbsfeltet for alle poster, inklusive alle finansbogføringsposter, der blev afledt af udligningen, f.eks. kontantrabat og kursgevinst/tab. Alle poster, der blev lukket af programmet, genåbnes.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn det relevante debitorkort.
3. Vælg handlingen **Poster**.
4. Vælg den relevante finanspost, og vælg derefter handlingen **Annuller udligning**.
5. Du kan også vælge handlingen **Detaljerede poster**.
6. Vælg udligningsposten, og vælg derefter handlingen **Annuller udligning**.
7. Udfyld felterne i hovedet, og vælg derefter handlingen **Annuller udligning**.  

> [!IMPORTANT]  
>   Hvis en post er udlignet med mere end en udligningspost, skal du fjerne udligningen af den sidste udligningspost først.  

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

