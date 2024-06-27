---
title: Opsætte flere valutaer
description: 'Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), og en anden valuta er oprettet som en ekstra valuta med en aktuel valutakurs tilknyttet.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'multiple currencies, foreign exchange rates'
ms.search.form: '5, 16,118, 483, 495'
ms.date: 06/13/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-an-additional-reporting-currency"></a>Opsætte en ekstra rapporteringsvaluta

Da virksomheder handler i stadig flere lande/områder, bliver det mere vigtigt, at de kan gennemgå eller rapportere finansielle oplysninger i mere end én valuta.

> [!NOTE]  
> Hvis du leder efter realtidsoplysninger om valutakurser (FX) eller historiske kurser, omtales de som valuta i [!INCLUDE[prod_short](includes/prod_short.md)]. Foruden denne artikel, kan du også se [Opdatere valutakurser](finance-how-update-currencies.md).

Finansprogrammet er konfigureret til at bruge den lokale valuta (RV), men du kan også konfigurere det til at bruge en anden valuta med en aktuel valutakurs tilknyttet. Hvis du angiver en anden valuta som en ekstra rapporteringsvaluta (EV), registrerer [!INCLUDE[prod_short](includes/prod_short.md)] automatisk beløb i LV og EV i hver enkelt finanspost og i andre poster, f.eks. momsposter.

> [!Warning]
> Du bør ikke bruge EV-funktionen som grundlag for oversættelse af regnskabsopgørelser, medmindre du forstår dens begrænsninger. Det kan ikke oversætte udenlandske datterselskabers regnskabsopgørelser som en del af en virksomhedskonsolidering. EV må kun bruges til at udarbejde rapporter i en anden valuta, som hvis den pågældende valuta var virksomhedens LV.
>
> Du har f.eks. en stor mængde tilgodehavender i britiske pund (GBP), og du har oprettet din EV som GBP. I dette scenario reguleres beløb i de tilgodehavender, der benytter GBP, ikke for valutagevinster/-tab i EV, men kun beløbene i tilgodehavender i andre valutaer. Det betyder, at hvis du bruger EV til at rapportere dine regnskabsopgørelser, kan det medføre, at der er under-eller udestående saldi for tilgodehavender.

## <a name="displaying-reports-and-amounts-in-acy"></a>Visning af rapporter og beløb i EV

Brug af en EV kan være en hjælp i rapporteringsprocessen for en virksomhed i følgende tilfælde:

- Virksomheder i lande uden for EU, som har et højt antal transaktioner med virksomheder i EU-lande. I dette tilfælde kan virksomheder i lande/områder uden for EU også ønske at rapportere i euro for at gøre regnskabsopgørelserne mere brugbare for EU-handelspartnere.
- Virksomheder, som også ønsker at vise rapporter i en mere internationalt handlet valuta end deres egen lokale valuta.

Flere finansrapporter er baseret på finansposter. Hvis rapportdata skal vises i rapporten i EV, skal du markere feltet **Vis beløb i ekstra rapporteringsvaluta** på oversigtspanelet **Indstillinger** for den relevante finansrapport.

## <a name="adjusting-exchange-rates"></a>Valutakurser reguleres

Fordi valutakurser svinger hele tiden, skal EV i systemet reguleres med jævne mellemrum. Hvis der ikke foretages reguleringer, kan de beløb, der er konverterede fra udenlandske (eller ekstra) valutaer, og som er bogførte i regnskabet i RV være vildledende. Derudover skal daglige poster, der er bogført før, en daglig valutakurs angives i programmet, opdateres, efter at de daglige oplysninger om valutakurser angives. Kørslen **Juster valutakurser** bruges til at regulere valutakursen for bogførte kunde-, leverandør- og bankkontoposter. Det kan også opdatere EV i finansposter. Du kan finde flere oplysninger i [Opdatere valutakurser](finance-how-update-currencies.md).

## <a name="setting-up-an-acy"></a>Opsætning af en EV

Udfør disse trin for at opsætte en EV:

- Angiv finanskonti til bogføring af valutakursreguleringer  
- Angiv metoden til regulering af valutakurser for alle finanskonti.  
- Angiv metoder til regulering af valutakurser for momsposter.  
- Aktivér EV'en.  

### <a name="to-specify-general-ledger-accounts-for-posting-exchange-rate-adjustments"></a>Angiv finanskonti til bogføring af valutakursreguleringer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **valutaer**, og vælg derefter det relaterede link.  
2. På siden **Valutaer** skal du udfylde følgende felter for EV.  

|Felt|Beskrivelse|  
|---------------------------------|---------------------------------------|  
|**Realiseret finansgevinstkonto**|Den finanskonto, hvor kursgevinster skal bogføres for kursreguleringer mellem LV og EV bliver bogført.|  
|**Realiseret finanstabskonto**|Den finanskonto, hvor kursgevinster skal bogføres for kurstab mellem LV og EV bliver bogført.|  
|**Afrundingskonto (gevinst)**|Den finanskonto, hvor positive afrundingsbeløb bogføres, hvis du bogfører i modulet Finans i både LV og EV.|  
|**Afrundingskonto (tab)**|Den finanskonto, hvor restbeløb, der er tab, bogføres, hvis du bogfører i modulet Finans i både LV og EV.|

> [!NOTE]  
> Restbeløb kan opstå, når [!INCLUDE[prod_short](includes/prod_short.md)] afrunder de debet- og kreditbeløb, som er blevet konverteret fra LV til en EV.  

For hver enkelt finanskonto skal du angive, hvordan bogførte beløb for kontoen skal reguleres, så der tages hensyn til udsving i valutakurserne mellem LV og EV.  

### <a name="to-specify-the-exchange-rate-adjustment-method-for-all-general-ledger-accounts"></a>Sådan angives metoden til regulering af valutakurser for alle finanskonti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. På siden **Kontoplan** skal du vælge den relevante konto og derefter vælge handlingen **Rediger**.  
3. På siden **Finanskort** skal du vælge den relevante metode i feltet **Valutakursregulering**.  

    Hvis du bogfører i en EV, skal du i feltet **Valutakursregulering** angive, hvordan denne finanskonto reguleres for kursudsving mellem LV og EV. Den følgende tabel beskriver indstillingerne.  

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Ingen regulering**|Der foretages ingen kursregulering af finanskontoen. Denne indstilling er standardvalget.<br /><br /> **BEMÆRK:** Vælg denne indstilling, hvis valutakursen mellem LV og EV altid er fast.|  
    |**Reguler beløb**|RV-beløbet reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Beløb** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  
    |**Reguler ekstra valutabeløb**|EV reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Ekstra valuta (beløb)** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  

    Gevinst og tab på valutakursudsving bliver bogført, når du udfører kørslen **Kursreguler valutabeholdninger**. I denne kørsel findes reguleringskursen på siden **Valutakurser**, og derefter sammenlignes beløbet i felterne **Beløb** og **Ekstra valuta (beløb)** på finansposten for at fastslå, om der foreligger et kurstab eller en kursgevinst. Kørslen bruger den mulighed, du har valgt i feltet **Valutakursregulering**, til at bestemme, hvordan kursgevinster eller -tab på finanskonti skal beregnes og bogføres.  

4.  Luk siden **Finanskort**.  

### <a name="to-specify-exchange-rate-adjustment-method-for-vat-entries"></a>Sådan angives metoder til regulering af valutakurser for momsposter

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. På siden **Opsætning af Finans** skal du vælge den relevante metode i feltet **Valutakursregulering (moms)**.  
3. Hvis du bogfører i en EV, kan du i feltet **Valutakursregulering (moms)** angive, hvordan kontiene til momsbogføring på siden **Momsbogføringsopsætning** skal reguleres for kursudsving mellem LV og EV.  

    Når du aktiverer kørslen **Kursreguler valutabeholdninger**, findes reguleringskursen på siden **Valutakurs**, og derefter sammenlignes beløbene i felterne **Beløb** og **Ekstra valuta (beløb)** på momsposten for at fastslå, om der foreligger et kurstab eller en kursgevinst. Kørslen bruger den mulighed, du har valgt i dette felt, til at bestemme, hvordan kursgevinster eller -tab på momsposter skal bogføres.  

    Du har de samme indstillinger som ved finansposter, men i dette tilfælde vil reguleringerne udføres på momsposterne. Den følgende tabel beskriver indstillingerne.

    |Felt|Beskrivelse|  
    |----------------------------------|---------------------------------------|  
    |**Ingen regulering**|Der foretages ingen kursregulering af finanskontoen. Denne indstilling er standardvalget.|  
    |**Reguler beløb**|LV-beløbet reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Beløb** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  
    |**Reguler ekstra valutabeløb**|EV reguleres for alle kursgevinster eller -tab. Valutakursgevinster eller -tab bogføres i finanskontoen i feltet **Ekstra valuta (beløb)** og i de konti, du angav til gevinster eller tab, i felterne **Realiseret finansgevinstkonto** og **Realiseret finanstabskonto** på siden **Valutaer**.|  

### <a name="to-activate-the-acy"></a>Sådan aktiverer du EV'en

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. På siden **Regnskabsopsætning** skal du i feltet **Ekstra rapporteringsvaluta** vælge den ekstra valuta, du vil rapportere i.  
3. Når du forlader feltet [!INCLUDE[prod_short](includes/prod_short.md)], vises en bekræftelsesmeddelelse, der beskriver konsekvensen af at aktivere EV'en.  
4. Tryk på knappen **Ja** for at bekræfte, at du vil aktivere valutaen.  
5. Batchjobbet **Reguler eks. rapport.valuta** åbnes.

    Kørslen konverterer LV-beløb i eksisterende poster til EV'en. Der bruges en standardvalutakurs i kørslen, som kopieres fra den valutakurs, der er gyldig på arbejdsdagen på siden **Valutakurser**. De afrundingsbeløb, som opstår ved konvertering af LV til EV, bogføres i de konti til afrundingsgevinst og -tab, der er angivet på siden **Valutaer**. Bogføringsdatoen og bilagsnummeret for disse poster er de samme som for den oprindelige finanspost. Når du bogfører alle afrundingsposterne, bogføres der en afrundingspost på ultimodatoen for hvert lukket år i resultatkontoen. Denne bogføring sikrer, at slutsaldoen i resultatkontiene for hvert lukket år er 0 i både LV og EV.
6. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]      
7. Vælg **OK** for at eksekvere kørslen.  

Når du har udført kørslen, vises beløb i de følgende eksisterende poster i både LV og EV:  

- Finansposter  
- Vareudligningsposter  
- Momsposter  
- Projektfinansposter  
- Værdiposter  
- Produktionslinjer  
- Produktionsordreposter  

Derudover vil beløbene i alle fremtidige poster af samme type være registreret i både LV og EV.  

> [!NOTE]  
> Feltet **Ekstra rapporteringsvaluta** vil kun være aktiveret, efter at du har valgt knappen **OK** i kørslen **Reguler eks. rapport.valuta**.  

## <a name="see-also"></a>Se også

[Opdatere valutakurser](finance-how-update-currencies.md)  
[Lukke år og perioder](year-close-years-periods.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
