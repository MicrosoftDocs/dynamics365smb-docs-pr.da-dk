---
title: Oprette forudbetalingsfakturaer
description: Få at vide, hvordan du håndterer situationer, hvor du eller din leverandør kræver forudbetaling. Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: db06612ed644f8db52d8c9e8247b6cc7fe9df339
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519169"
---
# <a name="create-prepayment-invoices"></a>Oprette forudbetalingsfakturaer

Hvis du kræver, at kunderne skal indsende en betaling, før du leverer en ordre til dem, kan du bruge forudbetalingsfunktionen. Det samme gælder, hvis din leverandør kræver, at du indsender betalingen, før de leverer en ordre til dig.  

Når du har oprettet en salgs- eller købsordre, kan du starte forudbetalingsprocessen. Hvis du har en standardforudbetalingsprocent for en given vare på ordren eller for debitor eller kreditor, vil den automatisk blive medtaget i den oprettede forudbetalingsfaktura. Du kan også angive en forudbetalingsprocent for hele dokumentet.

Når du har oprettet en salgs- eller købsordre, kan du oprette en forudbetalingsfaktura. Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov. Du kan f.eks. angive et samlet beløb til hele ordren.  

Følgende procedure beskriver, hvordan du fakturerer en forudbetaling for en salgsordre. Fremgangsmåden er den samme for købsordrer.  

## <a name="to-create-a-prepayment-invoice"></a>Sådan oprettes en forudbetalingsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Opret en ny salgsordre for den ønskede kunde. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  

    I oversigtspanelet **Forudbetaling** angiver feltet **Forudbetaling i %** den procentsats, der skal bruges til at beregne forudbetalingsbeløbet. Feltet udfyldes automatisk, hvis der er angivet en standardforudbetalingsprocent på debitorkortet. Du kan ændre procentsatsen. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Vælg feltet **Komprimer forudbetaling**, hvis du vil oprette linjer på forudbetalingsfakturaen, der kombinerer linjer fra salgsordren, hvis:  

    - De har samme finanskonto til forudbetalinger, som angivet i bogføringsopsætning.  
    - De har samme dimensioner.  

    Hvis du vil angive en forudbetalingsfaktura med én linje for hver salgsordre, der har en forudbetalingsprocent, skal du ikke vælge feltet **Komprimer forudbetaling**.  

    Forfaldsdatoen for forudbetalingen beregnes automatisk på grundlag af værdien af **Forudb. - kode for betal.betingelser**.

3. Udfyld salgslinjerne.  

    Hvis du har angivet en standardforudbetalingsprocent enten for debitoren eller i oversigtspanelet **Forudbetaling** i dette dokument, kopieres denne værdi til hver linje. Du kan ændre indholdet i feltet **Forudbetaling i %** på linjen.  

    > [!TIP]
    > Hvis du ikke kan se feltet **Forudbetaling i %**, kan du tilføje det via personlig tilpasning.  Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

4. Du kan se det samlede forudbetalingsbeløb ved at vælge handlingen **Statistik**.

    Hvis du vil regulere det samlede forudbetalingsbeløb for ordren, kan du ændre indholdet i feltet **Forudbetalingsbeløb** på siden **Salgsordrestatistik**.  

    Hvis feltet **Priser inkl. moms** er markeret, kan feltet **Forudbetalingsbeløb Inkl. moms** redigeres.  

    Hvis du ændrer indholdet i feltet **Forudbetalingsbeløb**, fordeles beløbet proportionalt mellem alle linjerne bortset fra dem, hvor der står **0** i feltet **Forudbetaling i %**.  

5. For at udskrive en kontrolrapport, inden du bogfører forudbetalingsfakturaen, skal du vælge handlingen **Forudbetaling** og derefter vælge **Forudbetalingstestrapport**.  
6. For at bogføre forudbetalingsfakturaen skal du vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura**.  

    Hvis du både vil bogføre og udskrive forudbetalingsfakturaen, skal du vælge handlingen **Bogfør og udskriv forudbetalingsfaktura**.  

Du kan udstede flere forudbetalingsfakturaer til ordren. I så fald skal du øge forudbetalingsbeløbet på en eller flere linjer, justere dokumentdatoen, hvis det er nødvendigt, og bogføre forudbetalingsfakturaen. Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløb.  

> [!NOTE]  
> Hvis du befinder dig i USA, kan du ikke ændre forudbetalingsprocenten, når forudbetalingsfakturaen er blevet bogført. Dette forhindres i den amerikanske version af [!INCLUDE[prod_short](includes/prod_short.md)], fordi beregningen af moms ellers ville være forkert.  

 Når du er klar til at bogføre resten af fakturaen, skal du benytte samme fremgangsmåde som med alle andre fakturaer, hvorefter det forudbetalte beløb automatisk trækkes fra det forfaldne beløb.  

## <a name="see-also"></a>Se også

[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Gennemgang: Opsætning og fakturering af salgsforudbetalinger](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
[Tilpas dit arbejdsområde](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]