---
title: Oprette Tilknytning af tekst til konto for tilbagevendende betalinger
description: 'Du kan sammenkæde tekst på betalinger med bestemte konti, så betalinger bogføres på kontiene, når du bogfører betalingsudligningskladden.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti

På siden **Tekst til kontotilknytning**, som du kan åbne fra siden **Betalingsudligningskladde**, kan du oprette tilknytninger mellem tekst på betalinger og specifikke debet-, kredit- og modkonti, så disse betalinger bliver bogført på de angivne konti, når du bogfører kladden til betalingsafstemning.

Der findes lignende funktioner til afstemning af overskydende beløb på betalingsudligningskladdelinjer på ad hoc-basis. Du kan finde flere oplysninger i [Afstemme betalinger, der ikke kan udlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md).

Betalinger, der er bogført baseret på tekst-til-kontotilknytning, udlignes ikke på åbne poster, men bliver blot bogført på de angivne konti i tillæg til at oprette finansposter på bankkonti. Derfor er tekst til kontotilknytning velegnet til tilbagevendende indbetalinger eller udgifter såsom hyppige køb af benzin eller bankgebyrer og -renter, der regelmæssigt forekommer på bankens kontoudtog, og ikke behøver et relateret forretningsdokument. Der er yderligere oplysninger i "Eksempel: Tekst-til kontotilknytning for udgift til benzin" under dette emne.

> [!NOTE]  
>   Betalinger på afstemningslinjerne i kladden er kun angivet til bogføring i overensstemmelse med tekst-til-kontotilknytning, hvis den automatiske udligningsfunktion kun kan give en udligningstillid af **Lav** eller **Mellem**. Hvis den automatiske udligningsfunktion indeholder matchtilliden Høj, bliver betalingen automatisk udlignet til en eller flere åbne poster, og betalingen bogføres ikke på de konti, der er angivet på siden **Tekst til kontotilknytning**. Med andre ord tilsidesætter udligningstilliden **Høj** en tekst-til-kontotilknytning.

På en betalingsudligningskladdelinje, hvor betalingen er angivet til bogføring i overensstemmelse med tekst-til-kontotilknytning, indeholder feltet **Matchtillid** **Høj – Tekst-til-kontotilknytning**, og felterne **Kontotype** og **Kontonr.** indeholder de tilknyttede konti.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Sådan knytter du tekst på tilbagevendende betalinger til automatisk afstemning af konti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsudligningskladder**, og vælg derefter det relaterede link.
2. Åbne en kladde til betalingsafstemning. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. Vælg handlingen **Knyt tekst til konto**. Siden **Tekst til kontotilknytning** åbnes.
4. Brug feltet **Koblingstekst** til at angive tekst, der forekommer på betalinger, du vil bogføre på de angivne konti uden udligning til en åben post. Du kan angive op til 50 tegn.

    > [!NOTE]  
    >   Hvis der ikke findes andre betalinger med den pågældende tilknytningstekst, kan teksten til kontotilknytning optræde, selv om kun en del af teksten på betalingen findes som en tilknytningstekst.
5. I feltet **Kreditornummer** skal du angive den kreditor, som betalingerne skal bogføres på.
6. Brug feltet **Modkontokildetype** til at angive, om betalingen skal bogføres på en finanskonto eller en debitor- eller kreditorkonto.
7. I feltet **Modkontokildenr.** skal du angive den konto, som betalingen vil blive bogført til, afhængig af valget i feltet **Modkontokildetype**.

    > [!NOTE]
    > Brug ikke felterne **Debetkontonr.** og **Kreditkontonr.** i forbindelse med afstemning af betaling. De bruges kun til indgående bilag. Du kan finde flere oplysninger i [Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).

8. Gentag trin 3 til 7 for al tekst på betalinger, du vil knytte til konti til direkte bogføring uden udligning.

Næste gang du importerer en bankkontofil eller vælge handlingen **Udlign automatisk** på siden **Betalingsudligningskladde**, vil kladdelinjerne til betalinger, der indeholder den angivne tilknytningstekst, indeholde tilknyttede konti i felterne **Kontotype** og **Kontonr.**. Feltet **Matchtillid** indeholder **Høj - Tilknytning af tekst til konto**. Det er på betingelse af, at den automatiske udligningsfunktion kun kan give en udligningstillid af **Lav** eller **Mellem**.

## <a name="example-text-to-account-mapping-for-bank-fees"></a>Eksempel: Tekst-til kontotilknytning for udgift til benzin

Hvis du altid vil bogføre udgifter, der er knyttet til gebyrer fra en bestemt bank, MyBank til finanskontoen for bankens gebyrer og gebyrer (konto 60400), skal du udfylde en linje på **siden til tilknytning af tekst til konto på** følgende måde.

| Koblingstekst | Debetkontonr. | Kreditkontonr. | Modkontokildetype | Modkontokildenr. |
| --- | --- | --- | --- | --- |
| MyBank |TOM |60400|Finanskonto |TOM |

## <a name="see-also"></a>Se også

[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Tilpasse [!INCLUDE[prod_short](includes/prod_short.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
