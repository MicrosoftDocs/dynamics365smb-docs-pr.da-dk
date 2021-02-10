---
title: Afregne købsfakturaer omgående
description: Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du få ordnet bogføringen, når du bogfører fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 10/06/2020
ms.author: bholtorf
ms.openlocfilehash: fb442c7b1e9e7bdcb727ca6de157657e370e254f
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4746837"
---
# <a name="settle-purchase-invoices-promptly"></a>Afregne købsfakturaer omgående

Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du bogføre betalingen, når du bogfører fakturaen.  

> [!NOTE]  
> Hvis du ofte afregner købsfakturaer kontant, med check eller bankoverførsel, kan det muligvis svare sig at oprette en specifik betalingsform med en tilknyttet modkonto og angive betalingsformen i feltet **Betalingsform** på kreditorkortet. Modkontonummeret indsættes automatisk på fakturahovedet, hver gang du opretter en ny faktura. Du kan finde flere oplysninger i [Definere betalingsmetoder](finance-payment-methods.md).  

## <a name="to-settle-purchase-invoices-promptly"></a>Sådan afregnes købsfakturaer omgående

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Du kan afregne kontant eller via bankoverførsel ved at angive nummeret på finanskontoen eller bankkontoen i feltet **Modkonto**.  

> [!IMPORTANT]  
> Felterne **Modkontotype** og **Modkonto** er ikke med i standardopsætningen for et fakturahoved. Hvis du vil bogføre betalingen af en faktura, skal du kontakte en Microsoft-partner, som kan føje felterne via kode.  
>
> Denne tilpasning er kun nødvendig, hvis du ikke angiver modkonti ved betalingsmetoderne som beskrevet ovenfor.

## <a name="see-also"></a>Se også

[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
