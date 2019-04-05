---
title: Opsætning af flere valutaer | Microsoft Docs
description: Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), og en anden valuta er oprettet som en ekstra valuta med en aktuel valutakurs tilknyttet.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies
ms.date: 01/07/2019
ms.author: sgroespe
ms.openlocfilehash: 294ed8019b12287e4b4ad59d46e842e4022a637f
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2019
ms.locfileid: "792475"
---
# <a name="set-up-an-additional-reporting-currency"></a>Oprette en ekstra rapporteringsvaluta
Da virksomheder handler i stadig flere lande, bliver det mere vigtigt, at de kan gennemgå eller rapportere finansielle oplysninger i mere end én valuta.

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Ved at angive en anden valuta som en såkaldt ekstra rapporteringsvaluta vil [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk registrere beløb i både RV og i den ekstra rapporteringsvaluta i hver enkelt finanspost og i andre poster, f.eks. momsposter.

> [!Warning]
> Funktionen Ekstra rapporteringsvaluta må ikke bruges som grundlag for oversættelse af regnskabsopgørelser. Det er ikke et værktøj, som kan udføre oversættelse af udenlandske datterselskabers regnskabsopgørelser som en del af en virksomhedskonsolidering. Funktionen Ekstra regnskabsvaluta må kun bruges til at udarbejde rapporter i en anden valuta, som hvis den pågældende valuta var virksomhedens lokale valuta.

## <a name="displaying-reports-and-amounts-in-the-additional-reporting-currency"></a>Visning af rapporter og beløb i den ekstra rapporteringsvaluta
Brug af en ekstra rapporteringsvaluta kan være en hjælp i rapporteringsprocessen for en virksomhed i følgende tilfælde:

- Virksomheder i lande uden for EU, som har et højt antal transaktioner med virksomheder i EU-lande. I dette tilfælde kan virksomheder i lande uden for EU også ønske at rapportere i euro for at gøre regnskabsopgørelserne mere brugbare for EU-handelspartnere.
- Virksomheder, som også ønsker at vise rapporter i en mere internationalt handlet valuta end deres egen lokale valuta.

Flere finansrapporter er baseret på finansposter. Hvis rapportdata skal vises i rapporten i den ekstra rapporteringsvaluta, skal du blot markere feltet **Vis beløb i ekstra rapporteringsvaluta** på oversigtspanelet **Indstillinger** for den relevante finansrapport.

## <a name="adjusting-exchange-rates"></a>Regulering af valutakurser
Fordi valutakurser svinger hele tiden, skal ekstra valutaer i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives. Kørslen **Juster valutakurser** bruges til at regulere valutakursen for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere ekstra rapporteringsvalutabeløb i finansposter. Du kan finde flere oplysninger i [Opdatere valutakurser](finance-how-update-currencies.md).

## <a name="setting-up-an-additional-reporting-currency"></a>Oprette en ekstra rapporteringsvaluta.
For at konfigurere en ekstra rapporteringsvaluta, skal du følge disse trin:

-   Angiv finanskonti til bogføring af valutakursreguleringer  
-   Angiv metoden til regulering af valutakurser for alle finanskonti.  
-   Angiv metoder til regulering af valutakurser for momsposter.  
-   Aktivér den ekstra rapporteringsvaluta.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Angiv finanskonti til bogføring af valutakursreguleringer  

1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Valutaer**, og vælg derefter det relaterede link.  
2. På siden **Valutaer** skal du udfylde følgende felter for den ekstra rapporteringsvaluta.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Realiseret finansgevinstkonto**|Den finanskonto, hvor kursgevinster skal bogføres for kursreguleringer mellem regnskabsvalutaen og den ekstra rapporteringsvaluta bliver bogført.|  
|**Realiseret finanstabskonto**|Den finanskonto, hvor kurstab skal bogføres for kursreguleringer mellem regnskabsvalutaen og den ekstra rapporteringsvaluta bliver bogført.|  
|**Afrundingskonto (gevinst)**|Den finanskonto, hvor positive afrundingsbeløb bogføres, hvis du bogfører i modulet Finans i både LV og ekstra rapporteringsvaluta.|  
|**Afrundingskonto (tab)**|Den finanskonto, hvor negative afrundingsbeløb bogføres, hvis du bogfører i modulet Finans i både LV og ekstra rapporteringsvaluta.|

> [!NOTE]  
>  Der kan opstå afrundingsbeløb, når [!INCLUDE[d365fin](includes/d365fin_md.md)] afrunder de debet- og kreditbeløb, som er blevet konverteret fra RV til en ekstra rapporteringsvaluta.  

For hver enkelt finanskonto skal du angive, hvordan bogførte beløb for kontoen skal reguleres, så der tages hensyn til udsving i valutakurserne mellem RV og den ekstra rapporteringsvaluta.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Sådan angives metoden til regulering af valutakurser for alle finanskonti  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
2. På siden **Kontoplan** skal du vælge den relevante konto og derefter vælge handlingen **Rediger**.  
3. På siden **Finanskort** skal du vælge den relevante metode i feltet **Valutakursregulering**.  

    Hvis du bogfører i en ekstra rapporteringsvaluta, skal du i feltet **Valutakursregulering** angive, hvordan denne finanskonto skal reguleres for kursudsving mellem RV og den ekstra rapporteringsvaluta. Følgende tabel viser de indstillinger, du kan vælge.  

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Ingen regulering**|Der foretages ingen kursregulering af finanskontoen. Dette er standardvalget.<br /><br /> **BEMÆRK:** Denne indstilling bør vælges, hvis valutakursen mellem RV og den ekstra rapporteringsvaluta altid er den samme.|  
    |**Regul. beløb**|RV-beløbet reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Beløb** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  
    |**Regul. ekstra valutabeløb**|Den ekstra rapporteringsvaluta reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Ekstra valuta (beløb)** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  

    Gevinst og tab på valutakursudsving bliver bogført, når du udfører kørslen **Kursreguler valutabeholdninger**. I denne kørsel findes reguleringskursen på siden **Valutakurser**, og derefter sammenlignes beløbet i felterne **Beløb** og **Ekstra valuta (beløb)** på finansposten for at fastslå, om der foreligger et kurstab eller en kursgevinst. Kørslen bruger den mulighed, du har valgt i feltet **Valutakursregulering**, til at bestemme, hvordan kursgevinster eller -tab på finanskonti skal beregnes og bogføres.  

4.  Luk siden **Finanskort**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Sådan angives metoder til regulering af valutakurser for momsposter  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. På siden **Opsætning af Finans** skal du vælge den relevante metode i feltet **Valutakursregulering (moms)**.  
3. Hvis du bogfører i en ekstra rapporteringsvaluta, kan du i feltet **Valutakursregulering (moms)** angive, hvordan kontiene til momsbogføring på siden **Momsbogføringsopsætning** skal justeres for kursudsving mellem RV og den ekstra rapporteringsvaluta.  

    Når du aktiverer kørslen **Kursreguler valutabeholdninger**, findes reguleringskursen på siden **Valutakurs**, og derefter sammenlignes beløbene i felterne **Beløb** og **Ekstra valuta (beløb)** på momsposten for at fastslå, om der foreligger et kurstab eller en kursgevinst. Kørslen bruger den mulighed, du har valgt i dette felt, til at bestemme, hvordan kursgevinster eller -tab på momsposter skal bogføres.  

    Du har de samme indstillinger som ved finansposter, men i dette tilfælde vil reguleringerne udføres på momsposterne. Følgende tabel viser de indstillinger, du kan vælge.

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Ingen regulering**|Der foretages ingen kursregulering af finanskontoen. Dette er standardvalget.|  
    |**Regul. beløb**|RV-beløbet reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Beløb** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  
    |**Regul. ekstra valutabeløb**|Den ekstra rapporteringsvaluta reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Ekstra valuta (beløb)** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  

### <a name="to-activate-the-additional-reporting-currency"></a>Sådan aktiveres den ekstra rapporteringsvaluta  
1. Vælg ikonet ![Elpære, der åbner funktionen Fortæl mig](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. På siden **Regnskabsopsætning** skal du vælge feltet **Ekstra rapporteringsvaluta** for at vælge den ekstra valuta, du vil rapportere i.  
3. Når du forlader feltet, vises der via [!INCLUDE[d365fin](includes/d365fin_md.md)] en bekræftelsesmeddelelse, der beskriver konsekvensen af at aktivere den ekstra rapporteringsvaluta.  
4. Tryk på knappen **Ja** for at bekræfte, at du vil aktivere valutaen.  
5. Batchjobbet **Reguler eks. rapport.valuta** åbnes.

    Kørslen konverterer RV-beløb i eksisterende poster til den ekstra rapporteringsvaluta. Der bruges en standardvalutakurs i kørslen, som kopieres fra den valutakurs, der er gyldig på arbejdsdagen på siden **Valutakurser**. De afrundingsbeløb, som opstår ved konvertering af RV til en ekstra rapporteringsvaluta, bogføres i de konti til afrundingsgevinst og -tab, der er angivet på siden **Valutaer**. Bogføringsdatoen og bilagsnummeret for disse poster er de samme som for den oprindelige finanspost. Når alle afrundingsposterne er bogført, bogføres der en afrundingspost på ultimodatoen for hvert lukket år i resultatkontoen. Dette er for at sikre, at slutsaldoen i resultatkontiene for hvert lukket år er 0 i både RV og den ekstra rapporteringsvaluta.
6. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Vælg **OK** for at eksekvere kørslen.  

Når du har udført kørslen, vil beløb i de følgende eksisterende poster være i både RV og i den ekstra rapporteringsvaluta:  

- Finansposter  
- Vareudligningsposter  
- Momsposter  
- Sagsposter  
- Værdiposter  
- Produktionslinjer  
- Produktionsordreposter  

Derudover vil beløbene i alle fremtidige poster af samme type være registreret i både RV og den ekstra rapporteringsvaluta.  

> [!NOTE]  
>  Feltet **Ekstra rapporteringsvaluta** vil kun være aktiveret, efter at du har valgt knappen **OK** i kørslen **Reguler eks. rapport.valuta**.  

## <a name="see-also"></a>Se også
[Opdatere valutakurser](finance-how-update-currencies.md)  
[Afslutning af år og perioder](year-close-years-periods.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
