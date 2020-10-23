---
title: Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter | Microsoft Docs
description: For at behandle, matche og afstemme kreditorbetalinger og refusioner manuelt kan du udligne beløbet med en eller flere åbne kreditorposter.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment application, payment processing, match payments
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: b981a0062c628f3ffe3b0de8eaf4c811a13632ec
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3916822"
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Afstemme kreditorbetalinger med udbetalingskladden eller fra kreditorposter
Når du sender en betaling eller modtager en fra en kreditor, skal du beslutte, om betalingen skal udlignes eller refunderes på en eller flere åbne poster. Du kan f.eks. angive det nøjagtige beløb, som du vil udligne med betalingen, og dermed kun delvist udligne kreditorposter. Det er vigtigt, at du på et vist tidspunkt lukker (udligner) alle kreditorposter for at få korrekte kreditorstatistikker og rapporter over kontoudtog og finansændringer.

> [!NOTE]  
>   Kreditorer kan til tider refundere betalingen i stedet for at udstede en kreditnota, til modregning i fremtidige fakturaer, specielt hvis du returnerer varer, som du allerede har betalt for, eller hvor du har betalt for meget i forhold til en faktura.

Du kan udligne kreditorposter på tre forskellige måder:

* Ved at indtaste oplysninger på dedikerede sider, f.eks. på siderne **Udbetalingskladde** og **Betalingsudligningskladde**.
* Fra købskreditnotadokumenter.
* Fra kreditorposter efter at købsdokumenter er bogført, men ikke udlignet.

> [!NOTE]  
>   Hvis feltet **Udligningsmetode** på kreditorkortet indeholder **Saldo**, bliver betalinger automatisk udlignet til den ældste åbne kreditpost, hvis du ikke angiver, hvad betalingen skal udlignes til. Hvis udligningsmetoden for en kunde er **Manuel**, skal du udligne posterne manuelt.

Du kan udligne kreditorbetalinger manuelt på deres relaterede købsdokumenter, når du bogfører betalinger på siden **Udbetalingskladde**. Du kan finde oplysninger om udfyldning af udbetalingskladden [Foretage betalinger](payables-make-payments.md).

Du kan også udligne kreditorbetalinger og debitorbetalinger, når betalinger vises som negative banktransaktioner i din bank. På siden **Betalingsudligningskladde** kan du kan bruge funktioner til import af bankkontoudtog, automatisk udligning og bankkontoudligning. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Sådan udlignes en betaling med en enkelt eller flere kreditorposter
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladde**, og vælg derefter det relaterede link.
2. Angiv den relevante information om betalingsposten på første kladdelinje på siden **Udbetalingskladde**.
3. Sådan udlignes en enkelt kreditorpost:
   1. I feltet **Udligningsbilagsnr.** skal du vælge feltet for at åbne siden **Udlign kred.poster**.
   2. Vælg den post, som betalingen skal udlignes med, på siden **Udlign kred.poster**.
   3. På linjen i feltet **Beløb, der skal udlignes** skal du og indtaste beløbet, som posten skal udlignes med.
4. Sådan udlignes flere kreditorposter:

   1. Vælg handlingen **Udlign**.
   2. Vælg linjerne med de poster, som betalingen skal udlignes med på siden **Udlign kreditorposter**.
   3. Vælg handlingen **Sæt udlignings-id**.  
   4. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som posten skal udlignes med.

      Hvis du ikke indtaster et beløb, udlignes der automatisk med det maksimale beløb. Nederst på siden **Udlign kred.poster** kan du se det specifikke beløb i feltet Udligningsbeløb, og om udligningen balancerer.
5. Vælg knappen **OK**.
6. Vælg handlingen **Bogfør** for at bogføre udbetalingskladden.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Sådan udlignes en kreditnota på en eller flere kreditorposter
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købskreditnota**, og vælg derefter det relaterede link.
2. Åbn den kreditnota du vil udligne.
3. Angiv de relevante oplysninger i hovedet.
4. Hvis du vil udligne en enkelt kreditorpost, skal du i oversigtspanelet **Udligning** i feltet **Udligningsbilagsnr.** vælge den post, kreditten skal udlignes til, og derefter i feltet **Beløb, der skal udlignes** angive beløbet, der posten skal udlignes med.
5. Sådan udlignes flere kreditorposter:

   1. Vælg handlingen **Udlign**.
   2. Marker linjerne med de poster, kreditnotaen skal udlignes med.
   3. Vælg handlingen **Sæt udlignings-id**.  
   4. På linjen i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som posten skal udlignes med.

       Hvis du ikke indtaster et beløb, udlignes der automatisk med det maksimale beløb. Nederst på siden **Udlign kred.poster** kan du se det specifikke beløb i feltet **Udligningsbeløb**, og om udligningen balancerer.
6. Vælg knappen **OK**.  
   Siden **Købskreditnota** viser posten, som du valgte, i felterne **Udligningsbilagstype** og **Udligningsbilagsnr.** . Siden viser også beløbet på kreditnotaen, som skal bogføres, justeret i forhold til eventuelle kontantrabatter.
7. Vælg knappen **Bogfør** for at bogføre købskreditnotaen.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Sådan udlignes bogførte kreditorposter
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.
2. Åbn den relevante kreditor med poster, der allerede er blevet bogført.
3. Vælg handlingen **Poster**, og vælg derefter handlingen **Udlign**.
4. På siden **Udlign kred.poster** kan du se kreditorens åbne poster.
5. Markér linjen med posten, der skal udlignes.
6. Vælg handlingen **Sæt udlignings-id**.

    Feltet **Udlignings-id** viser tre stjerner, hvis du arbejder i et enkeltbrugersystem eller dit bruger-id, hvis du arbejder i et flerbrugersystem.  
7. På hver linje i feltet **Beløb, der skal udlignes** skal du indtaste det beløb, som posten skal udlignes med.

    Hvis du ikke indtaster et beløb, udlignes der automatisk med det maksimale beløb. Nederst på siden **Udlign kred.poster** kan du se beløbet i feltet **Udligningsbeløb**.
8. Vælg handlingen **Efterudlign**.  

    Siden **Efterudlign** åbnes med dokumentnummeret på udligningsposten og bogføringsdatoen for posten med den nyeste bogføringsdato.
9. Vælg **OK** for at bogføre udligningen.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Sådan udlignes kreditorposter i forskellig valuta med hinanden
Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du alligevel udligne fakturaen med betalingen.

Hvis du udligner en post (post 1) i en valuta med en post (post 2) i en anden valuta, anvendes bogføringsdatoen i post 1 til at finde relevante valutakurser til at konvertere beløb i post 2. Den relevante valutakurs findes på siden **Valutakurser**. Når det er tilfældet, skal du aktivere udligning af kreditorposter i forskellige valutaer. Du kan finde flere oplysninger under [Aktivere anvendelsen af finansposter i forskellige valutaer](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Udbetalingskladde**, og vælg derefter det relaterede link.
2. Åbn den ønskede kladde, og udfyld den første tomme kladdelinje ved hjælp af en valutakode.
3. Vælg handlingen **Udlign**.
4. Marker linjen med den post, du vil udligne posten i udbetalingskladden med, vælg handlingen **Sæt udlignings-id**, og vælg derefter den post, du vil udligne posten med.
5. Vælg knappen **OK** for at vende tilbage til udbetalingskladde.
6. Bogfør udbetalingskladde.

> [!IMPORTANT]  
>   Når du udligner poster i forskellige valutaer med hinanden, konverteres posterne til RV. Selvom valutakursen for to relevante valutaer er fast, f.eks. mellem USD og EUR, kan der være et lille restbeløb, når disse udenlandske valutabeløb konverteres til RV. Disse små restbeløb bogføres som gevinst og tab på den konto, der er angivet i feltet **Realiseret gevinstkonto** eller **Realiseret tabskonto** på siden **Valutaer**. Feltet **Beløb (RV)** tilpasses også på relevante kreditorposter.

## <a name="to-unapply-an-application-of-vendor-entries"></a>Sådan annulleres en udligning af kreditorposter
Hvis du annullerer en fejlagtig udligning, oprettes og bogføres der automatisk korrigerende poster, der er identiske med den oprindelige post, men med modsat fortegn i beløbsfeltet for alle poster, inklusive alle finansbogføringsposter, der blev afledt af udligningen, f.eks. kontantrabat og kursgevinst/tab. Alle poster, der blev lukket af programmet, genåbnes.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Leverandører (Kreditorer)**, og vælg derefter det relaterede link.
2. Åbn det relevante kreditorkort.
3. Vælg handlingen **Poster**.
4. Vælg den relevante finanspost, og vælg derefter handlingen **Annuller udligning**.
5. Du kan også vælge handlingen **Detaljerede poster**.
6. Vælg udligningsposten, og vælg derefter handlingen **Annuller udligning**.
7. Udfyld felterne i hovedet, og vælg derefter handlingen **Annuller udligning**.

> [!IMPORTANT]  
>   Hvis en post er udlignet med mere end en udligningspost, skal du fjerne udligningen af den sidste udligningspost først.

## <a name="see-also"></a>Se også
[Gæld](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
