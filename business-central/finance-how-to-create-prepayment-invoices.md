---
title: Oprette forudbetalingsfakturaer
description: 'Få at vide, hvordan du håndterer situationer, hvor du eller din leverandør kræver forudbetaling. Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bhielse
ms.topic: how-to
ms.date: 02/02/2023
ms.custom: bap-template
ms.search.form: '42, 50, 9305, 9307'
---
# <a name="create-prepayment-invoices"></a>Oprette forudbetalingsfakturaer

Hvis du kræver, at kunderne betaler, før du leverer en ordre til dem, kan du bruge forudbetalingsfunktionen. Det samme gælder, hvis din leverandør kræver, at du betaler, før de leverer en ordre til dig.  

Når du har oprettet en salgs- eller købsordre, kan du starte forudbetalingsprocessen. Standardforudbetalingsprocent for en given vare på ordren eller for debitor eller kreditor, vil procentsatsen automatisk blive medtaget i den oprettede forudbetalingsfaktura. Du kan også angive en forudbetalingsprocent for hele dokumentet.

Når du har oprettet en salgs- eller købsordre, kan du oprette en forudbetalingsfaktura. Du kan enten bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov. Du kan f.eks. angive et samlet beløb for hele ordren.  

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

    > [!NOTE]
    > Når nogle linjer på en faktura kræver forudbetaling på 100 %, og der ikke er moms på forudbetalingskontoen, kan det afrundede beløb forårsage en fejl, når du opretter en forudbetalingsfaktura. Fejlen opstår, fordi forudbetalingsfaktura beløbet er højere end beløbene på bilagslinjerne. Du kan løse problemet ved at ændre beløbene på en eller alle linjer, der kræver forudbetaling på 100 %. Ændringen genberegner moms afrundingen og bruger den akkumulerede afrundingsdifference på den sidst ændrede linje.
    >
    > Der er to måder at løse problemet på:
    >
    > * Opret en ny momsproduktbogføringsgruppe og en Momsbogføringsopsætning med et separat moms-id, og brug den til de varer eller linjer, der kræver forudbetaling på 100 %. Afrunding foretages for hvert moms-id, så der foretages en særskilt afrunding for varer, der er knyttet til momsproduktbogføringsgruppen.
    > * Bruge en separat faktura til varer eller linjer, der ikke kræver, at der er 100 % forudbetalinger.

3. Udfyld salgslinjerne.  

    Hvis du har angivet en standardforudbetalingsprocent enten for debitoren eller i oversigtspanelet **Forudbetaling** i dette dokument, kopieres denne værdi til hver linje. Du kan ændre indholdet i feltet **Forudbetaling i %** på linjen.  

    > [!TIP]
    > Hvis du ikke kan se feltet **Forudbetaling i %**, kan du tilføje det via personlig tilpasning.  Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

4. Du kan se det samlede forudbetalingsbeløb ved at vælge handlingen **Statistik**.

    Hvis du vil regulere det samlede forudbetalingsbeløb for ordren, kan du ændre indholdet i feltet **Forudbetalingsbeløb** på siden **Salgsordrestatistik**.  

    Hvis feltet **Priser inkl. moms** er markeret, kan feltet **Forudbetalingsbeløb Inkl. moms** redigeres.  

    Hvis du ændrer indholdet i feltet **Forudbetalingsbeløb**, fordeles beløbet proportionalt mellem alle linjerne bortset fra linjer, hvor der står **0** i feltet **Forudbetaling i %**.  

5. For at udskrive en kontrolrapport, inden du bogfører forudbetalingsfakturaen, skal du vælge handlingen **Forudbetaling** og derefter vælge **Forudbetalingstestrapport**.  
6. For at bogføre forudbetalingsfakturaen skal du vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura**.  

    Hvis du både vil bogføre og udskrive forudbetalingsfakturaen, skal du vælge handlingen **Bogfør og udskriv forudbetalingsfaktura**.  

Du kan udstede andre forudbetalingsfakturaer til ordren. I så fald skal du udstede en anden faktura, øge forudbetalingsbeløbet på en eller flere linjer, justere dokumentdatoen, hvis det er nødvendigt, og bogføre forudbetalingsfakturaen. Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløb.  

> [!NOTE]  
> Hvis du befinder dig i USA, kan du ikke ændre forudbetalingsprocenten, når forudbetalingsfakturaen er blevet bogført. Dette forhindres i den amerikanske version af [!INCLUDE[prod_short](includes/prod_short.md)], fordi beregningen af moms ellers ville være forkert.  

 Når du er klar til at bogføre resten af fakturaen, skal du benytte samme fremgangsmåde som med alle andre fakturaer, hvorefter det forudbetalte beløb automatisk trækkes fra det forfaldne beløb.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Opdatere status for forudbetalte ordrer og fakturaer automatisk

Du kan gøre behandlingen hurtigere og oprette en faktura ved at indstille Opgavekøposter, der automatisk opdaterer status for de pågældende dokumenter. Når en forudbetalingsfaktura betales, kan posterne i opgavekøen automatisk ændre dokumentstatus fra **Afventende forudbetaling** til **Frigivet**. Når du opretter Opgavekøposter, er de kodeenheder, du skal bruge, **383 Opdateret Afventer forudbetaling af Salg** og **383 Opdateret Afventer forudbetaling af køb**. Det anbefales, at du planlægger posterne ofte, f. eks. hvert minut. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Gennemgang: Opsætning og fakturering af salgsforudbetalinger](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Tilpasse dit arbejdsområde](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
