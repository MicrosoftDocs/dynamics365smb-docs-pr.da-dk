---
title: Oversigt over opgaver til administration af indkøb
description: 'Beskriver opgaver, du kan bruge til at administrere dine indkøb eller indkøbsprocesser, herunder hvordan købsfakturaer og købsordrer fungerer.'
author: brentholtorf
ms.topic: overview
ms.devlang: al
ms.search.keywords: 'procurement, supply, vendor order'
ms.search.form: '460, 9307'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Indkøb

Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer også til dynamisk at opdatere lagerniveauer, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer, bidrager til avancebeløb og andre finansielle nøgletal i dit Rollecenter.

Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer.

Du kan få købsfakturaer oprettet automatisk ved hjælp af tjenesten OCR (Optical Character Recognition) for at konvertere PDF fakturaer fra dine kreditorer til elektroniske dokumenter, som derefter konverteres til købsfakturaer via et workflow. For at bruge denne funktion skal du først tilmelde dig OCR-tjenesten og derefter udføre forskellige installationer. Du kan finde flere oplysninger i [Indgående bilag](across-income-documents.md).

Produkterne kan være både lagervarer og services. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

Ved alle indkøbsprocesser kan du inkludere et godkendelsesworkflow, f.eks. for at kræve, at store køb godkendes af regnskabschefen. Du kan finde flere oplysninger i [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).

De følgende afsnit beskriver en opgavesekvens med links til de artikler, der dækker opgaverne.

## Introduktion til købsfunktioner

Før du køber varer, skal du angive, hvordan du vil administrere virksomhedens købsprocesser.

|Til...| Se |
|---|---|
| Konfigurere de regler og værdier, der definerer virksomhedens købsmetoder. | [Opsætte indkøb](purchasing-setup-purchasing.md) |
| Registrer hver kreditor, som du køber fra, med et kreditorkort. | [Registrere nye kreditorer](purchasing-how-register-new-vendors.md) |

## Købsanalyse

I dette afsnit beskrives de analyseværktøjer, du kan bruge til at få indsigt i dine købsprocesser.

| Til... | Se |
| --- | --- |
| Få mere at vide om funktioner til analyse af købsdata. | [Oversigt over indkøb](purchasing-analytics-overview.md) |
| Foretag ad hoc-analyser af købsdata direkte på listesider og forespørgsler. | [Ad hoc-analyse af indkøbsdata](ad-hoc-analysis-purchasing.md) |
| Udforsk indbyggede købsrapporter. | [Indbyggede indkøbsrapporter](purchase-reports.md) |

## Tilbud til ordre for købsfaktura

I følgende tabel kan du se, hvordan du bruger enkle købsprocesser.

| Til | Se |
| --- | --- |
|Oprette en købsrekvisition for at afspejle en tilbudsanmodning fra en leverandør, som du senere kan konvertere til en købsordre.|[Anmode om tilbud](purchasing-how-request-quotes.md)|
| Opret en købsfaktura for alle eller markerede linjer i en salgsfaktura. |[Købe varer til et salg](purchasing-how-purchase-products-sale.md) |
| Oprette en købsfaktura for at registrere din aftale med en kreditor om at købe produkter på bestemte leverings- og betalingsbetingelser. |[Registrere køb](purchasing-how-record-purchases.md) |
| Lær, hvordan [!INCLUDE[prod_short](includes/prod_short.md)] beregner, hvornår du skal bestille en vare for at modtage den på en bestemt dato.|[Beregne dato for køb](purchasing-date-calculation-for-purchases.md)|
|Forstå, hvad der sker, når du bogfører købsdokumenter.|[Bogføring af køb](ui-post-purchases.md)|

Hvis du har brug for mere komplekse købsprocesser, indeholder følgende tabel artikler, der forklarer, hvad du kan gøre med [!INCLUDE[prod_short](includes/prod_short.md)].

| Til | Se |
| --- | --- |
| Udfør en handling på en ubetalt bogført købsfaktura for automatisk at oprette en kreditnota og enten annullere købsfakturaen eller gendanne den, så du kan foretage rettelser. |[Rette eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opret en købskreditnota for at tilbageføre en bestemt bogført købsfaktura, så den afspejler, hvilke produkter du returnerer til kreditoren, og hvilke indbetalte beløb der skal opkræves. |[Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md) |
|Administrer dit tilsagn til en kreditor om at købe store mængder, der leveres i portioner over en periode.|[Arbejde med rammekøbsordrer](sales-how-to-create-blanket-sales-orders.md)|


## Annullerede ordrer, refusioner og returneringer

I følgende tabel beskrives det, hvordan du håndterer annullerede ordrer, refusioner og returneringer af varer, du køber.

| Til | Se |
| --- | --- |
|Forberede fakturering af flere leverancer fra den samme leverandør på én gang ved at kombinere leverancer på én faktura.|[Kombinere modtagelser på én enkelt faktura](purchasing-how-to-combine-receipts.md)|
|Konvertere eksempelvis elektroniske fakturaer fra dine leverandører til købsfakturaer i Business Central.|[Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|


## Øvrige processer i salg

I følgende tabel kan du se, hvordan du håndterer andre købsprocesser.

| Til | Se |
| --- | --- |
|Løse forvirring, når der findes to eller flere poster for samme kreditor.|[Flette dublerede poster](sales-how-merge-duplicate-records.md)|


## Eksterne bilagsnumre

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Se også

[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Oversigt over indkøbsanalyse](purchasing-analytics-overview.md)   
[Administrere skyldige beløb](payables-manage-payables.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
