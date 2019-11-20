---
title: Sådan afregnes købsfakturaer omgående | Microsoft Docs
description: Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du få ordnet bogføringen, når du bogfører fakturaen.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: 7392ec07c59974869dce6c1e8172eb48701e1d26
ms.sourcegitcommit: 319023e53627dbe8e68643908aacc6fd594a4957
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/04/2019
ms.locfileid: "2554010"
---
# <a name="settle-purchase-invoices-promptly"></a>Afregne købsfakturaer omgående
Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du bogføre betalingen, når du bogfører fakturaen.  

### <a name="to-settle-purchase-invoices-promptly"></a>Sådan afregnes købsfakturaer omgående  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Du kan afregne kontant eller via bankoverførsel ved at angive nummeret på finanskontoen eller bankkontoen i feltet **Modkonto**.  

> [!IMPORTANT]  
>  Felterne **Modkontotype** og **Modkonto** er ikke med i standardopsætningen for et fakturahoved. Disse felter skal derfor først indsættes med designfunktionerne, for at du kan bogføre betalingen af en faktura.  

> [!NOTE]  
>  Hvis du ofte afregner købsfakturaer kontant, kan det muligvis svare sig at oprette en specifik betalingsform med en tilknyttet modkonto og angive betalingsformen i feltet **Betalingsform** på kreditorkortet. Modkontonummeret indsættes automatisk på fakturahovedet, hver gang du opretter en ny faktura.  

## <a name="see-also"></a>Se også  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
