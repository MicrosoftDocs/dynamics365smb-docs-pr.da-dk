---
title: "Fremgangsmåde: Afstemme betalinger, der ikke kan udlignes automatisk | Microsoft Docs"
description: "Fremgangsmåde: Afstemme betalinger, der ikke kan udlignes automatisk"
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7b4c109ebda260ee86e2b955a17389b54493de65
ms.contentlocale: da-dk
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-reconcile-payments-that-cannot-be-applied-automatically"></a>Fremgangsmåde: Afstemme betalinger, der ikke kan udlignes automatisk
Det kan være nødvendigt at håndtere betalinger til din bankkonto, der ikke kan udlignes på en relateret åben debitor-, kreditor eller bankkontopost. Det kan skyldes, at der ikke findes noget dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], som betalingen kan udlignes til, eller at det relaterede dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)] har et andet beløb end f.eks. transaktionsbeløbet på grund af valutakurser. I vinduet **Betalingsudligningskladde** vises alle transaktionsbeløb for betalinger, som endnu ikke er udlignet, i feltet **Difference**, herunder beløb, der ikke kan udlignes af årsager som f.eks. dem ovenfor.

Betalinger, der ikke kan udlignes, kan blive vist på betalingsudligningskladdelinjer på følgende måder:

* Værdien i feltet **Difference** er lig med værdien i feltet **Transaktionsbeløb**, hvilket angiver, at ingen del af betalingen kan udlignes til en relateret åben debitor-, kreditor- eller bankkontopost.
* Værdien i feltet **Difference** er lavere end værdien i feltet **Transaktionsbeløb**, hvilket angiver, at en del af betalingen kan udlignes til en relateret åben debitor-, kreditor- eller bankkontopost. Den resterende del af betalingen kan ikke udlignes og skal afstemmes manuelt eller ved bogføring direkte på en konto.

Når du vil afstemme sådanne betalinger, kan du vælge knappen Overfør difference til konto og derefter angive, hvilken konto beløbet i feltet Difference skal bogføres på, når du bogfører betalingsudligningskladden.

**Bemærk**: Der findes lignende funktioner, som bruges til at konfigurere automatisk afstemning af tilbagevendende betalinger, der kan udlignes på relaterede åbne debitor-, kreditor- eller bankkontoposter. Du kan finde flere oplysninger under [Fremgangsmåde: Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)

## <a name="to-reconcile-payments-that-cannot-be-applied"></a>Sådan afstemmes betalinger, der ikke kan udlignes
1. I øverste højre hjørne skal du vælge ikonet **Søg efter side eller rapport** ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Betalingsudligningskladder** og derefter vælge det relaterede link.
2. Åbn en kladde til betalingsafstemning. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).
3. Vælg **Overfør difference til konto**. Vinduet **Overfør difference til konto** åbnes.
4. I feltet **Kontotype** skal du angive den kontotype, som betalingsbeløbet vil blive bogført til.
5. I feltet **Kontonr.** skal du angive den konto, som betalingsbeløbet bliver bogført på.
6. I feltet **Beskrivelse** skal du angive tekst, der beskriver denne direkte betalingsbogføring. Som standard indsættes teksten i feltet **Transaktionstekst** på betalingsudligningskladdelinjen.
7. Vælg knappen **OK**.

Hvis værdien i feltet **Difference** er lig med værdien i feltet **Transaktionsbeløb**, når du har bogført betalingsudligningskladden, bliver hele betalingen på kladdelinjen bogført direkte på den angivne modkonto.

Hvis værdien i feltet **Difference** er lavere end værdien i feltet **Transaktionsbeløb**, oprettes der en ekstra kladdelinje med den samme tekst og dato og differencen indsættes i feltet **Transaktionsbeløb**. På den oprindelige kladdelinje fratrækkes differencen fra værdien i feltet **Transaktionsbeløb**, og betalingen vil forsat blive udlignet på den relaterede debitor-, kreditor- eller bankkontopost. Når du bogfører betalingsudligningskladden, bliver en del af betalingen bogført som en udlignet betaling. Den anden del af betalingen vil blive bogført direkte på den angivne konto.

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

