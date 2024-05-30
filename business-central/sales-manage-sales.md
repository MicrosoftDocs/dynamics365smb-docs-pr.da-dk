---
title: Oversigt over opgaver til administration af salg
description: 'Læs alt om, hvordan du bruger Business Central''s services til at styre kundernes salgsaktiviteter med salgsfakturaer, ordrer, tilbud og meget mere.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: overview
ms.search.keywords: 'trade, sell'
ms.search.form: '253,'
ms.date: 01/25/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="sales"></a>Salg

Du opretter en salgsfaktura eller salgsordre for at registrere din aftale med en debitor om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.

Du skal bruge salgsordrer, hvis din salgsproces kræver, at du kan levere dele af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt med det samme. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge salgsordrer. I alle andre henseender fungerer salgsordrer på samme måde som salgsfakturaer. Ved salgsordrer kan du også bruge funktionen til beregning af leveringstid til at kommunikere bestemte leveringsdatoer til kunderne.  

Du kan forhandle med debitoren ved først at oprette et salgstilbud, som du kan konvertere til en salgsfaktura eller salgsordre, når I har aftalt salget. Når debitoren har bekræftet aftalen, kan du sende en ordrebekræftelse for at registrere din forpligtelse til at levere produkterne som aftalt.

Du kan nemt rette eller annullere en bogført salgsfaktura, før kunden betaler. Hvis du f.eks. vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Hvis den bogførte faktura betales, skal du oprette en salgskreditnota eller en salgsreturvareordre for at tilbageføre salget.

Gode fremgangsmåder ved salg og marketing drejer sig primært om, hvordan du træffer de bedste beslutninger på det rigtige tidspunkt. Microsoft-funktioner i [!INCLUDE[prod_short](includes/prod_short.md)] giver dig en præcis oversigt over dine kontaktoplysninger, så du kan betjene dine potentielle kunder mere effektivt og øge kundetilfredsheden. Flere oplysninger i [Relationsstyring](marketing-relationship-management.md).

Hvis du bruger Microsoft Dynamics 365 Sales til kundeengagementer, kan du bruge problemfri integration i lead-til-kontant-processen ved hjælp af [!INCLUDE [prod_short](includes/prod_short.md)] til back end-aktiviteter. For eksempel til at behandle ordrer, administrere lager og gennemføre din økonomi. Flere oplysninger i [Brug Dynamics 365 Sales fra Business Central](marketing-integrate-dynamicscrm.md).

I de situationer, hvor debitoren skal betale, før produkterne leveres, f.eks i detailbranchen, skal du vente på betalingsmodtagelse, før du leverer produkterne. I de fleste tilfælde kan du behandle indgående betalinger nogle uger efter levering ved at udligne betalingerne på de relaterede bogførte ubetalte salgsfakturaer. Flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

Salgsdokumenter kan sendes som PDF-filer, der er vedhæftet i en mail. Brødteksten i mailen indeholder et uddrag af salgsdokumentet, f.eks produkter, samlet beløb og et link til webstedet PayPal. Flere oplysninger i [Afsende dokumenter med e-mail](ui-how-send-documents-email.md).

For alle salgsprocesser kan du inkorporere en godkendelsesarbejdsgang. En godkendelsesproces kan f.eks. kræve, at en chef godkender stort salg til bestemte kunder. Flere oplysninger i [Bruge workflows](across-use-workflows.md).

De følgende afsnit beskriver en opgavesekvens med links til de artikler, der dækker opgaverne.

## <a name="get-started-with-sales-capabilities"></a>Introduktion til salgsfunktioner

Før du sælger, skal du angive, hvordan du vil administrere virksomhedens salgsprocesser.

|Til...| Se |
|---|---|
| Opret et debitorkort for hver debitor, du sælger til.|[Registrere nye debitorer](sales-how-register-new-customers.md) |
| Konfigurere den måde, du sælger på, f.eks. priser og rabatter, debitorpris- og rabatgrupper, sælgere, leveringsmetoder og agenter. | [Opsætte salg](sales-setup-sales.md) |

## <a name="sales-analytics"></a>Salgsanalyse

I dette afsnit beskrives de analyseværktøjer, du kan bruge til at få indsigt i dine salgsdata.

| Til... | Se |
| --- | --- |
| Få mere at vide om funktioner til analyse af salgsdata. | [Oversigt over salgsanalyse](sales-analytics-overview.md) |
| Foretag ad hoc-analyser af salgsdata direkte på listesider og forespørgsler. | [Oprette salgsanalyserapporter](bi-how-create-analysis-views-reports.md) |
| Udforsk indbyggede salgsrapporter. | [Indbyggede salgsrapporter](sales-reports.md) |

## <a name="quote-to-order-to-sales-invoice"></a>Tilbud til ordre for salgsfaktura

I følgende tabel kan du se, hvordan du bruger enkle salgsprocesser.

|Til...| Se |
|---|---|
| Opret et salgstilbud med produkter på betingelser, der kan forhandles, før du konverterer tilbuddet til en salgsfaktura. |[Foretage Salgstilbud](sales-how-make-offers.md) |
| Behandl en salgsordre (måske med en delvis levering eller brug af direkte levering.) |[Sælge produkter](sales-how-sell-products.md) |
| Opret en salgsfaktura for at registrere din aftale med en debitor om at sælge visse produkter på bestemte leverings- og betalingsbetingelser. |[Fakturasalg](sales-how-invoice-sales.md) |
|Forstå, hvad der sker, når du bogfører salgsdokumenter.|[Bogføring af salg](ui-post-sales.md)|

Hvis du har brug for mere komplekse salgsprocesser, indeholder følgende tabel artikler, der forklarer, hvad du kan gøre med [!INCLUDE[prod_short](includes/prod_short.md)].

|Til...| Se |
|---|---|
| Opfylde en salgsordre med flere delleverancer. | [Behandle delleverancer](sales-how-send-partial-shipments.md) |
| Du kan oprette standardsalgs- eller købslinjer, som du hurtigt kan indsætte i dokumenter, f.eks. for tilbagevendende genbestillingsordrer.|[Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)|  
|Administrer kundens tilsagn om at købe store mængder, der leveres i portioner over en periode.|[Arbejde med rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md)|
|Fakturer en kunde for flere leverancer én gang ved at samle leverancerne på samme faktura.|[Kombinere leverancer på én enkelt faktura](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Sælg montageelementer, der ikke er tilgængelige i øjeblikket, ved at oprette en tilknyttet montageordre. Montageordren kan levere hele eller en del af antallet på salgsordren.|[Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md)|

## <a name="pick-and-ship"></a>Pluk og levering

I følgende tabel beskrives, hvordan du plukker varer til en salgsordre og leverer dem til kunden.

| Til | Se |
| --- | --- |
|Forberedelse af plukning af varer til leverance.|[Udskrive pluklisten](sales-how-print-picking-list.md)|
| Knyt en salgsordre til en købsordre for at sælge en vare med direkte levering, som skal leveres direkte fra leverandøren til kunden. |[Foretage direkte leveringer](sales-how-drop-shipment.md) |
|Få en katalogvare sendt fra en leverandør til dit lagersted, så du kan levere varen til kunden.|[Oprette specialordrer](sales-how-to-create-special-orders.md)|
|Informer debitorerne om ordreleveringsdatoer ved at beregne enten den første mulige afsendelsesdato eller disponibel til leverings-dato.|[Beregne ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)|
| Få mere at vide om, hvordan du sporer en pakke fra en bogført salgsleverance. | [Spore pakker](sales-how-track-packages.md) |

## <a name="canceled-orders-refunds-and-returns"></a>Annullerede ordrer, refusioner og returneringer

I følgende tabel beskrives det, hvordan du håndterer annullerede ordrer, refusioner og returneringer af varer.

| Til | Se |
| --- | --- |
| Udfør en handling på en ubetalt bogført salgsfaktura for automatisk at oprette en kreditnota og enten annullere salgsfakturaen eller gendanne den, så du kan foretage rettelser. |[Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md) |
| Opret en salgskreditnota for at tilbageføre en bestemt bogført salgsfaktura, så den afspejler, hvilke produkter Customer Returns, og hvilke indbetalte beløb der skal refunderes. |[Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md) |

## <a name="other-processes-in-sales"></a>Øvrige processer i salg

I følgende tabel kan du se, hvordan du håndterer andre salgsprocesser.

| Til | Se |
| --- | --- |
|Løse forvirring, når der findes to eller flere poster for samme debitor.|[Flette dublerede poster](sales-how-merge-duplicate-records.md)|

## <a name="see-also"></a>Se også

[Konfigurere salg](sales-setup-sales.md)  
[Registrere nye debitorer](sales-how-register-new-customers.md)  
[Oversigt over salgsanalyse](sales-analytics-overview.md)   
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
