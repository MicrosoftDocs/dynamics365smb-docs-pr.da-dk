---
title: "Fremgangsmåde: Knytte tekst på tilbagevendende betalinger til konti for automatisk udligning | Microsoft Docs"
description: "Fremgangsmåde: Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7c6f79959027625a33961d42abe26514bc94e81e
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Fremgangsmåde: Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti
I vinduet **Tekst til kontotilknytning**, som du kan åbne fra vinduet **Betalingsudligningskladde**, kan du oprette tilknytninger mellem tekst på betalinger og specifikke debet-, kredit- og modkonti, så disse betalinger bliver bogført på de angivne konti, når du bogfører kladden til betalingsafstemning.

**Bemærk!** Emnet gælder også, når du bruger funktionen **Knyt tekst til konto** fra en indgående bilagsrecord som en hjælp ved konvertering af elektroniske dokumenter, der er modtaget fra eksterne tjenester, til dokumenter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Fremgangsmåde: Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).   

Der findes lignende funktioner til afstemning af overskydende beløb på betalingsudligningskladdelinjer på ad hoc-basis. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme betalinger, der ikke kan udlignes automatisk](receivables-how-reconcile-payments-cannot-apply-auto.md).

Betalinger, der er bogført baseret på tekst-til-kontotilknytning, udlignes ikke på åbne poster, men bliver blot bogført på de angivne konti i tillæg til at oprette finansposter på bankkonti. Derfor er tekst til kontotilknytning velegnet til tilbagevendende indbetalinger eller udgifter såsom hyppige køb af benzin eller bankgebyrer og -renter, der regelmæssigt forekommer på bankens kontoudtog, og ikke behøver et relateret forretningsdokument. Du kan finde flere oplysninger i afsnittet “Eksempel – Tekst-til kontotilknytning for udgift til benzin” i dette emne.

**Bemærk**: Betalinger på afstemningslinjerne i kladden er kun angivet til bogføring i overensstemmelse med tekst-til-kontotilknytning, hvis den automatiske udligningsfunktion kun kan give en udligningstillid af **Lav** eller **Mellem**. Hvis den automatiske udligningsfunktion indeholder matchtilliden Høj, bliver betalingen automatisk udlignet til en eller flere åbne poster, og betalingen bogføres ikke på de konti, der er angivet i vinduet **Tekst til kontotilknytning**. Med andre ord tilsidesætter udligningstilliden **Høj** en tekst-til-kontotilknytning.

På en betalingsudligningskladdelinje, hvor betalingen er angivet til bogføring i overensstemmelse med tekst-til-kontotilknytning, indeholder feltet **Matchtillid** **Høj – Tekst-til-kontotilknytning** og felterne **Kontotype** og **Kontonr.** indeholder de tilknyttede konti.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Sådan knytter du tekst på tilbagevendende betalinger til automatisk afstemning af konti
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Betalingsudligningskladder** og derefter vælge det relaterede link.
2. Åbn en kladde til betalingsafstemning. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. Vælg handlingen **Knyt tekst til konto**. Vinduet **Tekst til kontotilknytning** åbnes.
4. Brug feltet **Koblingstekst** til at angive tekst, der forekommer på betalinger, du vil bogføre på de angivne konti uden udligning til en åben post. Du kan angive op til 50 tegn.

    **Bemærk**! Hvis der ikke findes andre betalinger eller indgående bilag med den pågældende tilknytningstekst, kan teksten til kontotilknytning optræde, selv om kun en del af teksten på betalingen eller det indgående bilag findes som en tilknytningstekst.
5. I feltet **Kreditornr.** skal du angive den kreditor, som indgående bilag, der indeholder tilknytningsteksten, oprettes for, eller som betalinger bogføres til. Du kan finde flere oplysninger i [Fremgangsmåde: Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md).      
6. I feltet **Debetkontonr.** skal du angive den konto, som betalinger, der indeholder tilknytningsteksten, skal bogføres på, hvis de er indgående betalinger. For indgående betalinger er fortegnet for værdien i feltet **Kontoudtogsbeløb** positivt.
7. I feltet **Kreditkontonr.** skal du angive den konto, som betalinger, der indeholder tilknytningsteksten, skal bogføres på, hvis de er udgående betalinger. For udgående betalinger er fortegn for værdien i feltet **Kontoudtogsbeløb** er negativt.
8. Brug feltet **Modkontokildetype** til at angive, om betalingen skal bogføres på en finanskonto eller en debitor- eller kreditorkonto.
9. I feltet **Modkontokildenr.** skal du angive den konto, som betalingen vil blive bogført til, afhængig af valget i feltet **Modkontokildetype**.
10. Gentag trin 4 til 8 for al tekst på betalinger, du vil knytte til konti til direkte bogføring uden udligning.

Næste gang du importerer en bankkontofil eller vælge handlingen **Udlign automatisk** i vinduet **Betalingsudligningskladde**, vil kladdelinjerne til betalinger, der indeholder den angivne tilknytningstekst, indeholde tilknyttede konti i felterne **Kontotype** og feltet **Kontonr.** . Feltet **Matchtillid** indeholder **Høj - Tilknytning af tekst til konto**. Det er på betingelse af, at den automatiske udligningsfunktion kun kan give en udligningstillid af **Lav** eller **Mellem**.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Eksempel: Tekst-til kontotilknytning for udgift til benzin
Hvis du altid vil bogføre brændstofudgifter på Shell-benzinstationer til finanskontoen for benzin (konto 8510), skal du udfylde en linje i vinduet **Tekst til kontotilknytning** på følgende måde.

| Koblingstekst | Debetkonto nr. | Kreditkonto nr. | Modkonto kildetype | Modkonto kildenr. |
| --- | --- | --- | --- | --- |
| Shell |TOM |8510 |Finanskonto |TOM |

**Tip!** I emnet [Arbejde med [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md) kan du finde flere oplysninger om, hvordan du arbejder med feltet og kolonner. Se [Søg](ui-search.md) for at få flere oplysninger om søgning efter bestemte sider.

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Fremgangsmåde: Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Tilpasning af [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

