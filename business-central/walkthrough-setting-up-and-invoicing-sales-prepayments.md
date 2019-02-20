---
title: "Gennemgang - Opsætning og fakturering af salgsforudbetalinger | Microsoft Docs"
description: "Forudbetalinger faktureres og bogføres på en forudbetalingsordre for salg eller køb inden den endelige bogføring. Du kan f.eks. kræve et depositum, før du fremstiller varer efter ordre, eller du kan kræve betaling, før du sender varerne til en kunde. Du bruger forudbetalingsfunktionen i Business Central til at fakturere og opkræve depositum, der kræves af debitorer eller at sende depositummerne til kreditorer. På den måde kan du sikre, at alle betalinger bogføres i forhold til en faktura."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 01/31/2019
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: a94c4f2f8d622a91b74ba0de6f0f18e7eb84a5ef
ms.openlocfilehash: 5fb8201f85fe94ac124e80014a4f3ff5073fbf65
ms.contentlocale: da-dk
ms.lasthandoff: 01/31/2019

---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Gennemgang: Opsætning og fakturering af salgsforudbetalinger

**Bemærk**: Denne gennemgang skal udføres på et demoregnskab med indstillingen **Fuld evaluering - Komplette eksempeldata**, der findes i sandkassemiljøet. Du kan finde flere oplysninger i [Oprette et sandkassemiljø](across-how-create-sandbox-environment.md).

Forudbetalinger faktureres og bogføres på en forudbetalingsordre for salg eller køb inden den endelige bogføring. Du kan f.eks. kræve et depositum, før du fremstiller varer efter ordre, eller du kan kræve betaling, før du sender varerne til en kunde. Du bruger forudbetalingsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at fakturere og opkræve depositum, der kræves af debitorer eller at sende depositummerne til kreditorer. På den måde kan du sikre, at alle betalinger bogføres i forhold til en faktura.  

 Der kan defineres forudbetalingskrav for en debitor eller kreditor for alle varer eller udvalgte varer. Når du har fuldført den påkrævede opsætning, kan du generere forudbetalingsfakturaer fra salgs- og købsordrer for det beregnede forudbetalingsbeløb. Du kan ændre standardbeløbene på fakturaen efter behov. Du kan f.eks. sende yderligere forudbetalingsfakturaer, hvis der føjes ekstra varer til ordren.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
 I denne gennemgang vil du komme gennem følgende scenarier:  

-   Opsætning af forudbetalinger  
-   Oprettelse af en ordre, der kræver forudbetaling  
-   Oprettelse af en forudbetalingsfaktura  
-   Ændring af forudbetalingskrav på en ordre  
-   Anvendelse af forudbetalinger på en ordre  
-   Fakturering af det endelige beløb på en ordre med forudbetaling  

### <a name="roles"></a>Roller  
 Denne gennemgang indeholder opgaver for følgende roller:  

-   Regnskabschef (Pia)  
-   Ordrebehandler (Susan)  
-   Administrator af tilgodehavender (Arne)  

## <a name="story"></a>Historie  
 Pia er regnskabschef. Hun træffer beslutninger om, hvilke kunder der skal betale et depositum, inden varerne produceres eller leveres. Pia indstiller [!INCLUDE[d365fin](includes/d365fin_md.md)] til at beregne forudbetalinger automatisk.  

 Susan er salgsordrebehandler. Når en kunde ringer for at afgive en ordre, indtaster hun ordren i systemet, mens kunden er i telefonen. På denne måde kan hun få bekræftet pris- og betalingsbetingelserne med kunden med det samme, og hun kan foretage ændringer i ordren, mens hun forhandler med kunden.  

 Arne arbejder i afdelingen for tilgodehavender, hvor han bogfører fakturaer og betalinger.  

 I dette scenarie angiver Pia forudbetalingskrav for kunden Ravel Møbler ud fra deres kredithistorie og instruerer Susan i, hvordan denne kundes ordrer skal håndteres.  

 Når kunden ringer, forhandler Susanne med vedkommende, indtil de når en aftale. Derefter kan hun vælge at beregne forudbetalingen på flere forskellige måder.  

 Når Susanne sender forudbetalingsfakturaen, bestiller kunden en ekstra vare. Susanne opdaterer rækkefølgen, og der opretter endnu en forudbetalingsfaktura.  

 Arne registrerer kundens betaling, påfører den på fakturaen og sender derefter den endelige faktura.  

## <a name="setting-up-prepayments"></a>Opsætte forudbetalinger  
 Pia opsætter systemet til at håndtere forudbetalinger for debitorer.  

-   Pia beslutter at beholde den samme nummerserie for forudbetalinger som den, der bruges til salgsfakturering.  
-   Pia indstiller systemet til at kontrollere, om der skal bruges forudbetalinger før den endelige fakturering af en ordre.  
-   Pia indstiller standardværdierne for en påkrævet forudbetalingsprocent for specifikke varer og debitorer.  

Følgende procedurer beskriver, hvordan Pias opgaver udføres:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Sådan opsættes nummerserierne for forudbetalinger  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af salg og tilgodehavender**, og vælg derefter det relaterede link.  
2.  På siden **Salgsopsætning** skal du udvide oversigtspanelet **Nummerering**.  
3.  Kontroller, at nummerserierne for de bogførte forudbetalingsfakturaer i feltet **Bogførte forudbetalingsfakturanr.** er de samme som dem, der er bogført for salgsfakturaerne (**Bogførte fakturanumre**), og at nummerserierne for bogførte forudbetalingskreditnotaer (**Bogførte forudbetalingskreditnotanr.**) er de samme som dem, der er bogført for kreditnotaer (**Bogf. kreditnotanumre**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Sådan blokeres forsendelser ved ubetalte forudbetalinger  
1.  Gå til siden **Salgsopsætning**, og marker afkrydsningsfeltet **Kontroller forudbetaling ved bogføring** i oversigtspanelet **Generelt**.

    Nu kan du ikke kan levere eller fakturere en ordre med et forudbetalingsbeløb, der ikke er betalt.  

Pia angiver, at debitor 20000 som standard skal faktureres med en forudbetaling på 30 % på alle ordrer. Hun skal derfor indtaste en standardprocent for forudbetaling på debitorkortet.  

Pia angiver, at alle debitorer skal faktureres med et depositum på 20 % for vare 1100. Debitor 20000 har en dårlig betalingshistorie. Hun kræver derfor en forudbetaling på 40 % fra debitor 20000 for vare 1100. Følgende fremgangsmåde viser, hvordan standardprocenten for forudbetaling angives.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Sådan angives standardprocenten for forudbetalinger for debitorer og varer  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Debitorer**, og vælg derefter det relaterede link.  
2.  Åbn kortvinduet for debitor 20000 (Ravel Møbler).
3.  Skriv **30** i feltet **Forudbetaling i %**.  
4.  Vælg knappen **OK** for at lukke debitorkortet.  
5.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Varer**, og vælg derefter det relaterede link.  
6.  Åbn kortet for debitor 1100.
7.  Vælg handlingen **Forudbetalingsprocenter**.  
8.  Udfyld de to linjer på siden **Forudbetalingsprocenter - salg** på følgende måde.  

    |**Salgstype**|**Salgskode**|**Varenr.**|**Forudbetaling i %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Debitor**|**20000**|**1100**|**40**|  
    |**Alle debitorer**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Afhængigt af dit land eller område, skal du også angive en skattegruppekode i oversigtspanelet **Fakturering** for varerne 1000 og 1100.  

9. Luk alle sider.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Angive en konto for salgsforudbetalinger i den generelle bogføringsopsætning  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
2.  Markér linjen, hvor feltet **Virksomhedsbogføringsgruppe** er indstillet til **EKSPORTERE**, og feltet **Produktbogføringsgruppe** er indstillet til **DETAIL**, og vælg derefter handlingen **Rediger**.  
3.  Angiv den relevante konto i feltet **Forudbetalingskonto** for salg på siden **Bogføringsopsætningskort**.  
4.  Vælg knappen **OK**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Oprette en ordre, der kræver en forudbetaling  
 I følgende scenarie opretter ordrebehandleren Susan en ordre, mens hun taler med en kunde. De varer, hvor debitorordrer kræver en forudbetaling, og hvor debitor tidligere har foretaget nogle forsinkede betalinger. Susanne er derfor blevet instrueret i at kræve et fast beløb på 2.000 som en forudbetaling på ordren.  

Debitor ønsker at betale 35 %, hvilket Susanne accepterer. Hun ændrer derfor ordren.  

Susan opretter forudbetalingsfakturaen og sender den til kunden.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Sådan oprettes en salgsordre med en forudbetaling  
1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  I feltet **Kundenr** skal du vælge **20000**.  
5.  Accepter den viste advarslen om et forfaldent beløb.  
6.  Udfyld de to salgslinjer med følgende oplysninger.  

    |**Type**|**Nummer**|**Antal**|  
    |--------------|-------------|------------------|  
    |**Vare**|**1000**|**1**|  
    |**Vare**|**1100**|**1**|

    Forudbetalingsfelterne på salgslinjen er som standard skjult, så de skal vises.  

7. Kontroller, at feltet **Forudbetaling i %** på linjen med vare **1000** indeholder **30**. Standardværdien er taget fra salgshovedet, der blev udfyldt med oplysninger fra debitorkortet.  

    Feltet **Forudbetaling i %** på linjen med vare **1100** indeholder **40**. Det er denne procent, du har angivet på siden **Forudbetalingsprocenter - salg** for vare **1100** og debitor **20000**.  

    Du kan finde flere oplysninger i [Oprette forudbetalinger](finance-set-up-prepayments.md).  
8. Vælg handlingen **Statistik**.  
9. I oversigtspanelet **Forudbetaling** indeholder feltet **Linjebeløb for forudbetaling ekskl. moms** **1.560**. Hvis du opretter en forudbetalingsfaktura for ordren nu, er det dette beløb, der vises på fakturaen.  

    I dette scenarie har Susan fået at vide, at hun skal foreslå en samlet forudbetaling på 2000 for ordren.  

    > [!IMPORTANT]  
    >  Afhængigt af dit land/område gælder følgende trin muligvis ikke.  
10. Skift beløb i feltet **Linjebeløb for forudbetaling ekskl. moms** til **2000**, og luk derefter siden.  
11. Kontroller feltet **Forudbetaling i %** på salgslinjerne, og du vil kunne se, at det er genberegnet til **40,81625**.  

    Genberegningen inkluderer alle linjer med en forudbetalingsprocent, der er større end 0.  

    Kunden spørger nu, om forudbetalingsprocenten kan blive angivet til 35 %. Susannes tilsynsførende godkender ændringen.  

12. Gå til siden **Salgsordre**, og angiv **35** i feltet **Forudbetaling**.  
13. Vælg knappen **Ja** i den viste advarsel. Der anvendes en sats på 35 % som betalingsprocent for hele ordren.  
14. Kontrollér, at linjerne er opdateret tilsvarende.  

## <a name="creating-a-prepayment-invoice"></a>Oprette en forudbetalingsfaktura  
Når den korrekte forudbetalingsværdi er angivet på ordren, opretter Susan forudbetalingsfakturaen og sender den til kunden.  

#### <a name="to-create-a-prepayment-invoice"></a>Sådan oprettes en forudbetalingsfaktura  

1.  På siden **Salgsordre** skal du vælge handlingen **Bogfør forudbetalingsfaktura**.  

> [!NOTE]  
>  Susan vil her vælge **Bogfør og udskriv forudbetalingsfaktura** og sende fakturaen til kunden.  

## <a name="creating-an-additional-prepayment-invoice"></a>Oprette en forudbetalingsfaktura til  
Den næste dag ringer kunden til Susan med ændringer til ordren. Kunden vil gerne have to stk. af vare 1100. Susan åbner ordren igen og opdaterer den, hvorefter hun opretter en forudbetalingsfaktura til på ordren og sender den til kunden.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Sådan oprettes der en forudbetalingsfaktura til  

1.  På siden **Salgsordre** skal du vælge handlingen **Åbn igen**.  
2.  Gå til linjen for vare **1100** i feltet **Antal**, og indtast **2**.  

    Rul for at få vist forudbetalingsfelterne. Feltet **Forudbetaling - Linjebeløb ekskl. moms** indeholder nu **630**, og feltet **Forudbetalt beløb faktureret ekskl. moms** indeholder **315**. Dette viser, at der er et yderligere forudbetalingsbeløb, der endnu ikke er faktureret.  
3.  For at bogføre det ekstra forudbetalingsbeløb skal du på **Handlinger**, i gruppen **Bogføring** vælge **Forudbetaling** og derefter vælge **Bogfør forudbetalingsfaktura**.  

## <a name="applying-the-prepayments"></a>Påføre forudbetalinger  
Debitor betaler forudbetalingsbeløbet, og Arne, der arbejder i regnskabsafdelingen, registrerer betalingen og påføre den på forudbetalingsfakturaerne.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Sådan påføres en betaling på forudbetalingsfakturaer  

1.  Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Indbetalingskladder**, og vælg derefter det relaterede link.  
2.  Udfyld kladdelinjen med følgende oplysninger.  

    |Feltnavn|Indsæt|  
    |----------------|-----------|  
    |**Bilagstype**|**Betaling**|  
    |**Kontotype**|**Debitor**|  
    |**Kontonr.**|**20000**|  
3. Vælg handlingen **Udlign**.  
4.  Markér den første forudbetalingsfaktura, og vælg derefter handlingen **Angiv udlignings-id** på siden **Udlign debitorposter**.  
5.  Gentag det forrige trin for den anden forudbetaling.  
6.  Vælg knappen **OK**.  

    Beløbsfeltet er nu udfyldt med beløbet af de to forudbetalingsfakturaer.  

7.  Bogfør journalen.  

## <a name="invoicing-the-remaining-amount"></a>Fakturere restbeløbet  
Arne har nu fået oplyst, at varerne i ordren er blevet afsendt, og at ordren er klar til fakturering. Arne opretter fakturaen til ordren.  

#### <a name="to-invoice-the-remaining-amount"></a>Sådan faktureres restbeløbet  
1. Åbn salgsordren.  
2. Vælg handlingen **Lever og fakturer**, og derefter vælge knappen **OK**.  

> [!NOTE]  
>  Normalt ville forsendelsesafdelingen allerede have bogført forsendelsen.  

Arne kan få vist oversigten for at kontrollere, at salgsfakturaen blev oprettet, som tiltænkt.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  

## <a name="next-steps"></a>Efterfølgende trin  
Denne gennemgang har ført dig gennem trinnene i, hvordan du indstiller [!INCLUDE[d365fin](includes/d365fin_md.md)] til at håndtere forudbetalinger. Du har oprettet standardprocenter for forudbetaling for debitorer og varer, og du har også brugt forskellige andre metoder til beregning af forudbetalinger på en ordre. Du har prøvet at tildele forudbetalingsbeløb til ordren, og du har fået programmet til at beregne forudbetalingsbeløbet beregnet som en procent af hele ordren.  

Du har også bogført en forudbetalingsfaktura, oprettet endnu en forudbetalingsfaktura, når ordren er ændret, og bogført den endelige faktura for restbeløbet.  

Forudbetalingsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)] gør det nemmere at oprette og gennemtvinge regler for forudbetaling for debitorer og varer, og den giver dig mulighed for at bogføre hver betaling for en faktura.  

## <a name="see-also"></a>Se også  
[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)

