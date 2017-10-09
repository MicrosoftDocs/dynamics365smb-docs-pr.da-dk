---
title: Oversigt over opgaver til administration af salg | Microsoft Docs
description: Beskriver, hvordan du administrerer salgsaktiviteter.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 95f235e743ed97b1ac90a6e0583b9bd19dcb7ead
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="sales"></a>Salg
Du opretter en salgsfaktura eller salgsordre for at registrere din aftale med en debitor om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.

Du skal bruge salgsordrer, hvis din salgsproces kræver, at du kan levere dele af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt på én gang. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge salgsordrer. I alle andre henseender fungerer salgsordrer på samme måde som salgsfakturaer. Ved salgsordrer kan du også bruge funktionen til beregning af leveringstid til at kommunikere bestemte leveringsdatoer til kunderne.  

Du kan forhandle med debitoren ved først at oprette et salgstilbud, som du kan konvertere til en salgsfaktura eller salgsordre, når I har aftalt salget. Når debitoren har bekræftet aftalen, kan du sende en ordrebekræftelse for at registrere din forpligtelse til at levere produkterne som aftalt.

Du kan nemt rette eller annullere en bogført salgsfaktura, før den er betalt. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Hvis den bogførte faktura betales, skal du oprette en salgskreditnota eller en salgsreturvareordre for at tilbageføre salget.

Gode fremgangsmåder ved salg og marketing drejer sig primært om, hvordan du træffer de bedste beslutninger på det rigtige tidspunkt. Microsoft-funktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)] giver dig en præcis oversigt over dine kontaktoplysninger, så du kan betjene dine potentielle kunder mere effektivt og øge kundetilfredsheden. Du kan finde flere oplysninger i [Relationsstyring](marketing-relationship-management.md).

I de situationer, hvor debitoren skal betale, før produkterne leveres, f.eks i detailbranchen, skal du vente på betalingsmodtagelse, før du leverer produkterne. I de fleste tilfælde kan du behandle indgående betalinger nogle uger efter levering ved at udligne betalingerne på de relaterede bogførte ubetalte salgsfakturaer. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

Salgsdokumenter kan sendes som PDF-filer, der er vedhæftet i en mail. Brødteksten i mailen indeholder et uddrag af salgsdokumentet, f.eks produkter, samlet beløb og et link til webstedet PayPal. Du kan finde flere oplysninger under [Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md).

Ved alle salgsprocesser kan du inkludere et godkendelsesworkflow, f.eks. for at kræve, at store salg til bestemte kunder godkendes af regnskabschefen. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Opret et salgstilbud, hvor du f.eks. tilbyder produkter på betingelser, der kan forhandles, før du konverterer tilbuddet til en salgsfaktura. |[Fremgangsmåde: Fremsætte tilbud](sales-how-make-offers.md) |
| Opret en salgsfaktura for at registrere din aftale med en debitor om at sælge produkter på bestemte leverings- og betalingsbetingelser. |[Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md) |
| Behandl en salgsordre, der involverer delvis levering eller direkte levering. |[Fremgangsmåde: Sælge produkter](sales-how-sell-products.md) |
|Du kan oprette standardsalgs- eller købslinjer, som du hurtigt kan indsætte i dokumenter, f.eks. for tilbagevendende genbestillingsordrer.|[Fremgangsmåde: Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md)|  
| Knyt en salgsordre til en købsordre for at sælge en vare med direkte levering, som skal leveres direkte fra leverandøren til kunden. |[Fremgangsmåde: Foretage direkte leveringer](sales-how-drop-shipment.md) |
|Få en katalogvare sendt fra en leverandør til dit lagersted, så du kan levere varen til kunden.|[Sådan oprettes specialordrer](sales-how-to-create-special-orders.md)|
| Udfør en handling på en ubetalt bogført salgsfaktura for automatisk at oprette en kreditnota og enten annullere salgsfakturaen eller gendanne den, så du kan foretage rettelser. |[Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md) |
| Opret en salgskreditnota for at tilbageføre en bestemt bogført salgsfaktura, så den afspejler, hvilke produkter debitoren returnerer, og hvilke indbetalte beløb der skal refunderes. |[Fremgangsmåde: Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md) |
|Administrer kundens tilsagn om at købe store mængder, der leveres i portioner over en periode.|[Fremgangsmåde: Arbejde med rammesalgsordrer](sales-how-to-create-blanket-sales-orders.md)|
|Sælg montageelementer, der ikke er tilgængelige i øjeblikket, ved at oprette en tilknyttet montageordre for at levere den fulde eller delvise salgsordremængde.|[Sådan sælger du en vare, der er monteret efter ordre](assembly-how-to-sell-items-assembled-to-order.md)|
|Fakturer en kunde for flere leverancer én gang ved at samle leverancerne på samme faktura.|[Sådan kombineres leverancer på én enkelt faktura](sales-how-to-combine-shipments-on-a-single-invoice.md)|
|Informer debitorerne om ordreleveringsdatoer ved at beregne enten den første mulige afsendelsesdato eller disponibel til leverings-dato.|[Sådan beregnes ordrebekræftelsesdatoer](sales-how-to-calculate-order-promising-dates.md)|

## <a name="see-also"></a>Se også
[Konfigurere salg](sales-setup-sales.md)  
[Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Projektstyring](projects-manage-projects.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

