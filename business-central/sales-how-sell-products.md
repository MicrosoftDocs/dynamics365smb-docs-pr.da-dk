---
title: Oprette en kundesalgsordre og sælge produkter
description: Beskriver, hvordan du opretter en salgsnota for at registrere en aftale med en kunde om at sælge eller handle med produkter i henhold til bestemte betingelser.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, partial deliveries, customer sales order
ms.search.form: 42, 48, 9305
ms.date: 01/19/2022
ms.author: edupont
ms.openlocfilehash: 52060d74d7ef855a89dd3cffabd4ada435d6b117
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8523263"
---
# <a name="sell-products-with-a-customer-sales-order"></a>Sælge produkter med en kundesalgsordre  

Denne artikel giver brugerne vejledning om, hvornår de skal benytte en kunde salgsordre i stedet for blot en faktura. Hvis din salgsproces kræver, at du kun kan levere dele af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt på én gang, kan du sælge disse produkter ved at oprette en kundesalgsordre.  

Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge salgsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer salgsordrer på samme måde som salgsfakturaer. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).

Når du leverer varerne, enten helt eller delvist, kan du bogføre salgsordren som leveret eller leveret og faktureret for at oprette de relaterede vare- og debitorposter i systemet. Når du bogfører salgsordren, kan du også sende dokumentet som en vedhæftet PDF-fil i en mail. Du kan få brødteksten i mailen udfyldt med en oversigt over ordre- og betalingsoplysninger, f.eks. et link til PayPal. Du kan finde flere oplysninger i [Sende dokumenter via mail](ui-how-send-documents-email.md).

I forretningsmiljøer hvor debitor betaler med det samme, f.eks. via PayPal eller kontant, registreres betalingen med det samme, når du bogfører salgsordren som faktureret, dvs. at den bogførte salgsfaktura lukkes som fuldt udlignet. Du vælger den relevante metode i feltet **Betalingsformskode** på salgsordren. Se under trin 8. Ved elektroniske betalinger, f.eks. PayPal, skal du også udfylde feltet **Betalingstjeneste**. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan også oprette direkte betalte ordrer for ikke-registrerede kunder ved først at oprette et "kontantkunde"-kort, som du så peger hen på salgsordren. Der er flere oplysninger under [Oprette kontantkunder](finance-how-to-set-up-cash-customers.md).

## <a name="to-create-a-sales-order"></a>Sådan oprettes en salgsordre

> [!NOTE]  
> I følgende procedure antages det, at kunden allerede er oprettet. Yderligere oplysninger om, hvordan du gør dette, finder du i [Registrere nye kunder](sales-how-register-new-customers.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Salgsordrer**, og vælg derefter det relaterede link.
2. Vælg **Ny** for at oprette en ny post.
3. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

    Andre felter på siden **Salgsordre** er nu udfyldt med standardoplysningerne for den valgte debitor.  

4. Udfylde de resterende felter efter behov på siden **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du tillader, at kunden betaler med det samme, f.eks. med kreditkort eller via PayPal, skal du udfylde feltet **Betalingsformskode**. Betalingen registreres derefter, når du bogfører salgsordren som faktureret. Hvis du vælger KONTANT, registreres betalingen i en bestemt modkonto.

    Du er nu klar til at udfylde salgsordrelinjerne med lagervarer eller services, som du ønsker at sælge til debitoren.

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.
5. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.

6. I feltet **Nummer** angive nummeret på en vare eller en service.

    Lad feltet **Nummer** være tomt i følgende tilfælde:

    * Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    * Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger i [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).
7. Angiv det antal varer, der skal sælges, i feltet **Antal**.

    > [!NOTE]  
    > For varer af typen *Ressource* eller *Service* er antallet en tidsenhed, f.eks. timer, der er angivet i feltet **Enhedskode** på linjen. Du kan finde flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md).

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Enhedspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbene vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.
8. I feltet **Linjerabatpct.** kan du indtaste en procentdel, hvis du vil give debitoren en rabat på produktet. Værdien i feltet **Linjebeløb** opdateres tilsvarende.

    Hvis du har konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på tilbudslinjen automatisk, hvis de aftalte priskriterier opfyldes. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
9. Hvis du vil tilføje en kommentar om den ordrelinje, som debitoren kan se på det udskrevne ordrer, skal du skrive en kommentar i feltet **Beskrivelse** på en tom linje.  
10. Gentag trin 5 til 9 for hver vare, du ønsker at sælge til debitoren.

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

    > [!NOTE]
    > I meget sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.
    >
    > Hvis du vil kontrollere de beløb, der faktisk bogføres, kan du bruge siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.  

11. Eller angiv i feltet **Fakturarabatbeløb** et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger i [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
12. Hvis du kun vil sende en del af ordreantallet, skal du angive dette antal i feltet **Lever antal**. Værdien kopieres til feltet **Fakturer antal**.
13. Hvis du kun vil fakturere en del af det leverede antal, skal du angive dette antal i feltet **Fakturer antal**. Antallet skal være mindre end værdien i feltet **Lever antal**.  
14. Når salgsordrelinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Dialogboksen **Bekræftelse af bogfør og send** viser debitorens foretrukne metode til modtagelse af dokumenter. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger i [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

De relaterede vare- og debitorposter oprettes nu i systemet, og salgsordren udlæses som et PDF-dokument. Når salgsordren er bogført fuldstændigt, fjernes den fra listen over salgsordrer og erstattes med nye dokumenter på listen over bogførte salgsfakturaer og oversigten over bogførte salgsleverancer.  

## <a name="external-document-number"></a>Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Se også

[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Udskrive pluklisten](sales-how-print-picking-list.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]