---
title: Oprette en salgsordre og sælge produkter | Microsoft Docs
description: Beskriver, hvordan du opretter en salgsnota for at registrere en aftale med en kunde om at sælge eller handle med produkter i henhold til bestemte betingelser.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 04/27/2020
ms.author: sgroespe
ms.openlocfilehash: 9a2fdbaafd2a6668d7fb4edf42c25438bd881e98
ms.sourcegitcommit: 7d54d8abe52e0546378cf760f5082f46e8441b90
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/30/2020
ms.locfileid: "3324434"
---
# <a name="sell-products"></a>Sælge produkter
Du opretter en salgsordre eller salgsfaktura for at registrere din aftale med en kunde om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.

> [!NOTE]  
>   Du skal bruge salgsordrer, hvis din salgsproces kræver, at du kan levere dele af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt på én gang. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge salgsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer salgsordrer på samme måde som salgsfakturaer. Du kan finde flere oplysninger i [Fakturere salg](sales-how-invoice-sales.md).

Du kan forhandle med kunden ved først at oprette et salgstilbud, som du kan konvertere til en salgsordre, når I har aftalt salget. Der er flere oplysninger i [Give salgstilbud](sales-how-make-offers.md).

Når debitoren har bekræftet aftalen, f.eks. efter en tilbudsproces, kan du sende en ordrebekræftelse for at registrere din forpligtelse til at levere produkterne som aftalt.

Når du leverer varerne, enten helt eller delvist, kan du bogføre salgsordren som leveret eller leveret og faktureret for at oprette de relaterede vare- og debitorposter i systemet. Når du bogfører salgsordren, kan du også sende dokumentet som en vedhæftet PDF-fil i en mail. Du kan få brødteksten i mailen udfyldt med en oversigt over ordre- og betalingsoplysninger, f.eks. et link til PayPal. Du kan finde flere oplysninger under [Sende dokumenter via mail](ui-how-send-documents-email.md).

I virksomhedsmiljøer, hvor kunden betaler et stykke tid efter levering i overensstemmelse med betalingsbetingelserne, forbliver en bogført salgsfaktura åben (ubetalt), indtil afdelingen for tilgodehavender bekræfter, at betaling er modtaget og udligner betalingen til den bogførte salgsfaktura. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

I forretningsmiljøer hvor debitor betaler med det samme, f.eks. via PayPal eller kontant, registreres betalingen med det samme, når du bogfører salgsordren som faktureret, dvs. at den bogførte salgsfaktura lukkes som fuldt udlignet. Du vælger den relevante metode i feltet **Betalingsformskode** på salgsordren. Se under trin 8. Ved elektroniske betalinger, f.eks. PayPal, skal du også udfylde feltet **Betalingstjeneste**. Du kan finde flere oplysninger i [Aktivere debitorbetalinger via betalingstjenester](sales-how-enable-payment-service-extensions.md).

Du kan også oprette direkte betalte ordrer for ikke-registrerede kunder ved først at oprette et "kontantkunde"-kort, som du så peger hen på salgsordren. Der er flere oplysninger under [Oprette kontantkunder](finance-how-to-set-up-cash-customers.md).

Du kan nemt rette eller annullere en bogført salgsfaktura, der er oprettet i forbindelse med en salgsordre, inden den betales. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Du kan finde flere oplysninger under [Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bogførte faktura betales, skal du oprette en salgskreditnota for at tilbageføre salget. Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varekortet kan være af typen **Lager**, **Service** og **Ikke-lager** for at angive, om varekortet repræsenterer en fysisk lagerenhed, en arbejdstidsenhed eller en fysisk enhed, der ikke opbevares på lageret. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md). Salgsordreprocessen er den samme for alle tre varetyper.

Du kan udfylde debitorfelter i salgsordren på to måder, afhængigt af om debitoren allerede er registreret. Se trin 2 og 3 i følgende procedure.

## <a name="to-create-a-sales-order"></a>Sådan oprettes en salgsordre
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.
2. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

    Andre felter på siden **Salgsordre** er nu udfyldt med standardoplysningerne for den valgte debitor. Hvis debitoren ikke er registreret, skal du følge disse trin:
3. I feltet **Debitor** skal du indtaste navnet på den nye debitor.
4. I dialogboksen, hvor du registrerer den nye debitor, skal du trykke på knappen **Ja**.
5. På siden **Vælg en skabelon til en ny debitor** skal du vælge en skabelon, som det nye debitorkort skal baseres på, og derefter vælge knappen **OK**.

    Et nyt debitorkort åbnes, udfyldt med oplysninger om den valgte debitorskabelon. Feltet **Navn** udfyldes på forhånd med den nye debitors navn, som du har angivet på salgsordren.
6. Fortsæt med at udfylde resten af felterne på debitorkortet. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  
7. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til siden **Salgsordre**.

    En række af felterne i salgsordren er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.
8. Udfylde de resterende felter efter behov på siden **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Hvis du tillader, at kunden betaler med det samme, f.eks. med kreditkort eller via PayPal, skal du udfylde feltet **Betalingsformskode**. Betalingen registreres derefter, når du bogfører salgsordren som faktureret. Hvis du vælger KONTANT, registreres betalingen i en bestemt modkonto.

    Du er nu klar til at udfylde salgsordrelinjerne med lagervarer eller services, som du ønsker at sælge til debitoren.

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.
9. I oversigtspanelet **Linjer** skal du i feltet **Vare** indsætte nummeret på en vare eller en service.  
10. Angiv det antal varer, der skal sælges, i feltet **Antal**.

    > [!NOTE]  
    >   For varer af typen Service er antallet en tidsenhed, f.eks. timer, der er angivet i feltet **Enhedskode** på linjen.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Enhedspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbene vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.
11. I feltet **Linjerabatpct.** kan du indtaste en procentdel, hvis du vil give debitoren en rabat på produktet. Værdien i feltet **Linjebeløb** opdateres tilsvarende.

    Hvis du har konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på tilbudslinjen automatisk, hvis de aftalte priskriterier opfyldes. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
12. Hvis du vil tilføje en kommentar om den tilbudslinje, som kunden kan se på det udskrevne salgstilbud, skal du skrive en tekst i feltet **Beskrivelse** på en tom linje.  
13. Gentag trin 9 til 12 for hver vare, du ønsker at sælge til debitoren.

    Totalerne under linjerne beregnes automatisk, mens du opretter eller redigerer linjer.
14. Et nyt debitorkort viser oplysninger om den valgte debitorskabelon. Udfyld de resterende felter. Du kan finde flere oplysninger i [Registrere nye debitorer](sales-how-register-new-customers.md).  
15. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til siden **Salgsordre**.

    En række af felterne i salgsordren er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.
16. Udfylde de resterende felter efter behov på siden **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du er nu klar til at udfylde salgsordrelinjerne for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren, som du vil registrere i en finanskonto.   

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.  
17. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.

18. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** være tomt i følgende tilfælde:

    * Hvis der er tale om en kommentar. Skriv bemærkningen i feltet **Beskrivelse**.
    * Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger under [Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

19. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.  

    > [!NOTE]  
    > Hvis varen er af typen **Service**, eller hvis feltet **Type** indeholder **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen. Du kan finde flere oplysninger i [Oprette vareenheder](inventory-how-setup-units-of-measure.md).

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
20. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
21. Gentag trin 9 til 12 for hvert produkt eller gebyr, du ønsker at sælge til debitoren.  

    Totalfelterne under linjerne opdateres automatisk, når du opretter eller redigerer linjer for at få vist de beløb, der skal bogføres i finansposterne.

    > [!NOTE]
    > I meget sjældne tilfælde kan de bogførte beløb afvige fra det, der er vist i totalfelterne. Dette skyldes typisk afrundingsberegninger i relation til moms.<br /><br />Hvis du vil kontrollere de beløb, der faktisk bogføres, kan du bruge siden **Statistik**, som tager højde for afrundingsberegningerne. Hvis du vælger handlingen **Frigiv**, opdateres totalfelterne, så de omfatter afrundingsberegninger.  
22. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
23. Hvis du kun vil sende en del af ordreantallet, skal du angive dette antal i feltet **Lever antal**. Værdien kopieres til feltet **Fakturer antal**.
24. Hvis du kun vil fakturere en del af det leverede antal, skal du angive dette antal i feltet **Fakturer antal**. Antallet skal være mindre end værdien i feltet **Lever antal**.   
25. Når salgsordrelinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.

Dialogboksen **Bekræftelse af bogfør og send** viser debitorens foretrukne metode til modtagelse af dokumenter. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger under [Konfigurere dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

De relaterede vare- og debitorposter oprettes nu i systemet, og salgsordren udlæses som et PDF-dokument. Når salgsordren er bogført fuldstændigt, fjernes den fra listen over salgsordrer og erstattes med nye dokumenter på listen over bogførte salgsfakturaer og oversigten over bogførte salgsleverancer.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Udskrive pluklisten](sales-how-print-picking-list.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sende dokumenter som mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
