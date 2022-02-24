---
title: Sådan afregnes købsfakturaer omgående | Microsoft Docs
description: Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du få ordnet bogføringen, når du bogfører fakturaen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: bholtorf
ms.openlocfilehash: ec5723088553141c1f6df55ba8bac3303ee4e2bd
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183256"
---
# <a name="settle-purchase-invoices-promptly"></a>Afregne købsfakturaer omgående
Hvis det er nødvendigt at betale kreditoren kontant eller med check, kan du bogføre betalingen, når du bogfører fakturaen.  

### <a name="to-settle-purchase-invoices-promptly"></a>Sådan afregnes købsfakturaer omgående  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3.  Du kan afregne kontant eller via bankoverførsel ved at angive nummeret på finanskontoen eller bankkontoen i feltet **Modkonto**.  

> [!IMPORTANT]  
>  Felterne **Modkontotype** og **Modkonto** er ikke med i standardopsætningen for et fakturahoved. Disse felter skal derfor først indsættes med designfunktionerne, for at du kan bogføre betalingen af en faktura. Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md). 

> [!NOTE]  
>  Hvis du ofte afregner købsfakturaer kontant, kan det muligvis svare sig at oprette en specifik betalingsform med en tilknyttet modkonto og angive betalingsformen i feltet **Betalingsform** på kreditorkortet. Modkontonummeret indsættes automatisk på fakturahovedet, hver gang du opretter en ny faktura.  

## <a name="see-also"></a>Se også  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
