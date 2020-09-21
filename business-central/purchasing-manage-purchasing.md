---
title: Oversigt over opgaver til administration af køb | Microsoft Docs
description: Beskriver opgaver, du kan bruge til at administrere dine indkøb eller indkøbsprocesser, herunder hvordan købsfakturaer og købsordrer fungerer.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: aa6a7222807241280dfbeb4320d958afd6f55d51
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778811"
---
# <a name="purchasing"></a>Indkøb
Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer også til dynamisk at opdatere lagerniveauer, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer, bidrager til avancebeløb og andre finansielle nøgletal i dit Rollecenter.

Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer.

Du kan få købsfakturaer oprettet automatisk ved hjælp af tjenesten OCR (Optical Character Recognition) for at konvertere PDF fakturaer fra dine kreditorer til elektroniske dokumenter, som derefter konverteres til købsfakturaer via et workflow. For at bruge denne funktion skal du først tilmelde dig OCR-tjenesten og derefter udføre forskellige installationer. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle indgående bilag](across-process-income-documents.md).      

Produkterne kan være både lagervarer og services. Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).

Ved alle indkøbsprocesser kan du inkludere et godkendelsesworkflow, f.eks. for at kræve, at store køb godkendes af regnskabschefen. Du kan finde flere oplysninger under [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette en købsfaktura for at registrere din aftale med en kreditor om at købe produkter på bestemte leverings- og betalingsbetingelser. |[Registrere køb](purchasing-how-record-purchases.md) |
|Oprette en købsrekvisition for at afspejle en tilbudsanmodning fra en leverandør, som du senere kan konvertere til en købsordre.|[Anmode om tilbud](purchasing-how-request-quotes.md)|
| Opret en købsfaktura for alle eller markerede linjer i en salgsfaktura. |[Købe varer til et salg](purchasing-how-purchase-products-sale.md) |
|Forstå, hvad der sker, når du bogfører købsdokumenter.|[Bogføring af køb](ui-post-purchases.md)|
| Udfør en handling på en ubetalt bogført købsfaktura for automatisk at oprette en kreditnota og enten annullere købsfakturaen eller gendanne den, så du kan foretage rettelser. |[Rette eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opret en købskreditnota for at tilbageføre en bestemt bogført købsfaktura, så den afspejler, hvilke produkter du returnerer til kreditoren, og hvilke indbetalte beløb der skal opkræves. |[Behandle købsreturvarer eller annulleringer](purchasing-how-register-new-vendors.md) |
|Forberede fakturering af flere leverancer fra den samme leverandør på én gang ved at kombinere leverancer på én faktura.|[Kombinere modtagelser på én enkelt faktura](purchasing-how-to-combine-receipts.md)|
|Konvertere eksempelvis elektroniske fakturaer fra dine leverandører til købsfakturaer i Business Central.|[Modtage og konvertere elektroniske dokumenter](purchasing-how-to-receive-and-convert-electronic-documents.md)|
| Lær, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner, hvornår du skal bestille en vare for at modtage den på en bestemt dato.|[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)|
|Løse forvirring, når der findes to eller flere poster for samme kreditor.|[Flette dublerede poster](sales-how-merge-duplicate-records.md)|
|Administrer dit tilsagn til en kreditor om at købe store mængder, der leveres i portioner over en periode.|[Arbejde med rammekøbsordrer](sales-how-to-create-blanket-sales-orders.md)|

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/purchase-items-services-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Administrere projekter](projects-manage-projects.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
