---
title: Oprette en salgsfaktura eller salgsordre | Microsoft Docs
description: Beskriver, hvordan du opretter en salgsnota, en salgsfaktura eller salgsordre for at registrere en aftale med en kunde om at sælge produkter i henhold til bestemte betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: ccc909b56e3d1d1d48915470b819be2c91c92b9b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/01/2019
ms.locfileid: "2312192"
---
# <a name="invoice-sales"></a>Fakturere salg
Du opretter en salgsfaktura eller salgsordre for at registrere din aftale med en debitor om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.  

I nogle situationer skal du bruge en salgsordre i stedet for en salgsfaktura:  

* Hvis du kun vil levere en del af et ordreantal, f.eks. fordi hele antallet ikke er på lager.  
* Hvis du sælger varer, som leverandøren leverer direkte til kunden. Det kaldes direkte levering. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md).  

I alle andre henseender fungerer salgsordrer og salgsfakturaer på samme måde. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).

Du kan forhandle med debitoren ved først at oprette et salgstilbud, som du kan konvertere til en salgsfaktura, når I har aftalt salget. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).

Hvis kunden beslutter at købe, bogfører du salgsfakturaen for at oprette det relaterede antal og værdiposterne. Når du bogfører salgsfakturaen, kan du også sende dokumentet som en vedhæftet PDF-fil i en mail. Du kan få brødteksten i mailen udfyldt med en oversigt over faktura- og betalingsoplysninger, f.eks. et link til PayPal. Du kan finde flere oplysninger under [Sende dokumenter via mail](ui-how-send-documents-email.md). Når kunden derefter betaler fakturaen, kan du registrere betalingen på forskellige måder, afhængigt af størrelsen og de foretrukne arbejdsgange i organisationen. Du kan finde flere oplysninger i sektionen [Registrere udbetalinger](#registering-payments).  


Du kan nemt rette eller annullere en bogført salgsfaktura, før den er betalt. Dette er nyttigt, hvis du f.eks. vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Du kan finde flere oplysninger under [Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bogførte faktura betales, skal du oprette en salgskreditnota for at tilbageføre salget. Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varekortet kan være af typen **Lager**, **Service** og **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke opbevares på lageret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md). Salgsfakturaprocessen er den samme for alle tre varetyper.

Du kan udfylde debitorfelter i salgsfakturaen på to måder, afhængigt af om debitoren er registreret. Se trin 2 og 3 i følgende procedure.

## <a name="to-create-a-sales-invoice"></a>Sådan oprettes en salgsfaktura
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsfakturaer**, og vælg derefter det relaterede link.  
2. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

   Andre felter på siden **Salgsfaktura** indeholder standardoplysningerne om den valgte debitor. Hvis debitoren ikke er registreret, skal du følge disse trin:
3. I feltet **Debitor** skal du indtaste navnet på den nye debitor.
4. I dialogboksen, hvor du registrerer den nye debitor, skal du trykke på knappen **Ja**.
5. På siden **Vælg en skabelon til en ny debitor** skal du vælge en skabelon, som det nye debitorkort skal baseres på, og derefter vælge knappen **OK**.
6. Et nyt debitorkort viser oplysninger om den valgte debitorskabelon. Udfyld de resterende felter. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  
7. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til siden **Salgsfaktura**.

   En række af felterne i salgsfakturaen er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.  
8. Udfylde de resterende felter efter behov på siden **Salgsfaktura**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du tillader, at kunden betaler med det samme, f.eks. kontant eller via PayPal, skal du udfylde feltet **Betalingsformskode**. Betalingen registreres derefter, når du bogfører salgsfakturaen. Hvis du vælger KONTANT, registreres betalingen i en bestemt modkonto.

    Du er nu klar til at udfylde salgsfakturalinjerne for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren, som du vil registrere i en finanskonto.   

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.  
9. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.
10. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** være tomt i følgende tilfælde:

    * Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    * Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

11. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.  

    > [!NOTE]  
    > Hvis varen er af typen **Service**, eller hvis feltet **Type** indeholder **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen. Du kan finde flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md).

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
12. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Gentag trin 9 til 12 for hvert produkt eller gebyr, du vil fakturere debitoren for.  

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

    > [!NOTE]
    > I meget sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.<br /><br />Hvis du vil kontrollere de beløb, der faktisk bogføres, kan du bruge siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.
14. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Når salgsfakturalinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.  

Dialogboksen **Bekræftelse af bogfør og send** viser debitorens foretrukne metode til modtagelse af dokumenter. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

De relaterede vare- og debitorposter oprettes nu i systemet, og salgsfakturaen udlæses som et PDF-dokument. Salgsfakturaen fjernes fra listen over salgsfakturaer og erstattes med et nyt bilag i oversigten over bogførte salgsfakturaer.  

## <a name="registering-payments"></a>Registrere betalinger

Afhængigt af dine forretningsmæssige behov kan du modtage betaling og registrere den på forskellige måder: manuelt, automatisk og ved hjælp af betalingstjenester.  

Du kan behandle betalingerne direkte fra debitorkortet. Brug handlingen **Registrer debitorbetalinger** for at hente en oversigt over de ubetalte fakturaer for den pågældende kunde. Marker fakturaen som betalt delvist eller helt. Denne betalingsudligning behandler dine debitorbetalinger ved at afstemme beløb, der er modtaget på bankkontoen, med de relaterede ubetalte salgsfakturaer og derefter bogføre betalingerne. Du kan finde flere oplysninger i [Sådan afstemmes betalinger manuelt](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

I virksomhedsmiljøer, hvor kunden betaler et stykke tid efter levering i overensstemmelse med betalingsbetingelserne, forbliver en bogført salgsfaktura åben (ubetalt), indtil afdelingen for tilgodehavender bekræfter, at betaling er modtaget og udligner betalingen til den bogførte salgsfaktura. Dette kan gøres manuelt eller automatisk. Du kan finde flere oplysninger i [Afstemme betalinger fra debitorer med indbetalingskladden eller fra debitorposter](receivables-how-apply-sales-transactions-manually.md) og [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).  

I forretningsmiljøer hvor debitor betaler med det samme, f.eks. via PayPal eller kontant, registreres betalingen med det samme, når du bogfører salgsfakturaen, dvs. at den bogførte salgsfaktura lukkes, som fuldt udlignet. Du vælger den relevante metode i feltet **Betalingsformskode** på salgsordren. Se under trin 8. Ved elektroniske betalinger, f.eks. PayPal, skal du også udfylde feltet **Betalingstjeneste**. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).  

Du kan også oprette direkte betalte fakturaer for ikke-registrerede kunder ved først at oprette et "kontantkunde"-kort, som du så peger hen på salgsfakturaen. Der er flere oplysninger under [Oprette kontantkunder](finance-how-to-set-up-cash-customers.md).  

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Massefakturering fra Microsoft Bookings i Business Central](finance-bookings.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
