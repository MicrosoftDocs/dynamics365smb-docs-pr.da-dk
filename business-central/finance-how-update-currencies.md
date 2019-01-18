---
title: Opdatere valutakurser | Microsoft Docs
description: Hvis du vil bruge flere forskellige valutaer i virksomheden, skal du angive en kode for hver valuta og bruge en ekstern valutakurstjeneste, som FloatRates.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 23940bd1e5fd29dc92e8285c08679135889701e9
ms.contentlocale: da-dk
ms.lasthandoff: 11/26/2018

---
# <a name="update-currency-exchange-rates"></a>Opdatere valutakurser
Du skal oprette koder for hver valuta, du bruger, hvis du foretager køb og salg i andre valutaer end din lokale valuta, eller hvis du registrerer finanstransaktioner i forskellige valutaer.  

Da virksomheder handler i alt flere lande, bliver det mere vigtigt, at de kan gennemgå eller rapportere finansielle oplysninger i mere end én valuta. Programmet understøtter brug af flere valutaer. I programmet er finansposterne oprettet i den lokale valuta (RV), og en anden valuta er oprettet som en ekstra valuta med en aktuel valutakurs tilknyttet.  

 Ved at angive en anden valuta som en ekstra rapporteringsvaluta vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, som f.eks. momsposter. Når der beregnes beløb i finansposter i en ekstra rapporteringsvaluta, anvendes oplysningerne på siden **Valutakurser** til at finde den relevante valutakurs.  

> [!WARNING]  
>  Funktionen Ekstra rapporteringsvaluta må IKKE bruges som grundlag for oversættelse af regnskabsopgørelser. Det er ikke et værktøj, som kan udføre oversættelse af udenlandske datterselskabers regnskabsopgørelser som en del af en virksomhedskonsolidering. Funktionen Ekstra regnskabsvaluta giver kun mulighed for at udarbejde rapporter i en anden valuta, som hvis den valuta var virksomhedens lokale valuta.

## <a name="adjusting-exchange-rates"></a>Regulering af valutakurser  
Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives. Kørslen Juster valutakurser bruges til at regulere valutakursen for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter.  

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visning af rapporter og beløb i den ekstra rapporteringsvaluta  
Brug af en ekstra rapporteringsvaluta kan være en hjælp i rapporteringsprocessen for en virksomhed i følgende tilfælde:  

- Virksomheder i lande uden for EU, som har et højt antal transaktioner med virksomheder i EU-lande. I dette tilfælde kan virksomheder i lande uden for EU også ønske at rapportere i euro for at gøre regnskabsopgørelserne mere brugbare for deres EU-handelspartnere.  

- Virksomheder, som også ønsker at vise rapporter i en mere internationalt handlet valuta end deres egen lokale valuta.  

Flere rapporter i modulet Finanser baseret på finansposter. Hvis finansielle data skal vises i rapporten i den ekstra rapporteringsvaluta, skal du blot vælge feltet **Vis i ekstra valuta** på siden for den relevante finansrapport.  

## <a name="to-set-up-a-currency-exchange-rate-service"></a>Sådan konfigureres en valutakurstjeneste
Du kan bruge en ekstern tjeneste til at holde dine valutakurser opdateret, f.eks. FloatRates.

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutakurstjenester**, og vælg derefter det relaterede link.
2. Vælg handlingen **Ny**.
3. På siden **Valutakurstjenester** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Marker afkrydsningsfeltet **Aktiveret** for at aktivere tjenesten.

## <a name="to-update-currency-exchange-rates-through-a-service"></a>Sådan opdateres valutakurser fra en tjeneste
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutaer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Opdater valutakurser**.

Værdien i feltet **Valutakurs** på siden **Valutaer** opdateres med den seneste valutakurs.

## <a name="see-also"></a>Se også
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

