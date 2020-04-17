---
title: Opdatere valutakurser | Microsoft Docs
description: Spore beløb i forskellige valutaer ved hjælp af valutakoder, og lad Business Central hjælpe dig med at regulere valutakursen for bogførte poster med en ekstern service.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: multiple currencies, adjust exchange rates
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 252636417dab633b8b95a15f206d1be82fc78a32
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2020
ms.locfileid: "3183184"
---
# <a name="update-currency-exchange-rates"></a>Opdatere valutakurser
Da virksomheder handler i alt flere lande, bliver det mere vigtigt, at de kan handle eller rapportere finansielle oplysninger i mere end én valuta. Du skal oprette koder for hver valuta, du bruger, hvis du foretager køb og salg i andre valutaer end din lokale valuta, eller hvis du registrerer finanstransaktioner i forskellige valutaer.

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Ved at angive en anden valuta som en såkaldt ekstra rapporteringsvaluta vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter. Du kan finde flere oplysninger i [Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md).

## <a name="adjusting-exchange-rates"></a>Regulering af valutakurser
Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives.

Kørslen **Juster valutakurser** bruges til at regulere valutakursen manuelt for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter. Du kan også få valutakurserne reguleret automatisk ved hjælp af en tjeneste. Du kan finde flere oplysninger i [Sådan konfigureres en valutakurstjeneste](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

### <a name="effect-on-customers-and-vendors"></a>Indflydelse på debitorer/kreditorer
Det gælder for debitor- og kreditorkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene i de enkelte valutaopgørelser og bogfører beløbene på den finanskonto, der er angivet i feltet **Urealiseret gevinstkonto** eller i feltet **Urealiseret tabskonto** på siden **Valutaer**. Modposteringer bogføres automatisk på samlekontoen i finansbogholderiet.

Kørslen gennemgår alle åbne debitor- og kreditorposter. Hvis der er en kursdifference for en post, oprettes der en ny detaljeret debitor- eller leverandørpost, der viser det justerede beløb i debitor- eller leverandørposten.

#### <a name="dimensions-on-customer-and-vendor-ledger-entries"></a>Dimensioner for debitor- og kreditorposter
Reguleringsposterne tildeles dimensionerne fra debitor-/kreditorposter, og reguleringerne bogføres pr. kombination af dimensionsværdier.

### <a name="effect-on-bank-accounts"></a>Indflydelse på bankkonti
Det gælder for bankkonti, at kørslen regulerer valutaen vha. den valutakurs, der er gældende på den bogføringsdato, der er angivet i kørslen. Kørslen beregner forskellene for hver bankkonto, der er blevet tildelt en valutakode, og bogfører beløbene på den finanskonto, der er angivet i feltet **Realiseret gevinstkonto** eller i feltet **Realiseret tabskonto** på siden **Valutaer**. Modposter bogføres automatisk på de finansbankkonti, der er angivet i bankbogføringsgrupperne. Kørslen beregner én post pr. valuta pr. bogføringsgruppe.

#### <a name="dimensions-on-bank-account-entries"></a>Dimensioner for bankkontoposter
Reguleringsposterne for bankkontoens finanskonto og for gevinst-/tabskontoen tildeles bankkontoens standarddimensioner.

### <a name="effect-on-gl-accounts"></a>Indflydelse på finanskonti
Hvis du bogfører i en ekstra rapporteringsvaluta, kan du bruge kørslen til at oprette nye finansposter for kursreguleringer mellem den relevante regnskabsvaluta og den ekstra rapporteringsvaluta. Kørslen beregner forskellene for hver finanspost og regulerer finansposterne, afhængigt af oplysningerne i feltet **Valutakursregulering** for hver finanskonto.

##### <a name="dimensions-on-gl-account-entries"></a>Dimensioner for finanskontoposter
Reguleringsposterne tildeles standarddimensionerne fra de konti, de bogføres på.

> [!Important]
> Før du kan bruge kørslen, skal du indtaste de kursreguleringer, som den udenlandske valutabeholdning skal reguleres efter. Det kan du gøre på siden **Valutakurser**.<br><br>  

> [!Video https://www.microsoft.com/videoplayer/embed/RE3Q24s?rel=0]

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

## <a name="see-related-training-at-microsoft-learn"></a>Se relateret oplæring på [Microsoft Learn](/learn/paths/use-multiple-currencies-dynamics-365-business-central/)

## <a name="see-also"></a>Se også
[Oprette en ekstra rapporteringsvaluta](finance-how-setup-additional-currencies.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
