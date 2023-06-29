---
title: Oprette og fakturere salgsforudbetalinger
description: Forudbetalinger faktureres og bogføres på en forudbetalingsordre for salg eller køb inden den endelige bogføring.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a><a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Gennemgang: Opsætning og fakturering af salgsforudbetalinger

Denne gennemgang fører dig gennem konfigureringen og brugen af forudbetalinger i [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

Du kan f.eks. sende yderligere forudbetalingsfakturaer, hvis der føjes ekstra varer til ordren.  

## <a name="about-this-walkthrough"></a><a name="about-this-walkthrough"></a>Om denne gennemgang

I denne gennemgang vil du komme gennem følgende scenarier:  

- Opsætning af forudbetalinger  
- Oprettelse af en ordre, der kræver forudbetaling  
- Oprettelse af en forudbetalingsfaktura  
- Ændring af forudbetalingskrav på en ordre  
- Anvendelse af forudbetalinger på en ordre  
- Fakturering af det endelige beløb på en ordre med forudbetaling  

### <a name="roles"></a><a name="roles"></a>Roller

Denne gennemgang indeholder opgaver for følgende roller:  

- Regnskabschef (Pia)  
- Ordrebehandler (Susan)  
- Administrator af tilgodehavender (Arne)  

## <a name="story"></a><a name="story"></a>Historie

 Phyllis er regnskabschef og træffer beslutninger om, hvilke kunder der skal betale et depositum, inden varerne produceres eller leveres. Pia indstiller [!INCLUDE[prod_short](includes/prod_short.md)] til at beregne forudbetalinger automatisk.  

 Susan er salgsordrebehandler. Når en kunde ringer for at afgive en ordre, indtaster Susan ordren i systemet, mens kunden er i telefonen. På denne måde kan Susan få bekræftet pris- og betalingsbetingelserne med kunden med det samme, og hun kan foretage ændringer i ordren, mens hun forhandler med kunden.  

 Arnie arbejder i afdelingen for tilgodehavender, hvor han bogfører fakturaer og betalinger.  

 I dette scenarie angiver Pia forudbetalingskrav for kunden Ravel Møbler ud fra deres kredithistorie. Pia giver Susan instruktioner om, hvordan deres ordrer håndteres.  

 Når kunden ringer, forhandler Susan med kunden, indtil de når frem til en aftale – systemet giver hende mulighed for at beregne forudbetalingen på flere forskellige måder.  

 Når Susanne sender forudbetalingsfakturaen, bestiller kunden en ekstra vare. Susanne opdaterer rækkefølgen, og der opretter endnu en forudbetalingsfaktura.  

 Arne registrerer kundens betaling, påfører den på fakturaen og sender derefter den endelige faktura.  

## <a name="set-up-prepayments"></a><a name="set-up-prepayments"></a>Oprette forudbetalinger

Pia opsætter systemet til at håndtere forudbetalinger for debitorer.  

- Pia beslutter at beholde den samme nummerserie for forudbetalinger som den, der bruges til salgsfakturering.  
- Pia indstiller programmet til at kontrollere, om der skal bruges forudbetalinger før den endelige fakturering af en ordre.  
- Pia indstiller standardværdierne for en påkrævet forudbetalingsprocent for specifikke varer og debitorer.  

Følgende procedurer beskriver, hvordan Pias opgaver udføres:  

### <a name="to-set-up-number-series-for-prepayments"></a><a name="to-set-up-number-series-for-prepayments"></a>Sådan opsættes nummerserierne for forudbetalinger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Salgsopsætning**, og vælg derefter det relaterede link.  
2. På siden **Salgsopsætning** skal du udvide oversigtspanelet **Nummerering**.  
3. Kontroller, at nummerserierne for de bogførte forudbetalingsfakturaer i feltet **Bogførte forudbetalingsfakturanr.** er de samme som dem, der er bogført for salgsfakturaerne (**Bogførte fakturanumre**), og at nummerserierne for bogførte forudbetalingskreditnotaer (**Bogførte forudbetalingskreditnotanr.**) er de samme som dem, der er bogført for kreditnotaer (**Bogf. kreditnotanumre**).  

### <a name="to-block-shipments-for-unpaid-prepayment"></a><a name="to-block-shipments-for-unpaid-prepayment"></a>Sådan blokeres forsendelser ved ubetalte forudbetalinger

1. Gå til siden **Salgsopsætning**, og marker afkrydsningsfeltet **Kontroller forudbetaling ved bogføring** i oversigtspanelet **Generelt**.

Nu kan du ikke kan levere eller fakturere en ordre med et forudbetalingsbeløb, der ikke er betalt.  

Pia angiver, at debitor 20000 som standard skal faktureres med en forudbetaling på 30 % på alle ordrer. Phyllis skal derfor indtaste en standardprocent for forudbetaling på debitorkortet.  

Pia angiver, at alle debitorer skal faktureres med et depositum på 20 % for vare 1896-S. Debitor 20000 har en dårlig betalingshistorie, så Phyllis angiver en forudbetaling på 40 % for debitor 20000 på vare 1896-S. Følgende fremgangsmåde viser, hvordan standardprocenten for forudbetaling angives.  

### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a><a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Sådan angives standardprocenten for forudbetalinger for debitorer og varer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2. Åbn kortvinduet for debitor 20000 (Trey Research).
3. I oversigtspanelet **Betalinger** skal du angive **30** i feltet **Forudbetaling i %**.  
4. Vælg den **Relaterede** handling, vælg menupunktet **Salg**, og vælg derefter menupunktet **Forudbetalingsprocenter**.  
5. Udfyld de to linjer på siden **Forudbetalingsprocenter - salg** på følgende måde.  

    |**Salgstype**|**Salgskode**|**Varenr.**|**Forudbetaling i %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Debitor**|**20000**|**1896-S**|**40**|
    |**Debitor**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Afhængigt af dit land eller område, skal du også angive en skattegruppekode i oversigtspanelet **Omkostninger og bogføring** for vare 1896-S. Når du bruger demoregnskabet, er feltet allerede angivet.

6. Luk alle sider.  

### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a><a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Angive en konto for salgsforudbetalinger i den generelle bogføringsopsætning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
2. Markér linjen, hvor feltet **Virksomhedsbogføringsgruppe** er indstillet til **DOMESTIC**, og feltet **Produktbogføringsgruppe** er indstillet til **DETAIL**.  
3. Angiv den relevante konto i feltet **Forudbetalingskonto for salg**. Markeringen gemmes automatisk.  

> [!TIP]
> Hvis du ikke kan se feltet på siden **Bogføringsopsætning**, skal du bruge det vandrette rullepanel nederst på siden til at rulle til højre.  

## <a name="create-an-order-that-requires-a-prepayment"></a><a name="create-an-order-that-requires-a-prepayment"></a>Oprette en ordre, der kræver en forudbetaling

 I følgende scenarie opretter ordrebehandleren Susan en ordre, mens hun taler med en kunde. De varer, som kunden bestiller, kræver en forudbetaling. Desuden har debitoren allerede foretaget nogle forsinkede betalinger. Susan er derfor blevet instrueret i at kræve et fast beløb på **800** som en forudbetaling på ordren.  

Kunden beder om at betale 35 %, hvilket Susan går med til, og hun ændrer derfor ordren i overensstemmelse med dette.  

Susan opretter forudbetalingsfakturaen og sender den til kunden.  

### <a name="to-create-a-sales-order-with-a-prepayment"></a><a name="to-create-a-sales-order-with-a-prepayment"></a>Sådan oprettes en salgsordre med en forudbetaling

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Vælg **Trey Research** i feltet **Kundenavn**.  
4. Luk den viste advarslen om et forfaldent beløb.  
5. Udfyld de to salgslinjer med følgende oplysninger.  

    |**Type**|**Nummer**|**Antal**|  
    |--------------|-------------|------------------|  
    |**Vare**|**1896-S**|**1**|  
    |**Vare**|**1900-S**|**1**|

    Forudbetalingsfelterne på salgslinjen er som standard skjult, så de skal vises. For at få vist de felter, du skal tilpasse siden. Du kan finde flere oplysninger i [Start af tilpasning af en side gennem det personlige banner](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

6. Kontroller, at feltet **Forudbetaling i %** på linjen med vare **1900-S** indeholder **30**. Standardværdien er taget fra salgshovedet, der blev udfyldt med oplysninger fra debitorkortet.  

    Feltet **Forudbetaling i %** på linjen med vare **1896-S** indeholder **40**. 40 er den procentsats, du har angivet på siden **Forudbetalingsprocenter - salg** for vare **1896-S** og debitor **20000**.  

    Du kan finde flere oplysninger i [Oprette forudbetalinger](finance-set-up-prepayments.md).  
7. Klik på **Statistik** i **ordre handlingen**.  
8. I oversigtspanelet **Forudbetaling** indeholder feltet **Forudbetalingsbeløb Ekskl. moms** tallet **458,16**. Hvis du opretter en forudbetalingsfaktura for ordren nu, er det 458,16, der vises på fakturaen.  

    I dette scenarie har Susan fået at vide, at hun skal foreslå en samlet forudbetaling på **800** for ordren.  

    > [!IMPORTANT]  
    >  Afhængigt af dit land/område gælder følgende trin muligvis ikke.  
9. Ret beløb i feltet **Beløb for forudbetaling ekskl. moms** til **800**, og luk derefter siden.  
10. Kontroller feltet **Forudbetaling i %** på salgslinjerne, og du vil kunne se, at det er genberegnet til **67,02438** og **67,02282**.  

     Genberegningen inkluderer alle linjer med en forudbetalingsprocent, der er større end 0.  

     Kunden spørger nu, om forudbetalingsprocenten kan blive angivet til 35 %. Susannes tilsynsførende godkender ændringen.
11. Gå til siden **Salgsordre**, og angiv i oversigtspanelet **Forudbetaling** **35** i feltet **Forudbetaling i %**.  
12. Vælg knappen **Ja** i den viste advarsel. Der anvendes en sats på 35 % som betalingsprocent for hele ordren.  
13. Kontrollér, at linjerne er opdateret tilsvarende.  

## <a name="create-a-prepayment-invoice"></a><a name="create-a-prepayment-invoice"></a>Oprette en forudbetalingsfaktura

Når den korrekte forudbetalingsværdi er angivet på ordren, opretter Susan forudbetalingsfakturaen og sender den til kunden.  

### <a name="to-create-a-prepayment-invoice"></a><a name="to-create-a-prepayment-invoice"></a>Sådan oprettes en forudbetalingsfaktura

1. Vælg **Forudbetaling** og derefter **Bogfør og udskriv forudbetalingsfaktura** i gruppen **Bogføring** under fanen **Handlinger** i **salgsordren**.
2. Vælg **Ja** for at bogføre fakturaen.  

> [!NOTE]  
> Susan sender nu fakturaen til kunden.  

## <a name="create-an-additional-prepayment-invoice"></a><a name="create-an-additional-prepayment-invoice"></a>Oprette en yderligere forudbetalingsfaktura

Den næste dag ringer kunden til Susan med ændringer til ordren. Kunden vil gerne have to stk. af vare 1896-S. Susan åbner ordren igen og opdaterer den, hvorefter hun opretter en forudbetalingsfaktura til på ordren og sender den til kunden.  

### <a name="to-create-an-additional-prepayment-invoice"></a><a name="to-create-an-additional-prepayment-invoice"></a>Sådan oprettes der en forudbetalingsfaktura til

1. På siden **Salgsordre** skal du vælge handlingen **Frigiv** og **Åbn igen**.  
2. Gå til linjen for vare **1896-S** i feltet **Antal**, og indtast **2**.  

    Klik på **Statistik** i handlingen **Ordre**. Feltet **Forudbetalingsbeløb Ekskl. moms** indeholder nu **768,04**, og feltet **Forudbetalt beløb faktureret ekskl. moms** indeholder **417,76**. Dette viser, at der er et yderligere forudbetalingsbeløb, der endnu ikke er faktureret.  
3. For at bogføre det ekstra forudbetalingsbeløb skal du på vælge **Handlinger**, i gruppen **Bogfør og udskriv forudbetalingsfaktura** vælge **Forudbetaling** og derefter vælge **Bogfør**
4. Vælg **Ja** for at bogføre fakturaen.  

## <a name="apply-the-prepayments"></a><a name="apply-the-prepayments"></a>Påføre forudbetalinger

Kunden betaler forudbetalingsbeløbet. Arnie skal fra regnskabsafdelingen registrere betalingen og udligne den med forudbetalings fakturaerne.  

### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a><a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Sådan påføres en betaling på forudbetalingsfakturaer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indbetalingskladder**, og vælg derefter det relaterede link.  
2. Udfyld kladdelinjen med følgende oplysninger.  

    |Feltnavn|Indsæt|  
    |----------------|-----------|  
    |**Bilagstype**|**Betaling**|  
    |**Kontotype**|**Debitor**|  
    |**Kontonr.**|**20000**|  
3. Vælg handlingen **Proces** og derefter **Angiv poster**.  
4. Vælg den første forudbetalingsfaktura, og vælg derefter handlingen **Behandle** og derefter **Sæt udlignings-id** på siden **Udlign debitorposter**.  
5. Gentag det forrige trin for den anden forudbetaling.  
6. Vælg knappen **OK**.  

    Felterne **Beløb** er nu udfyldt med summen af de to forudbetalingsfakturaer.  

7. Du kan bogføre kladden ved at vælge handlingen **Bogfør/Udskriv** og derefter klikke på **Bogfør**.
8. Vælg knappen **Ja**.

## <a name="invoice-the-remaining-amount"></a><a name="invoice-the-remaining-amount"></a>Fakturere restbeløbet

Arne har nu fået oplyst, at varerne i ordren er blevet afsendt, og at ordren er klar til fakturering. Arne opretter fakturaen til ordren.  

### <a name="to-invoice-the-remaining-amount"></a><a name="to-invoice-the-remaining-amount"></a>Sådan faktureres restbeløbet

1. Åbn salgsordren.
2. Vælg **bogføring**-handling og derefter **Bogfør**.
3. Vælg **Lever og fakturer**, og vælg derefter knappen **OK**.
4. Hvis du vil genoprette fakturaen, skal du vælge knappen **Ja**.

    > [!NOTE]  
    > Normalt ville forsendelsesafdelingen allerede have bogført forsendelsen.  

    Arne kan få vist oversigten for at kontrollere, at salgsfakturaen blev oprettet, som tiltænkt.

5. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bogførte salgsfakturaer**, og vælg derefter det relaterede link.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a><a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>Opdatere status for forudbetalte ordrer og fakturaer automatisk

Du kan gøre behandlingen hurtigere og oprette en faktura ved at indstille Opgavekøposter, der automatisk opdaterer status for de pågældende dokumenter. Når en forudbetalingsfaktura betales, kan posterne i opgavekøen automatisk ændre dokumentstatus fra **Afventende forudbetaling** til **Frigivet**. Når du opretter Opgavekøposter, er de kodeenheder, du skal bruge, **383 Opdateret Afventer forudbetaling af Salg** og **383 Opdateret Afventer forudbetaling af køb**. Det anbefales, at du planlægger posterne ofte, f. eks. hvert minut. Du kan finde flere oplysninger i [Bruge opgavekøer til at planlægge opgaver](admin-job-queues-schedule-tasks.md).

## <a name="next-steps"></a><a name="next-steps"></a>Efterfølgende trin

Denne gennemgang har ført dig gennem trinnene i, hvordan du indstiller [!INCLUDE[prod_short](includes/prod_short.md)] til at håndtere forudbetalinger. 

- Konfigurere standardprocenten for forudbetalinger for debitorer og varer.
- Bruge forskellige metoder til at beregne forudbetalinger for en ordre.  
- Beregne forudbetalingsbeløbet som en procentdel af totalen på ordren.
- Tildele et samlet forudbetalingsbeløb til ordren.  

Du har også bogført en forudbetalingsfaktura, oprettet endnu en forudbetalingsfaktura, når ordren er ændret, og bogført den endelige faktura for restbeløbet.  

Forudbetalings funktionerne gør det nemmere at oprette og gennemtvinge regler for forudbetaling for debitorer og varer. De giver dig også mulighed for at bogføre hver betaling mod en faktura.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Se også

[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
