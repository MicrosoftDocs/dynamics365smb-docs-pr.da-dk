---
title: Sådan rettes forudbetalinger | Microsoft Docs
description: Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den. Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 0ed9bed71ca73e25197869f1f670251ae523648c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5783530"
---
# <a name="correct-prepayments"></a>Rette forudbetalinger

Du kan foretage en rettelse af en ordre, efter at du har bogført en forudbetalingsfaktura for den. Du kan indsætte nye linjer i ordren, efter at der er udstedt en forudbetaling, og derefter kan du bogføre en anden forudbetalingsfaktura, men du kan ikke slette en linje fra en ordre, hvis der allerede er faktureret en forudbetaling for linjen.  

> [!TIP]
> Hvis du har bogført en forudbetalingsfaktura for en salgsfaktura, som du derefter retter eller annullerer, skal du også rette eller annullere forudbetalingen.

## <a name="to-correct-a-prepayment"></a>Sådan rettes en forudbetaling

Følgende procedure viser, hvordan du kan udstede en forudbetalingskreditnota for at annullere alle fakturerede forudbetalinger for en salgsordre.  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2. Åbn den relevante Salgsordre.
3. Vælg handlingen **Forudbetaling**, og vælg derefter handlingen **Forudbetalingskreditnota** eller handlingen **Bogfør og udskriv forudbetalingskreditnota**.  
4. På siden **Salgskreditnota** skal du fortsætte med at løse de relevante poster som for en salgskreditnota. Du kan finde flere oplysninger i [Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).  

    > [!NOTE]  
    > For at reducere beløbet i feltet **Linjebeløb** skal du først øge forudbetalingsprocenten på linjen, så værdien i feltet **Linjebeløb for forudbetaling** ikke bliver mindre end værdien i feltet **Forudbetalt beløb faktureret**.

5. Du kan oprette en forudbetalingsfaktura for en hvilken som helst ny linje i salgskreditnotaen ved at vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura** eller handlingen **Bogfør og udskriv forudbetalingsfaktura**.  
6. Hvis du vil udstede en ekstra forudbetalingsfaktura, skal du øge forudbetalingsbeløbet på en eller flere linjer og bogføre forudbetalingsfakturaen. Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløbene.  

## <a name="see-also"></a>Se også

[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Gennemgang: Opsætning og fakturering af salgsforudbetalinger](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]