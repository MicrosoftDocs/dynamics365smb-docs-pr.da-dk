---
title: Fakturasalg
description: 'Beskriver, hvordan du opretter en salgsnota, en salgsfaktura eller salgsordre for at registrere en aftale med en kunde om at sælge produkter i henhold til bestemte betingelser.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Fakturasalg

Du kan normalt oprette en salgsordre eller salgsfaktura for at registrere din aftale med en kunde om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.  

Du skal imidlertid bruge en salgsordre i stedet for en salgsfaktura, hvis du:  

* Skal levere en del af et ordreantal, f.eks. fordi hele antallet ikke er på lager.  
* Levere produkter, efter at du har bogført de tilsvarende salgsfakturaer.
* Sælge varer, som leverandøren leverer direkte til kunden. Det kaldes direkte levering. Flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md).  

I alle andre tilfælde fungerer salgsordrer og salgsfakturaer på samme måde. Flere oplysninger om brug af salgsordrer i [Sælge produkter](sales-how-sell-products.md).

Du kan forhandle med debitoren ved først at oprette et salgstilbud, som du kan konvertere til en salgsfaktura, når I har aftalt salget. Flere oplysninger i [Oprette salgstilbud](sales-how-make-offers.md).

## Oprette salgsfakturaer

Hvis kunden beslutter at købe, bogfører du salgsfakturaen for at oprette det relaterede antal og værdiposterne. Når du bogfører salgsfakturaen, kan du også sende den som en vedhæftet PDF-fil i en mail. Du kan få brødteksten i mailen udfyldt med en oversigt over faktura- og betalingsoplysninger, f.eks. et link til PayPal. Flere oplysninger i [Afsende dokumenter med e-mail](ui-how-send-documents-email.md#to-send-documents-by-email). Når kunden derefter betaler fakturaen, kan du registrere betalingen på forskellige måder, afhængigt af størrelsen og de foretrukne arbejdsgange i organisationen. Flere oplysninger i afsnittet [Registrering af betalinger](#register-payments).  

Varekortet kan være af typen **Lager**, **Service** og **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke opbevares på lageret. Flere oplysninger i [Registrere nye emner](inventory-how-register-new-items.md). Salgsfakturaprocessen er den samme for alle tre varetyper.

Du kan udfylde debitorfelter i salgsfakturaen på en af to måder, afhængigt af om debitoren er registreret. Se trin 2 i følgende procedure.

### Sådan oprettes en salgsfaktura

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. I feltet **Debitornavn** skal du indtaste navnet på en eksisterende debitor. Hvis kunden imidlertid er ny og derfor ikke registreret, skal du benytte følgende fremgangsmåde til at udfylde standard debitoroplysninger på siden **Salgsfaktura**:

    1. I feltet **Kundenavn** skal du indtaste navnet på den nye kunde.
    2. I dialogboksen, hvor du registrerer den nye debitor, skal du trykke på knappen **OK**.
    3. På siden **Vælg en skabelon til en ny debitor** skal du vælge en skabelon, som det nye debitorkort skal baseres på, og derefter vælge knappen **OK**.
    4. Et nyt debitorkort viser oplysninger om den valgte debitorskabelon. Udfyld de resterende felter. Flere oplysninger i [Registrere nye kunder](sales-how-register-new-customers.md).  
    5. Når du er færdig med debitorkortet, skal du vælge **Luk** for at vende tilbage til siden **Salgsfaktura**.

   En række af felterne i salgsfakturaen er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.  
3. Udfylde de resterende felter efter behov på siden **Salgsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du tillader, at kunden betaler med det samme, f.eks. kontant eller via PayPal, skal du udfylde feltet **Betalingsmetodekode**. Betalingen registreres derefter, når du bogfører salgsfakturaen. Hvis du vælger *Kontant*, registreres betalingen i en bestemt modkonto.

    Du er nu klar til at udfylde oversigtspanelet **Linjer** for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren, som du vil registrere i en finanskonto.

4. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren på salgslinjen.
   > [!TIP]
   > Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du reflekterer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.
5. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** tomt felt i følgende tilfælde:

    * Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    * Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Flere oplysninger i [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

6. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen bør registrere for debitoren.  

    > [!NOTE]  
    > Hvis varen er af typen **Service**, eller hvis feltet **Type** indeholder **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen. Flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md)

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
7. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Gentag trin 4 til 7 for hvert produkt eller gebyr, du vil fakturere debitoren for.

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

    > [!NOTE]
    > I meget sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.<br /><br />Brug faktaboksen **Debitorstatistik** til at kontrollere de beløb, du bogfører. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.

9. I feltet **Fakturarabat ekskl. moms** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis rabatkriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).

10. Når salgsfakturalinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.  

Dialogboksen **Bekræftelse af bogfør og send** viser debitorens foretrukne metode til modtagelse af dokumenter. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

De relaterede vare- og debitorposter oprettes nu i systemet, og salgsfakturaen udlæses som et PDF-dokument. Salgsfakturaen fjernes fra listen over salgsfakturaer og erstattes med et nyt bilag i oversigten over bogførte salgsfakturaer.  

### Beregne fakturarabatter på salg

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## Bogførte fakturaer

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

Du kan nemt rette eller annullere en bogført salgsfaktura, før den sidste betaling. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Flere oplysninger i [Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bogførte faktura betales, skal du oprette en salgskreditnota for at tilbageføre salget. Flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).  

[Åbne listen **Bogførte salgsfakturaer**](https://businesscentral.dynamics.com/?page=143) i [!INCLUDE [prod_short](includes/prod_short.md)].

## Registrer betalinger

Afhængigt af dine forretningsmæssige behov kan du modtage betaling og registrere den på forskellige måder: manuelt, automatisk og ved hjælp af betalingstjenester.  

Du kan behandle betalingerne direkte fra debitorkortet. Brug handlingen **Registrer debitorbetalinger** for at hente en oversigt over de ubetalte fakturaer for den pågældende kunde. Marker fakturaen som betalt delvist eller helt. Denne betalingsudligning behandler dine debitorbetalinger ved at afstemme beløb, der er modtaget på bankkontoen, med de relaterede ubetalte salgsfakturaer og derefter bogføre betalingerne. Flere oplysninger i [Sådan afstemmes betalinger manuelt](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I erhvervsmiljøer, hvor kunden betaler noget tid efter levering. I overensstemmelse med betalingsbetingelserne forbliver en bogført salgsfaktura åben (ubetalt), indtil afdelingen for tilgodehavender bekræfter, at betaling er modtaget og udligner betalingen til den bogførte salgsfaktura. Dette kan gøres manuelt eller automatisk. Flere oplysninger i [Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter](receivables-how-apply-sales-transactions-manually.md) og [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).  

I forretningsmiljøer hvor debitor betaler med det samme, f.eks. via PayPal eller kontant, registreres betalingen med det samme, når du bogfører salgsfakturaen, dvs. at den bogførte salgsfaktura lukkes, som fuldt udlignet. Du vælger den relevante metode i feltet **Betalingsformskode** på salgsordren. Ved elektroniske betalinger, f.eks. PayPal, skal du også udfylde feltet **Betalingstjeneste**. Flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan også oprette direkte betalte fakturaer for ikke-registrerede kunder ved først at oprette et "kontantkunde"-kort for dem, som du så peger hen på salgsfakturaen. Flere oplysninger i [Konfigurere kontantkunder](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Hvis du vil sende rykkere til kunder om forfaldne betalinger, skal du oprette rykkerniveauer og-betingelser først. Flere oplysninger i [Oprette betingelser, niveauer og tekster for leveringsrykkere](finance-setup-reminders.md).  

## Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Udskrive pluklisten](sales-how-print-picking-list.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md#to-send-documents-by-email)  
[Indhente udestående beløb](receivables-collect-outstanding-balances.md)  
[Massefakturering fra Microsoft Bookings i Business Central](finance-bookings.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
